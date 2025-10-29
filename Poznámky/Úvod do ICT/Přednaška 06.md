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
