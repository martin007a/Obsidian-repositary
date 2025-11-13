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
14. Co to jsou jmenné prostory v jazyce C++? 
15. Která knihovna zahrnuje příkazy std::cin a std::cout ? K čemu tyto příkazy slouží? 
16. K čemu je v C++ konstrukce int main() ? 
17. K čemu slouží příkaz return 0; ve funkci main ?