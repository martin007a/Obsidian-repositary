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
