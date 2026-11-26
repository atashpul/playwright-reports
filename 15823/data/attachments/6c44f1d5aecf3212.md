# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\4-IssuedChecksSmoke.spec.ts >> Issued Checks — Smoke >> Pagination >> Previous page button returns to page 1, First page button re-enables disabled state
- Location: specs\Smoke\4-IssuedChecksSmoke.spec.ts:101:9

# Error details

```
Error: expect(locator).toContainText(expected) failed

Locator: locator('.k-grid-pager').locator('.k-pager-info')
Timeout: 15000ms
- Expected substring  - 1
+ Received string     + 3

- 1 - 20
+
+                 1 - 1 of 1 items
+             

Call log:
  - Expect "toContainText" with timeout 15000ms
  - waiting for locator('.k-grid-pager').locator('.k-pager-info')
    31 × locator resolved to <span class="k-pager-info" data-adaptive="true">…</span>
       - unexpected value "
                1 - 1 of 1 items
            "

```

```yaml
- text: 1 - 1 of 1 items
```

# Test source

```ts
  3   | import { LogoutPage } from '../../page-object/Login/Logout';
  4   | import { purgeSavedFilterPresets } from '../../utility/savedFilters';
  5   | import { captureSharedLogin, restoreSession, type CapturedAuth } from '../../utility/sessionAuth';
  6   | 
  7   | // One shared login for the whole file (per worker); every test replays it into its own
  8   | // fresh context. Constants is still used by the serial logout/re-login test below.
  9   | let auth: CapturedAuth;
  10  | 
  11  | test.beforeAll('Log in once and capture the session', async ({ browser }) => {
  12  |     auth = await captureSharedLogin(browser);
  13  | });
  14  | 
  15  | test.beforeEach('Restore the captured session', async ({ context }) => {
  16  |     await restoreSession(context, auth);
  17  | });
  18  | 
  19  | test.describe('Issued Checks — Smoke', () => {
  20  | 
  21  |     test.beforeEach('Open Issued Checks', async ({ pageManager }) => {
  22  |         await pageManager.issuedChecksPage.navigateToIssuedChecks();
  23  |         await pageManager.issuedChecksPage.waitForGridLoad();
  24  |     });
  25  | 
  26  |     test.describe('Grid', () => {
  27  | 
  28  |         test('Grid loads with data rows and key column headers', async ({ pageManager }) => {
  29  |             await expect(pageManager.issuedChecksPage.gridRows.first()).toBeVisible({ timeout: 15000 });
  30  |             await pageManager.issuedChecksPage.verifyGridColumnsVisible();
  31  |         });
  32  | 
  33  |     });
  34  | 
  35  |     test.describe('Navigation', () => {
  36  | 
  37  |         test('"+ Add Check" navigates to the add-check form', async ({ pageManager, page }) => {
  38  |             await pageManager.issuedCheckAddCheckPage.addCheckNavigationLink.click();
  39  |             await expect(page).toHaveURL(/\/issued-checks\/add-check/, { timeout: 15000 });
  40  |             await expect(pageManager.issuedCheckAddCheckPage.addCheckBreadcrumb).toBeVisible({ timeout: 15000 });
  41  |         });
  42  | 
  43  |         test('"Uploaded Checks" navigates to the uploads page', async ({ page }) => {
  44  |             await page.getByRole('link', { name: /Uploaded Checks/i }).first().click();
  45  |             await expect(page).toHaveURL(/\/issued-checks\/uploads/, { timeout: 15000 });
  46  |         });
  47  | 
  48  |     });
  49  | 
  50  |     test.describe('Toolbar', () => {
  51  | 
  52  |         test('Search box filters grid and clears correctly', async ({ pageManager }) => {
  53  |             await pageManager.issuedChecksPage.searchFor('__SMOKE_NO_RESULTS__');
  54  |             // Rows also vanish during Kendo's loading flash, so an empty grid is not proof the
  55  |             // search round-trip finished. The pager total is — and clearing while the search is
  56  |             // still in flight lets the two responses land out of order, leaving the grid empty.
  57  |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('0 - 0 of 0', { timeout: 15000 });
  58  |             await expect(pageManager.issuedChecksPage.gridRows.first()).not.toBeVisible({ timeout: 15000 });
  59  |             await pageManager.issuedChecksPage.clearSearch();
  60  |             await expect(pageManager.issuedChecksPage.gridRows.first()).toBeVisible({ timeout: 15000 });
  61  |         });
  62  | 
  63  |         test('Excel export button is visible and enabled', async ({ pageManager }) => {
  64  |             await expect(pageManager.issuedChecksPage.excelExportButton).toBeVisible();
  65  |             await expect(pageManager.issuedChecksPage.excelExportButton).toBeEnabled();
  66  |         });
  67  | 
  68  |     });
  69  | 
  70  |     test.describe('Pagination', () => {
  71  | 
  72  |         test('Page size change to 10 updates pagination info in bottom-right pager', async ({ pageManager }) => {
  73  |             await pageManager.issuedChecksPage.pageSizeDropdown.selectOption('10');
  74  |             // pager shows "1 - 10 of N items" after the grid reloads
  75  |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 10', { timeout: 15000 });
  76  |         });
  77  | 
  78  |         test('Next page arrow advances to page 2', async ({ pageManager }) => {
  79  |             await pageManager.issuedChecksPage.pageSizeDropdown.selectOption('20');
  80  |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 20', { timeout: 15000 });
  81  |             await pageManager.issuedChecksPage.nextPageButton.click();
  82  |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('21 -', { timeout: 15000 });
  83  |         });
  84  | 
  85  |         test('Last page arrow jumps to the final page', async ({ pageManager }) => {
  86  |             await pageManager.issuedChecksPage.lastPageButton.click();
  87  |             // on the last page both forward arrows must be disabled
  88  |             await expect(pageManager.issuedChecksPage.nextPageButton).toBeDisabled({ timeout: 15000 });
  89  |             await expect(pageManager.issuedChecksPage.lastPageButton).toBeDisabled({ timeout: 15000 });
  90  |         });
  91  | 
  92  |         test('Typing a page number navigates to that page', async ({ pageManager }) => {
  93  |             await pageManager.issuedChecksPage.pageSizeDropdown.selectOption('20');
  94  |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 20', { timeout: 15000 });
  95  |             await pageManager.issuedChecksPage.currentPageInput.fill('3');
  96  |             await pageManager.issuedChecksPage.currentPageInput.press('Enter');
  97  |             // page 3 with size 20 starts at item 41
  98  |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('41 -', { timeout: 15000 });
  99  |         });
  100 | 
  101 |         test('Previous page button returns to page 1, First page button re-enables disabled state', async ({ pageManager }) => {
  102 |             await pageManager.issuedChecksPage.pageSizeDropdown.selectOption('20');
> 103 |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 20', { timeout: 15000 });
      |                                                                       ^ Error: expect(locator).toContainText(expected) failed
  104 | 
  105 |             await pageManager.issuedChecksPage.nextPageButton.click();
  106 |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('21 -', { timeout: 15000 });
  107 | 
  108 |             // Previous returns to page 1
  109 |             await pageManager.issuedChecksPage.previousPageButton.click();
  110 |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 20', { timeout: 15000 });
  111 | 
  112 |             // Jump to page 3, then First page brings us back and disables both back buttons
  113 |             await pageManager.issuedChecksPage.currentPageInput.fill('3');
  114 |             await pageManager.issuedChecksPage.currentPageInput.press('Enter');
  115 |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('41 -', { timeout: 15000 });
  116 |             await pageManager.issuedChecksPage.firstPageButton.click();
  117 |             await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 20', { timeout: 15000 });
  118 |             await expect(pageManager.issuedChecksPage.previousPageButton).toBeDisabled({ timeout: 10000 });
  119 |             await expect(pageManager.issuedChecksPage.firstPageButton).toBeDisabled({ timeout: 10000 });
  120 |         });
  121 | 
  122 |     });
  123 | 
  124 |     test.describe('Saved Filters', () => {
  125 | 
  126 |         // Shared across every Saved Filters test (including the nested serial block):
  127 |         // any test that creates a preset on the shared env sets this, and afterEach
  128 |         // guarantees it is purged even if an assertion fails first.
  129 |         let pendingFilterPresetCleanup: string | undefined;
  130 | 
  131 |         test.afterEach(async ({ page, pageManager }) => {
  132 |             if (!pendingFilterPresetCleanup) return;
  133 |             pendingFilterPresetCleanup = undefined;
  134 | 
  135 |             await pageManager.issuedChecksPage.navigateToIssuedChecks();
  136 |             await purgeSavedFilterPresets(page, {
  137 |                 dropdown: pageManager.issuedChecksPage.savedFiltersDropdown,
  138 |                 deleteButton: pageManager.issuedChecksPage.deleteSavedFilterButton,
  139 |                 confirmDialog: pageManager.issuedChecksPage.confirmDialog,
  140 |                 confirmButton: pageManager.issuedChecksPage.confirmDialogConfirmButton,
  141 |             });
  142 |         });
  143 | 
  144 |         test('Saved Filters dropdown is visible and defaults to no preset', async ({ pageManager }) => {
  145 |             await expect(pageManager.issuedChecksPage.savedFiltersDropdown).toBeVisible();
  146 |             await expect(pageManager.issuedChecksPage.savedFiltersDropdown).toHaveValue('');
  147 |         });
  148 | 
  149 |         test('Save a filter preset, verify it is auto-selected, then delete it', async ({ pageManager }) => {
  150 |             // Sample the Check # from the first grid row to use as the filter value.
  151 |             // Check # is the 7th column (td index 6) in the default column order.
  152 |             const checkNo = (await pageManager.issuedChecksPage.gridRows.first()
  153 |                 .locator('td').nth(6).innerText()).trim();
  154 | 
  155 |             // Apply a column filter on Check # using the sampled value.
  156 |             await pageManager.issuedChecksPage.columnFilterButton('Check #').click();
  157 |             await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeVisible();
  158 |             const filterInput = pageManager.issuedChecksPage.columnFilterPopup
  159 |                 .locator('input[role="spinbutton"]:visible').first();
  160 |             await filterInput.fill(checkNo);
  161 |             await filterInput.press('Tab');
  162 |             await pageManager.issuedChecksPage.columnFilterApplyButton.click();
  163 |             await expect(pageManager.issuedChecksPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  164 | 
  165 |             // Save the active column filter as a named preset.
  166 |             const presetName = `SMK_Check_${Date.now()}`;
  167 |             await pageManager.issuedChecksPage.saveCurrentFilterAs(presetName);
  168 |             // Preset now exists on the shared env — afterEach removes it if we fail before deleting.
  169 |             pendingFilterPresetCleanup = presetName;
  170 | 
  171 |             // The dropdown should auto-select the newly saved preset.
  172 |             await expect(pageManager.issuedChecksPage.savedFiltersDropdown).toHaveValue(presetName, { timeout: 10000 });
  173 | 
  174 |             // Delete IS the assertion under test, so it stays inline (not moved to afterEach).
  175 |             await expect(pageManager.issuedChecksPage.deleteSavedFilterButton).toBeVisible();
  176 |             await pageManager.issuedChecksPage.deleteSavedFilterButton.click();
  177 |             await expect(pageManager.issuedChecksPage.confirmDialog).toBeVisible();
  178 |             await pageManager.issuedChecksPage.confirmDialogConfirmButton.click();
  179 |             await expect(pageManager.issuedChecksPage.confirmDialog).toBeHidden({ timeout: 10000 });
  180 |             await expect.poll(
  181 |                 async () => pageManager.issuedChecksPage.savedFiltersDropdown.locator('option').allInnerTexts(),
  182 |                 { timeout: 10000 }
  183 |             ).not.toContain(presetName);
  184 |             pendingFilterPresetCleanup = undefined; // deleted inline above
  185 |         });
  186 | 
  187 |         // Serial: modifies the account-global default filter (shared state), so its tests
  188 |         // must not run concurrently. It's shared by every browser on the same login, so it
  189 |         // runs on chromium only (see test.skip below) to keep concurrent projects from colliding.
  190 |         test.describe.serial('Default Filter', () => {
  191 | 
  192 |             test('Default filter auto-applies after logout and re-login', async ({ pageManager, page }, testInfo) => {
  193 |                 // The default filter is account-global and shared by every browser on the same login.
  194 |                 // Run on one browser only so concurrent projects can't collide on it (local 4-browser
  195 |                 // runs and the pipeline's 4 parallel browser jobs share the same account).
  196 |                 test.skip(testInfo.project.name !== 'chromium', 'Shared-account default filter runs on chromium only.');
  197 |                 const logoutPage = new LogoutPage(page);
  198 | 
  199 |                 // Self-heal: an interrupted prior run can leave an account-global default SMK_ preset
  200 |                 // that returns 0 rows, leaving no row to sample below. Purge any leftovers first
  201 |                 // (deleting a default preset also clears the account default), then reload a full grid.
  202 |                 await purgeSavedFilterPresets(page, {
  203 |                     dropdown: pageManager.issuedChecksPage.savedFiltersDropdown,
```