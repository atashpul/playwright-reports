# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: specs\Smoke\5-PresentedChecksSmoke.spec.ts >> Presented Checks — Smoke >> Saved Filters >> Default Filter >> Default filter auto-applies after logout and re-login
- Location: specs\Smoke\5-PresentedChecksSmoke.spec.ts:184:13

# Error details

```
Error: expect(received).not.toContain(expected) // indexOf

Expected value: not "SMK_Default_1791195607068"
Received array:     ["[No Filter]", "SMK_Default_1791195607068"]

Call Log:
- Timeout 10000ms exceeded while waiting on the predicate
```

# Page snapshot

```yaml
- generic [active] [ref=f5e1]:
  - banner [ref=f5e2]:
    - generic [ref=f5e3]:
      - link [ref=f5e4] [cursor=pointer]:
        - /url: /
      - text:              
      - generic [ref=f5e7]:
        - link "  Home" [ref=f5e8] [cursor=pointer]:
          - /url: /
          - generic [ref=f5e9]:  
          - generic [ref=f5e11]: Home
        - link "  Issued Checks" [ref=f5e13] [cursor=pointer]:
          - /url: /issued-checks
          - generic [ref=f5e14]:  
          - generic [ref=f5e16]: Issued Checks
        - link "  Presented Checks" [ref=f5e18] [cursor=pointer]:
          - /url: /paid-checks
          - generic [ref=f5e19]:  
          - generic [ref=f5e21]: Presented Checks
        - link "  Teller" [ref=f5e23] [cursor=pointer]:
          - /url: /teller
          - generic [ref=f5e24]:  
          - generic [ref=f5e26]: Teller
        - link "  ACH" [ref=f5e28] [cursor=pointer]:
          - /url: /paid-ach
          - generic [ref=f5e29]:  
          - generic [ref=f5e31]: ACH
        - link "  Exceptions" [ref=f5e33] [cursor=pointer]:
          - /url: /exceptions
          - generic [ref=f5e34]:  
          - generic [ref=f5e36]: Exceptions
        - link "  Settings" [ref=f5e38] [cursor=pointer]:
          - /url: /client-admin
          - generic [ref=f5e39]:  
          - generic [ref=f5e41]: Settings
      - generic [ref=f5e44]:
        - button "  F.I ACH&CHK User" [ref=f5e45] [cursor=pointer]:
          - generic [ref=f5e46]:  
          - generic [ref=f5e48]: F.I ACH&CHK User
        - text:  
  - generic [ref=f5e50]:
    - generic [ref=f5e52]:
      - generic [ref=f5e54]:
        - list [ref=f5e55]:
          - listitem [ref=f5e56]:
            - link " " [ref=f5e57] [cursor=pointer]:
              - /url: /
          - listitem [ref=f5e59]:
            - link "Presented Checks" [ref=f5e60] [cursor=pointer]:
              - /url: /paid-checks
        - text:   +
        - group [ref=f5e62]:
          - link " Uploaded Checks" [ref=f5e63] [cursor=pointer]:
            - /url: /paid-checks/uploads
            - generic [ref=f5e64]: 
            - text: Uploaded Checks
          - link "+ Add Check" [ref=f5e65] [cursor=pointer]:
            - /url: /paid-checks/check
            - generic [ref=f5e66]: +
            - text: Add Check
      - generic [ref=f5e68]:
        - toolbar "Grid toolbar" [ref=f5e69]:
          - generic [ref=f5e70]:
            - generic [ref=f5e71]:
              - generic [ref=f5e72]:
                - generic [ref=f5e73]: Page Size
                - combobox [ref=f5e75]:
                  - option "10"
                  - option "20" [selected]
                  - option "50"
                  - option "100"
              - button "Excel" [ref=f5e76] [cursor=pointer]
              - textbox "Search..." [ref=f5e83]
            - generic [ref=f5e85]:
              - generic [ref=f5e86]: Saved Filters
              - combobox [ref=f5e88]:
                - option "[No Filter]" [selected]
              - button "+" [ref=f5e90] [cursor=pointer]
        - grid "Data table" [ref=f5e92]:
          - rowgroup [ref=f5e111]:
            - row [ref=f5e112]:
              - columnheader "ID ID column filter menu settings" [ref=f5e113]:
                - generic [ref=f5e114]:
                  - generic [ref=f5e115] [cursor=pointer]: ID
                  - button "ID column filter menu settings" [ref=f5e117]
              - columnheader "Status Status column filter menu settings" [ref=f5e122]:
                - generic [ref=f5e123]:
                  - generic [ref=f5e124] [cursor=pointer]: Status
                  - button "Status column filter menu settings" [ref=f5e126]
              - columnheader "Decision Decision column filter menu settings" [ref=f5e131]:
                - generic [ref=f5e132]:
                  - generic [ref=f5e133] [cursor=pointer]: Decision
                  - button "Decision column filter menu settings" [ref=f5e135]
              - columnheader "Client Client column filter menu settings" [ref=f5e140]:
                - generic [ref=f5e141]:
                  - generic [ref=f5e142] [cursor=pointer]: Client
                  - button "Client column filter menu settings" [ref=f5e144]
              - columnheader "Account Account column filter menu settings" [ref=f5e149]:
                - generic [ref=f5e150]:
                  - generic [ref=f5e151] [cursor=pointer]: Account
                  - button "Account column filter menu settings" [ref=f5e153]
              - columnheader "Reference ID Reference ID column filter menu settings" [ref=f5e158]:
                - generic [ref=f5e159]:
                  - generic [ref=f5e160] [cursor=pointer]: Reference ID
                  - button "Reference ID column filter menu settings" [ref=f5e162]
              - 'columnheader "Routing # Routing # column filter menu settings" [ref=f5e167]':
                - generic [ref=f5e168]:
                  - generic [ref=f5e169] [cursor=pointer]: "Routing #"
                  - 'button "Routing # column filter menu settings" [ref=f5e171]'
              - 'columnheader "Account # Account # column filter menu settings" [ref=f5e176]':
                - generic [ref=f5e177]:
                  - generic [ref=f5e178] [cursor=pointer]: "Account #"
                  - 'button "Account # column filter menu settings" [ref=f5e180]'
              - 'columnheader "Check # Check # column filter menu settings" [ref=f5e185]':
                - generic [ref=f5e186]:
                  - generic [ref=f5e187] [cursor=pointer]: "Check #"
                  - 'button "Check # column filter menu settings" [ref=f5e189]'
              - columnheader "Amount Amount column filter menu settings" [ref=f5e194]:
                - generic [ref=f5e195]:
                  - generic [ref=f5e196] [cursor=pointer]: Amount
                  - button "Amount column filter menu settings" [ref=f5e198]
              - columnheader "Presented Date Presented Date column filter menu settings" [ref=f5e203]:
                - generic [ref=f5e204]:
                  - generic [ref=f5e205] [cursor=pointer]: Presented Date
                  - button "Presented Date column filter menu settings" [ref=f5e207]
              - columnheader "Payee Name Payee Name column filter menu settings" [ref=f5e212]:
                - generic [ref=f5e213]:
                  - generic [ref=f5e214] [cursor=pointer]: Payee Name
                  - button "Payee Name column filter menu settings" [ref=f5e216]
              - columnheader "Check Image" [ref=f5e221]
              - columnheader "Issued Check Data" [ref=f5e223]
              - columnheader "Added By Added By column filter menu settings" [ref=f5e228]:
                - generic [ref=f5e229]:
                  - generic [ref=f5e230] [cursor=pointer]: Added By
                  - button "Added By column filter menu settings" [ref=f5e232]
              - columnheader "Edit" [ref=f5e237]
              - columnheader "Change Log" [ref=f5e239]
          - rowgroup [ref=f5e263]:
            - row [ref=f5e264]:
              - gridcell "35996" [ref=f5e265]
              - gridcell "Completed[Manual Decision]" [ref=f5e266]:
                - text: Completed
                - generic [ref=f5e267]: "[Manual Decision]"
              - gridcell [ref=f5e268]:
                - link " Return " [ref=f5e269] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35996&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e270]: 
                  - text: Return
                  - generic [ref=f5e271]: 
              - gridcell "PJ_BC_Salon" [ref=f5e272]
              - gridcell "Account_Salon" [ref=f5e273]
              - gridcell [ref=f5e274]
              - gridcell "122199983" [ref=f5e275]
              - gridcell "05139491" [ref=f5e276]
              - gridcell "733103" [ref=f5e277]
              - gridcell "$250.00" [ref=f5e278]
              - gridcell "09/23/2026" [ref=f5e279]
              - gridcell [ref=f5e280]
              - gridcell [ref=f5e281]
              - gridcell [ref=f5e282]
              - gridcell [ref=f5e283]:
                - link "pw2_1790217849868_PresentedCheck_FixedLength.txt" [ref=f5e284] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17771
              - gridcell [ref=f5e285]:
                - link " Edit" [ref=f5e286] [cursor=pointer]:
                  - /url: /paid-checks/check/35996
                  - generic [ref=f5e287]: 
                  - text: Edit
                - link " Delete" [ref=f5e288] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e289]: 
                  - text: Delete
              - gridcell [ref=f5e290]:
                - link "View " [ref=f5e291] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35996&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e292]: 
            - row [ref=f5e293]:
              - gridcell "35995" [ref=f5e294]
              - gridcell "Completed[Manual Decision]" [ref=f5e295]:
                - text: Completed
                - generic [ref=f5e296]: "[Manual Decision]"
              - gridcell [ref=f5e297]:
                - link " Return " [ref=f5e298] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35995&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e299]: 
                  - text: Return
                  - generic [ref=f5e300]: 
              - gridcell "PJ_BC_Salon" [ref=f5e301]
              - gridcell "Account_Salon" [ref=f5e302]
              - gridcell [ref=f5e303]
              - gridcell "122199983" [ref=f5e304]
              - gridcell "05139491" [ref=f5e305]
              - gridcell "733102" [ref=f5e306]
              - gridcell "$531.00" [ref=f5e307]
              - gridcell "09/23/2026" [ref=f5e308]
              - gridcell [ref=f5e309]
              - gridcell [ref=f5e310]
              - gridcell [ref=f5e311]
              - gridcell [ref=f5e312]:
                - link "pw2_1790217849868_PresentedCheck_FixedLength.txt" [ref=f5e313] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17771
              - gridcell [ref=f5e314]:
                - link " Edit" [ref=f5e315] [cursor=pointer]:
                  - /url: /paid-checks/check/35995
                  - generic [ref=f5e316]: 
                  - text: Edit
                - link " Delete" [ref=f5e317] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e318]: 
                  - text: Delete
              - gridcell [ref=f5e319]:
                - link "View " [ref=f5e320] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35995&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e321]: 
            - row [ref=f5e322]:
              - gridcell "35994" [ref=f5e323]
              - gridcell "Completed[Manual Decision]" [ref=f5e324]:
                - text: Completed
                - generic [ref=f5e325]: "[Manual Decision]"
              - gridcell [ref=f5e326]:
                - link " Return " [ref=f5e327] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35994&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e328]: 
                  - text: Return
                  - generic [ref=f5e329]: 
              - gridcell "PJ_BC_Salon" [ref=f5e330]
              - gridcell "Account_Salon" [ref=f5e331]
              - gridcell [ref=f5e332]
              - gridcell "122199983" [ref=f5e333]
              - gridcell "05139491" [ref=f5e334]
              - gridcell "908000372" [ref=f5e335]
              - gridcell "$131.00" [ref=f5e336]
              - gridcell "09/23/2026" [ref=f5e337]
              - gridcell "AutoPresentedPayee" [ref=f5e338]
              - gridcell [ref=f5e339]
              - gridcell [ref=f5e340]
              - gridcell [ref=f5e341]:
                - link "pw2_1790217792798_PresentedCheck_Comma_Auto_632729.txt" [ref=f5e342] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17764
              - gridcell [ref=f5e343]:
                - link " Edit" [ref=f5e344] [cursor=pointer]:
                  - /url: /paid-checks/check/35994
                  - generic [ref=f5e345]: 
                  - text: Edit
                - link " Delete" [ref=f5e346] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e347]: 
                  - text: Delete
              - gridcell [ref=f5e348]:
                - link "View " [ref=f5e349] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35994&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e350]: 
            - row [ref=f5e351]:
              - gridcell "35993" [ref=f5e352]
              - gridcell "Completed[Manual Decision]" [ref=f5e353]:
                - text: Completed
                - generic [ref=f5e354]: "[Manual Decision]"
              - gridcell [ref=f5e355]:
                - link " Return " [ref=f5e356] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35993&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e357]: 
                  - text: Return
                  - generic [ref=f5e358]: 
              - gridcell "PJ_BC_Salon" [ref=f5e359]
              - gridcell "Account_Salon" [ref=f5e360]
              - gridcell [ref=f5e361]
              - gridcell "122199983" [ref=f5e362]
              - gridcell "05139491" [ref=f5e363]
              - gridcell "764831" [ref=f5e364]
              - gridcell "$250.00" [ref=f5e365]
              - gridcell "09/23/2026" [ref=f5e366]
              - gridcell [ref=f5e367]
              - gridcell [ref=f5e368]
              - gridcell [ref=f5e369]
              - gridcell [ref=f5e370]:
                - link "pw2_1790217762135_PresentedCheck_FixedLength.txt" [ref=f5e371] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17762
              - gridcell [ref=f5e372]:
                - link " Edit" [ref=f5e373] [cursor=pointer]:
                  - /url: /paid-checks/check/35993
                  - generic [ref=f5e374]: 
                  - text: Edit
                - link " Delete" [ref=f5e375] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e376]: 
                  - text: Delete
              - gridcell [ref=f5e377]:
                - link "View " [ref=f5e378] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35993&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e379]: 
            - row [ref=f5e380]:
              - gridcell "35992" [ref=f5e381]
              - gridcell "Completed[Manual Decision]" [ref=f5e382]:
                - text: Completed
                - generic [ref=f5e383]: "[Manual Decision]"
              - gridcell [ref=f5e384]:
                - link " Return " [ref=f5e385] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35992&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e386]: 
                  - text: Return
                  - generic [ref=f5e387]: 
              - gridcell "PJ_BC_Salon" [ref=f5e388]
              - gridcell "Account_Salon" [ref=f5e389]
              - gridcell [ref=f5e390]
              - gridcell "122199983" [ref=f5e391]
              - gridcell "05139491" [ref=f5e392]
              - gridcell "764830" [ref=f5e393]
              - gridcell "$531.00" [ref=f5e394]
              - gridcell "09/23/2026" [ref=f5e395]
              - gridcell [ref=f5e396]
              - gridcell [ref=f5e397]
              - gridcell [ref=f5e398]
              - gridcell [ref=f5e399]:
                - link "pw2_1790217762135_PresentedCheck_FixedLength.txt" [ref=f5e400] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17762
              - gridcell [ref=f5e401]:
                - link " Edit" [ref=f5e402] [cursor=pointer]:
                  - /url: /paid-checks/check/35992
                  - generic [ref=f5e403]: 
                  - text: Edit
                - link " Delete" [ref=f5e404] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e405]: 
                  - text: Delete
              - gridcell [ref=f5e406]:
                - link "View " [ref=f5e407] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35992&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e408]: 
            - row [ref=f5e409]:
              - gridcell "35991" [ref=f5e410]
              - gridcell "Completed[Manual Decision]" [ref=f5e411]:
                - text: Completed
                - generic [ref=f5e412]: "[Manual Decision]"
              - gridcell [ref=f5e413]:
                - link " Return " [ref=f5e414] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35991&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e415]: 
                  - text: Return
                  - generic [ref=f5e416]: 
              - gridcell "PJ_BC_Carshop" [ref=f5e417]
              - gridcell "Account_Carshop" [ref=f5e418]
              - gridcell [ref=f5e419]
              - gridcell "122199983" [ref=f5e420]
              - gridcell "93016897" [ref=f5e421]
              - gridcell "479339129" [ref=f5e422]
              - gridcell "$337.00" [ref=f5e423]
              - gridcell "09/23/2026" [ref=f5e424]
              - gridcell "AutoPresentedPayee" [ref=f5e425]
              - gridcell [ref=f5e426]
              - gridcell [ref=f5e427]
              - gridcell [ref=f5e428]:
                - link "pw1_1790217707655_PresentedCheck_Comma_Auto_342381.txt" [ref=f5e429] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17757
              - gridcell [ref=f5e430]:
                - link " Edit" [ref=f5e431] [cursor=pointer]:
                  - /url: /paid-checks/check/35991
                  - generic [ref=f5e432]: 
                  - text: Edit
                - link " Delete" [ref=f5e433] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e434]: 
                  - text: Delete
              - gridcell [ref=f5e435]:
                - link "View " [ref=f5e436] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35991&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e437]: 
            - row [ref=f5e438]:
              - gridcell "35990" [ref=f5e439]
              - gridcell "Completed[Manual Decision]" [ref=f5e440]:
                - text: Completed
                - generic [ref=f5e441]: "[Manual Decision]"
              - gridcell [ref=f5e442]:
                - link " Return " [ref=f5e443] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35990&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e444]: 
                  - text: Return
                  - generic [ref=f5e445]: 
              - gridcell "PJ_BC_Club" [ref=f5e446]
              - gridcell "Account_Club" [ref=f5e447]
              - gridcell [ref=f5e448]
              - gridcell "122199983" [ref=f5e449]
              - gridcell "23815974" [ref=f5e450]
              - gridcell "153914" [ref=f5e451]
              - gridcell "$250.00" [ref=f5e452]
              - gridcell "09/23/2026" [ref=f5e453]
              - gridcell [ref=f5e454]
              - gridcell [ref=f5e455]
              - gridcell [ref=f5e456]
              - gridcell [ref=f5e457]:
                - link "pw3_1790217654456_PresentedCheck_FixedLength.txt" [ref=f5e458] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17754
              - gridcell [ref=f5e459]:
                - link " Edit" [ref=f5e460] [cursor=pointer]:
                  - /url: /paid-checks/check/35990
                  - generic [ref=f5e461]: 
                  - text: Edit
                - link " Delete" [ref=f5e462] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e463]: 
                  - text: Delete
              - gridcell [ref=f5e464]:
                - link "View " [ref=f5e465] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35990&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e466]: 
            - row [ref=f5e467]:
              - gridcell "35989" [ref=f5e468]
              - gridcell "Completed[Manual Decision]" [ref=f5e469]:
                - text: Completed
                - generic [ref=f5e470]: "[Manual Decision]"
              - gridcell [ref=f5e471]:
                - link " Return " [ref=f5e472] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35989&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e473]: 
                  - text: Return
                  - generic [ref=f5e474]: 
              - gridcell "PJ_BC_Club" [ref=f5e475]
              - gridcell "Account_Club" [ref=f5e476]
              - gridcell [ref=f5e477]
              - gridcell "122199983" [ref=f5e478]
              - gridcell "23815974" [ref=f5e479]
              - gridcell "153913" [ref=f5e480]
              - gridcell "$531.00" [ref=f5e481]
              - gridcell "09/23/2026" [ref=f5e482]
              - gridcell [ref=f5e483]
              - gridcell [ref=f5e484]
              - gridcell [ref=f5e485]
              - gridcell [ref=f5e486]:
                - link "pw3_1790217654456_PresentedCheck_FixedLength.txt" [ref=f5e487] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17754
              - gridcell [ref=f5e488]:
                - link " Edit" [ref=f5e489] [cursor=pointer]:
                  - /url: /paid-checks/check/35989
                  - generic [ref=f5e490]: 
                  - text: Edit
                - link " Delete" [ref=f5e491] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e492]: 
                  - text: Delete
              - gridcell [ref=f5e493]:
                - link "View " [ref=f5e494] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35989&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e495]: 
            - row [ref=f5e496]:
              - gridcell "35988" [ref=f5e497]
              - gridcell "Completed[Manual Decision]" [ref=f5e498]:
                - text: Completed
                - generic [ref=f5e499]: "[Manual Decision]"
              - gridcell [ref=f5e500]:
                - link " Return " [ref=f5e501] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35988&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e502]: 
                  - text: Return
                  - generic [ref=f5e503]: 
              - gridcell "PJ_BC_Boutique" [ref=f5e504]
              - gridcell "Account_Boutique" [ref=f5e505]
              - gridcell "PJ456!" [ref=f5e506]
              - gridcell "122199983" [ref=f5e507]
              - gridcell "123456" [ref=f5e508]
              - gridcell "635251551" [ref=f5e509]
              - gridcell "$949.00" [ref=f5e510]
              - gridcell "09/23/2026" [ref=f5e511]
              - gridcell "AutoPresentedPayee" [ref=f5e512]
              - gridcell [ref=f5e513]
              - gridcell [ref=f5e514]
              - gridcell [ref=f5e515]:
                - link "pw0_1790217597087_PresentedCheck_Comma_Auto_366078.txt" [ref=f5e516] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17748
              - gridcell [ref=f5e517]:
                - link " Edit" [ref=f5e518] [cursor=pointer]:
                  - /url: /paid-checks/check/35988
                  - generic [ref=f5e519]: 
                  - text: Edit
                - link " Delete" [ref=f5e520] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e521]: 
                  - text: Delete
              - gridcell [ref=f5e522]:
                - link "View " [ref=f5e523] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35988&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e524]: 
            - row [ref=f5e525]:
              - gridcell "35987" [ref=f5e526]
              - gridcell "Completed[Manual Decision]" [ref=f5e527]:
                - text: Completed
                - generic [ref=f5e528]: "[Manual Decision]"
              - gridcell [ref=f5e529]:
                - link " Return " [ref=f5e530] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35987&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e531]: 
                  - text: Return
                  - generic [ref=f5e532]: 
              - gridcell "PJ_BC_Boutique" [ref=f5e533]
              - gridcell "Account_Boutique" [ref=f5e534]
              - gridcell "PJ456!" [ref=f5e535]
              - gridcell "122199983" [ref=f5e536]
              - gridcell "123456" [ref=f5e537]
              - gridcell "506010" [ref=f5e538]
              - gridcell "$250.00" [ref=f5e539]
              - gridcell "09/23/2026" [ref=f5e540]
              - gridcell [ref=f5e541]
              - gridcell [ref=f5e542]
              - gridcell [ref=f5e543]
              - gridcell [ref=f5e544]:
                - link "pw0_1790217561866_PresentedCheck_FixedLength.txt" [ref=f5e545] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17746
              - gridcell [ref=f5e546]:
                - link " Edit" [ref=f5e547] [cursor=pointer]:
                  - /url: /paid-checks/check/35987
                  - generic [ref=f5e548]: 
                  - text: Edit
                - link " Delete" [ref=f5e549] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e550]: 
                  - text: Delete
              - gridcell [ref=f5e551]:
                - link "View " [ref=f5e552] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35987&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e553]: 
            - row [ref=f5e554]:
              - gridcell "35986" [ref=f5e555]
              - gridcell "Completed[Manual Decision]" [ref=f5e556]:
                - text: Completed
                - generic [ref=f5e557]: "[Manual Decision]"
              - gridcell [ref=f5e558]:
                - link " Return " [ref=f5e559] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35986&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e560]: 
                  - text: Return
                  - generic [ref=f5e561]: 
              - gridcell "PJ_BC_Boutique" [ref=f5e562]
              - gridcell "Account_Boutique" [ref=f5e563]
              - gridcell "PJ456!" [ref=f5e564]
              - gridcell "122199983" [ref=f5e565]
              - gridcell "123456" [ref=f5e566]
              - gridcell "506009" [ref=f5e567]
              - gridcell "$531.00" [ref=f5e568]
              - gridcell "09/23/2026" [ref=f5e569]
              - gridcell [ref=f5e570]
              - gridcell [ref=f5e571]
              - gridcell [ref=f5e572]
              - gridcell [ref=f5e573]:
                - link "pw0_1790217561866_PresentedCheck_FixedLength.txt" [ref=f5e574] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17746
              - gridcell [ref=f5e575]:
                - link " Edit" [ref=f5e576] [cursor=pointer]:
                  - /url: /paid-checks/check/35986
                  - generic [ref=f5e577]: 
                  - text: Edit
                - link " Delete" [ref=f5e578] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e579]: 
                  - text: Delete
              - gridcell [ref=f5e580]:
                - link "View " [ref=f5e581] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35986&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e582]: 
            - row [ref=f5e583]:
              - gridcell "35985" [ref=f5e584]
              - gridcell "Completed[Manual Decision]" [ref=f5e585]:
                - text: Completed
                - generic [ref=f5e586]: "[Manual Decision]"
              - gridcell [ref=f5e587]:
                - link " Return " [ref=f5e588] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35985&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e589]: 
                  - text: Return
                  - generic [ref=f5e590]: 
              - gridcell "PJ_BC_Salon" [ref=f5e591]
              - gridcell "Account_Salon" [ref=f5e592]
              - gridcell [ref=f5e593]
              - gridcell "122199983" [ref=f5e594]
              - gridcell "05139491" [ref=f5e595]
              - gridcell "952267527" [ref=f5e596]
              - gridcell "$341.00" [ref=f5e597]
              - gridcell "09/23/2026" [ref=f5e598]
              - gridcell "AutoPresentedPayee" [ref=f5e599]
              - gridcell [ref=f5e600]
              - gridcell [ref=f5e601]
              - gridcell [ref=f5e602]:
                - link "pw2_1790217521803_PresentedCheck_Comma_Auto_420391.txt" [ref=f5e603] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17741
              - gridcell [ref=f5e604]:
                - link " Edit" [ref=f5e605] [cursor=pointer]:
                  - /url: /paid-checks/check/35985
                  - generic [ref=f5e606]: 
                  - text: Edit
                - link " Delete" [ref=f5e607] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e608]: 
                  - text: Delete
              - gridcell [ref=f5e609]:
                - link "View " [ref=f5e610] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35985&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e611]: 
            - row [ref=f5e612]:
              - gridcell "35984" [ref=f5e613]
              - gridcell "Completed[Manual Decision]" [ref=f5e614]:
                - text: Completed
                - generic [ref=f5e615]: "[Manual Decision]"
              - gridcell [ref=f5e616]:
                - link " Return " [ref=f5e617] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35984&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e618]: 
                  - text: Return
                  - generic [ref=f5e619]: 
              - gridcell "PJ_BC_Boutique" [ref=f5e620]
              - gridcell "Account_Boutique" [ref=f5e621]
              - gridcell "PJ456!" [ref=f5e622]
              - gridcell "122199983" [ref=f5e623]
              - gridcell "123456" [ref=f5e624]
              - gridcell "639535706183" [ref=f5e625]
              - gridcell "$753.00" [ref=f5e626]
              - gridcell "09/23/2026" [ref=f5e627]
              - gridcell "eMveuQXU" [ref=f5e628]
              - gridcell [ref=f5e629]
              - gridcell [ref=f5e630]
              - gridcell "Msedge Automation" [ref=f5e631]
              - gridcell [ref=f5e632]:
                - link " Edit" [ref=f5e633] [cursor=pointer]:
                  - /url: /paid-checks/check/35984
                  - generic [ref=f5e634]: 
                  - text: Edit
                - link " Delete" [ref=f5e635] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e636]: 
                  - text: Delete
              - gridcell [ref=f5e637]:
                - link "View " [ref=f5e638] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35984&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e639]: 
            - row [ref=f5e640]:
              - gridcell "35979" [ref=f5e641]
              - gridcell "Completed[Manual Decision]" [ref=f5e642]:
                - text: Completed
                - generic [ref=f5e643]: "[Manual Decision]"
              - gridcell [ref=f5e644]:
                - link " Return " [ref=f5e645] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35979&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e646]: 
                  - text: Return
                  - generic [ref=f5e647]: 
              - gridcell "PJ_BC_Salon" [ref=f5e648]
              - gridcell "Account_Salon" [ref=f5e649]
              - gridcell [ref=f5e650]
              - gridcell "122199983" [ref=f5e651]
              - gridcell "05139491" [ref=f5e652]
              - gridcell "231697" [ref=f5e653]
              - gridcell "$250.00" [ref=f5e654]
              - gridcell "09/23/2026" [ref=f5e655]
              - gridcell [ref=f5e656]
              - gridcell [ref=f5e657]
              - gridcell [ref=f5e658]
              - gridcell [ref=f5e659]:
                - link "PresentedCheck_FixedLength.txt" [ref=f5e660] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17739
              - gridcell [ref=f5e661]:
                - link " Edit" [ref=f5e662] [cursor=pointer]:
                  - /url: /paid-checks/check/35979
                  - generic [ref=f5e663]: 
                  - text: Edit
                - link " Delete" [ref=f5e664] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e665]: 
                  - text: Delete
              - gridcell [ref=f5e666]:
                - link "View " [ref=f5e667] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35979&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e668]: 
            - row [ref=f5e669]:
              - gridcell "35978" [ref=f5e670]
              - gridcell "Completed[Manual Decision]" [ref=f5e671]:
                - text: Completed
                - generic [ref=f5e672]: "[Manual Decision]"
              - gridcell [ref=f5e673]:
                - link " Return " [ref=f5e674] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35978&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e675]: 
                  - text: Return
                  - generic [ref=f5e676]: 
              - gridcell "PJ_BC_Salon" [ref=f5e677]
              - gridcell "Account_Salon" [ref=f5e678]
              - gridcell [ref=f5e679]
              - gridcell "122199983" [ref=f5e680]
              - gridcell "05139491" [ref=f5e681]
              - gridcell "231696" [ref=f5e682]
              - gridcell "$531.00" [ref=f5e683]
              - gridcell "09/23/2026" [ref=f5e684]
              - gridcell [ref=f5e685]
              - gridcell [ref=f5e686]
              - gridcell [ref=f5e687]
              - gridcell [ref=f5e688]:
                - link "PresentedCheck_FixedLength.txt" [ref=f5e689] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17739
              - gridcell [ref=f5e690]:
                - link " Edit" [ref=f5e691] [cursor=pointer]:
                  - /url: /paid-checks/check/35978
                  - generic [ref=f5e692]: 
                  - text: Edit
                - link " Delete" [ref=f5e693] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e694]: 
                  - text: Delete
              - gridcell [ref=f5e695]:
                - link "View " [ref=f5e696] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35978&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e697]: 
            - row [ref=f5e698]:
              - gridcell "35968" [ref=f5e699]
              - gridcell "Completed[Manual Decision]" [ref=f5e700]:
                - text: Completed
                - generic [ref=f5e701]: "[Manual Decision]"
              - gridcell [ref=f5e702]:
                - link " Return " [ref=f5e703] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35968&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e704]: 
                  - text: Return
                  - generic [ref=f5e705]: 
              - gridcell "PJ_BC_Salon" [ref=f5e706]
              - gridcell "Account_Salon" [ref=f5e707]
              - gridcell [ref=f5e708]
              - gridcell "122199983" [ref=f5e709]
              - gridcell "05139491" [ref=f5e710]
              - gridcell "362193057" [ref=f5e711]
              - gridcell "$903.00" [ref=f5e712]
              - gridcell "09/23/2026" [ref=f5e713]
              - gridcell "AutoPresentedPayee" [ref=f5e714]
              - gridcell [ref=f5e715]
              - gridcell [ref=f5e716]
              - gridcell [ref=f5e717]:
                - link "PresentedCheck_Comma_Auto_347909.txt" [ref=f5e718] [cursor=pointer]:
                  - /url: /paid-checks/uploads?Id=17733
              - gridcell [ref=f5e719]:
                - link " Edit" [ref=f5e720] [cursor=pointer]:
                  - /url: /paid-checks/check/35968
                  - generic [ref=f5e721]: 
                  - text: Edit
                - link " Delete" [ref=f5e722] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e723]: 
                  - text: Delete
              - gridcell [ref=f5e724]:
                - link "View " [ref=f5e725] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35968&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e726]: 
            - row [ref=f5e727]:
              - gridcell "35966" [ref=f5e728]
              - gridcell "Completed[Manual Decision]" [ref=f5e729]:
                - text: Completed
                - generic [ref=f5e730]: "[Manual Decision]"
              - gridcell [ref=f5e731]:
                - link " Return " [ref=f5e732] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35966&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e733]: 
                  - text: Return
                  - generic [ref=f5e734]: 
              - gridcell "PJ_BC_Boutique" [ref=f5e735]
              - gridcell "Account14" [ref=f5e736]
              - gridcell "Exlid777" [ref=f5e737]
              - gridcell "063110047" [ref=f5e738]
              - gridcell "10047" [ref=f5e739]
              - gridcell "7463" [ref=f5e740]
              - gridcell "$100.00" [ref=f5e741]
              - gridcell "09/23/2026" [ref=f5e742]
              - gridcell "fqgHyDUW" [ref=f5e743]
              - gridcell [ref=f5e744]
              - gridcell [ref=f5e745]:
                - link " View" [ref=f5e746] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e747]: 
                  - text: View
              - gridcell "F.I ACH&CHK User" [ref=f5e748]
              - gridcell [ref=f5e749]:
                - link " Edit" [ref=f5e750] [cursor=pointer]:
                  - /url: /paid-checks/check/35966
                  - generic [ref=f5e751]: 
                  - text: Edit
                - link " Delete" [ref=f5e752] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e753]: 
                  - text: Delete
              - gridcell [ref=f5e754]:
                - link "View " [ref=f5e755] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35966&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e756]: 
            - row [ref=f5e757]:
              - gridcell "35965" [ref=f5e758]
              - gridcell "Completed[Manual Decision]" [ref=f5e759]:
                - text: Completed
                - generic [ref=f5e760]: "[Manual Decision]"
              - gridcell [ref=f5e761]:
                - link " Return " [ref=f5e762] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35965&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e763]: 
                  - text: Return
                  - generic [ref=f5e764]: 
              - gridcell "PJ_BC_Boutique" [ref=f5e765]
              - gridcell "Account14" [ref=f5e766]
              - gridcell "Exlid777" [ref=f5e767]
              - gridcell "063110047" [ref=f5e768]
              - gridcell "10047" [ref=f5e769]
              - gridcell "7118" [ref=f5e770]
              - gridcell "$100.00" [ref=f5e771]
              - gridcell "09/23/2026" [ref=f5e772]
              - gridcell "OQlxbsABx" [ref=f5e773]
              - gridcell [ref=f5e774]
              - gridcell [ref=f5e775]:
                - link " View" [ref=f5e776] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e777]: 
                  - text: View
              - gridcell "F.I ACH&CHK User" [ref=f5e778]
              - gridcell [ref=f5e779]:
                - link " Edit" [ref=f5e780] [cursor=pointer]:
                  - /url: /paid-checks/check/35965
                  - generic [ref=f5e781]: 
                  - text: Edit
                - link " Delete" [ref=f5e782] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e783]: 
                  - text: Delete
              - gridcell [ref=f5e784]:
                - link "View " [ref=f5e785] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35965&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e786]: 
            - row [ref=f5e787]:
              - gridcell "35964" [ref=f5e788]
              - gridcell "Completed[Manual Decision]" [ref=f5e789]:
                - text: Completed
                - generic [ref=f5e790]: "[Manual Decision]"
              - gridcell [ref=f5e791]:
                - link " Return " [ref=f5e792] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35964&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e793]: 
                  - text: Return
                  - generic [ref=f5e794]: 
              - gridcell "PJ_BC_Boutique" [ref=f5e795]
              - gridcell "Account14" [ref=f5e796]
              - gridcell "Exlid777" [ref=f5e797]
              - gridcell "063110047" [ref=f5e798]
              - gridcell "10047" [ref=f5e799]
              - gridcell "8691" [ref=f5e800]
              - gridcell "$100.00" [ref=f5e801]
              - gridcell "09/23/2026" [ref=f5e802]
              - gridcell "YUeoYzcQ" [ref=f5e803]
              - gridcell [ref=f5e804]
              - gridcell [ref=f5e805]:
                - link " View" [ref=f5e806] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e807]: 
                  - text: View
              - gridcell "F.I ACH&CHK User" [ref=f5e808]
              - gridcell [ref=f5e809]:
                - link " Edit" [ref=f5e810] [cursor=pointer]:
                  - /url: /paid-checks/check/35964
                  - generic [ref=f5e811]: 
                  - text: Edit
                - link " Delete" [ref=f5e812] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e813]: 
                  - text: Delete
              - gridcell [ref=f5e814]:
                - link "View " [ref=f5e815] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35964&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e816]: 
            - row [ref=f5e817]:
              - gridcell "35963" [ref=f5e818]
              - gridcell "Completed[Manual Decision]" [ref=f5e819]:
                - text: Completed
                - generic [ref=f5e820]: "[Manual Decision]"
              - gridcell [ref=f5e821]:
                - link " Return " [ref=f5e822] [cursor=pointer]:
                  - /url: /exceptions/history?Id=35963&ExceptionType=Check&ReturnUrl=%2fpaid-checks
                  - generic [ref=f5e823]: 
                  - text: Return
                  - generic [ref=f5e824]: 
              - gridcell "PJ_BC_Boutique" [ref=f5e825]
              - gridcell "Account14" [ref=f5e826]
              - gridcell "Exlid777" [ref=f5e827]
              - gridcell "063110047" [ref=f5e828]
              - gridcell "10047" [ref=f5e829]
              - gridcell "5700" [ref=f5e830]
              - gridcell "$101.00" [ref=f5e831]
              - gridcell "09/23/2026" [ref=f5e832]
              - gridcell "oJNgLZHsn" [ref=f5e833]
              - gridcell [ref=f5e834]
              - gridcell [ref=f5e835]:
                - link " View" [ref=f5e836] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e837]: 
                  - text: View
              - gridcell "F.I ACH&CHK User" [ref=f5e838]
              - gridcell [ref=f5e839]:
                - link " Edit" [ref=f5e840] [cursor=pointer]:
                  - /url: /paid-checks/check/35963
                  - generic [ref=f5e841]: 
                  - text: Edit
                - link " Delete" [ref=f5e842] [cursor=pointer]:
                  - /url: javascript:;
                  - generic [ref=f5e843]: 
                  - text: Delete
              - gridcell [ref=f5e844]:
                - link "View " [ref=f5e845] [cursor=pointer]:
                  - /url: /client-admin/entity-log?EntityType=PresentedCheck&EntityId=35963&ReturnUrl=%2fpaid-checks
                  - text: View
                  - generic [ref=f5e846]: 
        - application "Page navigation, page 1 of 15" [ref=f5e847]:
          - generic [ref=f5e848]:
            - button "Go to the first page" [disabled]
            - button "Go to the previous page" [disabled]
            - generic [ref=f5e849]:
              - text: Page
              - spinbutton "Select a page" [ref=f5e851]: "1"
              - text: of 15
            - button "Go to the next page" [ref=f5e852] [cursor=pointer]
            - button "Go to the last page" [ref=f5e856] [cursor=pointer]
          - generic [ref=f5e860]: 1 - 20 of 299 items
    - contentinfo [ref=f5e861]:
      - generic [ref=f5e862]:
        - text: FI Playwright Automation
        - generic [ref=f5e863]: "[uat-release]"
      - generic [ref=f5e864]:
        - text: © Copyright Advanced Fraud Solutions 2005-2026 |
        - generic [ref=f5e865]: All Rights Reserved
        - text: "|"
        - link "Privacy Policy" [ref=f5e867] [cursor=pointer]:
          - /url: https://portal.advancedfraudsolutions.com/Help/PrivacyPolicy
```

# Test source

```ts
  61  |     );
  62  | }
  63  | 
  64  | /**
  65  |  * Fill in the already-open "Filter Name" dialog and save the preset.
  66  |  *
  67  |  * The caller is responsible for clicking the grid's save-filter (disk) button first —
  68  |  * that locator lives on each page object.
  69  |  */
  70  | export async function saveFilterPreset(
  71  |     page: Page,
  72  |     name: string,
  73  |     options: { asDefault?: boolean } = {}
  74  | ) {
  75  |     const dialog = saveFilterDialog(page);
  76  |     await waitForSaveFilterDialogSettled(page);
  77  | 
  78  |     const nameInput = dialog.locator('input[name="Filter.FilterName"]');
  79  |     const defaultCheckbox = dialog.getByRole('checkbox').first();
  80  |     const defaultSwitcher = dialog.locator('label.switcher-control', {
  81  |         has: page.locator('input[name="Filter.IsDefault"]'),
  82  |     });
  83  | 
  84  |     if (options.asDefault) {
  85  |         // Prefer the semantic checkbox API, then fall back to the visible switcher label.
  86  |         if (!(await defaultCheckbox.isChecked())) {
  87  |             await defaultCheckbox.check({ force: true }).catch(async () => {
  88  |                 await defaultSwitcher.click();
  89  |             });
  90  |         }
  91  |         await expect.poll(async () => defaultCheckbox.isChecked(), { timeout: 5000 }).toBe(true);
  92  |     }
  93  | 
  94  |     await nameInput.fill(name);
  95  |     // Blur commits the Blazor binding before Save is clicked.
  96  |     await nameInput.press('Tab');
  97  | 
  98  |     // Both values must still be intact at the moment Save is clicked; if a further
  99  |     // re-render ever wipes them again, this fails here with an obvious message rather
  100 |     // than as a mystery timeout on the dialog staying open.
  101 |     await expect(nameInput).toHaveValue(name);
  102 |     if (options.asDefault) {
  103 |         await expect.poll(async () => defaultCheckbox.isChecked(), { timeout: 5000 }).toBe(true);
  104 |     }
  105 | 
  106 |     await dialog.getByRole('button', { name: /Save/ }).click();
  107 | 
  108 |     try {
  109 |         await expect(dialog).toBeHidden({ timeout: 15000 });
  110 |     } catch (error) {
  111 |         // Surface the app's own validation text instead of "modal still visible".
  112 |         if (await systemMessageDialog(page).isVisible()) {
  113 |             const message = (await systemMessageDialog(page).innerText()).replace(/\s+/g, ' ').trim();
  114 |             throw new Error(`Save Filter was rejected by the app: "${message}"`);
  115 |         }
  116 |         throw error;
  117 |     }
  118 | }
  119 | 
  120 | /**
  121 |  * Delete every saved-filter preset whose name matches `match` from a grid's Saved Filters
  122 |  * dropdown. Selecting a preset reveals the trash button; deleting a preset that is marked
  123 |  * Default also clears the account's default filter. Used to self-heal leftover SMK_* presets
  124 |  * left behind when a run is interrupted before its own cleanup runs.
  125 |  *
  126 |  * Returns the names that were deleted.
  127 |  */
  128 | export async function purgeSavedFilterPresets(
  129 |     page: Page,
  130 |     locators: {
  131 |         dropdown: Locator;
  132 |         deleteButton: Locator;
  133 |         confirmDialog: Locator;
  134 |         confirmButton: Locator;
  135 |     },
  136 |     match: RegExp = /^SMK_/
  137 | ): Promise<string[]> {
  138 |     const { dropdown, deleteButton, confirmDialog, confirmButton } = locators;
  139 |     const deleted: string[] = [];
  140 | 
  141 |     await dropdown.waitFor({ state: 'visible', timeout: 20000 });
  142 | 
  143 |     // The option list shifts after each delete, so re-query every iteration.
  144 |     // The bound is a safety net against an unexpected non-terminating state.
  145 |     for (let guard = 0; guard < 200; guard++) {
  146 |         const options = (await dropdown.locator('option').allInnerTexts()).map((o) => o.trim());
  147 |         const target = options.find((o) => match.test(o));
  148 |         if (!target) break;
  149 | 
  150 |         // Preset value equals its name; selecting it applies the filter and reveals delete.
  151 |         await dropdown.selectOption(target);
  152 |         await expect(deleteButton).toBeVisible({ timeout: 10000 });
  153 |         await deleteButton.click();
  154 |         await expect(confirmDialog).toBeVisible({ timeout: 10000 });
  155 |         await confirmButton.click();
  156 |         await expect(confirmDialog).toBeHidden({ timeout: 10000 });
  157 |         await expect
  158 |             .poll(async () => (await dropdown.locator('option').allInnerTexts()).map((o) => o.trim()), {
  159 |                 timeout: 10000,
  160 |             })
> 161 |             .not.toContain(target);
      |                  ^ Error: expect(received).not.toContain(expected) // indexOf
  162 | 
  163 |         deleted.push(target);
  164 |     }
  165 | 
  166 |     return deleted;
  167 | }
  168 | 
  169 | 
```