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
- Vyžaduje hluboké znalosti hardwaru a je obtížnější číst a zapisovat než jazyky na vysoké úrovni.
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
## Programátorský model
- abstrakce, která popisuje, jak programátor „vidí“ a může ovládat procesor při psaní nízkoúrovňového kódu – například v assembleru nebo při vývoji operačních systémů.
### Obecný programátorský model 8 bitového procesoru
![[Pasted image 20251027093109.png]]
- PC - čítač instrukcí
- R0 - 
- ACC - acumulátor
- Můžu vytváře shluky 16 bit registrů
- Zpracovává 8bitů na jednou - Adresuje 16 registrů
![[Pasted image 20251027093319.png]]
Aby mohl střádat 16 bit paměti musí 