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
	- Hlavičkový soubor, Obsahuje **deklarace a definice**,
		Dva tipy:
			- **Soubory, které jsou součástí instalace překladače** (**iostream**)
			- **Soubory, které si programátor napíše sám**
		Připojení knihovny (hlavičkového souboru) k programu se provádí pomocí **preprocesorové direktivy** **#include**
14. Co to jsou jmenné prostory v jazyce C++? 
	- Pojem **jmenný prostor** (_namespace_) v jazyce C++ slouží k organizaci prvků a je prostorem, kam jsou uloženy určité objekty
15. Která knihovna zahrnuje příkazy std::cin a std::cout ? K čemu tyto příkazy slouží? 
	- knihovna ``iostream
	- std::cin - vstupní proud pro standartní vstup
	- std::cout - výstupní proud pro standartní výstup
16. K čemu je v C++ konstrukce int main() ? 
	- Konstrukce **int main()** v jazyce C++ má **zásadní význam**, protože **reprezentuje celý program** ve vztahu k operačnímu systému a zajišťuje komunikaci s ním
	- Konstrukce `int main()` je ve své podstatě **hlavní funkce programu** nebo **hlavní podprogram programu**
17. K čemu slouží příkaz return 0; ve funkci main 
	- má zásadní význam pro **komunikaci mezi spuštěným programem a operačním systémem (OS)**
	- **Indikace bezchybného ukončení:** Hodnota **nula (****0****)** je **domluvená hodnota**, která indikuje **bezchybné ukončení** programu*
18. Jak zapíšete test, že vstupní hodnota se nachází v uzavřeném intervalu od 1 do 20?
	- if(a>1 and a<=20)
19. Jak zapíšete větvení do tří větví? 
```
if (Podmínka 1)
    // Příkazy pro Větev 1 (pokud je Podmínka 1 splněna)
else if (Podmínka 2)
    // Příkazy pro Větev 2 (pokud Podmínka 1 NENÍ, ale Podmínka 2 JE splněna) 
else 
    // Příkazy pro Větev 3 (pokud NENÍ splněna ani Podmínka 1 ani Podmínka 2) 
```
20. Co znamená zápis int i, j=5; ? Jakou hodnotu bude mít po skončení tohoto příkazu proměnná i ? nebude mi žádnou hodnotu, neinicializovanou
21. Předpokládejte, že proměnná kolik má hodnotu 10. Jak se změní hodnota proměnné Cislo po provedení příkazu Cislo= --kolik + Cislo; ? 
22. Jaký datový typ se používá pro zpracování znakové informace? 
	-char
23. Jak zapíšete test, že znaková proměnná obsahuje velké písmeno anglické abecedy? 
	- if(a>=65 and a<=90)
24. Jak se zapisují znakové a jak řetězcové konstanty?
	-char - ' a'
	-string - "ahoj"
25. Jak zjistíte, které ze dvou jmen je první podle abecedy? 
	-if (a<b) - pak **a** je první podle ABECEDY
26. Co je to rekurentní vztah
	-Rekurentní vztah (nebo **rekurence**) je matematická rovnice, která definuje prvek **sekvence** (posloupnosti) jako funkci **jedného nebo více předchozích prvků** téže sekvence.
27. Čím se liší globální a lokální proměnné?
	**Globální** je přístupná pro všechny podprogramy 
	**Lokání** jen pro určitý programový celek
28. Jaký je rozdíl mezi formálním a skutečným parametrem? 
	**Formální parametr se uvádí v hlavičce podprogramu při jeho definici**
	**Skutečná** je ta kterou zadáváme do hlavičky když program voláme
29. Existují parametry vstupní (volané hodnotou) a vstupně-výstupní (volané odkazem). Kdy se používají a jak se rozlišují? 
	- **Vstupní** parametr je ten který, se používá v podprogramu a zanikne při jeho konci
	 - **Vstupně-výstupní** jsou takové na které se odkážeme odkazem a všechny změní v podprogramu se na nich projeví i mimo něj
30. V čem se liší funkce od procedury? 
	**Procedura** - Provádí nějaký proces neočekává se od ní že vrátí nějakou hodnotu
	**Funkce** - Je od ní vyžadováno a by vracela nějakou hodnotu.
31. Co je to návratová hodnota podprogramu? 
32. Co znamená, že je podprogram rekurzivní? 
33. Jaké jsou výhody a nevýhody rekurze? 
34. Jaký je rozdíl mezi přímou a nepřímou rekurzí? 
35. V čem se liší lineární a stromová rekurze?