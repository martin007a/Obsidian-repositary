### Vnitřní reprezentace dat II
Data jsou reprezentována podobě binárních sekvencí
**Znaky jsou v paměti počítače reprezentovány přirozenými čísly. Soubor kódů se nazývá znaková sada**
#### Znaky v Pc 
Každému znaku je přiřazeno jedno číslo

**Znakům je nutné přidělit číselné kódy podle tabulek** 
- **jednobajtové** -ASCII, EBCDIC 
- **vícebajtové** – UCS, Unicode, UTF
**Zobrazitelné znaky** 
- slouží pro zápis textové informace 
- písmena, číslice, interpunkční znaménka, matematické symboly a další znaky vyjádřené textově
**Řídicí znaky** 
- netisknutelné znaky (enter. atd.)
- slouží k ovládání přídavných zařízení nebo programu 
- přechod na nový řádek, tabulátor apod.
#### EBCDIC 
- Prehistorický kód navržený IBM v 60. letech 20. století
- Vychází z kódu používaného pro děrné štítky a BCD kódu využívaného v periferiích IBM
- Kódovací prostor 8 bitů – lze rozlišit 256 znaků – každý znak je uložen na 8 bitech – v některých asijských zemích rozšířený 16bitový kód
- **Rozložení kódu** 
	- **řídicí znaky** – #0 až #63, #255 
	- **zobrazitelné znaky** – #64 až #254
- **Nevýhoda:** znaky anglické abecedy netvoří spojitou posloupnost, nelze použít regulární výraz
![[Pasted image 20251017115411.png]]
### ASCII
**American Standard Code for Information Interchange (1968)**
- Kódovací prostor 8 bitů – lze rozlišit 256 znaků
- původně 7 bitů + 1 paritní bit pro kontrolu 
- každý znak je uložen na 8 bitech
**Rozložení Kódu**
- **řídicí znaky** – #0 až #31, #127 
- **zobrazitelné znaky** – #32 až #126, #128 až #255
**Kód má dvě části **
- **Základní část** - "#0 až  #32, #127" (původních 7 bitů)
- **Rozšířená část** - "#32 až #126, #128 až #255" (přidání 8. bitů)
#### Základní Část
 - je společná  pro všechny jazyky
#### Rozšířená Část 
- liší se podle národního prostředí 
	-Problémy se zobrazováním znaků národních abeced.

![[Pasted image 20251015152942.png]]
### ASCII – rozšířená část
**Národní znaky** (Jiné než anglické)
- Žádný znakový kód nebyl původně navržen pro zobrazování národních znaků
Základní kód ASCII neposkytoval dostatečný prostor pro uložení všech národních znaků.
- lze ale využít 8bit a získat dalších 128 pozic.
Pro různé skupiny jazyků vznikly různé znakové sady.
###### Varianty použité pro češtinu
- kód bratrů Kamenických, KOI-8 ČS2
- PC Latin 2, ISO Latin 2
- Windows-1250, MacCE
## Varianty kódování českých nár. znaků
### Kód bratrů Kamenických
- jiné označení: MJK, KEYBCS2, CP895 
- pro osobní počítače s operačním systémem MS-DOS 
- využití sady CP437 z IBM PC 
- náhrada pozic #128 až #171 českými a slovenskými národními znaky
#### PC Latin 2
- jiné označení: IBM Latin 2, CP852 
- pro osobní počítače s operačním systémem MS-DOS 
- podpora středoevropských jazyků používajících latinku (albánština, čeština, slovenština, polština, rumunština, maďarština, srbochorvatština aj.)
#### KOI-8 ČS2
- Код Обмена Информацией, 8 бит 
- vyvinut v SSSR v rámci RVHP, ČSN 36 9103
### ISO Latin 2
- jiné označení: ISO 8859-2 
- podpora středoevropských a východoevropských jazyků psaných latinkou nebo latinskou transkripcí 
- použitelné i pro němčinu a finštinu
- Standart pro Unixové servery (historicky)
#### Windows-1250
- jiné označení: CP1250 
- pro operační systém Windows 
- podpora středoevropských jazyků a němčiny 
- velmi podobné kódu ISO Latin 2(ISO 8859-2)
 ![[Pasted image 20251015153827.png]]
### Když ASCII přestává stačit
Ke konci 80. let 20. století přichází první potíže - 256 nestačí
- Potřeba sjednotit různé kódové tabulky pro národní abecedy (pro Čj minimálně 5.)
- Značné problémy pří **spolupráci aplikací a přenosech dat** mezi platformami
- Komputerizace **,,exotických " jazyků** s velkým počtem národních znaků
### Hledání nových možností
- Standard **USC** (ISO 10646)
- Standard **Unicode**
Počátkem 90. let 20. stol. se projekty spojily což vedlo k vytvoření **jednotné tabulky.**
- Oba projekty existují a publikují standardy samostatně
- tabulky jsou kompatibilní, rozšiřování je koordinováno
## Universal Character Set (UCS)
- znaky pro reprezentaci všech známých znaků 
- grafické, typografické, matematické a vědecké symboly
Kódovací prostor 31 **bitů** (přes 2 miliardy znaků)
- ty jsou rozděleny do 128 skupin po 24 bitech, každá skupina je rozdělena na 256 rovin po 16 bitech a každá rovina na 256 řad s 256 sloupci.
- většina používaných znaků je na prvních 65 536 pozicích (16 bitů) - **Basic Multilingual Plane**
###### Záměr a doporučení **používat max. 21 bitů**
###### Každému znaku přiřazen číselný kód a oficiální jméno
- např. ’A’ ∼ U+0041 ∼ „Latin capital letter A“
**Původní návrh Unicode** počítal pouze s BMP, ale postupem času se ukázalo, že pro pokrytí všech používaných abeced to nemůže stačit.
### Kompatibilita
U+0000 až U+007F ∼ základní kód ASCII 
U+0000 až U+00FF ∼ ISO 8859-1
### Basic Multilingual Plane
![[Pasted image 20251017131030.png]]
### Kód UCS-2
představuje původní způsob **zápisu znaků z projektu Unicode.** Nabízí kódovací prostor 16 bitů, na kterém lze zobrazit všechny znaky z BMP,
### Kód UCS-4 
zaznamenává každý znak na 4 bajtech, což umožňuje podporu všech znaků UCS-4, UTF-32 z UCS-2 včetně těch mimo BMP.
- UCS-2 zobrazují se bezezměn ale na dvojnásobném prostoru
- Ekvivalentní s UTF-32 (bit)
### UTF-32 (bit)
- každý znak reprezentován 32bitovým číslem
- teoretický rozsah U+00000000 až U+7FFFFFFF
- prakticky stačí U+000000 až U+10FFFF (21 bitů)
- výhodou stejná délka reprezentace všech znaků (4 B)
- nevýhoda velká neúspornost
### UTF-16 (bit)
* v C
* BMP je reprezentováno na 2B mimo BMP 4B
* 
* Teoretický rozsah je U+00000000 až U+0010FFFF,
Oba kódy se mohou objevit ve dvou variantách 
- **Little Endian** – nejdříve LSB, poté zbytek až po MSB 
- **Big Endian** – nejdříve MSB, poté zbytek až po LSB
### UTF-8 (bit)
Odstraňuje nevýhody kódu Unicode
- Usporný
- zpětná kompatibilita s ASCII
- nejsou problémy s endianitou
V současnosti **nejpoužívanější forma** USVC kódování 
- podpora ve všech internetový protokolech
- doporučeno pro tvůrce poštovních klientů
- standardní kódování v operačních systémech, programovacích jazycích a mnoha SW aplikací
- velikost proměnlivá, znak zabere tolik kolik potřebuje, délka reprezentace znaků se pohybuje od 1 do 6 bajtů
- každý znak zabere 2B, slováci - 3B jen kvůli euru 
### **BOM – Byte Order Mark**
UTF signatura
- specialní značky místěné na začátku souboru
- označení pořadí bajtů v souboru
- pro UTF-8 není nutná, ale usnadňuje identifikaci
![[Pasted image 20251017145728.png]]
![[Pasted image 20251015155340.png]]
### Znaky v praxi – jednobajtová kódování
# Reprezentace grafických dat
### Barvy a jejich reprezentace
##### Elektromagnetické záření na určité frekvenci – 
- frekvenční pásmo 3,9 ⋅ 10<sup>8</sup> až 7,9 ⋅ 10<sup>8</sup> MHz 
- nižší frekvence – infračervené záření (teplo) 
- vyšší frekvence – ultrafialové záření (opalování) 
**Lidské oko rozlišuje až 4 ⋅ 10<sup>5</sup> různých odstínů barev**
###### Barevné modely 
- definice základních barev 
- stanovení poměru jednotlivých základních barev 
- stanovení způsobu míchání základních barev
### Aditivní barevný model
- RGB
- Základní barvy jsou **přidávány do černé** 
- čím více přidáme, tím více se blížíme bílé 
- nepotřebujeme vnější světlo
### Subtraktivní barevný model
- odebírá bílou
- CMY(K)
	- K - Key - klíčovací barva
- Základní barvy jsou odečítány od bílé – čím více odebereme, tím více se blížíme černé – potřebujeme vnější zdroj světla
### Míchání barev v modelech RGB a CMY
![[Pasted image 20251015160715.png]]
## Grafika v počítači
### Rastrová grafika
- obraz je tvořen maticí bodů (pixelů) 
- značně rozšířené díky technologiím 
- prakticky vždy se zobrazuje rastrově 
- běžná zařízení: monitor, tiskárna, fotoaparát, skener
### Vektorová grafika 
- obraz je tvořen množinou objektů 
- velmi důležité pro možnosti úprav 
- schopnost efektivního uchování grafické informace 
- specifická zařízení: řezací plotr, tablet
### Grafický bod a jeho reprezentace
**Grafický bod = pixel** -
- picture element 
- každý bod má barvu
**Fyzický pixel**
- zobrazení na výstupním zařízení 
- **obrazovka** – tři prvky vysvítí jeden pixel 
- **inkoustová tiskárna** – kapka nebo shluk kapek barvy 
- **laserová tiskárna** – několik zrnek toneru
**Logický pixel** 
- matematický bod, který nemá rozměr 
- jeho souřadnice specifikuje polohu v obraze 
- při tisku se logické pixely převádí na fyzické
![[Pasted image 20251017153510.png]]
### Hustota obrazu
**Dána počtem pixelů na jednotku délky** 
**Jednotka dpi (dots per inch)**
- tedy počet bodů na jeden palec 
- 1 in = 2,54 cm
**Typické hodnoty hustoty**
- **monitor** – cca 100 dpi 
- **tiskárna** – 300, 600, 1 200 dpi 
- **osvitová jednotka** – 5 000 dpi
**Při vykreslování obrazu na rastrových zařízeních dochází ke změně hustoty**
- obraz (300 dpi) zobrazený na monitoru (100 dpi) - bude 3 krát vetší 
- obraz (300 dpi) vytištěný na tiskárně (600 dpi) 
- efektivní hustota při zobrazení šedých obrazů
### Barevný rastrový obraz v paměti
- Rastrový obraz je uložen po jednotlivých bodech
- Pro každý bod ukládáme intenzitu barvy každé složky
	- tedy 256 možností v intervalu 0 až 255
Model **RGB** vychází ze tří složek, v paměti proto informace o barvě každého bodu zabere 3 B 
- celkem možno rozlišit 256<sup>3</sup> = 16 777 216 barev 
- tedy mnohem více, než dokáže rozlišit lidské oko
 Model **RGBA** používá ještě bajt pro uložení informace o intenzitě průhlednosti pixelu (tzv. alfa kanál)
Model **CMYK** vychází ze čtyř složek, v paměti proto informace o barvě každého bodu zabere 4 B
#### Bitová hloubka
Množství informace o barvě každého pixelu v bitech
##### Monochromatický obraz (monochrome)
- Každý pixel buď barvu má nebo nemá
- informace zabírá 1bit
##### Obraz s barevnou paletou (indexed color)
- barva každého pixelu je vybrána z různě široké škaly
- informace zabírá 2, 4, 8 nebo 16 bitů
##### Obraz s odstíny šedé 
![[Pasted image 20251015162235.png]]
### Jak spočítat paměťovou náročnost?
Ovlivňuje 
- počet bodů
- počet bitů nutných k uložení
Souvislost s hustotou obrazu
	počet pixelů v skouvisloti na skutečných rozměrech
![[Pasted image 20251015162853.png]]
### Ukládání do paměti
![[Pasted image 20251015163301.png]]
Uložení vektorových obrazů
![[Pasted image 20251015163416.png]]
### Reprezentace zvukových dat
![[Pasted image 20251015163524.png]]
### Uložení zvuku – přímý záznam
![[Pasted image 20251015163556.png]]
### Pulsně kódová modulace (PCM)
![[Pasted image 20251015163635.png]]
### Pulsně kódová modulace (PCM)
![[Pasted image 20251015163901.png]]
### Paměťová náročnost zvuku
![[Pasted image 20251015163926.png]]
### Uložení zvuku – MIDI sekvence
![[Pasted image 20251015164146.png]]
### MIDI sekvence-
![[Pasted image 20251015164204.png]]