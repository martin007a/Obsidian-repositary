## Teorie Množin
V matematice je všechno množina 
- i čísla jsou definována pomocí množin 
- podrobnosti v navazujícím studiu
###### Informatika stojí na matematice 
###### Znalosti teorie množin využijeme
- v databázových systémech
- v informačních systémech
- při navrhovaní algoritmů apod.
## Pojem množina
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
kolik prvků má prázdná množina? (U zkoušky se bude smát ) "Haluza" 
Též označovaný pojmem **mohutnost** nebo **kardinalita**
**Značíme |M|**
- např. pro M = {1,2} je |M| = 2
##### Konečné množiny
- mají konečný počet prvků
- tedy |𝑀| ∈ ℕ
##### Nekonečné množiny
- mají nekonečný počet prvků
- tedy |𝑀| ∉ ℕ
##### Prázdná množina
- **nemá žádný prvek**
- značení ∅ nebo {}, nikoli {∅}
- platí tedy, že |∅| = 0
## Rovnost množin
**Definice: **
 - Dvě množiny jsou si rovny, jestliže mají stejné prvky.
##### Formálně: 
 $$𝐴 = 𝐵 ⇔ ((∀𝑥)((𝑥 ∈ 𝐴) ⇒ (𝑥 ∈ 𝐵))∧(∀𝑥)((𝑥 ∈ 𝐵) ⇒ (𝑥 ∈ 𝐴)))$$
##### **Platí zřejmá implikace: **
$$(𝐴 = 𝐵) ⇒ (|𝐴| = |𝐵|)$$
Jsou si množiny rovné 
## Podmnožina
Symbol **⊆** znamená **„je podmnožinou“** nebo také **„je (možná rovná) podmnožina“**.
Řekneme, že množina 𝐴 je podmnožinou množiny 𝐵 (značíme 𝐴 ⊆ 𝐵) právě tehdy, když každý prvek množiny 𝐴 je zároveň prvkem množiny B
- Platí tedy 𝐴 ⊆ 𝐵 ⇔ (∀𝑥)((𝑥 ∈ 𝐴) ⇒ (𝑥 ∈ 𝐵))
- Pojem podmnožina připouští i rovnost množin
	- každá podmnožina je podmnožinou sebe sama
	- 𝐴 = 𝐵 ⇒ 𝐴 ⊆ 𝐵, čili 𝐴 ⊆ A
- Prázdná množina je podmnožinou každé množiny
	- ∅ ⊆ 𝐴 pro libovolnou množinu 𝐴, tedy i ∅ ⊆ ∅
![[Pasted image 20251021132924.png]]
Kolik prvků má potenční množina 𝑛-prvkové množiny?
Počet prvků potenční množiny je 2<sup>n</sup> 
## Vlastní podmnožina
Symbol **⊂** znamená **„je vlastní podmnožinou“**.
Množina A je vlastní podmnožinou množiny B (značíme 𝐴 ⊂ 𝐵 nebo také 𝐴 ⊊ B) právě tehdy když je její podmnožinou, ale A  ≠ 𝐵.
- V množině B tedy existují prvky, které nejsou prvky množiny A
- Platí (A )
### Potenční množina
Množinu všech podmnožin množiny 𝐴 nazveme **potenční množinou** množiny 𝐴 a značíme 𝒫 (𝐴).
![[Pasted image 20251021133458.png]]
![[Pasted image 20251023142803.png]]
P(n) = 2<sup>n</sup> jiný zápis potoční množiny
**Žádná potenční množina nikdy není prázdná**
## Sjednocení množin
**Sjednocení množin** (značíme 𝐴 ∪ 𝐵) je množina prvků, které patří alespoň do jedné ze sjednocovaných množin.
- Formálně: $$𝐴 ∪ 𝐵 = {𝑥 | (𝑥 ∈ 𝐴) ∨ (𝑥 ∈ 𝐵)}$$
![[Pasted image 20251023143017.png]]
##### Vlastnosti sjednocení 
* 𝐴 ⊆ (𝐴 ∪ 𝐵) pro libovolné množiny 𝐴, 𝐵 ??????????? 
* (𝐴 ∪ 𝐵) = (𝐵 ∪ 𝐴)
* – (𝐴 ∪ ∅) = A
### Průnik množin
**Průnik množin** (značíme 𝐴 ∩ 𝐵) je množina prvků, které patří do obou množin současně.
- • Formálně: $$𝐴 ∩ 𝐵 = {𝑥 | (𝑥 ∈ 𝐴) ∧ (𝑥 ∈ 𝐵)}$$
###### Vlastnosti průniku 
- (𝐴 ∩ 𝐵) ⊆ 𝐴 pro libovolné množiny 𝐴, 𝐵 
- (𝐴 ∩ 𝐵) = (𝐵 ∩ 𝐴) 
- (𝐴 ∩ ∅) = ∅
Množiny se nazývají disjunktní, jestliže mají prázdný průnik (tj. nemají žádný společný prvek)
## Rozdíl množin
Rozdíl množin (značíme 𝐴 − 𝐵 nebo 𝐴 ∖ 𝐵) je množina prvků, které patří do množiny 𝐴 a nepatří do množiny 𝐵.
- **Formálně: 𝐴 − 𝐵 = {𝑥 | (𝑥 ∈ 𝐴) ∧ (𝑥 ∉ 𝐵)}**
![[Pasted image 20251023171321.png]]
##### Vlastnosti rozdílu 
- (𝐴 − 𝐵) ⊆ 𝐴 pro libovolné množiny 𝐴, 𝐵  
- (𝐴 − 𝐵) = (𝐵 − 𝐴) ⇒ (𝐴 = 𝐵) 
- (𝐴 − ∅) = A
- (∅ − A) = ∅
## Vlastnosti množinových operací
##### Sjednocení a průnik jsou komutativní a asociativní 
- 𝐴 ∪ 𝐵 = 𝐵 ∪ 𝐴 
- 𝐴 ∩ 𝐵 = 𝐵 ∩ 𝐴 
- 𝐴 ∪ (𝐵 ∪ 𝐶) = (𝐴 ∪ 𝐵) ∪ 𝐶
- 𝐴 ∩ (𝐵 ∩ 𝐶) = (𝐴 ∩ 𝐵) ∩ 𝐶
-- **Rozdíl** není ani komutativní, ani asociativní
Platí **zákony idempotence**
- 𝐴 ∪ 𝐴 = 𝐴 
- 𝐴 ∩ 𝐴 = A
Platí **distribuční zákony**
- 𝐴 ∪ (𝐵 ∩ 𝐶) = (𝐴 ∪ 𝐵) ∩ (𝐴 ∪ 𝐶) 
- 𝐴 ∩ (𝐵 ∪ 𝐶) = (𝐴 ∩ 𝐵) ∪ (𝐴 ∩ 𝐶)
### Příklady k domácímu procvičení
![[Pasted image 20251021135434.png]]
Doděláš kdyžtak sám ☺
### Doplněk množiny v množině
Nechť 𝐴 a 𝑀 jsou množiny a platí 𝐴 ⊆ 𝑀. Doplňkem množiny 𝐴 v množině 𝑀 (značíme 𝐴 ′𝑀 ) nazveme množinu všech prvků množiny 𝑀, které nejsou prvky množiny 𝐴.
- Platí 𝐴 ′𝑀 = 𝑀 − A
- O Doplňku hovoříme tehdy, je-li množina A podmnožinou nějakého univerza M
	-  jinak hovoříme o rozdílu
## Vlastnosti doplňku za předpokladu 𝐴 ⊆ 𝑀-
**Zákony jednotky**  
- 𝐴 ∪ 𝑀 = 𝑀 
- 𝐴 ∩ 𝑀 = 𝐴 
- 𝐴 ∪ ∅ = 𝐴 
- 𝐴 ∩ ∅ = ∅ 
**Zákony negace** 
- 𝐴 ∪ 𝐴′<sub>𝑀</sub> = 𝑀 
- 𝐴 ∩ 𝐴′<sub>𝑀</sub> = ∅ 
- 𝑀′<sub>𝑀</sub> = ∅
- ∅ ′<sub>𝑀</sub> = 𝑀 
**De Morganovy zákony**  
- (𝐴 ∩ 𝐵)′<sub>M</sub> = 𝐴′<sub>M</sub> ∪ 𝐵′<sub>M</sub>
- (𝐴 ∪ 𝐵)′<sub>M</sub> = 𝐴′<sub>M</sub> ∩ 𝐵′<sub>M</sub>
` doplněk 
![[Pasted image 20251023172847.png]]

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
- Množina spolu se zobrazením **následovníka** S(x)
	- z definice ordinální datový typ
![[Pasted image 20251021141912.png]]

### Přirozená čísla a nula
- Axiomatická definice vyžaduje, aby 0 ∈ ℕ
- **Všeobecně** platí, že 0 ∉ ℕ
	-  zejména z historických důvodů
- Nadále nulu **nebudeme** považovat za přirozené číslo
	-  rozlišujeme tedy množiny ℕ a ℕ0
- Pouze pro potřeby **axiomatické výstavby** nulu do množiny ℕ zahrneme
## Přirozená čísla jako množiny
Každé číslo 𝑛 ∈ ℕ<sub>0</sub> intuitivně vyjadřuje **mohutnost množiny** o právě n prvcích
Čísla 𝑛 ∈ ℕ0 jsou definována iterativně jako **množiny** 
- každé číslo je množinou čísel menších než ono samo
![[Pasted image 20251023174357.png]]
## Celá čísla (ℤ, z něm. Zahlen)
**Symbol ≈** - znamená **„přibližně rovno“** nebo **„zhruba rovno“**.
K množině ℕ „připojíme" všechny **rozdíly přirozených čísel**, které v ní dosud nejsou
Na množině ℕ × ℕ zavedeme ekvivalenci ≈
$$(𝑎, 𝑏) ≈ (𝑐, 𝑑) ⟺ 𝑎 + 𝑑 = 𝑏 + 𝑐$$

Množinu celých čísel definujeme jako **rozklad** příslušný této ekvivalenci: 
ℤ = ℕ × ℕ/≈
`1 = [(1, 0)] = [(2, 1)] = … = [(𝑘 + 1, 𝑘)]
`-1 = [(1, 0)] = [(2, 1)] = … = [(𝑘 + 1, 𝑘)]
Operace jsou definovány takto:
`[(𝑎, 𝑏)] + [(𝑐, 𝑑)] = [(𝑎 + 𝑐, 𝑏 + 𝑑)]
`[(𝑎, 𝑏)] ⋅ [(𝑐, 𝑑)] = [(𝑎𝑐 + 𝑏𝑑, 𝑎𝑑 + 𝑏𝑐)]
Teprve nyní lze zavést **operaci rozdílu!**
## Racionální čísla (ℚ, z ital. quoziente)
Racionální čísla lze vyjádřit jako podíl dvou celých čísel
- na přirozených ani celých číslech podíl nelze definovat
Na množině ℤ × (ℤ − {0}) zavedeme ekvivalenci ≈ 
$$(𝑎, 𝑏) ≈ (𝑐, 𝑑) ⟺ 𝑎 ⋅ 𝑑 = b ⋅ c$$
Množinu racionálních čísel definujeme jako **rozklad** příslušný této ekvivalenci:
$$ℚ = ℤ × (ℤ − {0})/≈$$
operace jsou definovány takto:
$$a/b + c/d = (𝑎 ⋅ 𝑑 + 𝑐 ⋅ 𝑏)/(𝑏 ⋅ 𝑑)$$
$$𝑎/𝑏 ⋅ 𝑐/𝑑 = (𝑎 ⋅ 𝑐)/(𝑏 ⋅ 𝑑)$$
## Reálná čísla (ℝ, z lat. realis)
Na množině ℚ definujeme **řez**, značíme (A/B), jako dvojici množin A,B ⊆ ℚ, 𝐴 ∪ 𝐵 = ℚ, které jsou neprázdné, disjunktivní a platí (∀𝑎 ∈ 𝐴)(∀𝑏 ∈ 𝐵)(𝑎 < 𝑏)
- tzv. **Dedekindův řez** ---------- RICHARD DEDEKIND (* 1831, † 1916)
Nastávají **tři možnosti:**
- 𝐴 obsahuje největší číslo, 𝐵 neobsahuje nejmenší číslo např. 
  ({𝑥 ∈ ℚ | 𝑥 ≤ 5}/{𝑥 ∈ ℚ | 𝑥 > 5})
- 𝐴 neobsahuje největší číslo, 𝐵 obsahuje nejmenší číslo např. 
  ({𝑥 ∈ ℚ | 𝑥 < 5}/{𝑥 ∈ ℚ | 𝑥 ≥ 5})
- 𝐴 neobsahuje největší číslo, 𝐵 neobsahuje nejmenší číslo např. 
  ({𝑥 ∈ ℚ | 𝑥<sup>2</sup> ≤ 2}/{𝑥 ∈ ℚ | 𝑥<sup>2</sup> > 2})
Množinu reálných čísel definuje jako **množinu všech řezů** na a ℚ: 
	ℝ = {(𝐴/𝐵)}
## Komplexní čísla (ℂ, z lat. complexus)
**Motivace:** řešení problémů s výpočtem odmocnin ze záporných čísel
Množina komplexních čísel definujeme jako množinu 
**uspořádaných dvojic reálných čísel:**
$$a ℚ: ℝ = {(𝐴/𝐵)}$$
- místo (a,b) píšeme a + bi
Operace jsou definovány takto:
$$(𝑎 + 𝑏i) + (𝑐 + 𝑑i) = (𝑎 + 𝑐) + (𝑏 + 𝑑)i$$
$$(𝑎 + 𝑏i) ⋅ (𝑐 + 𝑑i) = (𝑎𝑐 − 𝑏𝑑) + (𝑎𝑑 + 𝑏𝑐)i$$
**Imaginární jednotka** i
$$(0 + 1i) ⋅ (0 + 1i) = −1 + 0i$$

# Kontrolní otázky
## 1. Co je to množina? 
**Axiomatická teorie množin:**
    ◦ Množina je v tomto přístupu považována za **primitivní pojem**.
    ◦ Cílem axiomatické teorie je znemožnit konstrukci množin vedoucích ke sporu
 V matematice je **všechno množina**. Dokonce i čísla jsou definována pomocí množin
## 2. Jak lze určit množinu? 
- výčtem prvků: 𝑀 = {1, 2, 3} 
- vlastností: 𝑀 = {𝑛 ∈ ℕ | 𝑛 < 4}
## 3. Co je to mohutnost a jak se značí? 
mohutnost - počet prvků množiny
Značíme |𝑀|
## 4. Kolik prvků má prázdná množina? 
**nemá žádný prvek**
značení ∅ nebo {}, nikoliv {∅}
## 5. Kdy jsou si dvě množiny rovny?
Dvě množiny jsou si rovny, jestliže mají stejné prvky.
(𝐴 = 𝐵) ⇒ (|𝐴| = |𝐵|)
## 6. Co je to podmnožina? 
Řekneme, že množina 𝐴 je podmnožinou množiny 𝐵 (značíme 𝐴 ⊆ 𝐵) právě tehdy, když každý prvek množiny 𝐴 je zároveň prvkem množiny 𝐵.
- každá podmnožina je podmnožinou sebe sama
- Prázdná množina je podmnožinou každé množiny
## 7. Co je to vlastní podmnožina? 
Řekneme, že množina 𝐴 je vlastní podmnožinou množiny 𝐵 (značíme 𝐴 ⊂ 𝐵 nebo také 𝐴 ⊊ 𝐵) právě tehdy, když je její podmnožinou, ale 𝐴 ≠ 𝐵.
- V množině B tedy existují prvky, které nejsou prvky množiny A  
- Platí (𝐴 ⊂ 𝐵) ⇒ (𝐴 ⊆ 𝐵), ale ne naopak!
## 8. Co je to potenční množina? 
Množinu všech podmnožin množiny 𝐴 nazveme potenční množinou množiny 𝐴 a značíme 𝒫 (A)
## 9. Kolik podmnožin má 𝑛-prvková množina? 
Potenční množina má 2<sup>n</sup> prvků
## 10. Kolik podmnožin má prázdná množina?
jednu a to prázdnou množinu 
## 11. Co je to sjednocení množin? 
Sjednocení množin (značíme 𝐴 ∪ 𝐵) je množina prvků, které patří alespoň do jedné ze sjednocovaných množin.
![[Pasted image 20251024200344.png]]
## 12. Co je to průnik množin? 
Průnik množin (značíme 𝐴 ∩ 𝐵) je množina prvků, které patří do obou množin současně.
![[Pasted image 20251024200416.png]]
## 13. Co je to rozdíl množin?
Rozdíl množin (značíme 𝐴 − 𝐵 nebo 𝐴 ∖ 𝐵) je množina prvků, které patří do množiny 𝐴 a nepatří do množiny B
![[Pasted image 20251024200502.png]]
## 14. Co to znamená, že jsou množiny disjunktní? 
nemají žádný společný prvek
## 15. Jak zní idempotentní zákony? 
𝐴 ∪ 𝐴 = 𝐴
𝐴 ∩ 𝐴 = A
## 16. Jak zní distributivní zákony? 
![[Pasted image 20251024200741.png]]
## 17. Co je to doplněk množiny? 
Nechť 𝐴 a 𝑀 jsou množiny a platí 𝐴 ⊆ 𝑀. Doplňkem množiny 𝐴 v množině 𝑀 (značíme 𝐴 ′𝑀 ) nazveme množinu všech prvků množiny 𝑀, které nejsou prvky množiny 𝐴.
• Platí 𝐴 ′𝑀 = 𝑀 − A
## 18. Jak zní de Morganovy zákony? 
###### (𝐴 ∩ 𝐵)′𝑀 = 𝐴′𝑀 ∪ 𝐵′<sub>M</sub>
###### (𝐴 ∪ 𝐵)′𝑀 = 𝐴′<sub>𝑀</sub> ∩ 𝐵′<sub>M</sub>
## 19. Jak jsou definovány číselné množiny a jak se značí?
| Název                 | Značení | Slovní popis                                                                 | Příklady                                           |
| :-------------------- | :-----: | :--------------------------------------------------------------------------- | :------------------------------------------------- |
| **Přirozená čísla**   |    ℕ    | „počítací čísla“ – používají se k počítání                                   | ( {1,2,3,4,.....} ) nebo někdy ( {0,1,2,3,.....} ) |
| **Celá čísla**        |    ℤ    | přirozená čísla, jejich záporné protějšky a nula                             | ( {.....,-3,-2,-1,0,1,2,3,.....} )                 |
| **Racionální čísla**  |    ℚ    | všechna čísla, která lze vyjádřit jako zlomek                                | ( 1/2, -3, 0, 2.75 = 11/4                          |
| **Iracionální čísla** |    —    | čísla, která **nelze** vyjádřit jako zlomek dvou celých čísel                | ( √2​,π,e)                                         |
| **Reálná čísla**      |    ℝ    | všechna čísla, která lze znázornit na číselné ose (racionální + iracionální) | ( -5, 0, 3.5, π, √2 )                              |
| **Komplexní čísla**   |    ℂ    | všechna čísla tvaru ( a + bi ), kde  i^2 = -1 , ( a,b ∈ R)                   | ( 2 + 3i, ; -1 - 4i )                              |
|                       |         |                                                                              |                                                    |
