### Potřebnost komprese
**Redundance v datech** 
- na první pohled neúsporné ukládání 
- pro efektivní zpracování dat ale nezbytné
**Vznik redundance**
- nedokonalým kódováním dat 
- nutností rychlého přístupu k datům 
- přidáním zabezpečovacích prvků
**Cíl komprese**
- zmenšení velikosti dat při zachování všech důležitých informací, které obsahují původní data 
- odstranění redundance (nadbytečných informací) 
- odstranění irelevance (nepodstatných informací)
### Vnitřní fragmentace
Každý disk je složen z **alokačních bloků** určité délky
- soubor zabírá vždy určitý počet alokačních bloků 
- poslední alokační blok souboru není zcela využit
**Velikost souboru ≤ skutečný prostor na disku**
Shrnutí více souborů do jednoho archivu znamená **eliminaci vnitřní fragmentace**
- i bez komprese jde o zmenšení prostoru na disku
### Základní pojmy
**Hrubá komprimovaná (čistá data)část **
- objem dat před kompresí a po kompresi
**Kompresní poměr**
- vyjádření efektivity komprese různým způsobem
- ℎ/𝑘 – udává násobek hrubých dat 
- 𝑘/ℎ ⋅ 100 – **na kolik procent** se data zmenšují 
- (1 − 𝑘/ℎ) ⋅ 100 – **o kolik procent** se data zmenšují
**Režijní informace**
- metadata o původních datech a použité metodě
- nezbytné pro rekonstrukci původních dat
**Záporná komprese**
- nežádoucí jev, data kompresí zvětšují objem
### Druhy kompresí
![[Pasted image 20251112153558.png]]
![[Pasted image 20251112153611.png]]
### Metoda proudového kódování
**Run Length Encoding** 
- kódování délkou běhu, proudové kódování 
- **běh** = posloupnost stejných hodnot
**Základní princip – zhuštění opakovaný**
- zhuštění opakovaných znaků, které se v souboru vyskytují bezprostředně po sobě
- **paket RLE** – proudové číslo (opakovač) a hodnota
Dosažený kompresní poměr závisí na charakteru dat
![[Pasted image 20251112154134.png]]
- využití u Fotografii 
- Problém je když se data střídají
**Použití metody** -
 - problém způsobují střídavá data (záporná komprese) 
 - není vhodné pro textové soubory ani většinu binárních 
 - ideální pro jednoduché obrázky (max. 256 barev)
 **Úrovně komprese** 
 **bitová** – monochromatické rastrové obrazy 
 **bajtová** – rastrové obrazy s hloubkou 1 bajt na pixel 
 **pixelová** – obrazy v pravých barvách 
 na každé úrovni speciální tvar opakovače
![[Pasted image 20251112154421.png]]
![[Pasted image 20251112154924.png]]
### Modifikovaná metoda RLE
- Snaha o eliminaci záporné komprese 
- Každý paket se skládá ze **tří bajtů** 
	- příznaková hodnota (escape sekvence) 
	- proudové číslo 
	- proudová hodnota
![[Pasted image 20251112155115.png]]
### Složitější kompresní metody
**Statistické metody** 
- četnost výskytů znaků v komprimovaném souboru 
- Shannonovo-Fanovo kódování 
- Huffmanovo kódování 
- aritmetické kódování
**Slovníkové metody** 
kódování všech vyskytujících se posloupností 
LZW, LZMA 
Deflate 
CCITT
**Transformační metody** 
- ortogonální nebo jiné transformace 
- JPEG
## Aritmetické kódování
- Neztrátová kompresní metoda 
- Entropické kódování s proměnlivou délkou slova 
- Celý vstupní text je zakódován do jednoho čísla 0 ≤ 𝑛 < 1 
- Hardwarově velmi náročná metoda 
- **Princip kódování** -
	- rozdělení intervalu ⟨0; 1) podle pravděpodobnosti jednotlivých prvků ze vstupní abecedy 
	- po přečtení prvního znaku výběr příslušného podintervalu a jeho rozdělení 
	- rekurzivní pokračování do přečtení posledního znaku 
	- výsledný interval reprezentuje danou zprávu 
	- stačí vybrat libovolné číslo z intervalu