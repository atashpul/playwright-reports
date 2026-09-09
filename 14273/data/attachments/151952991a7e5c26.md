# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\5-PresentedChecksSmoke.spec.ts >> Presented Checks — Smoke (Continued) >> Column filter popup applies a filter and Clear restores the full row set
- Location: specs\Smoke\5-PresentedChecksSmoke.spec.ts:286:5

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
  - link "  Exceptions":
    - /url: /exceptions
  - link "  Settings":
    - /url: /client-admin
  - button "  F.I ACH&CHK User"
- list:
  - listitem:
    - link " ":
      - /url: /
  - listitem:
    - link "Presented Checks":
      - /url: /paid-checks
- group:
  - link " Uploaded Checks":
    - /url: /paid-checks/uploads
  - link "+ Add Check":
    - /url: /paid-checks/check
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
    - option "SMK_Default_1788777089315" [selected]
  - button ""
  - button ""
- grid "Data table":
  - rowgroup:
    - 'row "ID ID column filter menu settings Status Status column filter menu settings Decision Decision column filter menu settings Client Client column filter menu settings Account Account column filter menu settings Reference ID Reference ID column filter menu settings Routing # Routing # column filter menu settings Account # Account # column filter menu settings Check # Check # column filter menu settings Amount Amount column filter menu settings Presented Date Presented Date column filter menu settings Payee Name Payee Name column filter menu settings Check Image Issued Check Data Added By Added By column filter menu settings Edit Change Log"':
      - columnheader "ID ID column filter menu settings":
        - text: ID
        - button "ID column filter menu settings"
      - columnheader "Status Status column filter menu settings":
        - text: Status
        - button "Status column filter menu settings"
      - columnheader "Decision Decision column filter menu settings":
        - text: Decision
        - button "Decision column filter menu settings"
      - columnheader "Client Client column filter menu settings":
        - text: Client
        - button "Client column filter menu settings"
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
      - columnheader "Presented Date Presented Date column filter menu settings":
        - text: Presented Date
        - button "Presented Date column filter menu settings"
      - columnheader "Payee Name Payee Name column filter menu settings":
        - text: Payee Name
        - button "Payee Name column filter menu settings"
      - columnheader "Check Image"
      - columnheader "Issued Check Data"
      - columnheader "Added By Added By column filter menu settings":
        - text: Added By
        - button "Added By column filter menu settings"
      - columnheader "Edit"
      - columnheader "Change Log"
  - rowgroup:
    - row "33777 Completed[Default Decision]  Return  PJ_BC_Boutique(Both) Account2 Exlid123 231382306 7578091758 420254117 $815.00 08/20/2026 AutoPresentedPayee PresentedCheck_Comma_Auto_651073.txt  Edit  Delete View ":
      - gridcell "33777"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=33777&ExceptionType=Check&ReturnUrl=%2fpaid-checks
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account2"
      - gridcell "Exlid123"
      - gridcell "231382306"
      - gridcell "7578091758"
      - gridcell "420254117"
      - gridcell "$815.00"
      - gridcell "08/20/2026"
      - gridcell "AutoPresentedPayee"
      - gridcell
      - gridcell
      - gridcell "PresentedCheck_Comma_Auto_651073.txt":
        - link "PresentedCheck_Comma_Auto_651073.txt":
          - /url: /paid-checks/uploads?Id=15561
      - gridcell " Edit  Delete":
        - link " Edit":
          - /url: /paid-checks/check/33777
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=33777&ReturnUrl=%2fpaid-checks
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
  192 |         await expect.poll(
  193 |             async () => pageManager.presentedChecksPage.savedFiltersDropdown.inputValue(),
  194 |             { timeout: 15000 }
  195 |         ).toBe(presetName);
  196 |         await expect.poll(
  197 |             async () => pageManager.presentedChecksPage.gridRows.count(),
  198 |             { timeout: 10000 }
  199 |         ).toBe(filteredCount);
  200 | 
  201 |         // Cleanup (delete the Default preset) runs in afterEach via pendingFilterPresetCleanup.
  202 |     });
  203 | 
  204 | });
  205 | 
  206 | // Resume regular parallel execution for remaining tests
  207 | test.describe('Presented Checks — Smoke (Continued)', () => {
  208 | 
  209 |     test.beforeEach(async ({ pageManager }) => {
  210 |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  211 |         await pageManager.loginPage.login(
  212 |             Constants.USER_FI_EMAIL,
  213 |             Constants.USER_FI_PASSWORD
  214 |         );
  215 |         await pageManager.homePage.homePageLogo.waitFor({ state: 'visible', timeout: 20000 });
  216 |         await pageManager.presentedChecksPage.navigateToPresentedChecks();
  217 |         await pageManager.presentedChecksPage.waitForGridLoad();
  218 |     });
  219 | 
  220 |     // Safety net for the preset created below (non-default). afterEach removes any SMK_ preset
  221 |     // if an assertion fails before the inline delete runs.
  222 |     let pendingFilterPresetCleanup: string | undefined;
  223 | 
  224 |     test.afterEach(async ({ page, pageManager }) => {
  225 |         if (!pendingFilterPresetCleanup) return;
  226 |         pendingFilterPresetCleanup = undefined;
  227 | 
  228 |         await pageManager.presentedChecksPage.navigateToPresentedChecks();
  229 |         await purgeSavedFilterPresets(page, {
  230 |             dropdown: pageManager.presentedChecksPage.savedFiltersDropdown,
  231 |             deleteButton: pageManager.presentedChecksPage.deleteSavedFilterButton,
  232 |             confirmDialog: pageManager.presentedChecksPage.confirmDialog,
  233 |             confirmButton: pageManager.presentedChecksPage.confirmDialogConfirmButton,
  234 |         });
  235 |     });
  236 | 
  237 |     test('Save a filter preset, verify it is auto-selected, then delete it', async ({ pageManager }) => {
  238 |         // Check # is at td index 8 in the default Presented Checks column order.
  239 |         const checkNo = (await pageManager.presentedChecksPage.gridRows.first()
  240 |             .locator('td').nth(8).innerText()).trim();
  241 | 
  242 |         await pageManager.presentedChecksPage.columnFilterButton('Check #').click();
  243 |         await expect(pageManager.presentedChecksPage.columnFilterPopup).toBeVisible();
  244 |         const filterInput = pageManager.presentedChecksPage.columnFilterPopup
  245 |             .locator('input[role="spinbutton"]:visible').first();
  246 |         await filterInput.fill(checkNo);
  247 |         await filterInput.press('Tab');
  248 |         await pageManager.presentedChecksPage.columnFilterApplyButton.click();
  249 |         await expect(pageManager.presentedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  250 | 
  251 |         const presetName = `SMK_Check_${Date.now()}`;
  252 |         await pageManager.presentedChecksPage.saveCurrentFilterAs(presetName);
  253 |         // Preset now exists on the shared env — afterEach removes it if we fail before deleting.
  254 |         pendingFilterPresetCleanup = presetName;
  255 | 
  256 |         await expect(pageManager.presentedChecksPage.savedFiltersDropdown).toHaveValue(presetName, { timeout: 10000 });
  257 | 
  258 |         // Delete IS the assertion under test, so it stays inline (not moved to afterEach).
  259 |         await expect(pageManager.presentedChecksPage.deleteSavedFilterButton).toBeVisible();
  260 |         await pageManager.presentedChecksPage.deleteSavedFilterButton.click();
  261 |         await expect(pageManager.presentedChecksPage.confirmDialog).toBeVisible();
  262 |         await pageManager.presentedChecksPage.confirmDialogConfirmButton.click();
  263 |         await expect(pageManager.presentedChecksPage.confirmDialog).toBeHidden({ timeout: 10000 });
  264 |         await expect.poll(
  265 |             async () => pageManager.presentedChecksPage.savedFiltersDropdown.locator('option').allInnerTexts(),
  266 |             { timeout: 10000 }
  267 |         ).not.toContain(presetName);
  268 |         pendingFilterPresetCleanup = undefined; // deleted inline above
  269 |     });
  270 | 
  271 |     // ── Column sort ───────────────────────────────────────────────────────────
  272 | 
  273 |     test('Clicking a column header sorts ascending, clicking again sorts descending', async ({ pageManager, page }) => {
  274 |         await pageManager.presentedChecksPage.columnHeaderCheckNumber.getByText('Check #', { exact: true }).click();
  275 |         await expect(page.getByRole('columnheader', { name: 'Sorted in ascending order' }))
  276 |             .toBeVisible({ timeout: 10000 });
  277 | 
  278 |         await page.getByRole('columnheader', { name: 'Sorted in ascending order' })
  279 |             .getByText('Check #', { exact: true }).click();
  280 |         await expect(page.getByRole('columnheader', { name: 'Sorted in descending order' }))
  281 |             .toBeVisible({ timeout: 10000 });
  282 |     });
  283 | 
  284 |     // ── Column filter ─────────────────────────────────────────────────────────
  285 | 
  286 |     test('Column filter popup applies a filter and Clear restores the full row set', async ({ pageManager }) => {
  287 |         const baseline = await pageManager.presentedChecksPage.gridRows.count();
  288 |         // Check # is at td index 8 in the default Presented Checks column order.
  289 |         const checkNo = (await pageManager.presentedChecksPage.gridRows.first().locator('td').nth(8).innerText()).trim();
  290 | 
  291 |         await pageManager.presentedChecksPage.columnFilterButton('Check #').click();
> 292 |         await expect(pageManager.presentedChecksPage.columnFilterPopup).toBeVisible();
      |                                                                         ^ Error: expect(locator).toBeVisible() failed
  293 |         const input = pageManager.presentedChecksPage.columnFilterPopup
  294 |             .locator('input[role="spinbutton"]:visible').first();
  295 |         await input.fill(checkNo);
  296 |         await input.press('Tab');
  297 |         await pageManager.presentedChecksPage.columnFilterApplyButton.click();
  298 |         await expect(pageManager.presentedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  299 |         await expect(pageManager.presentedChecksPage.gridRows.first()).toBeVisible({ timeout: 10000 });
  300 | 
  301 |         // Clear the filter and verify baseline is restored.
  302 |         await pageManager.presentedChecksPage.columnFilterButton('Check #').click();
  303 |         await expect(pageManager.presentedChecksPage.columnFilterPopup).toBeVisible();
  304 |         await pageManager.presentedChecksPage.columnFilterClearButton.click();
  305 |         await expect(pageManager.presentedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  306 |         await expect.poll(async () => pageManager.presentedChecksPage.gridRows.count(), { timeout: 10000 })
  307 |             .toBe(baseline);
  308 |     });
  309 | 
  310 |     // ── Row actions ───────────────────────────────────────────────────────────
  311 | 
  312 |     test('"Edit" link on a row navigates to the check edit form', async ({ pageManager, page }) => {
  313 |         await pageManager.presentedChecksPage.gridRows.first()
  314 |             .getByRole('link', { name: /Edit/ }).click();
  315 |         await expect(page).toHaveURL(/\/paid-checks\/check\/\d+/, { timeout: 15000 });
  316 |     });
  317 | 
  318 |     test('"View" (Change Log) link on a row navigates to the entity log', async ({ pageManager, page }) => {
  319 |         const changeLogLink = pageManager.presentedChecksPage.gridRows.first()
  320 |             .locator('a[href*="/client-admin/entity-log"]')
  321 |             .first();
  322 | 
  323 |         await expect(changeLogLink).toBeVisible({ timeout: 15000 });
  324 |         await changeLogLink.click();
  325 |         await expect(page).toHaveURL(/\/client-admin\/entity-log/, { timeout: 15000 });
  326 |     });
  327 | 
  328 |     test('"Delete" on a row shows a confirm modal; Cancel dismisses it without deleting', async ({ pageManager }) => {
  329 |         await expect(pageManager.presentedChecksPage.gridRows.first()).toBeVisible({ timeout: 15000 });
  330 |         const rowCountBefore = await pageManager.presentedChecksPage.gridRows.count();
  331 |         await pageManager.presentedChecksPage.gridRows.first()
  332 |             .getByRole('link', { name: /Delete/ }).click();
  333 |         await expect(pageManager.presentedChecksPage.confirmDialog).toBeVisible({ timeout: 10000 });
  334 |         await expect(pageManager.presentedChecksPage.confirmDialog)
  335 |             .toContainText('This action cannot be undone');
  336 |         await pageManager.presentedChecksPage.confirmDialogCancelButton.click();
  337 |         await expect(pageManager.presentedChecksPage.confirmDialog).toBeHidden({ timeout: 10000 });
  338 |         expect(await pageManager.presentedChecksPage.gridRows.count()).toBe(rowCountBefore);
  339 |     });
  340 | 
  341 |     test('Pay/Return decision badge navigates to exception history', async ({ pageManager, page }) => {
  342 |         let decisionHistoryBadge = pageManager.presentedChecksPage.gridRows
  343 |             .locator('a[href*="/exceptions/history"]')
  344 |             .filter({ hasText: /Pay|Return/i })
  345 |             .first();
  346 | 
  347 |         // Navigate through pages until we find a Pay/Return decision badge
  348 |         let badgeFound = false;
  349 |         let pageCount = 0;
  350 |         const maxPages = 10; // Safety limit to prevent infinite loop
  351 | 
  352 |         while (!badgeFound && pageCount < maxPages) {
  353 |             const isVisible = await decisionHistoryBadge.isVisible({ timeout: 2000 }).catch(() => false);
  354 |             
  355 |             if (isVisible) {
  356 |                 badgeFound = true;
  357 |                 break;
  358 |             }
  359 | 
  360 |             // Check if next page button is enabled
  361 |             const nextButton = pageManager.presentedChecksPage.nextPageButton;
  362 |             const isNextEnabled = await nextButton.isEnabled().catch(() => false);
  363 | 
  364 |             if (!isNextEnabled) {
  365 |                 break; // No more pages to check
  366 |             }
  367 | 
  368 |             // Navigate to next page
  369 |             await nextButton.click();
  370 |             await pageManager.presentedChecksPage.waitForGridLoad();
  371 |             pageCount++;
  372 |         }
  373 | 
  374 |         if (!badgeFound) {
  375 |             throw new Error(`No Pay/Return decision badge found after checking ${pageCount + 1} page(s). The grid may only contain Pending decisions.`);
  376 |         }
  377 | 
  378 |         await expect(decisionHistoryBadge).toBeVisible({ timeout: 5000 });
  379 |         await decisionHistoryBadge.click();
  380 |         await expect(page).toHaveURL(/\/exceptions\/history/, { timeout: 15000 });
  381 |     });
  382 | 
  383 |     // ── Breadcrumb ────────────────────────────────────────────────────────────
  384 | 
  385 |     test('Presented Checks breadcrumb link is visible on the page', async ({ pageManager }) => {
  386 |         await expect(pageManager.presentedChecksPage.pageHeading).toBeVisible();
  387 |     });
  388 | 
  389 | });
  390 | 
```