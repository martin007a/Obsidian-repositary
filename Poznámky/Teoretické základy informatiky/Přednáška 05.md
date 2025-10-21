## Teorie Množin
V matematice je všechno množina 
- i čísla jsou definována pomocí množin 
- podrobnosti v navazujícím studiu
###### Informatika stojí na matematice 
###### Znalosti teorie množin využijeme
- v databázových systémech
- v informačních systémech
- při navrhovaní algoritmů apod.
### Pojem množina
**Cantorova naivní teorie množin** 
- množina je dobře definovaný soubor objektů 
- paradoxy naivní teorie množin
**Axiomatická teorie množin**
- množina je primitivní pojem
- množiny vedoucí ke sporu není možné konstruovat
##### Určení množiny
	- výčtem prvků: 𝑀 = {1, 2, 3}
	- vlastností: 𝑀 = {𝑛 ∈ ℕ | 𝑛 < 4}
### Příslušnost do množiny**
Intuitivně se držíme označení množina pro souhrn objektů
****Definice:** 
- Skutečnost, že 𝑎 je prvkem množiny 𝐴, značíme 𝑎 ∈ 𝐴.
**Definice:**
- Skutečnost, že a není prvkem množiny A, značíme 𝑎 ∉  A.
### Počet prvků množiny
- kolik prrvků má prázdná množina (U zkoušky se bude smát)
Též označovaný pojmem **mohutnost** nebo **kardinalita**
![[Pasted image 20251021132241.png]]
## Rovnost množin
![[Pasted image 20251021132326.png]]
Jsou si množiny rovné 
### Podmnožina
Řekneme, že množina 𝐴 je podmnožinou množiny 𝐵 (značíme 𝐴 ⊆ 𝐵) právě tehdy, když každý prvek množiny 𝐴 je zároveň prvkem množiny B
- Platí tedy 𝐴 ⊆ 𝐵 ⇔ (∀𝑥)((𝑥 ∈ 𝐴) ⇒ (𝑥 ∈ 𝐵))
- Pojem podmnožina připouští i rovnost množin
	- každá podmnožina je podmnožinou sebe sama
	- 𝐴 = 𝐵 ⇒ 𝐴 ⊆ 𝐵, čili 𝐴 ⊆ A
- Prázdná množina je podmnožinou každé množiny
	- ∅ ⊆ 𝐴 pro libovolnou množinu 𝐴, tedy i ∅ ⊆ ∅
![[Pasted image 20251021132924.png]]
## Vlastní podmnožina
Množina A je vlastní podmnožinou množiny B (značíme 𝐴 ⊂ 𝐵 nebo také 𝐴 ⊊ B) právě tehdy když je její podmnožinou, ale A  ≠ 𝐵.
![[Pasted image 20251021133238.png]]
### Potenční množina
Množinu všech podmnožin množiny 𝐴 nazveme potenční množinou množiny 𝐴 a značíme 𝒫 (𝐴).
![[Pasted image 20251021133458.png]]
P(n) = 2<sup>n</sup> jiný zápis potoční množiny
**Žádná potenční množina nikdy není prázdná**
## Sjednocení množin
**Sjednocení množin** (značíme 𝐴 ∪ 𝐵) je množina prvků, které patří alespoň do jedné ze sjednocovaných množin.
- Formálně: 𝐴 ∪ 𝐵 = {𝑥 | (𝑥 ∈ 𝐴) ∨ (𝑥 ∈ 𝐵)}
##### Vlastnosti sjednocení 
* 𝐴 ⊆ (𝐴 ∪ 𝐵) pro libovolné množiny 𝐴, 𝐵 ??????????? 
* (𝐴 ∪ 𝐵) = (𝐵 ∪ 𝐴)
* – (𝐴 ∪ ∅) = A
### Průnik množin
**Průnik množin** (značíme 𝐴 ∩ 𝐵) je množina prvků, které patří do obou množin současně.
- • Formálně: 𝐴 ∩ 𝐵 = {𝑥 | (𝑥 ∈ 𝐴) ∧ (𝑥 ∈ 𝐵)}
###### Vlastnosti průniku 
- (𝐴 ∩ 𝐵) ⊆ 𝐴 pro libovolné množiny 𝐴, 𝐵 
- (𝐴 ∩ 𝐵) = (𝐵 ∩ 𝐴) 
- (𝐴 ∩ ∅) = ∅
Množiny se nazývají disjunktní, jestliže mají prázdný průnik (tj. nemají žádný společný prvek)
## Rozdíl množin
Rozdíl množin (značíme 𝐴 − 𝐵 nebo 𝐴 ∖ 𝐵) je množina prvků, které patří do množiny 𝐴 a nepatří do množiny 𝐵.
- **Formálně: 𝐴 − 𝐵 = {𝑥 | (𝑥 ∈ 𝐴) ∧ (𝑥 ∉ 𝐵)}**
##### Vlastnosti rozdílu 
- (𝐴 − 𝐵) ⊆ 𝐴 pro libovolné množiny 𝐴, 𝐵  
- (𝐴 − 𝐵) = (𝐵 − 𝐴) ⇒ (𝐴 = 𝐵) 
- (𝐴 − ∅) = A
- (∅ − A) = ∅
#### Vlastnosti množinových operací
### Sjednocení a průnik jsou komutativní a asociativní 
- 𝐴 ∪ 𝐵 = 𝐵 ∪ 𝐴 
- 𝐴 ∩ 𝐵 = 𝐵 ∩ 𝐴 
- 𝐴 ∪ (𝐵 ∪ 𝐶) = (𝐴 ∪ 𝐵) ∪ 𝐶
- 𝐴 ∩ (𝐵 ∩ 𝐶) = (𝐴 ∩ 𝐵) ∩ 𝐶
**Rozdíl** není ani komutativní, ani asociativní

Platí zákony idempotence
- 𝐴 ∪ 𝐴 = 𝐴 
- 𝐴 ∩ 𝐴 = AS
![[Pasted image 20251021135406.png]]
### Příklady k domácímu procvičení
![[Pasted image 20251021135434.png]]
Doděláš kdyžtak sám ☺
### Doplněk množiny v množině
Nechť 𝐴 a 𝑀 jsou množiny a platí 𝐴 ⊆ 𝑀. Doplňkem množiny 𝐴 v množině 𝑀 (značíme 𝐴 ′𝑀 ) nazveme množinu všech prvků množiny 𝑀, které nejsou prvky množiny 𝐴.
![[Pasted image 20251021135616.png]]
## Vlastnosti doplňku za předpokladu 𝐴 ⊆ 𝑀
**Zákony jednotky**  
- 𝐴 ∪ 𝑀 = 𝑀 
- 𝐴 ∩ 𝑀 = 𝐴 
- 𝐴 ∪ ∅ = 𝐴 
- 𝐴 ∩ ∅ = ∅ 
**Zákony negace** 
- 𝐴 ∪ 𝐴′𝑀 = 𝑀 
- 𝐴 ∩ 𝐴′𝑀 = ∅ 
- 𝑀′𝑀 = ∅ – ∅ ′𝑀 = 𝑀 
**De Morganovy zákony**  
- (𝐴 ∩ 𝐵)′<sub>M</sub> = 𝐴′<sub>M</sub> ∪ 𝐵′<sub>M</sub>
- (𝐴 ∪ 𝐵)′<sub>M</sub> = 𝐴′<sub>M</sub> ∩ 𝐵′<sub>M</sub>
` doplněk 
### Teorie čísel
###### Část matematiky zabývající se čísly 
- definice číselných množin 
- definice operací na číselných množinách 
- vlastnosti (zejména dělitelnost) 
- souvislost s algebrou
##### Číselné množiny 
- ℕ – přirozená čísla 
- ℤ – celá čísla 
- ℚ – racionální čísla 
- 𝕀 – iracionální čísla 
- ℝ – reálná čísla 
- ℂ – komplexní čísla
### Přirozená čísla (ℕ, z lat. naturalis)
![[Pasted image 20251021141912.png]]
### Přirozená čísla a nula
![[Pasted image 20251021142606.png]]
## Přirozená čísla jako množiny
![[Pasted image 20251021142723.png]]
### Celá čísla (ℤ, z něm. Zahlen)
![[Pasted image 20251021142814.png]]
### Racionální čísla (ℚ, z ital. quoziente)
![[Pasted image 20251021142856.png]]
### Reálná čísla (ℝ, z lat. realis)
![[Pasted image 20251021143127.png]]
### Komplexní čísla (ℂ, z lat. complexus)
![[Pasted image 20251021143206.png]]


