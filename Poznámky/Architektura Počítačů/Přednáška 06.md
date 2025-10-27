## Programátorský model procesoru, strojový jazyk, assembler
**Řadič - funguje ve 2 fázích,**
### Proč znalost nízkoúrovňového programování
- Vývoj většiny programů(operačních systémů) vyžaduje přesnou kontrolu nad hardware
- Vývoj vestavěných zařízení v chytrých domácích spotřebičích, autech, lékařských zařízení vyžaduje optimalizovaný kód
## Nízkoúrovňový programovací jazyk
- Je velmi blízký instrukcím, kterým rozumí stroj a přímo je provádí
- Umožňuje přímou kontrolu nad součástmi stroje.
- Je extrémně rychlý a efektivní.
- Je specifický pro konkrétní typ procesoru nebo architektury.
- Vyžaduje hluboké znalosti hardwaru a je obtí-žnější číst a zapisovat než jazyky na vysoké úrovni.
![[Pasted image 20251027091546.png]]
Jelikož O a 1 jsou nepřehledné - vývoj mnemotechnický jazyk - 
#### **assembler**
- kopíruje strojový jazyk, jinak vypadá pro Intel, AMD....
	- každý procesor má jinou instrukční sadu
## Programování ve strojovém kódu
- Znalost tzv. programátorského modelu procesoru
- Znalost metod určování operandů
- Mít k dispozici překladač z jazyka symbolických adres do strojového kódu - assembler
### Rozsah adresace instrukcí
- Tříadresové
	- sečti a + b, výsledek c
![[Pasted image 20251027091759.png]]
- Dvouadresové
![[Pasted image 20251027091819.png]]
- Jednoadresové
![[Pasted image 20251027091842.png]]
Aby se ušetřila délka instrukcí tak používáme Jedno a dvou adresové
![[Pasted image 20251027092024.png]]
Implicitní adresování - procesor ho dá na domluvené místo : tady registr **R**
- Výhodnější než to **ukládat do paměti** dá se to do **registru páč je rychlejší**
celí program na 5 instrukcí
![[Pasted image 20251027092418.png]]
Výslede k ukládám do implicitního registru
- přídá se instrukce zapiš
![[Pasted image 20251027092608.png]]
V registru provedu operace jako `B*R`
Pak uložím do P1
Podstatné je že instrukce je zásadně kratší 
Ukládá do akumulátoru
## Programátorský model
- abstrakce, která popisuje, jak programátor „vidí“ a může ovládat procesor při psaní nízkoúrovňového kódu – například v assembleru nebo při vývoji operačních systémů.
- Je to zjednodušený pohled pro programátora, jsou zde prvky se kterými může programátor přímo pracovat.
	- Hlavně se jedná o Registry
	- Příznaky jednotlivé bity které si procesor nastavuje pří výpočtu
### Obecný programátorský model 8 bitového procesoru
![[Pasted image 20251027093109.png]]
- PC - čítač instrukcí - 16 bitový ukazuje další adresu v paměti kde je další instrukce ke spuštění
- R0 - 
- ACC - acumulátor
- Můžu vytváře shluky 16 bit registrů
- Zpracovává 8bitů na jednou - Adresuje 16 registrů
![[Pasted image 20251027093319.png]]
**obr. Programátorsky model*
- **Čítač instrukcí** - 16 bitový ukazuje další adresu v paměti kde je další instrukce ke spuštění
- **Střádač** -  je **speciální registr procesoru**, který se používá **pro ukládání mezivýsledků výpočtů** – hlavně při aritmetických a logických operacích.
Aby mohl střádat 16 bit paměti musí mí 16 bit sčítač
**ukazatel zásobníku stack Pointer(SP)**
- 16 bitoví ukazuje na speciální oblast v paměti které se říká zásobník
8080 měl je jednu sčítačku takže mohl pracovat **jen v pevné čárce**
##### Systémový řadič
- procesor se nesmí moc zatěžovat
Pomocí dekódéru - adresujeme buňky v paměti
## Základní registry Procesoru
- A (Accumulator) - střádač - 8 bitový,
- PC (Program Counter) - čítač instrukcí - 16 bitový,
- sadu univerzálních registrů B, C, D, E, H, L – 8 bitových,
	- dají se používat v párech jako 16 bitové což se hodí pro práci s adresami
- příznakové bity
	–Z (Zero) - = 1 při nulovém výsledku operace, =0 při nenulovém
	–S (Sign) - Kopie znaménkového bitu výsledku operace
	–CY (Carry) - Kopie bitu přenášeného z nejvyššího řádu výsledku operace
	–AC (Auxilary Carry) - přenos mezi bitem 3 a 4 výsledku
		-potože BCD zakódujeme do 4 kvůli přetečení
	–P (Parity) = 1 při sudé paritě výsledku, =0 při liché paritě výsledku

- Dále interní registry (programátorovi neviditelné):
	- IR - instrukční registr (8bitový); je napojen na dekodér instrukcí (řadič),
	- DR - datový registr (8 bitový); registr pro čtení/zápis dat z/do  paměti,
	- AR - adresový registr (16 bitový); adresa pro čtení/zápis z/do  paměti,
	- TA - Temporary Address register (skládá se z TAH (TA High - 8 bitů), TAL (TA Low - 8bitů)).
		- registr ve kterém jsou mezi výsledky
#### Instrukce procesoru
![[Pasted image 20251027094212.png]]
### Zápis instrukce MOV
![[Pasted image 20251027094304.png]]
### FORMÁT  INSTRUKCE
![[Pasted image 20251027094643.png]]
## Typy Operandů
Instrukce obecně nemusí podporovat kombinace libovolných typů (druhů) operandů!
1. Registr
	- operandem je obsah registru
![[Pasted image 20251027202835.png]]
2. **Konstanta (přímí operand)**
	-  pouze jako zdrojový operand
	- celočíselná konstanta (desítková, šestnáctková apod.)
	- textová konstanta ( jednoznakový nebo dvouznakový řetězec), v tomto případě je operandem ASCII kód
	- Symbolické jméno konstanty
	- jméno počítadla adres($)
	- konstantní výraz
![[Pasted image 20251027202853.png]]
3. **Přímá adresa**
	- pracuje se s paměťovým místem určením danou adresou 
	- adresa se udává ve tvaru: **segment:offset**
![[Pasted image 20251027203434.png]]
	- offset je uveden pomocí knostanty - **Offset** = vzdálenost (v bajtech) od určitého výchozího bodu (base address)
	- segment je uveden pomocí jména segmentového registru (nebo jména segmentu nebo jména skupiny segmentů – vyjasní se později)
	- segment i offset mohou být označeny symbolicky – např. návěští (později)
	- default segmentový registr je pro tento mód registr ds
	- překladače (některé) vyžadují, aby se implicitně specifikoval typ operandu  (8-mibitový, 16-tibitový, ...)
	- překladače (některé) vyžadují, aby se vždy explicitně zdůrazňoval fakt, že není uveden operand, ale jeho adresa (tzn. že operand je ukazatel – pointer)
![[Pasted image 20251027203922.png]]
4. **Nepřímá adresa**
	-  pracuje se s paměťovým místem určeným danou adresou
	- offset adresy je v některém z registrů: **bx, bp, di, si** 
	- default segmentové registry:
		- **ds** pro **bx, si ,di**
		- **ss** pro **bp**
![[Pasted image 20251027204412.png]]
**Segment** je **větší blok paměti**, který procesor používá jako **základní oblast** pro práci s daty, kódem nebo zásobníkem.
![[Pasted image 20251027204435.png]]
5. **bázovaná (bázová) adresa**
	- pracuje se s paměťovým místem určeným danou adresou
	- podobně jako nepřímá
	- offset adresy je v některém z registrů **bx, bp**
	- offset se získá jako **součet** obsahu registru a **posunutí** (je-li posunutí 0, nemusí se uvádět – pak jde o **nepřímou adresu**)
- **Báze (base)** = výchozí bod
- **Offset** = posun od báze
![[Pasted image 20251027204815.png]]
6.  indexovaná (indexová) adresa
	- pracuje se s paměťovým místem určeným danou adresou
	- podobně jako bázová
	- offset adresy je v některém z registrů **si, di**
	- offset se získá jako součet obsahu registru a posunutí (je-li posunutí 0, nemusí se uvádět – pak jde o nepřímou adresu)
![[Pasted image 20251027205100.png]]
7. bázově indexová adresa
	- pracuje se s paměťovým místem určeným danou adresou
	- kombinace předcházejících
	- offset adresy operandu se získá jako součet obsahu dvou registrů a příp. posunutí •(je-li posunutí 0, nemusí se uvádět)
	- jeden registr musí být indexový (**si** n. **di**) a jeden bázový (**bp** n. **bx**)
	- default segmentové registry:
		- **ss**  pro **reg1** = **bp**, jinak **ds**
![[Snímek obrazovky 2025-10-27 205433.png]]
![[Pasted image 20251027205527.png]]
![[Pasted image 20251027095625.png]]- To jsou v piči je to v prezentaci. GG
### Zásobník
- Ukazatel zásobníku SP obsahuje adresu vrcholu zásobníku.
- Zásobník slouží na uložení návratové adresy při volání podprogramu a dočasné odložení údajů v registrových párech.
- •Zásobník "roste" k nižším adresám, co znamená, že při vložení údaje do zásobníku se adresa zásobníku sníží o 2 a při vybrání údaje se zvýší o 2.