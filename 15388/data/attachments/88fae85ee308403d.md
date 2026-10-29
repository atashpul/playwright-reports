# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\9-AccountSettingsSmoke.spec.ts >> Settings — Account Section Smoke >> Users >> Add User opens an empty form and selecting a role reveals notification settings
- Location: specs\Smoke\9-AccountSettingsSmoke.spec.ts:317:9

# Error details

```
Error: expect(locator).toBeVisible() failed

Locator: getByText('Select a role to see the notifications this user can receive.')
Expected: visible
Timeout: 30000ms
Error: element(s) not found

Call log:
  - Expect "toBeVisible" with timeout 30000ms
  - waiting for getByText('Select a role to see the notifications this user can receive.')

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
    - link "FI Playwright Automation":
      - /url: /client-admin/business-clients/users/7
  - listitem:
    - link "[New User]":
      - /url: javascript:;
- group:
  - text:  User Info First Name *
  - textbox "First Name"
  - text: Last Name *
  - textbox "Last Name"
  - text: Email Address *
  - textbox "Email Address"
  - text: Cell Phone (for text message)
  - textbox: (___) ___-____
  - text: Send Welcome Email?
  - checkbox "No"
  - text: No Landing Page
  - combobox:
    - option "Home" [selected]
    - option "Issued Checks"
    - option "Presented Checks"
    - option "Teller Validation"
    - option "ACH"
    - option "Exceptions"
  - text: The default landing page after login. Roles and Accounts User Roles Allow user access to only selected role(s)
  - checkbox "Account Manager "
  - text: Account Manager 
  - checkbox "Pallavi Jakati's Role "
  - text: Pallavi Jakati's Role 
  - checkbox "AFS_ADMIN "
  - text: AFS_ADMIN  Notification Settings   New Exception Receive notification when new exceptions are pending decision. Require View Check/ACH Exceptions permission. Immediately
  - checkbox "Off"
  - text: Off Time Interval
  - combobox:
    - option "[Not Set]" [selected]
    - option "Every 15 Minutes"
    - option "Every 30 Minutes"
    - option "Every Hour"
  - text:   Approve Exception Decision Receive notification when exception decisions are pending approval. Require Approve Check/ACH Decisions permission. Immediately
  - checkbox "Off"
  - text: Off Time Interval
  - combobox:
    - option "[Not Set]" [selected]
    - option "Every 15 Minutes"
    - option "Every 30 Minutes"
    - option "Every Hour"
  - text:   Review Exception Decision Receive notification when exception decisions are completed and pending review. Require Review Check/ACH Decisions permission. Immediately
  - checkbox "Off"
  - text: Off Time Interval
  - combobox:
    - option "[Not Set]" [selected]
    - option "Every 15 Minutes"
    - option "Every 30 Minutes"
    - option "Every Hour"
  - text:   Pre-Decision Receive notification when exception pre-decisions are required. Require Review Pre-Decision permission. Immediately
  - checkbox "Off"
  - text: Off Time Interval
  - combobox:
    - option "[Not Set]" [selected]
    - option "Every 15 Minutes"
    - option "Every 30 Minutes"
    - option "Every Hour"
  - text:   File Upload Receive notification on successful and failed file uploads. Require Manage Files and Notifications permission. Immediately
  - checkbox "Off"
  - text: Off Time Interval
  - combobox:
    - option "[Not Set]" [selected]
    - option "Every 15 Minutes"
    - option "Every 30 Minutes"
    - option "Every Hour"
  - text: File Type
  - combobox "Select File Type(s)" [disabled]
  - separator: Notification Method
  - text:  By Email
  - checkbox "Off"
  - text: Off  By Text Message
  - checkbox "Off"
  - text: "Off"
  - button " Add User"
- contentinfo:
  - text: FI Playwright Automation[uat-release] © Copyright Advanced Fraud Solutions 2005-2026 | All Rights Reserved |
  - link "Privacy Policy":
    - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  228 |             await expect(businessClients.PAGE_INFO_TEXT).toContainText(/\b1 - ([1-9]|10) of \d+ items/, { timeout: 15000 });
  229 |             await expect.poll(async () => businessClients.GRID_ROWS.count()).toBeLessThanOrEqual(10);
  230 |         });
  231 | 
  232 |         test('Client Name column sorts ascending then descending', async ({ pageManager }) => {
  233 |             const businessClients = pageManager.businessClientsPage;
  234 | 
  235 |             await businessClients.columnSortTitle('Client Name').click();
  236 |             await expect(businessClients.columnHeader('Client Name')).toHaveAttribute('aria-sort', 'ascending', { timeout: 10000 });
  237 |             const firstAscending = (await businessClients.cellByHeader(0, 'Client Name').innerText()).trim();
  238 | 
  239 |             await businessClients.columnSortTitle('Client Name').click();
  240 |             await expect(businessClients.columnHeader('Client Name')).toHaveAttribute('aria-sort', 'descending', { timeout: 10000 });
  241 |             await expect(businessClients.cellByHeader(0, 'Client Name')).not.toHaveText(firstAscending, { timeout: 10000 });
  242 |         });
  243 | 
  244 |         test('Excel export downloads an .xlsx file', async ({ page, pageManager }) => {
  245 |             const [download] = await Promise.all([
  246 |                 page.waitForEvent('download', { timeout: 30000 }),
  247 |                 pageManager.businessClientsPage.EXCEL_BUTTON.click(),
  248 |             ]);
  249 |             expect(download.suggestedFilename()).toMatch(/\.xlsx$/);
  250 |         });
  251 | 
  252 |         test('Saving a client with no changes succeeds', async ({ page, pageManager }, testInfo) => {
  253 |             // Re-saves a shared client's settings; run on one browser only (see Account Settings save).
  254 |             test.skip(testInfo.project.name !== 'chromium', 'Writes shared client settings; runs on chromium only.');
  255 |             const businessClients = pageManager.businessClientsPage;
  256 |             const editPage = pageManager.businessClientEditPage;
  257 |             // A client with no product enabled cannot be saved, so pick the last Check-enabled row
  258 |             // on the page (the first rows are the clients other suites reconfigure).
  259 |             const checkEnabled = (await businessClients.cellByHeaderAll('Check?').allInnerTexts()).map((text) => text.includes('Yes'));
  260 |             const rowIndex = checkEnabled.lastIndexOf(true);
  261 |             expect(rowIndex, 'At least one Check-enabled client on the first page').toBeGreaterThanOrEqual(0);
  262 |             const clientLink = businessClients.cellByHeader(rowIndex, 'Client Name').getByRole('link');
  263 |             const clientName = (await clientLink.innerText()).trim();
  264 | 
  265 |             await clientLink.click();
  266 |             await expect(editPage.BUSINESS_NAME_TEXTBOX).toHaveValue(clientName, { timeout: 15000 });
  267 |             await editPage.SAVE_CHANGES_BUTTON.click();
  268 |             await expect(pageManager.settingsPage.TOAST_MESSAGE.filter({ hasText: 'Client info updated successfully' })).toBeVisible({ timeout: 15000 });
  269 |             await expect(page).toHaveURL(/\/client-admin\/business-clients$/);
  270 |         });
  271 | 
  272 |     });
  273 | 
  274 |     // ── Users ──────────────────────────────────────────────────────────────────
  275 | 
  276 |     test.describe('Users', () => {
  277 | 
  278 |         test.beforeEach('Open Users', async ({ page, pageManager }) => {
  279 |             await page.goto('/client-admin/users');
  280 |             await expect(pageManager.usersPage.cellByHeader(0, 'Email')).toBeVisible({ timeout: 15000 });
  281 |         });
  282 | 
  283 |         test('Grid loads with all column headers', async ({ pageManager }) => {
  284 |             const users = pageManager.usersPage;
  285 |             await expect(users.COLUMN_HEADERS).toHaveCount(UsersPage.EXPECTED_COLUMN_HEADERS.length);
  286 |             for (const header of UsersPage.EXPECTED_COLUMN_HEADERS) {
  287 |                 await expect(users.columnHeader(header), `Header "${header}"`).toBeVisible();
  288 |             }
  289 |         });
  290 | 
  291 |         test('Search by email finds the logged-in user', async ({ pageManager }) => {
  292 |             const users = pageManager.usersPage;
  293 |             const email = Constants.USER_FI_EMAIL;
  294 | 
  295 |             await users.SEARCH_TEXTBOX.fill(email);
  296 |             await expect(users.rowByEmail(email)).toBeVisible({ timeout: 15000 });
  297 |             await expect.poll(async () => {
  298 |                 const rows = await users.GRID_ROWS.allInnerTexts();
  299 |                 return rows.every((row) => row.toLowerCase().includes(email.toLowerCase()));
  300 |             }, { timeout: 15000 }).toBe(true);
  301 |         });
  302 | 
  303 |         test('Edit opens the user form populated with that user', async ({ page, pageManager }) => {
  304 |             const users = pageManager.usersPage;
  305 |             const email = Constants.USER_FI_EMAIL;
  306 | 
  307 |             await users.SEARCH_TEXTBOX.fill(email);
  308 |             await users.rowByEmail(email).getByRole('link', { name: /Edit/ }).click();
  309 |             await expect(page).toHaveURL(/\/client-admin\/users\/user\/\d+/, { timeout: 15000 });
  310 |             await expect.poll(async () => (await users.EMAIL_ADDRESS_TEXTBOX.inputValue()).toLowerCase(), { timeout: 15000 })
  311 |                 .toBe(email.toLowerCase());
  312 |             await expect(users.FIRST_NAME_TEXTBOX).not.toHaveValue('');
  313 |             await expect(users.LAST_NAME_TEXTBOX).not.toHaveValue('');
  314 |             await expect(users.UPDATE_USER_BUTTON).toBeVisible();
  315 |         });
  316 | 
  317 |         test('Add User opens an empty form and selecting a role reveals notification settings', async ({ page, pageManager }) => {
  318 |             const users = pageManager.usersPage;
  319 | 
  320 |             await users.ADD_USER_BUTTON.click();
  321 |             await expect(page).toHaveURL(/\/client-admin\/users\/user$/, { timeout: 15000 });
  322 |             await expect(users.FIRST_NAME_TEXTBOX).toHaveValue('', { timeout: 15000 });
  323 |             await expect(users.LAST_NAME_TEXTBOX).toHaveValue('');
  324 |             await expect(users.EMAIL_ADDRESS_TEXTBOX).toHaveValue('');
  325 |             await expect(users.LANDING_PAGE_DROPDOWN).toBeVisible();
  326 |             await expect(users.ADD_USER_SUBMIT_BUTTON).toBeVisible();
  327 | 
> 328 |             await expect(users.SELECT_ROLE_NOTIFICATION_HINT).toBeVisible();
      |                                                               ^ Error: expect(locator).toBeVisible() failed
  329 |             await users.ROLE_PICKERS.first().click();
  330 |             await expect(users.SELECT_ROLE_NOTIFICATION_HINT).toBeHidden({ timeout: 10000 });
  331 |             await expect(users.NOTIFICATION_SETTINGS_HEADER).toBeVisible();
  332 |         });
  333 | 
  334 |         test('Add User with required fields empty is blocked with a message', async ({ page, pageManager }) => {
  335 |             const users = pageManager.usersPage;
  336 |             const settings = pageManager.settingsPage;
  337 | 
  338 |             await users.ADD_USER_BUTTON.click();
  339 |             await expect(users.FIRST_NAME_TEXTBOX).toHaveValue('', { timeout: 15000 });
  340 |             await users.ADD_USER_SUBMIT_BUTTON.click();
  341 |             await expect(settings.MODAL).toContainText('Please provide all required user information', { timeout: 10000 });
  342 |             await settings.MODAL_OK_BUTTON.click();
  343 |             await expect(settings.MODAL).toBeHidden();
  344 |             await expect(page).toHaveURL(/\/client-admin\/users\/user$/);
  345 |         });
  346 | 
  347 |         test('Inactive Users page loads with the users grid', async ({ page, pageManager }) => {
  348 |             const users = pageManager.usersPage;
  349 |             await users.INACTIVE_USERS_BUTTON.click();
  350 |             await expect(page).toHaveURL(/\/client-admin\/users\/Inactive$/, { timeout: 15000 });
  351 |             await expect(pageManager.settingsPage.BREADCRUMB_CURRENT).toHaveText('Inactive Users', { timeout: 15000 });
  352 |             await expect(users.COLUMN_HEADERS).toHaveCount(UsersPage.EXPECTED_COLUMN_HEADERS.length);
  353 |         });
  354 | 
  355 |         test('Api Token icon opens the token dialog', async ({ pageManager }) => {
  356 |             const users = pageManager.usersPage;
  357 |             const settings = pageManager.settingsPage;
  358 |             const email = Constants.USER_FI_EMAIL;
  359 | 
  360 |             await users.SEARCH_TEXTBOX.fill(email);
  361 |             await expect(users.rowByEmail(email)).toBeVisible({ timeout: 15000 });
  362 |             await users.rowByEmail(email).locator('td').nth(UsersPage.EXPECTED_COLUMN_HEADERS.indexOf('Api Token')).locator('a').click();
  363 |             await expect(settings.MODAL_TITLE).toHaveText('Api Token', { timeout: 10000 });
  364 |             await expect(users.API_TOKEN_TEXTAREA).not.toHaveValue('');
  365 |             // Never click Re-Generate here: it would invalidate the shared user's token.
  366 |             await settings.MODAL_OK_BUTTON.click();
  367 |             await expect(settings.MODAL).toBeHidden();
  368 |         });
  369 | 
  370 |     });
  371 | 
  372 |     // ── Roles/Permissions ──────────────────────────────────────────────────────
  373 | 
  374 |     test.describe('Roles/Permissions', () => {
  375 | 
  376 |         test.beforeEach('Open Roles/Permissions', async ({ page, pageManager }) => {
  377 |             await page.goto('/client-admin/roles');
  378 |             // The grid briefly renders "No records available." before data arrives, and loads slowly
  379 |             // when several browser jobs hit the Settings pages at once.
  380 |             await expect(pageManager.rolesPermissionsPage.cellByHeader(0, 'Name')).toBeVisible({ timeout: 30000 });
  381 |         });
  382 | 
  383 |         test('Grid loads with column headers and populated roles', async ({ pageManager }) => {
  384 |             const roles = pageManager.rolesPermissionsPage;
  385 |             await expect(roles.COLUMN_HEADERS).toHaveCount(RolesPermissionsPage.EXPECTED_COLUMN_HEADERS.length);
  386 |             for (const header of RolesPermissionsPage.EXPECTED_COLUMN_HEADERS) {
  387 |                 await expect(roles.columnHeader(header), `Header "${header}"`).toBeVisible();
  388 |             }
  389 |             await expect(roles.cellByHeader(0, 'Name')).not.toHaveText('');
  390 |             await expect(roles.cellByHeader(0, 'Permission(s)')).not.toHaveText('');
  391 |         });
  392 | 
  393 |         test('Add Role opens the role-type dialog', async ({ pageManager }) => {
  394 |             const roles = pageManager.rolesPermissionsPage;
  395 |             await roles.ADD_ROLE_BUTTON.click();
  396 |             await expect(roles.CREATE_ROLE_DIALOG).toBeVisible({ timeout: 10000 });
  397 |             await expect(roles.FI_ROLE_TYPE_BUTTON).toBeVisible();
  398 |             await expect(roles.BC_ROLE_TYPE_BUTTON).toBeVisible();
  399 |         });
  400 | 
  401 |         test('Financial Institution role form shows every permission group', async ({ page, pageManager }) => {
  402 |             const roles = pageManager.rolesPermissionsPage;
  403 |             await roles.ADD_ROLE_BUTTON.click();
  404 |             await roles.FI_ROLE_TYPE_BUTTON.click();
  405 | 
  406 |             await expect(page).toHaveURL(/\/client-admin\/roles\/role$/, { timeout: 15000 });
  407 |             await expect(roles.ROLE_NAME_TEXTBOX).toHaveValue('', { timeout: 15000 });
  408 |             for (const permission of RolesPermissionsPage.FI_PERMISSION_GROUP_SAMPLES) {
  409 |                 await expect(roles.permissionCheckbox(permission), `Permission "${permission}"`).not.toBeChecked();
  410 |             }
  411 |             await expect(roles.SAVE_ROLE_LINK).toBeVisible();
  412 |             await expect(roles.CANCEL_ROLE_LINK).toBeVisible();
  413 |         });
  414 | 
  415 |         test('Business Clients role form shows the business-client permission set', async ({ page, pageManager }) => {
  416 |             const roles = pageManager.rolesPermissionsPage;
  417 |             await roles.ADD_ROLE_BUTTON.click();
  418 |             await roles.BC_ROLE_TYPE_BUTTON.click();
  419 | 
  420 |             await expect(page).toHaveURL(/\/client-admin\/roles\/role-bc$/, { timeout: 15000 });
  421 |             await expect(roles.ROLE_NAME_TEXTBOX).toHaveValue('', { timeout: 15000 });
  422 |             await expect(roles.permissionCheckbox('View Account')).toBeAttached({ timeout: 15000 });
  423 |             await expect(roles.permissionCheckbox(RolesPermissionsPage.FI_ONLY_PERMISSION)).toHaveCount(0);
  424 |         });
  425 | 
  426 |         test('By Permission view lists permissions with their roles', async ({ page, pageManager }) => {
  427 |             const roles = pageManager.rolesPermissionsPage;
  428 |             await roles.BY_PERMISSION_LINK.click();
```