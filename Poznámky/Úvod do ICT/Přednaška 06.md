# Zabezpečení dat při přenosu
### Proč zabezpečovat data při přenosu?
- Přenosu uložených dat do místa jejich zpracování se nikdy nelze vyhnout
	- přenos z disku počítače do operační paměti 
	- přenosy dat prostřednictvím počítačové sítě
- V průběhu přenosu se může objevit různé rušení
	-  data nesoucí informaci nemusí být doručena ve stejné podobě, ve které byla odeslána
- **Nezáměrné rušení**
	- plyne z **technické nedokonalosti** přenosového kanálu
	- útlum signálu, působení vnějších vlivů (atmosférické poruchy, činnost jiných strojů a zařízení apod.)
- **Záměrné rušení**
	- způsobené třetími osobami
	- snaha **získat** nebo **modifikovat** přenášenou informaci
### Zabezpečení dat proti technickým nedokonalostem přenosu
**Chyba** – změna 0 → 1 nebo 1 → 0
![[Pasted image 20251029151002.png]]
## Detekční kódy
**Detekce chyby**
- zjištění, že v přeneseném úseku nastala chyba 
- přesné místo výskytu chyby však není známo
**Možnost detekce**
- parita
- kontrolní součet
**Obojí na podobném principu**
- detekce chyb s lichou násobností 
- jednoduchá realizace 
- široké použití
![[Pasted image 20251029151156.png]]
## Jednoduchá parita
- Široce používaná metoda detekce jednoduchých chyb
- Doplnění vyslaných dat **jedním paritním bitem** tak, aby celkový počet jedniček v určitém úseku dat byl 
	- sudý – **sudá parita** 
	- lichý – **lichá parita**
![[Pasted image 20251029151310.png]]
![[Pasted image 20251029151543.png]]
## Kombinovaná parita
Můžeme zavést libovolný počet paritních bitů 
- zabezpečení různých kombinací datových bitů 
- zvýšená schopnost detekce chyb
![[Pasted image 20251029151647.png]]
![[Pasted image 20251029151741.png]]
obr: prej se zabezpečuje **or**
**U příčné zabezpečujeme řádek a u podélné sloupec** 
- Chyba se při zabezpečení kombinací podélné a příčné parity projeví na několika místech
- Místo výskytu chyby v datech lze spolehlivě zjistit podle hodnoty paritních bitů
![[Pasted image 20251029151935.png]]
- Chyby s vyšší násobností nelze opravit, ale lze je alespoň detekovat
![[Pasted image 20251029152011.png]]
### Kontrolní součet
- Komplikovanější způsob zabezpečení dat s vyšší schopností detekce chyb
- Přídavný údaj vypočtený z dat zvoleným způsobem a kontrolovaný stejným postupem na přijímací straně
- Používají se **různé varianty** pro různé účely
	- **podélná parita** – součet bloku dat bez přenosu (xor) 
	- **cyklický součet (CRC)** – zjištění zbytku po dělení dvou polynomů (jeden tvoří data, druhý je vhodně zvolen) 
	- **otisk (hash)** – složitější algoritmy zabezpečení, jednosměrné šifrovací metody MD5, SHA apod. 
	- **specifické případy** – bez nutnosti přenosu zabezpečovacích informací (ISBN, IČO, VIN, číslo účtu, označení lokomotiv ČD, rodná čísla apod.)
Každý soubor na disku má **CRC** - když se soubor změní tak se změní i CRC
**hash**, jednosměrné šifrování, heslo
![[Pasted image 20251029152358.png]]
## Samoopravné kódy
- Kódy schopné chybu **detekovat** a následně **opravit**
	- použitelné všude tam, kde nestačí kombinace parit 
	- někdy nelze připustit opakované posílání chybných dat, chybu je třeba opravit na přijímací straně 
- Povolené a zakázané kódové kombinace
	- ke každé zakázané kombinaci lze jednoduše dopočítat nejbližší povolenou kombinaci
- Lineátní binární Hammingovy kódy(n,k)
	- **počet paritních bitů** 𝑐 ≥ 2 
	- **délka bloku (počet bitů kódového slova)** 𝑛 = 2𝑐 − 1 
	- **délka zprávy (počet datových bitů)** 𝑘 = 2𝑐 − 𝑐 − 1 
	- **redundance kódu** 𝑟 = 1 − 𝑘/n
![[Pasted image 20251029152939.png]]
![[Pasted image 20251029153015.png]]
![[Pasted image 20251029153441.png]]
![[Pasted image 20251029153656.png]]
## Detekce a oprava chyby
**Definice:**
- **Hammingova váha** ‖𝑢‖𝐻 kódového slova 𝑢 je rovna počtu symbolů ve slově 𝑢, které se liší od 0.
**Definice:**
- Počet změn (z nuly na jedničku nebo opačně), které musí být provedeny, abychom ze slova 𝑢 dostali slovo 𝑣, vyjadřuje **Hammingova vzdálenost** 𝑑𝐻 (𝑢, 𝑣) = ‖𝑢 ⊕ 𝑣‖𝐻 .
![[Pasted image 20251029153911.png]]
![[Pasted image 20251029154011.png]]
Zakázaná kombinace - je kombinace když udělám jednu změnu v povolené
## Detekce a oprava chyby
**Syndrom slova**
- speciální kontrolní posloupnost vypočtená příjemcem 
- binární interpretace pozice chybného bitu ve slově 
- princip výpočtu shodný jako u paritních bitů 
- tvořen posloupností bitů 𝑠 = 𝑠<sub>𝑚</sub>𝑠<sub>𝑚−1</sub> … 𝑠<sub>2</sub> 𝑠<sub>1</sub>
![[Pasted image 20251029154209.png]]
Na straně příjemce se zase spočítá XOR, to co vyjde přečtu jako binární číslo - 6. opravím 6 bit z leva. 
![[Pasted image 20251029154416.png]]
## Zkrácené Hammingovy kódy
- Nepotřebujeme využít všechny dostupné datové bity 
- Odvodíme nutný minimální počet paritních bitů 
- Stačí najít takové 𝑐, pro které platí 2 <sup>𝑐</sup> ≥ 𝑘 + 𝑐 + 1
![[Pasted image 20251029154625.png]]
### Rozšířené Hammingovy kódy
- Přidáme paritní bit zabezpečující slovo sudou paritou - zabezpečí všech 8 bitů
- Minimální Hammingova vzdálenost bude 𝑑𝐻 = 4
- Oprava jednoduchých chyb a detekce dvojitých chyb nebo pouze detekce trojitých chyb
![[Pasted image 20251029154757.png]]
![[Pasted image 20251029154817.png]]
## Rozšířené Hammingovy kódy
![[Pasted image 20251029154904.png]]
## Rozšířené Hammingovy kódy – shrnutí
![[Pasted image 20251029155231.png]]
## Grayův kód
- Též **kód konstantní změny**
- Robustní zrcadlový binární kód
- Každé dvě po sobě jdoucí kódové hodnoty se liší změnou pouze jedné bitové pozice
- **Oprava chyb v digitální komunikaci**
	- původně zabránění rušivého výstupu z elektromagnetických relé
	- pozemní a kabelové televize odpovídače sekundárního radaru v letadlech 
	- inkrementální snímače teploty nebo polohy 
	- CNC stroje, počítačové myši
## Minimalizace logických funkcí
- Karnaughovy mapy
![[Pasted image 20251029155524.png]]
# Zabezpečení proti neoprávněnému čtení
- **Šifrování** – nahrazení (kódování) původních znaků (slov) novými, aby výsledek byl zdánlivě nesmyslný
- **Kryptologie** – věda zabývající se šifrováním 
	- **kryptografie** – úkrývání obsahu zpráv, tvorba šifer a jejich aplikace, dešifrování se znalostí postupu 
	- **kryptoanalýza**(Hackeří) – dešifrování zpráv bez znalosti klíče (prolamování šifer), analýza síly šifrovacích metod
**Steganografie** – podobor kryptografie, který se zabývá ukrýváním existence zpráv, nikoli jejich obsahu
## Kryptografie (šifrování)
- Původ z řečtiny (κρυπτός = tajný, γράφειν = psát)
- **Transpoziční šifry|**
	- uspořádání písmen zprávy jiným způsobem 
	- Skytale
- **Substituční šifry**
- nahrazení písmen zprávy jinými znaky 
- je zachována pozice písmen 
- Caesarova šifra 
- Morseova abeceda 
- Vigenèrova šifra
### Obecný šifrovací postup
![[Pasted image 20251029160808.png]]
### Šifrování v počítačové podobě
- **Změna frekvenčního spektra**
	- četnosti kódových znaků nesouvisejí s četnostmi původních znaků
- **Šifrovací klíč**
	- u primitivních způsobů je to kódová tabulka náhrad 
	- u jiných způsobů je to binární posloupnost sloužící k šifrování nebo dešifrování
- **Symetrický klíč**
	- pro šifrování i dešifrování je stejný a stejně se aplikuje
	- heslo
- **Asymetrický klíč**
	- klíč má dvě části
	- pro šifrování a dešifrování slouží různé části klíče
## Asymetrické šifrování
- **Klíč má dvě části**
	- veřejná část (veřejný klíč) 
	- soukromá část (soukromý klíč)
- **Použití 1**
	- pro šifrování veřejný klíč příjemce 
	- pro dešifrování soukromý klíč příjemce 
	- zprávu přečte jen oprávněný příjemce
- **Použití 2**
	- pro šifrování soukromý klíč odesílatele 
	- pro dešifrování veřejný klíč odesílatele 
	- **příjemce dokazuje identitu odesílatele**
## Distribuce klíčů
- Certifikační autorita
	- „notář“, který osvědčuje, že určitý soukromý klíč vlastní určitá osoba 
	- umožňuje dokázat totožnost odesílatele 
	- seznam akreditovaných certifikačních autorit zveřejňuje Ministerstvo vnitra
- Hlavní funkce certifikační autority
	- generování klíčů 
	- přidělování, evidence a obnovování klíčů 
	- osvědčování vlastnictví určitého klíče
- **Kvalifikovaní poskytovatelé certifikačních služeb**
- První certifikační autorita, a. s. 
- Česká pošta, s. p. 
- eIdentity, a. s
## Vlastnosti šifrovacích způsobů
![[Pasted image 20251029161636.png]]
## Zabezpečení proti neoprávněné modifikaci
- **Otisk zprávy**
![[Pasted image 20251029161724.png]]
## Princip odeslání a přijetí bezpečné a podepsané zprávy
![[Pasted image 20251029161744.png]]
## Šifra RSA (Rivest, Shamir, Adleman)
![[Pasted image 20251029161810.png]]