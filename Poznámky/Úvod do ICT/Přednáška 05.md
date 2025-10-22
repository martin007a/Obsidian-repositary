## Signál
![[Pasted image 20251022152540.png]]
## Dělení signálů dle časového parametru t
![[Pasted image 20251022152619.png]]
## Spojitý (analogový) signál
Je vždy získáván **ze vstupu**
- mikrofon, kamera, snímač teploty, …
![[Pasted image 20251022152657.png]]
### Diskrétní (digitální) signál
![[Pasted image 20251022152816.png]]
## Přenosový řetězec
Informační vazba - vzniká mezi dvěma systémy tvorbou, přenosem a výměnou informace.
- Informační vazba umožnuje tzv. **Komunikaci**
![[Pasted image 20251022153020.png]]
# Kódování dat
- Nahrazení znaků abecedy jinou abecedou
- Základní podmínkou komunikace je vytvoření signálního komunikačního kanálu
- Přiřazení znaků jedné abecedy znakům jiné abecedy se nazývá kódování, inverzní postup pak dekódování
## Kvalita kódování, redundance
- Z hlediska optimálního přenosu je efektivní kód, který obsahuje minimální počet informačních prvků, každý znak kódu tedy má maximální entropii
- Maximální entropii má kód, kde všechny znaky abecedy jsou stejně možné a jejich vzájemný výskyt není závislý
- Kvantitativně je hospodárnost kódu vyčíslitelná redundancí (nadbytečností)
![[Pasted image 20251022153351.png]]
- 𝐻 – skutečná entropie kódu – 
- 𝐻max – maximální entropie při použití téže abecedy 
Redundance evropských jazyků je větší než 0,5 (0,75?)
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
