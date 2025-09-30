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
PREFIX - VLP
POSTFIX - LPV
#### Algoritmus slepé(Kusé) koleje 
Vyhodnocení Výrazu postfixu
#### Pomocí Zásobníkového Automatu
Příklad = 1;
## Normální formy výrokových formulí
![[Pasted image 20250930140522.png]]
### Algoritmus převodu formule do DNF
Pravdivostní tabulka
![[IMG_20250930_141008.jpg]]
#### Minimalizace výrokových formulí
## Karnaughova mapa
- na pořadí nezáleží
K-mapa - postup minimalizace
