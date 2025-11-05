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
### Přenositelnost formátu
- Lze pracovně definovat jako množství programů schopných zpracovat tento formát
- Důležitým faktorem je podpora zpracování formátu v různých operačních systémech 
	- některé formáty úzce svázány s konkrétním OS
- Přenositelnost je také úzce svázána s otevřeností formátu, ale závisí také na majiteli formátu 
	- DOC × PDF a možnost generování 
	- podpora DOCX ve starších verzích MS Office
![[Pasted image 20251105155753.png]]
### Pojmenování souborů a jejich formát
- Pro usnadnění orientace v množství souborových formátů se používá rozšíření 
	- též přípona (extension) 
	- od jména souboru se odděluje tečkou
- Obvykle používáme přípony odpovídající konkrétním souborovým formátům 
	- .jpg nebo .jpeg pro rastrovou grafiku 
	- .htm nebo .html pro webovou stránku 
	- .mp3 pro komprimovaná zvuková data
- **Přípona sama o sobě však neurčuje formát souboru**
	- ve skutečnosti je tomu právě naopak! 
	- pravidla pro přípony nejsou přesně dána 
	- soubor ani příponu mít nemusí (Windows × Unix)
### Asociace formátů a aplikací
Usnadňuje zpracování dat zejména v OS Windows 
- **která aplikace umí se souborem pracovat?**
**Princip** – tabulka s řádky „formát → aplikace“ 
- Nastavení → Aplikace → Výchozí aplikace
**Spouštění aplikace** v okamžiku aktivace souboru 
- stažení přes webový prohlížeč 
- dvojklik v souborovém manažeru 
- výběr v dokumentech apod.
Orientace jen podle přípony proto může vést často ke zmatkům, které zpracování dat naopak komplikují
**Ideální stav: 1 formát → 1 aplikace** 
- platí jen pro speciální případy 
- formát CDR → aplikace Corel Draw!
**Problémové případy**
**Více formátů → 1 aplikace**
- časté, ale neproblematické
**1 formát → více aplikací**
- problém nejednoznačnosti, nepříjemné řešení 
- aktivuje se buď posledně instalovaná aplikace, nebo podle výběru z nabídky
**1 formát → žádná aplikace**
- chybové hlášení s nabídkou dostupných aplikací, z nichž si uživatel může vybrat (prakticky k ničemu) 
- Windows XP: rozšíření nabídky programů z Internetu
**Žádný formát → 1 aplikace**
- buď aplikace žádné formáty nepotřebuje, nebo se jedná o aplikaci DOS, nebo o chybnou instalaci
### Rozpoznávání formátu
Co dělat, když soubor abc.xyz nelze ničím otevřít? 
- soubor může být nenávratně poškozen 
- možná ale jen neexistuje asociovaná aplikace
**První krok**
- roztřídění na textové a binární formáty 
- využití běžných programů (poznámkový blok)
**Druhý krok**
- **rozšířené textové formáty** – rozpoznání původu souboru (OS, v němž pravděpodobně vznikl) a kódování národních znaků 
- **binární formáty** – použití rozpoznávacích programů
Softwarová podpora
 - Unix – file, enca, od 
 - Windows – není nástroj (zkusmo?)
 Potřebuji hexadecimální editor PSpad