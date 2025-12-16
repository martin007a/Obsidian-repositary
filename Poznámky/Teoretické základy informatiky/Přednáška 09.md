1 Co je graf?
	Graf je uspořádaná trojice $(U, H, f)$, kde $U$ je množina uzlů, $H$ je množina hran a $f: H \to U^2$ je incidenční zobrazení. Alternativní definice pro prosté grafy uvádí graf jako uspořádanou dvojici $(U, H)$, kde $U$ je množina uzlů a $H \subseteq U^2$ je množina hran.
**2 Co to znamená, že graf je prostý / orientovaný / neorientovaný / úplný / bipartitní / rovinný?**
- **Prostý graf:** Graf, který neobsahuje násobné hrany, se nazývá prostý.
- **Orientovaný graf (digraf):** Graf odpovídající základní definici, kde se rozlišuje počáteční a koncový uzel hrany, je orientovaný.
- **Neorientovaný graf:** Jestliže ke každé hraně $h$ existuje protisměrná hrana $h'$, jedná se o neorientovaný graf. Dvojice těchto hran je považována za jedinou a nerozlišuje se počáteční a koncový uzel.
- **Úplný graf ($K_n$):** Graf, ve kterém je každý uzel spojen se všemi ostatními uzly právě jednou neorientovanou hranou.
- **Bipartitní graf:** Graf, jehož množina uzlů je rozložena na dvě disjunktní třídy $U_1$ a $U_2$ ($U = U_1 \cup U_2$ a $U_1 \cap U_2 = \emptyset$), přičemž hrany spojují jen uzly z různých tříd.
- **Rovinný graf (planární):** Graf, k němuž existuje rovinné nakreslení. Rovinné nakreslení je takové zobrazení, v němž křivky zobrazující hrany mají společné nejvýše krajní body (obrazy uzlů).
3. Co je množina následníků / předchůdců / sousedů uzlu?
	Pro uzel $x$ platí:
	- **Množina následníků ($U_G^+(x)$):** Je to množina uzlů $z$ takových, že existuje hrana, pro kterou je $x$ počáteční uzel a $z$ koncový uzel (tedy $f(h)=(x,z)$).
	- **Množina předchůdců ($U_G^-(x)$):** Je to množina uzlů $z$ takových, že existuje hrana, pro kterou je $z$ počáteční uzel a $x$ koncový uzel (tedy $f(h)=(z,x)$).
	- **Množina sousedů ($U_G(x)$):** Je to sjednocení množiny následníků a množiny předchůdců ($U_G^+(x) \cup U_G^-(x)$). Uzly $x$ a $y$ se obecně nazývají sousední, jsou-li incidentní se stejnou hranou.
4. Co je vstupní / výstupní okolí uzlu?
	Pro uzel $x$ platí:
	- **Výstupní okolí ($H_G^+(x)$):** Je to množina hran, které vycházejí z uzlu $x$.
	- **Vstupní okolí ($H_G^-(x)$):** Je to množina hran, které vcházejí do uzlu $x$.
5. Co je vstupní / výstupní stupeň uzlu?
	Pro uzel $x$ platí:
	- **Výstupní stupeň ($d_G^+(x)$):** Je roven počtu hran ve výstupním okolí uzlu $x$ ($|H_G^+(x)|$), tedy počtu hran vedoucích z uzlu $x$.
	- **Vstupní stupeň ($d_G^-(x)$):** Je roven počtu hran ve vstupním okolí uzlu $x$ ($|H_G^-(x)|$), tedy počtu hran vedoucích do uzlu $x$.
	- **Celkový stupeň uzlu ($d_G(x)$):** Je součtem vstupního a výstupního stupně.
**6. Co je sled / tah / cesta / kružnice / cyklus?**
- **Sled (Walk):** Je střídavá posloupnost uzlů a hran $u_0, h_1, u_1, h_2, u_2, \dots, h_k, u_k$, kde každá hrana spojuje předchozí a následující uzel. Uzly i hrany se ve sledu mohou opakovat.
- **Tah (Trail):** Je sled, ve kterém se žádná hrana neopakuje.
- **Cesta (Path):** Je sled, ve kterém se neopakuje žádný vnitřní uzel. Každá cesta je také tah.
- **Kružnice (Circuit):** Je to uzavřená cesta v neorientovaném grafu.
- **Cyklus (Cycle):** Je to uzavřená orientovaná cesta.
3. Co je eulerovský tah?
	Eulerovský tah je takový tah, který obsahuje každou hranu grafu právě jednou. Graf je nazýván eulerovský, pokud v něm eulerovský tah existuje. Podmínkou existence uzavřeného eulerovského tahu je, že všechny uzly musí mít sudý stupeň; pro neuzavřený eulerovský tah musí mít právě dva uzly lichý stupeň.
**8. Co je hamiltonovská cesta / kružnice?**
- **Hamiltonovská cesta:** Cesta, která prochází každým uzlem v grafu, přičemž uzly se neopakují (každým projde právě jednou).
- **Hamiltonovská kružnice:** Je to uzavřená hamiltonovská cesta. Graf je hamiltonovský, jestliže v něm existuje hamiltonovská cesta.
**9. Co je souvislý / acyklický graf?**
- **Acyklický graf:** Graf, který neobsahuje kružnice (cykly).
- **Souvislý graf (neorientovaný):** Je souvislý, pokud mezi každými dvěma uzly existuje sled.
- **Souvislý graf (orientovaný):** Může být slabě souvislý (pokud je souvislá jeho symetrizace) nebo silně souvislý (pokud mezi každými dvěma různými uzly existuje orientovaný sled).
**10. Co je podgraf a komponenta grafu?**
- **Podgraf:** Neformálně řečeno, podgraf je „část grafu“ $G' = (U', H', f')$. Musí platit, že $U'$ je podmnožina uzlů $U$ původního grafu a $H'$ je podmnožina hran $H$ taková, že hrany v $H'$ spojují pouze uzly vybrané v $U'$. Pokud je $U' = U$, podgraf se nazývá faktor.
- **Komponenta grafu:** Každý maximální souvislý podgraf se nazývá komponenta. Počet komponent je důležitá charakteristika grafu.
**11. Co je (kořenový) strom a les?**
- **Les:** Prostý graf bez kružnic (tedy acyklický graf) se nazývá les.
- **Strom:** Souvislý les se nazývá strom. Les je graf, jehož každou komponentou je strom. Strom je také minimální souvislý graf na daných uzlech.
- **Kořenový strom:** Jedná se o orientovaný strom, který vznikne, jestliže se jeden uzel nazve kořenem a všechny hrany jsou orientovány směrem od tohoto kořene.