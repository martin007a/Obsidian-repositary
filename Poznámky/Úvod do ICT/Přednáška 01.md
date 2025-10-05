## **Číselné soustavy** 
- Číslo je zapsáno pomocí elementárních symbolů zvaných číslice a jejich kombinací
- Počet elementárních symbolů určuje základ soustavy, který není v soustavě nikdy obsažen
- Nekonečně mnoho soustav, ale vždy stejný princip
### Dělení podle způsobu určení hodnoty čísla
* nepoziční soustavy
- poziční soustavy
#### Nepoziční soustavy
- Dnes téměř nepoužíváno, spíše historická záležitost
-  Hodnota symbolu (číslice) není dána jeho umístěním v sekvenci symbolů (čísle)
 - Neobsahují symboly pro nulu
##### Významné nepoziční soustavy
- egyptské číslice
- řecké číslice
- římské číslice
##### Egyptské číslice
 - **Démotické číslice** 
    Rosettská deska (Rozšífrovaání hieroglyfů) 
- **Koptské číslice** 
##### **Řecké číslice**
![[Pasted image 20251005122047.png]]
##### **Římské číslice** 
ZÁKLAD tvoří 7 písmen latinské abecedy 
- Vetší čísla předchází vetší - bylo porušeno třeba pro 4 a 9 
- Hodnota je součtem 
- 1999 MCMXCIX 
### **Poziční soustavy** 
**Hodnota každého symbolu** (číslice) je dána jeho umístěním v sekvenci symbolů (čísle)
- – tím je dána váha pro výpočet celkové hodnoty čísla
**Nezbytný předpoklad:** objevení symbolu pro nulu 1 poziční nula – vyplňuje prázdné místo v čísle 2 nula ve významu „žádné množství“ – později
- **Babylónské číslice** 
	Poziční soustava se základem 60 (hodinky, úhly) 
- **Mayské** 
	Ve třetím řádu používaly 360 místo 400 
- **Čínské číslice**  
	Poziční 
- **Indické číslice** 
	Největší vliv na vývoj dnešních číslic 
	Vznik speciálních symbolů pro čísla 1-9 
- **Arabské číslice** 
	Východoarabské číslice 
	Západoarabské číslice - dnes používáme 
### Jedničková soustava
Číslo je vyjádřeno opakováním jediného symbolu 
Speciální případ poziční soustavy  
- „pozice“ symbolu může ulehčit počítání 
- nelze řadit mezi nepoziční soustavy
## Současné poziční soustavy
#### **Polyadické soustavy** 
- poziční systém s jedním nebo více základy
- Základem přirozené číslo >= 2
- nejčastější 𝑧-**adické soustavy** o jednom základu **𝑧** 
- počet dostupných symbolů pro číslice **je roven 𝑧**
#### Základy používané v historii 
- tucty (12), veletucty (144), kopy (60) 
- hodiny (24), minuty (60), vteřiny (60)
- úhlové stupně (360) 
- staroanglická libra, šilink (20), pence (12), farthing (4)
#### Možnosti jak vyjádři číslo
- **Zápis poziční**
	𝐴<sub>𝑧</sub>=(𝑎<sub>𝑛</sub>𝑎<sub>𝑛−1</sub>…𝑎<sub>1</sub>𝑎<sub>0</sub>,𝑎<sub>−1</sub>𝑎<sub>−2</sub>…𝑎<sub>−𝑚</sub>)<sub>z</sub> 
 - **Polynomem** 
	![[Pasted image 20250924205244.png]]
Význam proměnných 
- 𝑎<sub>𝑖</sub> je 𝑧-adická číslice na pozici 𝑖 (0≤𝑎<sub>𝑖</sub> <𝑧)
- 𝑖 je **řád** (pozice) číslice, který určuje její váhu v čísle
- 𝑛 je nejvyšší řád s nenulovou číslicí (𝑛∈ℕ<sub>0</sub>)
- 𝑚 je nejnižší řád s nenulovou číslicí (𝑚∈ℕ<sub>0</sub>) 
### Vyjádření čísel v 𝑧-adické soustavě
![[Pasted image 20251005123125.png]]
#### Číselné soustavy a záporná čísla
Definice standardních polyadických soustav uvažují pouze nezáporná čísla
- k čemu vlastně potřebujeme záporná čísla? 
- v Evropě záporná čísla až od 15. století
Pro vyjádření **záporného čísla** nutno použít nějaký předem dohodnutý způsob zápisu 
- běžně používáme symbol (unární operátor) **minus**
Počítač při práci se zápornými čísly používá některý z tzv. **číselných kódů** 
- transformace z omezené množiny celých čísel do omezené množiny nezáporných čísel
##### Čtyři nejvýznamnějším soustavy 
- **Desítková soustava 0-9**
- **Dvojková soustava 0,1** 
- **Osmičková soustava 0-7** 
- **Šestnáctková - používa 16 symbolů 10 čísel 6 písmen** 
#### Podoba čísel ve významných soustavách
![[Pasted image 20251005124153.png]]
**Morseova abeceda je 3 soustava** 
## Proč binární soustava?
Počítač je zařízení, které zpracovává jen číselné údaje 
- Tyto číselné údaje jsou v počítači uloženy ve dvojkové soustavě, tj. vše pouze v podobě 0 a 1
- Logické obvody počítačů pracují pouze se dvěma různými stavy – zapnuto (1), vypnuto (0), technicky není problém rozlišit (proud protéká × neprotéká) 
- Nejmenší jednotkou paměti počítače je buňka, která dokáže uchovat právě takovou informaci (**1 bit**)
### **Převody mezi soustavami** 
Hledáme ekvivalentní zápis daného čísla v číselné soustavě o jiném základu
Z praktického hlediska jsou užitečné převody 
- ze soustavy o základu 10 do libovolné soustavy  
- z libovolné soustavy do soustavy o základu 10 
- mezi soustavami o mocninách stejného základu
![[Pasted image 20251005124656.png]]
Číslo je nutno před převodem **rozložit na**
- celou část – koeficienty 𝑎<sub>i</sub>, kde 0 ≤ 𝑖 ≤ 𝑛 
- zlomkovou část – koeficienty 𝑎𝑖, kde −𝑚 ≤ i <0
- každá část se převádí odlišným způsobem
### Převod z desítkové soustavy do libovolné
##### Převod celé části 
- postupně dělíme základem cílové soustavy  
- zapisujeme zbytky po dělení (operace modulo) 
- výpočet končí, když je celá část 0 
- ekvivalent celé části v cílové soustavě pak představují **zbytky po dělení zapsané v opačném pořadí**
##### Převod zlomkové části 
- postupně násobíme základem cílové soustavy  
- zapisujeme celočíselné výsledky 
- výpočet končí, když je desetinná část 0 
- ekvivalent zlomkové části v cílové soustavě pak představují **celočíselné výsledky dělení**
![[Pasted image 20251005125125.png]]
#### Problémy při převodu zlomkové části
- ve zdrojové soustavě je každé číslo **přesné** 
- v cílové soustavě může být **neúplné**
Neúplnost čísla se projeví při aritmetických operacích 
- výsledek jakékoli operace je zatížen chybou
Pokud má číslo v cílové soustavě nekonečný nebo periodický rozvoj, musíme zvolit **požadovanou přesnost** 
- tedy počet platných číslic zlomkové části 
- o „desetinných místech“ můžeme hovořit pouze v souvislosti s desítkovou soustavou!
## Převod z libovolné soustavy do desítkové
#### Vyjádřením hodnoty čísla zapsaného polynomem
![[Pasted image 20251005130918.png]]
#### **Hornerovo schéma** - možnost jak si to ulehčit 
- základ soustavy vždy v první mocnině 
- zvlášť pro celou část 𝐶 a zlomkovou část Z
![[Pasted image 20251005131859.png]]
### Převody mezi příbuznými soustavami
- Základem obou soustav je mocnina stejného čísla 
- Jedna číslice v soustavě o základu 𝑧 𝑛 představuje
Převod mezi soustavami o základu $2^n$
![[Pasted image 20251005133238.png]]
### Sčítání
Pokud je při sčítání součet v některém řádu větší nebo roven základu, provedeme přenos do vyššího řádu 
- pravidlo platí pro všechny polyadické soustavy 
- kdo umí sčítat (pod sebe) v desítkové soustavě, umí sčítat v libovolné soustavě
###### **Obecný princip sčítání v soustavě o základu 𝑧** 
- postupujeme od nejnižšího řádu k nejvyššímu 
- v každém řádu určíme hodnotu součtu 
- tuto hodnotu vyjádříme jako 𝑎 ⋅ 𝑧 + 𝑏 
- hodnotu 𝑏 ∈ ℕ zapíšeme jako součet daného řádu 
- hodnotu 𝑎 ∈ ℤ+ 0 přeneseme do vyššího řádu 
Součtem dvou čísel o 𝑛 číslicích dostaneme číslo o nejvýše 𝑛 + 1 číslicích
### Odčítání
Princip opět platný pro všechny polyadické soustavy 
###### Obecný princip odčítání v soustavě o základu 𝑧 
- postupujeme od nejnižšího řádu k nejvyššímu 
- v každém řádu určíme hodnotu rozdílu 
- tuto hodnotu vyjádříme jako −𝑎 ⋅ 𝑧 + 𝑏 
- hodnotu 𝑏 ∈ ℕ zapíšeme jako rozdíl daného řádu 
- hodnotu 𝑎 ∈ ℤ+ 0 (výpůjčku) vrátíme do vyššího řádu
![[Pasted image 20251005134525.png]]
### **Násobení a dělení**
Násobení na stejném principu pro všechny soustavy 
- dílčí součty jsou ve stejné soustavě jako činitelé!
Dělení lze provést také, ale prakticky se nepoužívá
###### Jak realizuje výpočty počítač?
- sčítání – dle uvedeného principu 
- odčítání – přičítáním opačného čísla 
- násobení – opakovaným sčítáním 
- dělení – opakovaným „odčítáním“
### Kontrolní otázky
### Jaký je rozdíl mezi poziční a nepoziční soustavou?
**Poziční soustava:**  
Hodnota číslice závisí na její **pozici** (mocnině základu).  
Př.: 25410=2⋅102+5⋅101+4⋅100254_{10} = 2·10^2 + 5·10^1 + 4·10^025410​=2⋅102+5⋅101+4⋅100.
**Nepoziční soustava:**  
Hodnota číslice **nezávisí na poloze**, každá značka má pevnou hodnotu.  
Př.: římské číslice (X = 10, V = 5).
#### Jak je u pozičních soustav určena hodnota číslice?
Hodnota číslice je dána součinem:
každá číslice má hodnotu podle své **pozice (exponentu základu)** v zápisu čísla
#### Jakými způsoby lze vyjádřit číslo v poziční soustavě?
- pozičním zápisem
  5689
 - polynomem (hodnotou v desítkové soustavě)
   ![[Pasted image 20251005140319.png]]
#### Jaký je vztah mezi základem soustavy a počtem dostupných symbolů pro vyjádření čísla?
 Počet dostupných symbolů (číslic) je **rovný základu soustavy**.  
Např.:
- základ 10 → číslice 0–9,
- základ 2 → číslice 0, 1,
- základ 16 → číslice 0–9, A–F.
#### Jaké vlastnosti má binární číselná soustava?
- Používá **dvě číslice**: 0 a 1.
- Každá pozice představuje mocninu 2.
- Jednoduchá pro **elektronické obvody** (dva stavy – zapnuto/vypnuto).
- Je základem **digitální techniky a počítačů**.
#### Které další soustavy jsou důležité pro informatiku?
- **Oktalová (z=8)** – zjednodušený zápis binárních čísel.
- **Hexadecimální (z=16)** – kompaktní zápis binárních hodnot (např. v programech, paměťových adresách).
#### Jakým způsobem lze převést číslo mezi soustavami?
- Vyjádřením hodnoty čísla zapsaného polynomem
- Hornerovo schéma
- Převod mezi soustavami o základu 2<sup>n</sup>
#### Jaká jsou pravidla pro sčítání a odčítání?
**Sčítání:**
- Sčítáš číslice po sloupcích.
- Pokud je součet ≥ základ, přenášíš 1 do vyššího řádu.
**Odčítání:*
- Odčítáš číslice po sloupcích.
- Pokud je menšitel větší než menšenec, **půjčíš 1** z vyššího řádu (tj. přičteš základ k číslici).
#### Jakým způsobem realizuje aritmetické operace počítač?
Sčítáním 1 a 0
odčítání - přičtením záporného čísla
násobení - opakovaně sčítá
dělení - opakovaně odčítá