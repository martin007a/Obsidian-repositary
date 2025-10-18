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

#### Kontrolní otázky
###### **Co to je výrok?**
Výrok je tvrzení o němž jde smysluplné prohlásit,
zda je pravdivé nebo nepravdivé.
###### **Jak je definována výroková formule?**
Za výrokovou formuli považujeme takovou posloupnost symbolů jazyka výrokové logiky pro kterou platí že: 
	-Každý elementární výrok je výroková formule
	-je-li a výrokový formule, pak také ¬a je výroková formule
	 -![[Pasted image 20250929191848.png]]
	 - nic jiného není výroková formule
###### **Co je to pravdivostní hodnota výroku?**
Pravdivostní hodnota výroku je hodnota která nabývá dvou hodnot a to TRUE/FALSE
###### **Jak vypadá pravdivostní tabulka negace, konjunkce, disjunkce, implikace a ekvivalence**
![[Pasted image 20250929192525.png]]
###### **Co to je tautologie a Kontradikce? Uveď příklady**
- **Tautologie** - Výrokovou formuli nazveme tautologie, pokud je vždy pravdivá bez ohledu na pravdivostní hodnotu výrokových proměnných, které obsahuje.
-
- **Kontradikce** - Výrokovou formuli nazveme Kontradikce, pokud je vždy nepravdivá bez ohledu na pravdivostní hodnotu výrokových proměnných, které obsahuje.
![[Pasted image 20250929193211.png]]
###### **Jaký je rozdíl mezi obměnou a obrácením Implikace**
![[Pasted image 20250929193919.png]]
![[Pasted image 20250929193959.png]]
###### **Které z logických spojek jsou Komutativní a asociativní?**
- Konjunkce
- Disjunkce
- Ekvivalence
###### **Co znamená že dva výroky jsou logicky ekvivalentní?**
Výroky jsou logicky ekvivalentní pokud mají stejnou pravdivostní hodnotu.
###### **Jak se negují složené výroky?**
![[Pasted image 20250929195006.png]]
# Kontrolní otázky
#### Co je to úplný systém logických spojek?
**Úplný systém logických spojek** je **taková množina logických spojek**, pomocí které lze **vyjádřit libovolnou výrokovou formuli**
#### Které spojky tvoří úplný systém logických spojek?
- negace, konjunkce a disjunkce
- negace a konjunkce
- negace a disjunkce
- negace a implikace
- NOR  
- NAND 
#### Jak je definována Shefferova a Peirceova spojka?
**Shefferova spojka** (nazývaná také **NAND**, anglicky _Not AND_) je negace konjunkce.
**Peirceova spojka** (nazývaná také **NOR**, anglicky _Not OR_) je negace disjunkce.
#### Co je to infixový, prefixový a postfixový zápis?
![[Pasted image 20251004210741.png]]
#### Jak vyhodnotit výraz v postfixu?
Algoritmus Kusé koleje
#### Jak převést výraz z infixu do prefixu a do postfixu?
Pomocí Stromu: 
- INFIX - Levý podstrom - Vrchol - Pravý pod strom
- PREFIX - VLP 
- POSTFIX - LPV 
#### Co je to disjunktivní a konjunktivní normální forma?
### Disjunktivní normální forma
 Výroková formule je v **disjunktivní normální formě (DNF),** je-li disjunkcí formulí (klauzulí), pro které platí: 
 - Každá je konjunkcí literálů.
 - V žádné se nevyskytuje žádná atomická formule současně se svou negací.
 **DNF je úplná**, pokud jsou ve všech konjunkcích stejné atomické formule. 
### Konjunktivní normální forma
Výroková formule je **v konjunktivní normální formě (KNF),** jeli konjunkcí formulí (klauzulí), pro které platí:
- Každá je disjunkcí literálů,
- V žádné se nevyskytuje žádná atomická formule současně se svou negací.
**KNF je úplná**, pokud jsou ve všech disjunkcích stejné atomické formule.
#### K čemu se používá DNF a KNF?
Každou složitou logickou formuli lze přepsat do **jednotného tvaru**, tedy do DNF nebo KNF.
– automatizované vyhodnocování pravdivosti 
– dokazování vlastností formulí 
– základ pro další teoretické zkoumání
#### Jaký je algoritmus převodu do DNF/KNF?
![[IMG_20250930_141405.jpg]]
#### Na jakém principu funguje Karnaughova mapa?
Výraz: $$(a⇒(b∨¬c))∧(¬a⇔b).$$
**Pravdivostní tabulka**
![[IMG_20250930_141008 1.jpg]]
K-Mapa
![[Pasted image 20251004221313.png]]
DNF
![[Pasted image 20251004221918.png]]
KNF
![[Pasted image 20251004222530.png]]
### Jak je definován jazyk predikátové logiky?
Pokud potřebujeme zkoumat nějakou vlastnost nějaké množiny začneme používat predikátovou logiku
#### **Konstrukce termů**
Jazyk se dále definuje induktivním způsobem konstrukce výrazů, počínaje **termy**, které označují prvek definičního oboru:
1. Každá **konstanta** je term.
2. Každá **individuální proměnná** je term.
3. Pokud je f funkční symbol arity n a t1​,t2​,…,tn​ jsou termy, pak f(t1​,t2​,…,tn​) je rovněž term.
4. Nic jiného není term
#### Konstrukce predikátových formulí
Výsledkem predikátové formule je logická hodnota (pravda/nepravda). **Predikátová formule** je definována následovně:
1. Je-li P predikátový symbol arity m a t1​,t2​,…,tm​ jsou termy, pak P(t1​,t2​,…,tm​) je **atomická predikátová formule**.
2. Jsou-li α,β predikátové formule, pak i (¬α), (α∧β), (α∨β), (α⇒β), (α⇔β) jsou predikátové formule (analogicky jako ve výrokové logice).
3. Je-li α predikátová formule a x individuální proměnná, pak i (∀x)α a (∃x)α jsou predikátové formule.
4. Nic jiného není predikátová formule
### Které symboly obsahuje jazyk predikátové logiky?
##### Jazyk predikátové logiky zahrnuje následující základní symboly:
• **Individuální jména (konstanty)**, značí se a,b,c,… 
- ty označují **konkrétní objekt**.
• **Individuální proměnné**, značí se x,y,z,… 
- ty **neoznačují konkrétní objekt**, ale mají svůj definiční obor.
• **Funkční symboly**, značí se f,g,h,… 
- ty přiřazují prvkům definičního oboru jiné prvky.
• **Predikátové symboly**, značí se P,Q,R,… 
- ty označují **vlastnosti a vztahy**.
• **Logické spojky** ¬,∧,∨,⇒,⇔.
• **Kvantifikátory** 
- ∀ (univerzální) 
- ∃ (existenční). 
- Existuje také zesílený existenční kvantifikátor ∃! (existuje právě jeden).
• **Závorky**.
### Které kvantifikátory jsou využívány ve formulích jazyka predikátové logiky?
 **Kvantifikátory** 
- ∀ (univerzální) 
- ∃ (existenční). 
### Jak je definována volná a vázaná proměnná ve formuli jazyka predikátové logiky?
![[Pasted image 20251018194842.png]]
### **Vázaná proměnná**

Proměnná xxx je **vázaná** (bound variable) ve formuli,  
**pokud se nachází v dosahu kvantifikátoru**, který ji váže —  
tedy uvnitř formule typu:
![[Pasted image 20251018195139.png]]

![[Pasted image 20251018195055.png]]