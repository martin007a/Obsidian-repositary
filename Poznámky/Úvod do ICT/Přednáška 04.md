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
- informace zabírá **1bit**
##### Obraz s barevnou paletou (indexed color)
- barva každého pixelu je vybrána z různě široké škaly
- informace zabírá **2, 4, 8 nebo 16 bitů**
##### Obraz s odstíny šedé (gray scale)
 - barva každého pixelu je šedá (s různou intezitou)
 - informace zabírá **8 bitů**
 Obraz s pravými barvami (true color)
 - barva každého pixelu je složena ze základních barev
 - odpovídá modelu RGB
 - informace zabírá **24 bitů**
#### Barevná monochromatická separace
![[Pasted image 20251017154805.png]]
![[Pasted image 20251017154820.png]]
#### Tisk monochromatického obrazu
![[Pasted image 20251017154907.png]]
### Jak spočítat paměťovou náročnost?
**Ovlivňuje** 
- počet bodů
- počet bitů nutných k uložení každé barvy
Souvislost s hustotou obrazu
	počet pixelů v souvislosti na skutečných rozměrech
![[Pasted image 20251015162853.png]]
![[Pasted image 20251017155452.png]]
### Ukládání do paměti
![[Pasted image 20251015163301.png]]
## Uložení vektorových obrazů
Vektorový obraz je tvořen **geometrickými objekty**
- body, přímky, křivky,...
- využití pro tvorbu ilustrací, diagramů, schémat apod.
V paměti je vektorový obraz reprezentován **posloupností zakódovaných příkazů**
- například **{\put(1,15){\line(1,0){50}}}**
- různé možnosti řešení
##### Výhody
- libovolná úprava velikosti obrázků bez ztráty kvality
- práce s každým objektem v obrázku odděleně
- obvykle menší paměťová náročnost než u rastrů
##### Nevýhody
- Zpravidla složitější pořízení obrázku
- u složitých obrazů rostou nároky na RAM a procesor
## Reprezentace zvukových dat
**Zvuk je** mechanické vlnění v látkovém prostředí, které je schopno vyvolat sluchový vjem
- člověk slyší frekvence od 16 Hz do 20 kHz
- nižší frekvence - infrazvuk (sloni)
- vyšší frekvence - ultrazvuk (psi, delfíni, netopýři)
##### Digitalizace zvuku
- nalezení diskrétní reprezentace spojitého signálu
- snadná užitelnost, přenos a vyhledávání
- přidání metadat, komprese a zpracování bez zkreslení
### Možnost reprezentace zvuku v PC
- **Pulsně kódová modulace**
- **sekvence MIDI**
## Uložení zvuku – přímý záznam
##### Pulsně kódová modulace (PCM)
- pravidelné odečítání hodnoty signálu a její záznam v binární podobě
##### Určující Parametry
- vzorkovací frekvence
- jemnost rozlišení jednotlivých hodnot
##### Nyquist-Shannonova vzorkovací věta
- vzorkovací frekvence alespoň dvojnásobná oproti frekvenci zaznamenaného signálu
- v opačném případě dochází k deformaci (aliasing)
##### Typické hodnoty vzorkovací frekvence
- rozsah lidského sluchu od 16 Hz po 20 kHz
- digitální telefonní linky 8 kHz, zvukové CD 44,1 kHz
- doporučená frekvence pro většinu aplikací 48 kHz
## Pulsně kódová modulace (PCM)
Naměřená hodnota (vzorek) se zaokrouhlí na nejbližší celé číslo a uloží do paměti (kvantování)
- čím více paměti, tím menší zaokrouhlení
- zaokrouhlujeme ale vždy, tím vniká kvantilizační šum
##### Velikost vzorku
- obvikle 8 nebo16 bitů (256 nebo 65 536 hodnot)
- na obrázku 4 bity (16 hodnot)
![[Pasted image 20251017171145.png]]
###  Pulsně kódová modulace (PCM)
![[Pasted image 20251015163901.png]]
### Paměťová náročnost zvuku
![[Pasted image 20251015163926.png]]
### Uložení zvuku – MIDI sekvence
![[Pasted image 20251017171337.png]]
### MIDI sekvence-
- Celkem 128 sekvencí v 16 skupinách po 8 zvucích
- Klavíry, laděné bicí, varhany, kytary, basy, smyčce, zvuky souboru, žestě, plátkové nástroje, píšťaly, elektronické sólové zvuky, elektronické doprovodné zvuky, elektronické zvukové efekty, etnické zvuky, perkusní zvuky a další zvukové efekty (např. výstřel)
![[Pasted image 20251017171419.png]]
### Jak jsou v paměti počítače reprezentovány znaky?
### Jaký je rozdíl mezi řídicím a zobrazitelným znakem?
### Ze kterých částí se skládá tabulka ASCII?
### Jaké existují varianty kódování českých znaků?
### Jaké výhody a nevýhody přináší vícebajtové kódování?
##### Výhody vícebajtového kódování
- Umožňuje **použití jednotné tabulky pro všechny existující jazyky**
- **Umožňuje **použití jednotné tabulky pro všechny existující jazyky****
- **Podpora exotických jazyků** (zejména z jihovýchodní Asie)
- **Optimální kódování (u UTF-8):** Varianta **UTF-8** je obecně považována za **optimální kód** a dosahuje velmi podobných kvalit jako úsporné jednobajtové kódy
##### Nevýhody vícebajtového kódování
- **Neúspornost u pevných délek (UTF-16**) - zaznamenávají každý znak na **4 bajtech**
- . **Problémy s endianitou:** Některé vícebajtové kódy (jako UTF-16 a UTF-32) se mohou objevit ve dvou variantách (**Little Endian** a **Big Endian**
### Které kódování je v současnosti nejpoužívanější?
UTF-8
### Jaký je rozdíl mezi rastrovou a vektorovou grafikou?
Rastrový obraz se skládá z elementárních obrazových bodů (pixelů) určité barvy. Vektorový obraz se skládá z obrazových objektů (vektorů) reprezentovaných geometrickými útvary a jejich atributy.
### Čím se liší barevné modely RGB a CMYK?
Takže RGB
- je Aditivní
- monitory
- Základní barvy jsou **přidávány do černé** 
CMYK 
- tiskárny
- je Subtraktivní, 
- Základní barvy jsou odečítány od bílé
### Jak je v paměti počítače reprezentován rastrový obraz?
V paměti počítače je rastrový obrázek uložen jako **sekvence čísel**, která představují barvy jednotlivých pixelů.
### Jaké výhody a nevýhody mají vektorové obrazy?
- **Úprava bez ztráty kvality:** Existuje **možnost libovolné úpravy obrazu bez ztráty kvality**
- Malá velikost souboru(**Paměťová náročnost**)
- **Oddělená práce s objekty**
- **Vhodnost použití:** Vlastnosti vektorových obrazů je předurčují k použití pro **tvorbu ilustrací, diagramů, schémat, grafů apod.**
Nevýhody
- Nevhodné pro fotografie - Vektorová grafika **není vhodná pro práci s velkým množstvím barevných ploch**
- Pořízení kvalitního obrazu je **zpravidla obtížnější**
- U složitějších obrazů jsou spojeny **vyšší nároky na paměť a procesor**
### Na jakém principu funguje pulsně kódová modulace?
**Pulsně kódová modulace** funguje na principu **digitalizace analogového signálu**, Proces digitalizace (převodu spojitého signálu na diskrétní reprezentaci) zahrnuje **odečítání hodnoty signálu a její záznam v binární podobě**
**Vzorkování (Sampling):** Z analogového signálu jsou odebírány vzorky v **přesně definovaných pravidelných časových intervalech**.

Tento proces se řídí **Nyquistovou-Shannonovou vzorkovací větou**, která stanovuje, že vzorkovací frekvence musí být alespoň **dvojnásobná** oproti mezní frekvenci zaznamenaného signálu. Pokud je frekvence nižší, dochází k deformaci signálu, tzv. _aliasingu_.

Tímto výběrem hodnot jen v určitých okamžicích získáme **diskrétní (digitální) signál**.

**Kvantování (Quantization):** Naměřenou hodnotu signálu je nutné **kvantovat**, což znamená **zaokrouhlit na nejbližší celé číslo**.

Čím více paměti je k dispozici pro uložení vzorku (např. 8 nebo 16 bitů), tím jemnější může být rozlišení jednotlivých hodnot a tím menší kvantizační šum vzniká.

**Kódování (Encoding):** Kvantované (zaokrouhlené) hodnoty jsou **vyjádřeny binární posloupností**. Tím se získá digitální signál, který lze přenášet jako posloupnost čísel, typicky nul a jedniček
### Jaké výhody a nevýhody mají sekvence MIDI?
##### Výhody sekvencí MIDI
- **Minimální paměťová náročnost:** Sekvence MIDI obsahují pouze **stručný digitální popis** hudebního signálu
###### Nevýhody sekvencí MIDI
- Sekvence MIDI nereprezentují samotný zvuk, ale pouze pokyny pro jeho vytvoření (digitální popis výšky jednotlivých tónů, jejich intenzity, délky a doprovodných efektů). Z tohoto důvodu **nelze zaznamenat** například **lidský hlas** ani **hudební nástroj**, který by syntetizátor nedokázal „zahrát“
- **Náročnost převodu:** Převod zvuku do sekvence MIDI je **poměrně náročný**
