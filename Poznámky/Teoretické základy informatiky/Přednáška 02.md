# Formy zápisu výrokových formulí
## Úplný systém logických spojek
Množina logických spojek L tvoří **úplný systém logických spojek**, jestliže ke každé formuli existuje formule, která je s ní logicky evivalentní a která obsahuje pouze spojky z L.
- Úplný systém logických spojek tvoří:
	- negace, konjunkce a disjunkce
	- negace a konjunkce
	- negace a disjunkce
	- negace a implikace
**Tabulka logických spojek**
![[Pasted image 20250930132845.png]]
## Spojky které tvoří vlastní systém
#### Shefferova spojka (NAND)
![[Pasted image 20250930133011.png]]
$$(¬a∨¬b) $$
![[Pasted image 20250930192658.png]]

![[Pasted image 20250930133053.png]]
K čemu to je?
Všechny spojky je možné  vyjádřit pomocí Shefferovy Spojky
#### NOR Peirceova spojka
![[Pasted image 20250930192843.png]]
![[Pasted image 20250930192905.png]]
![[Pasted image 20250930192927.png]]

![[Pasted image 20250930133439.png]]
Překladač jazyk si převádí do Postfixový zápis (PC)
### Převod z infixu do prefixu
#### Pomocí stromového rozkladu +1
INFIX - Levý podstrom - Vrchol - Pravý pod strom
![[Pasted image 20250930194529.png]]
PREFIX - VLP $$∧⇒a∨b¬c⇔¬ab$$
POSTFIX - LPV $$abc¬∨⇒a¬b⇔∧$$
#### Algoritmus slepé(Kusé) koleje 
**Algoritmus slepé koleje** 
- čteme výraz v infixu zleva doprava
-  proměnná pokračuje na výstup 
- operátor padá do zásobníku (slepé koleje) 
- Avšak negace jako jediná se vysype ze zásobníku při následujícím načtení nečeká v zásobníku jako ostatní spojky na pravou závorku.
- levá závorka padá do zásobníku (slepé koleje) 
- pravá závorka vyráží ze zásobníku vše až po levou závorku (závorky na výstup nepíšeme) 
- na konci vyprázdníme zásobník
![[Pasted image 20251004105724.png]]
## Vyhodnocení Výrazu postfixu
#### Pomocí Zásobníkového Automatu 
- čteme výraz zleva doprava   
- přečteme-li operand, uložíme jej na zásobník 
- přečteme-li operátor, vybereme ze zásobníku tolik operandů, kolik je arita operátoru, aplikujeme na ně operátor a výsledek uložíme zpět do zásobníku 
- po dočtení výrazu je v zásobníku pouze výsledek výrazu 
- Stejným způsobem lze převádět z postfixu do infixu
![[Pasted image 20251004185030.png]]
![[Pasted image 20251004185003.png]]
## Normální formy výrokových formulí
- Každé výrokové formuli přísluší právě jedna pravdivostní funkce - viz pravdivostní tabulka
- Každé pravdivostní funkci odpovídá nekonečně mnoho formulí, které jsou vzájemně ekvivalentní
Je užitečné stanovit nějaký normální tvar formule výběrem jedné či dvou z nekonečně mnoha ekvivalentních formulí.
- Třída ekvivalentních formulí je pak reprezentována touto vybranou formulí v normálním tvaru
##### Využití normálních forem
- Automatické vyhodnocování pravdivosti
- Dokazování vlastností formulí
- Základ pro další teoretické zkoumání
![[Pasted image 20250930140522.png]]
**Literál** je výroková proměnná nebo její negace.
### Disjunktivní normální forma
 Výroková formule je v **disjunktivní normální formě (DNF),** je-li disjunkcí formulí (klauzulí), pro které platí: 
 - Každá je konjunkcí literálů.
 - V žádné se nevyskytuje žádná atomická formule současně se svou negací.
 **DNF je úplná**, pokud jsou ve všech konjunkcích stejné atomické formule. 
### Konjunktivní normální forma
Výroková formule je **v konjunktivní normální formě (KNF),** jeli konjunkcí formulí (klauzulí), pro které platí:
- Každá je disjunkcí literálů,
- V žádné se nevyskytuje žádná atomická formule současně se svou negací.
**KNF je úplná**, pokud jsou ve všech disjunkcích stejné atomické formule.
### Nalezení DNF a KNF
Ke každé výrokové formuli lze nalézt ekvivalentní formuli v úplné DNF a KNF
- literál je sám o sobě v DNF i KNF
Úplná DNF/KNF je určena vždy jednoznačně až na pořadí literálů a klauzulí.
##### Jaký je algoritmus převodu do DNF/KNF? 
- pomocí pravdivostní tabulky 
- pomocí pravidel pro úpravy logických formulí
#### Algoritmus převodu formule do DNF
1. Vytvoříme pravdivostní tabulku
2. Vyznačíme řádky v nichž je formule pravdivá
3. Každý řádek bude odpovídat jedné klauzuli
4. Napášeme jednotlivé klauzule DNF
### Algoritmus převodu formule do DNF
Pravdivostní tabulka
![[IMG_20250930_141008.jpg]]
#### Minimalizace výrokových formulí
## Karnaughova mapa
- na pořadí nezáleží
K-mapa - postup minimalizace
