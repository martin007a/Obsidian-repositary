#### Sekvenční logika
Základní sekvenční obvody: **klopné obvody, čítače, registry, posuvné registry**
**Sekvenční logické obvody si vždy něco pamatují** (obsah paměti, stav klopného obvodu, registru, hodnotu čítače), mají svůj vnitřní stav — stav na výstupech pak odpovídá jak momentálnímu stavu na vstupech, ale i vnitřnímu stavu.
### Klopný obvod R-S (Reset-Set))
- Slouží jako 1 bitová paměť
- Má jeden vstup pro nulování (R), jeden pro nastavení do 1 (S).
- Je **asynchronní**; na rozdíl od dalšího klopného obvodu D nemá hodinový vstup, a jeho výstup se mění okamžitě, když se změní vstup R či S do aktivní úrovně.
- Je asynchronní; na rozdíl od dalšího klopného obvodu D nemá hodinový vstup, a jeho výstup se mění okamžitě, když se změní vstup R či S do aktivní úrovně
### Klopný obvod D (Data)
- souží nám k zapamatování nějšího vstupu - Fakticky jde o jednobitový registr, pamatuje si 1 bit.
- Je synchronní; mění se při příchodu hodinového pulsu = při změně signálu CLK.
- Zápis může být **iniciován** náběžnou ↑ (0 → 1) nebo sestupnou ↓ (1 → 0) hranou CLK
	- to je definováno v dokumentaci k obvodu
- Hodnota přítomná na vstupu D ve chvíli aktivace zápisu se vepíše do registru a na výstup Q
### Kombinované - Klopný obvod D se vstupy R-S
![[Pasted image 20251013093637.png]]
- hobby projekty problém s napájení
### Klopný obvod J-K
Poměrně univerzální klopný obvod, jenž může nahradit R-S, D klopné obvody
- Myšlenka nepotřebuji tolik vstupů
	- lépe se využívají kombinace na vstupech(menší spotřeba  a zpoždění)
![[Pasted image 20251013094158.png]]
-koukni na PFD
### Paralelní Registry ??????
- Klopný obvod RS se dal označit za1bitový registr, pamatuje si 1 bit, viz Klopné obvody 
- 1 bit je ale málo, většinou potřebujeme registr na 4, 8, 32 … bitů — tedy **paralelní registr.**
- Registry často mívají třístavové výstupy (tri-state output).
8 ktrát D klopný obvod. (?)
**OE** - (output enabled), může být 0/1 na výstupu, když není OE, vstup není (vysoká impedance)

musím zajistit aby se aktivoval jen jeden. ??
### Posuvné (sériové) registry
Dva typy posuvných registrů: 
- **serial-in → parallel-out** - krmí se postupně bity a najednou lze přečíst obsah 
- **parallel-in → serial-out** - nakrmí se najednou a postupně umí bity vydávat ven
### Západky (Latches)
Západka je otevřená tak, vstup kopíruje výstup - rozdíl oproti registru?


