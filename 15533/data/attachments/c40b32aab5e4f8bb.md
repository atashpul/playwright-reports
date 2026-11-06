# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\9-AccountSettingsSmoke.spec.ts >> Settings — Account Section Smoke >> Users >> Api Token icon opens the token dialog
- Location: specs\Smoke\9-AccountSettingsSmoke.spec.ts:357:9

# Error details

```
Error: expect(locator).toHaveText(expected) failed

Locator: locator('.blazored-modal').locator('.blazored-modal-title')
Expected: "Api Token"
Timeout: 10000ms
Error: element(s) not found

Call log:
  - Expect "toHaveText" with timeout 10000ms
  - waiting for locator('.blazored-modal').locator('.blazored-modal-title')

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
    - link "Users":
      - /url: javascript:;
- group:
  - link "+ Add User":
    - /url: /client-admin/users/user
  - link " Inactive Users":
    - /url: /client-admin/users/Inactive
- toolbar "Grid toolbar":
  - text: Page Size
  - combobox:
    - option "10"
    - option "20" [selected]
    - option "50"
    - option "100"
  - button "Excel"
  - textbox "Search...": pjakati28+PP@gmail.com
- grid "Data table":
  - rowgroup:
    - row "ID ID column filter menu settings First Name First Name column filter menu settings Last Name Last Name column filter menu settings Email Email column filter menu settings Role(s) Role(s) column filter menu settings Notify by Email Notify by Email column filter menu settings Notify by Text Notify by Text column filter menu settings Api Token Edit":
      - columnheader "ID ID column filter menu settings":
        - text: ID
        - button "ID column filter menu settings"
      - columnheader "First Name First Name column filter menu settings":
        - text: First Name
        - button "First Name column filter menu settings"
      - columnheader "Last Name Last Name column filter menu settings":
        - text: Last Name
        - button "Last Name column filter menu settings"
      - columnheader "Email Email column filter menu settings":
        - text: Email
        - button "Email column filter menu settings"
      - columnheader "Role(s) Role(s) column filter menu settings":
        - text: Role(s)
        - button "Role(s) column filter menu settings"
      - columnheader "Notify by Email Notify by Email column filter menu settings":
        - text: Notify by Email
        - button "Notify by Email column filter menu settings"
      - columnheader "Notify by Text Notify by Text column filter menu settings":
        - text: Notify by Text
        - button "Notify by Text column filter menu settings"
      - columnheader "Api Token"
      - columnheader "Edit"
  - rowgroup:
    - row "8 F.I ACH&CHK User pjakati28+pp@gmail.com Account Manager, AFS_ADMIN  No  No   Edit":
      - gridcell "8"
      - gridcell "F.I ACH&CHK":
        - link "F.I ACH&CHK":
          - /url: /client-admin/users/user/8
      - gridcell "User":
        - link "User":
          - /url: /client-admin/users/user/8
      - gridcell "pjakati28+pp@gmail.com"
      - gridcell "Account Manager, AFS_ADMIN"
      - gridcell " No"
      - gridcell " No"
      - gridcell "":
        - link "":
          - /url: javascript:;
      - gridcell " Edit":
        - link " Edit":
          - /url: /client-admin/users/user/8
- application "Page navigation, page 1 of 1":
  - button "Go to the first page" [disabled]
  - button "Go to the previous page" [disabled]
  - text: Page
  - spinbutton "Select a page": "1"
  - text: of 1
  - button "Go to the next page" [disabled]
  - button "Go to the last page" [disabled]
  - text: 1 - 1 of 1 items
- contentinfo:
  - text: FI Playwright Automation[uat-release] © Copyright Advanced Fraud Solutions 2005-2026 | All Rights Reserved |
  - link "Privacy Policy":
    - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  265 | 
  266 |             await clientLink.click();
  267 |             await expect(editPage.BUSINESS_NAME_TEXTBOX).toHaveValue(clientName, { timeout: 15000 });
  268 |             await editPage.SAVE_CHANGES_BUTTON.click();
  269 |             await expect(pageManager.settingsPage.TOAST_MESSAGE.filter({ hasText: 'Client info updated successfully' })).toBeVisible({ timeout: 15000 });
  270 |             await expect(page).toHaveURL(/\/client-admin\/business-clients$/);
  271 |         });
  272 | 
  273 |     });
  274 | 
  275 |     // ── Users ──────────────────────────────────────────────────────────────────
  276 | 
  277 |     test.describe('Users', () => {
  278 | 
  279 |         test.beforeEach('Open Users', async ({ page, pageManager }) => {
  280 |             await page.goto('/client-admin/users');
  281 |             await expect(pageManager.usersPage.cellByHeader(0, 'Email')).toBeVisible({ timeout: 15000 });
  282 |         });
  283 | 
  284 |         test('Grid loads with all column headers', async ({ pageManager }) => {
  285 |             const users = pageManager.usersPage;
  286 |             await expect(users.COLUMN_HEADERS).toHaveCount(UsersPage.EXPECTED_COLUMN_HEADERS.length);
  287 |             for (const header of UsersPage.EXPECTED_COLUMN_HEADERS) {
  288 |                 await expect(users.columnHeader(header), `Header "${header}"`).toBeVisible();
  289 |             }
  290 |         });
  291 | 
  292 |         test('Search by email finds the logged-in user', async ({ pageManager }) => {
  293 |             const users = pageManager.usersPage;
  294 |             const email = Constants.USER_FI_EMAIL;
  295 | 
  296 |             await users.SEARCH_TEXTBOX.fill(email);
  297 |             await expect(users.rowByEmail(email)).toBeVisible({ timeout: 15000 });
  298 |             await expect.poll(async () => {
  299 |                 const rows = await users.GRID_ROWS.allInnerTexts();
  300 |                 return rows.every((row) => row.toLowerCase().includes(email.toLowerCase()));
  301 |             }, { timeout: 15000 }).toBe(true);
  302 |         });
  303 | 
  304 |         test('Edit opens the user form populated with that user', async ({ page, pageManager }) => {
  305 |             const users = pageManager.usersPage;
  306 |             const email = Constants.USER_FI_EMAIL;
  307 | 
  308 |             await users.SEARCH_TEXTBOX.fill(email);
  309 |             await users.rowByEmail(email).getByRole('link', { name: /Edit/ }).click();
  310 |             await expect(page).toHaveURL(/\/client-admin\/users\/user\/\d+/, { timeout: 15000 });
  311 |             await expect.poll(async () => (await users.EMAIL_ADDRESS_TEXTBOX.inputValue()).toLowerCase(), { timeout: 15000 })
  312 |                 .toBe(email.toLowerCase());
  313 |             await expect(users.FIRST_NAME_TEXTBOX).not.toHaveValue('');
  314 |             await expect(users.LAST_NAME_TEXTBOX).not.toHaveValue('');
  315 |             await expect(users.UPDATE_USER_BUTTON).toBeVisible();
  316 |         });
  317 | 
  318 |         // DISABLED pending UAT release of this feature. See PIPELINE-SKIPPED-TESTS.md.
  319 |         test.skip('Add User opens an empty form and selecting a role reveals notification settings', async ({ page, pageManager }) => {
  320 |             const users = pageManager.usersPage;
  321 | 
  322 |             await users.ADD_USER_BUTTON.click();
  323 |             await expect(page).toHaveURL(/\/client-admin\/users\/user$/, { timeout: 15000 });
  324 |             await expect(users.FIRST_NAME_TEXTBOX).toHaveValue('', { timeout: 15000 });
  325 |             await expect(users.LAST_NAME_TEXTBOX).toHaveValue('');
  326 |             await expect(users.EMAIL_ADDRESS_TEXTBOX).toHaveValue('');
  327 |             await expect(users.LANDING_PAGE_DROPDOWN).toBeVisible();
  328 |             await expect(users.ADD_USER_SUBMIT_BUTTON).toBeVisible();
  329 | 
  330 |             await expect(users.SELECT_ROLE_NOTIFICATION_HINT).toBeVisible();
  331 |             await users.ROLE_PICKERS.first().click();
  332 |             await expect(users.SELECT_ROLE_NOTIFICATION_HINT).toBeHidden({ timeout: 10000 });
  333 |             await expect(users.NOTIFICATION_SETTINGS_HEADER).toBeVisible();
  334 |         });
  335 | 
  336 |         test('Add User with required fields empty is blocked with a message', async ({ page, pageManager }) => {
  337 |             const users = pageManager.usersPage;
  338 |             const settings = pageManager.settingsPage;
  339 | 
  340 |             await users.ADD_USER_BUTTON.click();
  341 |             await expect(users.FIRST_NAME_TEXTBOX).toHaveValue('', { timeout: 15000 });
  342 |             await users.ADD_USER_SUBMIT_BUTTON.click();
  343 |             await expect(settings.MODAL).toContainText('Please provide all required user information', { timeout: 10000 });
  344 |             await settings.MODAL_OK_BUTTON.click();
  345 |             await expect(settings.MODAL).toBeHidden();
  346 |             await expect(page).toHaveURL(/\/client-admin\/users\/user$/);
  347 |         });
  348 | 
  349 |         test('Inactive Users page loads with the users grid', async ({ page, pageManager }) => {
  350 |             const users = pageManager.usersPage;
  351 |             await users.INACTIVE_USERS_BUTTON.click();
  352 |             await expect(page).toHaveURL(/\/client-admin\/users\/Inactive$/, { timeout: 15000 });
  353 |             await expect(pageManager.settingsPage.BREADCRUMB_CURRENT).toHaveText('Inactive Users', { timeout: 15000 });
  354 |             await expect(users.COLUMN_HEADERS).toHaveCount(UsersPage.EXPECTED_COLUMN_HEADERS.length);
  355 |         });
  356 | 
  357 |         test('Api Token icon opens the token dialog', async ({ pageManager }) => {
  358 |             const users = pageManager.usersPage;
  359 |             const settings = pageManager.settingsPage;
  360 |             const email = Constants.USER_FI_EMAIL;
  361 | 
  362 |             await users.SEARCH_TEXTBOX.fill(email);
  363 |             await expect(users.rowByEmail(email)).toBeVisible({ timeout: 15000 });
  364 |             await users.rowByEmail(email).locator('td').nth(UsersPage.EXPECTED_COLUMN_HEADERS.indexOf('Api Token')).locator('a').click();
> 365 |             await expect(settings.MODAL_TITLE).toHaveText('Api Token', { timeout: 10000 });
      |                                                ^ Error: expect(locator).toHaveText(expected) failed
  366 |             await expect(users.API_TOKEN_TEXTAREA).not.toHaveValue('');
  367 |             // Never click Re-Generate here: it would invalidate the shared user's token.
  368 |             await settings.MODAL_OK_BUTTON.click();
  369 |             await expect(settings.MODAL).toBeHidden();
  370 |         });
  371 | 
  372 |     });
  373 | 
  374 |     // ── Roles/Permissions ──────────────────────────────────────────────────────
  375 | 
  376 |     test.describe('Roles/Permissions', () => {
  377 | 
  378 |         test.beforeEach('Open Roles/Permissions', async ({ page, pageManager }) => {
  379 |             await page.goto('/client-admin/roles');
  380 |             // The grid briefly renders "No records available." before data arrives, and loads slowly
  381 |             // when several browser jobs hit the Settings pages at once.
  382 |             await expect(pageManager.rolesPermissionsPage.cellByHeader(0, 'Name')).toBeVisible({ timeout: 30000 });
  383 |         });
  384 | 
  385 |         test('Grid loads with column headers and populated roles', async ({ pageManager }) => {
  386 |             const roles = pageManager.rolesPermissionsPage;
  387 |             await expect(roles.COLUMN_HEADERS).toHaveCount(RolesPermissionsPage.EXPECTED_COLUMN_HEADERS.length);
  388 |             for (const header of RolesPermissionsPage.EXPECTED_COLUMN_HEADERS) {
  389 |                 await expect(roles.columnHeader(header), `Header "${header}"`).toBeVisible();
  390 |             }
  391 |             await expect(roles.cellByHeader(0, 'Name')).not.toHaveText('');
  392 |             await expect(roles.cellByHeader(0, 'Permission(s)')).not.toHaveText('');
  393 |         });
  394 | 
  395 |         test('Add Role opens the role-type dialog', async ({ pageManager }) => {
  396 |             const roles = pageManager.rolesPermissionsPage;
  397 |             await roles.ADD_ROLE_BUTTON.click();
  398 |             await expect(roles.CREATE_ROLE_DIALOG).toBeVisible({ timeout: 10000 });
  399 |             await expect(roles.FI_ROLE_TYPE_BUTTON).toBeVisible();
  400 |             await expect(roles.BC_ROLE_TYPE_BUTTON).toBeVisible();
  401 |         });
  402 | 
  403 |         test('Financial Institution role form shows every permission group', async ({ page, pageManager }) => {
  404 |             const roles = pageManager.rolesPermissionsPage;
  405 |             await roles.ADD_ROLE_BUTTON.click();
  406 |             await roles.FI_ROLE_TYPE_BUTTON.click();
  407 | 
  408 |             await expect(page).toHaveURL(/\/client-admin\/roles\/role$/, { timeout: 15000 });
  409 |             await expect(roles.ROLE_NAME_TEXTBOX).toHaveValue('', { timeout: 15000 });
  410 |             for (const permission of RolesPermissionsPage.FI_PERMISSION_GROUP_SAMPLES) {
  411 |                 await expect(roles.permissionCheckbox(permission), `Permission "${permission}"`).not.toBeChecked();
  412 |             }
  413 |             await expect(roles.SAVE_ROLE_LINK).toBeVisible();
  414 |             await expect(roles.CANCEL_ROLE_LINK).toBeVisible();
  415 |         });
  416 | 
  417 |         test('Business Clients role form shows the business-client permission set', async ({ page, pageManager }) => {
  418 |             const roles = pageManager.rolesPermissionsPage;
  419 |             await roles.ADD_ROLE_BUTTON.click();
  420 |             await roles.BC_ROLE_TYPE_BUTTON.click();
  421 | 
  422 |             await expect(page).toHaveURL(/\/client-admin\/roles\/role-bc$/, { timeout: 15000 });
  423 |             await expect(roles.ROLE_NAME_TEXTBOX).toHaveValue('', { timeout: 15000 });
  424 |             await expect(roles.permissionCheckbox('View Account')).toBeAttached({ timeout: 15000 });
  425 |             await expect(roles.permissionCheckbox(RolesPermissionsPage.FI_ONLY_PERMISSION)).toHaveCount(0);
  426 |         });
  427 | 
  428 |         test('By Permission view lists permissions with their roles', async ({ page, pageManager }) => {
  429 |             const roles = pageManager.rolesPermissionsPage;
  430 |             await roles.BY_PERMISSION_LINK.click();
  431 |             await expect(page).toHaveURL(/\/client-admin\/roles\/by-permission$/, { timeout: 15000 });
  432 |             for (const header of RolesPermissionsPage.BY_PERMISSION_COLUMN_HEADERS) {
  433 |                 await expect(roles.columnHeader(header), `Header "${header}"`).toBeVisible({ timeout: 15000 });
  434 |             }
  435 |             // The "No records available." placeholder row has a single cell; real rows have one per column.
  436 |             await expect(roles.GRID_ROWS.first().locator('td')).toHaveCount(RolesPermissionsPage.BY_PERMISSION_COLUMN_HEADERS.length, { timeout: 30000 });
  437 |         });
  438 | 
  439 |         test('By Event view lists the notification sections', async ({ page, pageManager }) => {
  440 |             const roles = pageManager.rolesPermissionsPage;
  441 |             await roles.BY_EVENT_LINK.click();
  442 |             await expect(page).toHaveURL(/\/client-admin\/roles\/by-event$/, { timeout: 15000 });
  443 |             for (const section of RolesPermissionsPage.BY_EVENT_SECTIONS) {
  444 |                 await expect(roles.byEventSection(section), `Section "${section}"`).toBeVisible({ timeout: 15000 });
  445 |             }
  446 |         });
  447 | 
  448 |         test('Edit opens a role with its saved permissions checked', async ({ page, pageManager }) => {
  449 |             const roles = pageManager.rolesPermissionsPage;
  450 |             const roleName = (await roles.cellByHeader(0, 'Name').innerText()).trim();
  451 |             const firstPermission = (await roles.permissionBadges(0).first().innerText()).trim();
  452 | 
  453 |             await roles.cellByHeader(0, 'Edit').getByRole('link', { name: /Edit/ }).click();
  454 |             await expect(page).toHaveURL(/\/client-admin\/roles\/role\/\d+$/, { timeout: 15000 });
  455 |             await expect(roles.ROLE_NAME_TEXTBOX).toHaveValue(roleName, { timeout: 15000 });
  456 |             await expect(roles.permissionCheckbox(firstPermission)).toBeChecked();
  457 |         });
  458 | 
  459 |         test.describe('Create and Delete', () => {
  460 | 
  461 |             let pendingRoleName: string | undefined;
  462 | 
  463 |             test.afterEach('Delete a role left behind by a failed run', async ({ pageManager }) => {
  464 |                 if (!pendingRoleName) return;
  465 |                 const name = pendingRoleName;
```