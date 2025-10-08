#### Teorie Informace
- Nejvíce matematizovaná disciplína současné informatiky
- Formáty Souborů - Ztrátová a bezztrátová komprese
- Datové přenosy - kódování, kapacita kanálů
- Počítačové sítě - Pokročilé modulace signálů
- Hazardní hry - Stanovení kurzu
- Filozofie - Příjímání dat z okolí a nakládání s nimi
- Fyzika - východisko k hledání teorie všeho
- Jazykověda - strojové překlady, matematická lingvistika
#### Údaje 
hodnoty získané měřením, pozorováním nebo pouhým zaznamenáním reálné skutečnosti
###### Příklad
Na váhu v sýpce nasypeme dodávku obilovin a zjistíme, že ručička se zastavila na hodnotě 471.
#### Data
- kvalitativně nebo kvantitativně formalizované údaje
- vyjádření skutečnosti schopné přenosu, uchování, interpretace či zpracování
	když si údaje z displeje váhy dohodnutým způsobem poznačíme, stávají se z nich data,
- sama o sobě data nehmotná, i když pro jejich uložení potřebujeme hmotné médium
###### Příklad
Údaj „471“ si zaznamenáme jako „0,471 t“, tím jsme získali data o krmivech, která můžeme dále zpracovávat.
#### Interpretace dat
Data v PC představují 1 a 0, Pro člověka musejí být vhodně zobrazeny.
- zobrazení stejné posloupnosti jedniček a nul může být provedeno nekonečně mnoha způsoby
- přisouzením významu zobrazeným údajům data interpretujeme
##### Datový typ
- Je množinou povolených hodnot a množinou povolených operací
- **Implementace** - přisouzením posloupnosti binárních hodnot v paměti počítače
- Přidělením datového typu určujeme velikost prostoru v paměti, na kterém budou data uložena v binárním kódu,
**Modelujeme objektivní realitu**
- hodnoty jsou zobrazeny pro vstup i výstup
- Příklad: datové tipy v Excelu
##### **Informace**
- smysluplné interpretace dat a vztahů mezi nimi
- snižují neznalost a vyvolávají změnu stavu čí chování příjemce
- množství informace je vždy relativní vzhledem k k určitému příjemci a určité situaci
##### **Znalosti**
- ucelený komplex informací o nějaké objektivní realitě
- výsledek poznávacího procesu, předpoklad uvědomělé činnosti, umožňují porozumět skutečnosti
### Chápání
**Kvalitativní hledisko**
- získávání, uchovávání, zpracování a přenos informací
- zkoumá informatika
**Kavantitativní hledisko**
- množství informace ve zprávě a jeho měření
- kódování a dekódování zpráv
- přenos zpráv
- zkoumá teorie informace
## Pojem informace
- Poslední v prezentaci je asi nejlepší "ph.D Haluza"
	- „Informace jsou údaje, čísla, znaky, povely, instrukce, příkazy, zprávy apod. Za informace považujeme také podněty a vjemy přijímané a vysílané živými organismy.“
### Základní pojmy
###### **Systém** - Komplex prvků a vazeb ve vzájemné interakci
###### **Informační systém**
- dynamický systém
- vazby tvoří informace
- prvky jsou místa transformace informací
**Využití informačního systému**:
- poskytování potřebných informace v požadovaném rozsahu, lhůtách, podrobnostech i formě
- dílčí úlohy: sběr informací, přenos, redukce, archivace, zpracování, distribuce
### Složky informačních systémů
![[Pasted image 20251001153840.png]]
#### Měření množství informace ve zprávě 
Americký fyzik **Claude Elwood Shannon** 
 - položení základů teorie informace
 - stanovení možností měření informačního množství
**Shannonova definice:** "Informace je míra množství neurčitosti nebo nejistoty o nějakém náhodném ději odstraněná realizací tohoto děje"
- Množství informace ve zprávě lze měřit podle toho, o kolik se sníží neurčitost nebo nejistota, když zprávu přijmeme a pochopíme
**Informační entropie**
**Entropie** - míra neurčitosti
- míra neurčitosti, která se odstraňuje přijetím zprávy
- vyjadřuje množství informace obsažené ve zprávě
![[Pasted image 20251001154345.png]]

#### Exkurze do kombinatoriky
#### **Variace**
**Variace 𝑘-té třídy z 𝑛 prvků** je každá uspořádaná 𝑘-tice vytvořená z celkového počtu 𝑛 prvků, přičemž při výběru záleží na pořadí jednotlivých prvků.
- Záleží na pořadí jednotlivých pravků
Bez Opakování
![[Pasted image 20251001154751.png]]
Každý člověk lze vybrat jen jednou
![[Pasted image 20251001154837.png]]
Každý může být víckrát
#### **Permutace**
![[Pasted image 20251001154926.png]]
#### **Kombinace**
![[Pasted image 20251001154953.png]]
### Požadované vlastnosti funkce pro výpočet množství informace
![[Pasted image 20251001155330.png]]
#### __Výpočet vlastní Informace
![[Pasted image 20251001155350.png]]
- log menší než 1 vrací záporná čísla proto tam je -log
**Aplikace Vlastní informace**
![[Pasted image 20251001155932.png]]
**Řešený příklad** 
![[Pasted image 20251001160911.png]]
#### Eutropie
![[Pasted image 20251001161109.png]]
Prý jedinný vzoreček
### Praktické použití entropie
![[Pasted image 20251001161408.png]]
![[Pasted image 20251001161512.png]]
![[Pasted image 20251001161705.png]]
![[Pasted image 20251001161838.png]]
Soutěž
![[Pasted image 20251001162100.png]]
![[Pasted image 20251001162116.png]]
![[Pasted image 20251001162152.png]]
Důležité není jestli uhodl ale že se dozví co je správná odpověď
#### Odvození nejmenší míry informace
![[Pasted image 20251001162944.png]]
![[Pasted image 20251001163048.png]]
![[Pasted image 20251001163034.png]]
