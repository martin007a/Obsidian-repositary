Základní myšlenka vztahů Stejně jako mezi objekty reálného světa, také mezi objekty v programech existují určité vztahy. Vztahy jsou různých typů. Z programátorského hlediska se jedná o interakci mezi objekty (obsažení, přístup, ...).
### Co musí model vztahu obsahovat
- Popis
- Násobnost 
- Typ 
- Orientaci
#### Směr (orientace) vazby
### Násobnost
Násobnosti: M:N, M:1, 1:N, 1:1
### Pojmenování vazby
Aby vztahy mezi třídami byly jasné, používáme pro vazby pojmenování a případně i komentáře.
![[Pasted image 20251021152237.png]]
### Reflexivní vazba
Objekt obsahuje odkaz na objekt stejné třídy jako je on sám. Tento vztah je označován jako reflexivní vazba
### Vazba M:N a asociativní třída
Implementačně jsou problémem vazby M:N. Žádný běžný programovací jazyk neumožňuje implementaci vazby N:M přímo. Je nutné ji „obejít“.
![[Pasted image 20251021152741.png]]
## Shrnutí modelování vztahů
- Vazby vyjadřují vztahy mezi objekty. 
- **U vazeb uvádíme násobnosti, popis, orientaci.** 
- Na první pohled speciálním případem je reflexivní asociace. Nicméně implementačně je stejná jako ostatní vazby.
- **Problémem je vazba M:N** (viz asociační třída). Tu musíme rozdělit.
### Asociace
V určitém okamžiku jeden např. zavolá metodu druhého nebo přistoupí k jeho vlastnosti.
1. Nejvolnější typ vazby, např. zasílání zprávy (volání metody) jiného objektu nebo přístup k jeho atributům.
2. Objekty existují nezávisle na sobě.
### Agregace
Umožňuje, abychom spolu dočasně provázali dva různé objekty (obvykle bude jeden objekt obsahovat odkaz na druhý).
- Silnější typ vazby, ve volném překladu vlastnění
- výstižnější je možná opis dočasná znalost
### Kompozice
Kompozice umožňuje, aby se objekt skládal z více různých částí (objektů).
- Dalším typem vztahu je kompozice – složení.
- Objekty jsou spolu svázány po celou dobu své existence.
- Význam: Zpřehlednění stavby objektů pomocí jejich rozdělení do logických částí.
