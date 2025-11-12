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
