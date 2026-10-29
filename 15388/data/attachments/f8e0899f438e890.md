# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\9-AccountSettingsSmoke.spec.ts >> Settings — Account Section Smoke >> Decision Files >> Generated Files >> Grid contains Completed decision files
- Location: specs\Smoke\9-AccountSettingsSmoke.spec.ts:727:13

# Error details

```
Error: expect(locator).toBeVisible() failed

Locator: getByRole('grid', { name: 'Data table' }).locator('tbody tr').filter({ hasNot: locator('text=No records available.') }).filter({ hasText: 'Completed' }).first()
Expected: visible
Timeout: 30000ms
Error: element(s) not found

Call log:
  - Expect "toBeVisible" with timeout 30000ms
  - waiting for getByRole('grid', { name: 'Data table' }).locator('tbody tr').filter({ hasNot: locator('text=No records available.') }).filter({ hasText: 'Completed' }).first()

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
      - /url: /client-admin
  - listitem:
    - link "Settings":
      - /url: /client-admin
  - listitem:
    - link "Decision Files":
      - /url: javascript:;
- link "  Settings":
  - /url: /client-admin/decision-files/settings
- toolbar "Grid toolbar":
  - text: Page Size
  - combobox:
    - option "10"
    - option "20" [selected]
    - option "50"
    - option "100"
  - button "Excel"
  - textbox "Search..."
- grid "Data table":
  - rowgroup:
    - row "ID ID column filter menu settings Name Name column filter menu settings Status Status column filter menu settings For Date For Date column filter menu settings Date Requested Date Requested column filter menu settings Date Generated Date Generated column filter menu settings Log File":
      - columnheader "ID ID column filter menu settings":
        - text: ID
        - button "ID column filter menu settings"
      - columnheader "Name Name column filter menu settings":
        - text: Name
        - button "Name column filter menu settings"
      - columnheader "Status Status column filter menu settings":
        - text: Status
        - button "Status column filter menu settings"
      - columnheader "For Date For Date column filter menu settings":
        - text: For Date
        - button "For Date column filter menu settings"
      - columnheader "Date Requested Date Requested column filter menu settings":
        - text: Date Requested
        - button "Date Requested column filter menu settings"
      - columnheader "Date Generated Date Generated column filter menu settings":
        - text: Date Generated
        - button "Date Generated column filter menu settings"
      - columnheader "Log"
      - columnheader "File"
  - rowgroup:
    - row "9196 Test_PJ[10282026].csv Delivered 10/28/2026 10/28/2026 8:00 AM EDT 10/28/2026 8:00 AM EDT  View  Download":
      - gridcell "9196"
      - gridcell "Test_PJ[10282026].csv"
      - gridcell "Delivered"
      - gridcell "10/28/2026"
      - gridcell "10/28/2026 8:00 AM EDT"
      - gridcell "10/28/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=9196&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "9158 Test_PJ[10272026].csv Delivered 10/27/2026 10/27/2026 8:00 AM EDT 10/27/2026 8:00 AM EDT  View  Download":
      - gridcell "9158"
      - gridcell "Test_PJ[10272026].csv"
      - gridcell "Delivered"
      - gridcell "10/27/2026"
      - gridcell "10/27/2026 8:00 AM EDT"
      - gridcell "10/27/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=9158&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "9119 Test_PJ[10262026].csv Delivered 10/26/2026 10/26/2026 8:00 AM EDT 10/26/2026 8:00 AM EDT  View  Download":
      - gridcell "9119"
      - gridcell "Test_PJ[10262026].csv"
      - gridcell "Delivered"
      - gridcell "10/26/2026"
      - gridcell "10/26/2026 8:00 AM EDT"
      - gridcell "10/26/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=9119&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "9061 Test_PJ[10232026].csv Delivered 10/23/2026 10/23/2026 8:00 AM EDT 10/23/2026 8:00 AM EDT  View  Download":
      - gridcell "9061"
      - gridcell "Test_PJ[10232026].csv"
      - gridcell "Delivered"
      - gridcell "10/23/2026"
      - gridcell "10/23/2026 8:00 AM EDT"
      - gridcell "10/23/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=9061&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "9022 Test_PJ[10222026].csv Delivered 10/22/2026 10/22/2026 8:00 AM EDT 10/22/2026 8:00 AM EDT  View  Download":
      - gridcell "9022"
      - gridcell "Test_PJ[10222026].csv"
      - gridcell "Delivered"
      - gridcell "10/22/2026"
      - gridcell "10/22/2026 8:00 AM EDT"
      - gridcell "10/22/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=9022&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8984 Test_PJ[10212026].csv Delivered 10/21/2026 10/21/2026 8:00 AM EDT 10/21/2026 8:00 AM EDT  View  Download":
      - gridcell "8984"
      - gridcell "Test_PJ[10212026].csv"
      - gridcell "Delivered"
      - gridcell "10/21/2026"
      - gridcell "10/21/2026 8:00 AM EDT"
      - gridcell "10/21/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8984&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8946 Test_PJ[10202026].csv Delivered 10/20/2026 10/20/2026 8:00 AM EDT 10/20/2026 8:00 AM EDT  View  Download":
      - gridcell "8946"
      - gridcell "Test_PJ[10202026].csv"
      - gridcell "Delivered"
      - gridcell "10/20/2026"
      - gridcell "10/20/2026 8:00 AM EDT"
      - gridcell "10/20/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8946&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8908 Test_PJ[10192026].csv Delivered 10/19/2026 10/19/2026 8:00 AM EDT 10/19/2026 8:00 AM EDT  View  Download":
      - gridcell "8908"
      - gridcell "Test_PJ[10192026].csv"
      - gridcell "Delivered"
      - gridcell "10/19/2026"
      - gridcell "10/19/2026 8:00 AM EDT"
      - gridcell "10/19/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8908&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8850 Test_PJ[10162026].csv Delivered 10/16/2026 10/16/2026 8:00 AM EDT 10/16/2026 8:00 AM EDT  View  Download":
      - gridcell "8850"
      - gridcell "Test_PJ[10162026].csv"
      - gridcell "Delivered"
      - gridcell "10/16/2026"
      - gridcell "10/16/2026 8:00 AM EDT"
      - gridcell "10/16/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8850&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8811 Test_PJ[10152026].csv Delivered 10/15/2026 10/15/2026 8:00 AM EDT 10/15/2026 8:00 AM EDT  View  Download":
      - gridcell "8811"
      - gridcell "Test_PJ[10152026].csv"
      - gridcell "Delivered"
      - gridcell "10/15/2026"
      - gridcell "10/15/2026 8:00 AM EDT"
      - gridcell "10/15/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8811&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8773 Test_PJ[10142026].csv Delivered 10/14/2026 10/14/2026 8:00 AM EDT 10/14/2026 8:00 AM EDT  View  Download":
      - gridcell "8773"
      - gridcell "Test_PJ[10142026].csv"
      - gridcell "Delivered"
      - gridcell "10/14/2026"
      - gridcell "10/14/2026 8:00 AM EDT"
      - gridcell "10/14/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8773&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8737 Test_PJ[10132026].csv Delivered 10/13/2026 10/13/2026 8:00 AM EDT 10/13/2026 8:00 AM EDT  View  Download":
      - gridcell "8737"
      - gridcell "Test_PJ[10132026].csv"
      - gridcell "Delivered"
      - gridcell "10/13/2026"
      - gridcell "10/13/2026 8:00 AM EDT"
      - gridcell "10/13/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8737&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8677 Test_PJ[10092026].csv Delivered 10/09/2026 10/09/2026 8:00 AM EDT 10/09/2026 8:00 AM EDT  View  Download":
      - gridcell "8677"
      - gridcell "Test_PJ[10092026].csv"
      - gridcell "Delivered"
      - gridcell "10/09/2026"
      - gridcell "10/09/2026 8:00 AM EDT"
      - gridcell "10/09/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8677&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8641 Test_PJ[10082026].csv Delivered 10/08/2026 10/08/2026 8:00 AM EDT 10/08/2026 8:00 AM EDT  View  Download":
      - gridcell "8641"
      - gridcell "Test_PJ[10082026].csv"
      - gridcell "Delivered"
      - gridcell "10/08/2026"
      - gridcell "10/08/2026 8:00 AM EDT"
      - gridcell "10/08/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8641&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8605 Test_PJ[10072026].csv Delivered 10/07/2026 10/07/2026 8:00 AM EDT 10/07/2026 8:00 AM EDT  View  Download":
      - gridcell "8605"
      - gridcell "Test_PJ[10072026].csv"
      - gridcell "Delivered"
      - gridcell "10/07/2026"
      - gridcell "10/07/2026 8:00 AM EDT"
      - gridcell "10/07/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8605&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8569 Test_PJ[10062026].csv Delivered 10/06/2026 10/06/2026 8:00 AM EDT 10/06/2026 8:00 AM EDT  View  Download":
      - gridcell "8569"
      - gridcell "Test_PJ[10062026].csv"
      - gridcell "Delivered"
      - gridcell "10/06/2026"
      - gridcell "10/06/2026 8:00 AM EDT"
      - gridcell "10/06/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8569&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8534 Test_PJ[10052026].csv Delivered 10/05/2026 10/05/2026 8:00 AM EDT 10/05/2026 8:00 AM EDT  View  Download":
      - gridcell "8534"
      - gridcell "Test_PJ[10052026].csv"
      - gridcell "Delivered"
      - gridcell "10/05/2026"
      - gridcell "10/05/2026 8:00 AM EDT"
      - gridcell "10/05/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8534&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8485 Test_PJ[10022026].csv Delivered 10/02/2026 10/02/2026 8:00 AM EDT 10/02/2026 8:00 AM EDT  View  Download":
      - gridcell "8485"
      - gridcell "Test_PJ[10022026].csv"
      - gridcell "Delivered"
      - gridcell "10/02/2026"
      - gridcell "10/02/2026 8:00 AM EDT"
      - gridcell "10/02/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8485&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8443 Test_PJ[10012026].csv Delivered 10/01/2026 10/01/2026 8:00 AM EDT 10/01/2026 8:00 AM EDT  View  Download":
      - gridcell "8443"
      - gridcell "Test_PJ[10012026].csv"
      - gridcell "Delivered"
      - gridcell "10/01/2026"
      - gridcell "10/01/2026 8:00 AM EDT"
      - gridcell "10/01/2026 8:00 AM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8443&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
    - row "8437 202609307 Delivered 09/30/2026 09/30/2026 4:00 PM EDT 09/30/2026 4:00 PM EDT  View  Download":
      - gridcell "8437"
      - gridcell "202609307"
      - gridcell "Delivered"
      - gridcell "09/30/2026"
      - gridcell "09/30/2026 4:00 PM EDT"
      - gridcell "09/30/2026 4:00 PM EDT"
      - gridcell " View":
        - link " View":
          - /url: /client-admin/decision-files/logs?ReportId=8437&ReturnUrl=%2fclient-admin%2fdecision-files
      - gridcell " Download":
        - link " Download":
          - /url: javascript:;
- application "Page navigation, page 1 of 37":
  - button "Go to the first page" [disabled]
  - button "Go to the previous page" [disabled]
  - text: Page
  - spinbutton "Select a page": "1"
  - text: of 37
  - button "Go to the next page"
  - button "Go to the last page"
  - text: 1 - 20 of 729 items
- contentinfo:
  - text: FI Playwright Automation[uat-release] © Copyright Advanced Fraud Solutions 2005-2026 | All Rights Reserved |
  - link "Privacy Policy":
    - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  629 |             test('View opens the report log', async ({ page, pageManager }) => {
  630 |                 const billing = pageManager.billingReportsPage;
  631 |                 const reportId = (await billing.FIRST_COMPLETED_ROW.locator('td').first().innerText()).trim();
  632 | 
  633 |                 await billing.FIRST_COMPLETED_ROW.getByRole('link', { name: /View/ }).click();
  634 |                 await expect(page).toHaveURL(new RegExp(`/client-admin/billing-reports/logs\\?ReportId=${reportId}`), { timeout: 15000 });
  635 |                 for (const header of BillingReportsPage.EXPECTED_LOG_COLUMN_HEADERS) {
  636 |                     await expect(billing.columnHeader(header), `Header "${header}"`).toBeVisible({ timeout: 15000 });
  637 |                 }
  638 |                 await expect(billing.GRID_ROWS.first().locator('td').first()).toHaveText(reportId, { timeout: 15000 });
  639 |             });
  640 | 
  641 |         });
  642 | 
  643 |         test('Generate Report with Report Name empty is blocked with a message', async ({ page, pageManager }) => {
  644 |             const billing = pageManager.billingReportsPage;
  645 |             const settings = pageManager.settingsPage;
  646 | 
  647 |             await page.goto('/client-admin/billing-reports/manual');
  648 |             await expect(billing.REPORT_NAME_TEXTBOX).toHaveValue('', { timeout: 15000 });
  649 |             await billing.GENERATE_REPORT_BUTTON.click();
  650 |             await expect(settings.MODAL).toContainText('Please enter a report name', { timeout: 10000 });
  651 |             await settings.MODAL_OK_BUTTON.click();
  652 |             await expect(settings.MODAL).toBeHidden();
  653 |             await expect(page).toHaveURL(/\/client-admin\/billing-reports\/manual$/);
  654 |         });
  655 | 
  656 |         test('Add New on Scheduled opens an empty schedule form', async ({ page, pageManager }) => {
  657 |             const billing = pageManager.billingReportsPage;
  658 |             await page.goto('/client-admin/billing-reports/settings');
  659 |             await billing.ADD_NEW_SCHEDULE_LINK.click();
  660 | 
  661 |             await expect(page).toHaveURL(/\/client-admin\/billing-reports\/add-new-setting$/, { timeout: 15000 });
  662 |             await expect(pageManager.settingsPage.BREADCRUMB_CURRENT).toHaveText('[Add New]', { timeout: 15000 });
  663 |             await expect(billing.REPORT_NAME_TEXTBOX).toHaveValue('');
  664 |             await expect(billing.FREQUENCY_DROPDOWN).toBeVisible();
  665 |             await expect(billing.SAVE_SCHEDULE_BUTTON).toBeVisible();
  666 |         });
  667 | 
  668 |         test('Manual request form switches date range presets and enables Custom dates', async ({ page, pageManager }) => {
  669 |             const billing = pageManager.billingReportsPage;
  670 |             await page.goto('/client-admin/billing-reports');
  671 |             await billing.MANUAL_BUTTON.click();
  672 |             await expect(page).toHaveURL(/\/client-admin\/billing-reports\/manual/, { timeout: 15000 });
  673 | 
  674 |             await expect(billing.REPORT_NAME_TEXTBOX).toBeVisible({ timeout: 15000 });
  675 |             await expect(billing.GENERATE_REPORT_BUTTON).toBeVisible();
  676 |             await expect(billing.FROM_DATE_INPUT).not.toHaveValue('');
  677 |             await expect(billing.FROM_DATE_INPUT).toBeDisabled();
  678 |             await expect(billing.TO_DATE_INPUT).toBeDisabled();
  679 |             const currentMonthFrom = await billing.FROM_DATE_INPUT.inputValue();
  680 | 
  681 |             await billing.DATE_RANGE_DROPDOWN.selectOption('Last Month');
  682 |             await expect(billing.FROM_DATE_INPUT).not.toHaveValue(currentMonthFrom, { timeout: 10000 });
  683 |             await expect(billing.FROM_DATE_INPUT).toBeDisabled();
  684 | 
  685 |             await billing.DATE_RANGE_DROPDOWN.selectOption('Custom');
  686 |             await expect(billing.FROM_DATE_INPUT).toBeEnabled({ timeout: 10000 });
  687 |             await expect(billing.TO_DATE_INPUT).toBeEnabled();
  688 |         });
  689 | 
  690 |         test('Scheduled page lists schedules with View, Edit and Delete', async ({ page, pageManager }) => {
  691 |             const billing = pageManager.billingReportsPage;
  692 |             await page.goto('/client-admin/billing-reports');
  693 |             await billing.SCHEDULE_BUTTON.click();
  694 |             await expect(page).toHaveURL(/\/client-admin\/billing-reports\/settings/, { timeout: 15000 });
  695 | 
  696 |             const firstRow = billing.GRID_ROWS.first();
  697 |             await expect(firstRow.getByRole('link', { name: /Edit/ })).toBeVisible({ timeout: 15000 });
  698 |             await expect(firstRow.getByRole('link', { name: /View/ })).toBeVisible();
  699 |             await expect(firstRow.getByRole('link', { name: /Delete/ })).toBeVisible();
  700 |             for (const header of BillingReportsPage.EXPECTED_SCHEDULED_COLUMN_HEADERS) {
  701 |                 await expect(billing.columnHeader(header), `Header "${header}"`).toBeVisible();
  702 |             }
  703 |             await expect(billing.ADD_NEW_SCHEDULE_LINK).toBeVisible();
  704 |         });
  705 | 
  706 |     });
  707 | 
  708 |     // ── Decision Files ─────────────────────────────────────────────────────────
  709 | 
  710 |     test.describe('Decision Files', () => {
  711 | 
  712 |         test.describe('Generated Files', () => {
  713 | 
  714 |             test.beforeEach('Open Decision Files', async ({ page, pageManager }) => {
  715 |                 await page.goto('/client-admin/decision-files');
  716 |                 await expect(pageManager.decisionFilesPage.FIRST_DOWNLOAD_LINK).toBeVisible({ timeout: 15000 });
  717 |             });
  718 | 
  719 |             test('Grid loads with all column headers', async ({ pageManager }) => {
  720 |                 const decisionFiles = pageManager.decisionFilesPage;
  721 |                 await expect(decisionFiles.COLUMN_HEADERS).toHaveCount(DecisionFilesPage.EXPECTED_COLUMN_HEADERS.length);
  722 |                 for (const header of DecisionFilesPage.EXPECTED_COLUMN_HEADERS) {
  723 |                     await expect(decisionFiles.columnHeader(header), `Header "${header}"`).toBeVisible();
  724 |                 }
  725 |             });
  726 | 
  727 |             test('Grid contains Completed decision files', async ({ pageManager }) => {
  728 |                 const completedRow = pageManager.decisionFilesPage.GRID_ROWS.filter({ hasText: 'Completed' }).first();
> 729 |                 await expect(completedRow).toBeVisible();
      |                                            ^ Error: expect(locator).toBeVisible() failed
  730 |                 await expect(completedRow.getByRole('link', { name: /View/ })).toBeVisible();
  731 |                 await expect(completedRow.getByRole('link', { name: /Download/ })).toBeVisible();
  732 |             });
  733 | 
  734 |             test('Download on a completed file downloads it', async ({ page, pageManager }, testInfo) => {
  735 |                 // Same script-triggered Download link as Billing Reports. See PIPELINE-SKIPPED-TESTS.md.
  736 |                 test.skip(testInfo.project.name === 'webkit', 'Script-triggered download emits no download event on WebKit.');
  737 |                 const [download] = await Promise.all([
  738 |                     page.waitForEvent('download', { timeout: 30000 }),
  739 |                     pageManager.decisionFilesPage.FIRST_DOWNLOAD_LINK.click(),
  740 |                 ]);
  741 |                 expect(download.suggestedFilename()).not.toBe('');
  742 |             });
  743 | 
  744 |             test('View opens the file log', async ({ page, pageManager }) => {
  745 |                 const decisionFiles = pageManager.decisionFilesPage;
  746 |                 const fileId = (await decisionFiles.cellByHeader(0, 'ID').innerText()).trim();
  747 | 
  748 |                 await decisionFiles.GRID_ROWS.first().getByRole('link', { name: /View/ }).click();
  749 |                 await expect(page).toHaveURL(new RegExp(`/client-admin/decision-files/logs\\?ReportId=${fileId}`), { timeout: 15000 });
  750 |                 for (const header of DecisionFilesPage.EXPECTED_LOG_COLUMN_HEADERS) {
  751 |                     await expect(decisionFiles.columnHeader(header), `Header "${header}"`).toBeVisible({ timeout: 15000 });
  752 |                 }
  753 |                 await expect(decisionFiles.GRID_ROWS.first().locator('td').first()).toHaveText(fileId, { timeout: 15000 });
  754 |             });
  755 | 
  756 |         });
  757 | 
  758 |         test.describe('File Setups', () => {
  759 | 
  760 |             test.beforeEach('Open Decision File settings', async ({ page, pageManager }) => {
  761 |                 await page.goto('/client-admin/decision-files/settings');
  762 |                 await expect(pageManager.decisionFilesPage.GRID_ROWS.first().getByRole('link', { name: /Edit/ })).toBeVisible({ timeout: 15000 });
  763 |             });
  764 | 
  765 |             test('Add New opens an empty file-setup form for the chosen product', async ({ page, pageManager }) => {
  766 |                 const decisionFiles = pageManager.decisionFilesPage;
  767 |                 await decisionFiles.ADD_NEW_BUTTON.click();
  768 |                 await decisionFiles.productButton('Check').click();
  769 | 
  770 |                 await expect(page).toHaveURL(/\/client-admin\/decision-files\/add-new-setting\/\d+$/, { timeout: 15000 });
  771 |                 await expect(pageManager.settingsPage.BREADCRUMB_CURRENT).toHaveText('[Add New]', { timeout: 15000 });
  772 |                 await expect(decisionFiles.FILE_NAME_TEXTBOX).toHaveValue('');
  773 |                 await expect(decisionFiles.SAVE_SETTINGS_BUTTON).toBeVisible();
  774 |             });
  775 | 
  776 |             test('Edit opens an existing file setup populated', async ({ page, pageManager }) => {
  777 |                 const decisionFiles = pageManager.decisionFilesPage;
  778 |                 const setupName = (await decisionFiles.cellByHeader(0, 'Name').innerText()).trim();
  779 | 
  780 |                 await decisionFiles.GRID_ROWS.first().getByRole('link', { name: /Edit/ }).click();
  781 |                 await expect(page).toHaveURL(/\/client-admin\/decision-files\/setting\/\d+$/, { timeout: 15000 });
  782 |                 await expect(decisionFiles.FILE_NAME_TEXTBOX).toHaveValue(setupName, { timeout: 15000 });
  783 |                 await expect(pageManager.settingsPage.BREADCRUMB_CURRENT).toHaveText(setupName);
  784 |                 await expect(decisionFiles.SAVE_SETTINGS_BUTTON).toBeVisible();
  785 |             });
  786 | 
  787 |         });
  788 | 
  789 |     });
  790 | 
  791 |     // ── Holiday Schedules ──────────────────────────────────────────────────────
  792 | 
  793 |     test.describe('Holiday Schedules', () => {
  794 | 
  795 |         test.beforeEach('Open Holiday Schedules', async ({ page, pageManager }) => {
  796 |             await page.goto('/client-admin/holiday-schedules');
  797 |             await expect(pageManager.holidaySchedulesPage.FEDERAL_HOLIDAYS_HEADER).toBeVisible({ timeout: 15000 });
  798 |         });
  799 | 
  800 |         test('Weekend/Holiday schedule toggle and description are shown', async ({ pageManager }) => {
  801 |             const holidays = pageManager.holidaySchedulesPage;
  802 |             await expect(holidays.ENABLE_SCHEDULE_LABEL).toBeVisible();
  803 |             await expect(holidays.ENABLE_SCHEDULE_TOGGLE).toBeAttached();
  804 |             await expect(holidays.SCHEDULE_DESCRIPTION).toBeVisible();
  805 |         });
  806 | 
  807 |         test('All federal holidays are listed', async ({ pageManager }) => {
  808 |             const holidays = pageManager.holidaySchedulesPage;
  809 |             await expect(holidays.FEDERAL_HOLIDAY_CHECKBOXES).toHaveCount(HolidaySchedulesPage.FEDERAL_HOLIDAYS.length);
  810 |             for (const holiday of HolidaySchedulesPage.FEDERAL_HOLIDAYS) {
  811 |                 await expect(holidays.federalHolidayCheckbox(holiday), `Holiday "${holiday}"`).toBeVisible();
  812 |             }
  813 |         });
  814 | 
  815 |         test('Custom holiday entry form is available', async ({ pageManager }) => {
  816 |             const holidays = pageManager.holidaySchedulesPage;
  817 |             await expect(holidays.CUSTOM_HOLIDAYS_HEADER).toBeVisible();
  818 |             await expect(holidays.CUSTOM_HOLIDAY_NAME_TEXTBOX).toBeVisible();
  819 |             await expect(holidays.CUSTOM_HOLIDAY_DATE_INPUT).toBeVisible();
  820 |             await expect(holidays.CUSTOM_HOLIDAY_REPEAT_DROPDOWN).toBeVisible();
  821 |             await expect(holidays.ADD_HOLIDAY_BUTTON).toBeVisible();
  822 |         });
  823 | 
  824 |         test('Add Holiday with Name and Date empty is blocked with a message', async ({ pageManager }) => {
  825 |             const holidays = pageManager.holidaySchedulesPage;
  826 |             const settings = pageManager.settingsPage;
  827 | 
  828 |             await holidays.ADD_HOLIDAY_BUTTON.click();
  829 |             await expect(settings.MODAL).toContainText('Please provide holiday name and date', { timeout: 10000 });
```