1. Co je proměnná? 
	- místo v operační paměti, kam lze uložit určitou hodnotu odpovídajícího datového typu
2. Jaké základní řídicí struktury se v algoritmech vyskytují? 
	- **Větvení** (Úplné Neúplné) - If/Else, podmíněný výraz
	- **Cyklus** - While, do while, for
	- **Nepodmíněný skok** - goto, break, continue, return.
3. Jak tyto řídicí struktury budeme zobrazovat? 
4. Jaké existují typy výrazů?
	- **Logické výrazy:** Tyto výrazy zahrnují logické operátory (`&&`, `and`, `||`, `or`, `!`, `not`)
	- **Aritmetické výrazy:** Obsahují aritmetické operátory (`+`, `-`, `*`, `/`, `%`)
	- Porovnání **v == 1** je výraz, jehož výsledkem je logická hodnota **false** **nebo** **true**
	- Přiřazení **v = 1** je výraz,
5. Co je cyklus? 
	- **Cyklus** (neboli smyčka) představuje **možnost opakování nějaké posloupnosti příkazů**. Jedná se o velmi důležitou a často používanou součást algoritmů a patří mezi základní algoritmické obraty
6. Jaké existují druhy cyklů a čím se liší?
	- **Cyklus s podmínkou na začátku (např. příkaz** **while** **v C++):** Pokud není podmínka splněna, tělo cyklu **neproběhne ani jednou**. Tato varianta umožňuje zabránit zpracování nesprávných hodnot
	- **Cyklus s podmínkou na konci (např. příkaz** **do** **v C++):** Cyklus proběhne **minimálně jednou**
	- Počítaný Cyklus: U počítaného cyklu **víme dopředu, kolikrát se má jeho tělo opakovat**
		- **Inicializace:** Nastavení počátečních hodnot (např. řídicí proměnné).
		- **Podmínka:** Určuje, zda se má tělo cyklu opakovat
		- **Aktualizace:** Požadovaná změna, která se provede automaticky na konci těla cyklu (např. zvýšení řídicí proměnné)
7. Podle čeho se rozhodneme, který typ cyklu zvolit?
	- **Počítaný cyklus** (např. `for` v C++) - Tento typ cyklu je vhodný, když **dopředu víme, kolikrát se má jeho tělo opakovat**
	- **Podmíněný cyklus** 
		- A) Cyklus s podmínkou na začátku (např. `while` v C++)
			Tento cyklus je vhodný, pokud **tělo cyklu nemusí proběhnout ani jednou**
			- **Posloupnost zakončená nezahrnutelnou hodnotou**
		- B)- Cyklus s podmínkou na konci
			Tento cyklus se používá v situacích, kdy **je nutné, aby tělo cyklu proběhlo minimálně jednou**
			- **Posloupnost zakončená zahrnutelnou hodnotou**
8.  K čemu slouží datové typy? 
	-  specifikace povolených hodnot a povolených operací, které lze s těmito hodnotami provádět.
9. Jaké datové typy jsou k dispozici pro číselné hodnoty? 
	- ![[Pasted image 20251113144202.png]]
10. Jaké aritmetické operace jsou k dispozici u číselných datových typů?  
	- ![[Pasted image 20251113144230.png]]
11. Jaké operace s jednotlivými bity lze provádět u celočíselných hodnot? 
	-![[Pasted image 20251113144356.png]]
12. Jak se deklarují proměnné a k čemu slouží?
	Slouží:
	- 1. **Manipulace s daty:** Proměnné slouží jako **paměťová místa**, se kterými je následně možné **manipulovat při zpracování dat**.
	- **Uchování hodnoty:** V proměnné se uchovává **hodnota** odpovídající jejímu datovému typu
	- Deklarace proměnné je **požadavek k systému, aby v paměti vyhradil prostor** pro proměnnou. Tento požadavek zajišťuje vytvoření paměťového místa, které je vnitřně propojeno s názvem (identifikátorem) proměnné![[Pasted image 20251113144541.png]]
13. Co je a jak se připojí k danému programu knihovna? 
	- Knihovna je v programování chápána jako **rozsáhlá množina již hotových, odladěných a optimalizovaných rekvizit**, které lze v programu opakovaně použít
	- Hlavičkový soubor, obsahuje **deklarace a definice**
	- Dva typy: **Soubory součástí instalace překladače** (`iostream`) a **soubory, které si programátor napíše sám**
	- Připojení se provádí pomocí **preprocesorové direktivy #include**

14. Co to jsou jmenné prostory v jazyce C++? 
	- Pojem **jmenný prostor** (_namespace_) v jazyce C++ slouží k organizaci prvků a je prostorem, kam jsou uloženy určité objekty

15. Která knihovna zahrnuje příkazy std::cin a std::cout ? K čemu tyto příkazy slouží? 
	- Knihovna `iostream`
	- **std::cin** - vstupní proud pro standardní vstup
	- **std::cout** - výstupní proud pro standardní výstup

16. K čemu je v C++ konstrukce int main() ? 
	- Konstrukce **int main()** reprezentuje **celý program** ve vztahu k operačnímu systému a zajišťuje komunikaci s ním
	- Je to **hlavní funkce programu** nebo **hlavní podprogram programu**

17. K čemu slouží příkaz return 0; ve funkci main 
	- Má zásadní význam pro **komunikaci mezi spuštěným programem a operačním systémem (OS)**
	- Hodnota **nula (0)** je domluvená hodnota, která indikuje **bezchybné ukončení** programu

18. Jak zapíšete test, že vstupní hodnota se nachází v uzavřeném intervalu od 1 do 20?
	- `if(a >= 1 && a <= 20)` (nebo s použitím `and`)

19. Jak zapíšete větvení do tří větví? 
	- Pomocí konstrukce `if`, `else if` a `else`
	- Příklad:
	  ```cpp
	  if (Podmínka 1) // Větev 1
	  else if (Podmínka 2) // Větev 2
	  else // Větev 3
	  ```

20. Co znamená zápis int i, j=5; ? Jakou hodnotu bude mít po skončení tohoto příkazu proměnná i ?
	- Deklaruje dvě proměnné; `j` je inicializována na 5, ale `i` nebude mít **žádnou hodnotu (neinicializovaná)**

21. Předpokládejte, že proměnná kolik má hodnotu 10. Jak se změní hodnota proměnné Cislo po provedení příkazu Cislo= --kolik + Cislo; ? 
	- Hodnota `kolik` se nejdříve dekrementuje na **9** a poté se přičte k aktuální hodnotě `Cislo`

22. Jaký datový typ se používá pro zpracování znakové informace? 
	- Datový typ **char**

23. Jak zapíšete test, že znaková proměnná obsahuje velké písmeno anglické abecedy? 
	- `if(a >= 65 && a <= 90)` (případně `if(a >= 'A' && a <= 'Z')`)

24. Jak se zapisují znakové a jak řetězcové konstanty?
	- Znakové: `'a'` (jednoduché apostrofy)
	- Řetězcové: `"ahoj"` (dvojité uvozovky)

25. Jak zjistíte, které ze dvou jmen je první podle abecedy? 
	- `if (a < b)` - operátor porovnává řetězce lexikograficky, tedy podle abecedy

26. Co je to rekurentní vztah?
	- Matematická rovnice, která definuje prvek sekvence jako funkci **jednoho nebo více předchozích prvků** téže sekvence

27. Čím se liší globální a lokální proměnné?
	- **Globální** proměnná je přístupná pro všechny podprogramy
	- **Lokální** proměnná je přístupná jen pro určitý programový celek (funkci), ve kterém byla deklarována

28. Jaký je rozdíl mezi formálním a skutečným parametrem? 
	- **Formální parametr** se uvádí v hlavičce podprogramu při jeho definici
	- **Skutečný parametr** je konkrétní hodnota/proměnná, kterou zadáváme při volání programu

29. Existují parametry vstupní (volané hodnotou) a vstupně-výstupní (volané odkazem). Kdy se používají a jak se rozlišují? 
	- **Vstupní (hodnotou)**: Hodnota se zkopíruje a zanikne při konci podprogramu
	- **Vstupně-výstupní (odkazem)**: Sdílí místo v paměti a změny v podprogramu se projeví i mimo něj
	- Rozlišení: V C++ se označují znakem **&** v hlavičce definice

30. V čem se liší funkce od procedury? 
	- **Procedura**: Provádí sekvenci akcí, ale nevrací žádnou hodnotu (`void`)
	- **Funkce**: Musí vracet hodnotu určitého datového typu (příkaz `return`)

31. Co je to návratová hodnota podprogramu? 
	- Hodnota, kterou funkce po svém provedení získá a předává zpět do místa, odkud byla vyvolána

32. Co znamená, že je podprogram rekurzivní? 
	- Znamená to, že podprogram ve svém těle obsahuje **volání sama sebe**

33. Jaké jsou výhody a nevýhody rekurze? 
	- **Nevýhody**: Při každém volání se deklaruje nová lokální proměnná v zásobníku (režie)
	- **Výhody**: Automatická úschova dat přes systémový zásobník a jednodušší řešení složitých úloh

34. Jaký je rozdíl mezi přímou a nepřímou rekurzí? 
	- **Přímá**: Podprogram volá přímo sám sebe
	- **Nepřímá**: Podprogram A volá podprogram B a ten následně volá zpět podprogram A

35. V čem se liší lineární a stromová rekurze?
	- **Lineární**: Funkce provede nejvýše jedno rekurzivní volání v každém kroku (řetěz)
	- **Stromová**: Funkce provede dvě nebo více rekurzivních volání v jednom kroku (větvení)

36. Co je klíčové slovo?
	- Identifikátor, jehož význam je v jazyce pevně určen a nelze jej změnit (např. `int`, `while`)

37. Čemu se vyhýbáme, pokud píšeme program spouštěný z příkazového řádku?
	- **Používání výstupů jako prostředku dialogu s uživatelem** (vyhýbáme se interaktivitě)

5.1 Čím se liší globální a lokální proměnné?
	- **Lokální**: Deklarovány uvnitř podprogramu, v zásobníku, zanikají po ukončení
	- **Globální**: Definované vně, přístupné všem
	- Vzájemný vztah: Lokální proměnná se stejným jménem **zakryje** globální

5.2 Jaký je rozdíl mezi formálním a skutečným parametrem?
	- **Formální**: "Prázdná místa" v definici podprogramu
	- **Skutečné**: Konkrétní hodnoty dosazené při volání

5.3 Vstupní (hodnotou) vs. vstupně-výstupní (odkazem) parametry
	- **Hodnotou**: Kopírování dat, změny se neprojeví vně
	- **Odkazem**: Sdílení adresy v paměti přes znak **&**, změny se projeví vně

5.4 V čem se liší funkce od procedury?
	- **Funkce**: Vrací výsledek přes `return`
	- **Procedura**: Provádí akce bez návratu hodnoty (`void`)

5.5 Co je to návratová hodnota podprogramu?
	- Hodnota předávaná funkcí zpět do místa vyvolání

5.6 Co znamená, že je podprogram rekurzivní?
	- Že ve svém těle volá sám sebe

5.7 Jaké jsou výhody a nevýhody rekurze?
	- **Výhody**: Snazší správa paměti pro složité úlohy
	- **Nevýhody**: Vysoká režie zásobníku a paměti

5.8 Jaký je rozdíl mezi přímou a nepřímou rekurzí?
	- **Přímá**: A volá A
	- **Nepřímá**: A volá B a B volá A

5.9 V čem se liší lineární a stromová rekurze?
	- **Lineární**: Jeden řetězec volání
	- **Stromová**: Volání se větví jako koruna stromu

6.1 Co je strukturovaná proměnná?
	- Proměnná reprezentující celek složený ze skupiny hodnot (např. pole nebo záznam)

6.2 Jaké známe strukturované datové typy?
	- **Pole**, **Záznam (struct)** a **Variantní záznam (union)**

6.3 Jak se definují datové typy?
	- Pomocí klíčových slov `typedef`, `enum` nebo `struct`

6.4 Jak se definují konstanty?
	- Přidáním klíčového slova **const** a okamžitou inicializací hodnoty

6.5 Jak se vytvoří pole?
	- Doplněním hranatých závorek s počtem složek k deklaraci typu a jména

6.6 Co je index, jaký může mít rozsah a jaké datové typy indexů lze používat?
	- **Index**: Pořadové číslo prvku (celočíselný výraz)
	- **Rozsah**: V C++ vždy od **0** do **N-1**

6.7 Co je záznam a jak se definuje?
	- Datový typ `struct` sdružující různé typy položek do jednoho celku

7.1 K čemu slouží příkazy setw(), right a setprecision()?
	- **setw(x)**: Šířka výstupu, **right**: Zarovnání doprava, **setprecision(p)**: Přesnost desetinných míst

7.2 Ve které knihovně se uvedené příkazy nacházejí?
	- Nacházejí se v knihovně **iomanip**

7.3 Jak lze vytvářet v jazyce C++ vícerozměrná pole?
	- Vytvořením pole, jehož prvky jsou opět pole (pole polí)

7.4 Jak se zpracovávají parametry zadané z příkazového řádku?
	- Předávají se jako argumenty funkce `main`: `argc` (počet) a `argv` (pole řetězců)

8.1 Co je staticky alokovaná a dynamicky alokovaná paměť?
	- **Statická**: Vzniká při deklaraci v zásobníku (stack), pevná velikost
	- **Dynamická**: Vzniká za běhu na hromadě (heap) pomocí `new`, flexibilní

8.2 Jaké zásadní výhody má dynamicky alokovaná paměť?
	- Flexibilní životnost a variabilní velikost určitelná až za běhu

8.3 Jaké nevýhody má práce s dynamicky alokovanou pamětí?
	- Režie při přístupu přes ukazatele a nutnost ruční správy

8.4 Jak se vytváří datový typ ukazatel?
	- Použitím znaku **\*** mezi typem a jménem (např. `int *p;`)

8.5 Jak se přistoupí k proměnné, na niž ukazuje nějaký ukazatel?
	- Pomocí dereference `*p` nebo operátoru šipka `->` u struktur

8.7 Co je binární strom a jak se implementuje každý jeho uzel?
	- Dynamická struktura uzlů, kde každý má data a ukazatele na levého a pravého syna

9.1 Jakým způsobem se čte ze standardního vstupu?
	- Přes `std::cin` pomocí operátoru `>>` nebo metody `get()`

9.2 Jakým způsobem se vypisuje na standardní výstup a na standardní chybový výstup?
	- Standardní výstup: `std::cout`, Chybový výstup: `std::cerr` (nebo `std::clog`)

9.3 K čemu slouží operace cin, cout, cerr, clog a v jaké knihovně se nacházejí?
	- Slouží pro vstupy, výstupy a chybová hlášení; jsou v knihovně **iostream**

9.4 K čemu dochází při výměně dat mezi standardními soubory a operační pamětí?
	- K automatické konverzi mezi znakovou (textovou) a binární podobou dat

10.1 K čemu slouží příkazy setw(), right a setprecision()?
	- Formátování výstupu (šířka, zarovnání, přesnost) v knihovně `iomanip`

10.3 Jak se definuje datový typ záznam?
	- Klíčovým slovem `struct` a výčtem položek ve složených závorkách

10.4 Jak se přistupuje ke složkám záznamu?
	- Pomocí tečkové notace: `jmeno_promenne.jmeno_slozky`

10.5 Jaké řadicí algoritmy s kvadratickou časovou složitostí znáte?
	- **Select sort**, **Bubble sort** a **Insert sort**

11.1 Jak se vypočítá adresa z indexu pole a s jakou časovou složitostí výpočet probíhá?
	- Pomocí vzorce `A = PA + (I - I0) * V`; složitost je konstantní **O(1)**

11.3 Co je množina (multimnožina) a jaký je princip její implementace?
	- Datová struktura pro unikátní (množina) nebo opakované (multimnožina) prvky; implementace polem četností nebo bool hodnot

11.4 Které řadicí metody patří k lineárně logaritmickým?
	- **Heap sort**, **Quick sort** a **Merge sort** ($O(N \cdot \log N)$)

11.5 Jaký je princip řazení množinou?
	- Data se vloží do pole četností a sekvenčně vyčtou; složitost je lineární **O(N)**

12.1 Jak se jmenuje knihovna umožňující práci s uživatelskými soubory?
	- Knihovna **fstream**

12.2 Jakým způsobem se provede otevření binárního souboru?
	- Použitím příznaku `ios::binary` v metodě `open()`

12.4 Co znamená get pointer a put pointer?
	- **Get pointer**: Pozice pro čtení (`tellg`), **Put pointer**: Pozice pro zápis (`tellp`)

12.6 Co je reference a jak se zapisuje?
	- Odkaz na existující proměnnou sdílející stejnou paměť; zapisuje se pomocí znaku **&**

# 5. Podprogramy a jejich vlastnosti

## 5.1 Čím se liší globální a lokální proměnné?
* **Lokální proměnné**: 
	* Jsou deklarovány uvnitř těla podprogramu a jsou použitelné pouze v něm. 
	* Technicky jsou v okamžiku volání umístěny do **systémového zásobníku** a po ukončení podprogramu z něj odstraněny (zanikají).
* **Globální proměnné**: 
	* Jsou definovány vně podprogramů a jsou přístupné (viditelné) pro všechny podprogramy.
* **Vzájemný vztah**: 
	* Pokud má lokální proměnná stejné jméno jako globální, lokální prvek v zásobníku **zakryje** a znepřístupní prvek globální. 
	* Manipulace s globálními prvky uvnitř podprogramu se považuje za nevhodnou praxi (tzv. **vedlejší efekt**), která vede k nepřehlednému „špagetovému kódu“.

---

## 5.2 Jaký je rozdíl mezi formálním a skutečným parametrem?
* **Formální parametry**: Jsou uvedeny v hlavičce podprogramu při jeho definici. Představují „prázdná nachystaná místa“ (proměnné), se kterými pracují příkazy v těle podprogramu.
* **Skutečné parametry**: Jsou konkrétní hodnoty nebo proměnné, které zadáváme do závorek v okamžiku, kdy podprogram voláme. Při volání dochází k **dosazení (substituci)** skutečných parametrů na místa formálních.

---

## 5.3 Vstupní (hodnotou) vs. vstupně-výstupní (odkazem) parametry
* **Vstupní parametry (volané hodnotou)**: 
	* Hodnota skutečného parametru se zkopíruje do formálního. 
	* Skutečným parametrem může být jakýkoliv výraz. 
	* Změny provedené uvnitř podprogramu se neprojeví vně, protože po ukončení podprogramu formální parametry zanikají.
* **Vstupně-výstupní parametry (volané odkazem)**: 
	* Formální parametr přebírá **adresu** skutečného parametru, takže v paměti sdílejí stejné umístění. 
	* Skutečným parametrem musí být proměnná. Jakákoliv operace v podprogramu se přímo projeví i mimo něj.
* **Rozlišení**: V jazyce C++ se parametry volané odkazem označují v definici hlavičky znakem ampersand `&`.

---

## 5.4 V čem se liší funkce od procedury?
* **Funkce**: Jejím hlavním cílem je získání jedné výsledné hodnoty. Při definici musí mít určen datový typ této hodnoty a v těle obsahuje příkaz `return`.
* **Procedura**: Provádí sekvenci akcí (změny v paměti, výstup dat), ale neočekává se od ní vrácení hodnoty. V C++ se definuje pomocí klíčového slova `void` a příkaz `return` v ní není povinný.

---

## 5.5 Co je to návratová hodnota podprogramu?
Je to hodnota, kterou funkce po svém provedení získá a předává zpět do místa, odkud byla vyvolána. V C++ se k jejímu určení používá příkaz `return`, za nímž následuje výraz, jehož vyčíslením hodnota vznikne.

---

## 5.6 Co znamená, že je podprogram rekurzivní?
Podprogram je rekurzivní, pokud na základě technického principu ve svém těle obsahuje **volání sama sebe**.

---

## 5.7 Jaké jsou výhody a nevýhody rekurze?
* **Výhody**: Umožňuje automatickou úschovu dat v paměti (využívá systémový zásobník) a nabízí jednodušší řešení složitých úloh, které by jinak vyžadovaly manuální správu paměti.
* **Nevýhody**: Při každém volání dochází k deklaraci nové lokální proměnné a uložení návratové adresy do zásobníku, což zvyšuje režii. U jednoduchých úloh může být rekurzivní zápis složitější a méně efektivní než cyklus (**iterace**).

---

## 5.8 Jaký je rozdíl mezi přímou a nepřímou rekurzí?
* **Přímá rekurze**: Podprogram volá přímo sám sebe.
* **Nepřímá rekurze**: Nastává, když podprogram A volá podprogram B a ten následně volá zpět podprogram A.

---

## 5.9 V čem se liší lineární a stromová rekurze?
* **Lineární rekurze**: Funkce provede nejvýše jedno rekurzivní volání v každém kroku, čímž vytváří jednoduchý „řetěz“ volání.
* **Stromová rekurze**: Funkce provede dvě nebo více rekurzivních volání v jednom kroku. Tato volání se dále větví a vytvářejí strukturu podobnou stromu.