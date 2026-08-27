# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\4-IssuedChecksSmoke.spec.ts >> Issued Checks — Smoke (Continued) >> "View" (Change Log) link on a row navigates to the entity log
- Location: specs\Smoke\4-IssuedChecksSmoke.spec.ts:334:5

# Error details

```
TimeoutError: locator.waitFor: Timeout 20000ms exceeded.
Call log:
  - waiting for locator('//span[text()="Home"]') to be visible

```

# Page snapshot

```yaml
- generic [ref=e1]:
  - main [ref=e2]:
    - heading [level=1] [ref=e4]
    - generic [ref=e7]:
      - generic [ref=e9]:
        - generic: Email *
        - textbox "Email Address" [ref=e10]: pjakati28+PP@gmail.com
      - generic [ref=e12]:
        - generic: Password *
        - textbox "Password" [ref=e13]: Password123!
      - button "Login to Positive Pay" [active] [ref=e15] [cursor=pointer]
      - link "Forgot Password?" [ref=e17] [cursor=pointer]:
        - /url: /forgot-password/
  - heading [level=5] [ref=e19]:
    - text: Could not reconnect to the server.
    - link "Reload" [ref=e20] [cursor=pointer]:
      - /url: ""
    - text: the page to restore functionality.
```

# Test source

```ts
  122 |     test.beforeEach(async ({ pageManager }) => {
  123 |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  124 |         await pageManager.loginPage.login(
  125 |             Constants.USER_FI_EMAIL,
  126 |             Constants.USER_FI_PASSWORD
  127 |         );
  128 |         await pageManager.homePage.homePageLogo.waitFor({ state: 'visible', timeout: 20000 });
  129 |         await pageManager.issuedChecksPage.navigateToIssuedChecks();
  130 |         await pageManager.issuedChecksPage.waitForGridLoad();
  131 |     });
  132 | 
  133 |     // Safety net: the preset created below is Default (account-global). If an assertion
  134 |     // fails before cleanup, afterEach removes every SMK_ preset so it can't poison later runs.
  135 |     let pendingFilterPresetCleanup: string | undefined;
  136 | 
  137 |     test.afterEach(async ({ page, pageManager }) => {
  138 |         if (!pendingFilterPresetCleanup) return;
  139 |         pendingFilterPresetCleanup = undefined;
  140 | 
  141 |         await pageManager.issuedChecksPage.navigateToIssuedChecks();
  142 |         await purgeSavedFilterPresets(page, {
  143 |             dropdown: pageManager.issuedChecksPage.savedFiltersDropdown,
  144 |             deleteButton: pageManager.issuedChecksPage.deleteSavedFilterButton,
  145 |             confirmDialog: pageManager.issuedChecksPage.confirmDialog,
  146 |             confirmButton: pageManager.issuedChecksPage.confirmDialogConfirmButton,
  147 |         });
  148 |     });
  149 | 
  150 |     test('Default filter auto-applies after logout and re-login', async ({ pageManager, page }, testInfo) => {
  151 |         // The default filter is account-global and shared by every browser on the same login.
  152 |         // Run on one browser only so concurrent projects can't collide on it (local 4-browser
  153 |         // runs and the pipeline's 4 parallel browser jobs share the same account).
  154 |         test.skip(testInfo.project.name !== 'chromium', 'Shared-account default filter runs on chromium only.');
  155 |         const logoutPage = new LogoutPage(page);
  156 | 
  157 |         // Sample the Check # from the first grid row and apply a column filter.
  158 |         const checkNo = (await pageManager.issuedChecksPage.gridRows.first()
  159 |             .locator('td').nth(6).innerText()).trim();
  160 | 
  161 |         await pageManager.issuedChecksPage.columnFilterButton('Check #').click();
  162 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeVisible();
  163 |         const filterInput = pageManager.issuedChecksPage.columnFilterPopup
  164 |             .locator('input[role="spinbutton"], input[type="text"], input.k-input-inner').first();
  165 |         await filterInput.fill(checkNo);
  166 |         await filterInput.press('Tab');
  167 |         await pageManager.issuedChecksPage.columnFilterApplyButton.click();
  168 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  169 | 
  170 |         const filteredPagerState = ((await pageManager.issuedChecksPage.paginationInfo.textContent()) ?? '')
  171 |             .replace(/\s+/g, ' ')
  172 |             .trim();
  173 | 
  174 |         // Save the active filter as a named preset and mark it as Default.
  175 |         const presetName = `SMK_Default_${Date.now()}`;
  176 |         await pageManager.issuedChecksPage.saveCurrentFilterAs(presetName, { asDefault: true });
  177 |         // Default preset now exists on the shared env — afterEach removes it even if we fail below.
  178 |         pendingFilterPresetCleanup = presetName;
  179 | 
  180 |         // Logout.
  181 |         await logoutPage.ACCOUNTNAME_TEXT.click();
  182 |         await logoutPage.LOGOUT_TEXT.click();
  183 |         await page.waitForURL(/\/auth\/(login|logout)/, { timeout: 15000 });
  184 | 
  185 |         // Login again.
  186 |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  187 |         await pageManager.loginPage.login(
  188 |             Constants.USER_FI_EMAIL,
  189 |             Constants.USER_FI_PASSWORD
  190 |         );
  191 |         await pageManager.homePage.homePageLogo.waitFor({ state: 'visible', timeout: 20000 });
  192 | 
  193 |         // Navigate to Issued Checks — the default preset should auto-apply.
  194 |         await pageManager.issuedChecksPage.navigateToIssuedChecks();
  195 |         await pageManager.issuedChecksPage.waitForGridLoad();
  196 | 
  197 |         await expect.poll(
  198 |             async () => pageManager.issuedChecksPage.savedFiltersDropdown.inputValue(),
  199 |             { timeout: 15000 }
  200 |         ).toBe(presetName);
  201 |         await expect.poll(
  202 |             async () => ((await pageManager.issuedChecksPage.paginationInfo.textContent()) ?? '')
  203 |                 .replace(/\s+/g, ' ')
  204 |                 .trim(),
  205 |             { timeout: 10000 }
  206 |         ).toBe(filteredPagerState);
  207 | 
  208 |         // Cleanup (delete the Default preset) runs in afterEach via pendingFilterPresetCleanup.
  209 |     });
  210 | 
  211 | });
  212 | 
  213 | // Resume regular parallel execution for remaining tests
  214 | test.describe('Issued Checks — Smoke (Continued)', () => {
  215 | 
  216 |     test.beforeEach(async ({ pageManager }) => {
  217 |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  218 |         await pageManager.loginPage.login(
  219 |             Constants.USER_FI_EMAIL,
  220 |             Constants.USER_FI_PASSWORD
  221 |         );
> 222 |         await pageManager.homePage.homePageLogo.waitFor({ state: 'visible', timeout: 20000 });
      |                                                 ^ TimeoutError: locator.waitFor: Timeout 20000ms exceeded.
  223 |         await pageManager.issuedChecksPage.navigateToIssuedChecks();
  224 |         await pageManager.issuedChecksPage.waitForGridLoad();
  225 |     });
  226 | 
  227 |     // Safety net for the preset created below (non-default). afterEach removes any SMK_ preset
  228 |     // if an assertion fails before the inline delete runs.
  229 |     let pendingFilterPresetCleanup: string | undefined;
  230 | 
  231 |     test.afterEach(async ({ page, pageManager }) => {
  232 |         if (!pendingFilterPresetCleanup) return;
  233 |         pendingFilterPresetCleanup = undefined;
  234 | 
  235 |         await pageManager.issuedChecksPage.navigateToIssuedChecks();
  236 |         await purgeSavedFilterPresets(page, {
  237 |             dropdown: pageManager.issuedChecksPage.savedFiltersDropdown,
  238 |             deleteButton: pageManager.issuedChecksPage.deleteSavedFilterButton,
  239 |             confirmDialog: pageManager.issuedChecksPage.confirmDialog,
  240 |             confirmButton: pageManager.issuedChecksPage.confirmDialogConfirmButton,
  241 |         });
  242 |     });
  243 | 
  244 |     test('Save a filter preset, verify it is auto-selected, then delete it', async ({ pageManager }) => {
  245 |         // Sample the Check # from the first grid row to use as the filter value.
  246 |         // Check # is the 7th column (td index 6) in the default column order.
  247 |         const checkNo = (await pageManager.issuedChecksPage.gridRows.first()
  248 |             .locator('td').nth(6).innerText()).trim();
  249 | 
  250 |         // Apply a column filter on Check # using the sampled value.
  251 |         await pageManager.issuedChecksPage.columnFilterButton('Check #').click();
  252 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeVisible();
  253 |         const filterInput = pageManager.issuedChecksPage.columnFilterPopup
  254 |             .locator('input[role="spinbutton"]:visible').first();
  255 |         await filterInput.fill(checkNo);
  256 |         await filterInput.press('Tab');
  257 |         await pageManager.issuedChecksPage.columnFilterApplyButton.click();
  258 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  259 | 
  260 |         // Save the active column filter as a named preset.
  261 |         const presetName = `SMK_Check_${Date.now()}`;
  262 |         await pageManager.issuedChecksPage.saveCurrentFilterAs(presetName);
  263 |         // Preset now exists on the shared env — afterEach removes it if we fail before deleting.
  264 |         pendingFilterPresetCleanup = presetName;
  265 | 
  266 |         // The dropdown should auto-select the newly saved preset.
  267 |         await expect(pageManager.issuedChecksPage.savedFiltersDropdown).toHaveValue(presetName, { timeout: 10000 });
  268 | 
  269 |         // Delete IS the assertion under test, so it stays inline (not moved to afterEach).
  270 |         await expect(pageManager.issuedChecksPage.deleteSavedFilterButton).toBeVisible();
  271 |         await pageManager.issuedChecksPage.deleteSavedFilterButton.click();
  272 |         await expect(pageManager.issuedChecksPage.confirmDialog).toBeVisible();
  273 |         await pageManager.issuedChecksPage.confirmDialogConfirmButton.click();
  274 |         await expect(pageManager.issuedChecksPage.confirmDialog).toBeHidden({ timeout: 10000 });
  275 |         await expect.poll(
  276 |             async () => pageManager.issuedChecksPage.savedFiltersDropdown.locator('option').allInnerTexts(),
  277 |             { timeout: 10000 }
  278 |         ).not.toContain(presetName);
  279 |         pendingFilterPresetCleanup = undefined; // deleted inline above
  280 |     });
  281 | 
  282 |     // ── Column sort ───────────────────────────────────────────────────────────
  283 | 
  284 |     test('Clicking a column header sorts ascending, clicking again sorts descending', async ({ pageManager, page }) => {
  285 |         // Click the sortable title text inside the Check # column header (not the filter button)
  286 |         await pageManager.issuedChecksPage.columnHeaderCheckNumber.getByText('Check #', { exact: true }).click();
  287 |         await expect(page.getByRole('columnheader', { name: 'Sorted in ascending order' }))
  288 |             .toBeVisible({ timeout: 10000 });
  289 | 
  290 |         await page.getByRole('columnheader', { name: 'Sorted in ascending order' })
  291 |             .getByText('Check #', { exact: true }).click();
  292 |         await expect(page.getByRole('columnheader', { name: 'Sorted in descending order' }))
  293 |             .toBeVisible({ timeout: 10000 });
  294 |     });
  295 | 
  296 |     // ── Column filter ─────────────────────────────────────────────────────────
  297 | 
  298 |     test('Column filter popup applies a filter and Clear restores the full row set', async ({ pageManager }) => {
  299 |         const baseline = await pageManager.issuedChecksPage.gridRows.count();
  300 |         // Check # is at td index 6 in the default column order
  301 |         const checkNo = (await pageManager.issuedChecksPage.gridRows.first().locator('td').nth(6).innerText()).trim();
  302 | 
  303 |         await pageManager.issuedChecksPage.columnFilterButton('Check #').click();
  304 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeVisible();
  305 |         const input = pageManager.issuedChecksPage.columnFilterPopup
  306 |             .locator('input[role="spinbutton"]:visible').first();
  307 |         await input.fill(checkNo);
  308 |         await input.press('Tab');
  309 |         await pageManager.issuedChecksPage.columnFilterApplyButton.click();
  310 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  311 |         await expect(pageManager.issuedChecksPage.gridRows.first()).toBeVisible({ timeout: 10000 });
  312 | 
  313 |         // Clear the filter and verify baseline is restored
  314 |         await pageManager.issuedChecksPage.columnFilterButton('Check #').click();
  315 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeVisible();
  316 |         await pageManager.issuedChecksPage.columnFilterClearButton.click();
  317 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  318 |         await expect.poll(async () => pageManager.issuedChecksPage.gridRows.count(), { timeout: 10000 })
  319 |             .toBe(baseline);
  320 |     });
  321 | 
  322 |     // ── Row actions ───────────────────────────────────────────────────────────
```