**Algoritmus** je přesný návod nebo postup pro řešení zadané úlohy.
Vlastnosti Algoritmu:
- **Jednoznačnost** - v každém kroku algoritmu je jednoznačně určeno c ose bude dít, je odstraněn prvek náhody.
- **Konečnost** - Vždy dojde k nějakému výsledku
- **Opakovatelnost** - pro stejné vstupní hodnoty dostaneme stejný výsledek.
- **Hromadnost(Obecnost)** - algoritmus popisuje celou třídu podobných úloh
#### Co to je proměnná?
**Proměnná** - Je to místo v paměti počítače, které je určeno datovým typem který specifikuje jakých hodnot bude nabývat a jak s ní pracovat.  
#### Vyjádření Algoritmu
- **Slovně** - Vyjádřeno slovní formou např. recept v kuchařce. nevýhoda, každý může stejnou větu pochopit jinak.
- **Matematicky** - Nejčastěji vyjádřen matematickým vztahem mezi vstupními hodnotami.
- **Graficky** - Jednotlivé kroky jsou vyjádřeny pomocí grafických prvků, a doplněny popisy, např. **vývojový diagram.** 
	- **kopenogram** - záznamy jsou strukturovány a snáze převeditelné do PGR jazyka.
	- **struktogram** - určený k vyjádření strukturového přístupu.
- **Počítačové** - jediná forma přímo zpracovatelná počítačem, používá  se programovací jazyk, bývá konečným cílem tvorby algorytmů.
#### Kdy použijeme výraz a kdy příkaz?
##### Výraz
**Výraz je konstrukce**, která se vyhodnocuje (vypočítává) na jednu jedinou hodnotu.
- Výrazy se používají všude tam, kde potřebujeme **vypočítat nebo získat hodnotu**:
##### **Příkaz**
**Příkaz** je kompletní jednotka kódu, která provádí určitou akci.
##### Kdy ho použijeme?
Příkazy definují **postup a logiku algoritmu**:
- **Přiřazovací příkaz:** Ke změně hodnoty proměnné.
    - _Příklad:_ **`a = b + 5;`**
- **Podmíněný příkaz (větvení):** K provedení akce jen za určitých podmínek.
    - _Příklad:_ **`if (x > 10) { ... } else { ... };`**
- **Příkaz cyklu:** K opakování bloku kódu.
    - _Příklad:_ **`while (i < 10) { ... };`**
- **Volání funkce s vedlejším účinkem (I/O):** K interakci s okolím.
    - _Příklad:_ **`vypis("Dobrý den");`** (Vypíše text, ale nevrací hodnotu pro další výpočet.)
#### Co je to úplné a neúplné větvení?
U uplného větvení definuje i podmínku jak If tak Else

na pracovních listech se nacházejí otázky které bych měl pochopit před cvičením
Průběžné testy - v průběhu 30b / 2 (dva testy) 2 termíny bere se ten lepší výsledek.
Zkouškové testy - zkouškové 70 bodů Příklady(Algoritmy)
**min 60 bodů**
Bonusy - 
## Pojem Algoritmus
- Algoritmus je přepis úlohy; 
##### Vlastnosti
- Konečnost 
	- Každý algoritmus má jasně definovaný začátek a konec 
- Opakovatelnost
	- stejné vstupy = stejný výstup
- Jednoznačnost 
	-  Je jednoznačné jak bude probíhat
- Hromadnost
	-  Je určen pro řešení větší třídy úloh
##### Vyjádření Algoritmu
- Graficky
- Matematicky
- Přirozený jazyk
- Programovací jazyk
![[Pasted image 20251001200745.png]]
### Algoritmizace / Programování
- **Vytváření** (hledání, konstrukce) algoritmu = algoritmizace
- **Vyjádření** algoritmu v programovacím jazyce = programování
- **Tyto procesy jsou obvykle propojeny** – člověk vytváří algoritmus a přímo jej zapisuje v programovacím jazyce
### **Programovací paradigmata**
**Procedurální, imperativní**
- Tímto způsobem pracuje stroj
- Je masívní složitý, vzdálený člověku
**Funkcionální (tabulkové procesory)**
- Vzorce nám řeší problém nepíšeme kroky
**Logické (Prolog)**
	Zachytává proces
*  Nějaký algoritmus je schopen vyvodit nějaké nové vztahy
**Objektové (Smalltalk)**
- stojí na procedurální
#### Úroveň programovacích jazyků
- Strojový kód - 050A5F3C01
- Jazyk symbolických instrukcí - LDA POM (Závisí to na procesory který má elementární instrukce)
- Vyšší programovací jazyk - POM = POM * 5 (přesouváme problém na překladač)
- Jazyk 4. generace - (SQL) select *  from  zaci where id = 5
**Překladače**
- Programy které jsou schopné převést programy do jazyka srozumitelného stroji.
- **Generační** x Interpretační překladač - vezme náš zápis a převede na strojový kód - Pro běh rychle je lepší
- **Dávkové** x interaktivní aplikace- vezme jeden příkaz a hned ho provede a pak přičte další příkaz
### Programování
Vyjádření algoritmu pomocí programovacího jazyka
Výhoda: jednoznačnost zápisu
### **Zásadní Pojmy**
**Přístup k vývoji programů**
- Algoritmy + Datové struktury = Programy
- Původní účel: Počítač počítá, tj. pouze numerická data
- Rozvoj technologii: více informací, využívá se úschovný prostor.
**Datový** typ
- Souhrn povolených hodnot a povolených operací
- S hodnotami jsou obvykle svázány možnosti manipulace, tj. 
- algoritmy
__Proměnná
- Je to nějaké místo v paměti
- název proměnné = identifikátor
- Hodnota proměnné
__Konstanta
 - **Literál** = **pevně zapsaná hodnota v programu**
**C++**
- Generativní překladač - g++
- zápis textu (editor)
	- cpp-
	- ↓
	- g++
	- ↓
	- Zdrojový kód
	- a
	- ↓
	- spuštění
	- →./a→
# Cviko 01
### Algoritmus 
##### Vlastnosti
- Konečnost 
- Opakovatelnost
	- stejné vstupy = stejný výstup
- Jednoznačnost 
	-  Je jednoznačné jak bude probíhat
- Hromadnost
	-  Je určen pro řešení větší třídy úloh
##### Vyjádření Algoritmu
- Graficky
- Matematicky
- Přirozený jazyk
- Programovací jazyk
###### Grafické vyjádření algoritmu:
![[diagram_MIN-ABC.jpg]] [^2]

- [ ] Procvičit si vývojové diagramy  📅 2025-09-30  🔁
