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
## 13. Co je a jak se připojí k danému programu knihovna?
* **Knihovna**: V programování chápána jako rozsáhlá množina již hotových, odladěných a optimalizovaných rekvizit, které lze v programu opakovaně použít.
* **Hlavičkový soubor**: Obsahuje deklarace a definice; rozlišujeme soubory překladače (např. `<iostream>`) nebo soubory vlastní (např. `"moje.h"`).
* **Připojení**: Provádí se pomocí preprocesorové direktivy `#include` na začátku zdrojového kódu.

## 14. Co to jsou jmenné prostory v jazyce C++?
* **Jmenný prostor**: (Namespace) slouží k organizaci prvků a je prostorem, kam jsou uloženy určité objekty, aby se zabránilo kolizím stejných názvů v různých částech kódu.

## 15. Která knihovna zahrnuje příkazy std::cin a std::cout? K čemu tyto příkazy slouží?
* **Knihovna iostream**: Základní knihovna pro standardní vstup a výstup.
* **std::cin**: Vstupní proud sloužící pro načítání dat ze standardního vstupu (zpravidla klávesnice).
* **std::cout**: Výstupní proud sloužící pro výpis dat na standardní výstup (zpravidla monitor).

## 16. K čemu je v C++ konstrukce int main()?
* **Význam**: Reprezentuje celý program ve vztahu k operačnímu systému a zajišťuje komunikaci s ním.
* **Podstata**: Je to hlavní funkce programu neboli hlavní podprogram, kde začíná samotné vykonávání kódu.

## 17. K čemu slouží příkaz return 0; ve funkci main?
* **Komunikace**: Má zásadní význam pro komunikaci mezi spuštěným programem a operačním systémem (OS).
* **Indikace**: Hodnota nula (0) je domluvená hodnota, která indikuje bezchybné ukončení programu.

## 18. Jak zapíšete test, že vstupní hodnota se nachází v uzavřeném intervalu od 1 do 20?
* **Zápis**: Používá se logický operátor AND: `if(a >= 1 && a <= 20)` nebo `if(a >= 1 and a <= 20)`.

## 19. Jak zapíšete větvení do tří větví?
* **Konstrukce**: Používá se struktura `if`, `else if` a `else`.
```cpp
if (Podmínka 1) // Příkazy pro Větev 1
else if (Podmínka 2) // Příkazy pro Větev 2
else // Příkazy pro Větev 3	  ```
```
## 20. Co znamená zápis int i, j=5; ? Jakou hodnotu bude mít po skončení tohoto příkazu proměnná i ?
* **Inicializace**: Proměnná `j` je inicializována na hodnotu 5.
* **Neinicializovaná proměnná**: Proměnná `i` nebude mít žádnou definovanou hodnotu, zůstane tzv. neinicializovaná (bude obsahovat náhodná data z paměti).
## 21. Předpokládejte, že proměnná kolik má hodnotu 10. Jak se změní hodnota proměnné Cislo po provedení příkazu Cislo= --kolik + Cislo; ? 
* **Prefixová dekrementace**: Hodnota proměnné `kolik` se nejdříve sníží na 9.
* **Výpočet**: Tato nová hodnota (9) se následně přičte k aktuální hodnotě proměnné `Cislo` a výsledek se do ní uloží.
## 22. Jaký datový typ se používá pro zpracování znakové informace? 
* **Znakový typ**: Pro zpracování znakové informace se v C++ používá základní datový typ `char`.
## 23. Jak zapíšete test, že znaková proměnná obsahuje velké písmeno anglické abecedy? 
* **Podmínka**: Zapíšeme ji jako `if(a >= 65 && a <= 90)` s využitím ASCII hodnot, nebo lépe čitelně `if(a >= 'A' && a <= 'Z')`.
## 24. Jak se zapisují znakové a jak řetězcové konstanty?
* **Znakové konstanty**: Zapisují se do jednoduchých apostrofů, například `'a'`.
* **Řetězcové konstanty**: Zapisují se do dvojitých uvozovek, například `"ahoj"`.
## 25. Jak zjistíte, které ze dvou jmen je první podle abecedy? 
* **Porovnání**: Použije se operátor menší než: `if (a < b)`. Pokud podmínka platí, je proměnná `a` abecedně dříve než `b`.
## 26. Co je to rekurentní vztah?
* **Definice**: Matematická rovnice, která definuje prvek sekvence (posloupnosti) jako funkci jednoho nebo více předchozích prvků téže sekvence.
## 27. Čím se liší globální a lokální proměnné?
* **Globální proměnné**: Jsou definovány vně všech podprogramů a jsou přístupné pro všechny části programu po celou dobu jeho běhu.
* **Lokální proměnné**: Jsou deklarovány uvnitř těla podprogramu, jsou použitelné pouze v něm a při jeho ukončení zanikají (uvolní se ze zásobníku).
## 28. Jaký je rozdíl mezi formálním a skutečným parametrem? 
* **Formální parametry**: Jsou uvedeny v hlavičce podprogramu při jeho definici a představují „prázdná nachystaná místa“, se kterými podprogram pracuje.
* **Skutečné parametry**: Jsou konkrétní hodnoty nebo proměnné, které zadáváme do závorek v okamžiku, kdy podprogram voláme (dosazují se za formální parametry).
## 29. Existují parametry vstupní (volané hodnotou) a vstupně-výstupní (volané odkazem). Kdy se používají a jak se rozlišují? 
* **Vstupní parametry (hodnotou)**: Hodnota se zkopíruje do podprogramu; změny uvnitř se neprojeví vně. Používají se, když potřebujeme data pouze předat k výpočtu.
* **Vstupně-výstupní parametry (odkazem)**: Formální parametr přebírá adresu skutečného parametru. Jakákoliv změna v podprogramu se přímo projeví i vně. V C++ se v hlavičce označují znakem `&`.
## 30. V čem se liší funkce od procedury? 
* **Funkce**: Má za cíl získat jednu výslednou hodnotu; musí mít určen datový typ a v těle obsahuje příkaz `return`.
* **Procedura**: Provádí sekvenci akcí (změny v paměti, výstup), ale nevrací hodnotu. V C++ se definuje pomocí klíčového slova `void`.
## 31. Co je to návratová hodnota podprogramu? 
* **Definice**: Je to hodnota, kterou funkce po svém provedení získá a předává ji zpět do místa, odkud byla vyvolána, pomocí příkazu `return`.
## 32. Co znamená, že je podprogram rekurzivní? 
* **Rekurze**: Podprogram je rekurzivní, pokud na základě technického principu ve svém těle obsahuje volání sama sebe.
## 33. Jaké jsou výhody a nevýhody rekurze? 
* **Výhody**: Nabízí jednodušší řešení složitých úloh (např. stromové struktury) a umožňuje automatickou úschovu dat v systémovém zásobníku.
* **Nevýhody**: Zvýšená režie, protože při každém volání vznikají nové lokální proměnné; u jednoduchých úloh bývá méně efektivní než cyklus.
## 34. Jaký je rozdíl mezi přímou a nepřímou rekurzí? 
* **Přímá rekurze**: Podprogram volá přímo sám sebe.
* **Nepřímá rekurze**: Nastává, když podprogram A volá podprogram B a ten následně volá zpět podprogram A.
## 35. V čem se liší lineární a stromová rekurze?
* **Lineární rekurze**: Funkce provede nejvýše jedno rekurzivní volání v každém kroku, čímž vytváří jednoduchý „řetěz“ volání.
* **Stromová rekurze**: Funkce provede dvě nebo více rekurzivních volání v jednom kroku, takže se volání dále větví jako koruna stromu.
## 36. Co je klíčové slovo?
* **Definice**: Identifikátor, jehož význam je v programovacím jazyce pevně určen a nelze jej změnit ani použít pro názvy vlastních proměnných (např. `int`, `while`).
## 37. Čemu se vyhýbáme, pokud píšeme program spouštěný z příkazového řádku?
* **Interaktivita**: Vyhýbáme se používání výstupů jako prostředku dialogu s uživatelem (např. vypisování dotazů a čekání na vstup), aby mohl být program snadno skriptován.
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
## 5.10 Kdy používáme vstupní a kdy výstupní parametr a jak se zapisuje v hlavičce podprogramu?
* **Vstupní parametry**: (Volané hodnotou) používáme, pokud hodnoty slouží pouze jako vstupy a nechceme, aby případné změny uvnitř podprogramu ovlivnily původní proměnné. V hlavičce se zapisují běžným způsobem: `datový typ identifikátor`.
* **Výstupní parametry**: (Volané odkazem) používáme, když potřebujeme vypočítané hodnoty dostat zpět do místa volání nebo měnit skutečné proměnné. V hlavičce se zapisují pomocí znaku ampersand `&` za datovým typem: `datový typ &identifikátor`.
## 5.11 Co se stane s hodnotami lokálních proměnných po skončení podprogramu?
* **Uložení v paměti**: Lokální proměnné jsou uloženy v tzv. systémovém zásobníku.
* **Zánik**: V okamžiku ukončení podprogramu jsou ze zásobníku odebrány, a tím automaticky zanikají.
## 5.12 K čemu slouží klíčové slovo return a kdy jej v podprogramu nepotřebujeme?
* **Účel return**: Slouží k okamžitému ukončení podprogramu a návratu k volajícímu příkazu. U funkcí navíc určuje návratovou hodnotu, kterou podprogram předává zpět.
* **Kdy není potřeba**: Příkaz `return` nepotřebujeme u procedur (podprogramy s typem `void`), kde se návratová instrukce vygeneruje automaticky na konci těla.
## 5.13 Pomocí kterého příkazu je možné načíst vstup znak po znaku včetně mezer a dalších oddělovačů?
* **Metoda cin.get(ch)**: Slouží k načtení jakéhokoliv znaku včetně mezer a konců řádků.
* **Rozdíl oproti >>**: Standardní operátor `>>` tzv. bílé znaky přeskakuje, zatímco metoda `get` načte vše.
## 5.14 Kdy je použití rekurzivního zápisu algoritmu nevhodné?
* **Jednoduché případy**: Rekurze je nevhodná tam, kde může být zápis složitější a méně efektivní než běžný cyklus (např. sčítání řady hodnot).
* **Vysoká režie**: Je nevýhodná kvůli vysokým nárokům na paměť, protože při každém volání dochází k nové deklaraci lokálních proměnných a ukládání návratových adres do zásobníku.
## 5.15 Při výpočtu N-tého prvku Fibonacciho posloupnosti se jedná o přímou/nepřímou lineární/stromovou rekurzi?
* **Typ rekurze**: Jedná se o **přímou stromovou rekurzi**.
* **Zdůvodnění**: Je přímá, protože podprogram volá přímo sám sebe. Je stromová, protože v každém kroku dochází ke dvěma rekurzivním voláním ($F_{n-1} + F_{n-2}$), což vytváří větvící se strukturu podobnou stromu.
## 5.16 Jaký je rozdíl mezi rekurentním vztahem a rekurzí?
* **Rekurentní vztah**: (Rekurence) je matematická rovnice, která abstraktně definuje člen posloupnosti pomocí členů předchozích.
* **Rekurze**: Je technický princip v programování, kdy podprogram ve svém těle skutečně obsahuje volání sama sebe, aby takový matematický vztah realizoval.
## 6.1 Co je strukturovaná proměnná?
* **Definice**: Strukturované proměnné reprezentují celý celek složený ze skupiny hodnot; slouží k uchovávání velkého množství dat současně v paměti počítače.
## 6.2 Jaké známe strukturované datové typy?
* **Pole**: Soubor prvků stejného typu přístupných přes index.
* **Záznam (struct)**: Seskupení položek rozdílných typů do jednoho logického celku.
* **Variantní záznam (union)**: Deklarované položky sdílejí v paměti stejný prostor.
## 6.3 Jak se definují datové typy?
* **typedef**: Slouží k přiřazení nového jména existujícímu typu.
* **enum**: Výčtový typ pro definování vlastních celočíselných hodnot výčtem jmen.
* **struct**: Klíčové slovo pro definici struktury záznamu.
## 6.4 Jak se definují konstanty?
* **Zápis**: Přidáním klíčového slova `const` k deklaraci proměnné; musí obsahovat inicializaci a její hodnotu nelze v programu měnit.
## 6.5 Jak se vytvoří pole?
* **Deklarace**: K obyčejné deklaraci proměnné se do hranatých závorek dopíše požadovaný počet prvků (složek).
## 6.6 Co je index, jaký může mít rozsah a jaké datové typy indexů lze používat?
* **Index**: Představuje pořadové číslo prvku v poli (musí to být celočíselný výraz).
* **Rozsah**: V C++ začínají indexy vždy nulou; pro pole o N prvcích je rozsah od 0 do N-1.
## 6.7 Co je záznam a jak se definuje?
* **Definice**: Datový typ (`struct`) pro sdružení položek rozdílných typů; položky jsou uzavřeny ve složených závorkách a identifikátor typu se uvádí před nimi.
## 6.8 Jak se uloží řada vstupních hodnot do pole?
* **Postup uložení**: Probíhá v cyklu (typicky `while`), přičemž je nutné provést několik kroků.
* **Deklarace**: Nejdříve se deklaruje pole s dostatečnou kapacitou $N$.
* **Čítač**: Použije se proměnná (např. `Pocet`), která sleduje index aktuální složky a celkový počet načtených prvků.
* **Podmínka čtení**: Musí hlídat kapacitu pole i dostupnost dat na vstupu: `while (Pocet < N && cin >> P[Pocet])`.
* **Inkrementace**: Po každém úspěšném načtení hodnoty se čítač zvýší.0
## 6.9 Jaký je princip algoritmu pro zjištění počtu podprůměrných hodnot vstupu?
* **Dvouprůchodový algoritmus**: Tento problém vyžaduje dva průchody, protože data nelze ze vstupu číst více než jednou.
* **První průchod**: Data se čtou, ukládají do pole a současně se vypočítává jejich součet a počet.
* **Mezikrok**: Po načtení všech dat se vypočítá aritmetický průměr jako $\text{součet} / \text{počet}$.
* **Druhý průchod**: Program prochází uložené pole prvek po prvku a porovnává je s průměrem; pokud je hodnota menší, zvýší se čítač podprůměrných hodnot.
## 6.10 Jak lze vypočítat ze dvou vstupních vektorů jejich skalární součin?
* **Princip výpočtu**: Vychází se ze zobecněného algoritmu pro práci s polem, kde se operuje s každým prvkem.
* **Algoritmus**: V cyklu `for` se vynásobí stejnolehlé prvky obou vektorů (např. $V1[i] \times V2[i]$).
* **Sumace**: Tyto dílčí součiny se postupně přičítají do sumární proměnné, která byla na začátku inicializována na nulu.
## 6.11 Jak se předává pole jako parametr podprogramu?
* **Způsob předání**: V jazyce C++ se pole vždy předává odkazem, respektive se předává adresa jeho první složky.
* **Zápis v hlavičce**: Pole se zapíše pomocí identifikátoru typu nebo jako datový typ s prázdnými hranatými závorkami (např. `float V[]`).
* **Informace o velikosti**: Protože podprogram dostává jen adresu, musí se s polem předat i celočíselná hodnota udávající počet obsazených položek.
* **Vedlejší efekt**: Jakákoliv změna složek pole uvnitř podprogramu se přímo projeví i v původní proměnné.
## 6.12 Jak se definuje pole záznamů?
* **Postup definice**: Nejprve se nadefinuje datový typ záznamu (`struct`) a následně se vytvoří pole, jehož bází je tento nadefinovaný typ.
* **Příklad**: `typedef Osoba TypSeznam[N];`, kde `Osoba` je dříve definovaná struktura
## 6.13 Jak se přistoupí k proměnné (složce záznamu), která je složkou pole?
* **Způsob přístupu**: Používá se kombinace indexace pole pomocí hranatých závorek a tečkové notace pro přístup k položce záznamu.
* **Syntaxe**: Zápis vypadá jako `JmenoPole[index].JmenoSlozky` (např. `Sklad[i].CenaKus`).
## 7.1 K čemu slouží příkazy setw(), right a setprecision()?
* **setw(x)**: Nastavuje šířku pole pro následující výstup na x znaků.
* **right**: Zarovnává vypisovanou hodnotu doprava v rámci nastavené šířky.
* **setprecision(p)**: Nastavuje přesnost (počet číslic) pro výpis desetinných čísel.
## 7.2 Ve které knihovně se uvedené příkazy nacházejí?
* **Knihovna**: Tyto formátovací manipulátory se nacházejí v knihovně `iomanip`.
## 7.3 Jak lze vytvářet v jazyce C++ vícerozměrná pole?
* **Princip**: Vícerozměrná pole vznikají tak, že jako datový typ složky pole určíme opět pole (např. pole polí vytvoří matici).
## 7.4 Jak se zpracovávají parametry zadané z příkazového řádku?
* **Předávání**: Hodnoty jsou předávány do funkce `main` pomocí parametrů: `int argc` (počet parametrů) a `char *argv[]` (pole řetězců s hodnotami).
## 7.5 Co je „null terminated string“ a jak se s ním pracuje?
* **Definice**: Je to pole znaků (`char`), kde konec textu označuje speciální nulový znak `\0`. Takto pracují standardní funkce pro řetězce v C.
## 8.1 Co je staticky alokovaná a dynamicky alokovaná paměť?
* **Statická paměť**: Vzniká při deklaraci v systémovém zásobníku, má pevnou velikost a existuje do konce bloku. Přistupuje se k ní přes identifikátor.
* **Dynamická paměť**: Vzniká za běhu programu na hromadě (halda) pomocí příkazu `new`. Velikost lze určit až v okamžiku vytvoření a přistupuje se k ní přes ukazatele.
## 8.2 Jaké zásadní výhody má dynamicky alokovaná paměť?
* **Výhody**: Flexibilní životnost (můžeme ji zrušit dříve), variabilní velikost a schopnost zpracovávat velmi velké objemy dat bez přetečení zásobníku.
## 8.3 Jaké nevýhody má práce s dynamicky alokovanou pamětí?
* **Nevýhody**: Režie spojená s nepřímým přístupem (přes ukazatele), nutnost manuální správy (uvolňování) a neefektivita u velmi jednoduchých typů.
## 8.4 Jak se vytváří datový typ ukazatel?
* **Deklarace**: Použitím znaku hvězdička `*` mezi datovým typem a názvem proměnné (např. `int *A`).
## 8.5 Jak se přistoupí k proměnné, na niž ukazuje nějaký ukazatel?
* **Dereference**: Provádí se operátorem `*` před ukazatelem (např. `*A`). U struktur se používá operátor šipka `A->slozka`.
## 8.6 Jaké operace se používají u fronty a jaké u zásobníku?
* **Operace**: Typicky jde o vkládání (push) a odebírání (pop) prvků na začátku nebo na konci struktury.
## 8.7 Co je binární strom a jak se implementuje každý jeho uzel?
* **Binární strom**: Struktura, kde každý uzel má nanejvýš dva následníky (levého a pravého syna).
* **Implementace**: Uzel se implementuje jako `struct` obsahující data a dva ukazatele na syny stejného typu.
## 9.1 Jakým způsobem se čte ze standardního vstupu?
* **Čtení**: Používá se objekt `std::cin` s operátorem `>>` (přeskakuje bílé znaky) nebo metoda `cin.get()` pro čtení včetně mezer.
## 9.2 Jakým způsobem se vypisuje na standardní výstup a na standardní chybový výstup?
* **Výstup**: Na standardní výstup pomocí `std::cout`, na chybový výstup pomocí `std::cerr` (vše přes operátor `<<`)
## 9.3 K čemu slouží operace cin, cout, cerr, clog a v jaké knihovně se nacházejí?
* **Proudy**: Slouží pro vstupy (`cin`), výstupy (`cout`) a chybová či stavová hlášení (`cerr`, `clog`). Vše je v knihovně `iostream`.
## 9.4 K čemu dochází při výměně dat mezi standardními soubory a operační pamětí?
* **Konverze**: Dochází k automatickému převodu mezi textovou podobou (znaky v souboru) a binární podobou (reálná data v paměti).
## 10.1 K čemu slouží příkazy setw(), right a setprecision()?
* **Formátování**: Slouží k nastavení šířky výstupního pole, zarovnání textu a určení počtu platných číslic u desetinných čísel.
## 10.2 Ve které knihovně se uvedené příkazy nacházejí?
* **Knihovna**: Nacházejí se v knihovně `iomanip`.
## 10.3 Jak se definuje datový typ záznam?
* **Zápis**: Pomocí klíčového slova `struct`, názvu typu a seznamu deklarací položek v závorkách `{}`.
## 10.4 Jak se přistupuje ke složkám záznamu?
* **Tečková notace**: Používá se zápis `jmeno_promenne.jmeno_slozky`.
## 10.5 Jaké řadicí algoritmy s kvadratickou časovou složitostí znáte?
* **Algoritmy**: Patří sem Select sort (přímý výběr), Bubble sort (bublinkové řazení) a Insert sort (přímé vkládání).
## 11.1 Jak se vypočítá adresa z indexu pole a s jakou časovou složitostí výpočet probíhá?
* **Vzorec**: $A = PA + (I - I_0) \times V$. Probíhá s konstantní časovou složitostí $O(1)$.
## 11.2 Jaký je obecný postup experimentálního stanovení časové složitosti?
* **Měření**: Spočívá v měření času běhu algoritmu pro různé velikosti vstupních dat (N) a následném vyhodnocení charakteru růstu této křivky.
## 11.3 Co je množina (multimnožina) a jaký je princip její implementace?
* **Množina**: Kolekce unikátních prvků (implementace polem `bool`).
* **Multimnožina**: Kolekce, kde se prvky mohou opakovat (implementace polem četností).
## 11.4 Které řadicí metody patří k lineárně logaritmickým a jaké mají vlastnosti?
* **Metody**: Quick sort, Heap sort a Merge sort. Mají časovou složitost $O(N \cdot \log N)$ a jsou velmi efektivní pro velká data.
## 11.5 Jaký je princip řazení množinou? Jaké výhody a nevýhody toto řazení má?
* **Princip**: Data se vloží do pole četností a pak se postupně vypisují podle počtu výskytů. Výhodou je extrémní rychlost $O(N)$, nevýhodou vysoká paměťová náročnost.
## 12.1 Jak se jmenuje knihovna umožňující práci s uživatelskými soubory?
* **Knihovna**: Práci se soubory umožňuje knihovna `fstream`.
## 12.2 Jakým způsobem se provede otevření binárního (netextového) souboru?
* **Otevření**: Při volání metody `open` je nutné uvést příznak `ios::binary`.
## 12.3 Jakými operacemi se provádí čtení a zápis dat v binárním souboru?
* **Operace**: Používají se metody `read` a `write`, které pracují s bloky bajtů (vyžadují přetypování na `char*`).
## 12.4 Co znamená get pointer (put pointer) a jakými operacemi jej lze zjisti nebo nastavit?
* **Ukazatele pozice**: `tellg/seekg` určují pozici pro čtení, `tellp/seekp` určují pozici pro zápis.
## 12.5 Co je bajtové (znakové) pole?
* **Definice**: Je to pole typu `char`, kde v binárním režimu chápeme každý prvek jako jeden bajt syrových dat.
## 12.6 Co je reference a jak se zapisuje?
* **Reference**: Odkaz na existující proměnnou, kdy formální parametr sdílí stejnou paměť jako skutečný parametr. Zapisuje se pomocí znaku `&`.

