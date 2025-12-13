1. soubor prvků se společnou vlastností
 25 
 35 relace jejíchž podmnožinou je identita
 36 Ke každá dvojici existuje její opačná
 37 K žádné dvovici nexistuje její opak, diagonála jsou nuly, a protilehlá políčka nesmí obsahovat dvě jedničky
 38 
 39
 41 
 44 
## Zamyšlení
Jsou dány množiny 𝐴, 𝐵 takové, že |𝐴| = 𝑚, |𝐵| = 𝑛. 
1 Kolik existuje různých zobrazení 𝐴 → 𝐵? 
	$m^n$
2 Kolik existuje různých zobrazení 𝐵 → 𝐴?
	$n^m$
3 Kolik z nich je injektivních? 
- Pokud je $m > n$ (prvků v $A$ je více než v $B$):
    Podle Dirichletova principu se musí nějaké prvky "mačkat" na stejný obraz.
    Počet: $0$ (žádné injektivní zobrazení neexistuje).
- Pokud je $m \leq n$:
    Pro první prvek máme $n$ možností, pro druhý už jen $n-1$, atd. Jde o variace bez opakování.
    Vzorec: $\frac{n!}{(n-m)!}$
4 Kolik z nich je bijektivních?
	Bijekce musí být zároveň injektivní (prostá) a surjektivní (na celou množinu). To vyžaduje, aby obě množiny měly **stejný počet prvků**.
	- Pokud $m \neq n$:
	    Nelze spárovat prvky 1:1.
	    Počet: $0$  
	- Pokud $m = n$:
	    Jde o permutace prvků. Prvnímu přiřadíme libovolný z $n$, druhému libovolný ze zbylých atd.
	    Vzorec:  $n!$
