# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\4-IssuedChecksSmoke.spec.ts >> Issued Checks — Smoke >> Next page arrow advances to page 2
- Location: specs\Smoke\4-IssuedChecksSmoke.spec.ts:64:5

# Error details

```
Error: expect(locator).toContainText(expected) failed

Locator: getByRole('application', { name: /Page navigation/ }).locator('text=items')
Timeout: 15000ms
- Expected substring  - 1
+ Received string     + 3

- 1 - 20
+
+                 1 - 1 of 1 items
+             

Call log:
  - Expect "toContainText" with timeout 15000ms
  - waiting for getByRole('application', { name: /Page navigation/ }).locator('text=items')
    30 × locator resolved to <span class="k-pager-info" data-adaptive="true">…</span>
       - unexpected value "
                1 - 1 of 1 items
            "

```

```yaml
- text: 1 - 1 of 1 items
```

# Test source

```ts
  1   | import { test, expect } from '../../utility/fixture';
  2   | import Constants from '../../utility/Constants';
  3   | import { LogoutPage } from '../../page-object/Login/Logout';
  4   | 
  5   | test.describe('Issued Checks — Smoke', () => {
  6   | 
  7   |     test.beforeEach(async ({ pageManager }) => {
  8   |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  9   |         await pageManager.loginPage.login(
  10  |             Constants.USER_FI_EMAIL,
  11  |             Constants.USER_FI_PASSWORD
  12  |         );
  13  |         await pageManager.homePage.homePageLogo.waitFor({ state: 'visible', timeout: 20000 });
  14  |         await pageManager.issuedChecksPage.navigateToIssuedChecks();
  15  |         await pageManager.issuedChecksPage.waitForGridLoad();
  16  |     });
  17  | 
  18  |     // ── Grid ─────────────────────────────────────────────────────────────────
  19  | 
  20  |     test('Grid loads with data rows and key column headers', async ({ pageManager }) => {
  21  |         await expect(pageManager.issuedChecksPage.gridRows.first()).toBeVisible({ timeout: 15000 });
  22  |         await pageManager.issuedChecksPage.verifyGridColumnsVisible();
  23  |     });
  24  | 
  25  |     // ── Navigation ───────────────────────────────────────────────────────────
  26  | 
  27  |     test('"+ Add Check" navigates to the add-check form', async ({ pageManager, page }) => {
  28  |         await pageManager.issuedChecksPage.addCheckNavigationLink.click();
  29  |         await expect(page).toHaveURL(/\/issued-checks\/add-check/, { timeout: 15000 });
  30  |         await expect(pageManager.issuedChecksPage.addCheckBreadcrumb).toBeVisible({ timeout: 15000 });
  31  |     });
  32  | 
  33  |     test('"Uploaded Checks" navigates to the uploads page', async ({ page }) => {
  34  |         await page.getByRole('link', { name: /Uploaded Checks/i }).first().click();
  35  |         await expect(page).toHaveURL(/\/issued-checks\/uploads/, { timeout: 15000 });
  36  |     });
  37  | 
  38  |     // ── Toolbar ──────────────────────────────────────────────────────────────
  39  | 
  40  |     test('Search box filters grid and clears correctly', async ({ pageManager }) => {
  41  |         await pageManager.issuedChecksPage.searchFor('__SMOKE_NO_RESULTS__');
  42  |         // Rows also vanish during Kendo's loading flash, so an empty grid is not proof the
  43  |         // search round-trip finished. The pager total is — and clearing while the search is
  44  |         // still in flight lets the two responses land out of order, leaving the grid empty.
  45  |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('0 - 0 of 0', { timeout: 15000 });
  46  |         await expect(pageManager.issuedChecksPage.gridRows.first()).not.toBeVisible({ timeout: 15000 });
  47  |         await pageManager.issuedChecksPage.clearSearch();
  48  |         await expect(pageManager.issuedChecksPage.gridRows.first()).toBeVisible({ timeout: 15000 });
  49  |     });
  50  | 
  51  |     test('Excel export button is visible and enabled', async ({ pageManager }) => {
  52  |         await expect(pageManager.issuedChecksPage.excelExportButton).toBeVisible();
  53  |         await expect(pageManager.issuedChecksPage.excelExportButton).toBeEnabled();
  54  |     });
  55  | 
  56  |     // ── Pagination ───────────────────────────────────────────────────────────
  57  | 
  58  |     test('Page size change to 10 updates pagination info in bottom-right pager', async ({ pageManager }) => {
  59  |         await pageManager.issuedChecksPage.pageSizeDropdown.selectOption('10');
  60  |         // pager shows "1 - 10 of N items" after the grid reloads
  61  |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 10', { timeout: 15000 });
  62  |     });
  63  | 
  64  |     test('Next page arrow advances to page 2', async ({ pageManager }) => {
  65  |         await pageManager.issuedChecksPage.pageSizeDropdown.selectOption('20');
> 66  |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 20', { timeout: 15000 });
      |                                                                   ^ Error: expect(locator).toContainText(expected) failed
  67  |         await pageManager.issuedChecksPage.nextPageButton.click();
  68  |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('21 -', { timeout: 15000 });
  69  |     });
  70  | 
  71  |     test('Last page arrow jumps to the final page', async ({ pageManager }) => {
  72  |         await pageManager.issuedChecksPage.lastPageButton.click();
  73  |         // on the last page both forward arrows must be disabled
  74  |         await expect(pageManager.issuedChecksPage.nextPageButton).toBeDisabled({ timeout: 15000 });
  75  |         await expect(pageManager.issuedChecksPage.lastPageButton).toBeDisabled({ timeout: 15000 });
  76  |     });
  77  | 
  78  |     test('Typing a page number navigates to that page', async ({ pageManager }) => {
  79  |         await pageManager.issuedChecksPage.pageSizeDropdown.selectOption('20');
  80  |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 20', { timeout: 15000 });
  81  |         await pageManager.issuedChecksPage.currentPageInput.fill('3');
  82  |         await pageManager.issuedChecksPage.currentPageInput.press('Enter');
  83  |         // page 3 with size 20 starts at item 41
  84  |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('41 -', { timeout: 15000 });
  85  |     });
  86  | 
  87  |     test('Previous page button returns to page 1, First page button re-enables disabled state', async ({ pageManager }) => {
  88  |         await pageManager.issuedChecksPage.pageSizeDropdown.selectOption('20');
  89  |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 20', { timeout: 15000 });
  90  | 
  91  |         await pageManager.issuedChecksPage.nextPageButton.click();
  92  |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('21 -', { timeout: 15000 });
  93  | 
  94  |         // Previous returns to page 1
  95  |         await pageManager.issuedChecksPage.previousPageButton.click();
  96  |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 20', { timeout: 15000 });
  97  | 
  98  |         // Jump to page 3, then First page brings us back and disables both back buttons
  99  |         await pageManager.issuedChecksPage.currentPageInput.fill('3');
  100 |         await pageManager.issuedChecksPage.currentPageInput.press('Enter');
  101 |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('41 -', { timeout: 15000 });
  102 |         await pageManager.issuedChecksPage.firstPageButton.click();
  103 |         await expect(pageManager.issuedChecksPage.paginationInfo).toContainText('1 - 20', { timeout: 15000 });
  104 |         await expect(pageManager.issuedChecksPage.previousPageButton).toBeDisabled({ timeout: 10000 });
  105 |         await expect(pageManager.issuedChecksPage.firstPageButton).toBeDisabled({ timeout: 10000 });
  106 |     });
  107 | 
  108 |     // ── Saved Filters ────────────────────────────────────────────────────────
  109 | 
  110 |     test('Saved Filters dropdown is visible and defaults to no preset', async ({ pageManager }) => {
  111 |         await expect(pageManager.issuedChecksPage.savedFiltersDropdown).toBeVisible();
  112 |         await expect(pageManager.issuedChecksPage.savedFiltersDropdown).toHaveValue('');
  113 |     });
  114 | 
  115 | });
  116 | 
  117 | // Separate serial test block for default filter test to prevent parallel execution conflicts.
  118 | // This test modifies global state (the default filter) and must not run concurrently.
  119 | test.describe.serial('Issued Checks — Default Filter (Serial)', () => {
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
```