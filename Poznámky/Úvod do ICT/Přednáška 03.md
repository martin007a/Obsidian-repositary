# Vnitřní reprezentace dat
Zobrazeni čísel v paměti počítače je limitováno, velikost prostoru úzce souvisí s datovým tipem.
- máme-li k dispozici 1 bajt paměti, můžeme zde ukládat čísla nevýše osmiciferné binární posloupnosti.
### Binární řádová mřížka
Formát zobrazitelných čísel jednoznačně definuje binární řádová mřížka
- definuje nejnižší řád m a nejvyšší rád n
- V závislosti na umístění řádové čárky 
![[Pasted image 20251010093751.png]]
##### **Základní vlastnosti řádové mřížky**
- **Délka (l)** - počet rozlišitelných hodnot (řádků)
- **Jednotka ()** - nejmenší kladné zobrazitelné číslo
- **Modul** - (M) - nejmenší číslo které již zobrazitelné není.
U binárních čísel mají nejnižší a nejvyšší řád označení
- **LSB** = Least Significant Bit
- MSB = Most Significant Bit
Operační paměť počítače je rozdělena do **adresovatelných buněk o velikosti 1 bajtu, kterým říkáme slabiky.**
![[Pasted image 20251008152055.png]]
- délka mřížky je dána počtem řádů nalevo a napravo od řádové čárky, tj. 𝑙 = 𝑚 + 𝑛 + 1;
- jednotka je číslo, které má jedničku pouze v nejnižším řádu, tj. 𝜖 = 𝑧<sup>−𝑚</sup>;
- modul je číslo, které má jedničku v řádu, který již není v mřížce obsažen, tj. 𝑀 = 𝑧<sup>𝑛+1</sup> .
### Přetečení a podtečení
Pokud je délka mřížky menší než počet cifer čísla 𝐴, číslo nebude zobrazitelné.
- do mřížky nebude možné uložit všechny číslice čísla 𝐴 
- řády, které se nevejdou, budou ignorovány
Dojde k **přetečení** a následné ztrátě přesnosti v reprezentaci čísla
- číslo bude uloženo s chybou
- číslo bude zaokrouhleno
- číslo bude zaměněno za číslo s opačným znaménkem
![[Pasted image 20251010100851.png]]
Opakem přetečení je **Podtečení**
- číslo A se blíží nule a je zobrazeno jako 0
- problém u racionálních čísel
![[Pasted image 20251010100927.png]]
### Ztráta přesnosti v praxi
![[Pasted image 20251008152638.png]]
###   Terminologie
![[Pasted image 20251008152713.png]]
## Celá čísla
Celá čísla jsou v počítači reprezentována s pevnou řádovou čárkou, což znamená, že řádová čárka v mřížce je umístěna vždy na pevné pozici vpravo za nejnižším bitem.
- Operační paměť počítače je rozdělena do adresovatelných jednotek velikosti slabiky (bajtu)
2 Ve dvojkové soustavě = 10.
Pozor v pc potřebuji vědět na kolika Bitech je zobrazeno
![[Pasted image 20251008152801.png]]
## Celočíselné datové typy
![[Pasted image 20251008153019.png]]
![[Pasted image 20251008153056.png]]
### Celá čísla bez znaménka
Zobrazení bez úprav na vymezeném prostoru 𝑛 bitů
![[Pasted image 20251008153146.png]]
### Celá čísla se znaménkem
Standardní polyadické číselné soustavy pouze pro zobrazení nezáporných čísel
Zobrazení záporných čísel pomocí **číselných kódů**
- přímý kód (sign magnitude) 
- inverzní kód (one’s complement) 
- doplňkový kód (two’s complement) 
- aditivní kód (biased)
Prakticky všechny operace na moderních počítačích založeny na reprezentaci doplňkovým kódem
- hardware je rychlejší 
- hardware je jednodušší (a tím i rychlejší)
### Přímý kód
Pro člověka jediná čitelná forma rozlišování mezi kladnými a zápornými čísly
- Hardware by byl ale pomalý a zbytečně složitý
**Princip**: použití nejvyššího řádu mřížky pro reprezentaci znaménka (tzv. znaménkový bit)
- 0 reprezentuje kladné číslo
- 1 reprezentuje záporné číslo
![[Pasted image 20251008153641.png]]
![[Pasted image 20251008153654.png]]
problémy 0 != -0
### Inverzní kód
Z historického hlediska velmi důležitý kód
Dnes neexistuje stroj pracující v tomto kódu  
- ale potřebujeme jej při zobrazení v doplňkovém kódu
#### Princip
- kladná čísla reprezentujeme beze změny 
- u záporných čísel najdeme doplněk všech řádů do jedničky (**doplňkem** 0 je 1, doplňkem 1 je 0)
![[Pasted image 20251008153949.png]]
### Doplňkový kód
Varianta inverzního kódu bez dvojí reprezentace nuly – hardware proto může pracovat rychleji,
#### Princip
- kladná čísla reprezentujeme beze změny 
- u záporných čísel nalezneme jedničkový doplněk a k výsledku přičteme 1(binární)
![[Pasted image 20251008154101.png]]
### Aritmetické operace v doplňkovém kódu
![[Pasted image 20251008154424.png]]
**Přenos z nejvyššího bitu je ignorován**
- je totiž mimo řádovou mřížku (Důvod proč už nemáme -0)
- číslo je automaticky ořezáno na daný počet bitů
**Je-li součet mimo interval zobrazitelných hodnot, dochází k přetečení**
- binární reprezentace čísla pak odpovídá jinému číslu.
- číslo -X má stejnou reprezentaci jako 2<sup>n</sup> - X
- proto je číslo 2<sup>n</sup> - X hledaným doplňkem čísla X
![[Pasted image 20251010105424.png]]
-26 = 230
		256 - 26
			2<sup>8</sup>
-128 __ 127
### Aditivní kód
![[Pasted image 20251008155057.png]]
![[Pasted image 20251008155109.png]]
![[Pasted image 20251008155304.png]]
### Rozšíření řádové mřížky
![[Pasted image 20251008155507.png]]
![[Pasted image 20251008155520.png]]
#### Kód BCD (Binary Coded Decimal)
Pro zařízení pracující v tzv. dvojkově desítkové soustavě
- kalkulačky, digitální měřicí přístroje apod.
**Princip**
- číslice 0 až 9 jsou uloženy v půlslabice (4 bity) 
- nesmí se vyskytovat kombinace 10 až 15
**Dvě možnosti řešení**
Dvě možnosti řešení 
- zhuštěný tvar – v jedné slabice jsou dvě BCD číslice 
- nezhuštěný tvar – v jedné slabice je jedna BCD číslice
![[Pasted image 20251008155727.png]]
### Znaménková čísla – shrnutí
![[Pasted image 20251008155810.png]]
Co mo řekne jak ten štrůdl 1 a 0 mám chápat?
- **Datový typ**
![[Pasted image 20251008155819.png]]
V podstatě to samý!!

O významu reprezentace čísla rozhoduje datový typ
![[Pasted image 20251008160003.png]]
### Celá čísla příklady
![[Pasted image 20251008160048.png]]
### Prefixy čísel v počítači
Některé programy a překladače programovacích jazyků podporují čísla v nedesítkových soustavách
- vědecká kalkulačka 
- překladač programovacího jazyka Pascal
/ Pokud ale zadáváme nedesítkové číslo tam, kde se očekává desítkové, musíme explicitně uvést soustavu
/ Před číslo uvedeme jednoznačný prefix soustavy
![[Pasted image 20251008160216.png]]
### Racionální čísla
![[Pasted image 20251008160306.png]]
![[Pasted image 20251008160424.png]]
### Zobrazení s pevnou řádovou čárkou
### Princip
- řádová čárka je v mřížce umístěna na pevné pozici 
- první bit je znaménkový 
- 𝑛 bitů pro celou část, 𝑚 pro desetinnou
![[Pasted image 20251008160530.png]]
![[Pasted image 20251008160550.png]]
### Pohyblivá desetinná čárka

### Vědecká notace obecně
![[Pasted image 20251008160927.png]]
### Zobrazení s pohyblivou řádovou čárkou
![[Pasted image 20251008161000.png]]
### Vědecká notace binárních čísel
![[Pasted image 20251008161039.png]]
- mantisa = příklad
#### Standardizované formáty čísel
**Nějčastější:**
- **Single precision (binary32, od r. 1985)**  
	- 1 bit znaménko, 8 bitů exponent, 23 bitů mantisa
- **Double precision (binary64, od r. 1985)**
	 - 1 bit znaménko, 11 bitů exponent, 52 bitů mantisa
- Quadruple precision (binary128, od r. 2008)
	- 1 bit znaménko, 15 bitů exponent, 112 bitů mantisa
### Zaokrouhlování dle standardu IEEE 754
Využití tří pomocných bitů uchovaných hardwarem navíc nad rámec těch, které se vlezly do mantisy.
- guard – chrání před ztrátou významného bitu při přenosu 
- round – umožňuje zaokrouhlení výsledku po normalizaci 
- sticky – logický součet všech zbývajících bitů
## Význam GRS bitů při zaokrouhlování
![[Pasted image 20251008161436.png]]
### Reprezentace podle IEEE – single precision
![[Pasted image 20251008161710.png]]
![[Pasted image 20251008161948.png]]
![[Pasted image 20251008162222.png]]
### Racionální čísla – příklady
![[Pasted image 20251008162439.png]]
## Denormalizovaná (subnormální) čísla
![[Pasted image 20251008162530.png]]
### Příklad
![[Pasted image 20251008162605.png]]
obr. Ukázka jak to vypadá
### Interpretace hodnot
![[Pasted image 20251008162742.png]]
### Problémy při práci s racionálními čísly
![[Pasted image 20251008163032.png]]
### Aritmetické operace s pohyblivou čárkou
![[Pasted image 20251008163138.png]]
m- mantisa
z - základ
ex - exponent
![[Pasted image 20251008163227.png]]!
![[Pasted image 20251008163244.png]]
![[Pasted image 20251008163332.png]]
![[Pasted image 20251008163504.png]]
pkračování v prezentaci .xd slid 55
### Jak je v paměti počítače reprezentována proměnná v celočíselném datovém typu bez znaménka?

V paměti počítače je proměnná **reprezentována binárně**, tedy jako posloupnost **bitů (0 a 1)**.
### Jak je v paměti počítače reprezentována proměnná v celočíselném datovém typu se znaménkem?
V paměti je číslo opět reprezentováno jako **posloupnost bitů (0 a 1)**, ale na rozdíl od typu _unsigned_ se **jeden bit používá pro znaménko**.  
Tento systém se dnes téměř vždy realizuje pomocí **dvojkového doplňku (two’s complement)**.
### Na jakém principu pracuje aditivní kód (kód s posunutou nulou) a k čemu se používá?
**Aditivní kód** (také **offset binary** nebo **biased code**) je způsob,  
jak **reprezentovat kladná i záporná čísla** **bez použití znaménkového bitu**.

Místo toho se do čísla **přidá určitá konstanta (posun, bias)**, takže **nulová hodnota se “posune” doprostřed číselného rozsahu**.
**Použití**
**– použití pro reprezentaci exponentu racionálních čísel**
### Jak je v paměti počítače reprezentována proměnná v racionálním datovém typu podle standardu IEEE?
![[Pasted image 20251014211129.png]]
![[Pasted image 20251014211245.png]]
![[Pasted image 20251014211307.png]]
### Co je přetečení a podtečení a co je způsobuje?
#### **PŘETEČENÍ (overflow)**

**Nastane, když je výsledek příliš velký**, aby se vešel do zadaného datového typu.
- číslo bude uloženo s chybou 
- číslo bude zaokrouhleno 
- číslo bude zaměněno za číslo s opačným znaménkem
#### **PODTEČENÍ (underflow)**

**Nastane, když je výsledek příliš malý (záporný nebo blízko nuly)**, aby ho daný typ dokázal vyjádřit.
- problém u racionálních čísel
### Jaká jsou pravidla pro zaokrouhlování racionálních čísel?
Využití tří pomocných bitů uchovaných hardwarem navíc nad rámec těch, které se vlezly do mantisy 
- guard – chrání před ztrátou významného bitu při přenosu 
- round – umožňuje zaokrouhlení výsledku po normalizaci 
- sticky – logický součet všech zbývajících bitů
![[Pasted image 20251014212437.png]]
### Které speciální hodnoty mohou být výsledkem operace nad racionálními čísly?
![[Pasted image 20251014212738.png]]
### Co jsou denormalizovaná čísla a kdy se používají?
**Denormalizovaná čísla** jsou ta úplně nejmenší kladná/záporná čísla,  
která se používají k tomu, aby počítač při velmi malých výsledcích  
**neskočil rovnou na nulu**, ale **plynule se k ní blížil**.
![[Pasted image 20251014213118.png]]
- Libovolná nenulová mantisa, nulový exponent 
- Mantisa uložena s pevnou řádovou čárkou umístěnou za nejvyšším bitem
![[Pasted image 20251014213211.png]]
