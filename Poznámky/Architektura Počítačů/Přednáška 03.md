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
Pro konkrétní přiřazení hodnot do vstupů X1 , X2 , X3 spočteme postupně YPříklady booleovských výrazů