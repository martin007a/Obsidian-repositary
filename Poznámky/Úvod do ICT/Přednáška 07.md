### Formáty souborů
![[Pasted image 20251105152029.png]]
ta 00 je oddělovač
0D 0A -> dvojice, jterá představuje Enter
### Porovnání způsobů uložení
![[Pasted image 20251105152438.png]]
## Formátová specifikace
**Formátová specifikace** 
- přesný popis formátu uložení dat 
- definuje význam jednotlivých bitů (bajtů) dat1
![[Pasted image 20251105152540.png]]
07 - Délka
## Textový a binární formát
- **Textový formát** – data jsou připravena pro zobrazení a přímé čtení člověkem 
- **Netextový (binární) formát** – data jsou připravena pro aritmetické a logické operace v paměti počítače
![[Pasted image 20251105152757.png]]
**latek**
### Definice textového a binárního formátu
**Textový formát** je dělaný tak aby byl čitelný člověkem 
#### Intuitivní definice
- **textový formát:** všechny prvky formátu jsou složeny výhradně ze zobrazitelných znaků 
- **binární formát:** alespoň některé prvky formátu jsou řešeny jiným způsobem (řídicími znaky)
#### Problémy 
-  kolik řádků může mít soubor, je-li v textovém formátu? 
- jak poznáme konec souboru?
### Upravená definice
- **textový formát:** všechny prvky formátu jsou složeny ze zobrazitelných znaků, mezi nimiž jsou použity jako oddělovače konce řádků a na konci dat nejvýše jeden znak konce souboru
	- Konce řádků 
	- A konec Dokumentu
### Konec řádku a konec souboru
- V různých operačních systémech jsou řídicí znaky různé 
- Vedlejší efekt: podle tvaru konce řádku lze zjistit operační systém, ve kterém byl soubor vytvořen 
- Dnešní kvalitní textové editory dokážou pracovat s libovolným koncem řádku a také jej změnit
![[Pasted image 20251105153602.png]]
### Problémy s koncem řádku
### Textový a binární formát – srovnání
![[Pasted image 20251105153927.png]]
### Souborový formát
Přesný popis **způsobu uložení dat v souborech** 
* pojem odvozený z pojmu „datový formát“ 
Místo podrobného popisu používáme jména formátů 
- rozšíření jména souboru o příponu 
**Dokument** – soubor obsahující 
- vlastní text 
- formátovací značky 
Dělení souborů podle tvaru značek 
- **textové** – HTML, XML, RTF, PostScript, TEX, CSV 
- **binární** – DOC, DOCX, INDD, PDF, Text602 
Programy určitého zaměření mohou zpracovávat datové soubory v obou formátech 
- rozdílné vlastnosti a možnosti použití
### Otevřený a uzavřený formát
**Otevřený formát** 
- specifikace formátu je volně dostupná -
- efektivní využití a zpracování uložených dat 
- ideální prostředek pro výměnu informací 
- příklady: JPG, PNG, PDF, všechny textové 
**Uzavřený formát** 
- specifikace formátu je utajována 
- umožňuje získat monopol pro jeho zpracování 
- silně omezuje možnosti využití uložených dat 
- příklady: CDR, INDD, dříve MS Office (DOC, XLS, PPT)
### Prostý a rozšířený text
U textových formátů rozlišujeme, zda obsahují či neobsahují národní znaky
**Prostý text** (plain text, ASCII text)
- obsahuje pouze znaky z dolní poloviny ASCII tabulky 
- žádné národní znaky → žádné problémy se zobrazením 
- bohužel méně časté řešení
**Rozšířený text** (extended text)
- obsahuje znaky z horní poloviny ASCII tabulky 
- nutno upřesnit kódování národních znaků 
- velmi časté řešení, proto časté problémy
**Poznámka k terminologii:** Mnoho zdrojů používá
pojem „plain text“ ještě v jiné souvislosti 
- neformátovaný text = plain text 
- formátovaný text = dokument
### Přehled základních souborových formátů
**Textové formáty**
- webové aplikace: HTML, XML, MHT, CSS 
- zdrojové kódy: JS, PAS, JAVA, PL, PHP, ASP 
- dokumenty: RTF, PS, CSV, TEX, TXT – grafika: SVG
**Binární formáty**
- historie: SAM, INDD, T602 
- dokumenty: DOC(X), XLS(X), PPT(X), ODF, PDF 
- grafika: BMP, JPG, PNG, GIF, TIFF, CDR, EPS 
- multimédia: MP3, AVI, MPEG – archivy: ZIP, RAR, 7Z