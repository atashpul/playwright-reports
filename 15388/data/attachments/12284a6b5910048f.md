# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\9-AccountSettingsSmoke.spec.ts >> Settings — Account Section Smoke >> Account Settings >> Dropdowns show their saved values
- Location: specs\Smoke\9-AccountSettingsSmoke.spec.ts:75:9

# Error details

```
Error: expect(locator).not.toHaveText(expected) failed

Locator: locator('xpath=(//*[normalize-space(text())=\'Notification Methods\'])[1]/following::select[1]').locator('option:checked')
Expected: not ""
Timeout: 30000ms
Error: element(s) not found

Call log:
  - Expect "not toHaveText" with timeout 30000ms
  - waiting for locator('xpath=(//*[normalize-space(text())=\'Notification Methods\'])[1]/following::select[1]').locator('option:checked')

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
    - link "Settings":
      - /url: /client-admin
  - listitem:
    - link "Info":
      - /url: javascript:;
- group:
  - text:  Account Settings Business Name *
  - textbox "Business Name": FI Playwright Automation
  - text: Client Id
  - textbox "Client Identifier" [disabled]
  - text: Time Zone *
  - combobox:
    - option "Alaska Time"
    - option "Arizona Time"
    - option "Central Time"
    - option "Eastern Time" [selected]
    - option "Hawaii Time"
    - option "Mountain Time"
    - option "Pacific Time"
  - text: Default Routing Number
  - textbox "Default Routing Number": "231382306"
  - text: Support Email * 
  - textbox "Support Email": pjakati@advancedfraudsolutions.com
  - text: Require Decision Notes 
  - checkbox "No"
  - text: No Hide Header and Footer 
  - checkbox "No"
  - text: "No"
  - link "Iframe Sample":
    - /url: /static/iframe.html
  - text: Disable All Notifications 
  - checkbox "No"
  - text: No Hide Logout 
  - checkbox "No"
  - text: No Welcome Email Default 
  - checkbox "No"
  - text: No Security Settings Enable MFA 
  - checkbox "No"
  - text: No Auto Logout Time 
  - combobox:
    - option "5 Minutes"
    - option "10 Minutes"
    - option "15 Minutes"
    - option "30 Minutes"
    - option "1 Hour (Default)" [selected]
    - option "2 Hours"
    - option "4 Hours"
  - text:   Product/Business Settings
  - group:
    - text: Check Settings Check Default Decision Cutoff Time 
    - combobox:
      - option "8 AM" [selected]
      - option "9 AM"
      - option "10 AM"
      - option "11 AM (Default)"
      - option "12 PM"
      - option "1 PM"
      - option "2 PM"
      - option "3 PM"
      - option "4 PM"
      - option "5 PM"
      - option "6 PM"
      - option "7 PM"
      - option "8 PM"
      - option "9 PM"
      - option "10 PM"
      - option "11 PM"
      - option "12 AM"
    - text: Check Default Decision Grace Period 
    - combobox:
      - option "0 Hour"
      - option "1 Hour" [selected]
      - option "2 Hours"
      - option "3 Hours"
      - option "4 Hours (Default)"
      - option "5 Hours"
      - option "6 Hours"
      - option "7 Hours"
      - option "8 Hours"
    - text: Enable Return Reason 
    - checkbox "Yes" [checked]
    - text: "Yes"
    - link "Configure Reasons":
      - /url: javascript:;
    - text: Payee Match Confidence Threshold 
    - combobox:
      - option "0"
      - option "1"
      - option "2"
      - option "3"
      - option "4"
      - option "5"
      - option "6"
      - option "7"
      - option "8"
      - option "9"
      - option "10"
      - option "11"
      - option "12"
      - option "13"
      - option "14"
      - option "15"
      - option "16"
      - option "17"
      - option "18"
      - option "19"
      - option "20"
      - option "21"
      - option "22"
      - option "23"
      - option "24"
      - option "25"
      - option "26"
      - option "27"
      - option "28"
      - option "29"
      - option "30"
      - option "31"
      - option "32"
      - option "33"
      - option "34"
      - option "35"
      - option "36"
      - option "37"
      - option "38"
      - option "39"
      - option "40"
      - option "41"
      - option "42"
      - option "43"
      - option "44"
      - option "45"
      - option "46"
      - option "47"
      - option "48"
      - option "49"
      - option "50"
      - option "51"
      - option "52"
      - option "53"
      - option "54"
      - option "55"
      - option "56"
      - option "57"
      - option "58"
      - option "59"
      - option "60"
      - option "61"
      - option "62"
      - option "63"
      - option "64"
      - option "65"
      - option "66"
      - option "67"
      - option "68"
      - option "69"
      - option "70" [selected]
      - option "71"
      - option "72"
      - option "73"
      - option "74"
      - option "75"
      - option "76"
      - option "77"
      - option "78"
      - option "79"
      - option "80"
      - option "81"
      - option "82"
      - option "83"
      - option "84"
      - option "85"
      - option "86"
      - option "87"
      - option "88"
      - option "89"
      - option "90"
      - option "91"
      - option "92"
      - option "93"
      - option "94"
      - option "95"
      - option "96"
      - option "97"
      - option "98"
      - option "99"
      - option "100"
  - group:
    - text: ACH Settings ACH Default Decision Cutoff Time 
    - combobox:
      - option "8 AM"
      - option "9 AM"
      - option "10 AM"
      - option "11 AM (Default)"
      - option "12 PM"
      - option "1 PM"
      - option "2 PM"
      - option "3 PM"
      - option "4 PM" [selected]
      - option "5 PM"
      - option "6 PM"
      - option "7 PM"
      - option "8 PM"
      - option "9 PM"
      - option "10 PM"
      - option "11 PM"
      - option "12 AM"
    - text: ACH Default Decision Grace Period 
    - combobox:
      - option "0 Hour"
      - option "1 Hour" [selected]
      - option "2 Hours"
      - option "3 Hours"
      - option "4 Hours (Default)"
      - option "5 Hours"
      - option "6 Hours"
      - option "7 Hours"
      - option "8 Hours"
    - text: Enable Return Reason 
    - checkbox "Yes" [checked]
    - text: "Yes"
    - link "Configure Reasons":
      - /url: javascript:;
  - text: Business Client Settings Allow Custom Email Templates 
  - checkbox "No"
  - text: No Allow Custom Issued Check File Format 
  - checkbox "Yes" [checked]
  - text: Yes Hide Logout 
  - checkbox "Yes" [checked]
  - text: "Yes"
  - button " Save Changes"
- contentinfo:
  - text: FI Playwright Automation[uat-release] © Copyright Advanced Fraud Solutions 2005-2026 | All Rights Reserved |
  - link "Privacy Policy":
    - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  1   | import { test, expect } from '../../utility/fixture';
  2   | import Constants from '../../utility/Constants';
  3   | import BusinessClientsPage from '../../page-object/Settings/BusinessClientsPage';
  4   | import UsersPage from '../../page-object/Settings/UsersPage';
  5   | import RolesPermissionsPage from '../../page-object/Settings/RolesPermissionsPage';
  6   | import BillingReportsPage from '../../page-object/Settings/BillingReportsPage';
  7   | import DecisionFilesPage from '../../page-object/Settings/DecisionFilesPage';
  8   | import HolidaySchedulesPage from '../../page-object/Settings/HolidaySchedulesPage';
  9   | import { getRandomNumberString, getFormattedDateAfterDays } from '../../utility/random';
  10  | import { captureSharedLogin, restoreSession, type CapturedAuth } from '../../utility/sessionAuth';
  11  | 
  12  | /**
  13  |  * Smoke tests — Settings > Account section.
  14  |  * Saves only re-save loaded values unchanged, and run on chromium only so the parallel browser jobs
  15  |  * don't repeat writes to shared tenant settings. Records the tests create (role, custom holiday)
  16  |  * are cleaned up.
  17  |  */
  18  | 
  19  | // One shared login for the whole file (per worker); every test replays it into its own
  20  | // fresh context and navigates to its own page below.
  21  | let auth: CapturedAuth;
  22  | 
  23  | test.beforeAll('Log in once and capture the session', async ({ browser }) => {
  24  |     auth = await captureSharedLogin(browser);
  25  | });
  26  | 
  27  | test.beforeEach('Restore the captured session', async ({ context }) => {
  28  |     await restoreSession(context, auth);
  29  | });
  30  | 
  31  | test.describe('Settings — Account Section Smoke', () => {
  32  | 
  33  |     // ── Account Settings ───────────────────────────────────────────────────────
  34  | 
  35  |     test.describe('Account Settings', () => {
  36  | 
  37  |         test.beforeEach('Open Account Settings', async ({ page, pageManager }) => {
  38  |             await page.goto('/client-admin/info');
  39  |             await expect(pageManager.accountSettingsPage.BUSINESS_NAME_TEXTBOX).not.toHaveValue('', { timeout: 15000 });
  40  |         });
  41  | 
  42  |         test('All section headers are visible', async ({ pageManager }) => {
  43  |             const accountSettings = pageManager.accountSettingsPage;
  44  |             await expect(accountSettings.ACCOUNT_SETTINGS_HEADER).toBeVisible();
  45  |             await expect(accountSettings.SECURITY_SETTINGS_HEADER).toBeVisible();
  46  |             await expect(accountSettings.PRODUCT_BUSINESS_SETTINGS_HEADER).toBeVisible();
  47  |             await expect(accountSettings.CHECK_SETTINGS_HEADER).toBeVisible();
  48  |             await expect(accountSettings.ACH_SETTINGS_HEADER).toBeVisible();
  49  |             await expect(accountSettings.BUSINESS_CLIENT_SETTINGS_HEADER).toBeVisible();
  50  |         });
  51  | 
  52  |         test('Required fields are populated and Client Id is read-only', async ({ pageManager }) => {
  53  |             const accountSettings = pageManager.accountSettingsPage;
  54  |             await expect(accountSettings.SUPPORT_EMAIL_TEXTBOX).not.toHaveValue('');
  55  |             await expect(accountSettings.TIME_ZONE_DROPDOWN).not.toHaveValue('');
  56  |             await expect(accountSettings.CLIENT_ID_TEXTBOX).toBeDisabled();
  57  |         });
  58  | 
  59  |         test('Save Changes with no edits succeeds and keeps the values', async ({ page, pageManager }, testInfo) => {
  60  |             // Re-saves tenant-wide settings; run on one browser only so parallel browser jobs don't
  61  |             // multiply the write window over changes made by other suites or users.
  62  |             test.skip(testInfo.project.name !== 'chromium', 'Writes shared tenant settings; runs on chromium only.');
  63  |             const accountSettings = pageManager.accountSettingsPage;
  64  |             const businessName = await accountSettings.BUSINESS_NAME_TEXTBOX.inputValue();
  65  |             const supportEmail = await accountSettings.SUPPORT_EMAIL_TEXTBOX.inputValue();
  66  | 
  67  |             await accountSettings.SAVE_CHANGES_BUTTON.click();
  68  |             await expect(accountSettings.SAVE_SUCCESS_TOAST).toBeVisible({ timeout: 15000 });
  69  | 
  70  |             await page.goto('/client-admin/info');
  71  |             await expect(accountSettings.BUSINESS_NAME_TEXTBOX).toHaveValue(businessName, { timeout: 15000 });
  72  |             await expect(accountSettings.SUPPORT_EMAIL_TEXTBOX).toHaveValue(supportEmail);
  73  |         });
  74  | 
  75  |         test('Dropdowns show their saved values', async ({ pageManager }) => {
  76  |             const accountSettings = pageManager.accountSettingsPage;
  77  |             const dropdowns = [
  78  |                 accountSettings.FI_NOTIFICATION_METHODS_DROPDOWN,
  79  |                 accountSettings.AUTO_LOGOUT_TIME_DROPDOWN,
  80  |                 accountSettings.CHECK_DEFAULT_DECISION_CUTOFF_TIME_DROPDOWN,
  81  |                 accountSettings.CHECK_DEFAULT_DECISION_GRACE_PERIOD_DROPDOWN,
  82  |                 accountSettings.PAYEE_MATCH_CONFIDENCE_THRESHOLD_DROPDOWN,
  83  |                 accountSettings.ACH_DEFAULT_DECISION_CUTOFF_TIME_DROPDOWN,
  84  |                 accountSettings.ACH_DEFAULT_DECISION_GRACE_PERIOD_DROPDOWN,
  85  |                 accountSettings.BC_NOTIFICATION_METHODS_DROPDOWN,
  86  |             ];
  87  |             for (const dropdown of dropdowns) {
> 88  |                 await expect(dropdown.locator('option:checked')).not.toHaveText('');
      |                                                                      ^ Error: expect(locator).not.toHaveText(expected) failed
  89  |             }
  90  |         });
  91  | 
  92  |         const requiredFields = [
  93  |             { name: 'Business Name', textbox: 'BUSINESS_NAME_TEXTBOX', message: 'Please enter business name' },
  94  |             { name: 'Support Email', textbox: 'SUPPORT_EMAIL_TEXTBOX', message: 'Please enter support email address' },
  95  |         ] as const;
  96  | 
  97  |         for (const field of requiredFields) {
  98  |             test(`Saving with ${field.name} empty is blocked with a message`, async ({ page, pageManager }) => {
  99  |                 const accountSettings = pageManager.accountSettingsPage;
  100 |                 const settings = pageManager.settingsPage;
  101 |                 const original = await accountSettings[field.textbox].inputValue();
  102 | 
  103 |                 await accountSettings[field.textbox].fill('');
  104 |                 await accountSettings.SAVE_CHANGES_BUTTON.click();
  105 |                 await expect(settings.MODAL).toContainText(field.message, { timeout: 10000 });
  106 |                 await settings.MODAL_OK_BUTTON.click();
  107 |                 await expect(settings.MODAL).toBeHidden();
  108 | 
  109 |                 await page.goto('/client-admin/info');
  110 |                 await expect(accountSettings[field.textbox]).toHaveValue(original, { timeout: 15000 });
  111 |             });
  112 |         }
  113 | 
  114 |         const reasonLinks = [
  115 |             { product: 'Check', link: 'CHECK_CONFIGURE_REASONS_LINK' },
  116 |             { product: 'ACH', link: 'ACH_CONFIGURE_REASONS_LINK' },
  117 |         ] as const;
  118 | 
  119 |         for (const reason of reasonLinks) {
  120 |             test(`${reason.product} Configure Reasons opens the return-reason dialog`, async ({ pageManager }) => {
  121 |                 const accountSettings = pageManager.accountSettingsPage;
  122 |                 const settings = pageManager.settingsPage;
  123 | 
  124 |                 await accountSettings[reason.link].click();
  125 |                 await expect(settings.MODAL_TITLE).toHaveText('Configure Return Reasons', { timeout: 10000 });
  126 |                 await expect(settings.MODAL).toContainText(`making ${reason.product} decisions`);
  127 |                 await expect.poll(async () => accountSettings.RETURN_REASON_CHECKBOXES.count()).toBeGreaterThan(0);
  128 | 
  129 |                 await settings.MODAL_CANCEL_BUTTON.click();
  130 |                 await expect(settings.MODAL).toBeHidden();
  131 |             });
  132 |         }
  133 | 
  134 |         test('Iframe Sample link opens the sample page in a new tab', async ({ page, pageManager }) => {
  135 |             const [popup] = await Promise.all([
  136 |                 page.waitForEvent('popup'),
  137 |                 pageManager.accountSettingsPage.IFRAME_SAMPLE_LINK.click(),
  138 |             ]);
  139 |             await expect(popup).toHaveURL(/\/static\/iframe\.html$/, { timeout: 15000 });
  140 |             await popup.close();
  141 |         });
  142 | 
  143 |     });
  144 | 
  145 |     // ── Business Clients ───────────────────────────────────────────────────────
  146 | 
  147 |     test.describe('Business Clients', () => {
  148 | 
  149 |         test.beforeEach('Open Business Clients', async ({ page, pageManager }) => {
  150 |             await page.goto('/client-admin/business-clients');
  151 |             await expect(pageManager.businessClientsPage.cellByHeader(0, 'Client Name').getByRole('link')).toBeVisible({ timeout: 15000 });
  152 |         });
  153 | 
  154 |         test('Grid loads with all column headers', async ({ pageManager }) => {
  155 |             const businessClients = pageManager.businessClientsPage;
  156 |             await expect(businessClients.COLUMN_HEADERS).toHaveCount(BusinessClientsPage.EXPECTED_COLUMN_HEADERS.length);
  157 |             for (const header of BusinessClientsPage.EXPECTED_COLUMN_HEADERS) {
  158 |                 await expect(businessClients.columnHeader(header), `Header "${header}"`).toBeVisible();
  159 |             }
  160 |         });
  161 | 
  162 |         test('Search filters the grid to the searched client', async ({ pageManager }) => {
  163 |             const businessClients = pageManager.businessClientsPage;
  164 |             const clientName = (await businessClients.cellByHeader(0, 'Client Name').innerText()).trim();
  165 | 
  166 |             await businessClients.SEARCH_TEXTBOX.fill(clientName);
  167 |             await expect(businessClients.rowByClientName(clientName)).toBeVisible({ timeout: 15000 });
  168 |             await expect.poll(async () => {
  169 |                 const rows = await businessClients.GRID_ROWS.allInnerTexts();
  170 |                 return rows.every((row) => row.toLowerCase().includes(clientName.toLowerCase()));
  171 |             }, { timeout: 15000 }).toBe(true);
  172 |         });
  173 | 
  174 |         test('Client name opens the edit form for that client', async ({ page, pageManager }) => {
  175 |             const clientLink = pageManager.businessClientsPage.cellByHeader(0, 'Client Name').getByRole('link');
  176 |             const clientName = (await clientLink.innerText()).trim();
  177 | 
  178 |             await clientLink.click();
  179 |             await expect(page).toHaveURL(/\/client-admin\/business-clients\/client\/\d+/, { timeout: 15000 });
  180 |             const editPage = pageManager.businessClientEditPage;
  181 |             await expect(editPage.BUSINESS_NAME_TEXTBOX).toHaveValue(clientName, { timeout: 15000 });
  182 |             await expect(editPage.ACCOUNT_SETTINGS_HEADER).toBeVisible();
  183 |             await expect(editPage.PRODUCT_SETTINGS_HEADER).toBeVisible();
  184 |             await expect(editPage.CHECK_SETTINGS_HEADER).toBeVisible();
  185 |             await expect(editPage.ACH_SETTINGS_HEADER).toBeVisible();
  186 |             await expect(editPage.SAVE_CHANGES_BUTTON).toBeVisible();
  187 |         });
  188 | 
```