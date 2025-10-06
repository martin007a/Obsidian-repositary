# Principy digitální techniky, logické obvody a kombinační logika
## Booleova Algebra
**Booleova algebra** je počítání s jedničkami a nulami; tak počítá drtivá většina počítačů, které jsou na bázi logických obvodů
- místo 0 a 1 můžeme říkat true a false (pravda, nepravda)
### Boolenovské oprace
operace nad logickými hodnotami 0, 1, kdy výsledkem je zase 0 nebo 1
AND, OR, NOT, pak XOR a dále jejich kombinace NAND, NOR
### Operace AND, OR, NOT, XOR
- AND - logický **součin** (konjunkce)
- OR - logický **součet** (disjunkce)
- NOT - logická **negace** 
- XOR - logický výlučný součet, 
#### Pravdivostní tabulka AND, OR, NOT, XOR
![[Pasted image 20251006091210.png]]
#### Odvozené operace
- Negací operace XOR získáme operaci ekvivalence, rovnosti (EQ) 
- Negací operace AND získáme operaci NAND 
- Negací operace OR získáme operaci NOR

### Booleovské výrazy
- Primitivní hodnota (=term) 0, 1 (true, false) 
- Proměnné nabývající booleovských hodnot, značíme obvykle Xn, Yn, A… 
- Výše uvedené operace AND, OR, NOT, XOR, … 
- Závorky obsahující booleovský výraz ( booleovský výraz )
Nejsou-li použity závorky, obvykle bereme, že konjunkce (AND) má přednost před disjunkcí (OR) podobně jako má násobení přednost před sčítáním.
![[Pasted image 20251006091855.png]]
![[Pasted image 20251006092112.png]]
## Vyhodnocení výrazu
Pro konkrétní přiřazení hodnot do vstupů X1 , X2 , X3 spočteme postupně Y
![[Pasted image 20251006092547.png]]
#### Příklady booleovských výrazů
![[Pasted image 20251006092623.png]]
### Ekvivalence výrazů
- Z logického hlediska jsou výrazy Z a Y ekvivaletní
- Z = X1 OR X2 je jednodušší, kratší, vyhodnotitelný v jednom kroku; obvodově realizovatelný jediným hradlem OR.
- Je již minimalizovaný na nejmenší počet logických operací.
- Existuje obecný postup minimalizace výrazu.
## Zákony: Identitní, Nulový, Dvojitá negace
Neutrální prvek:
- A AND 1 = A: jednička nemění výsledek konjunkce 
- A OR 0 = A: nula nemění výsledek disjunkce
Absorpce (pohlcení):  
- A AND 0 = 0: nula určuje výsledek konjunkce 
- A OR 1 = 1: jednička určuje výsledek disjunkce
Dvojitá negace:
- ¬(¬(A)) = A: negace negace dá původní hodnotu
### Zákony: Komplementární, Komutativní, Asociativní
**A OR ¬A = 1** 
- vždy platí A nebo negace A (pravidlo vyloučeného třetího)
**A AND ¬A = 0**
- ale nikdy obě současně
**A OR B = B OR A a A AND B = B AND A**
- operace disjunkce a konjunkce jsou komunitativní, lze prohodit pořadí 
**A OR (B OR C) = (A OR B) OR C**
- asociativita = u stejných operací nezáleží na závorkování; obdobně A AND (B AND C) = (A AND B) AND C
## Zákony: Distributivní, Absorpční, De Morganův
**A AND (B OR C) = (A AND B) OR (A AND C), rovněž A OR (B AND C) = (A OR B) AND (A OR C)**
- "roznásobení" závorky, funguje pro obě operace AND i OR!
**A OR (A AND B) = A a také A AND (A OR B) = A**
- A rozhoduje o výsledku, tj. "pohltí" B
¬(A OR B) = ¬A AND ¬B, ¬(A AND B) = ¬A OR ¬B
- de Morganovy zákony (negace operace je totéž jako "opačná" operace nad negovanými vstupy)
**Další pravidla už jsou aplikací předchozích, so go ahead and use 'em :)**
## Zjednodušování booleovských výrazů
![[Pasted image 20251006093655.png]]
## Příklad zjednodušení výrazu
![[Pasted image 20251006093732.png]]![[Pasted image 20251006093748.png]]
![[Pasted image 20251006093806.png]]
### K čemu je logický obvod?
![[Pasted image 20251006094221.png]]
### Logické úrovně
![[Pasted image 20251006093909.png]]
### Napěťové úrovně
- Doposud jsme rozlišovali "nižší" a "višší" napěťové úrovně.
- záleží na použité technologii
![[Pasted image 20251006094146.png]]
# Třístavový Výstup (tri-state output)
![[Pasted image 20251006094409.png]]
## Stavy Logického obvodu

![[Pasted image 20251006094532.png]]
## Kombinační obvody
![[Pasted image 20251006094631.png]]
### Hradla
![[Pasted image 20251006094708.png]]
### Technické provedení
![[Pasted image 20251006094949.png]]
### Standardy schematického značení
![[Pasted image 20251006095423.png]]
![[Pasted image 20251006095444.png]]

9.4 až 9.7 na zkoušce nebude. jaj 
# Sčítačka
- Sčítačka (adder) je typickým příkladem (stále ještě) jednoduchého kombinačního obvodu. 
- Úkolem je sečíst v nejjednodušším případě dva bity (tzn. dvě jednobitová čísla) a dostat jeden bit jako výsledek.
## Reálně používané sčítačky
![[Pasted image 20251006100407.png]]
## Výlučné OR (exclusive-or)
![[Pasted image 20251006100501.png]]![[Pasted image 20251006100544.png]]
## Polosčítačka (half-adder)
![[Pasted image 20251006100654.png]]
Protože se dá použít jen na sečtení 1bitu , to je málo potřebovaly bychom zaznamenat Carry do víššího řádu.
## **Úplná sčítačka (full-adder)**
![[Pasted image 20251006100824.png]]


