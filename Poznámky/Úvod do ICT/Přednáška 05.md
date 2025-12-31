### Kontrolní otázky
### 1, Jaký je rozdíl mezi spojitým a diskrétním signálem? 
Spojitý (analogový) signál je dán spojitou (nebo po částech spojitou) funkcí spojitého času. Tím se liší od signálu diskrétního (digitálního), který je dán funkcí definovanou pouze v diskrétních časových okamžicích a tvoří tak posloupnosti funkčních hodnot.
### 2 Proč je možné diskrétní signál přenášet bez zkreslení? 
Protože přenášíme pouze dvě hodnoty (0 a 1), které lze při přenosu spolehlivě rozlišit i v případě výskytu rušení.
### 3 Jaký je princip kódování informací? 
Přiřazení znaků jedné abecedy znakům jiné abecedy se nazývá kódování, inverzní postup pak dekódování
### 4 Co vyjadřuje redundance kódu a jak ji můžeme spočítat? 
Redundance vyjadřuje hospodárnost kódu. Počítáme ji podle vztahu 𝑅 = 1 − 𝐻 / 𝐻max , kde 𝐻 je skutečná entropie a 𝐻max je teoretická maximální entropie při použití stejné abecedy.
### 5 Jaký je rozdíl mezi blokovým a prefixovým kódováním? 
Prefixový kód je prosté kódování, u kterého žádné kódové slovo není prefixem jiného kódového slova. Blokový kód je prosté kódování, u kterého mají všechna kódová slova stejnou délku. Protože blokový kód musí být prostým zobrazením, je nutně také prefixovým kódem
### 6 Jak u blokového kódování zjistíme délku znaků kódu?  
Počet bitů potřebných pro zakódování jednotlivých znaků zjistíme výpočtem informační entropie jevu, který je zdrojem informace.
### 7 Jak ověříme, zda lze sestrojit prefixový kód s požadovanými vlastnostmi? 
Zjistíme platnost Kraftovy nerovnosti. Pokud existuje binární prefixový kód s 𝑛 kódovými znaky a délkami kódových slov 𝑑1 , 𝑑2 , … , 𝑑𝑛 , pak platí 2 −𝑑1 + 2−𝑑2 + … + 2−𝑑𝑛 ≤ 1
### 8 Kdy je blokový kód hospodárnější než prefixový? 
Všechny symboly mají stejnou pravděpodobnost výskytu.
### 9 Jakou redundanci a entropii by měl mít optimální kód? 
Optimální (nejkratší) kód by měl mít minimální redundanci a maximální entropii.
### 10 Jakým způsobem lze najít optimální kód?
Využijeme algirimů
#### Shannonův-Fanův algoritmus
Postup pro nalezení optimálního kódu pomocí **Shannonova-Fanova algoritmu** je následující:
1. Znaky uspořádáme sestupně podle **pravděpodobnosti jejich výskytu** ve zprávě.
2. Vypočteme **kumulativní pravděpodobnosti** jednotlivých znaků.
3. Rozdělíme znaky do **dvou skupin** tak, aby jejich součtové pravděpodobnosti byly co nejblíže hodnotě **0,5**.
4. Předchozí krok se opakuje tak dlouho, dokud existují vícečlenné skupiny znaků.
#### Huffmanův algoritmus
Postup pro nalezení optimálního kódu pomocí **Huffmanova algoritmu** je následující:
1. Znaky uspořádáme sestupně podle **pravděpodobnosti jejich výskytu** ve zprávě.
2. Vezmeme **dva znaky s nejmenší pravděpodobností**, přiřadíme jim nulu a jedničku, sečteme jejich pravděpodobnosti a výsledek zařadíme podle velikosti mezi ostatní.
3. Předchozí krok opakujeme tak dlouho, až dojdeme u dvou nejmenších hodnot pravděpodobnosti k součtu **1**.
4. Hodnoty kódových znaků získáme **zpětným postupem** a „sbíráním“ nul a jedniček.
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
### McMillanova věta
**Každý jednoznačně dekódovatelný binární kód splňuje Kraftovu nerovnost.** 
(Je buď prefixový, nebo existuje jiný kód nad stejnou kódovou abecedou se stejnými délkami kódových slov, který prefixový je.)
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

