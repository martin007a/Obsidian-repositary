## Signál
- Základní podmínkou využívání informací je jejich výměna mezi příjemci a odesílateli
- Informace má nehmotnou povahu, přenos musí být proveden nějakým nehmotným procesem
- Nositelem informace nazýváme **signál**
- Fyzikální veličinu lze matematicky modelovat funkcí prostoru a času
$$𝑠 = 𝑓 (𝑥, 𝑦, 𝑧, 𝑡),$$
	kde **s** je libovolný signál vyjádřený nezávislými souřadnicemi místa **(x,y,z)** a časovaným parametrem **t** 
## Dělení signálů dle časového parametru t
**Spojité** 
- každý časový okamžik signálu nese určitou informaci
- telefonní rozhovory
**Diskrétní**
- signál nese informaci jen v některých okamžicích 
- telegrafní zprávy
**Statické**
- hodnota **t** nemá vliv na hodnotu signálu
- kniha, mapa
**Dynamické**
- hodnota signálu závisí na hodnotě **t**
- televizní přenos
## Spojitý (analogový) signál
Je vždy získáván **ze vstupu**
- mikrofon, kamera, snímač teploty, …
![[Pasted image 20251022152657.png]]
### Diskrétní (digitální) signál
![[Pasted image 20251022152816.png]]
## Přenosový řetězec
**Informační vazba** - vzniká mezi dvěma systémy tvorbou, přenosem a výměnou informace.
- Informační vazba umožnuje tzv. **Komunikaci**
![[Pasted image 20251025111458.png]]
# Kódování dat
- Informaci je pro tento účel nutné **transformovat**, Nahrazení znaků abecedy jinou abecedou
- Základní podmínkou komunikace je vytvoření signálního komunikačního kanálu
- Přiřazení znaků jedné abecedy znakům jiné abecedy se nazývá **kódování**, inverzní postup pak **dekódování**
- Předpis, který toto přiřazování definuje, se nazývá **kód**
## Kvalita kódování, redundance
- Z hlediska optimálního přenosu je efektivní kód, který obsahuje **minimální počet informačních prvků,** každý znak kódu tedy má **maximální entropii**
- Maximální entropii má kód, kde všechny znaky abecedy jsou stejně možné a jejich vzájemný výskyt není závislý
- Kvantitativně je hospodárnost kódu vyčíslitelná **redundancí (nadbytečností)**
![[Pasted image 20251022153351.png]]
- 𝐻 – skutečná entropie kódu – 
- 𝐻max – maximální entropie při použití téže abecedy 
Redundance evropských jazyků je větší než 0,5 (0,75?)
### Příklady kódů
![[Pasted image 20251025125244.png]]
## Důležité souvislosti
##### Entropie zdroje zpráv
- uvažujeme pravděpodobnosti výskytu znaků ve zprávě
Entropie kódu
- uvažujeme pravděpodobnosti nul a jedniček v kódu 
- v ideálním případě je entropie binárního kódu rovna 1
Střední délka kódového slova
- průměrný počet bitů nesených jedním znakem 
- v nejlepším případě je rovna entropii zdroje zpráv 
- nejdůležitější kritérium pro srovnání kvality kódu
## Způsoby kódování
##### Rovnoměrné (blokové) kódování
- **Baudotovo kódování**
- každému znaku je přiřazen stejně dlouhý kód
- délku kódového slova zjistíme výpočtem entropie
- obvykle je jednodušší a rychlejší na zpracování
- méně hospodárné
##### Nerovnoměrné (prefixové) kódování
- každému znaku je přiřazen jinak dlouhý kód 
- žádný symbol kódové abecedy není prefixem jiného 
- pro konstrukci a zpracování je obtížnější 
- může však být maximálně hospodárné 
- příklady: Shannonovo-Fanovo kódování, Huffmanovo kódování
## Nerovnoměrné kódování
![[Pasted image 20251022155617.png]]
**Kód 3 je prefixový** - budeme s ním dále pracovat
### Konstrukce prefixového kódu
Binární prefixový kód pro 𝑛 kódových znaků s délkami kódových slov 𝑑<sub>1</sub> , 𝑑<sub>2</sub> , … , 𝑑<sub>𝑛</sub> existuje právě tehdy, pokud platí **Kraftova nerovnost**:
![[Pasted image 20251022160106.png]]
### Shannonův-Fanův algoritmus pro nalezení optimálního kódu
![[Pasted image 20251022160332.png]]
![[Pasted image 20251022160715.png]]
Průměrný počet znaků na znak?
## Huffmanův algoritmus
![[Pasted image 20251022160652.png]]
![[Pasted image 20251022160754.png]]
## Souvislosti a spolehlivá metoda srovnání
• Kritéria pro hledání optimálního kódu: 
- minimální délka kódub - pro účely přenosu 
- maximální entropie kódu – pro účely komprese
![[Pasted image 20251022161137.png]]
Neexistuje žádný bezztrátový algoritmus který by byl schopen to uložit na menším prostoru než 2.24.
#### Efektivita kódu v praxi

