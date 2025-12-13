2- množina uspořádaných n-tic
4- 
5- N násobný kartézkský součin množiny
6- libovoná podnožina na kartézkého součinu na 2 množin
7- n množin
8- libobolá pomnoina množiny
10- Sládání relaci na relaci
11- množiny vynásobím v opačném pořadí
13- nemá žádné prvky 
16- reflexivní relace musí obsahovat identitu
17- pro každá (a,b) existuje (b,a)
18- když (a,b) tak ne (b,a), diagonála všude **0**
19-
20- 
Zamyšlení
1 Kolik různých relací existuje na 𝑛-prvkové množině? 
	2<sup>n</sup>
2 Kolik různých relací existuje na prázdné množině? 
	1
3 Kolik různých reflexivních relací existuje na 𝑛-prvkové množině? 
	2<sup>n<sup>2</sup>-n</sup>
4 Kolik různých symetrických relací existuje na 𝑛-prvkové množině? 
	2<sup>n*(n+1)/2</sup>
5 Jaké vlastnosti má prázdná relace na neprázdné množině? 
6 Jaké vlastnosti má plná relace na neprázdné množině? 7 Jaké vlastnosti má prázdná relace na prázdné množině? 8 Jsou všechny relace na jednoprvkové množině tranzitivní? 9 Najděte úplnou relaci na množině {𝑎, 𝑏}, která není ekvivalencí 10 Najděte všechna uspořádání na množině {𝑎, �
1 2<sup>n</sup>
3 2<sup>n<sup>2</sup>-n</sup>
4 2<sup>n*(n+1)/2</sup>
5
7  je refelxivní a upná
## Využití skládání relací v praxi
## Zobrazení
**Definice:**
Jsou dány množiny 𝐴, 𝐵 a relace ℛ ⊆ 𝐴 × 𝐵. Relaci ℛ nazveme zobrazení právě tehdy, když (∀𝑎 ∈ 𝐴)(∃!𝑏 ∈ 𝐵)(𝑎ℛ𝑏).
- Zobrazením tedy nazveme takovou relaci, kde ke každému prvku z množiny 𝐴 existuje **jediný** prvek z množiny 𝐵, který je s ním v relaci 
- Zobrazení mezi číselnými množinami nazýváme **funkce**
## Spočetnost množin Závěr Vzor a obraz
Vzhledem k tomu, že ke každému prvku 𝑎 ∈ 𝐴 je prvek 𝑏 ∈ 𝐵 určen jednoznačně, lze místo 𝑎ℛ𝑏 nebo (𝑎, 𝑏) ∈ ℛ psát ℛ(𝑎) = b
**Definice:**
Je dáno zobrazení 𝑓 takové, že 𝑓 (𝑎) = 𝑏. Potom 
- prvek 𝑏 nazýváme **obraz** prvku 𝑎,
- prvek 𝑎 nazýváme vzor prvku 𝑏. 
Definice zobrazení vyžaduje, aby každý prvek množiny 𝐴 měl jediný obraz
 - naopak to však neplatí 
 - jeden prvek množiny 𝐵 může mít více vzorů
### Definiční obor a obor hodnot
**Definice**
Je dáno zobrazení 𝑓 ⊆ 𝐴 × 𝐵. 

Množinu 𝐴 nazýváme **definiční obor** zobrazení 𝑓 a značíme jej D(𝑓 ) nebo Dom(𝑓 ). 

Množinu H(𝑓 ) = {𝑏 ∈ 𝐵 | ∃𝑎 ∈ 𝐴 ∶ 𝑓 (𝑎) = 𝑏} nazveme **obor hodnot** zobrazení f.
Někdy se používá označení Im(𝑓).
- Obor hodnot zobrazení je tedy množina takových prvků, které mají svůj vzor 
- Skutečnost, že 𝑓 ⊆ 𝐴 × 𝐵 je zobrazení, častěji zapisujeme jako 𝑓 ∶ 𝐴 → 𝐵
### Poznámky k definici zobrazení
- Někdy se místo „existuje právě jeden“ říká „existuje maximálně jeden“
- V množině 𝐴 tak mohou existovat prvky, které nemají svůj obraz v množině 𝐵 
- Definiční obor zobrazení je pak podmnožinou množiny 𝐴 
- Rozlišujeme zobrazení „množiny 𝐴“ a zobrazení „z množiny 𝐴“ 
- My se budeme držet uvedené definice, v níž je definiční obor celá množina A
### Surjekce
**Definice**
Je dáno zobrazení 𝑓 ∶ 𝐴 → 𝐵. Jestliže Im(𝑓 ) = 𝐵, zobrazení 𝑓 nazýváme **zobrazením na množinu** nebo též **surjekce**.
- U surjektivního zobrazení je tedy oborem hodnot celá množina 𝐵, každý prvek má tedy svůj vzor v množině 𝐴 
- Formální zápis skutečnosti, že 𝑓 ∶ 𝐴 →𝐵 je surjektivní zobrazení: (∀𝑏 ∈ 𝐵)(∃𝑎 ∈ 𝐴)(𝑓 (𝑎) = 𝑏)
### Injekce
**Definice**
Je dáno zobrazení 𝑓 ∶ 𝐴 → 𝐵. Toto zobrazení nazveme **injekce** nebo **prosté zobrazení**, jestliže (∀𝑎1 , 𝑎2 ∈ 𝐴)(𝑓 (𝑎1 ) = 𝑓 (𝑎2 ) ⇒ 𝑎1 = 𝑎2 ).
- Tedy pokud každé dva různé prvky mají různé obrazy 
- Připomeňme, že žádný prvek nemůže mít dva různé obrazy (nebylo by to zobrazení), definice zobrazení však nevylučovala případ, kdy mají dva prvky stejný obraz
### Bijekce
**Definice**
Je dáno zobrazení 𝑓 ∶ 𝐴 → 𝐵. Zobrazení 𝑓 nazveme bijekce právě tehdy, když je zároveň injekce a surjekce.
- Tedy když je zároveň na množinu a prosté 
- Bijekce se též nazývá **párování 1 : 1**
**Definice**
Nechť 𝐴, 𝐵 jsou množiny a 𝑓 ∶ 𝐴 → 𝐵 je bijekce. Pak |𝐴| = |𝐵|.
- Existence bijekce **dokazuje stejnou mohutnost** množin
## Otázky k zamyšlení
Jsou dány množiny 𝐴, 𝐵 takové, že |𝐴| = 𝑚, |𝐵| = 𝑛.
1. Kolik existuje různých zobrazení 𝐴 → 𝐵? (n<sup>m</sup>) 
2. Kolik existuje různých zobrazení 𝐵 → 𝐴? 
3. Kolik z nich je injektivních? (|A|>|B|) - žádné není
4. Kolik z nich je bijektivních?
### Skládání zobrazení
**Definice**
Jsou dány množiny 𝐴, 𝐵, 𝐶 a zobrazení 𝑓 ∶ 𝐴 → 𝐵 a 𝑔 ∶ 𝐵 → 𝐶. **Složeným zobrazením** 𝑔 ∘ 𝑓 nazveme složenou relaci 𝑔 ∘ f
- Je zřejmé, že relace vzniklá složením dvou zobrazení je opět zobrazení 
- Platí 𝑔 ∘ 𝑓 ∶ 𝐴 → 𝐶 a také platí, že 𝑔 ∘ 𝑓 (𝑥) = 𝑔(𝑓 (𝑥)) • Skládání zobrazení není komutativní 
- Skládání zobrazení není komutativní
- Skládání zobrazení je asociativní
## Inverzní zobrazení
**Definice**
Je prosté zobrazení 𝑓 ∶ 𝐴 → 𝐵. Inverzním zobrazením k zobrazení 𝑓 nazveme zobrazení 𝑓 −1 ∶ Im(𝑓 ) → 𝐴 takové, že pro ∀𝑎 ∈ 𝐴 a ∀𝑏 ∈ 𝐵 platí 𝑓 −1(𝑏) = 𝑎 ⟺ 𝑓 (𝑎) = 𝑏.
- Požadavek prostosti zobrazení zaručuje, že inverzní relace bude zobrazením 
- Zřejmě 𝑓 −1(𝑓 (𝑥)) = 𝑥 
- Tedy 𝑓 −1 ∘ 𝑓 = id
![[Pasted image 20251111140620.png]]
### Inverze složeného zobrazení
![[Pasted image 20251111140827.png]]
## Operace
**Definice:**
Nechť 𝐴 je množina a 𝑛 je přirozené číslo. Zobrazení 𝐴 𝑛 → 𝐴 nazýváme 𝑛-ární **operací** na množině 𝐴. Číslo 𝑛 nazýváme **arita** (četnost) operace.
- Pro 𝑛 = 0 hovoříme o nulární operaci 
	- výběr konstanty 
- Pro 𝑛 = 1 hovoříme o unární operaci 
	- log𝑧 𝑥, 𝑥 2 , −𝑥, √𝑥 
- Pro 𝑛 = 2 hovoříme o binární operaci 
	- 𝑥 + 𝑦, 𝑥 ⋅ 𝑦
### Vztah relací, zobrazení a operací
- Operace je zobrazení, zobrazení je relace, tudíž operace je také relace
**Příklad**y
- Binární operace sčítání je tedy ve skutečnosti ternární relace obsahující právě prvky typu (𝑎, 𝑏, 𝑎 + 𝑏) 
- Unární operace minus je ve skutečnosti binární relace obsahující právě prvky typu (𝑥, −𝑥)
### Vlastnosti operací
- **Uzavřenost** množiny vzhledem k operaci 
	-  výsledek operace náleží do dané množiny 
	- plyne přímo z definice operace
![[Pasted image 20251111141228.png]]
## Neutrální Prvek
![[Pasted image 20251111141506.png]]
## Inverzní Prvek
![[Pasted image 20251111141544.png]]
### Kardinalita
![[Pasted image 20251111142613.png]]
## Spočetné množiny
![[Pasted image 20251111142644.png]]
### Spočetnost racionálních čísel
![[Pasted image 20251111143322.png]]
### Nespočetnost reálných čísel 
![[Pasted image 20251111143446.png]]
### Cantorova metoda diagonalizace
![[Pasted image 20251111143503.png]]
### Cantorova metoda diagonalizace
![[Pasted image 20251111143519.png]]
### Cantorova metoda diagonalizace
![[Pasted image 20251111143541.png]]
