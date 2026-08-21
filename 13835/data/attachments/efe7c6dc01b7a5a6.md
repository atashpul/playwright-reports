# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\4-IssuedChecksSmoke.spec.ts >> Issued Checks — Smoke (Continued) >> Save a filter preset, verify it is auto-selected, then delete it
- Location: specs\Smoke\4-IssuedChecksSmoke.spec.ts:212:5

# Error details

```
Error: expect(locator).toBeVisible() failed

Locator: locator('.k-grid-filter-popup:visible, [aria-label$="Filter Menu"]:visible, .k-animation-container:visible:has(.k-filter-menu-container)').first()
Expected: visible
Timeout: 30000ms
Error: element(s) not found

Call log:
  - Expect "toBeVisible" with timeout 30000ms
  - waiting for locator('.k-grid-filter-popup:visible, [aria-label$="Filter Menu"]:visible, .k-animation-container:visible:has(.k-filter-menu-container)').first()

```

```yaml
- banner:
  - link:
    - /url: /
    - img
  - link "  Home":
    - /url: /
  - link "  Issued Checks":
    - /url: /issued-checks
  - link "  Presented Checks":
    - /url: /paid-checks
  - link "  Teller":
    - /url: /teller
  - link "  ACH":
    - /url: /paid-ach
  - link "  Exceptions 8":
    - /url: /exceptions
  - link "  Settings":
    - /url: /client-admin
  - button "  F.I ACH&CHK User"
- list:
  - listitem:
    - link " ":
      - /url: /
  - listitem:
    - link "Issued Checks":
      - /url: /issued-checks
- group:
  - link " Uploaded Checks":
    - /url: /issued-checks/uploads
  - link "+ Add Check":
    - /url: /issued-checks/add-check
- toolbar "Grid toolbar":
  - text: Page Size
  - combobox:
    - option "10"
    - option "20" [selected]
    - option "50"
    - option "100"
  - button "Excel"
  - textbox "Search..."
  - text: Saved Filters
  - combobox:
    - option "[No Filter]"
    - option "SMK_Default_1786639509984"
    - option "SMK_Default_1786640788412"
    - option "SMK_Default_1786634840447"
    - option "SMK_Default_1786636722599"
    - option "SMK_Default_1786636837156"
    - option "SMK_Default_1787334161323"
    - option "SMK_Default_1787338791555" [selected]
  - button ""
  - button ""
- grid "Data table":
  - rowgroup:
    - 'row "Client Client column filter menu settings Presented Check Presented Check column filter menu settings Account Account column filter menu settings Reference ID Reference ID column filter menu settings Routing # Routing # column filter menu settings Account # Account # column filter menu settings Check # Check # column filter menu settings Amount Amount column filter menu settings Issue Date Issue Date column filter menu settings Payee Name Payee Name column filter menu settings Stop Payment? Stop Payment? column filter menu settings Voided Check? Voided Check? column filter menu settings ID ID column filter menu settings Added By Added By column filter menu settings Edit Change Log"':
      - columnheader "Client Client column filter menu settings":
        - text: Client
        - button "Client column filter menu settings"
      - columnheader "Presented Check Presented Check column filter menu settings":
        - text: Presented Check
        - button "Presented Check column filter menu settings"
      - columnheader "Account Account column filter menu settings":
        - text: Account
        - button "Account column filter menu settings"
      - columnheader "Reference ID Reference ID column filter menu settings":
        - text: Reference ID
        - button "Reference ID column filter menu settings"
      - 'columnheader "Routing # Routing # column filter menu settings"':
        - text: "Routing #"
        - 'button "Routing # column filter menu settings"'
      - 'columnheader "Account # Account # column filter menu settings"':
        - text: "Account #"
        - 'button "Account # column filter menu settings"'
      - 'columnheader "Check # Check # column filter menu settings"':
        - text: "Check #"
        - 'button "Check # column filter menu settings"'
      - columnheader "Amount Amount column filter menu settings":
        - text: Amount
        - button "Amount column filter menu settings"
      - columnheader "Issue Date Issue Date column filter menu settings":
        - text: Issue Date
        - button "Issue Date column filter menu settings"
      - columnheader "Payee Name Payee Name column filter menu settings":
        - text: Payee Name
        - button "Payee Name column filter menu settings"
      - columnheader "Stop Payment? Stop Payment? column filter menu settings":
        - text: Stop Payment?
        - button "Stop Payment? column filter menu settings"
      - columnheader "Voided Check? Voided Check? column filter menu settings":
        - text: Voided Check?
        - button "Voided Check? column filter menu settings"
      - columnheader "ID ID column filter menu settings":
        - text: ID
        - button "ID column filter menu settings"
      - columnheader "Added By Added By column filter menu settings":
        - text: Added By
        - button "Added By column filter menu settings"
      - columnheader "Edit"
      - columnheader "Change Log"
  - rowgroup:
    - row "PJ_BC_Boutique(Both) Account14 Exlid777 063110047 10047 999256 $430.50 08/20/2026  No  No 9971 IssuedCheck_FixedLength_Malformed.txt  Edit  Delete View ":
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell
      - gridcell "Account14"
      - gridcell "Exlid777"
      - gridcell "063110047"
      - gridcell "10047"
      - gridcell "999256"
      - gridcell "$430.50"
      - gridcell "08/20/2026"
      - gridcell
      - gridcell " No"
      - gridcell " No"
      - gridcell "9971"
      - gridcell "IssuedCheck_FixedLength_Malformed.txt":
        - link "IssuedCheck_FixedLength_Malformed.txt":
          - /url: /issued-checks/uploads?Id=15557
      - gridcell " Edit  Delete":
        - link " Edit":
          - /url: /issued-checks/check/9971
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=IssuedCheck&EntityId=9971&ReturnUrl=%2fissued-checks
- application "Page navigation, page 1 of 1":
  - button "Go to the first page" [disabled]
  - button "Go to the previous page" [disabled]
  - text: Page
  - spinbutton "Select a page": "1"
  - text: of 1
  - button "Go to the next page" [disabled]
  - button "Go to the last page" [disabled]
  - text: 1 - 1 of 1 items
- contentinfo:
  - text: PJ_FI_Bank (Playwright Automation)[uat-release] © Copyright Advanced Fraud Solutions 2005-2026 | All Rights Reserved |
  - link "Privacy Policy":
    - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  120 | 
  121 |     test.beforeEach(async ({ pageManager }) => {
  122 |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  123 |         await pageManager.loginPage.login(
  124 |             Constants.USER_FI_EMAIL,
  125 |             Constants.USER_FI_PASSWORD
  126 |         );
  127 |         await pageManager.homePage.homePageLogo.waitFor({ state: 'visible', timeout: 20000 });
  128 |         await pageManager.issuedChecksPage.navigateToIssuedChecks();
  129 |         await pageManager.issuedChecksPage.waitForGridLoad();
  130 |     });
  131 | 
  132 |     test('Default filter auto-applies after logout and re-login', async ({ pageManager, page }) => {
  133 |         const logoutPage = new LogoutPage(page);
  134 | 
  135 |         // Sample the Check # from the first grid row and apply a column filter.
  136 |         const checkNo = (await pageManager.issuedChecksPage.gridRows.first()
  137 |             .locator('td').nth(6).innerText()).trim();
  138 | 
  139 |         await pageManager.issuedChecksPage.columnFilterButton('Check #').click();
  140 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeVisible();
  141 |         const filterInput = pageManager.issuedChecksPage.columnFilterPopup
  142 |             .locator('input[role="spinbutton"], input[type="text"], input.k-input-inner').first();
  143 |         await filterInput.fill(checkNo);
  144 |         await filterInput.press('Tab');
  145 |         await pageManager.issuedChecksPage.columnFilterApplyButton.click();
  146 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  147 | 
  148 |         const filteredPagerState = ((await pageManager.issuedChecksPage.paginationInfo.textContent()) ?? '')
  149 |             .replace(/\s+/g, ' ')
  150 |             .trim();
  151 | 
  152 |         // Save the active filter as a named preset and mark it as Default.
  153 |         const presetName = `SMK_Default_${Date.now()}`;
  154 |         await pageManager.issuedChecksPage.saveCurrentFilterAs(presetName, { asDefault: true });
  155 | 
  156 |         // Logout.
  157 |         await logoutPage.ACCOUNTNAME_TEXT.click();
  158 |         await logoutPage.LOGOUT_TEXT.click();
  159 |         await page.waitForURL(/\/auth\/(login|logout)/, { timeout: 15000 });
  160 | 
  161 |         // Login again.
  162 |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  163 |         await pageManager.loginPage.login(
  164 |             Constants.USER_FI_EMAIL,
  165 |             Constants.USER_FI_PASSWORD
  166 |         );
  167 |         await pageManager.homePage.homePageLogo.waitFor({ state: 'visible', timeout: 20000 });
  168 | 
  169 |         // Navigate to Issued Checks — the default preset should auto-apply.
  170 |         await pageManager.issuedChecksPage.navigateToIssuedChecks();
  171 |         await pageManager.issuedChecksPage.waitForGridLoad();
  172 | 
  173 |         await expect.poll(
  174 |             async () => pageManager.issuedChecksPage.savedFiltersDropdown.inputValue(),
  175 |             { timeout: 15000 }
  176 |         ).toBe(presetName);
  177 |         await expect.poll(
  178 |             async () => ((await pageManager.issuedChecksPage.paginationInfo.textContent()) ?? '')
  179 |                 .replace(/\s+/g, ' ')
  180 |                 .trim(),
  181 |             { timeout: 10000 }
  182 |         ).toBe(filteredPagerState);
  183 | 
  184 |         // Cleanup: delete the default preset.
  185 |         await expect(pageManager.issuedChecksPage.deleteSavedFilterButton).toBeVisible();
  186 |         await pageManager.issuedChecksPage.deleteSavedFilterButton.click();
  187 |         await expect(pageManager.issuedChecksPage.confirmDialog).toBeVisible();
  188 |         await pageManager.issuedChecksPage.confirmDialogConfirmButton.click();
  189 |         await expect(pageManager.issuedChecksPage.confirmDialog).toBeHidden({ timeout: 10000 });
  190 |         await expect.poll(
  191 |             async () => pageManager.issuedChecksPage.savedFiltersDropdown.locator('option').allInnerTexts(),
  192 |             { timeout: 10000 }
  193 |         ).not.toContain(presetName);
  194 |     });
  195 | 
  196 | });
  197 | 
  198 | // Resume regular parallel execution for remaining tests
  199 | test.describe('Issued Checks — Smoke (Continued)', () => {
  200 | 
  201 |     test.beforeEach(async ({ pageManager }) => {
  202 |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  203 |         await pageManager.loginPage.login(
  204 |             Constants.USER_FI_EMAIL,
  205 |             Constants.USER_FI_PASSWORD
  206 |         );
  207 |         await pageManager.homePage.homePageLogo.waitFor({ state: 'visible', timeout: 20000 });
  208 |         await pageManager.issuedChecksPage.navigateToIssuedChecks();
  209 |         await pageManager.issuedChecksPage.waitForGridLoad();
  210 |     });
  211 | 
  212 |     test('Save a filter preset, verify it is auto-selected, then delete it', async ({ pageManager }) => {
  213 |         // Sample the Check # from the first grid row to use as the filter value.
  214 |         // Check # is the 7th column (td index 6) in the default column order.
  215 |         const checkNo = (await pageManager.issuedChecksPage.gridRows.first()
  216 |             .locator('td').nth(6).innerText()).trim();
  217 | 
  218 |         // Apply a column filter on Check # using the sampled value.
  219 |         await pageManager.issuedChecksPage.columnFilterButton('Check #').click();
> 220 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeVisible();
      |                                                                      ^ Error: expect(locator).toBeVisible() failed
  221 |         const filterInput = pageManager.issuedChecksPage.columnFilterPopup
  222 |             .locator('input[role="spinbutton"]:visible').first();
  223 |         await filterInput.fill(checkNo);
  224 |         await filterInput.press('Tab');
  225 |         await pageManager.issuedChecksPage.columnFilterApplyButton.click();
  226 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  227 | 
  228 |         // Save the active column filter as a named preset.
  229 |         const presetName = `SMK_Check_${Date.now()}`;
  230 |         await pageManager.issuedChecksPage.saveCurrentFilterAs(presetName);
  231 | 
  232 |         // The dropdown should auto-select the newly saved preset.
  233 |         await expect(pageManager.issuedChecksPage.savedFiltersDropdown).toHaveValue(presetName, { timeout: 10000 });
  234 | 
  235 |         // Cleanup: select the preset (delete button only appears when one is selected), delete it.
  236 |         await expect(pageManager.issuedChecksPage.deleteSavedFilterButton).toBeVisible();
  237 |         await pageManager.issuedChecksPage.deleteSavedFilterButton.click();
  238 |         await expect(pageManager.issuedChecksPage.confirmDialog).toBeVisible();
  239 |         await pageManager.issuedChecksPage.confirmDialogConfirmButton.click();
  240 |         await expect(pageManager.issuedChecksPage.confirmDialog).toBeHidden({ timeout: 10000 });
  241 |         await expect.poll(
  242 |             async () => pageManager.issuedChecksPage.savedFiltersDropdown.locator('option').allInnerTexts(),
  243 |             { timeout: 10000 }
  244 |         ).not.toContain(presetName);
  245 |     });
  246 | 
  247 |     // ── Column sort ───────────────────────────────────────────────────────────
  248 | 
  249 |     test('Clicking a column header sorts ascending, clicking again sorts descending', async ({ pageManager, page }) => {
  250 |         // Click the sortable title text inside the Check # column header (not the filter button)
  251 |         await pageManager.issuedChecksPage.columnHeaderCheckNumber.getByText('Check #', { exact: true }).click();
  252 |         await expect(page.getByRole('columnheader', { name: 'Sorted in ascending order' }))
  253 |             .toBeVisible({ timeout: 10000 });
  254 | 
  255 |         await page.getByRole('columnheader', { name: 'Sorted in ascending order' })
  256 |             .getByText('Check #', { exact: true }).click();
  257 |         await expect(page.getByRole('columnheader', { name: 'Sorted in descending order' }))
  258 |             .toBeVisible({ timeout: 10000 });
  259 |     });
  260 | 
  261 |     // ── Column filter ─────────────────────────────────────────────────────────
  262 | 
  263 |     test('Column filter popup applies a filter and Clear restores the full row set', async ({ pageManager }) => {
  264 |         const baseline = await pageManager.issuedChecksPage.gridRows.count();
  265 |         // Check # is at td index 6 in the default column order
  266 |         const checkNo = (await pageManager.issuedChecksPage.gridRows.first().locator('td').nth(6).innerText()).trim();
  267 | 
  268 |         await pageManager.issuedChecksPage.columnFilterButton('Check #').click();
  269 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeVisible();
  270 |         const input = pageManager.issuedChecksPage.columnFilterPopup
  271 |             .locator('input[role="spinbutton"]:visible').first();
  272 |         await input.fill(checkNo);
  273 |         await input.press('Tab');
  274 |         await pageManager.issuedChecksPage.columnFilterApplyButton.click();
  275 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  276 |         await expect(pageManager.issuedChecksPage.gridRows.first()).toBeVisible({ timeout: 10000 });
  277 | 
  278 |         // Clear the filter and verify baseline is restored
  279 |         await pageManager.issuedChecksPage.columnFilterButton('Check #').click();
  280 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeVisible();
  281 |         await pageManager.issuedChecksPage.columnFilterClearButton.click();
  282 |         await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  283 |         await expect.poll(async () => pageManager.issuedChecksPage.gridRows.count(), { timeout: 10000 })
  284 |             .toBe(baseline);
  285 |     });
  286 | 
  287 |     // ── Row actions ───────────────────────────────────────────────────────────
  288 | 
  289 |     test('"Edit" link on a row navigates to the check edit form', async ({ pageManager, page }) => {
  290 |         const firstEditableLink = pageManager.issuedChecksPage.gridRows
  291 |             .locator('a[href*="/issued-checks/check/"]')
  292 |             .first();
  293 | 
  294 |         await expect(firstEditableLink).toBeVisible({ timeout: 15000 });
  295 |         await firstEditableLink.click();
  296 |         await expect(page).toHaveURL(/\/issued-checks\/check\/\d+/, { timeout: 15000 });
  297 |     });
  298 | 
  299 |     test('"View" (Change Log) link on a row navigates to the entity log', async ({ pageManager, page }) => {
  300 |         await pageManager.issuedChecksPage.gridRows.first()
  301 |             .getByRole('link', { name: /View/ }).click();
  302 |         await expect(page).toHaveURL(/\/client-admin\/entity-log/, { timeout: 15000 });
  303 |     });
  304 | 
  305 |     test('"Delete" on a row shows a confirm modal; Cancel dismisses it without deleting', async ({ pageManager }) => {
  306 |         const rowCountBefore = await pageManager.issuedChecksPage.gridRows.count();
  307 |         const firstDeleteLink = pageManager.issuedChecksPage.gridRows
  308 |             .locator('a:has-text("Delete")')
  309 |             .first();
  310 | 
  311 |         await expect(firstDeleteLink).toBeVisible({ timeout: 15000 });
  312 |         await firstDeleteLink.click();
  313 |         await expect(pageManager.issuedChecksPage.confirmDialog).toBeVisible({ timeout: 10000 });
  314 |         await expect(pageManager.issuedChecksPage.confirmDialog)
  315 |             .toContainText('This action cannot be undone');
  316 |         await pageManager.issuedChecksPage.confirmDialogCancelButton.click();
  317 |         await expect(pageManager.issuedChecksPage.confirmDialog).toBeHidden({ timeout: 10000 });
  318 |         // Row count must be unchanged after cancelling
  319 |         expect(await pageManager.issuedChecksPage.gridRows.count()).toBe(rowCountBefore);
  320 |     });
```