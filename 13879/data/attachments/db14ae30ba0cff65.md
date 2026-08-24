# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\7-ACHSmoke.spec.ts >> ACH — Smoke >> Pay/Return decision badge navigates to exception history
- Location: specs\Smoke\7-ACHSmoke.spec.ts:279:5

# Error details

```
Error: expect(locator).toBeVisible() failed

Locator: locator('.k-grid-filter-popup:visible, [aria-label$="Filter Menu"]:visible, .k-animation-container:visible:has(.k-filter-menu-container)').first()
Expected: visible
Timeout: 30000ms
Error: element(s) not found

Call log:
  - Expect "toBeVisible" with timeout 30000ms
  - waiting for locator('.k-grid-filter-popup:visible, [aria-label$="Filter Menu"]:visible, .k-animation-container:visible:has(.k-filter-menu-container)').first()

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
  - link "  Exceptions 8":
    - /url: /exceptions
  - link "  Settings":
    - /url: /client-admin
  - button "  F.I ACH&CHK User"
- list:
  - listitem:
    - link " ":
      - /url: /
  - listitem:
    - link "ACH":
      - /url: /paid-ach
- group:
  - link " Uploaded ACH":
    - /url: /paid-ach/uploads
  - link "+ Add ACH":
    - /url: /paid-ach/add-ach
- toolbar "Grid toolbar":
  - text: Page Size
  - combobox:
    - option "10"
    - option "20" [selected]
    - option "50"
    - option "100"
  - button "Excel"
  - textbox "Search..."
  - text: Saved Filters
  - combobox:
    - option "[No Filter]" [selected]
    - option "SMK_Default_1786635401462"
  - button "+"
- grid "Data table":
  - rowgroup:
    - 'row "ID ID column filter menu settings Status Status column filter menu settings Decision Decision column filter menu settings Upload ID Upload ID column filter menu settings Added By Added By column filter menu settings Business Client Business Client column filter menu settings Account Account column filter menu settings Originator Originator column filter menu settings Originator Routing # Originator Routing # column filter menu settings Company ID Company ID column filter menu settings Amount Amount column filter menu settings SEC Code SEC Code column filter menu settings Trans Code Trans Code column filter menu settings Trans Type Trans Type column filter menu settings Entry Date  Entry Date column filter menu settings Settlement Date Settlement Date column filter menu settings Transaction ID Transaction ID column filter menu settings Edit Change Log"':
      - columnheader
      - columnheader "ID ID column filter menu settings":
        - text: ID
        - button "ID column filter menu settings"
      - columnheader "Status Status column filter menu settings":
        - text: Status
        - button "Status column filter menu settings"
      - columnheader "Decision Decision column filter menu settings":
        - text: Decision
        - button "Decision column filter menu settings"
      - columnheader "Upload ID Upload ID column filter menu settings":
        - text: Upload ID
        - button "Upload ID column filter menu settings"
      - columnheader "Added By Added By column filter menu settings":
        - text: Added By
        - button "Added By column filter menu settings"
      - columnheader "Business Client Business Client column filter menu settings":
        - text: Business Client
        - button "Business Client column filter menu settings"
      - columnheader "Account Account column filter menu settings":
        - text: Account
        - button "Account column filter menu settings"
      - columnheader "Originator Originator column filter menu settings":
        - text: Originator
        - button "Originator column filter menu settings"
      - 'columnheader "Originator Routing # Originator Routing # column filter menu settings"':
        - text: "Originator Routing #"
        - 'button "Originator Routing # column filter menu settings"'
      - columnheader "Company ID Company ID column filter menu settings":
        - text: Company ID
        - button "Company ID column filter menu settings"
      - columnheader "Amount Amount column filter menu settings":
        - text: Amount
        - button "Amount column filter menu settings"
      - columnheader "SEC Code SEC Code column filter menu settings":
        - text: SEC Code
        - button "SEC Code column filter menu settings"
      - columnheader "Trans Code Trans Code column filter menu settings":
        - text: Trans Code
        - button "Trans Code column filter menu settings"
      - columnheader "Trans Type Trans Type column filter menu settings":
        - text: Trans Type
        - button "Trans Type column filter menu settings"
      - columnheader "Entry Date  Entry Date column filter menu settings":
        - text: Entry Date 
        - button "Entry Date column filter menu settings"
      - columnheader "Settlement Date Settlement Date column filter menu settings":
        - text: Settlement Date
        - button "Settlement Date column filter menu settings"
      - columnheader "Transaction ID Transaction ID column filter menu settings":
        - text: Transaction ID
        - button "Transaction ID column filter menu settings"
      - columnheader "Edit"
      - columnheader "Change Log"
  - rowgroup:
    - row "8952 Completed[Default Decision]  Return  15559 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 102000979 20009 $8,412.50 WEB 27 Debit to Checking 08/20/2026 TXN8412  Delete View ":
      - gridcell
      - gridcell "8952"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8952&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15559"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15559
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "102000979"
      - gridcell "20009"
      - gridcell "$8,412.50"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/20/2026"
      - gridcell
      - gridcell "TXN8412"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8952&ReturnUrl=%2fpaid-ach
    - row "8951 Completed[Default Decision]  Return  15559 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 122199983 123456 $8,411.00 WEB 27 Debit to Checking 08/20/2026 TXN8411  Delete View ":
      - gridcell
      - gridcell "8951"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8951&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15559"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15559
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "122199983"
      - gridcell "123456"
      - gridcell "$8,411.00"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/20/2026"
      - gridcell
      - gridcell "TXN8411"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8951&ReturnUrl=%2fpaid-ach
    - row "8948 Completed[Default Decision]  Return  15542 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 102000979 20009 $9,649.50 WEB 27 Debit to Checking 08/20/2026 TXN9649  Delete View ":
      - gridcell
      - gridcell "8948"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8948&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15542"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15542
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "102000979"
      - gridcell "20009"
      - gridcell "$9,649.50"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/20/2026"
      - gridcell
      - gridcell "TXN9649"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8948&ReturnUrl=%2fpaid-ach
    - row "8947 Completed[Default Decision]  Return  15542 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 122199983 123456 $9,648.00 WEB 27 Debit to Checking 08/20/2026 TXN9648  Delete View ":
      - gridcell
      - gridcell "8947"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8947&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15542"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15542
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "122199983"
      - gridcell "123456"
      - gridcell "$9,648.00"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/20/2026"
      - gridcell
      - gridcell "TXN9648"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8947&ReturnUrl=%2fpaid-ach
    - row "8915 Completed[Manual Decision]  Return  15462 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 102000979 20009 $8,164.50 WEB 27 Debit to Checking 08/19/2026 TXN8164  Delete View ":
      - gridcell
      - gridcell "8915"
      - gridcell "Completed[Manual Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8915&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15462"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15462
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "102000979"
      - gridcell "20009"
      - gridcell "$8,164.50"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN8164"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8915&ReturnUrl=%2fpaid-ach
    - row "8914 Completed[Manual Decision]  Return  15462 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 122199983 123456 $8,163.00 WEB 27 Debit to Checking 08/19/2026 TXN8163  Delete View ":
      - gridcell
      - gridcell "8914"
      - gridcell "Completed[Manual Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8914&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15462"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15462
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "122199983"
      - gridcell "123456"
      - gridcell "$8,163.00"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN8163"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8914&ReturnUrl=%2fpaid-ach
    - row "8911 Completed[Default Decision]  Return  15449 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 102000979 20009 $4,078.50 WEB 27 Debit to Checking 08/19/2026 TXN4078  Delete View ":
      - gridcell
      - gridcell "8911"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8911&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15449"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15449
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "102000979"
      - gridcell "20009"
      - gridcell "$4,078.50"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN4078"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8911&ReturnUrl=%2fpaid-ach
    - row "8910 Completed[Default Decision]  Return  15449 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 122199983 123456 $4,077.00 WEB 27 Debit to Checking 08/19/2026 TXN4077  Delete View ":
      - gridcell
      - gridcell "8910"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8910&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15449"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15449
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "122199983"
      - gridcell "123456"
      - gridcell "$4,077.00"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN4077"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8910&ReturnUrl=%2fpaid-ach
    - row "8909 Completed[Default Decision]  Return  15445 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 102000979 20009 $7,200.50 WEB 27 Debit to Checking 08/19/2026 TXN7200  Delete View ":
      - gridcell
      - gridcell "8909"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8909&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15445"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15445
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "102000979"
      - gridcell "20009"
      - gridcell "$7,200.50"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN7200"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8909&ReturnUrl=%2fpaid-ach
    - row "8908 Completed[Default Decision]  Return  15445 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 122199983 123456 $7,199.00 WEB 27 Debit to Checking 08/19/2026 TXN7199  Delete View ":
      - gridcell
      - gridcell "8908"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8908&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15445"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15445
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "122199983"
      - gridcell "123456"
      - gridcell "$7,199.00"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN7199"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8908&ReturnUrl=%2fpaid-ach
    - row "8907 Completed[Default Decision]  Return  15438 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 102000979 20009 $1,353.50 WEB 27 Debit to Checking 08/19/2026 TXN1353  Delete View ":
      - gridcell
      - gridcell "8907"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8907&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15438"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15438
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "102000979"
      - gridcell "20009"
      - gridcell "$1,353.50"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN1353"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8907&ReturnUrl=%2fpaid-ach
    - row "8906 Completed[Default Decision]  Return  15438 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 122199983 123456 $1,352.00 WEB 27 Debit to Checking 08/19/2026 TXN1352  Delete View ":
      - gridcell
      - gridcell "8906"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8906&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15438"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15438
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "122199983"
      - gridcell "123456"
      - gridcell "$1,352.00"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN1352"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8906&ReturnUrl=%2fpaid-ach
    - row "8904 Completed[Default Decision]  Return  15430 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 102000979 20009 $8,477.50 WEB 27 Debit to Checking 08/19/2026 TXN8477  Delete View ":
      - gridcell
      - gridcell "8904"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8904&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15430"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15430
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "102000979"
      - gridcell "20009"
      - gridcell "$8,477.50"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN8477"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8904&ReturnUrl=%2fpaid-ach
    - row "8903 Completed[Default Decision]  Return  15430 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 122199983 123456 $8,476.00 WEB 27 Debit to Checking 08/19/2026 TXN8476  Delete View ":
      - gridcell
      - gridcell "8903"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8903&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15430"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15430
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "122199983"
      - gridcell "123456"
      - gridcell "$8,476.00"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN8476"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8903&ReturnUrl=%2fpaid-ach
    - row "8902 Completed[Default Decision]  Return  15428 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 102000979 20009 $7,143.50 WEB 27 Debit to Checking 08/19/2026 TXN7143  Delete View ":
      - gridcell
      - gridcell "8902"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8902&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15428"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15428
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "102000979"
      - gridcell "20009"
      - gridcell "$7,143.50"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN7143"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8902&ReturnUrl=%2fpaid-ach
    - row "8901 Completed[Default Decision]  Return  15428 ACH_FixedLength.txt PJ_BC_Boutique(Both) Account6 ACH Originator 122199983 123456 $7,142.00 WEB 27 Debit to Checking 08/19/2026 TXN7142  Delete View ":
      - gridcell
      - gridcell "8901"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8901&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15428"
      - gridcell "ACH_FixedLength.txt":
        - link "ACH_FixedLength.txt":
          - /url: /paid-ach/uploads?Id=15428
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "122199983"
      - gridcell "123456"
      - gridcell "$7,142.00"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN7142"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8901&ReturnUrl=%2fpaid-ach
    - row "8900 Completed[Default Decision]  Return  15427 ACH_FixedLength_debug_account6.txt PJ_BC_Boutique(Both) Account6 ACH Originator 102000979 20009 $1,607.50 WEB 27 Debit to Checking 08/19/2026 TXN1607  Delete View ":
      - gridcell
      - gridcell "8900"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8900&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15427"
      - gridcell "ACH_FixedLength_debug_account6.txt":
        - link "ACH_FixedLength_debug_account6.txt":
          - /url: /paid-ach/uploads?Id=15427
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "102000979"
      - gridcell "20009"
      - gridcell "$1,607.50"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN1607"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8900&ReturnUrl=%2fpaid-ach
    - row "8899 Completed[Default Decision]  Return  15427 ACH_FixedLength_debug_account6.txt PJ_BC_Boutique(Both) Account6 ACH Originator 122199983 123456 $1,606.00 WEB 27 Debit to Checking 08/19/2026 TXN1606  Delete View ":
      - gridcell
      - gridcell "8899"
      - gridcell "Completed[Default Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=8899&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell "15427"
      - gridcell "ACH_FixedLength_debug_account6.txt":
        - link "ACH_FixedLength_debug_account6.txt":
          - /url: /paid-ach/uploads?Id=15427
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account6"
      - gridcell "ACH Originator"
      - gridcell "122199983"
      - gridcell "123456"
      - gridcell "$1,606.00"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "08/19/2026"
      - gridcell
      - gridcell "TXN1606"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=8899&ReturnUrl=%2fpaid-ach
    - row "4971 Completed[Automatic Decision]  Return  F.I ACH&CHK User PJ_BC_Boutique(Both) Account2 OGName 32456789 hkjhkh $100.00 WEB 27 Debit to Checking 03/24/2026 35435  Delete View ":
      - gridcell
      - gridcell "4971"
      - gridcell "Completed[Automatic Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=4971&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell
      - gridcell "F.I ACH&CHK User"
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account2"
      - gridcell "OGName"
      - gridcell "32456789"
      - gridcell "hkjhkh"
      - gridcell "$100.00"
      - gridcell "WEB"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "03/24/2026"
      - gridcell
      - gridcell "35435"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=4971&ReturnUrl=%2fpaid-ach
    - row "3764 Completed[Automatic Decision]  Return  F.I ACH&CHK User PJ_BC_Boutique(Both) Account2 OGName 32456789 yiuyi686789 $678.00 CCD 27 Debit to Checking 01/16/2026 35435  Delete View ":
      - gridcell
      - gridcell "3764"
      - gridcell "Completed[Automatic Decision]"
      - gridcell " Return ":
        - link " Return ":
          - /url: /exceptions/history?Id=3764&ExceptionType=ACH&ReturnUrl=%2fpaid-ach
      - gridcell
      - gridcell "F.I ACH&CHK User"
      - gridcell "PJ_BC_Boutique(Both)"
      - gridcell "Account2"
      - gridcell "OGName"
      - gridcell "32456789"
      - gridcell "yiuyi686789"
      - gridcell "$678.00"
      - gridcell "CCD"
      - gridcell "27"
      - gridcell "Debit to Checking"
      - gridcell "01/16/2026"
      - gridcell
      - gridcell "35435"
      - gridcell " Delete":
        - link " Delete":
          - /url: javascript:;
      - gridcell "View ":
        - link "View ":
          - /url: /client-admin/entity-log?EntityType=ACH&EntityId=3764&ReturnUrl=%2fpaid-ach
- application "Page navigation, page 1 of 2":
  - button "Go to the first page" [disabled]
  - button "Go to the previous page" [disabled]
  - text: Page
  - spinbutton "Select a page": "1"
  - text: of 2
  - button "Go to the next page"
  - button "Go to the last page"
  - text: 1 - 20 of 39 items
- contentinfo:
  - text: PJ_FI_Bank (Playwright Automation)[uat-release] © Copyright Advanced Fraud Solutions 2005-2026 | All Rights Reserved |
  - link "Privacy Policy":
    - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  198 |         // Save the active column filter as a named preset.
  199 |         const presetName = `SMK_ID_${Date.now()}`;
  200 |         await pageManager.achPage.saveCurrentFilterAs(presetName);
  201 | 
  202 |         // The dropdown should auto-select the newly saved preset.
  203 |         await expect(pageManager.achPage.savedFiltersDropdown).toHaveValue(presetName, { timeout: 10000 });
  204 | 
  205 |         // Cleanup: select the preset (delete button only appears when one is selected), delete it.
  206 |         await expect(pageManager.achPage.deleteSavedFilterButton).toBeVisible();
  207 |         await pageManager.achPage.deleteSavedFilterButton.click();
  208 |         await expect(pageManager.achPage.confirmDialog).toBeVisible();
  209 |         await pageManager.achPage.confirmDialogConfirmButton.click();
  210 |         await expect(pageManager.achPage.confirmDialog).toBeHidden({ timeout: 10000 });
  211 |         await expect.poll(
  212 |             async () => pageManager.achPage.savedFiltersDropdown.locator('option').allInnerTexts(),
  213 |             { timeout: 10000 }
  214 |         ).not.toContain(presetName);
  215 |     });
  216 | 
  217 |     // ── Column sort ───────────────────────────────────────────────────────────
  218 | 
  219 |     test('Clicking a column header sorts ascending, clicking again sorts descending', async ({ pageManager, page }) => {
  220 |         // Click the sortable title text inside the Company ID column header (not the filter button).
  221 |         // Note: the "ID" column's title span can render at zero width, so Company ID is used instead.
  222 |         await pageManager.achPage.columnHeaderCompanyId.getByText('Company ID', { exact: true }).click();
  223 |         await expect(page.getByRole('columnheader', { name: 'Sorted in ascending order' }))
  224 |             .toBeVisible({ timeout: 10000 });
  225 | 
  226 |         await page.getByRole('columnheader', { name: 'Sorted in ascending order' })
  227 |             .getByText('Company ID', { exact: true }).click();
  228 |         await expect(page.getByRole('columnheader', { name: 'Sorted in descending order' }))
  229 |             .toBeVisible({ timeout: 10000 });
  230 |     });
  231 | 
  232 |     // ── Column filter ─────────────────────────────────────────────────────────
  233 | 
  234 |     test('Column filter popup applies a filter and Clear restores the full row set', async ({ pageManager }) => {
  235 |         const baseline = await pageManager.achPage.gridRows.count();
  236 |         // ID is at td index 1 in the default ACH column order.
  237 |         const idValue = (await pageManager.achPage.gridRows.first().locator('td').nth(1).innerText()).trim();
  238 | 
  239 |         await pageManager.achPage.columnFilterButton('ID').click();
  240 |         await expect(pageManager.achPage.columnFilterPopup).toBeVisible();
  241 |         const input = pageManager.achPage.columnFilterPopup
  242 |             .locator('input[role="spinbutton"], input[type="text"], input.k-input-inner').first();
  243 |         await input.fill(idValue);
  244 |         await input.press('Tab');
  245 |         await pageManager.achPage.columnFilterApplyButton.click();
  246 |         await expect(pageManager.achPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  247 |         await expect(pageManager.achPage.gridRows.first()).toBeVisible({ timeout: 10000 });
  248 | 
  249 |         // Clear the filter and verify baseline is restored
  250 |         await pageManager.achPage.columnFilterButton('ID').click();
  251 |         await expect(pageManager.achPage.columnFilterPopup).toBeVisible();
  252 |         await pageManager.achPage.columnFilterClearButton.click();
  253 |         await expect(pageManager.achPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  254 |         await expect.poll(async () => pageManager.achPage.gridRows.count(), { timeout: 10000 })
  255 |             .toBe(baseline);
  256 |     });
  257 | 
  258 |     // ── Row actions ───────────────────────────────────────────────────────────
  259 | 
  260 |     test('"View" (Change Log) link on a row navigates to the entity log', async ({ pageManager, page }) => {
  261 |         await pageManager.achPage.gridRows.first()
  262 |             .getByRole('link', { name: /View/ }).click();
  263 |         await expect(page).toHaveURL(/\/client-admin\/entity-log/, { timeout: 15000 });
  264 |     });
  265 | 
  266 |     test('"Delete" on a row shows a confirm modal; Cancel dismisses it without deleting', async ({ pageManager }) => {
  267 |         const rowCountBefore = await pageManager.achPage.gridRows.count();
  268 |         await pageManager.achPage.gridRows.first()
  269 |             .getByRole('link', { name: /Delete/ }).click();
  270 |         await expect(pageManager.achPage.confirmDialog).toBeVisible({ timeout: 10000 });
  271 |         await expect(pageManager.achPage.confirmDialog)
  272 |             .toContainText('This action cannot be undone');
  273 |         await pageManager.achPage.confirmDialogCancelButton.click();
  274 |         await expect(pageManager.achPage.confirmDialog).toBeHidden({ timeout: 10000 });
  275 |         // Row count must be unchanged after cancelling
  276 |         expect(await pageManager.achPage.gridRows.count()).toBe(rowCountBefore);
  277 |     });
  278 | 
  279 |     test('Pay/Return decision badge navigates to exception history', async ({ pageManager, page }) => {
  280 |         // ── Pay badge ─────────────────────────────────────────────────────────
  281 |         await pageManager.achPage.columnFilterButton('Decision').click();
  282 |         await expect(pageManager.achPage.columnFilterPopup).toBeVisible();
  283 |         let popup = pageManager.achPage.columnFilterPopup;
  284 |         await popup.getByLabel('Select All').setChecked(false);
  285 |         await popup.getByLabel('Pay').setChecked(true);
  286 |         await pageManager.achPage.columnFilterApplyButton.click();
  287 |         await expect(pageManager.achPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  288 | 
  289 |         await expect(pageManager.achPage.firstCompletedDecisionBadge).toBeVisible({ timeout: 15000 });
  290 |         await pageManager.achPage.firstCompletedDecisionBadge.click();
  291 |         await expect(page).toHaveURL(/\/exceptions\/history/, { timeout: 15000 });
  292 | 
  293 |         // ── Return badge ──────────────────────────────────────────────────────
  294 |         await page.goBack();
  295 |         await pageManager.achPage.waitForGridLoad();
  296 | 
  297 |         await pageManager.achPage.columnFilterButton('Decision').click();
> 298 |         await expect(pageManager.achPage.columnFilterPopup).toBeVisible();
      |                                                             ^ Error: expect(locator).toBeVisible() failed
  299 |         popup = pageManager.achPage.columnFilterPopup;
  300 |         await popup.getByLabel('Select All').setChecked(false);
  301 |         await popup.getByLabel('Return').setChecked(true);
  302 |         await pageManager.achPage.columnFilterApplyButton.click();
  303 |         await expect(pageManager.achPage.columnFilterPopup).toBeHidden({ timeout: 10000 });
  304 | 
  305 |         await expect(pageManager.achPage.firstCompletedDecisionBadge).toBeVisible({ timeout: 15000 });
  306 |         await pageManager.achPage.firstCompletedDecisionBadge.click();
  307 |         await expect(page).toHaveURL(/\/exceptions\/history/, { timeout: 15000 });
  308 |     });
  309 | 
  310 |     // ── Breadcrumb ────────────────────────────────────────────────────────────
  311 | 
  312 |     test('ACH breadcrumb link is visible on the page', async ({ pageManager }) => {
  313 |         await expect(pageManager.achPage.pageHeading).toBeVisible();
  314 |     });
  315 | 
  316 | });
  317 | 
```