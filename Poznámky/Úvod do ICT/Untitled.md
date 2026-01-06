## 1. Základní manipulace se soubory a cestami
- **`cd` (Change Directory):** Změna pracovního adresáře.
    - `cd ..` – posun o úroveň výš (do rodičovského adresáře).
    - `cd /` – posun do kořenového (root) adresáře.
- **`cp` (Copy):** Kopírování souborů a adresářů.
    - **Použití:** `cp [zdroj] [cíl]`
    - _Příklad ze zadání:_ `cp ../sbin/analyza.pdf .` (zkopíruje soubor z vedlejšího adresáře do aktuálního).
- **`rm` (Remove):** Mazání souborů.
    - `-r` – maže rekurzivně (nutné pro mazání složek).
    - `-f` – vynucené smazání bez ptaní.
    - _Příklad:_ `rm -r /err/critical` (smaže složku critical v adresáři /err).

--
## 2. Práce s textem a daty (Grep, Cut, Sort)

Tyto příkazy jsou klíčové pro filtrování řádků (jako v otázce č. 11 v prvním obrázku).
- **`grep`:** Vyhledávání textu pomocí vzorů.
    - `^` – hledá na začátku řádku (např. `grep '^8'` vybere řádky začínající osmičkou).
    - `-v` – invertovaný výběr (vypíše vše, co **neodpovídá** vzoru).
    - `-i` – ignoruje velikost písmen.
### Jak u `grep` zjistit počet (místo výpisu)
Pokud tě nezajímá, co v těch řádcích je, ale jen **kolik** jich je, použij přepínač **`-c`** (count).
- **Příkaz:** `grep -c "vzorek" soubor`
- **Příklad:** `grep -c "^8" ucastnici.txt` (vrátí ti jen jedno číslo – počet řádků začínajících osmičkou).
---
### Jak hledat jen "přesné slovo"
Standardně `grep` najde cokoli, kde se tvůj text vyskytuje (např. hledáš "auto" a on najde i "autobus"). Pokud chceš jen **přesné slovo**, máš dvě možnosti:
#### 1. Přepínač `-w` (Word regexp)
Hledá tvůj výraz jako celé slovo ohraničené mezerami nebo interpunkcí.
- **Příkaz:** `grep -w "objednavka" soubor`
- **Výsledek:** Najde "objednavka", ale ignoruje "objednavka_final" nebo "neobjednavka".
- **`cut`:** Rozřezání řádku na pole (sloupce). Často se používá pro CSV
    - `-d ' '` – definuje oddělovač (delimiter), např. mezera.
    - `-f 1` – vybere konkrétní pole (field), zde první.
    - _Příklad:_ `cut -d ' ' -f 1 info.txt` (vypíše první slovo z každého řádku).
- **`sort`:** Řazení řádků.
    - `-n` – řadí číselně (nikoliv abecedně).
    - `-r` – řadí sestupně (reverse).
- **`cat`:** Výpis obsahu souboru (nebo spojování souborů).
--
## 3. Oprávnění (Chmod)
V testu máš příklad na `chmod` (otázka č. 10). Oprávnění se dělí na **u**ser (vlastník), **g**roup (skupina) a **o**thers (ostatní).
- **Zkratky:** `r` (read/čtení), `w` (write/zápis), `x` (execute/spuštění).
- **Operátory:** `+` přidá právo, `-` odebere právo, `=` nastaví přesně daná práva.
- **Příklady:**
    - `chmod g-rw soubor` – skupině odebere čtení a zápis.
    - `chmod o=x soubor` – ostatním nastaví pouze právo spouštět.
    - `chmod a+rwx soubor` – všem (`a` jako all) přidá všechna práva.
--
### Anatomie zápisu oprávnění
Rozděl si ten řetězec na 4 části:
`[-] [rwx] [r-x] [r--]`
1. **První znak:** Určuje typ ( `-` je soubor, `d` je adresář/directory).
2. **První trojice (`u` - user):** Co smí **vlastník** souboru.
3. **Druhá trojice (`g` - group):** Co smí **skupina**.
4. **Třetí trojice (`o` - others):** Co smí **všichni ostatní**
---
### 🔢 Převod na čísla (Oktalová notace)
V testech se často setkáš s čísly (např. `chmod 755`). Každé písmeno má svou číselnou hodnotu

| **Písmeno** | **Význam**         | **Hodnota** |
| ----------- | ------------------ | ----------- |
| **r**       | read (čtení)       | **4**       |
| **w**       | write (zápis)      | **2**       |
| **x**       | execute (spuštění) | **1**       |
| **-**       | žádné právo        | **0**       |

Jak se to sčítá?
Pro každou trojici (vlastník, skupina, ostatní) sečteš hodnoty:
- `rwx` = 4 + 2 + 1 = **7** (plná práva)
- `r-x` = 4 + 0 + 1 = **5** (čtení a spuštění)
- `r--` = 4 + 0 + 0 = **4** (jen čtení)
- `---` = 0 + 0 + 0 = **0** (žádná práva)
**Příklad:** `chmod 754 soubor.txt`
- Vlastník: 7 (`rwx`)
- Skupina: 5 (`r-x`)
- Ostatní: 4 (`r--`)
---
### 🛠️ Jak číst příkazy ze zadání (Symbolická notace)
Když v testu vidíš příkaz jako `chmod g-rw ~/tar`, čti to takto:
1. **Kdo?**
    - `u` (user) = vlastník
    - `g` (group) = skupina
    - `o` (others) = ostatní
    - `a` (all) = všichni (vlastník + skupina + ostatní)
2. **Akce?**
    - `+` (přidat právo)
    - `-` (odebrat právo)
    - `=` (nastavit přesně, ostatní práva v té trojici se zruší)
3. **Co?**
    - `r`, `w`, `x`
**Příklad z tvého obrázku (úloha 10):**
4. `chmod a+rwx ~/tar` → **Všem** přidána všechna práva (`rwx`).
5. `chmod g-rw ~/tar` → **Skupině** sebráno čtení a zápis (zůstane jí jen `x`).
6. `chmod o=x ~/tar` → **Ostatním** se nastaví **pouze** spuštění (pokud měli `r` nebo `w`, přijdou o ně).
> [!ABSTRACT] Rychlý převod chmod
> - **7** = rwx (vše)
> - **6** = rw- (čtení + zápis)
> - **5** = r-x (čtení + spuštění)
> - **4** = r-- (jen čtení)
> - **0** = --- (nic)
> 
> **Příklad:** `chmod 644` je standard pro soubory (vlastník může vše kromě spouštění, ostatní jen čtou).
## 4. Masky souborů (Wildcards)
V Unixu se pro hromadné označování souborů používají tyto znaky:
- `*` – libovolný počet jakýchkoliv znaků (i nula).
    - _Příklad:_ `*objednavka*jp*` (soubor, který má v názvu "objednavka" a přípona začíná na "jp").
- `?` – právě jeden libovolný znak.
- `[abc]` – právě jeden znak z uvedených v závorce.
--
## 5. Přesměrování (Redirect)
Důležité pro ukládání výsledků příkazů do souboru.
- `>` – přesměruje výstup do souboru (přepíše existující obsah).
    - _Příklad:_ `sort soubor.txt > vysledek.txt`
- `>>` – přidá výstup na konec existujícího souboru
- `|` (Pipe/Roura) – pošle výstup jednoho příkazu jako vstup pro druhý.
    - _Příklad:_ `grep '^8' ucastnici.txt | sort` (vybere řádky začínající 8 a pak je seřadí).