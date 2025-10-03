Operační systém - Poskytuje spojku mez Hardwarem a uživatelem
**Neumanova Architektura** 
![[Pasted image 20250929090450.png]]
Procesor se skládá ze dvou částí
- Arytmickou logická jednotka 
- Řadič - řídící jednotka
	- na základě dekódovacích instrukcí ovládá ostatní části včetně aritmetické jednotky
### Zpracování informací v PC
Veškeré informace jsou zakódovány pomocí 0 a 1 (bool hodnoty).
**Analogové počítače** nepoužívají 0 a 1 ale třena na základě napětí el. proudu
### Zobrazení informací v PC
- **Zobrazení znaků** – v určené kódové soustavě
- **Zobrazení čísel** - ve dvojkové soustavě, v pevné nebo pohyblivé řádové čárce, v přímém, doplňkovém, inverzním kódu
Instrukce pokyny data
Program - soubor instrukcí pro nějaký úkol.
Zobrazení instrukcí
![[Pasted image 20250929152434.png]]
#### Číselný systém
Číslo je řada symbolů.
Každý symbol má váhu (hodnotu)
Každé číslo je součet matematických výrazů.
Každý výraz je dán součinem číselného symbolu a jeho váhy, přičemž váha je mocninou báze (základu). Mocnina (exponent) začíná nulou a roste po jedné(zprava doleva).
![[Pasted image 20250929153013.png]]
#### Váhy v dvojkové soustavě
![[Pasted image 20250929153233.png]]
#### Tabulka převodů mezi soustavami
![[Pasted image 20250929153341.png]]
### **Převody mezi soustavami** 
![[Pasted image 20250929153738.png]]
![[Pasted image 20250929155010.png]]
![[Pasted image 20250929155203.png]]
![[Pasted image 20250929160355.png]]
**Na zkoušce bude určitě nějaký takový jednoduchý příklad** (viz prezentace)
![[Pasted image 20250929160525.png]]
Při převodu mezi 10 a 16 soustavou si pomůžeme tím že ji převedeme na desítkovou na potom je rozdělíme po 4 číslech protože hodnoty je 0-15 odpovídají hodnotám 16 soustavy.
Obdobně tomu je i u osmičkové 3čísla dvojkové soustavy odpovídají hodnotám 0-7
![[Pasted image 20250929161150.png]]
![[Pasted image 20250929161406.png]]
![[Pasted image 20250929161517.png]]

#### Obecné uspořádání čísla v pevné řádové čárce
**pevná řádová čárka** - 1bit = znamínko, hodnoty = 2 na 7 - 127do127
	0 = kladné
	1 = záporné
**Přímí kód se nedá použít pro jednoduché sčítání** 
![[Pasted image 20250929164642.png]]
Kdy by jsme zobrazovali v Pevné řadové čárce tak jsme schopni zobrazit jen 4 miliardy
![[Pasted image 20250929171955.png]]
U doplňku provádíme inverzi kladného čísla 
$$
0,110 = 1,001 - inverze
$$
Potom k této inverzi musíme přičíst k nejméně významnému bitu jeden bit(1) 
**Pozor  při stavu 1+1 = 0 dochází k takzvanému carry a jeden byt si v podstatě držím. xd**
![[Pasted image 20250929172553.png]]
![[Pasted image 20250929173041.png]]
![[Pasted image 20250929174156.png]]
0,8128 a 8125 se na 4 bytech jeví stejné ale při delším rozvoji dojde k rozdílu.
![[Pasted image 20251003110931.png]]
#### Doplňkové sčítání
- odečítáme-li číslo, provedeme to jako přičtení doplňku odečítaného čísla
- Pokud při doplňkovém sčítání dojde k přenosu do vyššího řádu, je výsledek v normální formě.
	- Pokud k přenosu do vyššího řádu nedojde je výsledek  v dopňkové formě a je třeba provést následující kroky.
	1. Vytvořit doplněk k výsledku v doplňkové formě
	2. Změnit znaménko výsledku.
	- [ ] Pojebal el. Proud musím takže idk
### **Násobení**
![[Pasted image 20251003120011.png]]
### **Dělení**
![[Pasted image 20251003115825.png]]
### **Dělení s návratem ke kladnému zbytku**
1. Odečteme: Dělenec - dělitel výsledek je v A-B < 0 False(0) True(1)
2. Když je výsledek záporný dojde k návratu
	1. Přičteme: B+A
3. 1a2 potom opakuj pro všechny zbývající bity
![[Pasted image 20251003151807.png]]






#### Obecné uspořádání čísla v pohybové řádové čárce
Číslo se rozdělí na 3 části 
- **znaménko** pak **mantisa (platné číslice)**
- **exponent** - říká kde má být desetinná čárka
![[Pasted image 20250929093450.png]]
mantisa - číslo 1000 - mantisa je 1, 2000 - 2
**Avšak při operacích s pohyblivou řádovou čárkou dochází k malým chybám pro většinu výpočtů to není problém, ale třeba u financí už nastává problém Proto se pro ně zavedla třetí varianta BCD kód**

občas dojde k přetečení do znaménkového kódu proto se používá **Modifikovaný doplňkový kód**
zaporne (1), 0 značí že došlo k přetečení.
**V prezentaci jsou příklady**
   - [ ] Na dělení bez návratu ke kladnému zbytku atd. Mám se na něj kouknout
### Rotace bitů
![[Pasted image 20251003125508.png]]
### **Logický posun**
![[Pasted image 20251003125540.png]]
### **Aritmetický posun**
![[Pasted image 20251003125612.png]]
### Třetí varianta: Kód BCD
BCD zakóduje cifry do binárního Kód ne do dvojkové soustavy
![[Pasted image 20250929095723.png]]
![[Pasted image 20251003125843.png]]
### Aikenovy podmínky
1. Každé místo v kódu má mít určitou váhu.
2. Součet vah míst, v nichž je dvojková číslice kódu rovna 1, má dát hodnotu přiřazené desítkové číslice nebo alespoň, vetší desítkové číslici má odpovídat větší dvojkové číslo příslušného váhového kódu.
3. Vztah mezi lichými a sudými kódy a přiřazenými desítkovými číslicemi může být sice libovolný, ale u zvoleného kódu má být neměnný.
4. Desítkovým doplňkům desítkových číslic mají odpovídat doplňkové kódy, vzniklé inverzí jednotlivých bitů původního kódu
řešení pro Aikenovy podmínky +3
### Zabezpečení Kódu paritou
### Popis části počítače
Paměť je v podstatě repositář paměťových buněk
buňka - do ní se vleze je byte(8)
	-Každá buňka má jednozančnou přidělenou adresu
	-lze do ní zapsat novou informaci, s podmínkou, se zruší stará informace
	-při získání údajů ctením se obsah neporusí
**Údajový a Adresový registr Paměti**
adresový registr velikost u 32bit = 2<sup>32</sup>
adresový registr řekne kam
údajový registr - řekne co
řadič zapíše z údajového tam, kam řekne adresový
cash paměti - na pomezí disku a RAM
### Procesor
**Aritmeticko logická jednotka** - sčítačka
Řadič - 
-  Výběrová fáze - načtu instrukce
- Prováděcí fáze - Provedu instrukce



Asociativní vyhledávání
- nehledám na určitém místě  ale hledám pomocí jaké vlastnosti 

**Synchronizace periferii s procesorem**
metoda přerušením. přeruší se úkon a zapíše se do čítače instrukcí zapíše co už je hotovo, pak se zase k práci vrátí tam kde skončil.
DMA - procesor se odpojí(režim Hond), a řadič přenese data do paměti(Normálně do ní zapisuje procesor)

### Finnova Kategorizace 
4 typy
	-sisd (Neuman)
	-misd (Seriové, každý procesor provádí jinou operaci)
	-simd (Všchny provádí jednu instrukci na stejnými datami)