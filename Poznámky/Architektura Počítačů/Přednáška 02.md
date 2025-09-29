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
Instrukce pokyny data
Program - soubor instrukcí pro nějaký úkol.
Zobrazení instrukcí
- jednoadresní
- dvouadresní
- tříadresní
#### Číselný systém
Číslo je řada symbolů.
Každý symbol má váhu (hodnotu)
Převody mezi soustavami 
**Na zkoušce bude určitě nějaký takový jednoduchý příklad** (viz prezentace)
#### Obecné uspořádání čísla v pevné řádové čárce
**pevná řádová čárka** - 2 na 8 - 127do127
	0 = kladné
	1 = záporné
Kdy by jsme zobrazovali v Pevné řadové čárce tak jsme schopni zobrazit jen 4 miliardy
Obecné uspořádání čísla v pohybové řádové čárce
![[Pasted image 20250929093450.png]]
mantisa - číslo 1000 - mantisa je 1, 2000 - 2

Přímí kód se nedá použít pro jednoduché sčítání 

Inverzní kód (prezentace)

Doplňkový kód

občas dojde k přetečení do znaménkového kódu proto se používá **Modifikovaný doplňkový kód**
zaporne (1), 0 značí že došlo k přetečení.
**V prezentaci jsou příklady**
   - [ ] Na dělení bez návratu ke kladnému zbytku atd. Mám se na něj kouknout
### Třetí varianta: Kód BCD
BCD zakóduje cifry do binárního Kód ne do dvojkové soustavy
![[Pasted image 20250929095723.png]]
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