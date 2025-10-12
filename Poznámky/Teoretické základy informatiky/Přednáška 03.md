### Formální definice úsudku
**Značka ⊢** se nazývá **tvrzení (derivační) symbol** nebo také **syntaktický znak odvození**.  
Čte se například jako „⊢“ = _„je dokazatelné“, „plyne z“, „lze odvodit“_.
![[Pasted image 20251007132550.png]]
### Ověření správnosti úsudku
![[Pasted image 20251007132617.png]]
### Ověření správnosti úsudku
![[Pasted image 20251007133031.png]]
#### Příklad
![[Pasted image 20251007133113.png]]
- Výroku to nevyplívá
#### Příklad řešení
![[Pasted image 20251007133218.png]]
#### Příklad
![[Pasted image 20251007133755.png]]
## Pravidla
![[Pasted image 20251007134201.png]]
#### Substituční pravidla
![[Pasted image 20251007134636.png]]
### Odvození formulí
**Příklad- dokažte, že platí: (𝑎 ∨ 𝑏), (𝑎 ⇒ 𝑐), (𝑏 ⇒ 𝑑) ⊢ (𝑐 ∨ 𝑑)**
![[Pasted image 20251007134800.png]]
// Tohle po vás chtít nebudeme Ph.D Haluza
#### Splnitelnost množiny formulí
![[Pasted image 20251007135322.png]]
#### Klauzule, rezolventa
![[Pasted image 20251007135207.png]]
![[Pasted image 20251012162022.png]]
### Rezoluční metoda ve výrokové logice
![[Pasted image 20251007140018.png]]
- ψ⊂ψ′ tedy znamená, že všechny formule z ψ\psiψ jsou také ve ψ′\psi'ψ′, ale ψ′\psi'ψ′ obsahuje **nějaké další** navíc.
- Důkaz sporem
### Základní pravidla redukce klauzulí
| Název pravidla                                 | Popis                                                                                                           | Příklad                                                                                     |
| ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| **1. Odstranění tautologií**                   | Každá klauzule, která je **vždy pravdivá**, se může odstranit.                                                  | `{p, ¬p, q}` → tato klauzule je tautologie (protože obsahuje `p` i `¬p`), lze ji odstranit. |
| **2. Odstranění duplikátů literálů**           | V rámci jedné klauzule odstraníme opakující se literály.                                                        | `{p, p, ¬q}` → `{p, ¬q}`                                                                    |
| **3. Odstranění duplikátů klauzulí**           | Pokud je tatáž klauzule v množině vícekrát, ponecháme ji jen jednou.                                            | `{{p}, {p}, {¬q}}` → `{{p}, {¬q}}`                                                          |
| **4. Pravidlo subsumpce**                      | Pokud jedna klauzule je **podmnožinou** jiné, odstraníme tu větší.                                              | `{p}` a `{p, q}` → `{p}` subsumuje `{p, q}` → `{p, q}` odstraníme.                          |
| **5. Jednotková propagace (unit propagation)** | Pokud máme klauzuli s jediným literálem, můžeme ji použít k odstranění jejích komplementů z ostatních klauzulí. | `{p}`, `{¬p, q}` → z druhé klauzule odstraníme `¬p`, dostaneme `{q}`.                       |
| **6. Částečná evaluace(nepovinné)**            | Pokud je v klauzuli literál, který je již pravdivý podle nějaké jednotkové klauzule, klauzuli můžeme odstranit. | `{p}`, `{p ∨ q}` → druhá je pravdivá, odstraníme ji.                                        |

#### Příklad
![[Pasted image 20251007141055.png]]
- tady není 
## Příklad
Další vlastnosti úsudku
![[Pasted image 20251007142421.png]]


-Není nemocný jen přeplý
### Co je to úsudek a jak zní jeho formální definice?
**Úsudek** je **myšlenkový proces**, při kterém **z jedné nebo více vět (premis)** odvozujeme **novou větu (závěr)**.
Příklad:
> Premisa 1: Všichni lidé jsou smrtelní.  
> Premisa 2: Sokrates je člověk.  
> ————————————————  
  Závěr: Sokrates je smrtelný.
 To je **úsudek** — z daných výroků jsme logicky odvodili nový.
![[Pasted image 20251012175950.png]]J
### Jak ověřujeme správnost úsudku?
Z předpokladů 𝑃1 , 𝑃2 , … , 𝑃𝑚 vyplývá závěr 𝑍 právě tehdy, když formule (𝑃1 ∧ 𝑃2 ∧ … ∧ 𝑃𝑚) ⇒ 𝑍 je dokazatelná
Formule je ve výrokové logice dokazatelná právě tehdy, když je tautologie. Úsudek 𝑃1 , 𝑃2 , … , 𝑃𝑚 ⊢ 𝑍 je tedy správný, jestliže formule (implikace důsledku z konjunkce premis) 
(𝑃1 ∧ 𝑃2 ∧ … ∧ 𝑃𝑚) ⇒ 𝑍 
je tautologie.
Neznamená to, že závěr či některý předpoklad musí být pravdivý. Jde o platné úsudkové schéma, nutný vztah mezi předpoklady a závěrem. Pokud jsou pravdivé všechny předpoklady, pak musí být pravdivý i závěr.
### Co říká odvozovací pravidlo „modus ponens“?
Nechť 𝑋 a 𝑌 jsou formule. Potom platí 𝑋 ⇒ 𝑌 , 𝑋 ⊢ 𝑌 .
### Co říká odvozovací pravidlo „modus tollens“?
Nechť 𝑋 a 𝑌 jsou formule. Potom platí 𝑋 ⇒ 𝑌 , ¬𝑌 ⊢ ¬𝑋. Tomuto pravidlu říkáme modus tollens.
### Co je to substituční pravidlo a která substituční pravidla známe?
Když dvě formule znamenají totéž (jsou ekvivalentní),  
můžeme v libovolném logickém výrazu jednu nahradit druhou,  
aniž by se změnila pravdivost celé formule.
#### Substituční pravidlo pro proměnnou
Buď 𝑋 formule a 𝑞 její proměnná. Jestliže do 𝑋 za 𝑞 dosadíme formuli 𝐴, pak formuli vzniklou touto substitucí označíme 𝑆(𝐴/𝑞, 𝑋 ). Pak platí 𝑋 , (𝐴 ⇔ 𝑞) ⊢ 𝑆(𝐴/𝑞, 𝑋 ). Je-li formule 𝑋 tautologie, pak platí ⊢ 𝑆(𝐴/𝑞, 𝑋 ).
#### Substituční pravidlo pro formuli
Buď 𝑋 formule a 𝐵 její podformule. Jestliže do 𝑋 za 𝐵 dosadíme formuli 𝐴, pak formuli vzniklou touto substitucí označíme 𝑆(𝐴/𝐵, 𝑋 ). Pak platí 𝑋 , (𝐴 ⇔ 𝐵) ⊢ 𝑆(𝐴/𝐵, 𝑋 ).
### Jak vypadá odvození formule?
![[Pasted image 20251012184002.png]]
#### K čemu je rezoluční metoda a jaký je její princip?
**Rezoluční metoda** je **mechanický způsob dokazování** logické odvoditelnosti — tedy určuje, jestli z daných **premis** logicky **plyne** nějaký **závěr**.
![[Pasted image 20251012184338.png]]