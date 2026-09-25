# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\3-HomeDashboardSmoke.spec.ts >> Home Dashboard >> Verify navigation to Presented Checks via nav menu
- Location: specs\Smoke\3-HomeDashboardSmoke.spec.ts:176:5

# Error details

```
TimeoutError: locator.click: Timeout 30000ms exceeded.
Call log:
  - waiting for locator('a.btn-account[href="/paid-checks"]')
    - locator resolved to <a type="button" href="/paid-checks" class="btn-account d-md-flex nav-link pl-4 pr-4">…</a>
  - attempting click action
    - waiting for element to be visible, enabled and stable

```

# Page snapshot

```yaml
- generic [active] [ref=e1]:
  - banner [ref=e2]:
    - generic [ref=e3]:
      - link [ref=e4] [cursor=pointer]:
        - /url: /
      - text:              
      - generic [ref=e7]:
        - link "  Home" [ref=e8] [cursor=pointer]:
          - /url: /
          - generic [ref=e9]:  
          - generic [ref=e11]: Home
        - link "  Issued Checks" [ref=e13] [cursor=pointer]:
          - /url: /issued-checks
          - generic [ref=e14]:  
          - generic [ref=e16]: Issued Checks
        - link "  Presented Checks" [ref=e18] [cursor=pointer]:
          - /url: /paid-checks
          - generic [ref=e19]:  
          - generic [ref=e21]: Presented Checks
        - link "  Teller" [ref=e23] [cursor=pointer]:
          - /url: /teller
          - generic [ref=e24]:  
          - generic [ref=e26]: Teller
        - link "  ACH" [ref=e28] [cursor=pointer]:
          - /url: /paid-ach
          - generic [ref=e29]:  
          - generic [ref=e31]: ACH
        - link "  Exceptions" [ref=e33] [cursor=pointer]:
          - /url: /exceptions
          - generic [ref=e34]:  
          - generic [ref=e36]: Exceptions
        - link "  Settings" [ref=e38] [cursor=pointer]:
          - /url: /client-admin
          - generic [ref=e39]:  
          - generic [ref=e41]: Settings
      - generic [ref=e44]:
        - button "  F.I ACH&CHK User" [ref=e45] [cursor=pointer]:
          - generic [ref=e46]:  
          - generic [ref=e48]: F.I ACH&CHK User
        - text:  
  - generic [ref=e50]:
    - generic [ref=e52]:
      - generic [ref=e53]:
        - generic [ref=e54]:
          - checkbox "Combined View " [checked] [ref=e55]
          - generic [ref=e56] [cursor=pointer]:
            - generic [ref=e57]: Combined View
            - text: 
        - generic [ref=e59]:
          - checkbox "Check Only " [ref=e60]
          - generic [ref=e61] [cursor=pointer]:
            - generic [ref=e62]: Check Only
            - text: 
        - generic [ref=e64]:
          - checkbox "ACH Only " [ref=e65]
          - generic [ref=e66] [cursor=pointer]:
            - generic [ref=e67]: ACH Only
            - text: 
      - generic [ref=e69]:
        - generic [ref=e71]:
          - generic [ref=e73]:
            - generic [ref=e74]: 
            - text: Exceptions [6-Month Combined]
          - generic [ref=e76]:
            - generic [ref=e77]:
              - generic [ref=e78]:
                - strong [ref=e79]: "289"
                - generic [ref=e80]: Total Exceptions
              - img [ref=e82]:
                - generic [ref=e87]:
                  - generic [ref=e107]: Mar
                  - generic [ref=e109]: Apr
                  - generic [ref=e111]: Aug
                  - generic [ref=e113]: Sep
            - generic [ref=e115]:
              - generic [ref=e116]:
                - strong [ref=e117]: $872,568
                - generic [ref=e118]: Total Exception Amount
              - img [ref=e120]:
                - generic [ref=e125]:
                  - generic [ref=e145]: Mar
                  - generic [ref=e147]: Apr
                  - generic [ref=e149]: Aug
                  - generic [ref=e151]: Sep
        - generic [ref=e154]:
          - generic [ref=e156]:
            - generic [ref=e157]: 
            - text: Exceptions by Decision [Combined]
          - img [ref=e160]:
            - generic [ref=e161]:
              - generic [ref=e164]:
                - generic [ref=e165]:
                  - generic [ref=e167]: Return
                  - generic [ref=e169] [cursor=pointer]
                - generic [ref=e170]:
                  - generic [ref=e172]: Pay
                  - generic [ref=e174] [cursor=pointer]
              - generic [ref=e176]:
                - generic [ref=e183]: "445"
                - generic [ref=e186]: "39"
        - generic [ref=e190]:
          - generic [ref=e192]:
            - generic [ref=e193]: 
            - text: Exceptions by Reason [Check Only]
          - img [ref=e197]:
            - generic [ref=e199]:
              - generic [ref=e202]:
                - generic [ref=e252]: "Check # Not Found"
                - generic [ref=e254]: Wrong Payee
                - generic [ref=e256]: Duplicate Presented Check
                - generic [ref=e258]: Wrong Amount
                - generic [ref=e260]: Void or Stopped Check
                - generic [ref=e262]: Reverse Positive Pay
                - generic [ref=e264]: "Routing # Not Found"
                - generic [ref=e266]: "Check # Out of Range"
                - generic [ref=e268]: "Account # Not Found"
                - generic [ref=e270]: Over Limit
                - generic [ref=e272]: Stale Date
                - generic [ref=e274]: Missing Payee
                - generic [ref=e276]: Exact Match
                - generic [ref=e278]: Invalid Presented Date
                - generic [ref=e282]: "0"
                - generic [ref=e284]: "20"
                - generic [ref=e286]: "40"
                - generic [ref=e288]: "60"
                - generic [ref=e290]: "80"
                - generic [ref=e292]: "100"
                - generic [ref=e294]: "120"
              - generic [ref=e298]:
                - generic [ref=e300]: Total Exceptions
                - generic [ref=e302] [cursor=pointer]
        - generic [ref=e304]:
          - generic [ref=e306]:
            - generic [ref=e307]: 
            - text: Exceptions by SEC Code [ACH Only]
          - img [ref=e311]:
            - generic [ref=e313]:
              - generic [ref=e316]:
                - generic [ref=e330]: WEB
                - generic [ref=e332]: CCD
                - generic [ref=e336]: "0"
                - generic [ref=e338]: "20"
                - generic [ref=e340]: "40"
                - generic [ref=e342]: "60"
                - generic [ref=e344]: "80"
                - generic [ref=e346]: "100"
                - generic [ref=e348]: "120"
                - generic [ref=e350]: "140"
                - generic [ref=e352]: "160"
              - generic [ref=e356]:
                - generic [ref=e358]: Total Exceptions
                - generic [ref=e360] [cursor=pointer]
        - generic [ref=e362]:
          - generic [ref=e364]:
            - generic [ref=e365]: 
            - text: Exceptions by Return Reason [Combined]
          - img [ref=e369]:
            - generic [ref=e371]:
              - generic [ref=e374]:
                - generic [ref=e384]: Other
                - generic [ref=e388]: "0"
                - generic [ref=e390]: "10"
                - generic [ref=e392]: "20"
                - generic [ref=e394]: "30"
                - generic [ref=e396]: "40"
                - generic [ref=e398]: "50"
                - generic [ref=e400]: "60"
                - generic [ref=e402]: "70"
                - generic [ref=e404]: "80"
                - generic [ref=e406]: "90"
              - generic [ref=e410]:
                - generic [ref=e412]: Total Exceptions
                - generic [ref=e414] [cursor=pointer]
      - generic [ref=e417]:
        - strong [ref=e418]: Note
        - text: Chart data could be delayed up to 15 minutes. You may click
        - link "here" [ref=e419]:
          - /url: javascript:;
        - text: to force refresh.
    - contentinfo [ref=e420]:
      - generic [ref=e421]:
        - text: FI Playwright Automation
        - generic [ref=e422]: "[uat-release]"
      - generic [ref=e423]:
        - text: © Copyright Advanced Fraud Solutions 2005-2026 |
        - generic [ref=e424]: All Rights Reserved
        - text: "|"
        - link "Privacy Policy" [ref=e426]:
          - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  105 |     }
  106 | 
  107 |     get totalExceptionAmountValue(){
  108 |         return this.totalExceptionAmountLabel.first().locator('xpath=preceding-sibling::strong[1]');
  109 |     }
  110 | 
  111 |     get dashboardDelayNote(){
  112 |         return this.page.locator('text=Chart data could be delayed up to 15 minutes');
  113 |     }
  114 | 
  115 |     get forceRefreshLink(){
  116 |         return this.page.locator('a.text-danger:has-text("here")');
  117 |     }
  118 | 
  119 |     // ── Footer / footnote ─────────────────────────────────────────────────────
  120 | 
  121 |     get footerEnvironmentTag(){
  122 |         // FI / environment label at the start of the footer (e.g. "QA_AT Bank_TestFI").
  123 |         // Older builds bracketed it ([UAT]); match the label element itself so it resolves
  124 |         // whether or not brackets are present.
  125 |         return this.page.locator('footer, [role="contentinfo"]')
  126 |             .locator('span, div')
  127 |             .filter({ hasText: /\S/ })
  128 |             .filter({ hasNotText: /Copyright|All Rights Reserved|Privacy Policy/i })
  129 |             .first();
  130 |     }
  131 | 
  132 |     get footerCopyrightText(){
  133 |         return this.page.getByText(/Copyright Advanced Fraud Solutions/i).first();
  134 |     }
  135 | 
  136 |     get footerAllRightsReservedText(){
  137 |         return this.page.getByText(/All Rights Reserved/i).first();
  138 |     }
  139 | 
  140 |     get footerPrivacyPolicyLink(){
  141 |         return this.page.getByRole('link', { name: /Privacy Policy/i }).first();
  142 |     }
  143 | 
  144 |     async scrollFooterIntoView(){
  145 |         await this.footerPrivacyPolicyLink.scrollIntoViewIfNeeded();
  146 |     }
  147 | 
  148 |     // ── Navigation menu links ────────────────────────────────────────────────────
  149 |     // Desktop top-bar: <a class="btn-account d-md-flex nav-link" href="/...">
  150 |     // Hamburger (mobile-only-lg) is hidden on desktop viewport — use desktop links directly.
  151 | 
  152 |     get issuedChecksNavLink(){
  153 |         return this.page.locator('a.btn-account[href="/issued-checks"]');
  154 |     }
  155 | 
  156 |     get presentedChecksNavLink(){
  157 |         return this.page.locator('a.btn-account[href="/paid-checks"]');
  158 |     }
  159 | 
  160 |     get achNavLink(){
  161 |         return this.page.locator('a.btn-account[href="/paid-ach"]');
  162 |     }
  163 | 
  164 |     get exceptionsNavLink(){
  165 |         return this.page.locator('a.btn-account[href="/exceptions"]');
  166 |     }
  167 | 
  168 |     get settingsNavLink(){
  169 |         return this.page.locator('a.btn-account[href="/client-admin"]');
  170 |     }
  171 | 
  172 |     get userProfileMenuButton(){
  173 |         return this.page.getByRole('button', { name: /user/i }).first();
  174 |     }
  175 | 
  176 |     // The top-nav account button. Anchored on its own class rather than by accessible
  177 |     // name (userProfileMenuButton above matches /user/i, which only works while the
  178 |     // signed-in user's name happens to contain "user") so it resolves on any tenant.
  179 |     // The header renders TWO of these — a hidden responsive twin and the shown one — so
  180 |     // this is scoped to the visible instance. It carries the signed-in user's display
  181 |     // name, the same value the Issued Checks grid records in its "Added By" column.
  182 |     // Verified live on qa-master 2026-09-08.
  183 |     get accountMenuButton(){
  184 |         return this.page.locator('button.btn-account:visible').first();
  185 |     }
  186 | 
  187 |     async getCurrentUserName(): Promise<string> {
  188 |         await this.accountMenuButton.waitFor({ state: 'visible', timeout: 15000 });
  189 |         return (await this.accountMenuButton.innerText()).trim();
  190 |     }
  191 | 
  192 |     get myInfoMenuItem(){
  193 |         return this.page.locator('a.dropdown-item[href="/my/settings"]');
  194 |     }
  195 | 
  196 |     get logoutMenuItem(){
  197 |         return this.page.locator('a.dropdown-item[href="/prelogout"]');
  198 |     }
  199 | 
  200 |     async navigateToIssuedChecks(){
  201 |         await this.issuedChecksNavLink.click();
  202 |     }
  203 | 
  204 |     async navigateToPresentedChecks(){
> 205 |         await this.presentedChecksNavLink.click();
      |                                           ^ TimeoutError: locator.click: Timeout 30000ms exceeded.
  206 |     }
  207 | 
  208 |     async navigateToACH(){
  209 |         await this.achNavLink.click();
  210 |     }
  211 | 
  212 |     async navigateToExceptions(){
  213 |         await this.exceptionsNavLink.click();
  214 |     }
  215 | 
  216 |     async navigateToSettings(){
  217 |         await this.settingsNavLink.click();
  218 |     }
  219 | 
  220 |     async openUserProfileMenu(){
  221 |         // Use the class-anchored account button, not userProfileMenuButton (/user/i), which
  222 |         // only matches while the signed-in user's display name contains "user".
  223 |         await this.accountMenuButton.waitFor({ state: 'visible' });
  224 |         await this.accountMenuButton.click();
  225 |     }
  226 | }
  227 | 
```