 - Každý (digitální) počítač je postaven na určitém typu základního **spínacího elementu;** dnes jsou to polovodičové prvky, většinou tranzistory MOSFET.
 - Termín **digitální počítač** používáme pro zařízení, které provádí sekvenci výpočetních kroků nad datovými položkami s diskrétními hodnotami(Binární hodnoty atd.).
	 - *Diskrétní hodnota je taková hodnota, která může nabývat **jen určitých, oddělených (nespojité) množin hodnot**.*
 - Alternativou je **analogový počítač**, který pracuje s hodnotami, jež se v čase plynule mění.
#### Digitální počítač
* Digitální výpočty mají výhodu v přesnosti
* Jelikož se stali levnými a vysoce spolehlivými, analogové výpočty byli omezeny jen na několik speciálních případů.
### Historie Počítačů
**Počítač** je stroj na automatické zpracování dat podle předem připraveného programu
- Období vzniku: 30. léta 20. století (Konrad Zuse, Německo)
- Další vývoj: USA 40. léta 20. století, Významný vliv matematika Johna von Neumanna - Mnohé jeho principy platí do dnes.
#### Technický princip 
Každý (digitální) počítač je postaven na určitém typu základního **spínacího elementu** 
- Elektromagnetická relé
- Elektronky
- Tranzistory
- Integrované obvody ("čipy", obsahují tranzistory, diody, rezistory....)
##### Generace podle spínacích prvků

| Generace                                | Spínací prvek                                    |
| --------------------------------------- | ------------------------------------------------ |
| Nultá generace (30. léta – 40. léta)    | Hlavní prvek: **Relé**                           |
| První generace (40. léta – 50. léta)    | Hlavní prvek: **Elektronky**                     |
| Druhá generace (50. léta – 60. léta)    | Hlavní prvek: **Tranzistory (BJT)**              |
| Třetí generace (60. léta – 70. léta)    | Hlavní prvek: **Integrované obvody (IC)**        |
| Čtvrtá generace (70. léta – současnost) | Hlavní prvek: **Mikroprocesory (VLSI – MOSFET)** |
Vývoj: **Relé → Elektronka → Tranzistor → Integrovaný obvod / Mikroprocesor**
 
### Nultá Generace (30. léta – 40. léta)
Hlavním prvkem je **Relé**
- První programovatelné stroje
- Nízká rychlost, vysoká poruchovost, experimentální charakter
 ![[Pasted image 20250928145142.png]]
##### Reléjový počítač Z3
První programovatelný počítač
- **2600 relé**
- V paměti mohlo být 64 slov dlouhých 22 bitů.
- Frekvenci hodinového signálu měl **5,3 Hz** a délku slova **22 bitů**
- Rychlost sčítání 0,8 s a rychlost násobení 3 s
- Jeho spotřeba byla 4000 wattů a vážil 1tunu
- Výpočty prováděl v binární soustavě a pracoval s čísli s plovoucí desetinou čárkou
- Četl instrukce z děrovaného filmu
- Byl používán k výpočtu vibrací křídel v DLV 
- Zničen při náletu na Berlín v roce 1943
![[Pasted image 20250928145902.png]]
### První generace (40. léta – 50. léta)
- Hlavní prvek: Elekronky
- Příklady: ENIAC, UNIAC
- Velké, energeticky náročné, časté poruchy
#### Elektronka (vacuum tube)
- Baňka (obvykle skleněná, evt. kovová), z níž je vyčerpaný vzduch.
- Vakuum umožní, že ze záporné elektrody (=katody) zahřáté pomocí wolframového vlákna (jako v klasické žárovce) se emitují elektrony.
- Elektrony dopadají na kladně nabitou anodu a _elektronkou teče proud_.
- S tímto principem pracuje vakuová dioda, používaná jako usměrňovač → elektrony tečou jen od katody k anodě, ne naopak.
### Řízení proudu v elektronce
Intenzita proudu může být řízena_ dodatečnými elektrodami — _mřížkami_
- Záporně nabytá mřížka elektrony odpuzuje a tedy brzdí.
- Elektronka se tedy může sloužit jako 
**Usměrňovač**
- **dioda** — není třeba mřížka; elektrony tečou vakuem mezi katodou a anodou samy
**Zesilovač**
- malá změna mřížkového napětí způsobí změnu anodového proudu (obvykle **trioda**, **pentoda**)
**Spínač**
- záporné mřížkové napětí zastaví anodový proud
### Druhá generace (50. léta - 60. léta)
Hlavní prvek: polovodiče, konkrétně **Tranzistory (BJM)**
- Menší, spolehlivější, nižší spotřeba
- Vznik komerčních Počítačů
#### Polovodiče
- Základem těchto počítačů (ale i dnešních) jsou elektronické prvky založené na schopnosti určitých látek _vést proud jen za jistých okolností_ (jen jedním směrem, za přítomnosti elektrického pole, světla…​)
- Takovým látkám říkáme **polovodiče**.
- **Polovodičové spínací prvky** (zejména **tranzistory** různých provedení) jsou fundamentem současné elektroniky a počítačové techniky: od rádií přes senzory, paměti až k výkonným CPU.
#### Vodivost různých látek
**Kovy**
- Proud vedou volné elektrony.
**Izolanty**
- Proud téměř nevedou kvůli nedostatku volných elektronů.
**Polovodiče**
- Vedení proudu závisí na obohacení a vnějších podmínkách, jako je teplota, osvětlení či elektrické pole, které mění počet volných nosičů.
- Mohou se tak chovat buď jako vodiče, nebo jako izolanty.
### Historie polovodičových prvků

Dioda (1920s–1930s)
- první polovodičové součástky (usměrňovače)
- umožnila nahradit elektronky (tedy vakuové diody) zejména v usměrňovačích v napájecích zdrojích

Bipolární tranzistor – BJT (1947)
- objev na Bell Labs (Brattain, Bardeen, Shockley)
- revoluce v zesílení signálů a spínání
- základ pro první integrované obvody

MOSFET (1960s)

- Metal–Oxide–Semiconductor Field-Effect Transistor
- velmi nízká spotřeba, snadná miniaturizace
- umožnil vznik mikroprocesorů a dnešní digitální elektroniky

**➡ Vývoj: od jednoduché **diodové funkce**, přes univerzální **zesílení BJT**, až k masové integraci díky **MOSFETům**.**
### Bipolární tranzistory
- Bipolární tranzistor (Bipolar Junction Tranzistor)
- Prvek se třemi elektrodami (výhody)
- emitor (= zdroj nosičů náboje)
- báze (řídící elektroda - proud mezi bází a emitorem řídí mnohem vyšší proud mezi E a C)
- konektor (sběrač nosičů náboje)
- Vyrábí se v polaritách NPN a PNP dle vodivosti jednotlivých elektrod
	![[Pasted image 20250928155144.png]] ![[Pasted image 20250928155237.png]]
### Technické provedení BJT
![[Pasted image 20250928155306.png]]
### Tranzistor NPN v otevřeném (vodivém) stavu
![[Pasted image 20250928155357.png]]
### MOSFET
**MOSFET** (Metal-Oxide-Semiconductor Field-Effect Transistors)
- Proud v kanálu je veden jen jedním typem nosičů (elektrony v N-kanálových, díry v P-kanálových).
- Mají velmi vysoký vstupní odpor (prakticky žádný vstupní proud přes G).
- Rychlé spínání a nízké ztráty.
- Skvělé pro digitální obvody, spínané zdroje, procesory, paměti.
![[Pasted image 20250928161226.png]]
### Podobnost s BJT
- U **BJT** je hlavní rozdíl v tom, že proud je řízen **malým proudem v bázi** a nosiče (elektrony nebo díry) procházejí přes bázi do kolektoru.
- U **MOSFETu** se proud řídí **napětím na gate** a nosiče vznikají až v kanálu pod gate (elektrickým polem).
### Typické tranzistorové počítače
- 50. - 60. léta
- Tranzistory (BJT) místo elektronek
- menší rozměry
- nižší spotřeba
- vyšší spolehlivost
Typické příklady:
- IBM 1401 (1959) – komerční úspěch, využití v byznysu
- IBM 7090 – vědecké výpočty, nástupce IBM 709 (elektronkový)
- CDC 1604 (Control Data Corporation) – jeden z prvních tranzistorových superpočítačů
### Význam 2. generace
- otevřely cestu k širšímu nasazení počítačů
- začátek éry komerčního využití výpočetní techniky
## 3. generace (60. léta – 70. léta)
Výhody:
- další miniaturizace a zlenění
- vyšší spolehlivost oproti tranzistorům
- možnost multitaskingu a vyšších programovacích jazyků
Typické příklady:
- **IBM System/360** (1964) – univerzální architektura, kompatibilita napříč modely
- DEC PDP-8 a PDP-11 – minipočítače, dostupné menším firmám a univerzitám
- Honeywell 6000 Series – konkurenční řada k IBM, používaná v průmyslu
Význam 3. generace
- rozšíření počítačů do univerzit a firem
- standardizace architektur
- příprava půdy pro vznik osobních počítačů
![[Pasted image 20250928162420.png]]
## 4. generace (70. léta – současnost)
- Hlavní prvek: **Mikroprocesory (VLSI – MOSFET)**
- Milióny až miliardy tranzistorů na čipu
- Osobní počítače, mobilní zařízení, internet
Výhody:
- integrace milionů až miliard tranzistorů na jediný čip
- masová výroba → nízká cena a dostupnost
- vysoký výkon, malá spotřeba a mobilita

Typické příklady:
- **Intel 4004** (1971) – první komerční mikroprocesor
- IBM PC (1981) – začátek éry osobních počítačů
- Apple Macintosh (1984) – grafické rozhraní pro běžné uživatele
- moderní procesory (Intel Core, AMD Ryzen, ARM, Apple Silicon)
### Význam 4. generace
- rozšíření všude do komerce, veřejné správy i domů (i do kapsy)
- použití na práci i zábavu (první hry)
- v 70.-80. letech éra 8bitových mikropočítačů
### Současnost a budoucnost
- počítače pro širokou veřejnost (PC, notebooky, smartphony)
- základy digitální společnosti a internetu
- vývoj směrem k **paralelismu**, **GPU** a specializovaným čipům (AI, ML)
- úplně nové technologie (**kvantové**)