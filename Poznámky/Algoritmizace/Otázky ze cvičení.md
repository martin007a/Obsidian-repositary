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
	**Procedura** - Provádí sekvenci nějakých akcí proces neočekává se od ní že vrátí nějakou hodnotu (**void)**
	**Funkce** - Je od ní vyžadováno a by vracela nějakou hodnotu. (datový typ )
31. Co je to návratová hodnota podprogramu? 
	- Návratová hodnota podprogramu je **hodnota, kterou funkce (typ podprogramu) po svém provedení získá a předává zpět do místa, odkud byla vyvolána**
32. Co znamená, že je podprogram rekurzivní? 
	- Rekurzivní podprogram je definován na základě jednoduchého **technického principu**: **podprogram ve svém těle obsahuje volání sama sebe**
Formulace a ukončení rekurze
33. Jaké jsou výhody a nevýhody rekurze? 
	- Nevýhody rekurze
		Při každém zavolání rekurzivní funkce se provádí **deklarace nové lokální proměnné**
		V některých jednoduchých případech (např. při sčítání řady hodnot) může být rekurzivní zápis algoritmu **poněkud složitější** než iterativní řešení
	- Výhody rekurze
		-**Automatická úschova dat:** Rekurze je výhodná, pokud úloha **vyžaduje úschovu zpracovávaných údajů v paměti**
		-**Jednodušší řešení složitých úloh:** Rekurze je **opakování s využitím systémového zásobníku**
34. Jaký je rozdíl mezi přímou a nepřímou rekurzí? 
	 - **Přímá rekurze:** Podprogram ve svém těle přímo volá sám sebe
	- **Nepřímá rekurze:** Nastává, když podprogram A volá podprogram B, a ten následně volá zpět podprogram A.
35. V čem se liší lineární a stromová rekurze?
	- Lineární rekurze nastává, když funkce provede **nejvýše jedno** rekurzivní volání v každém kroku. V podstatě se jedná o jednoduchý, přímý "řetěz" volání.
	- Stromová rekurze nastává, když funkce provede **dvě nebo více** rekurzivních volání v každém kroku. Každé volání se pak rozvětvuje, což vytváří strukturu podobnou stromu.
36. Co je klíčové slovo?
	 - **Klíčové slovo** (Keyword) je identifikátor, jehož význam je pevně určen a nelze jej změnit pr. **int float While**
37.  Čemu se vyhýbáme, pokud píšeme program spouštěný z příkazového řádku nebo skriptu operačního systému?
	- **Používání výstupů jako prostředku dialogu s uživatelem**


## dalsi Otayky
6.1 Co je strukturovaná proměnná?

Strukturované proměnné reprezentují celý celek, který je složen ze skupiny hodnot. Slouží k uchovávání velkého množství hodnot současně v paměti počítače.

----------------------------------------------------------------

6.2 Jaké známe strukturované datové typy?

• Pole: Nejrozšířenější koncept strukturované proměnné.
• Záznam (struct): Používá se pro seskupení položek rozdílných typů do jednoho celku.
• Variantní záznam (union): Deklarované položky sdílejí stejný paměťový prostor.

----------------------------------------------------------------

6.3 Jak se definují datové typy?

• typedef: Přiřazuje nové jméno existujícímu typu nebo odvození jiného typu.
• enum: Výčtový typ pro definování vlastních celočíselných hodnot výčtem.
• struct: Slouží pro definici struktury záznamu.

----------------------------------------------------------------

6.4 Jak se definují konstanty?

Definují se přidáním klíčového slova const k obyčejné deklaraci proměnné.
• Inicializace: Deklarace musí obsahovat vložení počáteční hodnoty.
• Neměnnost: Hodnotu nelze dále v programu měnit.
• Hodnota: Může být uvedena i jako výraz, ale musí být vyčíslitelný v době překladu (obsahuje pouze jiné konstanty).

----------------------------------------------------------------

6.5 Jak se vytvoří pole?

Pole se vytvoří tak, že se k "obyčejné" deklaraci proměnné do hranatých závorek dopíše požadovaný počet prvků (složek). Počet složek je nutné určit v okamžiku deklarace.

----------------------------------------------------------------

6.6 Co je index, jaký může mít rozsah a jaké datové typy indexů lze používat?

• Index: Představuje pořadové číslo prvku pole. Může jím být jakýkoliv celočíselný výraz.
• Rozsah: V C++ mají pole vždy počáteční index I0 = 0. Pro pole o N složkách je rozsah <0, N-1>.

----------------------------------------------------------------

6.7 Co je záznam a jak se definuje?

Záznam je datový typ (struct), který slouží ke sdružení položek rozdílných typů do jednoho celku (např. atributy osoby).
• Definice: Pomocí klíčového slova struct.
• Obsah: Posloupnost položek (deklarace typu a identifikátoru zakončená středníkem) uzavřená ve složených závorkách. Identifikátor nového typu se uvádí před seznam položek.

================================================================

7.1 K čemu slouží příkazy setw(), right a setprecision()?

Jedná se o manipulátory pro formátování výstupu:
• setw(x): Nastavuje šířku výstupu na x znaků (platí pouze pro první následující výraz).
• right: Zarovnává hodnotu ve výstupu doprava.
• setprecision(p): Nastavuje přesnost desetinných čísel na p číslic.

----------------------------------------------------------------

7.2 Ve které knihovně se uvedené příkazy nacházejí?

Manipulátory setw a setprecision jsou obsaženy v knihovně iomanip.

----------------------------------------------------------------

7.3 Jak lze vytvářet v jazyce C++ vícerozměrná pole?

V jazyce C/C++ existují pouze jednorozměrná pole. Vícerozměrná pole lze vytvořit tak, že složkou pole je opět pole (pole polí).

----------------------------------------------------------------

7.4 Jak se zpracovávají parametry zadané z příkazového řádku?

Hodnoty jsou předávány do funkce main pomocí jejích parametrů:
1. První parametr (int pocet): Obsahuje počet parametrů (vždy min. 1, protože nultý je název programu).
2. Druhý parametr (char *param[]): Odkaz na pole řetězců s hodnotami jednotlivých parametrů.

----------------------------------------------------------------

7.5 Co je „null terminated string“ a jak se s ním pracuje?

8.1 Co je staticky alokovaná a dynamicky alokovaná paměť?

Staticky alokovaná paměť (Statické proměnné):
• Vznik: Při deklaraci (vyhradí se úsek odpovídající datovému typu).
• Umístění: Systémový zásobník.
• Životnost: Existují až do ukončení programového bloku, kde byly deklarovány.
• Velikost: Pevná, daná datovým typem.
• Přístup: Jsou uloženy na adrese symbolicky vyjádřené jejich identifikátorem.

Dynamicky alokovaná paměť (Dynamické proměnné):
• Vznik: Až za běhu programu speciálním příkazem.
• Umístění: Větší část paměti zvaná hromada (halda/heap).
• Velikost: Lze určit až v okamžiku vytvoření.
• Přístup: Nemají vlastní identifikátor, přistupuje se k nim přes adresy uložené v ukazatelích.

----------------------------------------------------------------

8.2 Jaké zásadní výhody má dynamicky alokovaná paměť?

1. Flexibilní životnost: Proměnná vzniká jen když je potřeba a lze ji kdykoliv zrušit (uvolnit paměť).
2. Variabilní velikost: Velikost lze určit až v okamžiku vytvoření.
3. Efektivní správa velkých dat: I velká struktura zabírá v zásobníku jen místo pro adresu (ukazatel), což obchází omezení paměti zásobníku.
4. Komplexní struktury: Umožňuje spojování do rozsáhlých dynamických struktur.

----------------------------------------------------------------

8.3 Jaké nevýhody má práce s dynamicky alokovanou pamětí?

1. Režie přístupu: Získání hodnoty vyžaduje dvojí přístup do paměti (nejprve získání adresy z ukazatele, poté přístup k hodnotě).
2. Režie ukazatelů: Nutnost správy ukazatelů pro svázání struktury.
3. Neefektivita u jednoduchých typů: U jednoduchých datových typů je tento způsob málo efektivní.

----------------------------------------------------------------

8.4 Jak se vytváří datový typ ukazatel?

Ukazatel je proměnná obsahující adresu.
• Deklarace: Použitím znaku hvězdička (*) mezi datovým typem a identifikátorem.
• Příklad: "int *A" (určitý ukazatel, ukazuje na typ int).
• Obecný ukazatel: Deklaruje se pomocí prázdného typu "void *X".

----------------------------------------------------------------

8.5 Jak se přistoupí k proměnné, na niž ukazuje nějaký ukazatel?

Přístup se provádí tzv. dereferencí:
• Základní přístup: Operátor hvězdička (*) před proměnnou (např. *A).
• Přístup ke složkám struktury (záznamu):
  a) Pomocí závorek a tečky: (*Z).slozka
  b) Pomocí operátoru šipka (preferované): Z->slozka

----------------------------------------------------------------

8.6 Jaké operace se používají u fronty a jaké u zásobníku?

Podle poskytnutých materiálů nejsou konkrétní názvy operací (jako push/pop) explicitně uvedeny.
• Obecná manipulace: Se seznamem se manipuluje typicky pouze s prvky na začátku nebo na konci.
• Systémový zásobník: Využívá se pro ukládání návratových adres a lokálních proměnných při volání podprogramů (zejména u rekurze).

----------------------------------------------------------------

8.7 Co je binární strom a jak se implementuje každý jeho uzel?

Binární strom:
Pravidelný strom, kde je počet následníků uzlu omezen nejvýše na dva. Častou variantou je Binární vyhledávací strom (BVS), kde platí uspořádání: Levý syn < Otec < Pravý syn.

Implementace uzlu:
Řešena pomocí dynamické struktury (záznamu), která obsahuje:
1. Datovou složku (TypData Data nebo void *Data).
2. Ukazatel na levého syna (TypUzel *Vlevo).
3. Ukazatel na pravého syna (TypUzel *Vpravo).
Celý strom je reprezentován ukazatelem na kořen.
----------------------------------------------------------------
9.1 Jakým způsobem se čte ze standardního vstupu?

Standardní vstup v C++ je reprezentován objektem std::cin (knihovna iostream).
• Pro jednoduchý vstup dat se používá operátor vložení >> (např. std::cin >> proměnná;).
• Dochází k automatické konverzi ze znakového tvaru do binárního.
• Operátor >> standardně vynechává bílé znaky (mezery, entery).
• Pro čtení znaků včetně bílých znaků lze využít metodu cin.get(ch);.

----------------------------------------------------------------

9.2 Jakým způsobem se vypisuje na standardní výstup a na standardní chybový výstup?

• Standardní výstup: Objekt std::cout. Používá se operátor << (např. std::cout << výraz;).
• Standardní chybový výstup: Objekt std::cerr (pro chyby) a std::clog (pro logy).
• Odřádkování: Používá se znak \n nebo manipulátor std::endl.

----------------------------------------------------------------

9.3 K čemu slouží operace cin, cout, cerr, clog a v jaké knihovně se nacházejí?

Nacházejí se v knihovně iostream a jmenném prostoru std.
• std::cin: Vstupní proud pro standardní vstup.
• std::cout: Výstupní proud pro standardní výstup.
• std::cerr: Standardní chybový výstup (console error), určený pro chybová hlášení.
• std::clog: Výstup pro záznamy (console log), např. info o úspěšném dokončení.

----------------------------------------------------------------

9.4 K čemu dochází při výměně dat mezi standardními soubory a operační pamětí?

Standardní soubory jsou logicky textové. Dochází k automatické konverzi:
• Při čtení (vstup): Konverze ze znakové podoby na binární podobu v paměti (aby šlo data zpracovat).
• Při zápisu (výstup): Konverze obsahu paměti na posloupnost znaků (člověkem čitelná podoba).

================================================================

10.1 K čemu slouží příkazy setw(), right a setprecision()?

Příkazy pro formátování výstupu:
• setw(x): Nastavuje šířku výstupu na x znaků (platí jen pro nejbližší výraz).
• right: Zarovná hodnotu ve výstupu doprava.
• setprecision(p): Nastavuje přesnost desetinných čísel na p číslic.

----------------------------------------------------------------

10.2 Ve které knihovně se uvedené příkazy nacházejí?

Manipulátory setw, setprecision (a setfill) jsou v knihovně iomanip.

----------------------------------------------------------------

10.3 Jak se definuje datový typ záznam?

Používá se klíčové slovo struct pro seskupení položek rozdílných typů s logickou souvislostí.
• Syntax: struct Identifikátor { typ polozka; ... };
• Příklad:
  struct Osoba { 
      string Jmeno; 
      int Plat; 
      float Hmotnost; 
  };

----------------------------------------------------------------

10.4 Jak se přistupuje ke složkám záznamu?

Pomocí tečkové notace: jméno_proměnné.jméno_složky.
Příklad: Franta.Jmeno

----------------------------------------------------------------

10.5 Jaké řadicí algoritmy s kvadratickou časovou složitostí znáte?

Mají složitost O(N^2) a jsou vhodné spíše pro malá data.
• Přímý výběr (Select sort)
• Bublinové řazení (Bubble sort)
• Přímé vkládání (Insert sort)

================================================================

11.1 Jak se vypočítá adresa z indexu pole a s jakou časovou složitostí výpočet probíhá?

• Vzorec: A = PA + (I - I0) * V
  (Kde PA je počátek pole, I je index, I0 je první index (v C++ 0), V je velikost složky).
• Složitost: Výpočet probíhá s konstantní časovou složitostí O(1).

----------------------------------------------------------------

11.2 Jaký je obecný postup experimentálního stanovení časové složitosti?

Měří se spotřebovaný čas (nebo prostor) pro různé velikosti vstupních dat (N). Výsledky se zanesou do tabulky a na jejich základě se interpoluje/extrapoluje charakter složitosti.

----------------------------------------------------------------

11.3 Co je množina (multimnožina) a jaký je princip její implementace?

• Množina (Set): Prvky se neopakují. Implementace pomocí pole bool hodnot (index = prvek, hodnota = je/není).
• Multimnožina (Multiset): Prvky se mohou opakovat. Implementace pomocí pole čísel (index = prvek, hodnota = počet výskytů).

----------------------------------------------------------------

11.4 Které řadicí metody patří k lineárně logaritmickým a jaké mají vlastnosti?

Složitost O(N * logN).
• Metody: Řazení hromadou (Heap sort), Quick sort, Merge sort, řazení binárním stromem.
• Vlastnosti:
  - Quick sort: Jeden z nejrychlejších obecně, průměrně k*N*logN.
  - Heap sort: Práce in situ (bez další paměti), nestabilní.
  - Merge sort: Sekvenční přístup, dříve vhodný pro vnější média.

----------------------------------------------------------------

11.5 Jaký je princip řazení množinou? Jaké výhody a nevýhody toto řazení má?

• Princip: Data se vloží do multimnožiny (pole četností) a pak se sekvenčně vyčtou.
• Výhoda: Nejnižší složitost O(N) - lineární.
• Nevýhoda: Není univerzální (data musí sloužit jako indexy), velká paměťová náročnost při velkém rozsahu hodnot.

================================================================

12.1 Jak se jmenuje knihovna umožňující práci s uživatelskými soubory?

Knihovna fstream.

----------------------------------------------------------------

12.2 Jakým způsobem se provede otevření binárního (netextového) souboru?

Při otevření (metoda open) se musí specifikovat režim ios::binary.
Příklad: Vstupy.open("../data/zdroje.txt", ios::binary);

----------------------------------------------------------------

12.3 Jakými operacemi se provádí čtení a zápis dat v binárním souboru?

• Čtení: soubor.read(pole, M); (nutné přetypovat na char*). Počet přečtených bajtů zjistí gcount().
• Zápis: soubor.write(pole, M); (nutné přetypovat na char*).

----------------------------------------------------------------

12.4 Co znamená get pointer (put pointer) a jakými operacemi jej lze zjisti nebo nastavit?

• Get pointer: Pozice pro čtení. Zjištění: tellg(), Nastavení: seekg(index).
• Put pointer: Pozice pro zápis. Zjištění: tellp(), Nastavení: seekp(index).

----------------------------------------------------------------

12.5 Co je bajtové (znakové) pole?

V binárních souborech se data chápou jako sled bajtů. Jelikož bajt v C++ odpovídá typu char, každé pole typu char (znakové pole) lze chápat jako bajtové pole.

----------------------------------------------------------------

12.6 Co je reference a jak se zapisuje?

Reference (odkaz) znamená, že formální parametr sdílí stejné místo v paměti jako skutečný parametr.
• Zápis: Pomocí znaku & v definici.
• Příklad: TypUzel &S.

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