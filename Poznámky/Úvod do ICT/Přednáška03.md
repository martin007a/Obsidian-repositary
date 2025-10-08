# Vnitřní reprezentace dat I
### Binární řádová mřížka
![[Pasted image 20251008151825.png]]
- **jednotka** jde zobrazit
- **modul** nejde zobrazit
![[Pasted image 20251008152055.png]]
### Přetečení a podtečení
Pokud je délka mřížky menší než počet cifer čísla 𝐴, číslo nebude zobrazitelné.
- do mřížky nebude možné uložit všechny číslice čísla 𝐴 
- řády, které se nevejdou, budou ignorovány
Dojde k **přetečení** a následné ztrátě přesnosti v reprezentaci čísla
![[Pasted image 20251008152500.png]]
### Ztráta přesnosti v praxi
![[Pasted image 20251008152638.png]]
### Terminologie
![[Pasted image 20251008152713.png]]
## Celá čísla
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
Varianta inverzního kódu bez dvojí reprezentace nuly – hardware proto může pracovat rychleji
#### Princip
- kladná čísla reprezentujeme beze změny 
- u záporných čísel nalezneme jedničkový doplněk a k výsledku přičteme 1
![[Pasted image 20251008154101.png]]
### Aritmetické operace v doplňkovém kódu
![[Pasted image 20251008154424.png]]
![[Pasted image 20251008154434.png]]
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
