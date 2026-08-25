# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\5-PresentedChecksSmoke.spec.ts >> Presented Checks — Smoke >> Excel export button is visible and enabled
- Location: specs\Smoke\5-PresentedChecksSmoke.spec.ts:52:5

# Error details

```
TimeoutError: locator.waitFor: Timeout 20000ms exceeded.
Call log:
  - waiting for locator('[aria-label="Data table"]') to be visible

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
        - link "  Exceptions" [ref=f1e33] [cursor=pointer]:
          - /url: /exceptions
          - generic [ref=f1e34]:  
          - generic [ref=f1e36]: Exceptions
        - link "  Settings" [ref=f1e38] [cursor=pointer]:
          - /url: /client-admin
          - generic [ref=f1e39]:  
          - generic [ref=f1e41]: Settings
      - generic [ref=f1e44]:
        - button "  F.I ACH&CHK User" [ref=f1e45] [cursor=pointer]:
          - generic [ref=f1e46]:  
          - generic [ref=f1e48]: F.I ACH&CHK User
        - text:  
  - generic [ref=f1e50]:
    - generic [ref=f1e54]:
      - list [ref=f1e55]:
        - listitem [ref=f1e56]:
          - link " " [ref=f1e57] [cursor=pointer]:
            - /url: /
        - listitem [ref=f1e59]:
          - link "Presented Checks" [ref=f1e60] [cursor=pointer]:
            - /url: /paid-checks
      - text:   +
      - group [ref=f1e62]:
        - link " Uploaded Checks" [ref=f1e63] [cursor=pointer]:
          - /url: /paid-checks/uploads
          - generic [ref=f1e64]: 
          - text: Uploaded Checks
        - link "+ Add Check" [ref=f1e65] [cursor=pointer]:
          - /url: /paid-checks/check
          - generic [ref=f1e66]: +
          - text: Add Check
    - contentinfo [ref=f1e69]:
      - generic [ref=f1e70]:
        - text: PJ_FI_Bank (Playwright Automation)
        - generic [ref=f1e71]: "[uat-release]"
      - generic [ref=f1e72]:
        - text: © Copyright Advanced Fraud Solutions 2005-2026 |
        - generic [ref=f1e73]: All Rights Reserved
        - text: "|"
        - link "Privacy Policy" [ref=f1e75] [cursor=pointer]:
          - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
  - heading [level=5] [ref=f1e77]:
    - text: Could not reconnect to the server.
    - link "Reload" [ref=f1e78] [cursor=pointer]:
      - /url: ""
    - text: the page to restore functionality.
```

# Test source

```ts
  99  | 
  100 |     columnFilterButton(columnName: string) {
  101 |         return this.page.getByRole('button', {
  102 |             name: `${columnName} column filter menu settings`,
  103 |             exact: true,
  104 |         });
  105 |     }
  106 | 
  107 |     get columnFilterPopup() {
  108 |         return this.page.locator(
  109 |             '.k-grid-filter-popup:visible, [aria-label$="Filter Menu"]:visible, .k-animation-container:visible:has(.k-filter-menu-container)'
  110 |         ).first();
  111 |     }
  112 | 
  113 |     get columnFilterApplyButton() {
  114 |         return this.columnFilterPopup.getByRole('button', { name: 'Filter', exact: true });
  115 |     }
  116 | 
  117 |     get columnFilterClearButton() {
  118 |         return this.columnFilterPopup.getByRole('button', { name: 'Clear', exact: true });
  119 |     }
  120 | 
  121 |     // ── Grid ──────────────────────────────────────────────────────────────────
  122 | 
  123 |     get dataGrid() {
  124 |         return this.page.locator('[aria-label="Data table"]');
  125 |     }
  126 | 
  127 |     get gridRows() {
  128 |         return this.page.locator('tr.k-master-row.k-table-row');
  129 |     }
  130 | 
  131 |     get columnHeaderStatus() {
  132 |         return this.page.getByRole('columnheader', { name: /^Status/ }).first();
  133 |     }
  134 | 
  135 |     get columnHeaderDecision() {
  136 |         return this.page.getByRole('columnheader', { name: /^Decision/ }).first();
  137 |     }
  138 | 
  139 |     get columnHeaderClient() {
  140 |         return this.page.getByRole('columnheader', { name: /^Client/ }).first();
  141 |     }
  142 | 
  143 |     get columnHeaderCheckNumber() {
  144 |         return this.page.getByRole('columnheader', { name: /^Check #/ }).first();
  145 |     }
  146 | 
  147 |     get columnHeaderAmount() {
  148 |         return this.page.getByRole('columnheader', { name: /^Amount/ }).first();
  149 |     }
  150 | 
  151 |     get columnHeaderPresentedDate() {
  152 |         return this.page.getByRole('columnheader', { name: /^Presented Date/ }).first();
  153 |     }
  154 | 
  155 |     // ── Pagination ────────────────────────────────────────────────────────────
  156 | 
  157 |     get paginationInfo() {
  158 |         return this.page.getByRole('application', { name: /Page navigation/ }).locator('text=items');
  159 |     }
  160 | 
  161 |     get nextPageButton() {
  162 |         return this.page.locator('button[title="Go to the next page"]');
  163 |     }
  164 | 
  165 |     get previousPageButton() {
  166 |         return this.page.locator('button[title="Go to the previous page"]');
  167 |     }
  168 | 
  169 |     get firstPageButton() {
  170 |         return this.page.locator('button[title="Go to the first page"]');
  171 |     }
  172 | 
  173 |     get lastPageButton() {
  174 |         return this.page.locator('button[title="Go to the last page"]');
  175 |     }
  176 | 
  177 |     get currentPageInput() {
  178 |         return this.page.getByRole('spinbutton', { name: /Select a page/i });
  179 |     }
  180 | 
  181 |     // ── Methods ───────────────────────────────────────────────────────────────
  182 | 
  183 |     async searchFor(term: string) {
  184 |         await this.searchInput.fill(term);
  185 |         await this.page.keyboard.press('Enter');
  186 |     }
  187 | 
  188 |     async clearSearch() {
  189 |         await this.searchInput.clear();
  190 |         await this.page.keyboard.press('Enter');
  191 |     }
  192 | 
  193 |     // Kendo renders the "No records available." row when the grid has no data.
  194 |     get noRecordsRow() {
  195 |         return this.page.locator('tr.k-grid-norecords');
  196 |     }
  197 | 
  198 |     async waitForGridLoad() {
> 199 |         await this.dataGrid.waitFor({ state: 'visible', timeout: 20000 });
      |                             ^ TimeoutError: locator.waitFor: Timeout 20000ms exceeded.
  200 |         // The grid shell renders before Kendo binds data, so a caller that counts rows right
  201 |         // after this returns can read 0 on a grid that does have data. Wait until the row set
  202 |         // exists one way or the other — data rows, or the explicit no-records row.
  203 |         await this.gridRows.first().or(this.noRecordsRow.first())
  204 |             .waitFor({ state: 'visible', timeout: 20000 });
  205 |     }
  206 | 
  207 |     async verifyGridColumnsVisible() {
  208 |         await expect(this.columnHeaderStatus).toBeVisible();
  209 |         await expect(this.columnHeaderDecision).toBeVisible();
  210 |         await expect(this.columnHeaderClient).toBeVisible();
  211 |         await expect(this.columnHeaderCheckNumber).toBeVisible();
  212 |         await expect(this.columnHeaderAmount).toBeVisible();
  213 |         await expect(this.columnHeaderPresentedDate).toBeVisible();
  214 |     }
  215 | 
  216 |     // ── Add Check Navigation ──────────────────────────────────────────────────
  217 | 
  218 |     get addCheckNavigationLink() {
  219 |         return this.page.locator('a.btn:has-text("Add Check")');
  220 |     }
  221 | 
  222 |     get addCheckBreadcrumb() {
  223 |         return this.page.getByRole('link', { name: '[New Check]' });
  224 |     }
  225 | 
  226 |     // Pay/Return badges link to exception history; Pending badges link to the open exception.
  227 |     get firstCompletedDecisionBadge() {
  228 |         return this.page.locator('td[data-col-index="2"] a').filter({ hasText: /Pay|Return/ }).first();
  229 |     }
  230 | }
  231 | 
```