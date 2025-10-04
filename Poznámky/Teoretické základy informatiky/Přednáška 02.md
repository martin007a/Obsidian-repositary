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
2. Vyznačíme řádky v nichž je formule __pravdivá
3. Každý řádek bude odpovídat jedné klauzuli
4. Napášeme jednotlivé klauzule DNF
5. Je-li v daném řádku proměnná **pravdivá**, bude v klauzuli **bez negace**, je-li **nepravdivá**, bude v klauzuli **negována**
 ![[Pasted image 20251004192902.png]]
#### Algoritmus převodu formule do KNF
1. Vytvoříme pravdivostní tabulku
2. Vyznačíme řádky v nichž je formule **nepravdivá**
3. Každý řádek bude odpovídat jedné klauzuli
4. Napášeme jednotlivé klauzule KNF
5. Je-li v daném řádku proměnná **pravdivá**, bude v klauzuli ** negována**, je-li **nepravdivá**, bude v klauzuli **bez negace**
![[Pasted image 20251004193526.png]]

### Algoritmus převodu formule do DNF
Pravdivostní tabulka
![[IMG_20250930_141405.jpg]]
### Minimalizace výrokových formulí
##### Jak najít minimální tvar logické funkce?
- co nejméně použitých součástek při konstrukci obvodu 
- co nejefektivnější vyhodnocování podmínky v algoritmu
## Karnaughova mapa
- Zobrazení n-rozměrné tabulky do dvoj rozměrné mapy
- Mapa pro n nezávislých proměnných obsahuje 2<sup>n</sup> políček
- Každé políčko zastupuje jeden řádek pravdivostní tabulky 
###### Pří konstrukci se využívá **Grayův kód**
- dvě sousední políčka v mapě se liší o právě jeden bit
- podrobněji v rámci kódování dat (Předmět UICT)
###### Rychleji než matematická úprava úplné DNF/KNF
- Efektivní pro formule s nejvýše 4 proměnnými
###### Karnaughova mapa – příklad konstrukce
![[Pasted image 20251004204207.png]]
### K-mapa – postup minimalizace
Vytváříme smyčky (podmapy) podle těchto pravidel: 
 1. můžeme spojovat pouze navzájem sousední políčka 
 2. můžeme spojovat pouze políčka se stejnými hodnotami 
 3. počet políček ve vytvořené smyčce musí být roven 2<sup>𝑛</sup>  
 4. smyčky vytváříme co možná největší (prosté implikanty)
 5. snažíme se vytvořit co nejméně smyček (implikantů) 
 6. smyčky se mohou v mapě libovolně překrývat 
Každou smyčku poté vyjádříme jako součinový term nezávisle proměnných, jejichž hodnoty se v rámci dané smyčky nemění  
Logickým součtem jednotlivých součinových termů získáme minimální DNF (analogicky minimální KNF) 
Může existovat více rovnocenných řešení

# Kontrolní otázky
#### Co je to úplný systém logických spojek?
**Úplný systém logických spojek** je **taková množina logických spojek**, pomocí které lze **vyjádřit libovolnou výrokovou formuli**
#### Které spojky tvoří úplný systém logických spojek?
- negace, konjunkce a disjunkce
- negace a konjunkce
- negace a disjunkce
- negace a implikace
- NOR  
- NAND 
#### Jak je definována Shefferova a Peirceova spojka?
**Shefferova spojka** (nazývaná také **NAND**, anglicky _Not AND_) je negace konjunkce.
**Peirceova spojka** (nazývaná také **NOR**, anglicky _Not OR_) je negace disjunkce.
#### Co je to infixový, prefixový a postfixový zápis?
![[Pasted image 20251004210741.png]]
