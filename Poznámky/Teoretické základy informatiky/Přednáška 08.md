
 25 
 35 relace jejíchž podmnožinou je identita
 36 Ke každá dvojici existuje její opačná
 37 K žádné dvovici nexistuje její opak, diagonála jsou nuly, a protilehlá políčka nesmí obsahovat dvě jedničky
 38 
 39
 41 
 44 Co je to zobrazení?
	 Jsou dány množiny 𝐴, 𝐵 a relace ℛ ⊆ 𝐴 × 𝐵. Relaci ℛ nazveme zobrazení právě tehdy, když (∀𝑎 ∈ 𝐴)(∃!𝑏 ∈ 𝐵)(𝑎ℛ𝑏).
	 - $A$ = definiční obor (domain).
	 - $B$ = obor hodnot (codomain).
 45 Co je to injekce? 
	 Zobrazení, kde se žádné dva různé prvky nezobrazí na stejné místo. "Každý má svou vlastní židli."
	 Je dáno zobrazení 𝑓 ∶ 𝐴 → 𝐵. Toto zobrazení nazveme injekce nebo prosté zobrazení, jestliže (∀𝑎1 , 𝑎2 ∈ 𝐴)(𝑓 (𝑎1 ) = 𝑓 (𝑎2 ) ⇒ 𝑎1 = 𝑎2 ).
 46 Co je to surjekce?
	 Zobrazení, kde je cílová množina $B$ zcela pokryta. Každý prvek z $B$ je obrazem alespoň jednoho prvku z $A$. "Všechny židle jsou obsazené." 
	- Je dáno zobrazení 𝑓 ∶ 𝐴 → 𝐵. Jestliže Im(𝑓 ) = 𝐵, zobrazení 𝑓 nazýváme zobrazením na množinu nebo též surjekce.
 47 Co je to bijekce? 
	 Zobrazení, které je zároveň **injektivní i surjektivní**.
	 - Je dáno zobrazení 𝑓 ∶ 𝐴 → 𝐵. Zobrazení 𝑓 nazveme bijekce právě tehdy, když je zároveň injekce a surjekce.
 48 Co je to složené zobrazení? 
	 Jsou dány množiny 𝐴, 𝐵, 𝐶 a zobrazení 𝑓 ∶ 𝐴 → 𝐵 a 𝑔 ∶ 𝐵 → 𝐶. Složeným zobrazením 𝑔 ∘ 𝑓 nazveme složenou relaci 𝑔 ∘ 𝑓 .
 49 Co je to inverzní zobrazení? 
	 Je dáno prosté zobrazení 𝑓 ∶ 𝐴 → 𝐵. Inverzním zobrazením k zobrazení 𝑓 nazveme zobrazení 𝑓 −1 ∶ Im(𝑓 ) → 𝐴 tak
 50 Jak určíme inverzi složeného zobrazení? 
 51 Co je to 𝑛-ární operace? 
 52 Co znamená, že operace je komutativní? 
 53 Co znamená, že operace je asociativní? 
 54 Co je to neutrální prvek? 
	 Prvek $e$, který při operaci s jakýmkoli jiným prvkem $a$ tento prvek nezmění.
 55 Co je to inverzní prvek?
	Prvek $a^{-1}$, který "vyruší" vliv prvku $a$ a výsledkem je neutrální prvek $e$.
## Zamyšlení
Jsou dány množiny 𝐴, 𝐵 takové, že |𝐴| = 𝑚, |𝐵| = 𝑛. 
1 Kolik existuje různých zobrazení 𝐴 → 𝐵? 
	$n^m$
2 Kolik existuje různých zobrazení 𝐵 → 𝐴?
	$m^n$
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
Na množině všech řetězců nad abecedou 𝛴 je dána operace zřetězení. 
1 Zdůvodněte, proč se jedná o operaci 
	Aby byla nějaká činnost považována za **binární operaci** na množině $M$, musí platit, že když vezmeme libovolné dva prvky z $M$, jejich výsledek musí **opět patřit do $M$**.
2 Rozhodněte, zda je tato operace komutativní 
	NE.
3 Rozhodněte, zda je tato operace asociativní 
ANO.
4 Nalezněte neutrální prvek 
5 Jak je to s inverzními prvky?
