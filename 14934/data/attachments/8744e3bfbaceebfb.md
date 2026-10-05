# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\1-LoginSmoke.spec.ts >> Login — Smoke >> Forgot Password >> Validate forgot password with unregistered email
- Location: specs\Smoke\1-LoginSmoke.spec.ts:84:5

# Error details

```
Error: expect(locator).toBeVisible() failed

Locator: locator('div.alert.alert-danger')
Expected: visible
Timeout: 10000ms
Error: element(s) not found

Call log:
  - Expect "toBeVisible" with timeout 10000ms
  - waiting for locator('div.alert.alert-danger')

```

```yaml
- dialog:
  - heading "System Message" [level=3]
  - paragraph: Please enter your email address before continue
  - button "OK"
- main:
  - heading [level=1]:
    - img
  - text:   Forgot Password Your Email Address
  - textbox "Email Address"
  - link "Submit":
    - /url: "#"
```

# Test source

```ts
  1   | import { Locator } from '../../utility/index';
  2   | import {test, expect} from '../../utility/fixture';
  3   | import Constants from '../../utility/Constants';
  4   | import { loginCases, CaseName } from '../../test-data/Login/loginCases';
  5   | 
  6   | 
  7   | test.describe('Login — Smoke', () => {
  8   | 
  9   |   // ── Login ──────────────────────────────────────────────────────────────────
  10  | 
  11  |   test.describe('Login', () => {
  12  | 
  13  |     for (const scenarioName in loginCases) {
  14  | 
  15  |       const caseData = loginCases[scenarioName as CaseName];
  16  | 
  17  |       test(`Validate Login functionality with ${scenarioName}`, async ({ pageManager }) => {
  18  | 
  19  |         // Step 1: Go to login page
  20  |         // Step 2: Enter username and password
  21  |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  22  |         await pageManager.loginPage.login(caseData.username(),caseData.password());
  23  | 
  24  |         // Step 3: Validate based on scenario
  25  |         if (scenarioName === 'correctCredentials' || scenarioName === 'caseSensitiveEmail') {
  26  | 
  27  |           await expect(pageManager.homePage.homePageLogo).toBeVisible({ timeout: 20000 });
  28  | 
  29  |         } else if (scenarioName === 'incorrectPassword') {
  30  | 
  31  |           const message = await pageManager.loginPage.invalidCredentialMessage();
  32  |           expect(message?.trim()).toEqual('Invalid password');
  33  | 
  34  |         } else if (scenarioName === 'incorrectUsername' || scenarioName === 'invalidEmailFormat') {
  35  | 
  36  |           const message = await pageManager.loginPage.invalidCredentialMessage();
  37  |           expect(message?.trim()).toEqual('Invalid email address');
  38  | 
  39  |         } else if (
  40  |           scenarioName === 'emptyFields' ||
  41  |           scenarioName === 'missingPassword' ||
  42  |           scenarioName === 'missingUsername'
  43  |         ) {
  44  | 
  45  |           const message = await pageManager.loginPage.enterRequiredFieldMessage();
  46  |           expect(message).toEqual('Please enter all required fields');
  47  | 
  48  |         } else if (
  49  |           scenarioName === 'sqlInjection' ||
  50  |           scenarioName === 'xssInUsername' ||
  51  |           scenarioName === 'veryLongInput'
  52  |         ) {
  53  | 
  54  |           // Security tests: verify login was rejected (credential alert visible, no navigation to dashboard)
  55  |           await expect(pageManager.loginPage.credentialAlertMessage).toBeVisible({ timeout: 10000 });
  56  |         }
  57  |       });
  58  |     }
  59  | 
  60  |   });
  61  | 
  62  |   // ── Forgot password ────────────────────────────────────────────────────────
  63  | 
  64  |   test.describe('Forgot Password', () => {
  65  | 
  66  |     test('Validate forgot password functionality', async ({pageManager}) =>{
  67  |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  68  |         await pageManager.loginPage.clickOnForgotPasswordButton();
  69  |       await pageManager.loginPage.enterUsername(Constants.USER_FI_EMAIL);
  70  |         await pageManager.loginPage.clickOnForgotPasswordSubmitButon();
  71  |         const alertMessageOnForgetPassPage:Locator = pageManager.loginPage.credentialAlertMessage;
  72  |         await expect(alertMessageOnForgetPassPage).toContainText('An email will be sent to your email address shortly.',{timeout:10000})
  73  |     })
  74  | 
  75  |     test('Validate forgot password functionality with No email', async ({pageManager}) =>{
  76  |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  77  |         await pageManager.loginPage.clickOnForgotPasswordButton();
  78  |         await pageManager.loginPage.enterUsername('');
  79  |         await pageManager.loginPage.clickOnForgotPasswordSubmitButon();
  80  |         const alertMessageOnForgetPassPage:string | undefined =await pageManager.loginPage.enterRequiredFieldMessage();
  81  |         expect(alertMessageOnForgetPassPage).toEqual('Please enter your email address before continue');
  82  |     })
  83  | 
  84  |     test('Validate forgot password with unregistered email', async ({pageManager}) =>{
  85  |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  86  |         await pageManager.loginPage.clickOnForgotPasswordButton();
  87  |         await pageManager.loginPage.enterUsername('unregistered.user.99999@example.com');
  88  |         await pageManager.loginPage.clickOnForgotPasswordSubmitButon();
> 89  |         await expect(pageManager.loginPage.credentialAlertMessage).toBeVisible({ timeout: 10000 });
      |                                                                    ^ Error: expect(locator).toBeVisible() failed
  90  |     })
  91  | 
  92  |   });
  93  | 
  94  |   // ── Session & security ─────────────────────────────────────────────────────
  95  | 
  96  |   test.describe('Session & Security', () => {
  97  | 
  98  |     test('Validate session persists after page refresh', async ({pageManager}) =>{
  99  |         await pageManager.loginPage.navigateToLoginPage('/auth/login');
  100 |         await pageManager.loginPage.login(
  101 |         Constants.USER_FI_EMAIL,
  102 |         Constants.USER_FI_PASSWORD
  103 |         );
  104 |         await expect(pageManager.homePage.homePageLogo).toBeVisible({ timeout: 20000 });
  105 |         await pageManager.loginPage.page.reload();
  106 |         await expect(pageManager.homePage.homePageLogo).toBeVisible({ timeout: 20000 });
  107 |     })
  108 | 
  109 |     test('Validate unauthenticated access to protected route is redirected to login', async ({pageManager, page}) =>{
  110 |         // Navigate directly to a protected route without logging in
  111 |         await pageManager.loginPage.navigateToLoginPage('/issued-checks');
  112 |         // App should redirect to the login page — verify login form is present
  113 |         await expect(pageManager.loginPage.email).toBeVisible({ timeout: 10000 });
  114 |         await expect(pageManager.loginPage.loginButton).toBeVisible({ timeout: 10000 });
  115 |         // Confirm we are NOT on the protected route — web-first assertion, auto-retries
  116 |         // instead of reading page.url() once at whatever instant the redirect may still be in flight.
  117 |         await expect(page).not.toHaveURL(/\/issued-checks/, { timeout: 10000 });
  118 |     })
  119 | 
  120 |   });
  121 | 
  122 | });
  123 | 
  124 | 
  125 | 
```