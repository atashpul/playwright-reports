# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Legacy\Settings\Account\AccountSettingsPage.spec.ts >> Account Settings - Header & Field Visibility Validation >> @settings All section headers are visible
- Location: specs\Legacy\Settings\Account\AccountSettingsPage.spec.ts:56:3

# Error details

```
TimeoutError: locator.fill: Timeout 30000ms exceeded.
Call log:
  - waiting for getByRole('textbox', { name: 'Email Address' })

```

# Page snapshot

```yaml
- generic [active] [ref=e1]:
  - heading "502 Bad Gateway" [level=1] [ref=e3]
  - separator [ref=e4]
  - generic [ref=e5]: Microsoft-Azure-Application-Gateway/v2
```

# Test source

```ts
  1   | import { test, expect } from "@playwright/test";
  2   | import Constants from "../../../../utility/Constants";
  3   | import LoginPage from "../../../../page-object/Login/Login";
  4   | import NavigationTabs from "../../../../page-object/Navigations/NavigationTabs";
  5   | import SettingsPage from "../../../../page-object/Settings/SettingsPage";
  6   | import AccountSettingsPage from "../../../../page-object/Settings/AccountSettingsPage";
  7   | 
  8   | /**
  9   |  * Expected counts per section (cross-check on each run; failure => a field was added/removed).
  10  |  *   Account Settings        : 10 fields
  11  |  *   Security Settings       :  2 fields
  12  |  *   Check Settings          :  4 fields
  13  |  *   ACH Settings            :  3 fields
  14  |  *   Business Client Settings:  3 fields
  15  |  */
  16  | const EXPECTED_COUNTS = {
  17  |   accountSettings: 10,
  18  |   securitySettings: 2,
  19  |   checkSettings: 4,
  20  |   achSettings: 3,
  21  |   businessClientSettings: 3,
  22  | };
  23  | 
  24  | async function waitForAccountSettingsReady(accountSettings: AccountSettingsPage) {
  25  |   await expect(accountSettings.ACCOUNT_SETTINGS_HEADER).toBeVisible({ timeout: 20000 });
  26  |   await expect(accountSettings.BUSINESS_NAME_LABEL).toBeVisible({ timeout: 20000 });
  27  |   await expect(accountSettings.TIME_ZONE_DROPDOWN).toBeVisible({ timeout: 20000 });
  28  | }
  29  | 
  30  | test.describe("Account Settings - Header & Field Visibility Validation", () => {
  31  |   let loginPage: LoginPage;
  32  |   let navigationTabs: NavigationTabs;
  33  |   let settingsPage: SettingsPage;
  34  |   let accountSettings: AccountSettingsPage;
  35  | 
  36  |   test.beforeEach(async ({ page }) => {
  37  |     loginPage = new LoginPage(page);
  38  |     navigationTabs = new NavigationTabs(page);
  39  |     settingsPage = new SettingsPage(page);
  40  |     accountSettings = new AccountSettingsPage(page);
  41  | 
  42  |     await page.goto(Constants.BASE_URL,{waitUntil:'domcontentloaded',timeout:150000});
  43  |     await page.waitForTimeout(7000);
> 44  |     await loginPage.EMAIL_TEXTBOX.fill(Constants.USER_FI_EMAIL);
      |                                   ^ TimeoutError: locator.fill: Timeout 30000ms exceeded.
  45  |     await loginPage.PASSWORD_TEXTBOX.fill(Constants.USER_FI_PASSWORD);
  46  |     await loginPage.LOGIN_BUTTON.click();
  47  | 
  48  |     await expect(navigationTabs.SETTINGS_TAB).toBeVisible({ timeout: 30000 });
  49  |     // Navigate Settings → Account Settings using existing POMs
  50  |     await navigationTabs.SETTINGS_TAB.click();
  51  |     await expect(navigationTabs.SETTINGS_ASSERTIONS).toBeVisible();
  52  |     await settingsPage.ACCOUNT_SETTINGS_LINK.click();
  53  |     await waitForAccountSettingsReady(accountSettings);
  54  |   });
  55  | 
  56  |   test("@settings All section headers are visible", async () => {
  57  |     await expect(accountSettings.ACCOUNT_SETTINGS_HEADER).toBeVisible();
  58  |     await expect(accountSettings.SECURITY_SETTINGS_HEADER).toBeVisible();
  59  |     await expect(accountSettings.PRODUCT_BUSINESS_SETTINGS_HEADER).toBeVisible();
  60  |     await expect(accountSettings.CHECK_SETTINGS_HEADER).toBeVisible();
  61  |     await expect(accountSettings.ACH_SETTINGS_HEADER).toBeVisible();
  62  |     await expect(accountSettings.BUSINESS_CLIENT_SETTINGS_HEADER).toBeVisible();
  63  |   });
  64  | 
  65  |   test("Account Settings - all 10 fields are visible", async () => {
  66  |     await expect(accountSettings.BUSINESS_NAME_LABEL).toBeVisible();
  67  |     await expect(accountSettings.BUSINESS_NAME_TEXTBOX).toBeVisible();
  68  | 
  69  |     await expect(accountSettings.CLIENT_ID_LABEL).toBeVisible();
  70  |     await expect(accountSettings.CLIENT_ID_TEXTBOX).toBeVisible();
  71  | 
  72  |     await expect(accountSettings.TIME_ZONE_LABEL).toBeVisible();
  73  |     await expect(accountSettings.TIME_ZONE_DROPDOWN).toBeVisible();
  74  | 
  75  |     await expect(accountSettings.DEFAULT_ROUTING_NUMBER_LABEL).toBeVisible();
  76  |     await expect(accountSettings.DEFAULT_ROUTING_NUMBER_TEXTBOX).toBeVisible();
  77  | 
  78  |     await expect(accountSettings.SUPPORT_EMAIL_LABEL).toBeVisible();
  79  |     await expect(accountSettings.SUPPORT_EMAIL_TEXTBOX).toBeVisible();
  80  | 
  81  |     await expect(accountSettings.REQUIRE_DECISION_NOTES_LABEL).toBeVisible();
  82  |     await expect(accountSettings.HIDE_HEADER_FOOTER_LABEL).toBeVisible();
  83  |     await expect(accountSettings.IFRAME_SAMPLE_LINK).toBeVisible();
  84  |     await expect(accountSettings.DISABLE_ALL_NOTIFICATIONS_LABEL).toBeVisible();
  85  |     await expect(accountSettings.HIDE_LOGOUT_LABEL).toBeVisible();
  86  |     await expect(accountSettings.WELCOME_EMAIL_DEFAULT_LABEL).toBeVisible();
  87  |   });
  88  | 
  89  |   test("Security Settings - all 2 fields are visible", async () => {
  90  |     await expect(accountSettings.ENABLE_MFA_LABEL).toBeVisible();
  91  |     await expect(accountSettings.AUTO_LOGOUT_TIME_LABEL).toBeVisible();
  92  |     await expect(accountSettings.AUTO_LOGOUT_TIME_DROPDOWN).toBeVisible();
  93  |   });
  94  | 
  95  |   test("Check Settings - all 4 fields are visible", async () => {
  96  |     await expect(accountSettings.CHECK_DEFAULT_DECISION_CUTOFF_TIME_LABEL).toBeVisible();
  97  |     await expect(accountSettings.CHECK_DEFAULT_DECISION_CUTOFF_TIME_DROPDOWN).toBeVisible();
  98  | 
  99  |     await expect(accountSettings.CHECK_DEFAULT_DECISION_GRACE_PERIOD_LABEL).toBeVisible();
  100 |     await expect(accountSettings.CHECK_DEFAULT_DECISION_GRACE_PERIOD_DROPDOWN).toBeVisible();
  101 | 
  102 |     await expect(accountSettings.CHECK_ENABLE_RETURN_REASON_LABEL).toBeVisible();
  103 |     await expect(accountSettings.CHECK_CONFIGURE_REASONS_LINK).toBeVisible();
  104 | 
  105 |     await expect(accountSettings.PAYEE_MATCH_CONFIDENCE_THRESHOLD_LABEL).toBeVisible();
  106 |     await expect(accountSettings.PAYEE_MATCH_CONFIDENCE_THRESHOLD_DROPDOWN).toBeVisible();
  107 |   });
  108 | 
  109 |   test("ACH Settings - all 3 fields are visible", async () => {
  110 |     await expect(accountSettings.ACH_DEFAULT_DECISION_CUTOFF_TIME_LABEL).toBeVisible();
  111 |     await expect(accountSettings.ACH_DEFAULT_DECISION_CUTOFF_TIME_DROPDOWN).toBeVisible();
  112 | 
  113 |     await expect(accountSettings.ACH_DEFAULT_DECISION_GRACE_PERIOD_LABEL).toBeVisible();
  114 |     await expect(accountSettings.ACH_DEFAULT_DECISION_GRACE_PERIOD_DROPDOWN).toBeVisible();
  115 | 
  116 |     await expect(accountSettings.ACH_ENABLE_RETURN_REASON_LABEL).toBeVisible();
  117 |     await expect(accountSettings.ACH_CONFIGURE_REASONS_LINK).toBeVisible();
  118 |   });
  119 | 
  120 |   test("Business Client Settings - all 3 fields are visible", async () => {
  121 |     await expect(accountSettings.ALLOW_CUSTOM_EMAIL_TEMPLATES_LABEL).toBeVisible();
  122 |     await expect(accountSettings.ALLOW_CUSTOM_ISSUED_CHECK_FILE_FORMAT_LABEL).toBeVisible();
  123 |     await expect(accountSettings.BC_HIDE_LOGOUT_LABEL).toBeVisible();
  124 |   });
  125 | 
  126 |   test("Save Changes button is visible", async () => {
  127 |     await expect(accountSettings.SAVE_CHANGES_BUTTON).toBeVisible();
  128 |   });
  129 | 
  130 |   test("Cross-check field counts under each header (detects added/removed fields)", async () => {
  131 |     // Retry counts until they stabilize (handles late hydration of toggles/selects).
  132 |     // expect.poll itself asserts the value matches; no separate expect() block needed.
  133 |     await expect.poll(async () => accountSettings.ACCOUNT_SETTINGS_FIELDS.count(), { timeout: 15000 })
  134 |       .toBe(EXPECTED_COUNTS.accountSettings);
  135 |     await expect.poll(async () => accountSettings.SECURITY_SETTINGS_FIELDS.count(), { timeout: 15000 })
  136 |       .toBe(EXPECTED_COUNTS.securitySettings);
  137 |     await expect.poll(async () => accountSettings.CHECK_SETTINGS_FIELDS.count(), { timeout: 15000 })
  138 |       .toBe(EXPECTED_COUNTS.checkSettings);
  139 |     await expect.poll(async () => accountSettings.ACH_SETTINGS_FIELDS.count(), { timeout: 15000 })
  140 |       .toBe(EXPECTED_COUNTS.achSettings);
  141 |     await expect.poll(async () => accountSettings.BUSINESS_CLIENT_SETTINGS_FIELDS.count(), { timeout: 15000 })
  142 |       .toBe(EXPECTED_COUNTS.businessClientSettings);
  143 | 
  144 |     // Log actual counts for cross-checking against any future field additions/removals.
```