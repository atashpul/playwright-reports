# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\7-ACHSmoke.spec.ts >> ACH — Smoke >> "Delete" on a row shows a confirm modal; Cancel dismisses it without deleting
- Location: specs\Smoke\7-ACHSmoke.spec.ts:266:5

# Error details

```
TimeoutError: locator.click: Timeout 30000ms exceeded.
Call log:
  - waiting for locator('button[type="submit"]')
    - locator resolved to <button type="submit" data-testid="login-submit" class="btn btn-lg btn-primary btn-block">Login to Positive Pay</button>
  - attempting click action
    - waiting for element to be visible, enabled and stable

```

# Page snapshot

```yaml
- main [ref=e2]:
  - heading [level=1] [ref=e4]
  - generic [ref=e7]:
    - generic [ref=e9]:
      - generic: Email *
      - textbox "Email Address" [ref=e10]: pjakati28+PP@gmail.com
    - generic [ref=e12]:
      - generic: Password *
      - textbox "Password" [active] [ref=e13]: Password123!
    - button "Login to Positive Pay" [ref=e15] [cursor=pointer]
    - link "Forgot Password?" [ref=e17]:
      - /url: /forgot-password/
```

# Test source

```ts
  70  |     }
  71  | 
  72  | 
  73  | 
  74  |     
  75  |      //This method performs click on forgot password button on login page
  76  |      
  77  |     async clickOnForgotPasswordButton(): Promise<void>{
  78  |         await this.forgotPasswordLink.click();
  79  |     }
  80  | 
  81  |     
  82  |     //This method performs click on submit button on forgot password page
  83  |     
  84  |     async clickOnForgotPasswordSubmitButon(): Promise<void>{
  85  |         await this.submitButtonOnForgotPasswordPage.click();
  86  |     }
  87  | 
  88  |     
  89  |     //This method returns invalid credential message
  90  |     //@returns 
  91  |     
  92  |     async invalidCredentialMessage(): Promise<string | null>{
  93  |        return await this.credentialAlertMessage.textContent();
  94  |     }
  95  | 
  96  |     
  97  |     //This method returns system alert message when input fields are empty
  98  |     //@returns 
  99  |     
  100 |     async enterRequiredFieldMessage(): Promise<string| undefined>{
  101 |         await this.systemMessage.waitFor({state:'visible'})
  102 |         const systemMessageText : string | null = await this.systemMessage.textContent();
  103 |         await this.okButtonOnSystemAlertWindow.click();
  104 |         return systemMessageText?.trim();
  105 |     }
  106 | 
  107 |     
  108 |     //This method navigates to base url
  109 |     //@param url 
  110 |     
  111 |     async navigateToLoginPage(url: string): Promise<void> {
  112 |         const maxAttempts = 3;
  113 |         let lastError: unknown;
  114 | 
  115 |         for (let attempt = 1; attempt <= maxAttempts; attempt++) {
  116 |             try {
  117 |                 await this.page.goto(url, { waitUntil: 'domcontentloaded', timeout: 45000 });
  118 |                 return;
  119 |             } catch (error) {
  120 |                 lastError = error;
  121 |                 const message = error instanceof Error ? error.message : String(error);
  122 |                 const isTransientNetworkError =
  123 |                     message.includes('ERR_CONNECTION_TIMED_OUT') ||
  124 |                     message.includes('Timeout') ||
  125 |                     message.includes('ERR_NETWORK_CHANGED') ||
  126 |                     message.includes('ERR_NAME_NOT_RESOLVED');
  127 | 
  128 |                 if (!isTransientNetworkError || attempt === maxAttempts) {
  129 |                     throw error;
  130 |                 }
  131 |             }
  132 |         }
  133 | 
  134 |         throw lastError;
  135 |     }
  136 | 
  137 |     
  138 |     //This method inputs username on login page
  139 |     //@param username 
  140 |     
  141 |     async enterUsername(username: string): Promise<void> {
  142 |         const isForgotPasswordFlow = await this.submitButtonOnForgotPasswordPage.isVisible().catch(() => false);
  143 |         const emailField = isForgotPasswordFlow ? this.forgotPasswordEmail : this.email;
  144 | 
  145 |         await emailField.waitFor({ state: 'visible', timeout: 15000 });
  146 | 
  147 |         for (let attempt = 1; attempt <= 2; attempt++) {
  148 |             await emailField.click();
  149 |             await emailField.fill(username);
  150 | 
  151 |             const currentValue = await emailField.inputValue();
  152 |             if (currentValue === username) {
  153 |                 return;
  154 |             }
  155 |         }
  156 |     }
  157 | 
  158 |     
  159 |     //This method inputs password on login page
  160 |     //@param password 
  161 |     
  162 |     async enterPassword(password: string): Promise<void> {
  163 |         await this.password.fill(password);
  164 |     }
  165 | 
  166 |     
  167 |     //This method performs click operation on login button
  168 |     
  169 |     async clickLoginButton(): Promise<void> {
> 170 |        await this.loginButton.click();
      |                               ^ TimeoutError: locator.click: Timeout 30000ms exceeded.
  171 |     }
  172 | 
  173 |     
  174 |     //This method perform Login action 
  175 |     //@param username 
  176 |     //@param password 
  177 |     
  178 |     async login(username: string, password: string): Promise<void> {
  179 |         await this.enterUsername(username);
  180 |         await this.enterPassword(password);
  181 |         await this.clickLoginButton();
  182 |     }
  183 | }
```