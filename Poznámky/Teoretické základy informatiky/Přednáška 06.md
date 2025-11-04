### 1 soubor prvků které mají nějakou společnou vlastnost
### 5 stejné prvky
## Uspořádaná dvojice
- Prvky množiny nejsou uspořádané
- Dvouprvková množina společně s uspořádáním prvků se nazývá **uspořádaná dvojice** 
	- značí se (𝑎, 𝑏) 
	- neplést s {𝑎, 𝑏}
- Formálně (a,b) = 
- Důsledek uspořádání
	- {𝑎, 𝑏} = {𝑏, 𝑎} 
	- (𝑎, 𝑏) ≠ (𝑏, 𝑎) pro 𝑎 ≠ b
### Kartézský součin
**Definice:**
- Jsou dány množiny 𝐴, 𝐵. Jejich kartézským součinem 𝐴 × 𝐵 rozumíme množinu 𝐴 × 𝐵 = {(𝑎, 𝑏) | 𝑎 ∈ 𝐴 ∧ 𝑏 ∈ 𝐵}.
- Kartézský součin je tedy množina všech uspořádaných dvojic takových, že první prvek patří do první množiny a druhý prvek patří do druhé množiny
- Kartézský součin **není komutativní** 
- plyne z nerovnosti (𝑎, 𝑏) ≠ (𝑏, 𝑎) 
- (𝐴 × 𝐵 = 𝐵 × 𝐴) ⟺ (𝐴 = 𝐵 ∨ 𝐴 = ∅ ∨ 𝐵 = ∅)
 A×∅ = ∅
#### Vlastnosti kartézského součinu
Platí-li |𝐴| = 𝑚, |𝐵| = 𝑛, pak |𝐴 × 𝐵| = 𝑚 ⋅ 𝑛 
- **Distributivní zákony** 
	- 𝐴 × (𝐵 ∩ 𝐶) = (𝐴 × 𝐵) ∩ (𝐴 × 𝐶) 
	- 𝐴 × (𝐵 ∪ 𝐶) = (𝐴 × 𝐵) ∪ (𝐴 × 𝐶) 
	- … a stejně tak i kartézské násobení zprava 
- Prázdná množina v kartézském součinu 
	- 𝐴 × ∅ = ∅ pro libovolnou množinu 𝐴 
	- ∅ × 𝐴 = ∅ pro libovolnou množinu A
	- ∅ × ∅ = ∅
### Kartézský součin více množin
- Kartézská mocnina 
	- 𝐴 <sup>1</sup> = 𝐴 
	- 𝐴 <sup>𝑛</sup> = 𝐴<sup>𝑛−1</sup> × A
- Kartézský součin více množin 
	- 𝐴1 × 𝐴2 × … × 𝐴𝑛 = = {(𝑎1 , 𝑎2 , … , 𝑎𝑛) | ∀𝑖 ∈ {1, 2, … , 𝑛} ∶ 𝑎𝑖 ∈ 𝐴𝑖}
![[Pasted image 20251104133144.png]]
### Binární relace
**Definice:**
(Binární) **relací** rozumíme libovolnou podmnožinu kartézského součinu dvou množin, tedy ℛ ⊆ 𝐴 × 𝐵.
- Pro prvky 𝑎 ∈ 𝐴 a 𝑏 ∈ 𝐵 takové, že (𝑎, 𝑏) ∈ ℛ, lze jejich příslušnost do binární relace zapisovat infixově 𝑎ℛ𝑏 
- Relace je **množina**, můžeme na ni tedy aplikovat množinové operace 
- **Speciální případy** 
	- **prázdná relace:** ∅ ⊆ 𝐴 × 𝐵 
	- **plná relace:** ℛ = 𝐴 × 𝐵 - Všechny uspořádané prvky- celý kartézský součin
### 𝑁-ární relace
• **Připomenutí:** arita = počet operandů
![[Pasted image 20251104133737.png]]
- Jde tedy o podmnožinu kartézského součinu 𝑛 množin
- **Speciální případ** 
	- unární relace: ℛ ⊆ A
## Určení relace
**Výčtem prvků**
- 𝐴 = {0, 1, 2}, 𝐵 = {𝑎, 𝑏} 
- ℛ = {(0, 𝑎), (0, 𝑏), (1, 𝑏), (2, 𝑎)}
**Požadovanou vlastností (vztahem prvků)**
- 𝐴 = 𝐵 = ℤ 
- ℛ = {(𝑎, 𝑏) ∈ 𝐴 × 𝐵 | 𝑎 ≤ 𝑏}
![[Pasted image 20251104134031.png]] 

### Skládání Relací
![[Pasted image 20251104134328.png]]
![[Pasted image 20251104134336.png]]
### Inverzní relace
![[Pasted image 20251104134548.png]]
![[Pasted image 20251104134557.png]]
**Prostě vynásobíme tu množinu obrácené**
### Relace na množině
![[Pasted image 20251104134742.png]]
relace na množině - násobím množinu samu se sebou
Relace  a identita - relace, která obsahuje 
### Reflexivní relace
![[Pasted image 20251104134911.png]]
Reflexivní relace je když je každý prvek podmnožinou sám se sebou.
- Každý má sejné jméno jako on sám
### Symetrická relace
![[Pasted image 20251104135128.png]]
Ke každé relaci existuje i relace opačná
jeli (a,b) tak musí být i (b,a)
- Anička je sourozenec Pepíčka a naopak
### Antisymetrická relace
![[Pasted image 20251104135305.png]]
Prostě někde najdem dvě stejné relace současně, jinak nesmí být
## Asymetrická relace
![[Pasted image 20251104135602.png]]
Zakazuje i to že jsou relace stejné
- průnik relace a její inverze musí být null
**Tranzitivní relace**
![[Pasted image 20251104135703.png]]
**a** je v relaci s **b** a s **c** tak a má také **s**
i když má množina Jeden prvek tak je taky tranzitivní
### Relace úplná
![[Pasted image 20251104135901.png]]
Obsahuje alespoň jednu dvojici pro dva prvky
Nemůže tam být dvojice která je neporovnatelná
### Relace ekvivalence
![[Pasted image 20251104140030.png]]
pokud splní 3 vlastnosti, je ekvivalentní
## Relace uspořádání
![[Pasted image 20251104140120.png]]
zase pokud splní ty 3, tak je uspořádání, pokud úplná tak je Úplná uspořádání.
![[Pasted image 20251104140401.png]]
je symetrická, tranzititvní refexivní, -> ekvivalence,
##### Být v relaci dává stejný zbytek po dělení 7 jako 0
Tabuka 
reflexivita = 1 na diaginále
Symetrie = Dvakrát c

##### Vlastnosti se na vzájem nevilučují a stejně nemusí mít žásnou 
### Mocnina relace
![[Pasted image 20251104141149.png]]
Vezmu relaci a aplikuji ji ještě jednou. ?
relace Identita na diagonále jsou 1 jinde 0
## Mocnina relace
![[Pasted image 20251104141351.png]]
### Uzávěr relace
![[Pasted image 20251104141718.png]]
## Uzávěr relace
![[Pasted image 20251104141835.png]]
