# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\2-NavigationSmoke.spec.ts >> Application Navigation Smoke Tests >> Automatic Check Decision Rules sub-page loads correctly
- Location: specs\Smoke\2-NavigationSmoke.spec.ts:127:5

# Error details

```
Error: expect(received).toContain(expected) // indexOf

Expected substring: "Decision Rules"
Received string:    "·····································································
PJ_FI_Bank (Playwright Automation)[uat-release]·········
            © Copyright Advanced Fraud Solutions 2005-2026 | All Rights Reserved  | Privacy Policy························································································································································································································
    "
```

# Page snapshot

```yaml
- generic [active] [ref=f1e1]:
  - banner [ref=f1e2]:
    - generic [ref=f1e3]:
      - link [ref=f1e4] [cursor=pointer]:
        - /url: /
      - text:              
      - generic [ref=f1e7]:
        - link "  Home" [ref=f1e8] [cursor=pointer]:
          - /url: /
          - generic [ref=f1e9]:  
          - generic [ref=f1e11]: Home
        - link "  Issued Checks" [ref=f1e13] [cursor=pointer]:
          - /url: /issued-checks
          - generic [ref=f1e14]:  
          - generic [ref=f1e16]: Issued Checks
        - link "  Presented Checks" [ref=f1e18] [cursor=pointer]:
          - /url: /paid-checks
          - generic [ref=f1e19]:  
          - generic [ref=f1e21]: Presented Checks
        - link "  Teller" [ref=f1e23] [cursor=pointer]:
          - /url: /teller
          - generic [ref=f1e24]:  
          - generic [ref=f1e26]: Teller
        - link "  ACH" [ref=f1e28] [cursor=pointer]:
          - /url: /paid-ach
          - generic [ref=f1e29]:  
          - generic [ref=f1e31]: ACH
        - link "  Exceptions 12" [ref=f1e33] [cursor=pointer]:
          - /url: /exceptions
          - generic [ref=f1e34]:  
          - generic [ref=f1e36]: Exceptions
          - generic [ref=f1e38]: "12"
        - link "  Settings" [ref=f1e39] [cursor=pointer]:
          - /url: /client-admin
          - generic [ref=f1e40]:  
          - generic [ref=f1e42]: Settings
      - generic [ref=f1e45]:
        - button "  F.I ACH&CHK User" [ref=f1e46] [cursor=pointer]:
          - generic [ref=f1e47]:  
          - generic [ref=f1e49]: F.I ACH&CHK User
        - text:  
  - generic [ref=f1e51]:
    - generic [ref=f1e53]:
      - generic [ref=f1e55]:
        - list [ref=f1e56]:
          - listitem [ref=f1e57]:
            - link " " [ref=f1e58] [cursor=pointer]:
              - /url: /
          - listitem [ref=f1e60]:
            - link "Settings" [ref=f1e61] [cursor=pointer]:
              - /url: /client-admin
          - listitem [ref=f1e62]:
            - link "Check Decision Rules" [ref=f1e63]:
              - /url: javascript:;
        - text:  +
        - button "+ Add Rule" [ref=f1e65] [cursor=pointer]:
          - generic [ref=f1e66]: +
          - text: Add Rule
      - generic [ref=f1e68]:
        - toolbar "Grid toolbar" [ref=f1e69]:
          - generic [ref=f1e70]:
            - generic [ref=f1e71]:
              - generic [ref=f1e72]:
                - generic [ref=f1e73]: Page Size
                - combobox [ref=f1e75]:
                  - option "10"
                  - option "20" [selected]
                  - option "50"
                  - option "100"
              - button "Excel" [ref=f1e76] [cursor=pointer]
              - textbox "Search..." [ref=f1e83]
            - generic [ref=f1e85]:
              - generic [ref=f1e86]: Saved Filters
              - combobox [ref=f1e88]:
                - option "[No Filter]" [selected]
                - option "Whitelist"
                - option "Blacklist"
              - button "+" [ref=f1e90] [cursor=pointer]
        - grid "Data table" [ref=f1e92]:
          - rowgroup [ref=f1e102]:
            - row [ref=f1e103]:
              - columnheader "ID ID column filter menu settings" [ref=f1e104]:
                - generic [ref=f1e105]:
                  - generic [ref=f1e106] [cursor=pointer]: ID
                  - button "ID column filter menu settings" [ref=f1e108]
              - columnheader "Client Client column filter menu settings" [ref=f1e113]:
                - generic [ref=f1e114]:
                  - generic [ref=f1e115] [cursor=pointer]: Client
                  - button "Client column filter menu settings" [ref=f1e117]
              - columnheader "Name Name column filter menu settings" [ref=f1e122]:
                - generic [ref=f1e123]:
                  - generic [ref=f1e124] [cursor=pointer]: Name
                  - button "Name column filter menu settings" [ref=f1e126]
              - columnheader "Effective Effective column filter menu settings" [ref=f1e131]:
                - generic [ref=f1e132]:
                  - generic [ref=f1e133] [cursor=pointer]: Effective
                  - button "Effective column filter menu settings" [ref=f1e135]
              - columnheader "Expire Expire column filter menu settings" [ref=f1e140]:
                - generic [ref=f1e141]:
                  - generic [ref=f1e142] [cursor=pointer]: Expire
                  - button "Expire column filter menu settings" [ref=f1e144]
              - columnheader "Conditions Conditions column filter menu settings" [ref=f1e149]:
                - generic [ref=f1e150]:
                  - generic [ref=f1e151] [cursor=pointer]: Conditions
                  - button "Conditions column filter menu settings" [ref=f1e153]
              - columnheader "Decision Decision column filter menu settings" [ref=f1e158]:
                - generic [ref=f1e159]:
                  - generic [ref=f1e160] [cursor=pointer]: Decision
                  - button "Decision column filter menu settings" [ref=f1e162]
              - columnheader "Edit" [ref=f1e167]
          - rowgroup [ref=f1e182]:
            - row [ref=f1e183]:
              - gridcell "840" [ref=f1e184]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e185]
              - gridcell "Rule 3" [ref=f1e186]
              - gridcell "3/24/2026" [ref=f1e187]
              - gridcell [ref=f1e188]
              - gridcell "If Amount Equal To 100, then apply decision Pay" [ref=f1e189]:
                - generic [ref=f1e190]:
                  - text: If Amount Equal To 100, then apply decision
                  - generic [ref=f1e191]: Pay
              - gridcell "Pay" [ref=f1e192]
              - gridcell [ref=f1e193]:
                - link " Edit" [ref=f1e194] [cursor=pointer]:
                  - /url: /decision-rules/rule/840?ReturnUrl=%2fclient-admin%2fdecision-rules
                  - generic [ref=f1e195]: 
                  - text: Edit
                - link " Delete" [ref=f1e196] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e197]: 
                  - text: Delete
            - row [ref=f1e198]:
              - gridcell "96" [ref=f1e199]
              - gridcell "BC_SeCoGarden8" [ref=f1e200]
              - gridcell "Exact Match" [ref=f1e201]
              - gridcell "7/29/2024" [ref=f1e202]
              - gridcell [ref=f1e203]
              - gridcell "If Routing Number Matches Issued Check and Account Number Matches Issued Check and Amount Matches Issued Check and Check Number Matches Issued Check and Payee Name Matches Issued Check and Check Voided or Stopped Equal To false, then apply decision Pay" [ref=f1e204]:
                - generic [ref=f1e205]:
                  - text: If Routing Number Matches Issued Check and Account Number Matches Issued Check and Amount Matches Issued Check and Check Number Matches Issued Check and Payee Name Matches Issued Check and Check Voided or Stopped Equal To false, then apply decision
                  - generic [ref=f1e206]: Pay
              - gridcell "Pay" [ref=f1e207]
              - gridcell [ref=f1e208]:
                - link " Edit" [ref=f1e209] [cursor=pointer]:
                  - /url: /decision-rules/rule/96?ReturnUrl=%2fclient-admin%2fdecision-rules
                  - generic [ref=f1e210]: 
                  - text: Edit
                - link " Delete" [ref=f1e211] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e212]: 
                  - text: Delete
            - row [ref=f1e213]:
              - gridcell "31" [ref=f1e214]
              - gridcell "NewBC" [ref=f1e215]
              - gridcell "Exact Match" [ref=f1e216]
              - gridcell "8/1/2023" [ref=f1e217]
              - gridcell [ref=f1e218]
              - gridcell "If Routing Number Matches Issued Check and Account Number Matches Issued Check and Amount Matches Issued Check and Check Number Matches Issued Check and Payee Name Matches Issued Check and Check Voided or Stopped Equal To false, then apply decision Pay" [ref=f1e219]:
                - generic [ref=f1e220]:
                  - text: If Routing Number Matches Issued Check and Account Number Matches Issued Check and Amount Matches Issued Check and Check Number Matches Issued Check and Payee Name Matches Issued Check and Check Voided or Stopped Equal To false, then apply decision
                  - generic [ref=f1e221]: Pay
              - gridcell "Pay" [ref=f1e222]
              - gridcell [ref=f1e223]:
                - link " Edit" [ref=f1e224] [cursor=pointer]:
                  - /url: /decision-rules/rule/31?ReturnUrl=%2fclient-admin%2fdecision-rules
                  - generic [ref=f1e225]: 
                  - text: Edit
                - link " Delete" [ref=f1e226] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e227]: 
                  - text: Delete
            - row [ref=f1e228]:
              - gridcell "7" [ref=f1e229]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e230]
              - gridcell "Decision 4" [ref=f1e231]
              - gridcell "3/9/2023" [ref=f1e232]
              - gridcell [ref=f1e233]
              - gridcell "If Routing Number Equal To 122199983 and Account Number Matches Issued Check and Amount Less Than 15 and Check Number Not Between (Inclusive) 5000 to 6000 and Check Voided or Stopped Equal To false and Payee Name Matches Issued Check, then apply decision Return" [ref=f1e234]:
                - generic [ref=f1e235]:
                  - text: If Routing Number Equal To 122199983 and Account Number Matches Issued Check and Amount Less Than 15 and Check Number Not Between (Inclusive) 5000 to 6000 and Check Voided or Stopped Equal To false and Payee Name Matches Issued Check, then apply decision
                  - generic [ref=f1e236]: Return
              - gridcell "Return" [ref=f1e237]
              - gridcell [ref=f1e238]:
                - link " Edit" [ref=f1e239] [cursor=pointer]:
                  - /url: /decision-rules/rule/7?ReturnUrl=%2fclient-admin%2fdecision-rules
                  - generic [ref=f1e240]: 
                  - text: Edit
                - link " Delete" [ref=f1e241] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e242]: 
                  - text: Delete
            - row [ref=f1e243]:
              - gridcell "6" [ref=f1e244]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e245]
              - gridcell "Decision Rule 3" [ref=f1e246]
              - gridcell "3/9/2023" [ref=f1e247]
              - gridcell [ref=f1e248]
              - gridcell "If Routing Number Equal To 122199983 and Account Number Matches Issued Check and Amount Greater Than 100 and Check Number Between (Inclusive) 20000 to 20015 and Check Voided or Stopped Equal To false and Payee Name Matches Issued Check, then apply decision Pay" [ref=f1e249]:
                - generic [ref=f1e250]:
                  - text: If Routing Number Equal To 122199983 and Account Number Matches Issued Check and Amount Greater Than 100 and Check Number Between (Inclusive) 20000 to 20015 and Check Voided or Stopped Equal To false and Payee Name Matches Issued Check, then apply decision
                  - generic [ref=f1e251]: Pay
              - gridcell "Pay" [ref=f1e252]
              - gridcell [ref=f1e253]:
                - link " Edit" [ref=f1e254] [cursor=pointer]:
                  - /url: /decision-rules/rule/6?ReturnUrl=%2fclient-admin%2fdecision-rules
                  - generic [ref=f1e255]: 
                  - text: Edit
                - link " Delete" [ref=f1e256] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e257]: 
                  - text: Delete
            - row [ref=f1e258]:
              - gridcell "2" [ref=f1e259]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e260]
              - gridcell "Rule 2" [ref=f1e261]
              - gridcell "3/6/2023" [ref=f1e262]
              - gridcell [ref=f1e263]
              - gridcell "If Check Voided or Stopped Equals To true, then apply decision Return" [ref=f1e264]:
                - generic [ref=f1e265]:
                  - text: If Check Voided or Stopped Equals To true, then apply decision
                  - generic [ref=f1e266]: Return
              - gridcell "Return" [ref=f1e267]
              - gridcell [ref=f1e268]:
                - link " Edit" [ref=f1e269] [cursor=pointer]:
                  - /url: /decision-rules/rule/2?ReturnUrl=%2fclient-admin%2fdecision-rules
                  - generic [ref=f1e270]: 
                  - text: Edit
                - link " Delete" [ref=f1e271] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e272]: 
                  - text: Delete
            - row [ref=f1e273]:
              - gridcell "1" [ref=f1e274]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e275]
              - gridcell "Rule 1" [ref=f1e276]
              - gridcell "3/6/2023" [ref=f1e277]
              - gridcell [ref=f1e278]
              - gridcell "If Routing Number Matches Issued Check and Account Number Matches Issued Check and Check Number Matches Issued Check and Amount Matches Issued Check and Payee Name Matches Issued Check and Check Voided or Stopped Equals To false, then apply decision Return" [ref=f1e279]:
                - generic [ref=f1e280]:
                  - text: If Routing Number Matches Issued Check and Account Number Matches Issued Check and Check Number Matches Issued Check and Amount Matches Issued Check and Payee Name Matches Issued Check and Check Voided or Stopped Equals To false, then apply decision
                  - generic [ref=f1e281]: Return
              - gridcell "Return" [ref=f1e282]
              - gridcell [ref=f1e283]:
                - link " Edit" [ref=f1e284] [cursor=pointer]:
                  - /url: /decision-rules/rule/1?ReturnUrl=%2fclient-admin%2fdecision-rules
                  - generic [ref=f1e285]: 
                  - text: Edit
                - link " Delete" [ref=f1e286] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e287]: 
                  - text: Delete
        - application "Page navigation, page 1 of 1" [ref=f1e288]:
          - generic [ref=f1e289]:
            - button "Go to the first page" [disabled]
            - button "Go to the previous page" [disabled]
            - generic [ref=f1e290]:
              - text: Page
              - spinbutton "Select a page" [ref=f1e292]: "1"
              - text: of 1
            - button "Go to the next page" [disabled]
            - button "Go to the last page" [disabled]
          - generic [ref=f1e293]: 1 - 7 of 7 items
    - contentinfo [ref=f1e294]:
      - generic [ref=f1e295]:
        - text: PJ_FI_Bank (Playwright Automation)
        - generic [ref=f1e296]: "[uat-release]"
      - generic [ref=f1e297]:
        - text: © Copyright Advanced Fraud Solutions 2005-2026 |
        - generic [ref=f1e298]: All Rights Reserved
        - text: "|"
        - link "Privacy Policy" [ref=f1e300] [cursor=pointer]:
          - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  34  | 
  35  |     test('Presented Checks page loads correctly', async ({ page }) => {
  36  |         await page.goto('/paid-checks');
  37  |         await expect(page.getByRole('link', { name: /Presented Checks/ }).first()).toBeVisible({ timeout: 15000 });
  38  |         await expect(page).toHaveURL(/\/paid-checks/);
  39  |     });
  40  | 
  41  |     test('Teller page loads correctly', async ({ page }) => {
  42  |         await page.goto('/teller');
  43  |         await expect(page.getByRole('link', { name: /Teller/ }).first()).toBeVisible({ timeout: 15000 });
  44  |         await expect(page).toHaveURL(/\/teller/);
  45  |     });
  46  | 
  47  |     test('ACH page loads correctly', async ({ page }) => {
  48  |         await page.goto('/paid-ach');
  49  |         await expect(page.getByRole('link', { name: /^ACH$/ }).first()).toBeVisible({ timeout: 15000 });
  50  |         await expect(page).toHaveURL(/\/paid-ach/);
  51  |     });
  52  | 
  53  |     test('Exceptions page loads correctly', async ({ page }) => {
  54  |         await page.goto('/exceptions');
  55  |         await expect(page.locator('text=Open Exceptions').first()).toBeVisible({ timeout: 15000 });
  56  |         await expect(page).toHaveURL(/\/exceptions/);
  57  |     });
  58  | 
  59  |     test('Settings page loads correctly', async ({ page }) => {
  60  |         await page.goto('/client-admin');
  61  |         await expect(page.locator('text=Account').first()).toBeVisible({ timeout: 15000 });
  62  |         await expect(page).toHaveURL(/\/client-admin/);
  63  |     });
  64  | 
  65  |     // ── Settings sub-navigation ────────────────────────────────────────────────
  66  | 
  67  |     test('Account Settings sub-page loads correctly', async ({ page }) => {
  68  |         await page.goto('/client-admin/info');
  69  |         await expect(page).toHaveURL(/\/client-admin\/info/, { timeout: 15000 });
  70  |         await expect(page.locator('text=Account Settings').first()).toBeVisible({ timeout: 15000 });
  71  |     });
  72  | 
  73  |     test('Business Clients sub-page loads correctly', async ({ page }) => {
  74  |         await page.goto('/client-admin/business-clients');
  75  |         await expect(page).toHaveURL(/\/client-admin\/business-clients/, { timeout: 15000 });
  76  |         await expect(page.locator('text=Business Clients').first()).toBeVisible({ timeout: 15000 });
  77  |     });
  78  | 
  79  |     test('Users sub-page loads correctly', async ({ page }) => {
  80  |         await page.goto('/client-admin/users');
  81  |         await expect(page).toHaveURL(/\/client-admin\/users/, { timeout: 15000 });
  82  |         await expect(page.locator('text=Users').first()).toBeVisible({ timeout: 15000 });
  83  |     });
  84  | 
  85  |     test('Roles/Permissions sub-page loads correctly', async ({ page }) => {
  86  |         await page.goto('/client-admin/roles');
  87  |         await expect(page).toHaveURL(/\/client-admin\/roles/, { timeout: 15000 });
  88  |         await expect(page.locator('text=Roles/Permissions').first()).toBeVisible({ timeout: 15000 });
  89  |     });
  90  | 
  91  |     test('Branding sub-page loads correctly', async ({ page }) => {
  92  |         await page.goto('/client-admin/branding');
  93  |         await expect(page).toHaveURL(/\/client-admin\/branding/, { timeout: 15000 });
  94  |         await expect(page.locator('text=Branding').first()).toBeVisible({ timeout: 15000 });
  95  |     });
  96  | 
  97  |     test('Billing Reports sub-page loads correctly', async ({ page }) => {
  98  |         await page.goto('/client-admin/billing-reports');
  99  |         await expect(page).toHaveURL(/\/client-admin\/billing-reports/, { timeout: 15000 });
  100 |         await expect(page.locator('text=Billing Reports').first()).toBeVisible({ timeout: 15000 });
  101 |     });
  102 | 
  103 |     test('Decision Files sub-page loads correctly', async ({ page }) => {
  104 |         await page.goto('/client-admin/decision-files');
  105 |         await expect(page).toHaveURL(/\/client-admin\/decision-files/, { timeout: 15000 });
  106 |         await expect(page.locator('text=Decision Files').first()).toBeVisible({ timeout: 15000 });
  107 |     });
  108 | 
  109 |     test('Holiday Schedules sub-page loads correctly', async ({ page }) => {
  110 |         await page.goto('/client-admin/holiday-schedules');
  111 |         await expect(page).toHaveURL(/\/client-admin\/holiday-schedules/, { timeout: 15000 });
  112 |         await expect(page.locator('text=Holiday Schedules').first()).toBeVisible({ timeout: 15000 });
  113 |     });
  114 | 
  115 |     test('File Formats sub-page loads correctly', async ({ page }) => {
  116 |         await page.goto('/file-formats');
  117 |         await expect(page).toHaveURL(/\/file-formats/, { timeout: 15000 });
  118 |         await expect(page.locator('text=File Formats').first()).toBeVisible({ timeout: 15000 });
  119 |     });
  120 | 
  121 |     test('Notification Templates sub-page loads correctly', async ({ page }) => {
  122 |         await page.goto('/client-admin/emails');
  123 |         await expect(page).toHaveURL(/\/client-admin\/emails/, { timeout: 15000 });
  124 |         await expect(page.locator('text=Notifications').first()).toBeVisible({ timeout: 15000 });
  125 |     });
  126 | 
  127 |     test('Automatic Check Decision Rules sub-page loads correctly', async ({ page }) => {
  128 |         await page.goto('/client-admin/decision-rules');
  129 |         await expect(page).toHaveURL(/\/client-admin\/decision-rules/, { timeout: 15000 });
  130 |         // Wait for Blazor to render content
  131 |         await page.waitForLoadState('networkidle');
  132 |         // Verify page has content (Blazor may not use traditional headings)
  133 |         const pageText = await page.locator('body').textContent();
> 134 |         expect(pageText).toContain('Decision Rules');
      |                          ^ Error: expect(received).toContain(expected) // indexOf
  135 |     });
  136 | 
  137 |     test('Check Approval Rules sub-page loads correctly', async ({ page }) => {
  138 |         await page.goto('/client-admin/approval-rules');
  139 |         await expect(page).toHaveURL(/\/client-admin\/approval-rules/, { timeout: 15000 });
  140 |         await expect(page.locator('text=Check Approval Rules').first()).toBeVisible({ timeout: 15000 });
  141 |     });
  142 | 
  143 |     test('Automatic ACH Decision Rules sub-page loads correctly', async ({ page }) => {
  144 |         await page.goto('/client-admin/decision-rules/ach');
  145 |         await expect(page).toHaveURL(/\/client-admin\/decision-rules\/ach/, { timeout: 15000 });
  146 |         // Wait for Blazor to render content
  147 |         await page.waitForLoadState('domcontentloaded');
  148 |         // Verify at least one element is rendered on page
  149 |         await expect(page.locator('body > *')).not.toHaveCount(0, { timeout: 10000 });
  150 |     });
  151 | 
  152 |     test('ACH Approval Rules sub-page loads correctly', async ({ page }) => {
  153 |         await page.goto('/client-admin/approval-rules/ach');
  154 |         await expect(page).toHaveURL(/\/client-admin\/approval-rules\/ach/, { timeout: 15000 });
  155 |         await expect(page.locator('text=ACH Approval Rules').first()).toBeVisible({ timeout: 15000 });
  156 |     });
  157 | 
  158 |     test('Notification Log sub-page loads correctly', async ({ page }) => {
  159 |         await page.goto('/client-admin/notification-log');
  160 |         await expect(page).toHaveURL(/\/client-admin\/notification-log/, { timeout: 15000 });
  161 |         await expect(page.locator('text=Notification Log').first()).toBeVisible({ timeout: 15000 });
  162 |     });
  163 | 
  164 |     test('Default Decision Log sub-page loads correctly', async ({ page }) => {
  165 |         await page.goto('/client-admin/default-decision-log');
  166 |         await expect(page).toHaveURL(/\/client-admin\/default-decision-log/, { timeout: 15000 });
  167 |         await expect(page.locator('text=Default Decision Log').first()).toBeVisible({ timeout: 15000 });
  168 |     });
  169 | 
  170 |     test('System Log sub-page loads correctly', async ({ page }) => {
  171 |         await page.goto('/client-admin/entity-log');
  172 |         await expect(page).toHaveURL(/\/client-admin\/entity-log/, { timeout: 15000 });
  173 |         await expect(page.locator('text=System Log').first()).toBeVisible({ timeout: 15000 });
  174 |     });
  175 | 
  176 |     test('File Processing sub-page loads correctly', async ({ page }) => {
  177 |         await page.goto('/client-admin/uploaded-files');
  178 |         await expect(page).toHaveURL(/\/client-admin\/uploaded-files/, { timeout: 15000 });
  179 |         await expect(page.locator('text=File Processing').first()).toBeVisible({ timeout: 15000 });
  180 |     });
  181 | 
  182 |     test('API link is visible and points to swagger', async ({ page }) => {
  183 |         await page.goto('/client-admin');
  184 |         await expect(page).toHaveURL(/\/client-admin/, { timeout: 15000 });
  185 |         const apiLink = page.locator("a[href*='swagger']").first();
  186 |         await expect(apiLink).toBeVisible({ timeout: 15000 });
  187 |         await expect(apiLink).toHaveAttribute('href', /swagger/i);
  188 |     });
  189 | 
  190 |     test('Web Hooks sub-page loads correctly', async ({ page }) => {
  191 |         await page.goto('/client-admin/web-hooks');
  192 |         await expect(page).toHaveURL(/\/client-admin\/web-hooks/, { timeout: 15000 });
  193 |         await expect(page.getByRole('link', { name: 'Web Hook' })).toBeVisible({ timeout: 15000 });
  194 |         await expect(page.getByRole('link', { name: 'View Logs' })).toBeVisible({ timeout: 15000 });
  195 |     });
  196 | 
  197 | 
  198 | });
  199 | 
```