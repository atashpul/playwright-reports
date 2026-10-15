# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\8-ExceptionsSmoke.spec.ts >> Exceptions — Smoke >> Exception History >> Column Filter >> Column filter menu applies a filter and Clear restores the full row set
- Location: specs\Smoke\8-ExceptionsSmoke.spec.ts:263:13

# Error details

```
Error: expect(received).toBe(expected) // Object.is equality

Expected: true
Received: false

Call Log:
- Timeout 15000ms exceeded while waiting on the predicate
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
      - list [ref=e55]:
        - listitem [ref=e56]:
          - link " " [ref=e57] [cursor=pointer]:
            - /url: /
        - listitem [ref=e59]:
          - link "Exceptions" [ref=e60] [cursor=pointer]:
            - /url: /exceptions
        - listitem [ref=e61]:
          - link "History" [ref=e62]:
            - /url: javascript:;
      - generic [ref=e64]:
        - toolbar "Grid toolbar" [ref=e65]:
          - generic [ref=e66]:
            - generic [ref=e67]:
              - generic [ref=e68]:
                - generic [ref=e69]: Page Size
                - combobox [ref=e71]:
                  - option "10"
                  - option "20" [selected]
                  - option "50"
                  - option "100"
              - button "Excel" [ref=e72] [cursor=pointer]
              - textbox "Search..." [ref=e79]
            - button " Mark as Reviewed [0]" [ref=e81] [cursor=pointer]:
              - generic [ref=e82]: 
              - text: Mark as Reviewed [0]
            - generic [ref=e84]:
              - generic [ref=e85]: Saved Filters
              - combobox [ref=e87]:
                - option "[No Filter]" [selected]
                - option "Active"
                - option "Reviewed"
              - button "+" [ref=e89] [cursor=pointer]
        - grid "Data table" [ref=e91]:
          - rowgroup [ref=e122]:
            - row [ref=e123]:
              - columnheader [ref=e124]:
                - checkbox "Select all rows" [ref=e126] [cursor=pointer]
              - columnheader "Reviewed? Reviewed? column filter menu settings" [ref=e127]:
                - generic [ref=e128]:
                  - generic [ref=e129] [cursor=pointer]: Reviewed?
                  - button "Reviewed? column filter menu settings" [ref=e131]
              - columnheader "ID ID column filter menu settings" [ref=e136]:
                - generic [ref=e137]:
                  - generic [ref=e138] [cursor=pointer]: ID
                  - button "ID column filter menu settings" [ref=e140]
              - columnheader "Status Status column filter menu settings" [ref=e145]:
                - generic [ref=e146]:
                  - generic [ref=e147] [cursor=pointer]: Status
                  - button "Status column filter menu settings" [ref=e149]
              - columnheader "Business Client Business Client column filter menu settings" [ref=e154]:
                - generic [ref=e155]:
                  - generic [ref=e156] [cursor=pointer]: Business Client
                  - button "Business Client column filter menu settings" [ref=e158]
              - columnheader "Type Type column filter menu settings" [ref=e163]:
                - generic [ref=e164]:
                  - generic [ref=e165] [cursor=pointer]: Type
                  - button "Type column filter menu settings" [ref=e167]
              - columnheader "Decision Decision column filter menu settings" [ref=e172]:
                - generic [ref=e173]:
                  - generic [ref=e174] [cursor=pointer]: Decision
                  - button "Decision column filter menu settings" [ref=e176]
              - columnheader "Reference ID Reference ID column filter menu settings" [ref=e181]:
                - generic [ref=e182]:
                  - generic [ref=e183] [cursor=pointer]: Reference ID
                  - button "Reference ID column filter menu settings" [ref=e185]
              - 'columnheader "Routing # Routing # column filter menu settings" [ref=e190]':
                - generic [ref=e191]:
                  - generic [ref=e192] [cursor=pointer]: "Routing #"
                  - 'button "Routing # column filter menu settings" [ref=e194]'
              - 'columnheader "Account # Account # column filter menu settings" [ref=e199]':
                - generic [ref=e200]:
                  - generic [ref=e201] [cursor=pointer]: "Account #"
                  - 'button "Account # column filter menu settings" [ref=e203]'
              - columnheader "Account Name Account Name column filter menu settings" [ref=e208]:
                - generic [ref=e209]:
                  - generic [ref=e210] [cursor=pointer]: Account Name
                  - button "Account Name column filter menu settings" [ref=e212]
              - 'columnheader "Check #/SEC Code Check #/SEC Code column filter menu settings" [ref=e217]':
                - generic [ref=e218]:
                  - generic [ref=e219] [cursor=pointer]: "Check #/SEC Code"
                  - 'button "Check #/SEC Code column filter menu settings" [ref=e221]'
              - columnheader "Amount Amount column filter menu settings" [ref=e226]:
                - generic [ref=e227]:
                  - generic [ref=e228] [cursor=pointer]: Amount
                  - button "Amount column filter menu settings" [ref=e230]
              - columnheader "Payee/Originator Payee/Originator column filter menu settings" [ref=e235]:
                - generic [ref=e236]:
                  - generic [ref=e237] [cursor=pointer]: Payee/Originator
                  - button "Payee/Originator column filter menu settings" [ref=e239]
              - columnheader "Trans Code Trans Code column filter menu settings" [ref=e244]:
                - generic [ref=e245]:
                  - generic [ref=e246] [cursor=pointer]: Trans Code
                  - button "Trans Code column filter menu settings" [ref=e248]
              - columnheader "Trans Type Trans Type column filter menu settings" [ref=e253]:
                - generic [ref=e254]:
                  - generic [ref=e255] [cursor=pointer]: Trans Type
                  - button "Trans Type column filter menu settings" [ref=e257]
              - columnheader "Trans Date  Trans Date column filter menu settings" [ref=e262]:
                - generic [ref=e263]:
                  - generic [ref=e265] [cursor=pointer]:
                    - text: Trans Date
                    - generic "Check Presented Date or ACH Entry Date or the date when ACH transaction was presented" [ref=e266]: 
                  - button "Trans Date column filter menu settings" [ref=e267]
              - columnheader "Settlement Date Settlement Date column filter menu settings" [ref=e272]:
                - generic [ref=e273]:
                  - generic [ref=e274] [cursor=pointer]: Settlement Date
                  - button "Settlement Date column filter menu settings" [ref=e276]
              - columnheader "Issued Check Data" [ref=e281]
              - columnheader "Check Image" [ref=e283]
              - columnheader "Exception Reason Exception Reason column filter menu settings" [ref=e285]:
                - generic [ref=e286]:
                  - generic [ref=e287] [cursor=pointer]: Exception Reason
                  - button "Exception Reason column filter menu settings" [ref=e289]
              - columnheader "Exception" [ref=e294]
              - columnheader [ref=e296]:
                - text: Exception Date
                - button "Exception Date column filter menu settings" [ref=e297]
              - columnheader "Approval" [ref=e302]
              - columnheader "Decision By Decision By column filter menu settings" [ref=e304]:
                - generic [ref=e305]:
                  - generic [ref=e306] [cursor=pointer]: Decision By
                  - button "Decision By column filter menu settings" [ref=e308]
              - columnheader "Decision Notes Decision Notes column filter menu settings" [ref=e313]:
                - generic [ref=e314]:
                  - generic [ref=e315] [cursor=pointer]: Decision Notes
                  - button "Decision Notes column filter menu settings" [ref=e317]
              - columnheader [ref=e322]:
                - text: Decision Date
                - button "Decision Date column filter menu settings" [ref=e323]
              - columnheader "Return Code Return Code column filter menu settings" [ref=e328]:
                - generic [ref=e329]:
                  - generic [ref=e330] [cursor=pointer]: Return Code
                  - button "Return Code column filter menu settings" [ref=e332]
              - columnheader "Return Reason Return Reason column filter menu settings" [ref=e337]:
                - generic [ref=e338]:
                  - generic [ref=e339] [cursor=pointer]: Return Reason
                  - button "Return Reason column filter menu settings" [ref=e341]
          - rowgroup [ref=e380]:
            - row [ref=e381]:
              - gridcell [ref=e382]:
                - checkbox "Select a row" [ref=e385] [cursor=pointer]
              - gridcell " No" [ref=e386]:
                - generic [ref=e387]: 
                - text: "No"
              - gridcell "895" [ref=e388]
              - gridcell "Completed[Manual Decision]" [ref=e389]:
                - text: Completed
                - generic [ref=e390]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e391]
              - gridcell "Teller" [ref=e392]
              - gridcell " Return" [ref=e393]:
                - generic [ref=e394]:
                  - generic [ref=e395]: 
                  - text: Return
              - gridcell "Exlid777" [ref=e396]
              - gridcell "063110047" [ref=e397]
              - gridcell "10047" [ref=e398]
              - gridcell "Account14" [ref=e399]
              - gridcell "7463" [ref=e400]
              - gridcell "$100.00" [ref=e401]
              - gridcell [ref=e402]
              - gridcell [ref=e403]
              - gridcell [ref=e404]
              - gridcell "09/24/2026" [ref=e405]
              - gridcell [ref=e406]
              - gridcell [ref=e407]:
                - link " View" [ref=e408] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e409]: 
                  - text: View
              - gridcell [ref=e410]
              - gridcell "Missing Payee, Void or Stopped Check" [ref=e411]
              - gridcell [ref=e412]
              - gridcell "09/24/2026 12:00 AM EDT" [ref=e413]:
                - text: 09/24/2026
                - generic [ref=e414]: 12:00 AM EDT
              - gridcell [ref=e415]
              - gridcell "F.I ACH&CHK User" [ref=e416]
              - gridcell [ref=e417]
              - gridcell "09/24/2026 8:03 PM EDT" [ref=e418]:
                - text: 09/24/2026
                - generic [ref=e419]: 8:03 PM EDT
              - gridcell [ref=e420]
              - gridcell [ref=e421]
            - row [ref=e422]:
              - gridcell [ref=e423]:
                - checkbox "Select a row" [ref=e426] [cursor=pointer]
              - gridcell " No" [ref=e427]:
                - generic [ref=e428]: 
                - text: "No"
              - gridcell "894" [ref=e429]
              - gridcell "Completed[Manual Decision]" [ref=e430]:
                - text: Completed
                - generic [ref=e431]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e432]
              - gridcell "Teller" [ref=e433]
              - gridcell "$ Pay" [ref=e434]:
                - generic [ref=e435]:
                  - generic [ref=e436]: $
                  - text: Pay
              - gridcell "PJ456!" [ref=e437]
              - gridcell "122199983" [ref=e438]
              - gridcell "123456" [ref=e439]
              - gridcell "Account_Boutique" [ref=e440]
              - gridcell "812345678901" [ref=e441]
              - gridcell "$50.00" [ref=e442]
              - gridcell [ref=e443]
              - gridcell [ref=e444]
              - gridcell [ref=e445]
              - gridcell "09/24/2026" [ref=e446]
              - gridcell [ref=e447]
              - gridcell [ref=e448]
              - gridcell [ref=e449]
              - 'gridcell "Check # Not Found" [ref=e450]'
              - gridcell [ref=e451]
              - gridcell "09/24/2026 12:00 AM EDT" [ref=e452]:
                - text: 09/24/2026
                - generic [ref=e453]: 12:00 AM EDT
              - gridcell [ref=e454]
              - gridcell "F.I ACH&CHK User" [ref=e455]
              - gridcell [ref=e456]
              - gridcell "09/24/2026 3:49 PM EDT" [ref=e457]:
                - text: 09/24/2026
                - generic [ref=e458]: 3:49 PM EDT
              - gridcell [ref=e459]
              - gridcell [ref=e460]
            - row [ref=e461]:
              - gridcell [ref=e462]:
                - checkbox "Select a row" [ref=e465] [cursor=pointer]
              - gridcell " No" [ref=e466]:
                - generic [ref=e467]: 
                - text: "No"
              - gridcell "891" [ref=e468]
              - gridcell "Completed[Manual Decision]" [ref=e469]:
                - text: Completed
                - generic [ref=e470]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e471]
              - gridcell "Teller" [ref=e472]
              - gridcell "$ Pay" [ref=e473]:
                - generic [ref=e474]:
                  - generic [ref=e475]: $
                  - text: Pay
              - gridcell "PJ456!" [ref=e476]
              - gridcell "122199983" [ref=e477]
              - gridcell "123456" [ref=e478]
              - gridcell "Account_Boutique" [ref=e479]
              - gridcell "361437535361" [ref=e480]
              - gridcell "$50.00" [ref=e481]
              - gridcell [ref=e482]
              - gridcell [ref=e483]
              - gridcell [ref=e484]
              - gridcell "09/24/2026" [ref=e485]
              - gridcell [ref=e486]
              - gridcell [ref=e487]
              - gridcell [ref=e488]
              - 'gridcell "Check # Not Found" [ref=e489]'
              - gridcell [ref=e490]
              - gridcell "09/24/2026 12:00 AM EDT" [ref=e491]:
                - text: 09/24/2026
                - generic [ref=e492]: 12:00 AM EDT
              - gridcell [ref=e493]
              - gridcell "Chromium Automation" [ref=e494]
              - gridcell [ref=e495]
              - gridcell "09/24/2026 3:36 PM EDT" [ref=e496]:
                - text: 09/24/2026
                - generic [ref=e497]: 3:36 PM EDT
              - gridcell [ref=e498]
              - gridcell [ref=e499]
            - row [ref=e500]:
              - gridcell [ref=e501]:
                - checkbox "Select a row" [ref=e504] [cursor=pointer]
              - gridcell " No" [ref=e505]:
                - generic [ref=e506]: 
                - text: "No"
              - gridcell "890" [ref=e507]
              - gridcell "Completed[Manual Decision]" [ref=e508]:
                - text: Completed
                - generic [ref=e509]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e510]
              - gridcell "Teller" [ref=e511]
              - gridcell "$ Pay" [ref=e512]:
                - generic [ref=e513]:
                  - generic [ref=e514]: $
                  - text: Pay
              - gridcell "PJ456!" [ref=e515]
              - gridcell "122199983" [ref=e516]
              - gridcell "123456" [ref=e517]
              - gridcell "Account_Boutique" [ref=e518]
              - gridcell "631734800708" [ref=e519]
              - gridcell "$50.00" [ref=e520]
              - gridcell [ref=e521]
              - gridcell [ref=e522]
              - gridcell [ref=e523]
              - gridcell "09/24/2026" [ref=e524]
              - gridcell [ref=e525]
              - gridcell [ref=e526]
              - gridcell [ref=e527]
              - 'gridcell "Check # Not Found" [ref=e528]'
              - gridcell [ref=e529]
              - gridcell "09/24/2026 12:00 AM EDT" [ref=e530]:
                - text: 09/24/2026
                - generic [ref=e531]: 12:00 AM EDT
              - gridcell [ref=e532]
              - gridcell "Chromium Automation" [ref=e533]
              - gridcell [ref=e534]
              - gridcell "09/24/2026 3:36 PM EDT" [ref=e535]:
                - text: 09/24/2026
                - generic [ref=e536]: 3:36 PM EDT
              - gridcell [ref=e537]
              - gridcell [ref=e538]
            - row [ref=e539]:
              - gridcell [ref=e540]:
                - checkbox "Select a row" [ref=e543] [cursor=pointer]
              - gridcell " No" [ref=e544]:
                - generic [ref=e545]: 
                - text: "No"
              - gridcell "888" [ref=e546]
              - gridcell "Completed[Manual Decision]" [ref=e547]:
                - text: Completed
                - generic [ref=e548]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e549]
              - gridcell "Teller" [ref=e550]
              - gridcell " Return" [ref=e551]:
                - generic [ref=e552]:
                  - generic [ref=e553]: 
                  - text: Return
              - gridcell "PJ456!" [ref=e554]
              - gridcell "122199983" [ref=e555]
              - gridcell "123456" [ref=e556]
              - gridcell "Account_Boutique" [ref=e557]
              - gridcell "361865537101" [ref=e558]
              - gridcell "$50.00" [ref=e559]
              - gridcell [ref=e560]
              - gridcell [ref=e561]
              - gridcell [ref=e562]
              - gridcell "09/24/2026" [ref=e563]
              - gridcell [ref=e564]
              - gridcell [ref=e565]
              - gridcell [ref=e566]
              - 'gridcell "Check # Not Found" [ref=e567]'
              - gridcell [ref=e568]
              - gridcell "09/24/2026 12:00 AM EDT" [ref=e569]:
                - text: 09/24/2026
                - generic [ref=e570]: 12:00 AM EDT
              - gridcell [ref=e571]
              - gridcell "Chromium Automation" [ref=e572]
              - gridcell [ref=e573]
              - gridcell "09/24/2026 3:36 PM EDT" [ref=e574]:
                - text: 09/24/2026
                - generic [ref=e575]: 3:36 PM EDT
              - gridcell [ref=e576]
              - gridcell [ref=e577]
            - row [ref=e578]:
              - gridcell [ref=e579]:
                - checkbox "Select a row" [ref=e582] [cursor=pointer]
              - gridcell " No" [ref=e583]:
                - generic [ref=e584]: 
                - text: "No"
              - gridcell "887" [ref=e585]
              - gridcell "Completed[Manual Decision]" [ref=e586]:
                - text: Completed
                - generic [ref=e587]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e588]
              - gridcell "Teller" [ref=e589]
              - gridcell "$ Pay" [ref=e590]:
                - generic [ref=e591]:
                  - generic [ref=e592]: $
                  - text: Pay
              - gridcell "PJ456!" [ref=e593]
              - gridcell "122199983" [ref=e594]
              - gridcell "123456" [ref=e595]
              - gridcell "Account_Boutique" [ref=e596]
              - gridcell "491929821092" [ref=e597]
              - gridcell "$50.00" [ref=e598]
              - gridcell [ref=e599]
              - gridcell [ref=e600]
              - gridcell [ref=e601]
              - gridcell "09/24/2026" [ref=e602]
              - gridcell [ref=e603]
              - gridcell [ref=e604]
              - gridcell [ref=e605]
              - 'gridcell "Check # Not Found" [ref=e606]'
              - gridcell [ref=e607]
              - gridcell "09/24/2026 12:00 AM EDT" [ref=e608]:
                - text: 09/24/2026
                - generic [ref=e609]: 12:00 AM EDT
              - gridcell [ref=e610]
              - gridcell "Chromium Automation" [ref=e611]
              - gridcell [ref=e612]
              - gridcell "09/24/2026 3:36 PM EDT" [ref=e613]:
                - text: 09/24/2026
                - generic [ref=e614]: 3:36 PM EDT
              - gridcell [ref=e615]
              - gridcell [ref=e616]
            - row [ref=e617]:
              - gridcell [ref=e618]:
                - checkbox "Select a row" [ref=e621] [cursor=pointer]
              - gridcell " No" [ref=e622]:
                - generic [ref=e623]: 
                - text: "No"
              - gridcell "886" [ref=e624]
              - gridcell "Completed[Manual Decision]" [ref=e625]:
                - text: Completed
                - generic [ref=e626]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e627]
              - gridcell "Teller" [ref=e628]
              - gridcell " Return" [ref=e629]:
                - generic [ref=e630]:
                  - generic [ref=e631]: 
                  - text: Return
              - gridcell "PJ456!" [ref=e632]
              - gridcell "122199983" [ref=e633]
              - gridcell "123456" [ref=e634]
              - gridcell "Account_Boutique" [ref=e635]
              - gridcell "899988887777" [ref=e636]
              - gridcell "$66.00" [ref=e637]
              - gridcell [ref=e638]
              - gridcell [ref=e639]
              - gridcell [ref=e640]
              - gridcell "09/24/2026" [ref=e641]
              - gridcell [ref=e642]
              - gridcell [ref=e643]
              - gridcell [ref=e644]
              - 'gridcell "Check # Not Found" [ref=e645]'
              - gridcell [ref=e646]
              - gridcell "09/24/2026 12:00 AM EDT" [ref=e647]:
                - text: 09/24/2026
                - generic [ref=e648]: 12:00 AM EDT
              - gridcell [ref=e649]
              - gridcell "F.I ACH&CHK User" [ref=e650]
              - gridcell [ref=e651]
              - gridcell "09/24/2026 3:29 PM EDT" [ref=e652]:
                - text: 09/24/2026
                - generic [ref=e653]: 3:29 PM EDT
              - gridcell [ref=e654]
              - gridcell [ref=e655]
            - row [ref=e656]:
              - gridcell [ref=e657]:
                - checkbox "Select a row" [ref=e660] [cursor=pointer]
              - gridcell " No" [ref=e661]:
                - generic [ref=e662]: 
                - text: "No"
              - gridcell "885" [ref=e663]
              - gridcell "Completed[Manual Decision]" [ref=e664]:
                - text: Completed
                - generic [ref=e665]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e666]
              - gridcell "Teller" [ref=e667]
              - gridcell "$ Pay" [ref=e668]:
                - generic [ref=e669]:
                  - generic [ref=e670]: $
                  - text: Pay
              - gridcell "PJ456!" [ref=e671]
              - gridcell "122199983" [ref=e672]
              - gridcell "123456" [ref=e673]
              - gridcell "Account_Boutique" [ref=e674]
              - gridcell "812345678901" [ref=e675]
              - gridcell "$55.00" [ref=e676]
              - gridcell [ref=e677]
              - gridcell [ref=e678]
              - gridcell [ref=e679]
              - gridcell "09/24/2026" [ref=e680]
              - gridcell [ref=e681]
              - gridcell [ref=e682]
              - gridcell [ref=e683]
              - 'gridcell "Check # Not Found" [ref=e684]'
              - gridcell [ref=e685]
              - gridcell "09/24/2026 12:00 AM EDT" [ref=e686]:
                - text: 09/24/2026
                - generic [ref=e687]: 12:00 AM EDT
              - gridcell [ref=e688]
              - gridcell "F.I ACH&CHK User" [ref=e689]
              - gridcell [ref=e690]
              - gridcell "09/24/2026 3:28 PM EDT" [ref=e691]:
                - text: 09/24/2026
                - generic [ref=e692]: 3:28 PM EDT
              - gridcell [ref=e693]
              - gridcell [ref=e694]
            - row [ref=e695]:
              - gridcell [ref=e696]:
                - checkbox "Select a row" [ref=e699] [cursor=pointer]
              - gridcell "  Yes" [ref=e700]:
                - generic [ref=e701]:  
                - text: "Yes"
              - gridcell "9886" [ref=e702]
              - gridcell "Completed[Manual Decision]" [ref=e703]:
                - text: Completed
                - generic [ref=e704]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e705]
              - gridcell "ACH" [ref=e706]
              - gridcell [ref=e707]:
                - link " Return" [ref=e708] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e709]: 
                  - text: Return
              - gridcell "Exlid123" [ref=e710]
              - gridcell "24308334" [ref=e711]
              - gridcell [ref=e712]
              - gridcell "Account2" [ref=e713]
              - gridcell "WEB" [ref=e714]
              - gridcell "$751.04" [ref=e715]
              - gridcell "Omega FCU" [ref=e716]
              - gridcell "27" [ref=e717]
              - gridcell "Debit to Checking" [ref=e718]
              - gridcell "03/13/2026" [ref=e719]
              - gridcell [ref=e720]
              - gridcell [ref=e721]
              - gridcell [ref=e722]
              - gridcell [ref=e723]
              - gridcell [ref=e724]:
                - link " View" [ref=e725] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e726]: 
                  - text: View
              - gridcell "09/24/2026 1:56 PM EDT" [ref=e727]:
                - text: 09/24/2026
                - generic [ref=e728]: 1:56 PM EDT
              - gridcell [ref=e729]
              - gridcell "F.I ACH&CHK User" [ref=e730]
              - gridcell [ref=e731]
              - gridcell "09/24/2026 1:57 PM EDT" [ref=e732]:
                - text: 09/24/2026
                - generic [ref=e733]: 1:57 PM EDT
              - gridcell [ref=e734]
              - gridcell [ref=e735]
            - row [ref=e736]:
              - gridcell [ref=e737]:
                - checkbox "Select a row" [ref=e740] [cursor=pointer]
              - gridcell "  Yes" [ref=e741]:
                - generic [ref=e742]:  
                - text: "Yes"
              - gridcell "9885" [ref=e743]
              - gridcell "Completed[Manual Decision]" [ref=e744]:
                - text: Completed
                - generic [ref=e745]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e746]
              - gridcell "ACH" [ref=e747]
              - gridcell [ref=e748]:
                - link " Return" [ref=e749] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e750]: 
                  - text: Return
              - gridcell "Exlid123" [ref=e751]
              - gridcell "24308334" [ref=e752]
              - gridcell [ref=e753]
              - gridcell "Account2" [ref=e754]
              - gridcell "WEB" [ref=e755]
              - gridcell "$654.38" [ref=e756]
              - gridcell "Omega FCU" [ref=e757]
              - gridcell "22" [ref=e758]
              - gridcell "Credit to Checking" [ref=e759]
              - gridcell "03/13/2026" [ref=e760]
              - gridcell [ref=e761]
              - gridcell [ref=e762]
              - gridcell [ref=e763]
              - gridcell [ref=e764]
              - gridcell [ref=e765]:
                - link " View" [ref=e766] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e767]: 
                  - text: View
              - gridcell "09/24/2026 1:56 PM EDT" [ref=e768]:
                - text: 09/24/2026
                - generic [ref=e769]: 1:56 PM EDT
              - gridcell [ref=e770]
              - gridcell "F.I ACH&CHK User" [ref=e771]
              - gridcell [ref=e772]
              - gridcell "09/24/2026 1:56 PM EDT" [ref=e773]:
                - text: 09/24/2026
                - generic [ref=e774]: 1:56 PM EDT
              - gridcell [ref=e775]
              - gridcell [ref=e776]
            - row [ref=e777]:
              - gridcell [ref=e778]:
                - checkbox "Select a row" [ref=e781] [cursor=pointer]
              - gridcell "  Yes" [ref=e782]:
                - generic [ref=e783]:  
                - text: "Yes"
              - gridcell "9866" [ref=e784]
              - gridcell "Completed[Manual Decision]" [ref=e785]:
                - text: Completed
                - generic [ref=e786]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e787]
              - gridcell "ACH" [ref=e788]
              - gridcell [ref=e789]:
                - link " Return" [ref=e790] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e791]: 
                  - text: Return
              - gridcell "Exlid123" [ref=e792]
              - gridcell "24308334" [ref=e793]
              - gridcell [ref=e794]
              - gridcell "Account2" [ref=e795]
              - gridcell "WEB" [ref=e796]
              - gridcell "$554.38" [ref=e797]
              - gridcell "Omega FCU" [ref=e798]
              - gridcell "22" [ref=e799]
              - gridcell "Credit to Checking" [ref=e800]
              - gridcell "03/13/2026" [ref=e801]
              - gridcell [ref=e802]
              - gridcell [ref=e803]
              - gridcell [ref=e804]
              - gridcell [ref=e805]
              - gridcell [ref=e806]:
                - link " View" [ref=e807] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e808]: 
                  - text: View
              - gridcell "09/24/2026 9:51 AM EDT" [ref=e809]:
                - text: 09/24/2026
                - generic [ref=e810]: 9:51 AM EDT
              - gridcell [ref=e811]
              - gridcell "F.I ACH&CHK User" [ref=e812]
              - gridcell [ref=e813]
              - gridcell "09/24/2026 9:51 AM EDT" [ref=e814]:
                - text: 09/24/2026
                - generic [ref=e815]: 9:51 AM EDT
              - gridcell [ref=e816]
              - gridcell [ref=e817]
            - row [ref=e818]:
              - gridcell [ref=e819]:
                - checkbox "Select a row" [ref=e822] [cursor=pointer]
              - gridcell "  Yes" [ref=e823]:
                - generic [ref=e824]:  
                - text: "Yes"
              - gridcell "9867" [ref=e825]
              - gridcell "Completed[Manual Decision]" [ref=e826]:
                - text: Completed
                - generic [ref=e827]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e828]
              - gridcell "ACH" [ref=e829]
              - gridcell [ref=e830]:
                - link " Return" [ref=e831] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e832]: 
                  - text: Return
              - gridcell "Exlid123" [ref=e833]
              - gridcell "24308334" [ref=e834]
              - gridcell [ref=e835]
              - gridcell "Account2" [ref=e836]
              - gridcell "WEB" [ref=e837]
              - gridcell "$651.04" [ref=e838]
              - gridcell "Omega FCU" [ref=e839]
              - gridcell "27" [ref=e840]
              - gridcell "Debit to Checking" [ref=e841]
              - gridcell "03/13/2026" [ref=e842]
              - gridcell [ref=e843]
              - gridcell [ref=e844]
              - gridcell [ref=e845]
              - gridcell [ref=e846]
              - gridcell [ref=e847]:
                - link " View" [ref=e848] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e849]: 
                  - text: View
              - gridcell "09/24/2026 9:51 AM EDT" [ref=e850]:
                - text: 09/24/2026
                - generic [ref=e851]: 9:51 AM EDT
              - gridcell [ref=e852]
              - gridcell "F.I ACH&CHK User" [ref=e853]
              - gridcell [ref=e854]
              - gridcell "09/24/2026 9:51 AM EDT" [ref=e855]:
                - text: 09/24/2026
                - generic [ref=e856]: 9:51 AM EDT
              - gridcell [ref=e857]
              - gridcell [ref=e858]
            - row [ref=e859]:
              - gridcell [ref=e860]:
                - checkbox "Select a row" [ref=e863] [cursor=pointer]
              - gridcell "  Yes" [ref=e864]:
                - generic [ref=e865]:  
                - text: "Yes"
              - gridcell "9777" [ref=e866]
              - gridcell "Completed[Manual Decision]" [ref=e867]:
                - text: Completed
                - generic [ref=e868]: "[Manual Decision]"
              - gridcell "PJ_BC_Carshop" [ref=e869]
              - gridcell "ACH" [ref=e870]
              - gridcell [ref=e871]:
                - link " Return" [ref=e872] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e873]: 
                  - text: Return
              - gridcell [ref=e874]
              - gridcell "122199983" [ref=e875]
              - gridcell [ref=e876]
              - gridcell "Account_Carshop" [ref=e877]
              - gridcell "WEB" [ref=e878]
              - gridcell "$2,442.00" [ref=e879]
              - gridcell "ACH Originator" [ref=e880]
              - gridcell "27" [ref=e881]
              - gridcell "Debit to Checking" [ref=e882]
              - gridcell "09/23/2026" [ref=e883]
              - gridcell [ref=e884]
              - gridcell [ref=e885]
              - gridcell [ref=e886]
              - gridcell [ref=e887]
              - gridcell [ref=e888]:
                - link " View" [ref=e889] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e890]: 
                  - text: View
              - gridcell "09/23/2026 10:39 PM EDT" [ref=e891]:
                - text: 09/23/2026
                - generic [ref=e892]: 10:39 PM EDT
              - gridcell [ref=e893]
              - gridcell "Chromium Automation" [ref=e894]
              - gridcell [ref=e895]
              - gridcell "09/23/2026 11:41 PM EDT" [ref=e896]:
                - text: 09/23/2026
                - generic [ref=e897]: 11:41 PM EDT
              - gridcell [ref=e898]
              - gridcell [ref=e899]
            - row [ref=e900]:
              - gridcell [ref=e901]:
                - checkbox "Select a row" [ref=e904] [cursor=pointer]
              - gridcell "  Yes" [ref=e905]:
                - generic [ref=e906]:  
                - text: "Yes"
              - gridcell "9778" [ref=e907]
              - gridcell "Completed[Manual Decision]" [ref=e908]:
                - text: Completed
                - generic [ref=e909]: "[Manual Decision]"
              - gridcell "PJ_BC_Carshop" [ref=e910]
              - gridcell "ACH" [ref=e911]
              - gridcell [ref=e912]:
                - link " Return" [ref=e913] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e914]: 
                  - text: Return
              - gridcell [ref=e915]
              - gridcell "102000979" [ref=e916]
              - gridcell [ref=e917]
              - gridcell "Account_Carshop" [ref=e918]
              - gridcell "WEB" [ref=e919]
              - gridcell "$2,443.50" [ref=e920]
              - gridcell "ACH Originator" [ref=e921]
              - gridcell "27" [ref=e922]
              - gridcell "Debit to Checking" [ref=e923]
              - gridcell "09/23/2026" [ref=e924]
              - gridcell [ref=e925]
              - gridcell [ref=e926]
              - gridcell [ref=e927]
              - gridcell [ref=e928]
              - gridcell [ref=e929]:
                - link " View" [ref=e930] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e931]: 
                  - text: View
              - gridcell "09/23/2026 10:39 PM EDT" [ref=e932]:
                - text: 09/23/2026
                - generic [ref=e933]: 10:39 PM EDT
              - gridcell [ref=e934]
              - gridcell "Chromium Automation" [ref=e935]
              - gridcell [ref=e936]
              - gridcell "09/23/2026 11:41 PM EDT" [ref=e937]:
                - text: 09/23/2026
                - generic [ref=e938]: 11:41 PM EDT
              - gridcell [ref=e939]
              - gridcell [ref=e940]
            - row [ref=e941]:
              - gridcell [ref=e942]:
                - checkbox "Select a row" [ref=e945] [cursor=pointer]
              - gridcell "  Yes" [ref=e946]:
                - generic [ref=e947]:  
                - text: "Yes"
              - gridcell "9779" [ref=e948]
              - gridcell "Completed[Manual Decision]" [ref=e949]:
                - text: Completed
                - generic [ref=e950]: "[Manual Decision]"
              - gridcell "PJ_BC_Carshop" [ref=e951]
              - gridcell "ACH" [ref=e952]
              - gridcell [ref=e953]:
                - link " Return" [ref=e954] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e955]: 
                  - text: Return
              - gridcell [ref=e956]
              - gridcell "122199983" [ref=e957]
              - gridcell [ref=e958]
              - gridcell "Account_Carshop" [ref=e959]
              - gridcell "WEB" [ref=e960]
              - gridcell "$7,963.00" [ref=e961]
              - gridcell "ACH Originator" [ref=e962]
              - gridcell "27" [ref=e963]
              - gridcell "Debit to Checking" [ref=e964]
              - gridcell "09/23/2026" [ref=e965]
              - gridcell [ref=e966]
              - gridcell [ref=e967]
              - gridcell [ref=e968]
              - gridcell [ref=e969]
              - gridcell [ref=e970]:
                - link " View" [ref=e971] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e972]: 
                  - text: View
              - gridcell "09/23/2026 10:40 PM EDT" [ref=e973]:
                - text: 09/23/2026
                - generic [ref=e974]: 10:40 PM EDT
              - gridcell [ref=e975]
              - gridcell "Chromium Automation" [ref=e976]
              - gridcell [ref=e977]
              - gridcell "09/23/2026 11:41 PM EDT" [ref=e978]:
                - text: 09/23/2026
                - generic [ref=e979]: 11:41 PM EDT
              - gridcell [ref=e980]
              - gridcell [ref=e981]
            - row [ref=e982]:
              - gridcell [ref=e983]:
                - checkbox "Select a row" [ref=e986] [cursor=pointer]
              - gridcell "  Yes" [ref=e987]:
                - generic [ref=e988]:  
                - text: "Yes"
              - gridcell "9780" [ref=e989]
              - gridcell "Completed[Manual Decision]" [ref=e990]:
                - text: Completed
                - generic [ref=e991]: "[Manual Decision]"
              - gridcell "PJ_BC_Carshop" [ref=e992]
              - gridcell "ACH" [ref=e993]
              - gridcell [ref=e994]:
                - link " Return" [ref=e995] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e996]: 
                  - text: Return
              - gridcell [ref=e997]
              - gridcell "102000979" [ref=e998]
              - gridcell [ref=e999]
              - gridcell "Account_Carshop" [ref=e1000]
              - gridcell "WEB" [ref=e1001]
              - gridcell "$7,964.50" [ref=e1002]
              - gridcell "ACH Originator" [ref=e1003]
              - gridcell "27" [ref=e1004]
              - gridcell "Debit to Checking" [ref=e1005]
              - gridcell "09/23/2026" [ref=e1006]
              - gridcell [ref=e1007]
              - gridcell [ref=e1008]
              - gridcell [ref=e1009]
              - gridcell [ref=e1010]
              - gridcell [ref=e1011]:
                - link " View" [ref=e1012] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e1013]: 
                  - text: View
              - gridcell "09/23/2026 10:40 PM EDT" [ref=e1014]:
                - text: 09/23/2026
                - generic [ref=e1015]: 10:40 PM EDT
              - gridcell [ref=e1016]
              - gridcell "Chromium Automation" [ref=e1017]
              - gridcell [ref=e1018]
              - gridcell "09/23/2026 11:41 PM EDT" [ref=e1019]:
                - text: 09/23/2026
                - generic [ref=e1020]: 11:41 PM EDT
              - gridcell [ref=e1021]
              - gridcell [ref=e1022]
            - row [ref=e1023]:
              - gridcell [ref=e1024]:
                - checkbox "Select a row" [ref=e1027] [cursor=pointer]
              - gridcell "  Yes" [ref=e1028]:
                - generic [ref=e1029]:  
                - text: "Yes"
              - gridcell "9781" [ref=e1030]
              - gridcell "Completed[Manual Decision]" [ref=e1031]:
                - text: Completed
                - generic [ref=e1032]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e1033]
              - gridcell "ACH" [ref=e1034]
              - gridcell [ref=e1035]:
                - link " Return" [ref=e1036] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e1037]: 
                  - text: Return
              - gridcell "PJ456!" [ref=e1038]
              - gridcell "122199983" [ref=e1039]
              - gridcell [ref=e1040]
              - gridcell "Account_Boutique" [ref=e1041]
              - gridcell "WEB" [ref=e1042]
              - gridcell "$2,054.00" [ref=e1043]
              - gridcell "ACH Originator" [ref=e1044]
              - gridcell "27" [ref=e1045]
              - gridcell "Debit to Checking" [ref=e1046]
              - gridcell "09/23/2026" [ref=e1047]
              - gridcell [ref=e1048]
              - gridcell [ref=e1049]
              - gridcell [ref=e1050]
              - gridcell [ref=e1051]
              - gridcell [ref=e1052]:
                - link " View" [ref=e1053] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e1054]: 
                  - text: View
              - gridcell "09/23/2026 10:40 PM EDT" [ref=e1055]:
                - text: 09/23/2026
                - generic [ref=e1056]: 10:40 PM EDT
              - gridcell [ref=e1057]
              - gridcell "Chromium Automation" [ref=e1058]
              - gridcell [ref=e1059]
              - gridcell "09/23/2026 11:41 PM EDT" [ref=e1060]:
                - text: 09/23/2026
                - generic [ref=e1061]: 11:41 PM EDT
              - gridcell [ref=e1062]
              - gridcell [ref=e1063]
            - row [ref=e1064]:
              - gridcell [ref=e1065]:
                - checkbox "Select a row" [ref=e1068] [cursor=pointer]
              - gridcell "  Yes" [ref=e1069]:
                - generic [ref=e1070]:  
                - text: "Yes"
              - gridcell "9782" [ref=e1071]
              - gridcell "Completed[Manual Decision]" [ref=e1072]:
                - text: Completed
                - generic [ref=e1073]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e1074]
              - gridcell "ACH" [ref=e1075]
              - gridcell [ref=e1076]:
                - link " Return" [ref=e1077] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e1078]: 
                  - text: Return
              - gridcell "PJ456!" [ref=e1079]
              - gridcell "102000979" [ref=e1080]
              - gridcell [ref=e1081]
              - gridcell "Account_Boutique" [ref=e1082]
              - gridcell "WEB" [ref=e1083]
              - gridcell "$2,055.50" [ref=e1084]
              - gridcell "ACH Originator" [ref=e1085]
              - gridcell "27" [ref=e1086]
              - gridcell "Debit to Checking" [ref=e1087]
              - gridcell "09/23/2026" [ref=e1088]
              - gridcell [ref=e1089]
              - gridcell [ref=e1090]
              - gridcell [ref=e1091]
              - gridcell [ref=e1092]
              - gridcell [ref=e1093]:
                - link " View" [ref=e1094] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e1095]: 
                  - text: View
              - gridcell "09/23/2026 10:40 PM EDT" [ref=e1096]:
                - text: 09/23/2026
                - generic [ref=e1097]: 10:40 PM EDT
              - gridcell [ref=e1098]
              - gridcell "Chromium Automation" [ref=e1099]
              - gridcell [ref=e1100]
              - gridcell "09/23/2026 11:41 PM EDT" [ref=e1101]:
                - text: 09/23/2026
                - generic [ref=e1102]: 11:41 PM EDT
              - gridcell [ref=e1103]
              - gridcell [ref=e1104]
            - row [ref=e1105]:
              - gridcell [ref=e1106]:
                - checkbox "Select a row" [ref=e1109] [cursor=pointer]
              - gridcell "  Yes" [ref=e1110]:
                - generic [ref=e1111]:  
                - text: "Yes"
              - gridcell "9783" [ref=e1112]
              - gridcell "Completed[Manual Decision]" [ref=e1113]:
                - text: Completed
                - generic [ref=e1114]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e1115]
              - gridcell "ACH" [ref=e1116]
              - gridcell [ref=e1117]:
                - link " Return" [ref=e1118] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e1119]: 
                  - text: Return
              - gridcell "PJ456!" [ref=e1120]
              - gridcell "122199983" [ref=e1121]
              - gridcell [ref=e1122]
              - gridcell "Account_Boutique" [ref=e1123]
              - gridcell "WEB" [ref=e1124]
              - gridcell "$5,576.00" [ref=e1125]
              - gridcell "ACH Originator" [ref=e1126]
              - gridcell "27" [ref=e1127]
              - gridcell "Debit to Checking" [ref=e1128]
              - gridcell "09/23/2026" [ref=e1129]
              - gridcell [ref=e1130]
              - gridcell [ref=e1131]
              - gridcell [ref=e1132]
              - gridcell [ref=e1133]
              - gridcell [ref=e1134]:
                - link " View" [ref=e1135] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e1136]: 
                  - text: View
              - gridcell "09/23/2026 10:41 PM EDT" [ref=e1137]:
                - text: 09/23/2026
                - generic [ref=e1138]: 10:41 PM EDT
              - gridcell [ref=e1139]
              - gridcell "Chromium Automation" [ref=e1140]
              - gridcell [ref=e1141]
              - gridcell "09/23/2026 11:41 PM EDT" [ref=e1142]:
                - text: 09/23/2026
                - generic [ref=e1143]: 11:41 PM EDT
              - gridcell [ref=e1144]
              - gridcell [ref=e1145]
            - row [ref=e1146]:
              - gridcell [ref=e1147]:
                - checkbox "Select a row" [ref=e1150] [cursor=pointer]
              - gridcell "  Yes" [ref=e1151]:
                - generic [ref=e1152]:  
                - text: "Yes"
              - gridcell "9784" [ref=e1153]
              - gridcell "Completed[Manual Decision]" [ref=e1154]:
                - text: Completed
                - generic [ref=e1155]: "[Manual Decision]"
              - gridcell "PJ_BC_Boutique" [ref=e1156]
              - gridcell "ACH" [ref=e1157]
              - gridcell [ref=e1158]:
                - link " Return" [ref=e1159] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e1160]: 
                  - text: Return
              - gridcell "PJ456!" [ref=e1161]
              - gridcell "102000979" [ref=e1162]
              - gridcell [ref=e1163]
              - gridcell "Account_Boutique" [ref=e1164]
              - gridcell "WEB" [ref=e1165]
              - gridcell "$5,577.50" [ref=e1166]
              - gridcell "ACH Originator" [ref=e1167]
              - gridcell "27" [ref=e1168]
              - gridcell "Debit to Checking" [ref=e1169]
              - gridcell "09/23/2026" [ref=e1170]
              - gridcell [ref=e1171]
              - gridcell [ref=e1172]
              - gridcell [ref=e1173]
              - gridcell [ref=e1174]
              - gridcell [ref=e1175]:
                - link " View" [ref=e1176] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=e1177]: 
                  - text: View
              - gridcell "09/23/2026 10:41 PM EDT" [ref=e1178]:
                - text: 09/23/2026
                - generic [ref=e1179]: 10:41 PM EDT
              - gridcell [ref=e1180]
              - gridcell "Chromium Automation" [ref=e1181]
              - gridcell [ref=e1182]
              - gridcell "09/23/2026 11:41 PM EDT" [ref=e1183]:
                - text: 09/23/2026
                - generic [ref=e1184]: 11:41 PM EDT
              - gridcell [ref=e1185]
              - gridcell [ref=e1186]
        - application "Page navigation, page 1 of 23" [ref=e1187]:
          - generic [ref=e1188]:
            - button "Go to the first page" [disabled]
            - button "Go to the previous page" [disabled]
            - generic [ref=e1189]:
              - text: Page
              - spinbutton "Select a page" [ref=e1191]: "1"
              - text: of 23
            - button "Go to the next page" [ref=e1192] [cursor=pointer]
            - button "Go to the last page" [ref=e1196] [cursor=pointer]
          - generic [ref=e1200]: 1 - 20 of 444 items
    - contentinfo [ref=e1201]:
      - generic [ref=e1202]:
        - text: FI Playwright Automation
        - generic [ref=e1203]: "[uat-release]"
      - generic [ref=e1204]:
        - text: © Copyright Advanced Fraud Solutions 2005-2026 |
        - generic [ref=e1205]: All Rights Reserved
        - text: "|"
        - link "Privacy Policy" [ref=e1207] [cursor=pointer]:
          - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  394 |         await this.page
  395 |             .locator('a[href*="/exceptions/history"]')
  396 |             .filter({ visible: true })
  397 |             .first()
  398 |             .click();
  399 |     }
  400 | 
  401 |     get exceptionHistoryTypeFilterMenuButton() {
  402 |         return this.page.getByRole('button', { name: 'Type column filter menu settings', exact: true });
  403 |     }
  404 | 
  405 |     get exceptionHistoryFilterApplyButton() {
  406 |         return this.page.getByRole('button', { name: 'Filter', exact: true });
  407 |     }
  408 | 
  409 |     get exceptionHistoryFilterClearButton() {
  410 |         return this.page.getByRole('button', { name: 'Clear', exact: true });
  411 |     }
  412 | 
  413 |     get exceptionHistoryGridRows() {
  414 |         return this.page.locator('tr.k-master-row.k-table-row');
  415 |     }
  416 | 
  417 |     async navigateToExceptionHistory() {
  418 |         await this.page.goto('/exceptions/history');
  419 |         await this.page.waitForLoadState('domcontentloaded');
  420 |         // A saved filter marked as the account default auto-applies on load and pre-filters the
  421 |         // grid; reset it to "[No Filter]" so every test starts from the full, unfiltered result set.
  422 |         await this.ensureNoExceptionHistorySavedFilter();
  423 |         await this.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 15000 });
  424 |     }
  425 | 
  426 |     // The Saved Filters dropdown is empty-valued ('') for "[No Filter]"; any other value is an
  427 |     // applied preset. If a default preset auto-applied on load, switch back to "[No Filter]" and
  428 |     // wait for the grid to re-bind to the unfiltered set. No-op when nothing is applied.
  429 |     async ensureNoExceptionHistorySavedFilter(): Promise<void> {
  430 |         await this.historySavedFiltersDropdown.waitFor({ state: 'visible', timeout: 15000 });
  431 |         // Let the grid settle (data rows or the no-records row) so the dropdown reflects any auto-applied default.
  432 |         await this.exceptionHistoryGridRows.first().or(this.historyNoRecordsRow.first())
  433 |             .waitFor({ state: 'visible', timeout: 20000 });
  434 |         if ((await this.historySavedFiltersDropdown.inputValue()) === '') {
  435 |             return;
  436 |         }
  437 |         await this.historySavedFiltersDropdown.selectOption('');
  438 |         await this.exceptionHistoryGridRows.first().or(this.historyNoRecordsRow.first())
  439 |             .waitFor({ state: 'visible', timeout: 20000 });
  440 |     }
  441 | 
  442 |     async openExceptionHistoryTypeFilter() {
  443 |         await this.exceptionHistoryTypeFilterMenuButton.waitFor({ state: 'visible', timeout: 15000 });
  444 |         await this.exceptionHistoryTypeFilterMenuButton.click();
  445 |         await this.page.locator('.k-grid-filter-popup[aria-label="Type Filter Menu"]').waitFor({ state: 'visible', timeout: 10000 });
  446 |     }
  447 | 
  448 |     private getExceptionHistoryFilterPopup(columnName: string) {
  449 |         return this.page.locator(`.k-grid-filter-popup[aria-label="${columnName} Filter Menu"]`);
  450 |     }
  451 | 
  452 |     private getTypeFilterPopup() {
  453 |         return this.getExceptionHistoryFilterPopup('Type');
  454 |     }
  455 | 
  456 |     async openExceptionHistoryColumnFilter(columnName: string) {
  457 |         const filterButton = this.page.getByRole('button', { name: `${columnName} column filter menu settings`, exact: true });
  458 |         await filterButton.waitFor({ state: 'visible', timeout: 15000 });
  459 |         await filterButton.click();
  460 |         await this.getExceptionHistoryFilterPopup(columnName).waitFor({ state: 'visible', timeout: 10000 });
  461 |     }
  462 | 
  463 |     // After a column filter is applied, Kendo/Blazor re-binds the grid asynchronously and keeps the
  464 |     // pre-filter rows in the DOM until the update lands, so a caller that reads immediately gets
  465 |     // stale, unfiltered rows. Read the target column in a single atomic pass (evaluateAll) so we
  466 |     // never catch it mid-detach, and report whether every visible value matches (or the grid emptied).
  467 |     private async exceptionHistoryColumnMatches(colIndex: number, matcher: (value: string) => boolean): Promise<boolean> {
  468 |         if (await this.historyNoRecordsRow.first().isVisible().catch(() => false)) {
  469 |             return true;
  470 |         }
  471 |         const values = await this.exceptionHistoryGridRows
  472 |             .locator(`td:nth-child(${colIndex + 1})`)
  473 |             .evaluateAll((nodes) => nodes.map((node) => (node.textContent || '').replace(/\s+/g, ' ').trim()).filter(Boolean))
  474 |             .catch(() => [] as string[]);
  475 |         return values.length > 0 && values.every(matcher);
  476 |     }
  477 | 
  478 |     // Poll the target column until every visible value matches the filter — this both waits out the
  479 |     // re-bind AND proves the filter actually took. Returns whether it converged within the timeout.
  480 |     private async exceptionHistoryColumnConverges(headerText: string, matcher: (value: string) => boolean, timeout = 15000): Promise<boolean> {
  481 |         const colIndex = await this.exceptionHistoryColumnIndex(headerText);
  482 |         try {
  483 |             await expect.poll(async () => this.exceptionHistoryColumnMatches(colIndex, matcher),
  484 |                 { timeout, intervals: [300, 300, 500, 700, 1000, 1000] }).toBe(true);
  485 |             return true;
  486 |         } catch {
  487 |             return false;
  488 |         }
  489 |     }
  490 | 
  491 |     private async waitForExceptionHistoryColumnFilter(headerText: string, matcher: (value: string) => boolean, timeout = 15000): Promise<void> {
  492 |         const colIndex = await this.exceptionHistoryColumnIndex(headerText);
  493 |         await expect.poll(async () => this.exceptionHistoryColumnMatches(colIndex, matcher),
> 494 |             { timeout, intervals: [300, 300, 500, 700, 1000, 1000] }).toBe(true);
      |                                                                       ^ Error: expect(received).toBe(expected) // Object.is equality
  495 |     }
  496 | 
  497 |     async setExceptionHistoryTypeFilter(typeText: 'Check' | 'ACH' | 'Teller') {
  498 |         const options: Array<'Check' | 'ACH' | 'Teller'> = ['Check', 'ACH', 'Teller'];
  499 |         // Blazor Server occasionally drops a checkbox's @onchange over SignalR before the Filter
  500 |         // click, so the server filters on a stale (all-types) selection and the grid never narrows.
  501 |         // Re-open and re-apply once if the Type column doesn't converge, instead of failing outright.
  502 |         const attempts = 2;
  503 |         for (let attempt = 1; attempt <= attempts; attempt++) {
  504 |             await this.openExceptionHistoryTypeFilter();
  505 |             const popup = this.getTypeFilterPopup();
  506 | 
  507 |             for (const option of options) {
  508 |                 await popup.locator(`input#${option}`).setChecked(option === typeText);
  509 |             }
  510 |             // Confirm the selection registered in the DOM before applying it.
  511 |             await expect(popup.locator(`input#${typeText}`)).toBeChecked();
  512 | 
  513 |             await popup.getByRole('button', { name: 'Filter', exact: true }).click();
  514 | 
  515 |             const converged = await this.exceptionHistoryColumnConverges(
  516 |                 'Type',
  517 |                 (value) => value === typeText,
  518 |                 attempt < attempts ? 8000 : 15000,
  519 |             );
  520 |             if (converged) {
  521 |                 return;
  522 |             }
  523 |         }
  524 | 
  525 |         throw new Error(`Exception History Type filter did not narrow the grid to "${typeText}" after ${attempts} attempts.`);
  526 |     }
  527 | 
  528 |     async applyExceptionHistoryMultiSelectFilter(columnName: string, optionText: string) {
  529 |         await this.openExceptionHistoryColumnFilter(columnName);
  530 |         const popup = this.getExceptionHistoryFilterPopup(columnName);
  531 |         const selectAll = popup.getByLabel('Select All', { exact: true });
  532 | 
  533 |         if (await selectAll.isVisible().catch(() => false)) {
  534 |             await selectAll.setChecked(false);
  535 |         }
  536 | 
  537 |         const checkedOptions = popup.locator('.k-filter-menu-container input[type="checkbox"]:checked');
  538 |         while ((await checkedOptions.count()) > 0) {
  539 |             await checkedOptions.first().setChecked(false);
  540 |         }
  541 | 
  542 |         await popup.getByLabel(optionText, { exact: true }).check();
  543 |         await popup.getByRole('button', { name: 'Filter', exact: true }).click();
  544 |         // Wait for the re-bind and confirm every visible cell in this column now equals the picked option.
  545 |         await this.waitForExceptionHistoryColumnFilter(columnName, (value) => value === optionText);
  546 |     }
  547 | 
  548 |     async applyExceptionHistoryTextFilter(columnName: string, filterValue: string) {
  549 |         await this.openExceptionHistoryColumnFilter(columnName);
  550 |         const popup = this.getExceptionHistoryFilterPopup(columnName);
  551 |         const filterInput = popup.locator('.k-textbox input.k-input-inner').first();
  552 |         await filterInput.fill(filterValue);
  553 |         await popup.getByRole('button', { name: 'Filter', exact: true }).click();
  554 |         // Wait for the re-bind and confirm every visible cell in this column now contains the filter text.
  555 |         await this.waitForExceptionHistoryColumnFilter(columnName, (value) => value.includes(filterValue));
  556 |     }
  557 | 
  558 |     // Read the Business Client of the first data row. Aligned by visible column position
  559 |     // (header order == row cell order) rather than data-col-index, which Kendo offsets by a
  560 |     // hidden column. Callers filter on this so the value is guaranteed present on the current
  561 |     // FI — a hardcoded client can be absent on some tenants and yield a 0-row saved filter.
  562 |     async getFirstExceptionHistoryBusinessClient(): Promise<string> {
  563 |         await this.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 15000 });
  564 |         const headerTexts = await this.historyDataGrid.getByRole('columnheader').allInnerTexts();
  565 |         const colIndex = headerTexts.findIndex((text) => text.trim().startsWith('Business Client'));
  566 |         if (colIndex < 0) {
  567 |             throw new Error('Business Client column not found in the Exception History grid.');
  568 |         }
  569 |         const value = (await this.exceptionHistoryGridRows.first().locator('td').nth(colIndex).innerText()).trim();
  570 |         if (!value) {
  571 |             throw new Error('First Exception History row has an empty Business Client value.');
  572 |         }
  573 |         return value;
  574 |     }
  575 | 
  576 |     async clearExceptionHistoryTypeFilter() {
  577 |         await this.openExceptionHistoryTypeFilter();
  578 |         await this.getTypeFilterPopup().getByRole('button', { name: 'Clear', exact: true }).click();
  579 |         await this.exceptionHistoryGridRows.first().waitFor({ state: 'visible', timeout: 15000 });
  580 |     }
  581 | 
  582 |     async getExceptionHistoryTypeValues(limit = 10) {
  583 |         const values = await this.getExceptionHistoryColumnValues(6, limit);
  584 | 
  585 |         return values.filter(Boolean);
  586 |     }
  587 | 
  588 |     async getExceptionHistoryColumnValues(colIndex: number, limit = 10) {
  589 |         return this.page
  590 |             .locator(`tr.k-master-row.k-table-row td[data-col-index="${colIndex}"]`)
  591 |             .evaluateAll((nodes, payload) =>
  592 |                 nodes
  593 |                     .slice(0, Number(payload))
  594 |                     .map((node) => node.textContent?.replace(/\n/g, '').trim() || ''),
```