1. Co je graf?
	Graf je uspořádaná trojice (U, H, f), kde U je množina uzlů, H je množina hran, a f: H -> U x U je incidenční zobrazení. 
2. Co to znamená, že graf je prostý / orientovaný / neorientovaný / úplný / bipartitní / rovinný?
	• Prostý graf: Graf, který neobsahuje násobné hrany, se nazývá prostý.
	• Orientovaný graf (digraf): Graf odpovídající základní definici, kde se rozlišuje počáteční a koncový uzel hrany, je orientovaný.
	• Neorientovaný graf: Jestliže ke každé hraně h existuje protisměrná hrana h', jedná se o neorientovaný graf. Dvojice těchto hran je považována za jedinou a nerozlišuje se počáteční a koncový uzel.
	• Úplný graf (Kn): Graf, ve kterém je každý uzel spojen se všemi ostatními uzly právě jednou neorientovanou hranou.
	• Bipartitní graf: Graf, jehož množina uzlů je rozložena na dvě disjunktní třídy U1 a U2 (U = U1 sjednoceno s U2 a průnik U1 a U2 je prázdný), přičemž hrany spojují jen uzly z různých tříd.
	• Rovinný graf (planární): Graf, k němuž existuje rovinné nakreslení. Rovinné nakreslení je takové zobrazení, v němž křivky zobrazující hrany mají společné nejvýše krajní body (obrazy uzlů).

3. Co je množina následníků / předchůdců / sousedů uzlu?
Pro uzel x platí:
• Množina následníků (U_G+(x)): Je to množina uzlů z takových, že existuje hrana, pro kterou je x počáteční uzel a z koncový uzel (tedy f(h)=(x,z)).
• Množina předchůdců (U_G-(x)): Je to množina uzlů z takových, že existuje hrana, pro kterou je z počáteční uzel a x koncový uzel (tedy f(h)=(z,x)).
• Množina sousedů (U_G(x)): Je to sjednocení množiny následníků a množiny předchůdců. Uzly x a y se obecně nazývají sousední, jsou-li incidentní se stejnou hranou.

4. Co je vstupní / výstupní okolí uzlu?
Pro uzel x platí:
• Výstupní okolí (H_G+(x)): Je to množina hran, které vycházejí z uzlu x.
• Vstupní okolí (H_G-(x)): Je to množina hran, které vcházejí do uzlu x.

5. Co je vstupní / výstupní stupeň uzlu?
Pro uzel x platí:
• Výstupní stupeň (d_G+(x)): Je roven počtu hran ve výstupním okolí uzlu x, tedy počtu hran vedoucích z uzlu x.
• Vstupní stupeň (d_G-(x)): Je roven počtu hran ve vstupním okolí uzlu x, tedy počtu hran vedoucích do uzlu x.
• Celkový stupeň uzlu d_G(x) je součtem vstupního a výstupního stupně.

6. Co je sled / tah / cesta / kružnice / cyklus?
• Sled (Walk): Je střídavá posloupnost uzlů a hran u0, h1, u1, h2, u2, ..., hk, uk, kde každá hrana spojuje předchozí a následující uzel. Uzly i hrany se ve sledu mohou opakovat.
• Tah (Trail): Je sled, ve kterém se žádná hrana neopakuje.
• Cesta (Path): Je sled, ve kterém se neopakuje žádný vnitřní uzel. Každá cesta je také tah.
• Kružnice (Circuit): Je to uzavřená cesta v neorientovaném grafu.
• Cyklus (Cycle): Je to uzavřená orientovaná cesta.

7. Co je eulerovský tah?
Eulerovský tah je takový tah, který obsahuje každou hranu grafu právě jednou. Graf je nazýván eulerovský, pokud v něm eulerovský tah existuje. Podmínkou existence uzavřeného eulerovského tahu je, že všechny uzly musí mít sudý stupeň; pro neuzavřený eulerovský tah musí mít právě dva uzly lichý stupeň.

8. Co je hamiltonovská cesta / kružnice?
• Hamiltonovská cesta: Cesta, která prochází každým uzlem v grafu, přičemž uzly se neopakují (každým projde právě jednou).
• Hamiltonovská kružnice: Je to uzavřená hamiltonovská cesta. Graf je hamiltonovský, jestliže v něm existuje hamiltonovská cesta.

9. Co je souvislý / acyklický graf?
• Acyklický graf: Graf, který neobsahuje kružnice (cykly).
• Souvislý graf (neorientovaný): Je souvislý, pokud mezi každými dvěma uzly existuje sled.
• Souvislý graf (orientovaný): Může být slabě souvislý (pokud je souvislá jeho symetrizace) nebo silně souvislý (pokud mezi každými dvěma různými uzly existuje orientovaný sled).

10. Co je podgraf a komponenta grafu?
• Podgraf: Neformálně řečeno, podgraf je „část grafu“ G' = (U', H', f'). Musí platit, že U' je podmnožina uzlů U původního grafu a H' je podmnožina hran H taková, že hrany v H' spojují pouze uzly vybrané v U'. Pokud je U' = U, podgraf se nazývá faktor.
• Komponenta grafu: Každý maximální souvislý podgraf se nazývá komponenta. Počet komponent je důležitá charakteristika grafu.

11. Co je (kořenový) strom a les?
• Les: Prostý graf bez kružnic (tedy acyklický graf) se nazývá les.
• Strom: Souvislý les se nazývá strom. Les je graf, jehož každou komponentou je strom. Strom je také minimální souvislý graf na daných uzlech.
• Kořenový strom: Jedná se o orientovaný strom, který vznikne, jestliže se jeden uzel nazve kořenem a všechny hrany jsou orientovány směrem od tohoto kořene.

--- (Druhá část) ---

1. Co je cílem prohledávání grafu?
Cílem prohledávání grafu je systematická „návštěva“ všech uzlů v grafu. „Navštívit uzel“ znamená provést s ním nějakou operaci nebo se podívat, zda nese hledanou hodnotu. Prohledávání vždy začíná od zvoleného počátečního uzlu u0. Pro souvislé grafy prohledávání slouží také jako test souvislosti grafu, jelikož jsou na konci zpracovány všechny uzly.

2. Čím se liší prohledávání do šířky a do hloubky?
Prohledávání do šířky (Breadth-first search - BFS) a prohledávání do hloubky (Depth-first search - DFS) se liší především použitou datovou strukturou.
• Prohledávání do šířky využívá datovou strukturu FIFO – frontu. Při iteraci se odebere uzel z fronty, zpracuje se, a všichni neoznačení následníci uzlu se označí a vloží do fronty.
• Prohledávání do hloubky využívá datovou strukturu LIFO – zásobník. Při iteraci se odebere uzel ze zásobníku, zpracuje se, a všichni neoznačení následníci uzlu se označí a vloží do zásobníku.
Oba algoritmy prohledávání jsou základní algoritmy, na nichž jsou založeny další, a liší se pouze použitou datovou strukturou.

3. K čemu slouží Dijkstrův algoritmus?
Dijkstrův algoritmus slouží k nalezení nejkratší cesty z počátečního uzlu s do všech uzlů v hranově ohodnoceném grafu. Tato cesta má nejmenší možný součet hranových ohodnocení. Je důležité, že Dijkstrův algoritmus je použitelný pouze pro grafy s nezáporným ohodnocením hran.

4. Na jakém principu pracuje Dijkstrův algoritmus?
Dijkstrův algoritmus udržuje a rozšiřuje množinu zpracovaných uzlů (Z) a nezpracovaných uzlů (N). U každého uzlu udržuje značku (d, p), kde d je délka dosud nejkratší nalezené cesty z počátečního uzlu s, a p je bezprostředně předcházející uzel na této cestě.
Princip práce:
5. Inicializace: Uzel s má značku (0, -), ostatní uzly (nekonečno, -) a všechny jsou nezpracované.
6. Iterace: Dokud existují nezpracované uzly, vybere se ten nezpracovaný uzel w, který má minimální délku d.
7. Relaxace: Provedou se relaxace všech hran vedoucích z uzlu w do jeho nezpracovaných následníků.
8. Uzel w se nastaví jako zpracovaný.
9. Algoritmus může být ukončen, jakmile je zpracován cílový uzel.

10. Co je to relaxace hrany?
Relaxace hrany znamená přepočítání značky koncového uzlu hrany. Pokud je součet délky cesty do počátečního uzlu hrany a délky samotné hrany menší než aktuálně zaznamenaná délka cesty do koncového uzlu, pak se aktualizuje značka.
Formálně: Je-li zacatek(h).d + delka(h) < konec(h).d, pak se nastaví:
konec(h).d = zacatek(h).d + delka(h) a
konec(h).p = zacatek(h).

6. Na jakém principu pracuje Bellmanův-Fordův alg.?
Bellmanův-Fordův algoritmus je založen na prohledávání grafu do šířky (resp. relaxaci v cyklech). Na rozdíl od Dijkstrova algoritmu připouští hrany se záporným ohodnocením, ale nesmí existovat cyklus záporné délky. Stejně jako Dijkstrův algoritmus najde cesty z počátečního uzlu do všech uzlů v grafu.
Princip práce:
7. Inicializace: Uzel s dostane značku (0, -, 0), ostatní uzly (nekonečno, -, 0), kde třetí složka značí počet hran na cestě.
8. Iterace: Probíhá cyklus pro k < |U| (počet uzlů).
9. U každého uzlu, který je dostupný cestou o k hranách, se provede relaxace všech výstupních hran a nastaví se počet hran na k+1.
10. Do fronty se přidávají uzly, u nichž došlo ke změně značky.

11. Na jakém principu pracuje Floydův-Warshallův alg.?
Floydův-Warshallův algoritmus slouží k nalezení nejkratších cest mezi všemi dvojicemi uzlů. Také připouští hrany se záporným ohodnocením, ale nesmí existovat cyklus záporné délky.
Princip algoritmu je založen na opakovaném porovnávání a minimalizaci vzdáleností pomocí mezilehlého uzlu k:
aij = min(aij, aik + akj)
Vstupem je matice délek D, která se postupně upravuje na matici vzdáleností, a zároveň se konstruuje matice předchůdců P pro rekonstrukci cest.

8. Co je minimální kostra grafu?
Kostra grafu je takový podgraf, který obsahuje všechny uzly původního grafu a je to strom. Je to tedy souvislý acyklický podgraf, který je zároveň faktorem grafu. Cena (délka) kostry je definována jako součet délek hran.
Cílem hledání minimální kostry je nalezení propojení všech uzlů s nejmenším možným součtem hranových ohodnocení.

9. Na jakém principu pracuje Kruskalův algoritmus?
Kruskalův algoritmus slouží k nalezení minimální kostry.
Princip práce:
10. Inicializace: Vytvoří se graf G' tvořený pouze izolovanými uzly.
11. Příprava: Hrany původního grafu G se seřadí vzestupně podle hranového ohodnocení.
12. Iterace: Prochází se každá hrana v seřazeném pořadí a přidá se do G', pokud tím nevznikne v G' cyklus.
13. Kontrola cyklu se řeší přidělením identifikátoru každé komponentě: hranu lze přidat jen tehdy, pokud identifikátory počátečního a koncového uzlu hrany jsou různé. Po přidání hrany je nutné sjednotit identifikátory uzlů v dané komponentě. Přidáním každé hrany se sníží počet komponent grafu.

14. Jakým způsobem lze graf reprezentovat staticky?
Graf lze staticky reprezentovat pomocí matic. Mezi statické reprezentace patří:
• Matice sousednosti: Čtvercová matice řádu |U|, kde aij=1, pokud existuje hrana z ui do uj, a 0 jinak. Lze ji zobecnit pro multigrafy (počtem hran) a hranově ohodnocené grafy (hodnotou hrany).
• Matice incidence: Obdélníková matice |U|x|H|. Hodnoty jsou 1 (hrana vychází), -1 (hrana vchází) nebo 2 (smyčka). Lze ji zobecnit pro hranově ohodnocené grafy bez smyček.
• Matice délek: Používá se pro hranově ohodnocené grafy, kde aij je délka hrany, nekonečno značí neexistenci hrany a 0 pro i=j.
• Matice vzdáleností: Obsahuje délku nejkratší cesty mezi uzly ui a uj.
• Matice předchůdců: Zaznamenává předcházející uzel na nejkratší cestě z ui do uj.
• Halda (heap): Statická reprezentace prioritního stromu, realizovaná jako pole, kde uzly jsou určeny indexy.
Maticové reprezentace ovšem nemusí být paměťově efektivní, protože často obsahují mnoho nul (u řídkých grafů).

11. Jaké jsou možnosti dynamické reprezentace grafu?
Dynamické reprezentace grafu využívají datové struktury jako jsou seznamy a objekty. Patří mezi ně:
• Dynamický seznam sousedů (Adjacency List): Uzel má v sobě seznam následníků. Tato reprezentace umožňuje snadné prohledávání grafu.
• Dynamický seznam uzlů a hran: Zahrnuje samostatný seznam pro uzly a samostatný seznam pro hrany (implementace odpovídá definici grafu G=(U,H,f)). Tato metoda je vhodná například při hledání kostry, protože poskytuje přímý přístup k seznamu hran.
• Objektová reprezentace: Často se kombinuje s dynamickými seznamy, kde třída/objekt uzlu může obsahovat další informace o uzlu (pro uzlově ohodnocené grafy).
Pro běžné použití jsou nejvýhodnější dynamické seznamy, případně s pomocí hashů a indexů.