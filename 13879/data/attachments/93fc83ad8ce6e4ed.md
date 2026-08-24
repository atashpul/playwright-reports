# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\8-ExceptionsSmoke.spec.ts >> Exceptions — Smoke >> Column filter menu applies a filter and Clear restores the full row set
- Location: specs\Smoke\8-ExceptionsSmoke.spec.ts:212:5

# Error details

```
TimeoutError: locator.waitFor: Timeout 10000ms exceeded.
Call log:
  - waiting for locator('.k-grid-filter-popup[aria-label="Business Client Filter Menu"]') to be visible

```

# Page snapshot

```yaml
- generic [ref=f1e1]:
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
        - link "  Exceptions 8" [ref=f1e33] [cursor=pointer]:
          - /url: /exceptions
          - generic [ref=f1e34]:  
          - generic [ref=f1e36]: Exceptions
          - generic [ref=f1e38]: "8"
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
      - list [ref=f1e56]:
        - listitem [ref=f1e57]:
          - link " " [ref=f1e58] [cursor=pointer]:
            - /url: /
        - listitem [ref=f1e60]:
          - link "Exceptions" [ref=f1e61] [cursor=pointer]:
            - /url: /exceptions
        - listitem [ref=f1e62]:
          - link "History" [ref=f1e63]:
            - /url: javascript:;
      - generic [ref=f1e65]:
        - toolbar "Grid toolbar" [ref=f1e66]:
          - generic [ref=f1e67]:
            - generic [ref=f1e68]:
              - generic [ref=f1e69]:
                - generic [ref=f1e70]: Page Size
                - combobox [ref=f1e72]:
                  - option "10"
                  - option "20" [selected]
                  - option "50"
                  - option "100"
              - button "Excel" [ref=f1e73] [cursor=pointer]
              - textbox "Search..." [ref=f1e80]
            - button " Mark as Reviewed [0]" [ref=f1e82] [cursor=pointer]:
              - generic [ref=f1e83]: 
              - text: Mark as Reviewed [0]
            - generic [ref=f1e85]:
              - generic [ref=f1e86]: Saved Filters
              - combobox [ref=f1e88]:
                - option "[No Filter]"
                - option "Active"
                - option "Reviewed"
                - option "SMK_Default_4421" [selected]
              - generic [ref=f1e89]:
                - button "" [ref=f1e90] [cursor=pointer]
                - button "" [ref=f1e92] [cursor=pointer]
        - grid "Data table" [ref=f1e94]:
          - rowgroup [ref=f1e124]:
            - row [ref=f1e125]:
              - columnheader [ref=f1e126]:
                - checkbox "Select all rows" [ref=f1e128] [cursor=pointer]
              - columnheader "Reviewed? Reviewed? column filter menu settings" [ref=f1e129]:
                - generic [ref=f1e130]:
                  - generic [ref=f1e131] [cursor=pointer]: Reviewed?
                  - button "Reviewed? column filter menu settings" [ref=f1e133]
              - columnheader "ID ID column filter menu settings" [ref=f1e138]:
                - generic [ref=f1e139]:
                  - generic [ref=f1e140] [cursor=pointer]: ID
                  - button "ID column filter menu settings" [ref=f1e142]
              - columnheader "Status Status column filter menu settings" [ref=f1e147]:
                - generic [ref=f1e148]:
                  - generic [ref=f1e149] [cursor=pointer]: Status
                  - button "Status column filter menu settings" [ref=f1e151]
              - columnheader "Business Client Business Client column filter menu settings" [ref=f1e156]:
                - generic [ref=f1e157]:
                  - generic [ref=f1e158] [cursor=pointer]: Business Client
                  - button "Business Client column filter menu settings" [active] [ref=f1e160] [cursor=pointer]
              - columnheader "Type Type column filter menu settings" [ref=f1e165]:
                - generic [ref=f1e166]:
                  - generic [ref=f1e167] [cursor=pointer]: Type
                  - button "Type column filter menu settings" [ref=f1e169]
              - columnheader "Decision Decision column filter menu settings" [ref=f1e174]:
                - generic [ref=f1e175]:
                  - generic [ref=f1e176] [cursor=pointer]: Decision
                  - button "Decision column filter menu settings" [ref=f1e178]
              - columnheader "Reference ID Reference ID column filter menu settings" [ref=f1e183]:
                - generic [ref=f1e184]:
                  - generic [ref=f1e185] [cursor=pointer]: Reference ID
                  - button "Reference ID column filter menu settings" [ref=f1e187]
              - 'columnheader "Routing # Routing # column filter menu settings" [ref=f1e192]':
                - generic [ref=f1e193]:
                  - generic [ref=f1e194] [cursor=pointer]: "Routing #"
                  - 'button "Routing # column filter menu settings" [ref=f1e196]'
              - 'columnheader "Account # Account # column filter menu settings" [ref=f1e201]':
                - generic [ref=f1e202]:
                  - generic [ref=f1e203] [cursor=pointer]: "Account #"
                  - 'button "Account # column filter menu settings" [ref=f1e205]'
              - columnheader "Account Name Account Name column filter menu settings" [ref=f1e210]:
                - generic [ref=f1e211]:
                  - generic [ref=f1e212] [cursor=pointer]: Account Name
                  - button "Account Name column filter menu settings" [ref=f1e214]
              - 'columnheader "Check #/SEC Code Check #/SEC Code column filter menu settings" [ref=f1e219]':
                - generic [ref=f1e220]:
                  - generic [ref=f1e221] [cursor=pointer]: "Check #/SEC Code"
                  - 'button "Check #/SEC Code column filter menu settings" [ref=f1e223]'
              - columnheader "Amount Amount column filter menu settings" [ref=f1e228]:
                - generic [ref=f1e229]:
                  - generic [ref=f1e230] [cursor=pointer]: Amount
                  - button "Amount column filter menu settings" [ref=f1e232]
              - columnheader "Payee/Originator Payee/Originator column filter menu settings" [ref=f1e237]:
                - generic [ref=f1e238]:
                  - generic [ref=f1e239] [cursor=pointer]: Payee/Originator
                  - button "Payee/Originator column filter menu settings" [ref=f1e241]
              - columnheader "Trans Code Trans Code column filter menu settings" [ref=f1e246]:
                - generic [ref=f1e247]:
                  - generic [ref=f1e248] [cursor=pointer]: Trans Code
                  - button "Trans Code column filter menu settings" [ref=f1e250]
              - columnheader "Trans Type Trans Type column filter menu settings" [ref=f1e255]:
                - generic [ref=f1e256]:
                  - generic [ref=f1e257] [cursor=pointer]: Trans Type
                  - button "Trans Type column filter menu settings" [ref=f1e259]
              - columnheader "Trans Date  Trans Date column filter menu settings" [ref=f1e264]:
                - generic [ref=f1e265]:
                  - generic [ref=f1e267] [cursor=pointer]:
                    - text: Trans Date
                    - generic "Check Presented Date or ACH Entry Date or the date when ACH transaction was presented" [ref=f1e268]: 
                  - button "Trans Date column filter menu settings" [ref=f1e269]
              - columnheader "Settlement Date Settlement Date column filter menu settings" [ref=f1e274]:
                - generic [ref=f1e275]:
                  - generic [ref=f1e276] [cursor=pointer]: Settlement Date
                  - button "Settlement Date column filter menu settings" [ref=f1e278]
              - columnheader "Issued Check Data" [ref=f1e283]
              - columnheader "Check Image" [ref=f1e285]
              - columnheader "Exception Reason Exception Reason column filter menu settings" [ref=f1e287]:
                - generic [ref=f1e288]:
                  - generic [ref=f1e289] [cursor=pointer]: Exception Reason
                  - button "Exception Reason column filter menu settings" [ref=f1e291]
              - columnheader "Exception" [ref=f1e296]
              - columnheader [ref=f1e298]:
                - text: Exception Date
                - button "Exception Date column filter menu settings" [ref=f1e299]
              - columnheader "Approval" [ref=f1e304]
              - columnheader "Decision By Decision By column filter menu settings" [ref=f1e306]:
                - generic [ref=f1e307]:
                  - generic [ref=f1e308] [cursor=pointer]: Decision By
                  - button "Decision By column filter menu settings" [ref=f1e310]
              - columnheader "Decision Notes Decision Notes column filter menu settings" [ref=f1e315]:
                - generic [ref=f1e316]:
                  - generic [ref=f1e317] [cursor=pointer]: Decision Notes
                  - button "Decision Notes column filter menu settings" [ref=f1e319]
              - columnheader [ref=f1e324]:
                - text: Decision Date
                - button "Decision Date column filter menu settings" [ref=f1e325]
              - columnheader "Return Reason Return Reason column filter menu settings" [ref=f1e330]:
                - generic [ref=f1e331]:
                  - generic [ref=f1e332] [cursor=pointer]: Return Reason
                  - button "Return Reason column filter menu settings" [ref=f1e334]
          - rowgroup [ref=f1e372]:
            - row [ref=f1e373]:
              - gridcell [ref=f1e374]:
                - checkbox "Select a row" [ref=f1e377] [cursor=pointer]
              - gridcell " No" [ref=f1e378]:
                - generic [ref=f1e379]: 
                - text: "No"
              - gridcell "8952" [ref=f1e380]
              - gridcell "Completed[Default Decision]" [ref=f1e381]:
                - text: Completed
                - generic [ref=f1e382]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e383]
              - gridcell "ACH" [ref=f1e384]
              - gridcell [ref=f1e385]:
                - link " Return" [ref=f1e386] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e387]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e388]
              - gridcell "102000979" [ref=f1e389]
              - gridcell [ref=f1e390]
              - gridcell "Account6" [ref=f1e391]
              - gridcell "WEB" [ref=f1e392]
              - gridcell "$8,412.50" [ref=f1e393]
              - gridcell "ACH Originator" [ref=f1e394]
              - gridcell "27" [ref=f1e395]
              - gridcell "Debit to Checking" [ref=f1e396]
              - gridcell "08/20/2026" [ref=f1e397]
              - gridcell [ref=f1e398]
              - gridcell [ref=f1e399]
              - gridcell [ref=f1e400]
              - gridcell [ref=f1e401]
              - gridcell [ref=f1e402]:
                - link " View" [ref=f1e403] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e404]: 
                  - text: View
              - gridcell "08/20/2026 5:03 PM EDT" [ref=f1e405]:
                - text: 08/20/2026
                - generic [ref=f1e406]: 5:03 PM EDT
              - gridcell [ref=f1e407]
              - gridcell "[Default Decision]" [ref=f1e408]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e409]
              - gridcell "08/21/2026 11:00 AM EDT" [ref=f1e410]:
                - text: 08/21/2026
                - generic [ref=f1e411]: 11:00 AM EDT
              - gridcell [ref=f1e412]
            - row [ref=f1e413]:
              - gridcell [ref=f1e414]:
                - checkbox "Select a row" [ref=f1e417] [cursor=pointer]
              - gridcell " No" [ref=f1e418]:
                - generic [ref=f1e419]: 
                - text: "No"
              - gridcell "8951" [ref=f1e420]
              - gridcell "Completed[Default Decision]" [ref=f1e421]:
                - text: Completed
                - generic [ref=f1e422]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e423]
              - gridcell "ACH" [ref=f1e424]
              - gridcell [ref=f1e425]:
                - link " Return" [ref=f1e426] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e427]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e428]
              - gridcell "122199983" [ref=f1e429]
              - gridcell [ref=f1e430]
              - gridcell "Account6" [ref=f1e431]
              - gridcell "WEB" [ref=f1e432]
              - gridcell "$8,411.00" [ref=f1e433]
              - gridcell "ACH Originator" [ref=f1e434]
              - gridcell "27" [ref=f1e435]
              - gridcell "Debit to Checking" [ref=f1e436]
              - gridcell "08/20/2026" [ref=f1e437]
              - gridcell [ref=f1e438]
              - gridcell [ref=f1e439]
              - gridcell [ref=f1e440]
              - gridcell [ref=f1e441]
              - gridcell [ref=f1e442]:
                - link " View" [ref=f1e443] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e444]: 
                  - text: View
              - gridcell "08/20/2026 5:03 PM EDT" [ref=f1e445]:
                - text: 08/20/2026
                - generic [ref=f1e446]: 5:03 PM EDT
              - gridcell [ref=f1e447]
              - gridcell "[Default Decision]" [ref=f1e448]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e449]
              - gridcell "08/21/2026 11:00 AM EDT" [ref=f1e450]:
                - text: 08/21/2026
                - generic [ref=f1e451]: 11:00 AM EDT
              - gridcell [ref=f1e452]
            - row [ref=f1e453]:
              - gridcell [ref=f1e454]:
                - checkbox "Select a row" [ref=f1e457] [cursor=pointer]
              - gridcell " No" [ref=f1e458]:
                - generic [ref=f1e459]: 
                - text: "No"
              - gridcell "8948" [ref=f1e460]
              - gridcell "Completed[Default Decision]" [ref=f1e461]:
                - text: Completed
                - generic [ref=f1e462]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e463]
              - gridcell "ACH" [ref=f1e464]
              - gridcell [ref=f1e465]:
                - link " Return" [ref=f1e466] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e467]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e468]
              - gridcell "102000979" [ref=f1e469]
              - gridcell [ref=f1e470]
              - gridcell "Account6" [ref=f1e471]
              - gridcell "WEB" [ref=f1e472]
              - gridcell "$9,649.50" [ref=f1e473]
              - gridcell "ACH Originator" [ref=f1e474]
              - gridcell "27" [ref=f1e475]
              - gridcell "Debit to Checking" [ref=f1e476]
              - gridcell "08/20/2026" [ref=f1e477]
              - gridcell [ref=f1e478]
              - gridcell [ref=f1e479]
              - gridcell [ref=f1e480]
              - gridcell [ref=f1e481]
              - gridcell [ref=f1e482]:
                - link " View" [ref=f1e483] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e484]: 
                  - text: View
              - gridcell "08/20/2026 4:35 PM EDT" [ref=f1e485]:
                - text: 08/20/2026
                - generic [ref=f1e486]: 4:35 PM EDT
              - gridcell [ref=f1e487]
              - gridcell "[Default Decision]" [ref=f1e488]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e489]
              - gridcell "08/21/2026 11:00 AM EDT" [ref=f1e490]:
                - text: 08/21/2026
                - generic [ref=f1e491]: 11:00 AM EDT
              - gridcell [ref=f1e492]
            - row [ref=f1e493]:
              - gridcell [ref=f1e494]:
                - checkbox "Select a row" [ref=f1e497] [cursor=pointer]
              - gridcell " No" [ref=f1e498]:
                - generic [ref=f1e499]: 
                - text: "No"
              - gridcell "8947" [ref=f1e500]
              - gridcell "Completed[Default Decision]" [ref=f1e501]:
                - text: Completed
                - generic [ref=f1e502]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e503]
              - gridcell "ACH" [ref=f1e504]
              - gridcell [ref=f1e505]:
                - link " Return" [ref=f1e506] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e507]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e508]
              - gridcell "122199983" [ref=f1e509]
              - gridcell [ref=f1e510]
              - gridcell "Account6" [ref=f1e511]
              - gridcell "WEB" [ref=f1e512]
              - gridcell "$9,648.00" [ref=f1e513]
              - gridcell "ACH Originator" [ref=f1e514]
              - gridcell "27" [ref=f1e515]
              - gridcell "Debit to Checking" [ref=f1e516]
              - gridcell "08/20/2026" [ref=f1e517]
              - gridcell [ref=f1e518]
              - gridcell [ref=f1e519]
              - gridcell [ref=f1e520]
              - gridcell [ref=f1e521]
              - gridcell [ref=f1e522]:
                - link " View" [ref=f1e523] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e524]: 
                  - text: View
              - gridcell "08/20/2026 4:35 PM EDT" [ref=f1e525]:
                - text: 08/20/2026
                - generic [ref=f1e526]: 4:35 PM EDT
              - gridcell [ref=f1e527]
              - gridcell "[Default Decision]" [ref=f1e528]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e529]
              - gridcell "08/21/2026 11:00 AM EDT" [ref=f1e530]:
                - text: 08/21/2026
                - generic [ref=f1e531]: 11:00 AM EDT
              - gridcell [ref=f1e532]
            - row [ref=f1e533]:
              - gridcell [ref=f1e534]:
                - checkbox "Select a row" [ref=f1e537] [cursor=pointer]
              - gridcell " No" [ref=f1e538]:
                - generic [ref=f1e539]: 
                - text: "No"
              - gridcell "33777" [ref=f1e540]
              - gridcell "Pending Pre-Decision" [ref=f1e541]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e542]
              - gridcell "Check" [ref=f1e543]
              - gridcell [ref=f1e544]:
                - link " Pending " [ref=f1e545] [cursor=pointer]:
                  - /url: /exceptions/33777?ReturnUrl=%2fexceptions%2fhistory
                  - generic [ref=f1e546]: 
                  - text: Pending
                  - generic [ref=f1e547]: 
              - gridcell "Exlid123" [ref=f1e548]
              - gridcell "231382306" [ref=f1e549]
              - gridcell "7578091758" [ref=f1e550]
              - gridcell "Account2" [ref=f1e551]
              - gridcell "420254117" [ref=f1e552]
              - gridcell "$815.00" [ref=f1e553]
              - gridcell "AutoPresentedPayee" [ref=f1e554]
              - gridcell [ref=f1e555]
              - gridcell [ref=f1e556]
              - gridcell "08/20/2026" [ref=f1e557]
              - gridcell [ref=f1e558]
              - gridcell [ref=f1e559]
              - gridcell [ref=f1e560]
              - 'gridcell "Check # Not Found" [ref=f1e561]'
              - gridcell [ref=f1e562]:
                - link "View " [ref=f1e563] [cursor=pointer]:
                  - /url: /exceptions/33777?ReturnUrl=%2fexceptions%2fhistory
                  - text: View
                  - generic [ref=f1e564]: 
              - gridcell "08/20/2026 5:05 PM EDT" [ref=f1e565]:
                - text: 08/20/2026
                - generic [ref=f1e566]: 5:05 PM EDT
              - gridcell [ref=f1e567]
              - gridcell [ref=f1e568]
              - gridcell [ref=f1e569]
              - gridcell [ref=f1e570]
              - gridcell [ref=f1e571]
            - row [ref=f1e572]:
              - gridcell [ref=f1e573]:
                - checkbox "Select a row" [ref=f1e576] [cursor=pointer]
              - gridcell " No" [ref=f1e577]:
                - generic [ref=f1e578]: 
                - text: "No"
              - gridcell "33775" [ref=f1e579]
              - gridcell "Pending Pre-Decision" [ref=f1e580]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e581]
              - gridcell "Check" [ref=f1e582]
              - gridcell [ref=f1e583]:
                - link " Pending " [ref=f1e584] [cursor=pointer]:
                  - /url: /exceptions/33775?ReturnUrl=%2fexceptions%2fhistory
                  - generic [ref=f1e585]: 
                  - text: Pending
                  - generic [ref=f1e586]: 
              - gridcell "Exlid123" [ref=f1e587]
              - gridcell "231382306" [ref=f1e588]
              - gridcell "7578091758" [ref=f1e589]
              - gridcell "Account2" [ref=f1e590]
              - gridcell "885284" [ref=f1e591]
              - gridcell "$531.00" [ref=f1e592]
              - gridcell [ref=f1e593]
              - gridcell [ref=f1e594]
              - gridcell [ref=f1e595]
              - gridcell "08/20/2026" [ref=f1e596]
              - gridcell [ref=f1e597]
              - gridcell [ref=f1e598]
              - gridcell [ref=f1e599]
              - 'gridcell "Check # Not Found" [ref=f1e600]'
              - gridcell [ref=f1e601]:
                - link "View " [ref=f1e602] [cursor=pointer]:
                  - /url: /exceptions/33775?ReturnUrl=%2fexceptions%2fhistory
                  - text: View
                  - generic [ref=f1e603]: 
              - gridcell "08/20/2026 4:49 PM EDT" [ref=f1e604]:
                - text: 08/20/2026
                - generic [ref=f1e605]: 4:49 PM EDT
              - gridcell [ref=f1e606]
              - gridcell [ref=f1e607]
              - gridcell [ref=f1e608]
              - gridcell [ref=f1e609]
              - gridcell [ref=f1e610]
            - row [ref=f1e611]:
              - gridcell [ref=f1e612]:
                - checkbox "Select a row" [ref=f1e615] [cursor=pointer]
              - gridcell " No" [ref=f1e616]:
                - generic [ref=f1e617]: 
                - text: "No"
              - gridcell "33776" [ref=f1e618]
              - gridcell "Pending Pre-Decision" [ref=f1e619]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e620]
              - gridcell "Check" [ref=f1e621]
              - gridcell [ref=f1e622]:
                - link " Pending " [ref=f1e623] [cursor=pointer]:
                  - /url: /exceptions/33776?ReturnUrl=%2fexceptions%2fhistory
                  - generic [ref=f1e624]: 
                  - text: Pending
                  - generic [ref=f1e625]: 
              - gridcell "Exlid123" [ref=f1e626]
              - gridcell "231382306" [ref=f1e627]
              - gridcell "7578091758" [ref=f1e628]
              - gridcell "Account2" [ref=f1e629]
              - gridcell "885285" [ref=f1e630]
              - gridcell "$250.00" [ref=f1e631]
              - gridcell [ref=f1e632]
              - gridcell [ref=f1e633]
              - gridcell [ref=f1e634]
              - gridcell "08/20/2026" [ref=f1e635]
              - gridcell [ref=f1e636]
              - gridcell [ref=f1e637]
              - gridcell [ref=f1e638]
              - 'gridcell "Check # Not Found" [ref=f1e639]'
              - gridcell [ref=f1e640]:
                - link "View " [ref=f1e641] [cursor=pointer]:
                  - /url: /exceptions/33776?ReturnUrl=%2fexceptions%2fhistory
                  - text: View
                  - generic [ref=f1e642]: 
              - gridcell "08/20/2026 4:49 PM EDT" [ref=f1e643]:
                - text: 08/20/2026
                - generic [ref=f1e644]: 4:49 PM EDT
              - gridcell [ref=f1e645]
              - gridcell [ref=f1e646]
              - gridcell [ref=f1e647]
              - gridcell [ref=f1e648]
              - gridcell [ref=f1e649]
            - row [ref=f1e650]:
              - gridcell [ref=f1e651]:
                - checkbox "Select a row" [ref=f1e654] [cursor=pointer]
              - gridcell " No" [ref=f1e655]:
                - generic [ref=f1e656]: 
                - text: "No"
              - gridcell "33774" [ref=f1e657]
              - gridcell "Pending Pre-Decision" [ref=f1e658]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e659]
              - gridcell "Check" [ref=f1e660]
              - gridcell [ref=f1e661]:
                - link " Pending " [ref=f1e662] [cursor=pointer]:
                  - /url: /exceptions/33774?ReturnUrl=%2fexceptions%2fhistory
                  - generic [ref=f1e663]: 
                  - text: Pending
                  - generic [ref=f1e664]: 
              - gridcell "Exlid123" [ref=f1e665]
              - gridcell "231382306" [ref=f1e666]
              - gridcell "7578091758" [ref=f1e667]
              - gridcell "Account2" [ref=f1e668]
              - gridcell "574066732" [ref=f1e669]
              - gridcell "$263.00" [ref=f1e670]
              - gridcell "AutoPresentedPayee" [ref=f1e671]
              - gridcell [ref=f1e672]
              - gridcell [ref=f1e673]
              - gridcell "08/20/2026" [ref=f1e674]
              - gridcell [ref=f1e675]
              - gridcell [ref=f1e676]
              - gridcell [ref=f1e677]
              - 'gridcell "Check # Not Found" [ref=f1e678]'
              - gridcell [ref=f1e679]:
                - link "View " [ref=f1e680] [cursor=pointer]:
                  - /url: /exceptions/33774?ReturnUrl=%2fexceptions%2fhistory
                  - text: View
                  - generic [ref=f1e681]: 
              - gridcell "08/20/2026 4:46 PM EDT" [ref=f1e682]:
                - text: 08/20/2026
                - generic [ref=f1e683]: 4:46 PM EDT
              - gridcell [ref=f1e684]
              - gridcell [ref=f1e685]
              - gridcell [ref=f1e686]
              - gridcell [ref=f1e687]
              - gridcell [ref=f1e688]
            - row [ref=f1e689]:
              - gridcell [ref=f1e690]:
                - checkbox "Select a row" [ref=f1e693] [cursor=pointer]
              - gridcell " No" [ref=f1e694]:
                - generic [ref=f1e695]: 
                - text: "No"
              - gridcell "33767" [ref=f1e696]
              - gridcell "Pending Pre-Decision" [ref=f1e697]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e698]
              - gridcell "Check" [ref=f1e699]
              - gridcell [ref=f1e700]:
                - link " Pending " [ref=f1e701] [cursor=pointer]:
                  - /url: /exceptions/33767?ReturnUrl=%2fexceptions%2fhistory
                  - generic [ref=f1e702]: 
                  - text: Pending
                  - generic [ref=f1e703]: 
              - gridcell "Exlid123" [ref=f1e704]
              - gridcell "231382306" [ref=f1e705]
              - gridcell "7578091758" [ref=f1e706]
              - gridcell "Account2" [ref=f1e707]
              - gridcell "637988679" [ref=f1e708]
              - gridcell "$267.00" [ref=f1e709]
              - gridcell "AutoPresentedPayee" [ref=f1e710]
              - gridcell [ref=f1e711]
              - gridcell [ref=f1e712]
              - gridcell "08/20/2026" [ref=f1e713]
              - gridcell [ref=f1e714]
              - gridcell [ref=f1e715]
              - gridcell [ref=f1e716]
              - 'gridcell "Check # Not Found" [ref=f1e717]'
              - gridcell [ref=f1e718]:
                - link "View " [ref=f1e719] [cursor=pointer]:
                  - /url: /exceptions/33767?ReturnUrl=%2fexceptions%2fhistory
                  - text: View
                  - generic [ref=f1e720]: 
              - gridcell "08/20/2026 4:35 PM EDT" [ref=f1e721]:
                - text: 08/20/2026
                - generic [ref=f1e722]: 4:35 PM EDT
              - gridcell [ref=f1e723]
              - gridcell [ref=f1e724]
              - gridcell [ref=f1e725]
              - gridcell [ref=f1e726]
              - gridcell [ref=f1e727]
            - row [ref=f1e728]:
              - gridcell [ref=f1e729]:
                - checkbox "Select a row" [ref=f1e732] [cursor=pointer]
              - gridcell " No" [ref=f1e733]:
                - generic [ref=f1e734]: 
                - text: "No"
              - gridcell "33766" [ref=f1e735]
              - gridcell "Pending Pre-Decision" [ref=f1e736]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e737]
              - gridcell "Check" [ref=f1e738]
              - gridcell [ref=f1e739]:
                - link " Pending " [ref=f1e740] [cursor=pointer]:
                  - /url: /exceptions/33766?ReturnUrl=%2fexceptions%2fhistory
                  - generic [ref=f1e741]: 
                  - text: Pending
                  - generic [ref=f1e742]: 
              - gridcell "Exlid123" [ref=f1e743]
              - gridcell "231382306" [ref=f1e744]
              - gridcell "7578091758" [ref=f1e745]
              - gridcell "Account2" [ref=f1e746]
              - gridcell "877341095" [ref=f1e747]
              - gridcell "$418.00" [ref=f1e748]
              - gridcell "AutoPresentedPayee" [ref=f1e749]
              - gridcell [ref=f1e750]
              - gridcell [ref=f1e751]
              - gridcell "08/20/2026" [ref=f1e752]
              - gridcell [ref=f1e753]
              - gridcell [ref=f1e754]
              - gridcell [ref=f1e755]
              - 'gridcell "Check # Not Found" [ref=f1e756]'
              - gridcell [ref=f1e757]:
                - link "View " [ref=f1e758] [cursor=pointer]:
                  - /url: /exceptions/33766?ReturnUrl=%2fexceptions%2fhistory
                  - text: View
                  - generic [ref=f1e759]: 
              - gridcell "08/20/2026 4:35 PM EDT" [ref=f1e760]:
                - text: 08/20/2026
                - generic [ref=f1e761]: 4:35 PM EDT
              - gridcell [ref=f1e762]
              - gridcell [ref=f1e763]
              - gridcell [ref=f1e764]
              - gridcell [ref=f1e765]
              - gridcell [ref=f1e766]
            - row [ref=f1e767]:
              - gridcell [ref=f1e768]:
                - checkbox "Select a row" [ref=f1e771] [cursor=pointer]
              - gridcell " No" [ref=f1e772]:
                - generic [ref=f1e773]: 
                - text: "No"
              - gridcell "33764" [ref=f1e774]
              - gridcell "Pending Pre-Decision" [ref=f1e775]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e776]
              - gridcell "Check" [ref=f1e777]
              - gridcell [ref=f1e778]:
                - link " Pending " [ref=f1e779] [cursor=pointer]:
                  - /url: /exceptions/33764?ReturnUrl=%2fexceptions%2fhistory
                  - generic [ref=f1e780]: 
                  - text: Pending
                  - generic [ref=f1e781]: 
              - gridcell "Exlid123" [ref=f1e782]
              - gridcell "231382306" [ref=f1e783]
              - gridcell "7578091758" [ref=f1e784]
              - gridcell "Account2" [ref=f1e785]
              - gridcell "581506" [ref=f1e786]
              - gridcell "$531.00" [ref=f1e787]
              - gridcell [ref=f1e788]
              - gridcell [ref=f1e789]
              - gridcell [ref=f1e790]
              - gridcell "08/20/2026" [ref=f1e791]
              - gridcell [ref=f1e792]
              - gridcell [ref=f1e793]
              - gridcell [ref=f1e794]
              - 'gridcell "Check # Not Found" [ref=f1e795]'
              - gridcell [ref=f1e796]:
                - link "View " [ref=f1e797] [cursor=pointer]:
                  - /url: /exceptions/33764?ReturnUrl=%2fexceptions%2fhistory
                  - text: View
                  - generic [ref=f1e798]: 
              - gridcell "08/20/2026 4:35 PM EDT" [ref=f1e799]:
                - text: 08/20/2026
                - generic [ref=f1e800]: 4:35 PM EDT
              - gridcell [ref=f1e801]
              - gridcell [ref=f1e802]
              - gridcell [ref=f1e803]
              - gridcell [ref=f1e804]
              - gridcell [ref=f1e805]
            - row [ref=f1e806]:
              - gridcell [ref=f1e807]:
                - checkbox "Select a row" [ref=f1e810] [cursor=pointer]
              - gridcell " No" [ref=f1e811]:
                - generic [ref=f1e812]: 
                - text: "No"
              - gridcell "33765" [ref=f1e813]
              - gridcell "Pending Pre-Decision" [ref=f1e814]
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e815]
              - gridcell "Check" [ref=f1e816]
              - gridcell [ref=f1e817]:
                - link " Pending " [ref=f1e818] [cursor=pointer]:
                  - /url: /exceptions/33765?ReturnUrl=%2fexceptions%2fhistory
                  - generic [ref=f1e819]: 
                  - text: Pending
                  - generic [ref=f1e820]: 
              - gridcell "Exlid123" [ref=f1e821]
              - gridcell "231382306" [ref=f1e822]
              - gridcell "7578091758" [ref=f1e823]
              - gridcell "Account2" [ref=f1e824]
              - gridcell "581507" [ref=f1e825]
              - gridcell "$250.00" [ref=f1e826]
              - gridcell [ref=f1e827]
              - gridcell [ref=f1e828]
              - gridcell [ref=f1e829]
              - gridcell "08/20/2026" [ref=f1e830]
              - gridcell [ref=f1e831]
              - gridcell [ref=f1e832]
              - gridcell [ref=f1e833]
              - 'gridcell "Check # Not Found" [ref=f1e834]'
              - gridcell [ref=f1e835]:
                - link "View " [ref=f1e836] [cursor=pointer]:
                  - /url: /exceptions/33765?ReturnUrl=%2fexceptions%2fhistory
                  - text: View
                  - generic [ref=f1e837]: 
              - gridcell "08/20/2026 4:35 PM EDT" [ref=f1e838]:
                - text: 08/20/2026
                - generic [ref=f1e839]: 4:35 PM EDT
              - gridcell [ref=f1e840]
              - gridcell [ref=f1e841]
              - gridcell [ref=f1e842]
              - gridcell [ref=f1e843]
              - gridcell [ref=f1e844]
            - row [ref=f1e845]:
              - gridcell [ref=f1e846]:
                - checkbox "Select a row" [ref=f1e849] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e850]:
                - generic [ref=f1e851]:  
                - text: "Yes"
              - gridcell "33671" [ref=f1e852]
              - gridcell "Completed[Default Decision]" [ref=f1e853]:
                - text: Completed
                - generic [ref=f1e854]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e855]
              - gridcell "Check" [ref=f1e856]
              - gridcell [ref=f1e857]:
                - link " Return" [ref=f1e858] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e859]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e860]
              - gridcell "231382306" [ref=f1e861]
              - gridcell "7578091758" [ref=f1e862]
              - gridcell "Account2" [ref=f1e863]
              - gridcell "791768" [ref=f1e864]
              - gridcell "$250.00" [ref=f1e865]
              - gridcell [ref=f1e866]
              - gridcell [ref=f1e867]
              - gridcell [ref=f1e868]
              - gridcell "08/19/2026" [ref=f1e869]
              - gridcell [ref=f1e870]
              - gridcell [ref=f1e871]
              - gridcell [ref=f1e872]
              - 'gridcell "Check # Not Found" [ref=f1e873]'
              - gridcell [ref=f1e874]:
                - link " View" [ref=f1e875] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e876]: 
                  - text: View
              - gridcell "08/19/2026 9:20 PM EDT" [ref=f1e877]:
                - text: 08/19/2026
                - generic [ref=f1e878]: 9:20 PM EDT
              - gridcell [ref=f1e879]
              - gridcell "[Default Decision]" [ref=f1e880]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e881]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e882]:
                - text: 08/20/2026
                - generic [ref=f1e883]: 3:10 PM EDT
              - gridcell [ref=f1e884]
            - row [ref=f1e885]:
              - gridcell [ref=f1e886]:
                - checkbox "Select a row" [ref=f1e889] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e890]:
                - generic [ref=f1e891]:  
                - text: "Yes"
              - gridcell "33670" [ref=f1e892]
              - gridcell "Completed[Default Decision]" [ref=f1e893]:
                - text: Completed
                - generic [ref=f1e894]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e895]
              - gridcell "Check" [ref=f1e896]
              - gridcell [ref=f1e897]:
                - link " Return" [ref=f1e898] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e899]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e900]
              - gridcell "231382306" [ref=f1e901]
              - gridcell "7578091758" [ref=f1e902]
              - gridcell "Account2" [ref=f1e903]
              - gridcell "791767" [ref=f1e904]
              - gridcell "$531.00" [ref=f1e905]
              - gridcell [ref=f1e906]
              - gridcell [ref=f1e907]
              - gridcell [ref=f1e908]
              - gridcell "08/19/2026" [ref=f1e909]
              - gridcell [ref=f1e910]
              - gridcell [ref=f1e911]
              - gridcell [ref=f1e912]
              - 'gridcell "Check # Not Found" [ref=f1e913]'
              - gridcell [ref=f1e914]:
                - link " View" [ref=f1e915] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e916]: 
                  - text: View
              - gridcell "08/19/2026 9:20 PM EDT" [ref=f1e917]:
                - text: 08/19/2026
                - generic [ref=f1e918]: 9:20 PM EDT
              - gridcell [ref=f1e919]
              - gridcell "[Default Decision]" [ref=f1e920]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e921]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e922]:
                - text: 08/20/2026
                - generic [ref=f1e923]: 3:10 PM EDT
              - gridcell [ref=f1e924]
            - row [ref=f1e925]:
              - gridcell [ref=f1e926]:
                - checkbox "Select a row" [ref=f1e929] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e930]:
                - generic [ref=f1e931]:  
                - text: "Yes"
              - gridcell "33669" [ref=f1e932]
              - gridcell "Completed[Default Decision]" [ref=f1e933]:
                - text: Completed
                - generic [ref=f1e934]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e935]
              - gridcell "Check" [ref=f1e936]
              - gridcell [ref=f1e937]:
                - link " Return" [ref=f1e938] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e939]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e940]
              - gridcell "231382306" [ref=f1e941]
              - gridcell "7578091758" [ref=f1e942]
              - gridcell "Account2" [ref=f1e943]
              - gridcell "166319234" [ref=f1e944]
              - gridcell "$206.00" [ref=f1e945]
              - gridcell "AutoPresentedPayee" [ref=f1e946]
              - gridcell [ref=f1e947]
              - gridcell [ref=f1e948]
              - gridcell "08/19/2026" [ref=f1e949]
              - gridcell [ref=f1e950]
              - gridcell [ref=f1e951]
              - gridcell [ref=f1e952]
              - 'gridcell "Check # Not Found" [ref=f1e953]'
              - gridcell [ref=f1e954]:
                - link " View" [ref=f1e955] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e956]: 
                  - text: View
              - gridcell "08/19/2026 9:17 PM EDT" [ref=f1e957]:
                - text: 08/19/2026
                - generic [ref=f1e958]: 9:17 PM EDT
              - gridcell [ref=f1e959]
              - gridcell "[Default Decision]" [ref=f1e960]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e961]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e962]:
                - text: 08/20/2026
                - generic [ref=f1e963]: 3:10 PM EDT
              - gridcell [ref=f1e964]
            - row [ref=f1e965]:
              - gridcell [ref=f1e966]:
                - checkbox "Select a row" [ref=f1e969] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e970]:
                - generic [ref=f1e971]:  
                - text: "Yes"
              - gridcell "33668" [ref=f1e972]
              - gridcell "Completed[Default Decision]" [ref=f1e973]:
                - text: Completed
                - generic [ref=f1e974]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e975]
              - gridcell "Check" [ref=f1e976]
              - gridcell [ref=f1e977]:
                - link " Return" [ref=f1e978] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e979]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e980]
              - gridcell "231382306" [ref=f1e981]
              - gridcell "7578091758" [ref=f1e982]
              - gridcell "Account2" [ref=f1e983]
              - gridcell "5784" [ref=f1e984]
              - gridcell "$5,784.00" [ref=f1e985]
              - gridcell "TestUser5788" [ref=f1e986]
              - gridcell [ref=f1e987]
              - gridcell [ref=f1e988]
              - gridcell "08/20/2026" [ref=f1e989]
              - gridcell [ref=f1e990]
              - gridcell [ref=f1e991]
              - gridcell [ref=f1e992]
              - 'gridcell "Check # Not Found" [ref=f1e993]'
              - gridcell [ref=f1e994]:
                - link " View" [ref=f1e995] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e996]: 
                  - text: View
              - gridcell "08/19/2026 8:03 PM EDT" [ref=f1e997]:
                - text: 08/19/2026
                - generic [ref=f1e998]: 8:03 PM EDT
              - gridcell [ref=f1e999]
              - gridcell "[Default Decision]" [ref=f1e1000]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e1001]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e1002]:
                - text: 08/20/2026
                - generic [ref=f1e1003]: 3:10 PM EDT
              - gridcell [ref=f1e1004]
            - row [ref=f1e1005]:
              - gridcell [ref=f1e1006]:
                - checkbox "Select a row" [ref=f1e1009] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e1010]:
                - generic [ref=f1e1011]:  
                - text: "Yes"
              - gridcell "33667" [ref=f1e1012]
              - gridcell "Completed[Default Decision]" [ref=f1e1013]:
                - text: Completed
                - generic [ref=f1e1014]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e1015]
              - gridcell "Check" [ref=f1e1016]
              - gridcell [ref=f1e1017]:
                - link " Return" [ref=f1e1018] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1019]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e1020]
              - gridcell "231382306" [ref=f1e1021]
              - gridcell "7578091758" [ref=f1e1022]
              - gridcell "Account2" [ref=f1e1023]
              - gridcell "2151" [ref=f1e1024]
              - gridcell "$238.00" [ref=f1e1025]
              - gridcell "PreCheckUpload" [ref=f1e1026]
              - gridcell [ref=f1e1027]
              - gridcell [ref=f1e1028]
              - gridcell "09/03/2025" [ref=f1e1029]
              - gridcell [ref=f1e1030]
              - gridcell [ref=f1e1031]
              - gridcell [ref=f1e1032]
              - 'gridcell "Check # Not Found" [ref=f1e1033]'
              - gridcell [ref=f1e1034]:
                - link " View" [ref=f1e1035] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1036]: 
                  - text: View
              - gridcell "08/19/2026 8:02 PM EDT" [ref=f1e1037]:
                - text: 08/19/2026
                - generic [ref=f1e1038]: 8:02 PM EDT
              - gridcell [ref=f1e1039]
              - gridcell "[Default Decision]" [ref=f1e1040]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e1041]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e1042]:
                - text: 08/20/2026
                - generic [ref=f1e1043]: 3:10 PM EDT
              - gridcell [ref=f1e1044]
            - row [ref=f1e1045]:
              - gridcell [ref=f1e1046]:
                - checkbox "Select a row" [ref=f1e1049] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e1050]:
                - generic [ref=f1e1051]:  
                - text: "Yes"
              - gridcell "33662" [ref=f1e1052]
              - gridcell "Completed[Default Decision]" [ref=f1e1053]:
                - text: Completed
                - generic [ref=f1e1054]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e1055]
              - gridcell "Check" [ref=f1e1056]
              - gridcell [ref=f1e1057]:
                - link " Return" [ref=f1e1058] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1059]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e1060]
              - gridcell "231382306" [ref=f1e1061]
              - gridcell "7578091758" [ref=f1e1062]
              - gridcell "Account2" [ref=f1e1063]
              - gridcell "654026230" [ref=f1e1064]
              - gridcell "$176.00" [ref=f1e1065]
              - gridcell "AutoPresentedPayee" [ref=f1e1066]
              - gridcell [ref=f1e1067]
              - gridcell [ref=f1e1068]
              - gridcell "08/19/2026" [ref=f1e1069]
              - gridcell [ref=f1e1070]
              - gridcell [ref=f1e1071]
              - gridcell [ref=f1e1072]
              - 'gridcell "Check # Not Found" [ref=f1e1073]'
              - gridcell [ref=f1e1074]:
                - link " View" [ref=f1e1075] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1076]: 
                  - text: View
              - gridcell "08/19/2026 7:42 PM EDT" [ref=f1e1077]:
                - text: 08/19/2026
                - generic [ref=f1e1078]: 7:42 PM EDT
              - gridcell [ref=f1e1079]
              - gridcell "[Default Decision]" [ref=f1e1080]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e1081]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e1082]:
                - text: 08/20/2026
                - generic [ref=f1e1083]: 3:10 PM EDT
              - gridcell [ref=f1e1084]
            - row [ref=f1e1085]:
              - gridcell [ref=f1e1086]:
                - checkbox "Select a row" [ref=f1e1089] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e1090]:
                - generic [ref=f1e1091]:  
                - text: "Yes"
              - gridcell "33661" [ref=f1e1092]
              - gridcell "Completed[Default Decision]" [ref=f1e1093]:
                - text: Completed
                - generic [ref=f1e1094]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e1095]
              - gridcell "Check" [ref=f1e1096]
              - gridcell [ref=f1e1097]:
                - link " Return" [ref=f1e1098] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1099]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e1100]
              - gridcell "231382306" [ref=f1e1101]
              - gridcell "7578091758" [ref=f1e1102]
              - gridcell "Account2" [ref=f1e1103]
              - gridcell "161852" [ref=f1e1104]
              - gridcell "$250.00" [ref=f1e1105]
              - gridcell [ref=f1e1106]
              - gridcell [ref=f1e1107]
              - gridcell [ref=f1e1108]
              - gridcell "08/19/2026" [ref=f1e1109]
              - gridcell [ref=f1e1110]
              - gridcell [ref=f1e1111]
              - gridcell [ref=f1e1112]
              - 'gridcell "Check # Not Found" [ref=f1e1113]'
              - gridcell [ref=f1e1114]:
                - link " View" [ref=f1e1115] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1116]: 
                  - text: View
              - gridcell "08/19/2026 7:42 PM EDT" [ref=f1e1117]:
                - text: 08/19/2026
                - generic [ref=f1e1118]: 7:42 PM EDT
              - gridcell [ref=f1e1119]
              - gridcell "[Default Decision]" [ref=f1e1120]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e1121]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e1122]:
                - text: 08/20/2026
                - generic [ref=f1e1123]: 3:10 PM EDT
              - gridcell [ref=f1e1124]
            - row [ref=f1e1125]:
              - gridcell [ref=f1e1126]:
                - checkbox "Select a row" [ref=f1e1129] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e1130]:
                - generic [ref=f1e1131]:  
                - text: "Yes"
              - gridcell "33660" [ref=f1e1132]
              - gridcell "Completed[Default Decision]" [ref=f1e1133]:
                - text: Completed
                - generic [ref=f1e1134]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e1135]
              - gridcell "Check" [ref=f1e1136]
              - gridcell [ref=f1e1137]:
                - link " Return" [ref=f1e1138] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1139]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e1140]
              - gridcell "231382306" [ref=f1e1141]
              - gridcell "7578091758" [ref=f1e1142]
              - gridcell "Account2" [ref=f1e1143]
              - gridcell "161851" [ref=f1e1144]
              - gridcell "$531.00" [ref=f1e1145]
              - gridcell [ref=f1e1146]
              - gridcell [ref=f1e1147]
              - gridcell [ref=f1e1148]
              - gridcell "08/19/2026" [ref=f1e1149]
              - gridcell [ref=f1e1150]
              - gridcell [ref=f1e1151]
              - gridcell [ref=f1e1152]
              - 'gridcell "Check # Not Found" [ref=f1e1153]'
              - gridcell [ref=f1e1154]:
                - link " View" [ref=f1e1155] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1156]: 
                  - text: View
              - gridcell "08/19/2026 7:42 PM EDT" [ref=f1e1157]:
                - text: 08/19/2026
                - generic [ref=f1e1158]: 7:42 PM EDT
              - gridcell [ref=f1e1159]
              - gridcell "[Default Decision]" [ref=f1e1160]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e1161]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e1162]:
                - text: 08/20/2026
                - generic [ref=f1e1163]: 3:10 PM EDT
              - gridcell [ref=f1e1164]
        - application "Page navigation, page 1 of 8" [ref=f1e1165]:
          - generic [ref=f1e1166]:
            - button "Go to the first page" [disabled]
            - button "Go to the previous page" [disabled]
            - generic [ref=f1e1167]:
              - text: Page
              - spinbutton "Select a page" [ref=f1e1169]: "1"
              - text: of 8
            - button "Go to the next page" [ref=f1e1170] [cursor=pointer]
            - button "Go to the last page" [ref=f1e1174] [cursor=pointer]
          - generic [ref=f1e1178]: 1 - 20 of 157 items
    - contentinfo [ref=f1e1179]:
      - generic [ref=f1e1180]:
        - text: PJ_FI_Bank (Playwright Automation)
        - generic [ref=f1e1181]: "[uat-release]"
      - generic [ref=f1e1182]:
        - text: © Copyright Advanced Fraud Solutions 2005-2026 |
        - generic [ref=f1e1183]: All Rights Reserved
        - text: "|"
        - link "Privacy Policy" [ref=f1e1185] [cursor=pointer]:
          - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  292 | 
  293 | 
  294 |     //Get Locator for Approvals Button in Exceptions Grid View
  295 |     //Method to click on Approvals Button in Exceptions Grid View
  296 |     get buttonApprovals(){
  297 |         return this.page.locator('//a[contains(@class, "btn") and contains(@href, "/approvals")]');
  298 |     }
  299 | 
  300 |     async clickOnApprovalsButton(){
  301 |         await this.buttonApprovals.click();
  302 |     }
  303 | 
  304 |     //Get Locator of Approve Button in Approvals Card View
  305 |     //Method to Click on Approve Button in Approvals Card View Page
  306 |     get cardViewApproveButton(){
  307 |          return this.page.locator('span[class = "d-block  text-success font-weight-bold nowrap mt-1"]');
  308 |     }
  309 | 
  310 |     
  311 |     async clickOnApproveButton(){
  312 |         await this.cardViewApproveButton.click();
  313 |     }
  314 | 
  315 |     // Get locator of exception grid rows.
  316 | 
  317 |     get exceptionGridRows() {
  318 |         return this.page.locator('tr.k-master-row.k-table-row');
  319 |     }
  320 | 
  321 |     //Get Locator of last page arrow button in card view
  322 |     get lastPageArrowButton() {
  323 |         return this.page.locator('button[title="Go to the last page"]');
  324 |     }
  325 | 
  326 |     
  327 |     //get locator for Exception History button
  328 |     //Method to Click on Exception History Button
  329 |     get exceptionHistoryButton(){
  330 |         return this.page.locator('//a[contains(@href,"/exceptions/history") and contains(@class,"btn-subtle-primary")]');
  331 |     }
  332 | 
  333 |     async clickOnExceptionHistoryButton(){
  334 |         const directHistoryButton = this.exceptionHistoryButton.filter({ visible: true }).first();
  335 |         if (await directHistoryButton.count() > 0) {
  336 |             await directHistoryButton.click();
  337 |             return;
  338 |         } 
  339 | 
  340 |         const moreActionsButton = this.page.locator('button.btn.btn-icon.btn-light').filter({ visible: true }).first();
  341 |         if (await moreActionsButton.count() > 0) {
  342 |             await moreActionsButton.click();
  343 |         }
  344 | 
  345 |         await this.page
  346 |             .locator('a[href*="/exceptions/history"]')
  347 |             .filter({ visible: true })
  348 |             .first()
  349 |             .click();
  350 |     }
  351 | 
  352 |     get exceptionHistoryTypeFilterMenuButton() {
  353 |         return this.page.getByRole('button', { name: 'Type column filter menu settings', exact: true });
  354 |     }
  355 | 
  356 |     get exceptionHistoryFilterApplyButton() {
  357 |         return this.page.getByRole('button', { name: 'Filter', exact: true });
  358 |     }
  359 | 
  360 |     get exceptionHistoryFilterClearButton() {
  361 |         return this.page.getByRole('button', { name: 'Clear', exact: true });
  362 |     }
  363 | 
  364 |     get exceptionHistoryGridRows() {
  365 |         return this.page.locator('tr.k-master-row.k-table-row');
  366 |     }
  367 | 
  368 |     async navigateToExceptionHistory() {
  369 |         await this.page.goto('/exceptions/history');
  370 |         await this.page.waitForLoadState('domcontentloaded');
  371 |         await this.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 15000 });
  372 |     }
  373 | 
  374 |     async openExceptionHistoryTypeFilter() {
  375 |         await this.exceptionHistoryTypeFilterMenuButton.waitFor({ state: 'visible', timeout: 15000 });
  376 |         await this.exceptionHistoryTypeFilterMenuButton.click();
  377 |         await this.page.locator('.k-grid-filter-popup[aria-label="Type Filter Menu"]').waitFor({ state: 'visible', timeout: 10000 });
  378 |     }
  379 | 
  380 |     private getExceptionHistoryFilterPopup(columnName: string) {
  381 |         return this.page.locator(`.k-grid-filter-popup[aria-label="${columnName} Filter Menu"]`);
  382 |     }
  383 | 
  384 |     private getTypeFilterPopup() {
  385 |         return this.getExceptionHistoryFilterPopup('Type');
  386 |     }
  387 | 
  388 |     async openExceptionHistoryColumnFilter(columnName: string) {
  389 |         const filterButton = this.page.getByRole('button', { name: `${columnName} column filter menu settings`, exact: true });
  390 |         await filterButton.waitFor({ state: 'visible', timeout: 15000 });
  391 |         await filterButton.click();
> 392 |         await this.getExceptionHistoryFilterPopup(columnName).waitFor({ state: 'visible', timeout: 10000 });
      |                                                               ^ TimeoutError: locator.waitFor: Timeout 10000ms exceeded.
  393 |     }
  394 | 
  395 |     async setExceptionHistoryTypeFilter(typeText: 'Check' | 'ACH' | 'Teller') {
  396 |         await this.openExceptionHistoryTypeFilter();
  397 |         const popup = this.getTypeFilterPopup();
  398 | 
  399 |         const options: Array<'Check' | 'ACH' | 'Teller'> = ['Check', 'ACH', 'Teller'];
  400 |         for (const option of options) {
  401 |             const checkbox = popup.locator(`input#${option}`);
  402 |             if (option === typeText) {
  403 |                 await checkbox.setChecked(true);
  404 |             } else {
  405 |                 await checkbox.setChecked(false);
  406 |             }
  407 |         }
  408 | 
  409 |         await popup.getByRole('button', { name: 'Filter', exact: true }).click();
  410 |         await this.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 15000 });
  411 |     }
  412 | 
  413 |     async applyExceptionHistoryMultiSelectFilter(columnName: string, optionText: string) {
  414 |         await this.openExceptionHistoryColumnFilter(columnName);
  415 |         const popup = this.getExceptionHistoryFilterPopup(columnName);
  416 |         const selectAll = popup.getByLabel('Select All', { exact: true });
  417 | 
  418 |         if (await selectAll.isVisible().catch(() => false)) {
  419 |             await selectAll.setChecked(false);
  420 |         }
  421 | 
  422 |         const checkedOptions = popup.locator('.k-filter-menu-container input[type="checkbox"]:checked');
  423 |         while ((await checkedOptions.count()) > 0) {
  424 |             await checkedOptions.first().setChecked(false);
  425 |         }
  426 | 
  427 |         await popup.getByLabel(optionText, { exact: true }).check();
  428 |         await popup.getByRole('button', { name: 'Filter', exact: true }).click();
  429 |         await this.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 15000 });
  430 |     }
  431 | 
  432 |     async applyExceptionHistoryTextFilter(columnName: string, filterValue: string) {
  433 |         await this.openExceptionHistoryColumnFilter(columnName);
  434 |         const popup = this.getExceptionHistoryFilterPopup(columnName);
  435 |         const filterInput = popup.locator('.k-textbox input.k-input-inner').first();
  436 |         await filterInput.fill(filterValue);
  437 |         await popup.getByRole('button', { name: 'Filter', exact: true }).click();
  438 |         await this.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 15000 });
  439 |     }
  440 | 
  441 |     async clearExceptionHistoryTypeFilter() {
  442 |         await this.openExceptionHistoryTypeFilter();
  443 |         await this.getTypeFilterPopup().getByRole('button', { name: 'Clear', exact: true }).click();
  444 |         await this.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 15000 });
  445 |     }
  446 | 
  447 |     async getExceptionHistoryTypeValues(limit = 10) {
  448 |         const values = await this.getExceptionHistoryColumnValues(6, limit);
  449 | 
  450 |         return values.filter(Boolean);
  451 |     }
  452 | 
  453 |     async getExceptionHistoryColumnValues(colIndex: number, limit = 10) {
  454 |         return this.page
  455 |             .locator(`tr.k-master-row.k-table-row td[data-col-index="${colIndex}"]`)
  456 |             .evaluateAll((nodes, payload) =>
  457 |                 nodes
  458 |                     .slice(0, Number(payload))
  459 |                     .map((node) => node.textContent?.replace(/\n/g, '').trim() || ''),
  460 |                 limit,
  461 |             );
  462 |     }
  463 | 
  464 |     async getExceptionHistoryRowCount() {
  465 |         return this.exceptionHistoryGridRows.count();
  466 |     }
  467 | 
  468 |     async getExceptionHistoryTypeFilterOptions() {
  469 |         await this.openExceptionHistoryTypeFilter();
  470 |         const options = await this.getTypeFilterPopup().locator('.k-filter-menu-container label').allTextContents();
  471 |         return options.map((option) => option.trim()).filter(Boolean);
  472 |     }
  473 | 
  474 |     async isExceptionHistoryTypeFilterOptionChecked(typeText: 'Check' | 'ACH' | 'Teller') {
  475 |         await this.openExceptionHistoryTypeFilter();
  476 |         return this.getTypeFilterPopup().locator(`.k-filter-menu-container input#${typeText}`).isChecked();
  477 |     }
  478 | 
  479 |     //get locator for Approval History button
  480 |     //Method to Click on Approval History Button
  481 |     get approvalHistoryButton(){
  482 |         //return this.page.locator('//a[contains(@href,"/approvals/history") and contains(@class,"btn-subtle-primary")]');
  483 |         return this.page.locator('(//a[@class="btn btn-subtle-primary"])[2]');
  484 |     }
  485 | 
  486 |     async clickOnApprovalHistoryButton(){
  487 |         await this.approvalHistoryButton.click();
  488 |     }
  489 | 
  490 |     //Get Locator to capture ExceptionId from Card View
  491 | 
  492 |     get exceptionIdFromCardView() {
```