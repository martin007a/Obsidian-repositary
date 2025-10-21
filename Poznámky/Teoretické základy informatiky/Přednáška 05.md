## Teorie Množin
### Počet prvků množiny
- kolik prrvků má prázdná množina (U zkoušky se bude smát)
Též označovaný pojmem mohutnost nebo kardinalita
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