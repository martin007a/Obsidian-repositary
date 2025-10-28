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
- Instrukce s konstantou **vždy zabírá víc než 1 bajt**, protože musí mít zvlášť místo pro tu konstantní hodnotu.

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
	- **Registr SS (Stack Segment)** určuje **začátek (bázi)** paměťové oblasti,  kde je uložen **zásobník (stack)**.
|Registr|Název|Účel|Kombinuje se s|K čemu se používá

| Registr | Název           | Účel                                                          | Kombinuje se s                                        | K čemu se používá                                                         |
| ------- | --------------- | ------------------------------------------------------------- | ----------------------------------------------------- | ------------------------------------------------------------------------- |
| **CS**  | _Code Segment_  | určuje, kde v paměti je uložen **programový kód (instrukce)** | **IP** (_Instruction Pointer_)                        | procesor z této oblasti **čte instrukce**, které vykonává                 |
| **SS**  | _Stack Segment_ | určuje, kde v paměti je uložen **zásobník (stack)**           | **SP** (_Stack Pointer_) nebo **BP** (_Base Pointer_) | používá se při **PUSH**, **POP**, volání podprogramů, návratu z nich atd. |

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
![[Pasted image 20251028121328.png]]
7. bázově indexová adresa
	- pracuje se s paměťovým místem určeným danou adresou
	- kombinace předcházejících
	- offset adresy operandu se získá jako součet obsahu dvou registrů a příp. posunutí •(je-li posunutí 0, nemusí se uvádět)
	- jeden registr musí být indexový (**si** n. **di**) a jeden bázový (**bp** n. **bx**)
	- default segmentové registry:
		- **ss**  pro **reg1** = **bp**, jinak **ds**
![[Snímek obrazovky 2025-10-27 205433.png]]
![[Pasted image 20251027205527.png]]
## Zápis instrukce LDA
Načtení operandu do registru A
![[Pasted image 20251028122457.png]]
Zápis v symbolickém jazyku
- LDA adresa
- LDA 100b, LDA 8h

![[Pasted image 20251027095625.png]]- 
**To jsu v piči je to v prezentaci. GG**
## **Vykonávání instrukcí, programu**
Vykonání každé instrukce trvá určitou dobu. Délka této doby je obecně závislá na složitosti instrukce. Některé instrukce mají i několik různých dob provádění (podle podmínek, za kterých jsou vykonávány). U reálných procesorů je doba vykonávání instrukcí v řádech ns až ms.

Instrukce jsou vykonávány po sobě, v pořadí, v jakém jsou zapsány v programu. Jen po některých instrukcích může být vykonávána jiná instrukce než je ta, která je v programu bezprostředně následující.<span style="color:rgb(255, 0, 0)"> K<span style="color:rgb(255, 0, 0)">teré to jsou instrukce?</span><br></span>
Jedná se o instrukce <span style="color:rgb(255, 0, 0)">skoku </span>(podmíněného, nepodmíněného), volání podprogramu,..

Procesor vždy vykonává nějakou instrukci. Zapnutý procesor nezná jinou činnost než vykonávat instrukce. Po zapnutí procesor přečte z dohodnuté adresy, obvykle 0000H, jeden byte a interpretuje ho jako operační kód své první instrukce, provede ji a pokračuje dále.
## Přehled instrukcí
### Přesun dat (Data Transfer Instructions)
Slouží k přesunu dat mezi registry, pamětí a akumulátorem.
- **MOV** dest, src – přesun dat mezi registry
- **MVI** reg, data – vložení konstanty do registru
- **LXI** rp, data16 – načtení 16bitové konstanty do páru registrů
- **LDA** addr / **STA** addr – načtení/uložení akumulátoru z/do paměti
- **LHLD** addr / **SHLD** addr – načtení/uložení páru HL z/do paměti
- **XCHG** – výměna **HL** a **DE**
### Aritmetické instrukce
Provádějí sčítání, odčítání a další operace.
- **ADD** reg / **ADI** data – sčítání s akumulátorem
- **SUB** reg / **SUI** data – odčítání od akumulátoru
- **INR** reg / **DCR** reg – inkrementace/dekrementace
- **DAD** rp – sčítání páru registrů s **HL**
* **DAA** – úprava akumulátoru pro **BCD**
### Logické instrukce
Provádějí logické operace jako AND, OR, XOR.
- **ANA** reg / **ANI** data – AND s akumulátorem
- **ORA** reg / ORI **data** – OR s akumulátorem
- **XRA** reg / XRI **data** – XOR s akumulátorem
- **CMP** reg / **CPI** data – porovnání s akumulátorem
- **RLC**, **RRC**, **RAL**, **RAR** – rotace bitů v akumulátoru
![[Pasted image 20251028141432.png]]
### Řídicí instrukce
Slouží k řízení toku programu.
- **JMP** addr – skok na adresu
-  **JC**, **JNC**, **JZ**, **JNZ**, **JP**, **JM** – podmíněné skoky
- **CALL** addr / **RET** – volání a návrat z podprogramu
- RET - - Návrat z podprogramu
    Co se děje:  
    1. Procesor **načte adresu z vrcholu zásobníku**
    2. Skáče zpět na místo, odkud byl volán podprogram
- **CPI**, **CPE**, **CPO**, **CP**, **CM** – podmíněné volání/návrat
![[Pasted image 20251028133323.png]]
> `addr` = adresa, kam procesor skočí, pokud je podmínka splněna.
![[Pasted image 20251028134427.png]]
### Příznaky
- **S - Sign flag** (znaménko) - Příznak záporného výsledku. Čísla větší jak **127** jsou chápané jako záporné.  **0 = plus,** **1 = mínus.**
- **Z - Zero flag** - Příznak nulového výsledku - má hodnotu **1, nebo** hodnotu **0** pro nenulový výsledek.
- **AC - Auxilliary Carry flag** - Příznak přenosu ze 3. bitu do 4.
- **P - Parity flag** - Příznak parity - má hodnotu **1 pro sudou paritu (sudý počet jedniček)**
- **CY - Carry flag** - Příznak pretečení - má hodnotu **1**, když doško k přetečení.
### **Instrukce zásobníku a I/O**
- PUSH rp - sníží adresu SP a uloží rp do zásobníku
- POP rp – vybere ze zásobníku rp a zvýší adresu SP
- IN port / OUT port – vstup/výstup z/do I/O portu
- SPHL – nastavení SP podle HL
- XTHL – výměna HL s vrcholem zásobníku
### Zásobník 
- Ukazatel zásobníku SP obsahuje adresu vrcholu zásobníku.
- Zásobník slouží na uložení návratové adresy při volání podprogramu a dočasné odložení údajů v registrových párech.
- Zásobník "roste" k nižším adresám, co znamená, že při vložení údaje do zásobníku se adresa zásobníku sníží o 2 a při vybrání údaje se zvýší o 2.
![[Pasted image 20251028140530.png]]
### Řídicí instrukce
- NOP – žádná operace
- HLT – zastavení procesoru
- DI / EI – zakázání/povolení přerušení
### Příklady
![[Pasted image 20251028140959.png]]
CMA - Invertuje bity v A
INR A - Přičte 1 k A
- Převod do doplňkového kódu
### ZDROJOVÝ TEXT PROGRAMU V ASSEMBLERU
- program složený z řádků
- zápis jedné akce nesmí přesahovat hranice řádků
- na jednom řádku nelze soustředit zápis dvou akcí
![[Pasted image 20251028142305.png]]
#### direktivy:
- povely pro překladač
- negenerují žádný kód
- řídí využívání paměti, segmentaci, umožňují definici dat, řízení podmíněného překladu, nastavení voleb překladače, 
### makra:
- symbolicky označená část zdrojového textu, kterou v případě jejího výskytu není nutné opakovaně opisovat, ale pouze uvést název
- lze parametrizovat
- tzv. nepravý podprogram
- podobné jako makra v C
### FORMÁLNÍ ÚPRAVA PROGRAMU
- kromě členění na řádky nestanovena
- parametry (operandy) se od předchozího pole oddělují alespoň jedním znakem mezera, tabulátor nebo čárka
- nadbytečné oddělovače nevadí
- všechna pole jsou nepovinná (prázdný řádek je formálně správný)
- doporučuje se psát program tak, aby odpovídající pole byla pod sebou
- doporučuje se, aby každý řádek měl komentář
![[Pasted image 20251028143030.png]]
### Násobení (8bit × 8bit)
- Inicializuj výsledek na 0.
- Opakuj B-krát:
	+ Přičti A k výsledku.
- **Použij registr jako čítač smyčky.**
- Výsledek je 16bitový, protože 8bit × 8bit může dát až 65535.
![[Pasted image 20251028143300.png]]
### Dělení
- **Dělení A / B (výsledek: podíl v C, zbytek v A)**
- Výsledek je:
	C = podíl (kolikrát se B vejde do A)
	A = zbytek (co zůstane po dělení)
### Algoritmus dělení pomocí odčítání
- **Inicializuj podíl na 0.**
- Dokud je čitatel větší nebo roven jmenovateli:
	- Odečti jmenovatel od čitatele.
	- Inkrementuj podíl.
- Zbytek je to, co zůstane z čitatele.
![[Pasted image 20251028150843.png]]
![[Pasted image 20251028171814.png]]
### Programátorský model 64bitového procesoru Intel
##### 64bitové registry:
- 16 obecných registrů (např. RAX, RBX, RCX, RDX, RSI, RDI, RSP, RBP, R8–R15)
- Každý registr má přístup k různým částem: 64bit (např. RAX), 32bit (EAX), 16bit (AX), 8bit (AL, AH)
##### Instrukční sada x84-64 
- Rozšířená o nové instrukce pro práci s 64bitovými daty
- Podpora SIMD instrukcí (např. SSE, AVX)
##### Paměťový model:
- Virtuální adresace s 64bitovými adresami (prakticky omezeno na 48bit)
- Podpora segmentace (i když v 64bit režimu je většina segmentů ignorována)
##### Režim běhu
- Legacy mode (pro 16/32bit aplikace)
- Compatibility mode (pro 32bit aplikace v 64bit OS)
- 64bit mode (plná 64bit funkcionalita)
##### Stavy procesoru:
- Stavové příznaky v registru FLAGS (např. Zero, Carry, Overflow)
- Řídicí registry jako CR0–CR4, EFER (Extended Feature Enable Register)
##### Floating-point jednotka (FPU)
- Podpora x87, SSE, AVX pro výpočty s plovoucí desetinnou čárkou
## Obecné registry
Používají se pro výpočty, uchovávání dat, adres a dočasných hodnot:
- RAX – akumulátor, často pro návratové hodnoty funkcí
- RBX – bázový registr, někdy pro adresování
- RCX – čítač, např. pro smyčky
- RDX – datový registr, často pro parametry funkcí
- RSI – zdrojový index, při kopírování dat
- RDI – cílový index, při kopírování dat
- RSP – ukazatel zásobníku (Stack Pointer)
- RBP – základní ukazatel (Base Pointer), pro rámec funkce
- R8–R15 – dodatečné registry pro parametry a lokální proměnné
Každý z těchto registrů má i přístup k menším částem:
- Např. RAX → EAX (32bit), AX (16bit), AL/AH (8bit)
### Speciální registry
- **RIP** – Instruction Pointer, ukazuje na aktuální instrukci
- **FLAGS** – registr příznaků, obsahuje bity jako:
	- ZF (Zero Flag) – výsledek operace je nula
	- CF (Carry Flag) – přenos při aritmetice
	- SF (Sign Flag) – znaménko výsledku
	- OF (Overflow Flag) – přetečení
**Vektorové a plovoucí registry**
- **XMM0–XMM15** – 128bitové registry pro SIMD operace (SSE)
- **YMM0–YMM15** – 256bitové (AVX)
- **ZMM0–ZMM31** – 512bitové (AVX-512)
- **ST(0)–ST(7)** – zásobníkové registry pro výpočty s reálnými čísly (x87)
**Řídicí registry (CR0–CR4, EFER)**
- Používají se pro správu režimů procesoru, stránkování, virtualizaci – důležité pro operační systém.
## Nástroje a prostředí pro nízkoúrovňové programování
- **NASM (Netwide Assembler):** Populární assembler pro x86 a x86-64.
- **MASM (Microsoft Macro Assembler):** Standardní assembler společnosti Microsoft pro Windows.
- **GAS (GNU Assembler):** Část sady nástrojů GNU, široce používaná na systémech podobných Unixu.
- **IDA Pro:** Pokročilý disassembler a debugger, užitečný pro reverzní inženýrství.
- **OllyDbg:** 32bitový debugger pro Windows, oblíbený mezi analytiky malwaru.