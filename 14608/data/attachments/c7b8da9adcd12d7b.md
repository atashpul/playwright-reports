# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\8-ExceptionsSmoke.spec.ts >> Exceptions — Smoke (Continued) >> Decision badge on an already-reviewed row is blocked with a system message
- Location: specs\Smoke\8-ExceptionsSmoke.spec.ts:341:5

# Error details

```
Error: locator.scrollIntoViewIfNeeded: Element is not attached to the DOM
Call log:
  - attempting scroll into view action
    - waiting for element to be stable

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
    - generic [ref=f1e52]:
      - list [ref=f1e55]:
        - listitem [ref=f1e56]:
          - link " " [ref=f1e57] [cursor=pointer]:
            - /url: /
        - listitem [ref=f1e59]:
          - link "Exceptions" [ref=f1e60] [cursor=pointer]:
            - /url: /exceptions
        - listitem [ref=f1e61]:
          - link "History" [ref=f1e62]:
            - /url: javascript:;
      - generic [ref=f1e64]:
        - toolbar "Grid toolbar" [ref=f1e65]:
          - generic [ref=f1e66]:
            - generic [ref=f1e67]:
              - generic [ref=f1e68]:
                - generic [ref=f1e69]: Page Size
                - combobox [ref=f1e71]:
                  - option "10"
                  - option "20" [selected]
                  - option "50"
                  - option "100"
              - button "Excel" [ref=f1e72] [cursor=pointer]
              - textbox "Search..." [ref=f1e79]
            - button " Mark as Reviewed [0]" [ref=f1e81] [cursor=pointer]:
              - generic [ref=f1e82]: 
              - text: Mark as Reviewed [0]
            - generic [ref=f1e84]:
              - generic [ref=f1e85]: Saved Filters
              - combobox [ref=f1e87]:
                - option "[No Filter]" [selected]
                - option "Active"
                - option "Reviewed"
              - button "+" [ref=f1e89] [cursor=pointer]
        - grid "Data table" [ref=f1e91]:
          - rowgroup [ref=f1e121]:
            - row [ref=f1e122]:
              - columnheader [ref=f1e123]:
                - checkbox "Select all rows" [ref=f1e125] [cursor=pointer]
              - columnheader "Reviewed? Reviewed? column filter menu settings" [ref=f1e126]:
                - generic [ref=f1e127]:
                  - generic [ref=f1e128] [cursor=pointer]: Reviewed?
                  - button "Reviewed? column filter menu settings" [ref=f1e130]
              - columnheader "ID ID column filter menu settings" [ref=f1e135]:
                - generic [ref=f1e136]:
                  - generic [ref=f1e137] [cursor=pointer]: ID
                  - button "ID column filter menu settings" [ref=f1e139]
              - columnheader "Status Status column filter menu settings" [ref=f1e144]:
                - generic [ref=f1e145]:
                  - generic [ref=f1e146] [cursor=pointer]: Status
                  - button "Status column filter menu settings" [ref=f1e148]
              - columnheader "Business Client Business Client column filter menu settings" [ref=f1e153]:
                - generic [ref=f1e154]:
                  - generic [ref=f1e155] [cursor=pointer]: Business Client
                  - button "Business Client column filter menu settings" [ref=f1e157]
              - columnheader "Type Type column filter menu settings" [ref=f1e162]:
                - generic [ref=f1e163]:
                  - generic [ref=f1e164] [cursor=pointer]: Type
                  - button "Type column filter menu settings" [ref=f1e166]
              - columnheader "Decision Decision column filter menu settings" [ref=f1e171]:
                - generic [ref=f1e172]:
                  - generic [ref=f1e173] [cursor=pointer]: Decision
                  - button "Decision column filter menu settings" [ref=f1e175]
              - columnheader "Reference ID Reference ID column filter menu settings" [ref=f1e180]:
                - generic [ref=f1e181]:
                  - generic [ref=f1e182] [cursor=pointer]: Reference ID
                  - button "Reference ID column filter menu settings" [ref=f1e184]
              - 'columnheader "Routing # Routing # column filter menu settings" [ref=f1e189]':
                - generic [ref=f1e190]:
                  - generic [ref=f1e191] [cursor=pointer]: "Routing #"
                  - 'button "Routing # column filter menu settings" [ref=f1e193]'
              - 'columnheader "Account # Account # column filter menu settings" [ref=f1e198]':
                - generic [ref=f1e199]:
                  - generic [ref=f1e200] [cursor=pointer]: "Account #"
                  - 'button "Account # column filter menu settings" [ref=f1e202]'
              - columnheader "Account Name Account Name column filter menu settings" [ref=f1e207]:
                - generic [ref=f1e208]:
                  - generic [ref=f1e209] [cursor=pointer]: Account Name
                  - button "Account Name column filter menu settings" [ref=f1e211]
              - 'columnheader "Check #/SEC Code Check #/SEC Code column filter menu settings" [ref=f1e216]':
                - generic [ref=f1e217]:
                  - generic [ref=f1e218] [cursor=pointer]: "Check #/SEC Code"
                  - 'button "Check #/SEC Code column filter menu settings" [ref=f1e220]'
              - columnheader "Amount Amount column filter menu settings" [ref=f1e225]:
                - generic [ref=f1e226]:
                  - generic [ref=f1e227] [cursor=pointer]: Amount
                  - button "Amount column filter menu settings" [ref=f1e229]
              - columnheader "Payee/Originator Payee/Originator column filter menu settings" [ref=f1e234]:
                - generic [ref=f1e235]:
                  - generic [ref=f1e236] [cursor=pointer]: Payee/Originator
                  - button "Payee/Originator column filter menu settings" [ref=f1e238]
              - columnheader "Trans Code Trans Code column filter menu settings" [ref=f1e243]:
                - generic [ref=f1e244]:
                  - generic [ref=f1e245] [cursor=pointer]: Trans Code
                  - button "Trans Code column filter menu settings" [ref=f1e247]
              - columnheader "Trans Type Trans Type column filter menu settings" [ref=f1e252]:
                - generic [ref=f1e253]:
                  - generic [ref=f1e254] [cursor=pointer]: Trans Type
                  - button "Trans Type column filter menu settings" [ref=f1e256]
              - columnheader "Trans Date  Trans Date column filter menu settings" [ref=f1e261]:
                - generic [ref=f1e262]:
                  - generic [ref=f1e264] [cursor=pointer]:
                    - text: Trans Date
                    - generic "Check Presented Date or ACH Entry Date or the date when ACH transaction was presented" [ref=f1e265]: 
                  - button "Trans Date column filter menu settings" [ref=f1e266]
              - columnheader "Settlement Date Settlement Date column filter menu settings" [ref=f1e271]:
                - generic [ref=f1e272]:
                  - generic [ref=f1e273] [cursor=pointer]: Settlement Date
                  - button "Settlement Date column filter menu settings" [ref=f1e275]
              - columnheader "Issued Check Data" [ref=f1e280]
              - columnheader "Check Image" [ref=f1e282]
              - columnheader "Exception Reason Exception Reason column filter menu settings" [ref=f1e284]:
                - generic [ref=f1e285]:
                  - generic [ref=f1e286] [cursor=pointer]: Exception Reason
                  - button "Exception Reason column filter menu settings" [ref=f1e288]
              - columnheader "Exception" [ref=f1e293]
              - columnheader [ref=f1e295]:
                - text: Exception Date
                - button "Exception Date column filter menu settings" [ref=f1e296]
              - columnheader "Approval" [ref=f1e301]
              - columnheader "Decision By Decision By column filter menu settings" [ref=f1e303]:
                - generic [ref=f1e304]:
                  - generic [ref=f1e305] [cursor=pointer]: Decision By
                  - button "Decision By column filter menu settings" [ref=f1e307]
              - columnheader "Decision Notes Decision Notes column filter menu settings" [ref=f1e312]:
                - generic [ref=f1e313]:
                  - generic [ref=f1e314] [cursor=pointer]: Decision Notes
                  - button "Decision Notes column filter menu settings" [ref=f1e316]
              - columnheader [ref=f1e321]:
                - text: Decision Date
                - button "Decision Date column filter menu settings" [ref=f1e322]
              - columnheader "Return Reason Return Reason column filter menu settings" [ref=f1e327]:
                - generic [ref=f1e328]:
                  - generic [ref=f1e329] [cursor=pointer]: Return Reason
                  - button "Return Reason column filter menu settings" [ref=f1e331]
          - rowgroup [ref=f1e369]:
            - row [ref=f1e370]:
              - gridcell [ref=f1e371]:
                - checkbox "Select a row" [ref=f1e374] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e375]:
                - generic [ref=f1e376]:  
                - text: "Yes"
              - gridcell "33777" [ref=f1e377]
              - gridcell "Completed[Default Decision]" [ref=f1e378]:
                - text: Completed
                - generic [ref=f1e379]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e380]
              - gridcell "Check" [ref=f1e381]
              - gridcell [ref=f1e382]:
                - link " Return" [ref=f1e383] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e384]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e385]
              - gridcell "231382306" [ref=f1e386]
              - gridcell "7578091758" [ref=f1e387]
              - gridcell "Account2" [ref=f1e388]
              - gridcell "420254117" [ref=f1e389]
              - gridcell "$815.00" [ref=f1e390]
              - gridcell "AutoPresentedPayee" [ref=f1e391]
              - gridcell [ref=f1e392]
              - gridcell [ref=f1e393]
              - gridcell "08/20/2026" [ref=f1e394]
              - gridcell [ref=f1e395]
              - gridcell [ref=f1e396]
              - gridcell [ref=f1e397]
              - 'gridcell "Check # Not Found" [ref=f1e398]'
              - gridcell [ref=f1e399]:
                - link " View" [ref=f1e400] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e401]: 
                  - text: View
              - gridcell "08/20/2026 5:05 PM EDT" [ref=f1e402]:
                - text: 08/20/2026
                - generic [ref=f1e403]: 5:05 PM EDT
              - gridcell [ref=f1e404]
              - gridcell "[Default Decision]" [ref=f1e405]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e406]
              - gridcell "08/21/2026 3:00 PM EDT" [ref=f1e407]:
                - text: 08/21/2026
                - generic [ref=f1e408]: 3:00 PM EDT
              - gridcell [ref=f1e409]
            - row [ref=f1e410]:
              - gridcell [ref=f1e411]:
                - checkbox "Select a row" [ref=f1e414] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e415]:
                - generic [ref=f1e416]:  
                - text: "Yes"
              - gridcell "33776" [ref=f1e417]
              - gridcell "Completed[Default Decision]" [ref=f1e418]:
                - text: Completed
                - generic [ref=f1e419]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e420]
              - gridcell "Check" [ref=f1e421]
              - gridcell [ref=f1e422]:
                - link " Return" [ref=f1e423] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e424]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e425]
              - gridcell "231382306" [ref=f1e426]
              - gridcell "7578091758" [ref=f1e427]
              - gridcell "Account2" [ref=f1e428]
              - gridcell "885285" [ref=f1e429]
              - gridcell "$250.00" [ref=f1e430]
              - gridcell [ref=f1e431]
              - gridcell [ref=f1e432]
              - gridcell [ref=f1e433]
              - gridcell "08/20/2026" [ref=f1e434]
              - gridcell [ref=f1e435]
              - gridcell [ref=f1e436]
              - gridcell [ref=f1e437]
              - 'gridcell "Check # Not Found" [ref=f1e438]'
              - gridcell [ref=f1e439]:
                - link " View" [ref=f1e440] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e441]: 
                  - text: View
              - gridcell "08/20/2026 4:49 PM EDT" [ref=f1e442]:
                - text: 08/20/2026
                - generic [ref=f1e443]: 4:49 PM EDT
              - gridcell [ref=f1e444]
              - gridcell "[Default Decision]" [ref=f1e445]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e446]
              - gridcell "08/21/2026 3:00 PM EDT" [ref=f1e447]:
                - text: 08/21/2026
                - generic [ref=f1e448]: 3:00 PM EDT
              - gridcell [ref=f1e449]
            - row [ref=f1e450]:
              - gridcell [ref=f1e451]:
                - checkbox "Select a row" [ref=f1e454] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e455]:
                - generic [ref=f1e456]:  
                - text: "Yes"
              - gridcell "33775" [ref=f1e457]
              - gridcell "Completed[Default Decision]" [ref=f1e458]:
                - text: Completed
                - generic [ref=f1e459]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e460]
              - gridcell "Check" [ref=f1e461]
              - gridcell [ref=f1e462]:
                - link " Return" [ref=f1e463] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e464]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e465]
              - gridcell "231382306" [ref=f1e466]
              - gridcell "7578091758" [ref=f1e467]
              - gridcell "Account2" [ref=f1e468]
              - gridcell "885284" [ref=f1e469]
              - gridcell "$531.00" [ref=f1e470]
              - gridcell [ref=f1e471]
              - gridcell [ref=f1e472]
              - gridcell [ref=f1e473]
              - gridcell "08/20/2026" [ref=f1e474]
              - gridcell [ref=f1e475]
              - gridcell [ref=f1e476]
              - gridcell [ref=f1e477]
              - 'gridcell "Check # Not Found" [ref=f1e478]'
              - gridcell [ref=f1e479]:
                - link " View" [ref=f1e480] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e481]: 
                  - text: View
              - gridcell "08/20/2026 4:49 PM EDT" [ref=f1e482]:
                - text: 08/20/2026
                - generic [ref=f1e483]: 4:49 PM EDT
              - gridcell [ref=f1e484]
              - gridcell "[Default Decision]" [ref=f1e485]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e486]
              - gridcell "08/21/2026 3:00 PM EDT" [ref=f1e487]:
                - text: 08/21/2026
                - generic [ref=f1e488]: 3:00 PM EDT
              - gridcell [ref=f1e489]
            - row [ref=f1e490]:
              - gridcell [ref=f1e491]:
                - checkbox "Select a row" [ref=f1e494] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e495]:
                - generic [ref=f1e496]:  
                - text: "Yes"
              - gridcell "33774" [ref=f1e497]
              - gridcell "Completed[Default Decision]" [ref=f1e498]:
                - text: Completed
                - generic [ref=f1e499]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e500]
              - gridcell "Check" [ref=f1e501]
              - gridcell [ref=f1e502]:
                - link " Return" [ref=f1e503] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e504]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e505]
              - gridcell "231382306" [ref=f1e506]
              - gridcell "7578091758" [ref=f1e507]
              - gridcell "Account2" [ref=f1e508]
              - gridcell "574066732" [ref=f1e509]
              - gridcell "$263.00" [ref=f1e510]
              - gridcell "AutoPresentedPayee" [ref=f1e511]
              - gridcell [ref=f1e512]
              - gridcell [ref=f1e513]
              - gridcell "08/20/2026" [ref=f1e514]
              - gridcell [ref=f1e515]
              - gridcell [ref=f1e516]
              - gridcell [ref=f1e517]
              - 'gridcell "Check # Not Found" [ref=f1e518]'
              - gridcell [ref=f1e519]:
                - link " View" [ref=f1e520] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e521]: 
                  - text: View
              - gridcell "08/20/2026 4:46 PM EDT" [ref=f1e522]:
                - text: 08/20/2026
                - generic [ref=f1e523]: 4:46 PM EDT
              - gridcell [ref=f1e524]
              - gridcell "[Default Decision]" [ref=f1e525]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e526]
              - gridcell "08/21/2026 3:00 PM EDT" [ref=f1e527]:
                - text: 08/21/2026
                - generic [ref=f1e528]: 3:00 PM EDT
              - gridcell [ref=f1e529]
            - row [ref=f1e530]:
              - gridcell [ref=f1e531]:
                - checkbox "Select a row" [ref=f1e534] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e535]:
                - generic [ref=f1e536]:  
                - text: "Yes"
              - gridcell "33767" [ref=f1e537]
              - gridcell "Completed[Default Decision]" [ref=f1e538]:
                - text: Completed
                - generic [ref=f1e539]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e540]
              - gridcell "Check" [ref=f1e541]
              - gridcell [ref=f1e542]:
                - link " Return" [ref=f1e543] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e544]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e545]
              - gridcell "231382306" [ref=f1e546]
              - gridcell "7578091758" [ref=f1e547]
              - gridcell "Account2" [ref=f1e548]
              - gridcell "637988679" [ref=f1e549]
              - gridcell "$267.00" [ref=f1e550]
              - gridcell "AutoPresentedPayee" [ref=f1e551]
              - gridcell [ref=f1e552]
              - gridcell [ref=f1e553]
              - gridcell "08/20/2026" [ref=f1e554]
              - gridcell [ref=f1e555]
              - gridcell [ref=f1e556]
              - gridcell [ref=f1e557]
              - 'gridcell "Check # Not Found" [ref=f1e558]'
              - gridcell [ref=f1e559]:
                - link " View" [ref=f1e560] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e561]: 
                  - text: View
              - gridcell "08/20/2026 4:35 PM EDT" [ref=f1e562]:
                - text: 08/20/2026
                - generic [ref=f1e563]: 4:35 PM EDT
              - gridcell [ref=f1e564]
              - gridcell "[Default Decision]" [ref=f1e565]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e566]
              - gridcell "08/21/2026 3:00 PM EDT" [ref=f1e567]:
                - text: 08/21/2026
                - generic [ref=f1e568]: 3:00 PM EDT
              - gridcell [ref=f1e569]
            - row [ref=f1e570]:
              - gridcell [ref=f1e571]:
                - checkbox "Select a row" [ref=f1e574] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e575]:
                - generic [ref=f1e576]:  
                - text: "Yes"
              - gridcell "33766" [ref=f1e577]
              - gridcell "Completed[Default Decision]" [ref=f1e578]:
                - text: Completed
                - generic [ref=f1e579]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e580]
              - gridcell "Check" [ref=f1e581]
              - gridcell [ref=f1e582]:
                - link " Return" [ref=f1e583] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e584]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e585]
              - gridcell "231382306" [ref=f1e586]
              - gridcell "7578091758" [ref=f1e587]
              - gridcell "Account2" [ref=f1e588]
              - gridcell "877341095" [ref=f1e589]
              - gridcell "$418.00" [ref=f1e590]
              - gridcell "AutoPresentedPayee" [ref=f1e591]
              - gridcell [ref=f1e592]
              - gridcell [ref=f1e593]
              - gridcell "08/20/2026" [ref=f1e594]
              - gridcell [ref=f1e595]
              - gridcell [ref=f1e596]
              - gridcell [ref=f1e597]
              - 'gridcell "Check # Not Found" [ref=f1e598]'
              - gridcell [ref=f1e599]:
                - link " View" [ref=f1e600] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e601]: 
                  - text: View
              - gridcell "08/20/2026 4:35 PM EDT" [ref=f1e602]:
                - text: 08/20/2026
                - generic [ref=f1e603]: 4:35 PM EDT
              - gridcell [ref=f1e604]
              - gridcell "[Default Decision]" [ref=f1e605]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e606]
              - gridcell "08/21/2026 3:00 PM EDT" [ref=f1e607]:
                - text: 08/21/2026
                - generic [ref=f1e608]: 3:00 PM EDT
              - gridcell [ref=f1e609]
            - row [ref=f1e610]:
              - gridcell [ref=f1e611]:
                - checkbox "Select a row" [ref=f1e614] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e615]:
                - generic [ref=f1e616]:  
                - text: "Yes"
              - gridcell "33765" [ref=f1e617]
              - gridcell "Completed[Default Decision]" [ref=f1e618]:
                - text: Completed
                - generic [ref=f1e619]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e620]
              - gridcell "Check" [ref=f1e621]
              - gridcell [ref=f1e622]:
                - link " Return" [ref=f1e623] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e624]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e625]
              - gridcell "231382306" [ref=f1e626]
              - gridcell "7578091758" [ref=f1e627]
              - gridcell "Account2" [ref=f1e628]
              - gridcell "581507" [ref=f1e629]
              - gridcell "$250.00" [ref=f1e630]
              - gridcell [ref=f1e631]
              - gridcell [ref=f1e632]
              - gridcell [ref=f1e633]
              - gridcell "08/20/2026" [ref=f1e634]
              - gridcell [ref=f1e635]
              - gridcell [ref=f1e636]
              - gridcell [ref=f1e637]
              - 'gridcell "Check # Not Found" [ref=f1e638]'
              - gridcell [ref=f1e639]:
                - link " View" [ref=f1e640] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e641]: 
                  - text: View
              - gridcell "08/20/2026 4:35 PM EDT" [ref=f1e642]:
                - text: 08/20/2026
                - generic [ref=f1e643]: 4:35 PM EDT
              - gridcell [ref=f1e644]
              - gridcell "[Default Decision]" [ref=f1e645]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e646]
              - gridcell "08/21/2026 3:00 PM EDT" [ref=f1e647]:
                - text: 08/21/2026
                - generic [ref=f1e648]: 3:00 PM EDT
              - gridcell [ref=f1e649]
            - row [ref=f1e650]:
              - gridcell [ref=f1e651]:
                - checkbox "Select a row" [ref=f1e654] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e655]:
                - generic [ref=f1e656]:  
                - text: "Yes"
              - gridcell "33764" [ref=f1e657]
              - gridcell "Completed[Default Decision]" [ref=f1e658]:
                - text: Completed
                - generic [ref=f1e659]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e660]
              - gridcell "Check" [ref=f1e661]
              - gridcell [ref=f1e662]:
                - link " Return" [ref=f1e663] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e664]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e665]
              - gridcell "231382306" [ref=f1e666]
              - gridcell "7578091758" [ref=f1e667]
              - gridcell "Account2" [ref=f1e668]
              - gridcell "581506" [ref=f1e669]
              - gridcell "$531.00" [ref=f1e670]
              - gridcell [ref=f1e671]
              - gridcell [ref=f1e672]
              - gridcell [ref=f1e673]
              - gridcell "08/20/2026" [ref=f1e674]
              - gridcell [ref=f1e675]
              - gridcell [ref=f1e676]
              - gridcell [ref=f1e677]
              - 'gridcell "Check # Not Found" [ref=f1e678]'
              - gridcell [ref=f1e679]:
                - link " View" [ref=f1e680] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e681]: 
                  - text: View
              - gridcell "08/20/2026 4:35 PM EDT" [ref=f1e682]:
                - text: 08/20/2026
                - generic [ref=f1e683]: 4:35 PM EDT
              - gridcell [ref=f1e684]
              - gridcell "[Default Decision]" [ref=f1e685]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e686]
              - gridcell "08/21/2026 3:00 PM EDT" [ref=f1e687]:
                - text: 08/21/2026
                - generic [ref=f1e688]: 3:00 PM EDT
              - gridcell [ref=f1e689]
            - row [ref=f1e690]:
              - gridcell [ref=f1e691]:
                - checkbox "Select a row" [ref=f1e694] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e695]:
                - generic [ref=f1e696]:  
                - text: "Yes"
              - gridcell "33671" [ref=f1e697]
              - gridcell "Completed[Default Decision]" [ref=f1e698]:
                - text: Completed
                - generic [ref=f1e699]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e700]
              - gridcell "Check" [ref=f1e701]
              - gridcell [ref=f1e702]:
                - link " Return" [ref=f1e703] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e704]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e705]
              - gridcell "231382306" [ref=f1e706]
              - gridcell "7578091758" [ref=f1e707]
              - gridcell "Account2" [ref=f1e708]
              - gridcell "791768" [ref=f1e709]
              - gridcell "$250.00" [ref=f1e710]
              - gridcell [ref=f1e711]
              - gridcell [ref=f1e712]
              - gridcell [ref=f1e713]
              - gridcell "08/19/2026" [ref=f1e714]
              - gridcell [ref=f1e715]
              - gridcell [ref=f1e716]
              - gridcell [ref=f1e717]
              - 'gridcell "Check # Not Found" [ref=f1e718]'
              - gridcell [ref=f1e719]:
                - link " View" [ref=f1e720] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e721]: 
                  - text: View
              - gridcell "08/19/2026 9:20 PM EDT" [ref=f1e722]:
                - text: 08/19/2026
                - generic [ref=f1e723]: 9:20 PM EDT
              - gridcell [ref=f1e724]
              - gridcell "[Default Decision]" [ref=f1e725]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e726]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e727]:
                - text: 08/20/2026
                - generic [ref=f1e728]: 3:10 PM EDT
              - gridcell [ref=f1e729]
            - row [ref=f1e730]:
              - gridcell [ref=f1e731]:
                - checkbox "Select a row" [ref=f1e734] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e735]:
                - generic [ref=f1e736]:  
                - text: "Yes"
              - gridcell "33670" [ref=f1e737]
              - gridcell "Completed[Default Decision]" [ref=f1e738]:
                - text: Completed
                - generic [ref=f1e739]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e740]
              - gridcell "Check" [ref=f1e741]
              - gridcell [ref=f1e742]:
                - link " Return" [ref=f1e743] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e744]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e745]
              - gridcell "231382306" [ref=f1e746]
              - gridcell "7578091758" [ref=f1e747]
              - gridcell "Account2" [ref=f1e748]
              - gridcell "791767" [ref=f1e749]
              - gridcell "$531.00" [ref=f1e750]
              - gridcell [ref=f1e751]
              - gridcell [ref=f1e752]
              - gridcell [ref=f1e753]
              - gridcell "08/19/2026" [ref=f1e754]
              - gridcell [ref=f1e755]
              - gridcell [ref=f1e756]
              - gridcell [ref=f1e757]
              - 'gridcell "Check # Not Found" [ref=f1e758]'
              - gridcell [ref=f1e759]:
                - link " View" [ref=f1e760] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e761]: 
                  - text: View
              - gridcell "08/19/2026 9:20 PM EDT" [ref=f1e762]:
                - text: 08/19/2026
                - generic [ref=f1e763]: 9:20 PM EDT
              - gridcell [ref=f1e764]
              - gridcell "[Default Decision]" [ref=f1e765]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e766]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e767]:
                - text: 08/20/2026
                - generic [ref=f1e768]: 3:10 PM EDT
              - gridcell [ref=f1e769]
            - row [ref=f1e770]:
              - gridcell [ref=f1e771]:
                - checkbox "Select a row" [ref=f1e774] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e775]:
                - generic [ref=f1e776]:  
                - text: "Yes"
              - gridcell "33669" [ref=f1e777]
              - gridcell "Completed[Default Decision]" [ref=f1e778]:
                - text: Completed
                - generic [ref=f1e779]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e780]
              - gridcell "Check" [ref=f1e781]
              - gridcell [ref=f1e782]:
                - link " Return" [ref=f1e783] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e784]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e785]
              - gridcell "231382306" [ref=f1e786]
              - gridcell "7578091758" [ref=f1e787]
              - gridcell "Account2" [ref=f1e788]
              - gridcell "166319234" [ref=f1e789]
              - gridcell "$206.00" [ref=f1e790]
              - gridcell "AutoPresentedPayee" [ref=f1e791]
              - gridcell [ref=f1e792]
              - gridcell [ref=f1e793]
              - gridcell "08/19/2026" [ref=f1e794]
              - gridcell [ref=f1e795]
              - gridcell [ref=f1e796]
              - gridcell [ref=f1e797]
              - 'gridcell "Check # Not Found" [ref=f1e798]'
              - gridcell [ref=f1e799]:
                - link " View" [ref=f1e800] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e801]: 
                  - text: View
              - gridcell "08/19/2026 9:17 PM EDT" [ref=f1e802]:
                - text: 08/19/2026
                - generic [ref=f1e803]: 9:17 PM EDT
              - gridcell [ref=f1e804]
              - gridcell "[Default Decision]" [ref=f1e805]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e806]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e807]:
                - text: 08/20/2026
                - generic [ref=f1e808]: 3:10 PM EDT
              - gridcell [ref=f1e809]
            - row [ref=f1e810]:
              - gridcell [ref=f1e811]:
                - checkbox "Select a row" [ref=f1e814] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e815]:
                - generic [ref=f1e816]:  
                - text: "Yes"
              - gridcell "33668" [ref=f1e817]
              - gridcell "Completed[Default Decision]" [ref=f1e818]:
                - text: Completed
                - generic [ref=f1e819]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e820]
              - gridcell "Check" [ref=f1e821]
              - gridcell [ref=f1e822]:
                - link " Return" [ref=f1e823] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e824]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e825]
              - gridcell "231382306" [ref=f1e826]
              - gridcell "7578091758" [ref=f1e827]
              - gridcell "Account2" [ref=f1e828]
              - gridcell "5784" [ref=f1e829]
              - gridcell "$5,784.00" [ref=f1e830]
              - gridcell "TestUser5788" [ref=f1e831]
              - gridcell [ref=f1e832]
              - gridcell [ref=f1e833]
              - gridcell "08/20/2026" [ref=f1e834]
              - gridcell [ref=f1e835]
              - gridcell [ref=f1e836]
              - gridcell [ref=f1e837]
              - 'gridcell "Check # Not Found" [ref=f1e838]'
              - gridcell [ref=f1e839]:
                - link " View" [ref=f1e840] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e841]: 
                  - text: View
              - gridcell "08/19/2026 8:03 PM EDT" [ref=f1e842]:
                - text: 08/19/2026
                - generic [ref=f1e843]: 8:03 PM EDT
              - gridcell [ref=f1e844]
              - gridcell "[Default Decision]" [ref=f1e845]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e846]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e847]:
                - text: 08/20/2026
                - generic [ref=f1e848]: 3:10 PM EDT
              - gridcell [ref=f1e849]
            - row [ref=f1e850]:
              - gridcell [ref=f1e851]:
                - checkbox "Select a row" [ref=f1e854] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e855]:
                - generic [ref=f1e856]:  
                - text: "Yes"
              - gridcell "33667" [ref=f1e857]
              - gridcell "Completed[Default Decision]" [ref=f1e858]:
                - text: Completed
                - generic [ref=f1e859]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e860]
              - gridcell "Check" [ref=f1e861]
              - gridcell [ref=f1e862]:
                - link " Return" [ref=f1e863] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e864]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e865]
              - gridcell "231382306" [ref=f1e866]
              - gridcell "7578091758" [ref=f1e867]
              - gridcell "Account2" [ref=f1e868]
              - gridcell "2151" [ref=f1e869]
              - gridcell "$238.00" [ref=f1e870]
              - gridcell "PreCheckUpload" [ref=f1e871]
              - gridcell [ref=f1e872]
              - gridcell [ref=f1e873]
              - gridcell "09/03/2025" [ref=f1e874]
              - gridcell [ref=f1e875]
              - gridcell [ref=f1e876]
              - gridcell [ref=f1e877]
              - 'gridcell "Check # Not Found" [ref=f1e878]'
              - gridcell [ref=f1e879]:
                - link " View" [ref=f1e880] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e881]: 
                  - text: View
              - gridcell "08/19/2026 8:02 PM EDT" [ref=f1e882]:
                - text: 08/19/2026
                - generic [ref=f1e883]: 8:02 PM EDT
              - gridcell [ref=f1e884]
              - gridcell "[Default Decision]" [ref=f1e885]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e886]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e887]:
                - text: 08/20/2026
                - generic [ref=f1e888]: 3:10 PM EDT
              - gridcell [ref=f1e889]
            - row [ref=f1e890]:
              - gridcell [ref=f1e891]:
                - checkbox "Select a row" [ref=f1e894] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e895]:
                - generic [ref=f1e896]:  
                - text: "Yes"
              - gridcell "33663" [ref=f1e897]
              - gridcell "Completed[Default Decision]" [ref=f1e898]:
                - text: Completed
                - generic [ref=f1e899]: "[Default Decision]"
              - gridcell [ref=f1e900]
              - gridcell "Check" [ref=f1e901]
              - gridcell [ref=f1e902]:
                - link " Return" [ref=f1e903] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e904]: 
                  - text: Return
              - gridcell [ref=f1e905]
              - gridcell "122199983" [ref=f1e906]
              - gridcell "123456" [ref=f1e907]
              - gridcell [ref=f1e908]
              - gridcell "4225" [ref=f1e909]
              - gridcell "$4,225.00" [ref=f1e910]
              - gridcell "TestUser6695" [ref=f1e911]
              - gridcell [ref=f1e912]
              - gridcell [ref=f1e913]
              - gridcell "08/19/2026" [ref=f1e914]
              - gridcell [ref=f1e915]
              - gridcell [ref=f1e916]
              - gridcell [ref=f1e917]
              - 'gridcell "Check # Not Found" [ref=f1e918]'
              - gridcell [ref=f1e919]:
                - link " View" [ref=f1e920] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e921]: 
                  - text: View
              - gridcell "08/19/2026 7:52 PM EDT" [ref=f1e922]:
                - text: 08/19/2026
                - generic [ref=f1e923]: 7:52 PM EDT
              - gridcell [ref=f1e924]
              - gridcell "[Default Decision]" [ref=f1e925]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for unidentifiable business client]" [ref=f1e926]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e927]:
                - text: 08/20/2026
                - generic [ref=f1e928]: 3:10 PM EDT
              - gridcell [ref=f1e929]
            - row [ref=f1e930]:
              - gridcell [ref=f1e931]:
                - checkbox "Select a row" [ref=f1e934] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e935]:
                - generic [ref=f1e936]:  
                - text: "Yes"
              - gridcell "33662" [ref=f1e937]
              - gridcell "Completed[Default Decision]" [ref=f1e938]:
                - text: Completed
                - generic [ref=f1e939]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e940]
              - gridcell "Check" [ref=f1e941]
              - gridcell [ref=f1e942]:
                - link " Return" [ref=f1e943] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e944]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e945]
              - gridcell "231382306" [ref=f1e946]
              - gridcell "7578091758" [ref=f1e947]
              - gridcell "Account2" [ref=f1e948]
              - gridcell "654026230" [ref=f1e949]
              - gridcell "$176.00" [ref=f1e950]
              - gridcell "AutoPresentedPayee" [ref=f1e951]
              - gridcell [ref=f1e952]
              - gridcell [ref=f1e953]
              - gridcell "08/19/2026" [ref=f1e954]
              - gridcell [ref=f1e955]
              - gridcell [ref=f1e956]
              - gridcell [ref=f1e957]
              - 'gridcell "Check # Not Found" [ref=f1e958]'
              - gridcell [ref=f1e959]:
                - link " View" [ref=f1e960] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e961]: 
                  - text: View
              - gridcell "08/19/2026 7:42 PM EDT" [ref=f1e962]:
                - text: 08/19/2026
                - generic [ref=f1e963]: 7:42 PM EDT
              - gridcell [ref=f1e964]
              - gridcell "[Default Decision]" [ref=f1e965]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e966]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e967]:
                - text: 08/20/2026
                - generic [ref=f1e968]: 3:10 PM EDT
              - gridcell [ref=f1e969]
            - row [ref=f1e970]:
              - gridcell [ref=f1e971]:
                - checkbox "Select a row" [ref=f1e974] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e975]:
                - generic [ref=f1e976]:  
                - text: "Yes"
              - gridcell "33661" [ref=f1e977]
              - gridcell "Completed[Default Decision]" [ref=f1e978]:
                - text: Completed
                - generic [ref=f1e979]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e980]
              - gridcell "Check" [ref=f1e981]
              - gridcell [ref=f1e982]:
                - link " Return" [ref=f1e983] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e984]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e985]
              - gridcell "231382306" [ref=f1e986]
              - gridcell "7578091758" [ref=f1e987]
              - gridcell "Account2" [ref=f1e988]
              - gridcell "161852" [ref=f1e989]
              - gridcell "$250.00" [ref=f1e990]
              - gridcell [ref=f1e991]
              - gridcell [ref=f1e992]
              - gridcell [ref=f1e993]
              - gridcell "08/19/2026" [ref=f1e994]
              - gridcell [ref=f1e995]
              - gridcell [ref=f1e996]
              - gridcell [ref=f1e997]
              - 'gridcell "Check # Not Found" [ref=f1e998]'
              - gridcell [ref=f1e999]:
                - link " View" [ref=f1e1000] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1001]: 
                  - text: View
              - gridcell "08/19/2026 7:42 PM EDT" [ref=f1e1002]:
                - text: 08/19/2026
                - generic [ref=f1e1003]: 7:42 PM EDT
              - gridcell [ref=f1e1004]
              - gridcell "[Default Decision]" [ref=f1e1005]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e1006]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e1007]:
                - text: 08/20/2026
                - generic [ref=f1e1008]: 3:10 PM EDT
              - gridcell [ref=f1e1009]
            - row [ref=f1e1010]:
              - gridcell [ref=f1e1011]:
                - checkbox "Select a row" [ref=f1e1014] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e1015]:
                - generic [ref=f1e1016]:  
                - text: "Yes"
              - gridcell "33660" [ref=f1e1017]
              - gridcell "Completed[Default Decision]" [ref=f1e1018]:
                - text: Completed
                - generic [ref=f1e1019]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e1020]
              - gridcell "Check" [ref=f1e1021]
              - gridcell [ref=f1e1022]:
                - link " Return" [ref=f1e1023] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1024]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e1025]
              - gridcell "231382306" [ref=f1e1026]
              - gridcell "7578091758" [ref=f1e1027]
              - gridcell "Account2" [ref=f1e1028]
              - gridcell "161851" [ref=f1e1029]
              - gridcell "$531.00" [ref=f1e1030]
              - gridcell [ref=f1e1031]
              - gridcell [ref=f1e1032]
              - gridcell [ref=f1e1033]
              - gridcell "08/19/2026" [ref=f1e1034]
              - gridcell [ref=f1e1035]
              - gridcell [ref=f1e1036]
              - gridcell [ref=f1e1037]
              - 'gridcell "Check # Not Found" [ref=f1e1038]'
              - gridcell [ref=f1e1039]:
                - link " View" [ref=f1e1040] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1041]: 
                  - text: View
              - gridcell "08/19/2026 7:42 PM EDT" [ref=f1e1042]:
                - text: 08/19/2026
                - generic [ref=f1e1043]: 7:42 PM EDT
              - gridcell [ref=f1e1044]
              - gridcell "[Default Decision]" [ref=f1e1045]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e1046]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e1047]:
                - text: 08/20/2026
                - generic [ref=f1e1048]: 3:10 PM EDT
              - gridcell [ref=f1e1049]
            - row [ref=f1e1050]:
              - gridcell [ref=f1e1051]:
                - checkbox "Select a row" [ref=f1e1054] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e1055]:
                - generic [ref=f1e1056]:  
                - text: "Yes"
              - gridcell "33659" [ref=f1e1057]
              - gridcell "Completed[Default Decision]" [ref=f1e1058]:
                - text: Completed
                - generic [ref=f1e1059]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e1060]
              - gridcell "Check" [ref=f1e1061]
              - gridcell [ref=f1e1062]:
                - link " Return" [ref=f1e1063] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1064]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e1065]
              - gridcell "231382306" [ref=f1e1066]
              - gridcell "7578091758" [ref=f1e1067]
              - gridcell "Account2" [ref=f1e1068]
              - gridcell "600248" [ref=f1e1069]
              - gridcell "$250.00" [ref=f1e1070]
              - gridcell [ref=f1e1071]
              - gridcell [ref=f1e1072]
              - gridcell [ref=f1e1073]
              - gridcell "08/19/2026" [ref=f1e1074]
              - gridcell [ref=f1e1075]
              - gridcell [ref=f1e1076]
              - gridcell [ref=f1e1077]
              - 'gridcell "Check # Not Found" [ref=f1e1078]'
              - gridcell [ref=f1e1079]:
                - link " View" [ref=f1e1080] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1081]: 
                  - text: View
              - gridcell "08/19/2026 6:44 PM EDT" [ref=f1e1082]:
                - text: 08/19/2026
                - generic [ref=f1e1083]: 6:44 PM EDT
              - gridcell [ref=f1e1084]
              - gridcell "[Default Decision]" [ref=f1e1085]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e1086]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e1087]:
                - text: 08/20/2026
                - generic [ref=f1e1088]: 3:10 PM EDT
              - gridcell [ref=f1e1089]
            - row [ref=f1e1090]:
              - gridcell [ref=f1e1091]:
                - checkbox "Select a row" [ref=f1e1094] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e1095]:
                - generic [ref=f1e1096]:  
                - text: "Yes"
              - gridcell "33658" [ref=f1e1097]
              - gridcell "Completed[Default Decision]" [ref=f1e1098]:
                - text: Completed
                - generic [ref=f1e1099]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e1100]
              - gridcell "Check" [ref=f1e1101]
              - gridcell [ref=f1e1102]:
                - link " Return" [ref=f1e1103] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1104]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e1105]
              - gridcell "231382306" [ref=f1e1106]
              - gridcell "7578091758" [ref=f1e1107]
              - gridcell "Account2" [ref=f1e1108]
              - gridcell "600247" [ref=f1e1109]
              - gridcell "$531.00" [ref=f1e1110]
              - gridcell [ref=f1e1111]
              - gridcell [ref=f1e1112]
              - gridcell [ref=f1e1113]
              - gridcell "08/19/2026" [ref=f1e1114]
              - gridcell [ref=f1e1115]
              - gridcell [ref=f1e1116]
              - gridcell [ref=f1e1117]
              - 'gridcell "Check # Not Found" [ref=f1e1118]'
              - gridcell [ref=f1e1119]:
                - link " View" [ref=f1e1120] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1121]: 
                  - text: View
              - gridcell "08/19/2026 6:44 PM EDT" [ref=f1e1122]:
                - text: 08/19/2026
                - generic [ref=f1e1123]: 6:44 PM EDT
              - gridcell [ref=f1e1124]
              - gridcell "[Default Decision]" [ref=f1e1125]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e1126]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e1127]:
                - text: 08/20/2026
                - generic [ref=f1e1128]: 3:10 PM EDT
              - gridcell [ref=f1e1129]
            - row [ref=f1e1130]:
              - gridcell [ref=f1e1131]:
                - checkbox "Select a row" [ref=f1e1134] [cursor=pointer]
              - gridcell "  Yes" [ref=f1e1135]:
                - generic [ref=f1e1136]:  
                - text: "Yes"
              - gridcell "33657" [ref=f1e1137]
              - gridcell "Completed[Default Decision]" [ref=f1e1138]:
                - text: Completed
                - generic [ref=f1e1139]: "[Default Decision]"
              - gridcell "PJ_BC_Boutique(Both)" [ref=f1e1140]
              - gridcell "Check" [ref=f1e1141]
              - gridcell [ref=f1e1142]:
                - link " Return" [ref=f1e1143] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1144]: 
                  - text: Return
              - gridcell "Exlid123" [ref=f1e1145]
              - gridcell "231382306" [ref=f1e1146]
              - gridcell "7578091758" [ref=f1e1147]
              - gridcell "Account2" [ref=f1e1148]
              - gridcell "464137983" [ref=f1e1149]
              - gridcell "$673.00" [ref=f1e1150]
              - gridcell "AutoPresentedPayee" [ref=f1e1151]
              - gridcell [ref=f1e1152]
              - gridcell [ref=f1e1153]
              - gridcell "08/19/2026" [ref=f1e1154]
              - gridcell [ref=f1e1155]
              - gridcell [ref=f1e1156]
              - gridcell [ref=f1e1157]
              - 'gridcell "Check # Not Found" [ref=f1e1158]'
              - gridcell [ref=f1e1159]:
                - link " View" [ref=f1e1160] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f1e1161]: 
                  - text: View
              - gridcell "08/19/2026 6:41 PM EDT" [ref=f1e1162]:
                - text: 08/19/2026
                - generic [ref=f1e1163]: 6:41 PM EDT
              - gridcell [ref=f1e1164]
              - gridcell "[Default Decision]" [ref=f1e1165]
              - gridcell "[Default decision (Return) applied automatically by cutoff time for PJ_BC_Boutique(Both)]" [ref=f1e1166]
              - gridcell "08/20/2026 3:10 PM EDT" [ref=f1e1167]:
                - text: 08/20/2026
                - generic [ref=f1e1168]: 3:10 PM EDT
              - gridcell [ref=f1e1169]
        - application "Page navigation, page 1 of 6" [ref=f1e1170]:
          - generic [ref=f1e1171]:
            - button "Go to the first page" [disabled]
            - button "Go to the previous page" [disabled]
            - generic [ref=f1e1172]:
              - text: Page
              - spinbutton "Select a page" [ref=f1e1174]: "1"
              - text: of 6
            - button "Go to the next page" [ref=f1e1175] [cursor=pointer]
            - button "Go to the last page" [ref=f1e1179] [cursor=pointer]
          - generic [ref=f1e1183]: 1 - 20 of 107 items
    - contentinfo [ref=f1e1184]:
      - generic [ref=f1e1185]:
        - text: PJ_FI_Bank (Playwright Automation)
        - generic [ref=f1e1186]: "[uat-release]"
      - generic [ref=f1e1187]:
        - text: © Copyright Advanced Fraud Solutions 2005-2026 |
        - generic [ref=f1e1188]: All Rights Reserved
        - text: "|"
        - link "Privacy Policy" [ref=f1e1190] [cursor=pointer]:
          - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  272 |     });
  273 | 
  274 |     // ── Exception History: Row actions ───────────────────────────────────────
  275 | 
  276 |     test('"View" link on a row opens the Exception Details dialog', async ({ pageManager, page }) => {
  277 |         await pageManager.exceptionPage.navigateToExceptionHistory();
  278 |         
  279 |         // Filter Decision column by Pay and Return to exclude Pending decisions
  280 |         await pageManager.exceptionPage.openExceptionHistoryColumnFilter('Decision');
  281 |         const filterPopup = page.locator('.k-grid-filter-popup[aria-label="Decision Filter Menu"]');
  282 |         
  283 |         // Uncheck "Select All" first to clear all selections
  284 |         const selectAll = filterPopup.getByLabel('Select All', { exact: true });
  285 |         if (await selectAll.isVisible().catch(() => false)) {
  286 |             await selectAll.setChecked(false);
  287 |         }
  288 |         
  289 |         // Select both Pay and Return
  290 |         await filterPopup.getByLabel('Pay', { exact: true }).check();
  291 |         await filterPopup.getByLabel('Return', { exact: true }).check();
  292 |         await filterPopup.getByRole('button', { name: 'Filter', exact: true }).click();
  293 |         
  294 |         // Wait for filter popup to close
  295 |         await filterPopup.waitFor({ state: 'hidden', timeout: 10000 });
  296 |         
  297 |         // Wait for grid to reload with filtered data
  298 |         await pageManager.exceptionPage.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 15000 });
  299 | 
  300 |         // Navigate through filtered pages if needed to find a visible View link
  301 |         let exceptionDetailsViewLink = pageManager.exceptionPage.exceptionHistoryGridRows
  302 |             .first()
  303 |             .getByRole('link', { name: /View/i });
  304 |         
  305 |         let viewLinkFound = false;
  306 |         let pageCount = 0;
  307 |         const maxPages = 5; // Safety limit (should be fewer pages after filtering)
  308 | 
  309 |         while (!viewLinkFound && pageCount < maxPages) {
  310 |             const isVisible = await exceptionDetailsViewLink.isVisible({ timeout: 2000 }).catch(() => false);
  311 |             
  312 |             if (isVisible) {
  313 |                 viewLinkFound = true;
  314 |                 break;
  315 |             }
  316 | 
  317 |             // Check if next page button is enabled
  318 |             const nextButton = pageManager.exceptionPage.nextPageButton;
  319 |             const isNextEnabled = await nextButton.isEnabled().catch(() => false);
  320 | 
  321 |             if (!isNextEnabled) {
  322 |                 break; // No more pages to check
  323 |             }
  324 | 
  325 |             // Navigate to next page
  326 |             await nextButton.click();
  327 |             await pageManager.exceptionPage.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 10000 });
  328 |             pageCount++;
  329 |         }
  330 | 
  331 |         if (!viewLinkFound) {
  332 |             throw new Error(`No View link found in Pay/Return filtered results after checking ${pageCount + 1} page(s).`);
  333 |         }
  334 | 
  335 |         await expect(exceptionDetailsViewLink).toBeVisible({ timeout: 5000 });
  336 |         await exceptionDetailsViewLink.click();
  337 |         await expect(pageManager.exceptionPage.exceptionDetailsDialog).toBeVisible({ timeout: 10000 });
  338 |         await pageManager.exceptionPage.closeExceptionDetailsDialog();
  339 |     });
  340 | 
  341 |     test('Decision badge on an already-reviewed row is blocked with a system message', async ({ pageManager, page }) => {
  342 |         await pageManager.exceptionPage.navigateToExceptionHistory();
  343 |         
  344 |         // Filter Reviewed? column by Yes to show only already-reviewed exceptions
  345 |         await pageManager.exceptionPage.openExceptionHistoryColumnFilter('Reviewed?');
  346 |         const filterPopup = page.locator('.k-grid-filter-popup[aria-label="Reviewed? Filter Menu"]');
  347 |         
  348 |         // Uncheck "Select All" first to clear all selections
  349 |         const selectAll = filterPopup.getByLabel('Select All', { exact: true });
  350 |         if (await selectAll.isVisible().catch(() => false)) {
  351 |             await selectAll.setChecked(false);
  352 |         }
  353 |         
  354 |         // Select only "Yes"
  355 |         await filterPopup.getByLabel('Yes', { exact: true }).check();
  356 |         await filterPopup.getByRole('button', { name: 'Filter', exact: true }).click();
  357 |         
  358 |         // Wait for filter popup to close
  359 |         await filterPopup.waitFor({ state: 'hidden', timeout: 10000 });
  360 |         
  361 |         // Wait for grid to reload with filtered data
  362 |         await pageManager.exceptionPage.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 15000 });
  363 | 
  364 |         // Get the Return or Pay decision badge from the first row
  365 |         const decisionBadge = pageManager.exceptionPage.exceptionHistoryGridRows
  366 |             .first()
  367 |             .locator('a[href="javascript:;"]')
  368 |             .filter({ hasText: /Pay|Return/i })
  369 |             .first();
  370 | 
  371 |         await expect(decisionBadge).toBeVisible({ timeout: 15000 });
> 372 |         await decisionBadge.scrollIntoViewIfNeeded();
      |                             ^ Error: locator.scrollIntoViewIfNeeded: Element is not attached to the DOM
  373 |         await decisionBadge.click();
  374 |         await expect(pageManager.exceptionPage.systemMessageDialog).toBeVisible({ timeout: 10000 });
  375 |         await expect(pageManager.exceptionPage.systemMessageDialog)
  376 |             .toContainText('Decision cannot be changed after exception has been reviewed');
  377 |         await pageManager.exceptionPage.closeSystemMessageDialog();
  378 |     });
  379 | 
  380 |     // ── Exception History: Breadcrumb ────────────────────────────────────────
  381 | 
  382 |     test('Exceptions breadcrumb link is visible on the page', async ({ pageManager }) => {
  383 |         await pageManager.exceptionPage.navigateToExceptionHistory();
  384 |         await expect(pageManager.exceptionPage.pageHeading).toBeVisible();
  385 |     });
  386 | 
  387 |     // ── Open Exceptions (Card View) ──────────────────────────────────────────
  388 | 
  389 |     test('Navigation tabs to Pre-Decisions, Approvals, and Exception History are visible', async ({ pageManager }) => {
  390 |         await pageManager.exceptionPage.navigateToOpenExceptions();
  391 |         await expect(pageManager.exceptionPage.openExceptionsNavLink).toBeVisible();
  392 |         await expect(pageManager.exceptionPage.preDecisionsNavLink).toBeVisible();
  393 |         await expect(pageManager.exceptionPage.approvalsNavLink).toBeVisible();
  394 |         await expect(pageManager.exceptionPage.exceptionHistoryNavLink).toBeVisible();
  395 |     });
  396 | 
  397 |     test('Open Exceptions page loads with either exception cards or the empty-state message', async ({ pageManager }) => {
  398 |         await pageManager.exceptionPage.navigateToOpenExceptions();
  399 |         await expect.poll(async () => {
  400 |             const hasCards = await pageManager.exceptionPage.exceptionIdFromCardView.first().isVisible().catch(() => false);
  401 |             const hasEmptyMessage = await pageManager.exceptionPage.noExceptionsMessage.isVisible().catch(() => false);
  402 |             return hasCards || hasEmptyMessage;
  403 |         }, { timeout: 15000 }).toBeTruthy();
  404 |     });
  405 | 
  406 |     test('Grid View toggle navigates to the open-exceptions grid and shows key column headers', async ({ pageManager, page }) => {
  407 |         await pageManager.exceptionPage.navigateToOpenExceptions();
  408 |         await pageManager.exceptionPage.exceptionsGridViewButton.click();
  409 |         await expect(page).toHaveURL(/\/exceptions\/open/, { timeout: 15000 });
  410 |         await expect(page.getByRole('columnheader', { name: /^Business Client/ }).first()).toBeVisible({ timeout: 15000 });
  411 |     });
  412 | 
  413 |     // ── Approvals ─────────────────────────────────────────────────────────────
  414 | 
  415 |     test('Approvals page loads with either records or the empty-state message', async ({ pageManager }) => {
  416 |         await pageManager.exceptionPage.navigateToApprovals();
  417 |         // Blazor renders the empty-state text (or rows) asynchronously after domcontentloaded fires.
  418 |         await expect.poll(async () => {
  419 |             const hasEmptyMessage = await pageManager.exceptionPage.noApprovalsMessage.isVisible().catch(() => false);
  420 |             const hasRows = await pageManager.exceptionPage.exceptionGridRows.first().isVisible().catch(() => false);
  421 |             return hasEmptyMessage || hasRows;
  422 |         }, { timeout: 15000 }).toBeTruthy();
  423 |     });
  424 | 
  425 |     // ── Pre-Decisions ─────────────────────────────────────────────────────────
  426 | 
  427 |     test('Pre-Decisions page loads with either records or the empty-state message', async ({ pageManager }) => {
  428 |         await pageManager.exceptionPage.navigateToPreDecisions();
  429 |         await expect.poll(async () => {
  430 |             const hasEmptyMessage = await pageManager.exceptionPage.noPreDecisionsMessage.isVisible().catch(() => false);
  431 |             const hasRows = await pageManager.exceptionPage.exceptionGridRows.first().isVisible().catch(() => false);
  432 |             const hasCards = await pageManager.exceptionPage.preDecisionExceptionCards.first().isVisible().catch(() => false);
  433 |             return hasEmptyMessage || hasRows || hasCards;
  434 |         }, { timeout: 15000 }).toBeTruthy();
  435 |     });
  436 | 
  437 | });
  438 | 
```