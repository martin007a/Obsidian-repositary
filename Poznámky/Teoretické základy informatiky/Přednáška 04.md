1-

2
pokud je něco dokazatelné tak to je tautologie
3
# Predikátová logika
- Pokud potřebujeme zkoumat nějakou vlastnost nějaké množiny začneme používat predikátovou logiku
![[Pasted image 20251018144313.png]]
## Kvantifikátory
### Kvantifikátor univerzální  **∀**
- každý všechny
- ∀𝑥 ∈ ℕ ∶ (𝑥 + 1) ∈ ℕ
- „pro všechna přirozená čísla 𝑥 platí …“
### Existenční Kvantifikátor ∃
- existuje, některý, … 
- ∃𝑥 ∈ ℕ ∶ (𝑥 − 100) ∈ ℕ 
- „existuje přirozené číslo 𝑥 takové, že …“
### Zesílený existenční kvantifikátor ∃!
- existuje právě jeden, jediný, … 
- ∃!𝑥 ∈ ℕ ∶ (𝑥 − 1) ∉ ℕ 
- „existuje jediné přirozené číslo 𝑥, pro které platí …“
### Formální jazyk predikátové logiky
- **Individuální jména (konstanty)          𝑎, 𝑏, 𝑐, …** 
	- označují konkrétní objekt 
- **Individuální proměnné   𝑥, 𝑦, 𝑧, …** 
	- neoznačují konkrétní objekt, mají svůj definiční obor 
- **Funkční symboly  𝑓 , 𝑔, ℎ, …** 
	- přiřazují prvkům definičního oboru jiné prvky 
- **Predikátové symboly    𝑃, 𝑄, 𝑅, …** 
	- označují vlastnosti a vztahy 
- **Logické spojky    ¬, ∧, ∨,⇒,⇔** 
- **Kvantifikátory   ∀, ∃** 
- **Závorky**  
### Arita operátoru
Počet operandů, parametrů, argumentů
Podle **počtu operandů** rozlišujeme operátory na 
- nulární
- unární
- binární
- ternární
##### Binární operátory
- jejich arita je 2, mají 2 operandy
- +, −, ×, /, ∧, ∨, ⇒, ⇔
##### Unární operátory
- jejich arita je 1, mají 1 operand
- √ , ¬
### Term
• Označuje prvek definičního oboru
1. Každá konstanta je term 
2. Každá individuální proměnná je term 
3. Je-li 𝑓 funkční symbol arity 𝑛 a 𝑡<sub>1</sub> , 𝑡<sub>2</sub> , … , 𝑡𝑛 jsou termy, pak 𝑓 (𝑡1 , 𝑡2 , … , 𝑡<sub>𝑛</sub> ) je rovněž term 
4. Nic jiného není term
### Predikátová Formule
Výsledkem je logická hodnota (pravda/nepravda)
![[Pasted image 20251014132732.png]]
### Jazyk predikátové logiky
![[Pasted image 20251014133044.png]]
![[Pasted image 20251014133127.png]]
![[Pasted image 20251014133529.png]]
succ - susceader - následník 
succ(0) -> 1
(∃𝑥)(∀𝑦)(¬ succ(𝑦) = 𝑥) -> popisuje prvek 0
### Přirozený jazyk → jazyk predikátové logiky
(∀𝑥) = všichni, každý, kdo …, žádný
(∃𝑥) = existuje, někdo, něco, nějaký
![[Pasted image 20251014134624.png]]
#### Volný a vázaný výskyt proměnné
![[Pasted image 20251014134944.png]]
### Sémantika predikátové logiky
- Též hovoříme o **realizaci predikátové logiky**
- Dosud definované objekty (termy, formule aj.) popisovali pouze syntaxi
- Sémantika svazuje jazyk s objekty reálného světa
- Definuje **univerzum**, tedy množinu objektů, jejichž vlastnosti zkoumáme
- Funkční symboly odpovídají zobrazením na univerzu
- Predikátové symboly popisují vlastnosti a vztahy prvků univerza
#### Ohodnocení proměnných
![[Pasted image 20251014135151.png]]
#### Hodnota termu
Když říkáme, že něco platí **induktivně**, myslíme tím, že to **platí pro všechny přirozené čísla**, protože:
1. **Platí to pro první prvek (základ)** — obvykle pro 0 nebo 1.
2. **A pokud to platí pro nějaké číslo n, pak to musí platit i pro jeho následníka (n + 1)**.
![[Pasted image 20251014135221.png]]
### Pravdivost atomické formule
Atomická predikátová formule vzniká aplikací n-árního predikátového symbolu na n termů
#### Určeni pravdivostní hodnoty
- záleží na konkrétní realizaci predikátové logiky
- predikáty odpovídají výrokům ve výrokové logice
**Unární predikát je pravdivý právě tehdy**, když prvek, jenž je hodnotou termu, který je argumentem daného predikátového symbolu, má požadovanou vlastnost.

Predikát vyšší arity je pak pravdivý právě tehdy, když hodnoty vstupních termů splňují vlastnosti (vztahy) požadované při definici významu predikátu.
### Pravdivost formule
![[Pasted image 20251014135442.png]]
(∀𝑥) - všichni
(∃𝑥) - alespoň jeden
![[Pasted image 20251014135659.png]]
### Tautologie a negace v predikátové logice
![[Pasted image 20251014135911.png]]
### Negace predikátových formulí
![[Pasted image 20251014140748.png]]
### Negace predikátových formulí

### Omezení počtu spojek a kvantifikátorů
Vezmeme spojku která tvoří uplný systém spojek a přidáme kvantifikátor
![[Pasted image 20251014141328.png]]
### Úlohy predikátové logiky
### Splnitelná množina formulí
![[Pasted image 20251014141734.png]]
![[Pasted image 20251014141746.png]]
Našli jsme model kdy to je pravdivé,
jelikož význam tech predikátu není jedno proto to není tautologie
![[Pasted image 20251014142054.png]]
# dělat to nebudeme
## Odvozovací pravidla predikátové logiky
![[Pasted image 20251014142407.png]]
### Syntaxe predikátové logiky
![[Pasted image 20251018171802.png]]
### **Zákony distribuce kvantifikátorů**
![[Pasted image 20251018171821.png]]
![[Pasted image 20251014142458.png]]
Pravidlo specializace to dokazuje
![[Pasted image 20251014142714.png]]

