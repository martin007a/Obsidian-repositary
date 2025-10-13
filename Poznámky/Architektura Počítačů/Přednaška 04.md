#### Sekvenční logika
Základní sekvenční obvody: **klopné obvody, čítače, registry, posuvné registry**
**Sekvenční logické obvody si vždy něco pamatují** (obsah paměti, stav klopného obvodu, registru, hodnotu čítače), mají svůj vnitřní stav — stav na výstupech pak odpovídá jak momentálnímu stavu na vstupech, ale i vnitřnímu stavu.
### Klopný obvod R-S (Reset-Set))
- Slouží jako 1 bitová paměť
- Má jeden vstup pro nulování (R), jeden pro nastavení do 1 (S).
- Je **asynchronní**; na rozdíl od dalšího klopného obvodu D nemá hodinový vstup, a jeho výstup se mění okamžitě, když se změní vstup R či S do aktivní úrovně.
- Je asynchronní; na rozdíl od dalšího klopného obvodu D nemá hodinový vstup, a jeho výstup se mění okamžitě, když se změní vstup R či S do aktivní úrovně
### Klopný obvod D (Data0))
- souží nám k zapamatování nějšího vstupu - Fakticky jde o jednobitový registr, pamatuje si 1 bit.
- Je synchronní; mění se při příchodu hodinového pulsu = při změně signálu CLK.
- Zápis může být **iniciován** náběžnou ↑ (0 → 1) nebo sestupnou ↓ (1 → 0) hranou CLK
- Hodnota přítomná na vstupu D ve chvíli aktivace zápisu se vepíše do registru a na výstup Q