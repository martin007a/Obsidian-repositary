---
tags: [IoT, zkouska, internet_veci, skripta]
aliases: [Okruhy ke zkoušce IoT]
---
### 1. Trendy digitalizace a řízení, automatizace a sítě kolem nás
Digitalizace v dnešním pojetí neznamená jen prosté přepisování papírových dokumentů do počítače. Jedná se o komplexní proces, při kterém se celé fyzické a provozní činnosti převádějí do digitálních modelů, čímž se podnikání stává rychlejším a efektivnějším. Cílem Internetu věcí (IoT) je propojení fyzických věcí s internetem, kde jsou elektronická zařízení schopna sbírat, vyměňovat a analyzovat data pro automatizaci a vzdálené řízení.
**Klíčové pojmy a technologie, které tento trend umožňují:**
- **Cloud Computing:** Služby poskytující výpočetní zdroje, datové úložiště a softwarové služby přes internet na vzdálených serverech.
- **AI a strojové učení:** Vytváření systémů zastupujících lidskou inteligenci; strojové učení umožňuje počítačům učit se na základě dat a zkušeností.
- **Big Data:** Zpracování a analýza velkého objemu dat z různých zdrojů k získání cenných poznatků a vzorců chování.
- **Kybernetická bezpečnost:** Zásadní oblast chránící stále propojenější systémy před neoprávněnými přístupy a hrozbami.
Tento obor historicky vychází ze dvou technologií: **Telemetrie** (měření veličin na dálku, např. systém HDO zapínající bojlery přes elektrické dráty) a **Telematiky** (sledování aut a vlaků v logistice). V současnosti tyto trendy vrcholí v automatizaci budov (tzv. Smart Home), kde nejvyšším stupněm je úroveň 4 – "pozorný domov". Ten se sám aktivně učí zvyky obyvatel (ráno sám rozhrne žaluzie a spustí kávovar). Technologickým pilířem je **konvergence sítí** – dřívější oddělené kabely pro TV, telefon a počítač se spojily do jediné sítě na bázi TCP/IP. Vzniká tak koncept **IoE (Internet of Everything)**, který integruje lidi, data, procesy a fyzické věci.
### 2. Průmyslové revoluce z pohledu kybernetiky a řízení
Historii průmyslu dělíme do 4 revolučních fází:
1. **1. průmyslová revoluce (18.–19. stol.):** Mechanizace poháněná vodou a párou. Přinesla masovou produkci a mechanické řízení bez inteligence.
2. **2. průmyslová revoluce (19.–20. stol.):** Elektrifikace, ropný průmysl a pásová výroba (tzv. fordisismus) s jednoduchou reléovou logikou.
3. **3. průmyslová revoluce (pol. 20. stol.):** Zásadní zlom s nástupem IT, prvních PLC automatů a robotů. Vznikají ASŘ (Automatizované systémy řízení), které byly sice automatické, ale vysoce rigidní (nepružné) a centralizované (stroj uměl jen jednu pevně naprogramovanou činnost).
4. **4. průmyslová revoluce (Průmysl 4.0):** Současný stav zaměřený na digitální transformaci. Staví na CPS (Kyberneticko-fyzikálních systémech), kde jsou stroje a produkty připojeny k internetu věcí a flexibilně komunikují v reálném čase.
Z pohledu kybernetiky (vědy o řízení, definované N. Wienerem) fungují systémy na principu **zpětné vazby (feedback loop)**. Ta se skládá ze 3 kroků:
- **Senzorický podsystém:** Změří aktuální stav (např. pokles teploty na 15 °C).
- **Řídicí podsystém (Controller):** Porovná data s cílem (např. chceme 22 °C), provede analýzu a vygeneruje povel k optimalizaci.
- **Akční podsystém (Aktuátor):** Provede fyzickou změnu (sepne kotel). Smyčka se tím uzavírá a neustále se opakuje.
- **Příklad z praxe (Zemědělství 4.0):** Krávám se do žaludku zavádí senzory (bolusy) měřící teplotu a pH. Cloud výkyv vyhodnotí jako nemoc a pošle farmáři SMS pro brzkou izolaci dříve, než se objeví příznaky.
### 3. Přehled problematiky IoT, kořeny IoT a další rozvoj
Myšlenky na propojení přes internet sahají do 90. let. Pojem "Internet of Things" poprvé použil v roce 1999 výzkumník Kevin Ashton (MIT) pro kosmetickou firmu Procter & Gamble. Uvědomil si, že počítače byly "slepé a hluché" závislé jen na datech od lidí. Zavedl tak vizi dát jim vlastní smysly (senzory a čipy).
- **Příklad P&G:** Na rtěnky se nalepil RFID čip a chytrý regál si sám spočítal a doobjednal chybějící zboží bez inventury prodavačkou.
Základním principem je sběr dat a D2D (Device-to-Device) komunikace bez člověka. K masivnímu rozvoji bylo nutné vyřešit kritický technický problém: starý protokol IPv4 (4,3 miliardy adres) přestal stačit. Zásadní tak byl **přechod na IPv6** s prostorem $2^{128}$ adres, schopným připojit každý atom. Budoucnost IoT obrovsky ovlivní rozšíření 5G sítí (rychlejší připojení) a rozvoj AI v analýze dat, zatímco největší výzvou zůstává kyberbezpečnost.
### 4. Porovnání struktury IoT (4. PR) a struktury ASŘ (3. PR)
Zde se zásadně mění tvar a chování řídicí architektury.
**Struktura ASŘ (3. PR):** Definována modelem CIM (Computer Integrated Manufacturing), tvoří přísnou, nepropustnou pyramidu shora dolů.
1. Technologická vrstva (senzory, motory, PLC).
2. Procesní vrstva (SCADA dispečinky).
3. Výrobní vrstva (MES pro rozvrhování).
4. Podniková vrstva (ERP účetnictví a prodej). Komunikace je zdlouhavá a centrálně dirigovaná.
**Struktura IoT (4. PR):** Opouští pyramidu a využívá trojrozměrný Referenční model RAMI 4.0. Umožňuje plně decentralizovanou komunikaci – senzor může svá data poslat rovnou do cloudového ERP systému přes internet, aniž by musel projít všemi vrstvami. Skládá se ze zařízení, sítí, cloudových služeb a aplikací.
**Klíčový rozdíl – Smart Product (Inteligentní výrobek):** Ve staré pyramidě byl kus plechu pasivní. V IoT má polotovar paměťový modul, sám přijede k lakovacímu robotovi a naváže komunikaci: "Jsem speciální zakázka, nalakuj mě na modro"

| **Vlastnost**      | **ASŘ (3. PR)**                       | **IoT (4. PR)**                              |
| ------------------ | ------------------------------------- | -------------------------------------------- |
| **Cíl**            | Automatizace průmyslového procesu     | Propojení fyzických zařízení přes internet   |
| **Architektura**   | Hierarchická, uzavřená (CIM pyramida) | Decentralizovaná, otevřená (RAMI 4.0)        |
| **Komunikace**     | Tradiční protokoly (Modbus, Profibus) | Moderní protokoly (MQTT, OPC UA, HTTP, CoAP) |
| **Flexibilita**    | Nízká – pevně dané funkce             | Vysoká – snadná rozšířitelnost               |
| **Zpracování dat** | Lokální, centrální                    | Lokální i vzdálené v cloudu                  |

### 5. Signály, jejich typy, vzorkování a kvantování
Počítače v IoT fyzikálním veličinám nerozumí, potřebují A/D (analogově-digitální) převodník. Proces má tyto fáze:
1. **Analogový signál:** Přirozený stav z přírody, který nabývá libovolných hodnot. Je spojitý (plynulý) v čase i v amplitudě.
2. **Vzorkovaný signál (Diskrétní v čase):** Plynulá křivka se rozseká v časových intervalech (v Hz). Musí být dodržen **Shannon-Kotělnikovův teorém**: Vzorkovací frekvence musí být minimálně dvakrát větší, než je nejrychlejší kmitání měřeného signálu ($f_{v} \ge 2 \cdot f_{max}$).
3. **Kvantovaný signál (Diskrétní v amplitudě):** Hardwarový čip naměřené napětí zaokrouhlí na předpřipravené "schůdky" (bity). Tímto zaokrouhlením vzniká kvantizační chyba (šum).
4. **Číslicový (digitální) signál:** Výsledné binární nuly a jedničky (0/1).
- **Zajímavost (Audio CD):** Lidské ucho slyší 20 kHz. CD se tedy vzorkuje minimálně dvakrát rychleji na 44,1 kHz. Kvantuje se jemně na 16 bitů (65 536 schůdků), čímž je kvantizační chyba lidským uchem neznatelná (0,0015 %).
### 6. Senzory a senzorové klastry v IoT
- **Senzor (Primitivum 1):** Základ systému, který převádí fyzikální svět na elektrický signál. Posuzují se podle metrologických parametrů:
    - **Rozsah (Range):** Od jaké do jaké hodnoty spolehlivě měří.
    - **Rozlišení (Resolution):** Nejmenší možná zaznamenatelná změna (např. $0.1^{\circ}C$).
    - **Přesnost (Accuracy):** Jak moc se naměřená hodnota blíží absolutní fyzikální skutečnosti.
    - **Hystereze:** Setrvačnost senzoru (odlišná hodnota při zahřívání vs. ochlazování).
- **Senzorové klastry (WSN):** Skupiny bezdrátově propojených senzorů pro získání komplexnějších dat z většího prostoru.
- **Fúze dat:** Hlavní důvod tvorby klastrů. Znamená spojení dat z různých senzorů dohromady (např. akcelerometr a gyroskop v mobilu pro přesný 3D pohyb). Moderní dron využívá multisenzorovou hlavu (optika, termokamera, lidar) k tvorbě map vlhkosti polí z fúze dat.
### 7. IoT agregátory a Fog Computing
- **Agregátor (Primitivum 2):** Lokální mikrokontrolér (Raspberry Pi, Arduino, PLC), který fyzicky přebírá data od senzorů. Centralizuje je, z velkého objemu filtruje informační šum a překládá komunikační protokoly do sítě.
- **Problém Cloudu:** Původní myšlenka posílat všechna surová data na vzdálený Cloud narazila na technické překážky: Latence (zpoždění – letící dron nebo robot by nezastavil a naboural), úzká Šířka pásma a Bezpečnost/Dostupnost (výpadek Wi-Fi odstaví továrnu).
- **Fog / Edge Computing:** Řeší tyto problémy stažením inteligence z cloudu na okraj sítě (Edge) k agregátoru. Výpočet se provede lokálně – spotřebič zjistí přehřátí a vypne se sám bez odesílání dat do cloudu. Do sítě pak pošle jen občasnou malou zprávu, což eliminuje latenci i vytížení sítě. Například drony počítají překážky pro vyhýbání zcela lokálně na vlastních palubních počítačích.
### 8. Komunikační kanály v IoT, funkce, standardy
Pro přenos dat slouží **Primitivum 3 – Komunikační kanál**. Na rozdíl od běžného webu se v IoT dělá kompromis mezi _dosahem signálu_, _množstvím dat_ a _spotřebou energie_.
- **Drátové:** Ethernet, RS-485 (protokol pro sériovou průmyslovou komunikaci, odolný vůči rušení).
- **Mobilní sítě:** GSM (hlas a data), 4G LTE, 5G (vysoká rychlost a kapacita, nízká odezva).
- **Sítě krátkého dosahu (PAN/LAN):** Wi-Fi, Bluetooth, Zigbee (úsporný mesh protokol), Z-wave (chytré domácnosti). Mají velkou rychlost, ale dosah jen desítky metrů a rychleji vybíjejí baterie.
- **Sítě dlouhého dosahu (LPWAN):** Vytvořené čistě pro IoT (LoRaWAN, Sigfox, NB-IoT). Dosah i 20 km, extrémně nízká spotřeba energie (senzor na baterii vydrží roky), ale přenesou jen velmi omezené množství dat.
- **Protokoly v softwaru:** Standardem je **MQTT** – lehký a efektivní protokol pracující na principu Vydavatel/Odběratel (Publish/Subscribe) přes uzlového Brokera, ideální pro úspornou komunikaci. Dále se využívá CoAP a klasické HTTP.
### 9. IoT a eUtility, zpětná vazba a Decision trigger
- **eUtility (Primitivum 4):** Silné výpočetní servery, cloudová datová centra nebo velké systémy ERP (řízení podniku). Data se zde trvale ukládají a optimalizují prostřednictvím analytiky nebo umělé inteligence. Skládají se z Cloudové platformy (analýza), Databáze (historie), Ovládacího centra a Mobilních aplikací (notifikace uživateli).
- **Decision trigger (rozhodovací spouštěč):** Softwarový algoritmus (kus kódu), který neustále vyhodnocuje přijatá data a na základě pravidel autonomně rozhodne o akci (aniž by člověk mačkal tlačítko). Dává podněty k optimalizaci a údržbě.
- **Zpětná vazba:** Umožňuje reakci na aktuální stav přes kybernetickou smyčku:
    1. Spouštěč zjistí, že je v pěstírně sucho, a vydá povel k zavlažování.
    2. Akční člen (aktuátor) zapne vodu a změní prostředí.
    3. Senzor měří nový stav vlhkosti a posílá nová data zpět.
    4. eUtilita přijme data a Decision trigger vodu opět vypne. (Praxe: Dron rozpozná plevel AI algoritmem a Trigger zcela sám pošle autonomnímu traktoru GPS přesně tam, kde má aplikovat herbicid).
### 10. Koncept IoT z pohledu vymezení OT a IT
Průmysl 4.0 a IoT propojují dva přísně oddělené světy.
	• OT – **Operační technologie**, zaměřuje se na technologie a systémy pro automatizaci fyzických operací. Využívají se senzory, kontrolní systémy a další technologie na sběr dat, řízení a monitorování. Zahrnují: průmyslovou automatizaci, energetiku, výrobu, dopravu, PLC (Programovatelný logický automat) • IT – **Informační technologie**, zaměřují se na datové centra, sítě, software… Specificky na sběr, analýzu, zpracování a distribuci dat a informací. Také na správu sítí, databází… 
	• Vymezení OT a IT v IoT – vzájemně se propojují a spolupracují, OT sbírá data a řídí fyzické operace, IT zajišťuje správu a analýzu těchto dat.
- **Konvergence a kyberbezpečnost:** Dříve tyto světy izolovalo tzv. Air Gap (vzduchová mezera) – výrobní stroje nebyly připojeny k internetu. IoT tento Air Gap prolamuje, nutí OT data posílat do IT cloudu kvůli analytice, což vystavuje staré stroje bez antivirů vůbec poprvé kybernetickým hrozbám.
### 11. Výhody a nevýhody OPC UA a MQTT v IoT
Tyto dva komunikační protokoly slouží k výměně dat mezi zařízeními, každý se ale hodí na něco jiného.
- **Protokol MQTT:** Velmi lehký a jednoduchý protokol fungující přes Brokera s minimální režií.
    - _Výhody:_ Extrémně datově nenáročný (šetří šířku pásma), spolehlivý i na špatných sítích (senzory na poli) a má nízkou spotřebu energie.
    - _Nevýhody:_ Přenáší pouze raw data ("holý text"). Neřeší strukturu – systém nepozná, zda jde o Celsius či Fahrenheit. Má omezenou škálovatelnost.
- **Protokol OPC UA:** Aktuální zlatý standard a komplexní moderní architektura pro Průmysl 4.0.
    - _Výhody:_ Je univerzální, nezávislý na platformě (Windows, Linux, Cloud), a především řeší sémantiku a rozšířená metadata. Nepošle jen číslo "22", ale strukturovaný balíček ("22 °C, čidlo 5, robot KUKA"). Má zabudovanou velmi silnou kybernetickou bezpečnost (šifrování).
    - _Nevýhody:_ Je to "těžký" a komplexní protokol náročný na výpočetní výkon, paměť i datovou propustnost, který se nehodí pro bateriové levné čipy.
### 12. Průmyslový internet věcí (IIoT)
Rozdíl mezi běžným spotřebitelským IoT a IIoT (Industrial Internet of Things) je propastný. U běžného IoT (chytré hodinky, ledničky) výpadek internetu nezpůsobí tragédii. IIoT představuje implementaci do kritické infrastruktury, propojující průmyslová zařízení, senzory a systémy např. v chemických továrnách či elektrárnách.
**Zásadní požadavky a rozdíly IIoT:**
- **Kritičnost a Safety:** Jakékoliv selhání ohrožuje lidské životy (výbuch) nebo nese obří finanční ztráty. Kybernetická bezpečnost vyžaduje autentizaci a šifrování.
- **Extrémní podmínky:** Hardware musí odolávat silným vibracím, žáru, prachu a agresivním chemikáliím.
- **Životnost:** Zařízení se do linek instalují s očekáváním spolehlivého chodu 15 až 20 let (oproti 3 letům u telefonu).
- **Výsledek:** Integrací s AI a Big Data zavádí prediktivní údržbu – stroj dokáže analyzovat vzorce, předpovídat chování a nahlásit budoucí poruchu dříve, než se skutečně rozbije.
### 13. Architektura IIoT – model IIRA a RRI&IoT
Pro bezproblémové globální fungování IIoT strojů od různých výrobců vznikly standardizované architektury, dominují zejména americký a evropský/asijský přístup.
- **Americký model IIRA (Industrial Internet Reference Architecture):** Vyvinutý konsorciem IIC (GE, AT&T, IBM). Je zaměřený softwarově a byznysově. Chce harmonizovat OT a IT systémy a dělí architekturu do 4 vrstev (Viewpoints):
    1. Business (Ekonomický smysl a návratnost investic).
    2. Usage (Uživatelské reálné použití).
    3. Functional/Information (Softwarové moduly, analýza dat).
    4. Implementation/Technology (Fyzické zapojení a servery).
- **Evropské a japonské modely:** Jsou historicky orientovány přímo na výrobní linky a hardware (Německo je strojírenská velmoc). Patří sem koncept **RRI&IoT (Robot Revolution Initiative)** z Japonska, který klade důraz na Real-time procesy, rychlou odezvu, minimalizaci latence a využití AI v reálném čase. V praxi se modely IIRA a např. evropské RAMI doplňují (IIRA řeší IT a byznys, RAMI reálné OT stroje).
### 14. Model architektury I4.0 – RAMI 4.0 a digitalizace
Německým standardem pro digitalizaci (převod fyzického světa do virtuálního) je model **RAMI 4.0**. Tento model opouští starou 2D pyramidu a tvoří komplexní 3D matici umožňující propojování od systémů až po cloud.
**Skládá se ze tří os:**
1. **Osa hierarchie (Hierarchy Levels):** Popisuje fyzický svět zespodu nahoru – Výrobek, Stroj (Control Device), Hala (Station) a Propojený svět (Connected World).
2. **Osa životního cyklu (Life Cycle):** Převratná novinka. Sleduje produkt celým životem: Fáze "Type" (vývoj a prototypování) a Fáze "Instance" (reálná výroba a servis).
3. **Osa vrstev (Layers):** Tvoří od fyzického "Assetu" dole, přes komunikaci (Business, Function, Information, Communication), model nahoru.
**Digitální dvojče (Digital Twin):** Výsledkem modelu RAMI je, že pro fyzický motor dole existuje na 100 % identický virtuální odraz v datech. Automobilka už nestaví linku systémem "pokus-omyl"; vše se virtuálně postaví a nasimuluje v PC, a teprve, když si roboti nepřekážejí, se začne stavět fyzicky, což ušetří obrovské finance.
### 15. Logistika věcí (Supply chain), automatická identifikace (AutoID)
- **Supply Chain (Logistika věcí):** Obrovská síť toku materiálů a informací od těžby železné rudy přes dodavatele, nákup a montáž až po doručení k zákazníkovi domů. Cílem je zajištění správného zboží ve správný čas; IoT zaznamenává polohu přes GPS a monitoruje teplotu.
- **AutoID (Automatická identifikace):** Odstraňuje pomalého a chybujícího skladníka s tužkou. Technologie automaticky, strojově sbírá a čte data. Patří sem: Čárové a QR kódy, RFID čipy, Biometrie a OCR kamery (čtení SPZ).
- **Traceability (Sledovatelnost):** Hlavním cílem logistiky. V potravinářství lze díky AutoID zkažené maso v supermarketu do vteřiny zpětně vytrasovat ke konkrétnímu kamionu, jatkám i přesné krávě na farmě.
### 16. Značení věcí, čárové a QR kódy, GS1
Pro automatickou identifikaci v dodavatelském řetězci používáme nejčastěji tištěné kódy.
- **1D kódy (Lineární čárové kódy):** Kódy typu EAN přečtené laserem. Mají velmi malou kapacitu – zakódují do sebe v podstatě jen jedno identifikační číslo (ID), nenese to cenu ani název. Systém si vše musí dohledat v databázi pokladny.
- **2D kódy (QR kódy, DataMatrix):** Čtvercové matice s obrovskou kapacitou. Ke čtení se užívá kamera a software. Unesou odstavce textu, datum spotřeby, URL i šarži. Výhodou je matematická samoopravitelnost – kamera přečte kód bezchybně i zčásti utržený či zašpiněný.
- **Systém GS1:** Aby kód českého mléka neznačil v Číně televizi, globální organizace GS1 zajišťuje mezinárodní standardy (GTIN, SSCC, GLN). Čísla přiděluje tak, aby byl kód unikátní pro celou planetu a logistický řetězec.
### 17. Typy elektromagnetického záření, frekvenční pásma v AutoID
Při přechodu na RFID se už nepoužívá k identifikaci optický laser (pro IrDA a kódy z infračerveného spektra), ale rádiové elektromagnetické vlny. Jsou striktně odděleny do pásem. Fyzika zní: čím vyšší frekvence, tím dál signál doletí, ale tím hůř prostupuje překážkami.
1. **LF (Low Frequency - Nízkofrekvenční):** 125–134 kHz. Dosáhne jen na centimetry, ale bez problémů prostupuje lidskou tkání i vodou. Použití: čipování domácích zvířat a přístupové "pípáky" k otevírání dveří.
2. **HF (High Frequency - Vysokofrekvenční):** 13,56 MHz. Dosah je pár centimetrů, avšak přináší výhodu v bezpečnosti. Leží zde standard NFC. Použití: bezkontaktní platby terminálem, jízdenky a elektronické pasy.
3. **UHF (Ultra High Frequency):** V EU 868 MHz (850-960 MHz). Páteř logistiky s dosahem 5 až 10 metrů. Čtečka je na stropě a čte pohyb palet, kartonů i průjezd aut přes závory. (Sítě jako Bluetooth využívají frekvenci 2,4 GHz pro komunikaci na 1–100 metrů).
### 18. Materiály a rušivé zdroje z pohledu el-mag signálů
Fyzika se nedá oklamat – materiály, stojící v cestě UHF signálům, útlum zásadně ovlivňují.
1. **Prostupné (Transparentní):** Plast, papír, karton. Rádiová vlna jimi jednoduše projde – čip v krabici přečtete přes stěnu krabice bez problému.
2. **Absorpční (Pohlcující):** Voda, beton, tlusté zdi. Pohlcují elektromagnetické vlny (molekuly vody je sežerou a přemění na teplo). Čip za člověkem degraduje v dosahu z 10 metrů na centimetry.
3. **Odrazivé (Reflexní):** Kovy. Tvoří dokonalé zrcadlo a vlnu odrazí zpět, čímž způsobují vícenásobné cesty, tzv. Multipath efekt, který čtečku a signál oslepí.
- **Praxe z pivovarů:** Ocelový sud plný vody by RFID běžným čipem zcela oslepil. Používají se proto tlusté "Metal-mount" tagy, které mají distanční pěnovou vložku oddalující čip od kovu. V továrnách navíc ruší i neviditelné zdroje (tzv. EMI rušení), jako jsou obrovské elektromotory či zářivky, proti kterým se využívá stíněných ethernet kabelů v rámci ochrany EMC.
### 19. Struktura a komponenty RFID systému
RFID systém není "pouhý čip", ale systém sestávající ze čtyř stavebních prvků:
1. **Tag (Transpondér):** Nálepka nebo pouzdro připevněné k objektu. Ukládá data do paměti a pomocí své miniaturní antény reaguje na čtečku.
2. **Anténa:** Vysílá generované elektromagnetické vlny do prostoru a chytá odrazy zpět od tagů.
3. **Reader (Čtečka / Řídicí jednotka):** Mozek systému (stojací brána nebo ruční pistole). Řídí anténu, posílá jí energii a digitalizuje přijaté rádiové signály na nuly a jedničky.
4. **Middleware (Software):** Čtečka sejme 500 palet za vteřinu, což by ERP systém zahltilo. Middleware sedí mezi nimi a data vyfiltruje. Maže duplicity a odešle jen pročištěnou informaci ("Paleta XY dorazila").
### 20. Aktivní a pasivní tagy, transpondéry
Rozlišujeme je primárně podle způsobu zisku energie.
- **Pasivní tagy:** Jsou nejběžnější a nejlevnější (nálepky v obchodě). Nemají vlastní baterii. Jsou "mrtvé" do chvíle, dokud čtečka nevyšle rádiovou vlnu; tu anténa z tagu chytí, vyrobí drobný proud k probuzení čipu a odrazí zpět data. Mají mnohem kratší dosah (centimetry až pár metrů), ale vydrží bezúdržbově desetiletí.
- **Aktivní tagy:** Větší, s vlastní baterií. Své rádiové signály generují aktivně a neustále křičí do okolí "Tady jsem!". Mají masivní dosah i na stovky metrů a spolehlivou komunikaci; ideální pro námořní kontejnery a drahou techniku v logistice.
- (Samotný termín Transpondér pak znamená jakékoliv chytré elektronické zařízení – jako je právě RFID tag –, jež automaticky na nějaký signál přijme a odešle adekvátní zpětnou odpověď bez asistence člověka).
### 21. Principy komunikace FFC a NFC
Tyto komunikační technologie se dělí podle toho, s jakou zónou – blízkou, nebo dalekou – pracují.
- **NFC (Near Field Communication):** Zóna blízkého pole (na pár centimetrů) pro nízké (LF) a vysoké frekvence (HF). Vůbec nevyužívá šíření vln prostorem; principem je **magnetická indukce** (funguje jako transformátor). Anténa čtečky (aktivní cívka) vytvoří magnetické pole a tag (např. mobil u platby) energii pro předání dat nasaje. Může mít pasivní (karta) i aktivní režim (dva telefony vysílající vzájemně).
- **FFC (Far Field Communication):** Zóna dalekého pole. Operuje s UHF vlnami s dosahem až do deseti metrů. Zde nedochází k indukci; vzduchem letí skutečná elektromagnetická rádiová vlna. Ta narazí do RFID tagu, tag vlnu zdeformuje a pošle tzv. **zpětný odraz (Backscatter)** do čtečky.
### 22. EPC, standardy a systémy AutoID, EPCIS
Pokud využíváme UHF RFID v řetězci, starý kód EAN nepostačuje – zná jen "To je plechovka Coly", nerozezná, která konkrétní ze 100 to je.
- **EPC (Electronic Product Code):** Nový standard. Je to dlouhé číslo pro UHF tagy, absolutně unikátní pro každičký jednotlivý specifický kus zboží na světě. Standardy rozvíjí globální organizace **EPC Global**.
- **EPCIS (EPC Information Services):** Když RFID čtečky vygenerují obrovská data pohybu, všechno se propojí v EPCIS – standardizované sdílené databázi. To umožňuje dokonalou sledovatelnost a transparentnost (Traceability).

| **Událost (Event)** | **Popis v EPCIS databázi**                                         |
| ------------------- | ------------------------------------------------------------------ |
| **Create**          | Výrobce vytvořil krabici a zaznamenal do ní unikátní EPC.          |
| **Ship**            | Zboží opustilo sklad – EPCIS uloží událost jako odeslanou.         |
| **Receive**         | Distributor krabici přijal a přečetl – zaznamenáno.                |
| **Cold chain**      | Napojený senzor během logistiky potvrdí, že teplota se nezhoršila. |
### 23. IoT ve Smart City a eHealth
IoT přímo zlepšuje komfort měst a efektivitu zdravotnictví. Ve Smart City monitorují klastry infrastrukturu k hospodárnosti, v eHealth pomáhají dálkově pečovat.
**Smart City z pohledu řešení:**
- **Odpady:** Popelnice vybavené ultrazvukem hlásí svou hladinu přes LPWAN síť a přivolají popeláře výhradně na plný koš.
- **Doprava a Parkování:** Senzory v asfaltu detekují auta, přesměrují MHD i navedou řidiče na volné místo v mobilní aplikaci.
- **Energie a Osvětlení:** Lampy snižují spotřebu energie ztlumením, rozsvítí se pouze v přítomnosti občana.
- Dále sítě s čidly zvládají diagnostiku úniků vody či míru škodlivin z ovzduší.
**eHealth z pohledu řešení:**
- **Domácí péče (Wearables):** Chytré hodinky a náramky v reálném čase snímají tep či krevní tlak. Data jdou agregátorem do cloudové eUtility k doktorovi (Telemedicína).
- **Senior monitoring:** IoT dokáže zjistit nepřítomnost pohybu nebo tvrdý pád pacienta. Bez lidského zásahu okamžitě přes "Decision trigger" automaticky zavolá sanitku a udrží tím klidný pobyt mimo nemocnici se zajištěním dohledu.
- Do systému patří i chytré dávkovače léků a celková AI analytika ohrožení pacienta.
### 24. Aplikace IoT v Car sharing a Smart grid
- **Car sharing (Sdílení aut):** Staré půjčovny s papírováním zmizely. Auta obsahují "on-board" hardware s GPS modulem pro polohu, GSM síť, senzory nárazu a bezkontaktní chytré zámky NFC/Bluetooth. Uživatel z mobilní aplikace auto vyhledá, autorizuje požadavek v Cloudu, odemkne vůz, a jakmile dojede, systém zcela sám propočítá trasu, stav paliva i platbu z účtu.
- **Smart grid (Chytré energetické sítě):** Klasická síť rozesílala proud jen od elektrárny ke spotřebiteli. Jenže majitelé domů osazených solárními panely se stali i výrobci (tzv. Prosumeři – Producer a Consumer), což starou síť ničí a vrací nestabilitu do obousměrného toku. Smart Grid využívá sítě chytrých elektroměrů a senzorů k masivní prediktivní analýze a distribuci – systém vidí přebytky výkonu ze střech, inteligentně ošetřuje výpadky poruch a sám dokáže automaticky vyvážit optimální nabíjení vozidel (elektromobilů).
### 25. EMC – elektromagnetická kompatibilita, odolnost a rušivé zdroje
Množství elektroniky vyžaduje dodržování standardu EMC – schopnosti zařízení spolehlivě fungovat tak, aby samo nevytvářelo nesnesitelný šum, ani jím nebylo narušeno (např. běžící mixér nesmí způsobit zrnění staré televize). Splnění normy je zákonnou podmínkou pro uvedení produktu na trh.
1. **Rušivé zdroje (EMI / Emise):** Nežádoucí signál přístrojů putující do prostoru. Nejkritičtějšími rušičkami v továrně jsou obří elektromotory, svářečky, frekvenční měniče a spínací zdroje s blikající zářivkou.
2. **Odolnost proti rušení (EMS / Imunita):** Senzory v IoT a linky se musí osadit prvotřídními stíněnými plechovými kryty a uzemněnými filtrovanými kabely, aby tuto industriální zátěžovou palbu šumu vydržely.
### 26. Rozpětí EMC, meze rušení a vyzařování
Mezinárodní normy definují meze rušení, za kterých prostředí zůstane pod kontrolou (v Evropě zakončeno certifikací CE). Testy EMC probíhají obousměrně:
1. **Měření vyzařování (Emissions):** Nový senzor uzavřou do speciální bezodrazové měřicí komory. Pomocí citlivých přijímacích antén prověří, že produkt nepouští do prostoru zbytečné vlny s nežádoucí silou, případně nešumí zpátky po uzemněném kabelu tak moc, že překročí povolenou normu (např. v decibelech).
2. **Měření odolnosti (Immunity):** Následně obrátí zbraň. Produkt se silně ozařuje radiovými vlnami a uměle probíjí silnými elektrostatickými jiskrami s blesky. Pakliže hardware nezhasne, a ani systém nevytuhne při přenosu zpráv, úspěšně u zkoušky prodeje obstál.
### 27. Vlivy prostředí na útlum el-mag signálu, význam jednotek dB, dBm, dBi
Senzor je instalován u brány. Cestující vysílaný rádiový výkon však s délkou vadne. Signál zachvacuje **útlum**, který vzniká jednak zvětšující se vzdáleností šíření, ale i odražením či nárazem do vody, stěn stavení či interference vlhkosti na dešti (Multipath). Běžné stovky Wattů propadnou zlomkům nuly. Místo mnohaciferných výpočtů se používají **logaritmické jednotky** o snazších matematických součtech pro inženýry.
- **dB (Decibel):** Udává pouhý poměr zisku a ztrát (je bezrozměrný). Signál se snížením o "-3 dB" tak naprosto exaktně ztratí právě ideální polovinu sil.
- **dBm (Decibel-milliwatt):** Měří přímo fixní absolutní výkon, kdy se vztahuje jako báze srovnání na referenční nulu o velikosti energie 1 mW (vhodné pro mobilní telefon a citlivost v -80 dBm).
- **dBi (Decibel-izotropní):** Parametr konstrukce zisku u antény udávající, v jak dokonalém měřítku směřovaný prvek signál do terče nahušťuje proti naprosto rovnoměrně plošně zářící ideální fiktivní "všesměrové izotropní anténě".
### 28. Kyberneticko-fyzikální systémy (CPS) a principy kolaborace
Ve 4. průmyslové revoluci nevévodí pasivní stroje nýbrž silné CPS systémy propojující fyzický svět s digitálním mozkem. CPS je tvořen reálným připojeným přístrojem, softwarovým řízením a hlavně trvalým zrcadlovým AI obrazem nahoře na webu jako Digitální dvojče (což dovoluje naprostou synchronizaci informovanosti).
**Vzájemná závislost a distribuované rozhodování:** Složky mají přímou provázanost. V minulé éře musel poruchu na výrobním opasku přenastavit a vyřešit stopnutím centrální lidský operátor. V Průmyslu 4.0 řeší CPS agendu s metodou přímé síťové decentralizace M2M (Machine to Machine) pro vzájemnou efektivní Kolaboraci napřímo. Zjistí-li linkový stroj závadu na vlastním ložisku rotoru, síťovým oknem pošle informativní hlášení přímo všem následným opaskovým strojům ve výrobě. Obdržené upozornění ("zpomaluji proces") automatizovaně a s naprostou elegancí odstartuje balanční rekonfiguraci napříč celou linkou – aniž by člověk sahal na ovládání a celková fabrika jakkoliv kolabovala či zastavila chod.
### 29. Agent a multiagentní systémy, autonomní systémy
Autonomní rozhodování z okruhu 28. řídí zóna "Softwarových Agentů" postavených na systému MAS.
- **Agent a autonomie:** Oproti dřívějšímu "pasivnímu" programu (ten je spuštěn mačkáním člověka), představuje Agent softwarového či vizuálního průmyslového robota s mozkem s určitým logickým zacílením (i jako dron, algoritmus a vyhledávač). Má vlastnosti autonomie, reaktivity (vnímající okolí senzory) a silné proaktivity, což mu dává instinkt ke splnění určeného cíle nejlepším stylem (např. postavit levně) bez asistence dohledu pro řízení auta.
- **Multi-agentní systémy (MAS):** Tímto termínem označujeme mraveniště plné spolupracujících entit agentů a to buď pro montáž nebo sborové kooperace harvestorů u lánu obilí. Agentem však není zprostředkován exkluzivně svářeč robota, ale zastupuje i vrtačku či neúplný svařovaný Produkt.
    - **Klíčové vyjednávání v Aukci:** Fabrika MAS je geniálně efektivní. Rám vyráběného automobilu (identifikovaný Agent) sjede z pásu a rozezná úkol upnout a namontovat kola. Namísto pasivního naprogramování na pevnou dráhu k jedné pozici vypíše rám bez zaváhání napříč Wi-Fi síti Aukci: „Kdo mi ihned, přesně a lacino sešroubuje kola?“. Dostupní opaskoví roboti začnou dohadovat časové kvóty (vyjednávání). Výrobek analyzuje tu ekonomicky nejbrilantnější odpověď a vydá se v továrně s flexibilním směrováním rovnou k vítěznému stroji.
### 30. Umělá inteligence (AI) a její aplikace kolem nás
Z mračna miliard všudypřítomných monitorujících senzorů propukla krize Big Data; jsou tak enormní, že z nich nelze listovat tužkou tabulky trendů a proto nastoupilo AI – algoritmus kopírující napodobování lidského inteligentního myšlení oboru informatiky. Rozsah aplikace tvoří:
- **Počítačové vidění a Bezpečnost:** Detekování obrazů pouličních bezpečnostních kamer pro spolehlivou evidenci průjezdu kódů obličejů, chování teroristy nebo ochrana před síťovým kyberútokem a viry na síti.
- **Zpracování jazyka (NLP):** Srdce chatbotů (ChatGPT, Alexa, Google). Porozumí významu příkazu mluvené fráze a přes okruh propojení s řízením domovních zařízení IoT vyhodnotí úkon k přepnutí domovních světel a informací.
- **Prediktivní Průmyslová údržba:** Stroj nedosáhne náhlého krachu; AI rozluští vzorce v historických měřeních neškodných vibrací IoT a oznámí operátorům fatální smrt ocelového ložiska plných čtrnácti dní v předstihu naprosto bezchybně, což radikálně drží plynulý optimalizovaný chod. Dále zajišťuje Personalizované reklamy, burzovní obchody či orientaci a dráhu aut.
### 31. Expertní systémy a neuronové sítě (induktivní učení) v IoT
Aplikace znalostí má dva odlišné přístupy v metodě rozuzlení AI.
- **Expertní systémy (Dřívější, logický model):** K dosažení cíle potřebuje systém do paměti nalít od vývojáře zkušenosti lékařů do tabulkových odstavců deduktivních příkazů. Ty tvoří podmínkovou konstrukci (IF-Then/KDYŽ-TAK). („KDYŽ teplota stoupla TAK ho diagnostikuj angínou“) . Je silně limitovaný – nic mimo přesné nakódování situace nezkoumá, nevyhledá a nevyhodnotí, neumí být pružný.
- **Neuronové sítě (Moderní strojové "Induktivní učení"):** Metoda obohacena procesem prožívání s inspirací neuronového propojení mozkové architektury lidí, schopná učení bez fixních definic vývojáře v kódu. Vědec programu nevnucuje vizuální stavbu psího oka či velikosti srsti. Nasype mu balík fotografií, řekne: „Na všech je odraz psa“, a chytré tisíce neuronů postupným doladěním vah uvnitř datové mřížky sítě sami bezvýhradně induktivně určí spojitosti detailů k vytvoření obecného obrazce pravidla. Načež stroj rozpozná jakéhokoli chlupáče nadále spolehlivě v obměnách situace (často pro vizuální, adaptivní i IoT předpověď v cloudu).
### 32. Aplikace prvků umělé inteligence, umělý život, AIoT
- **AIoT (Spojení Intelligence s Things):** Vznikla fúze dvou špičkových technologií zrušením závislosti na obří centralizované eUtilitě vzdáleného cloudu internetu, na jehož výkon se klasické primitivum senzoru z minula plně vymlouvalo a data posílalo. Koncept Edge computingu dostal silný Al čip integrován přímo do vnitřností okrajových kamer budovy. Kamera nesupluje trubku pro zátěž gigabyty surového videa pro internet, pročeše obraz vteřinám v čipu zcela sama, provede rozpoznání hlavy s maskou zaměstnance, přenese úspornou vteřinovou a stoprocentně spolehlivou šifrovanou notifikaci „Karel přišel do dílny v 8:00“ a šetří ohromný přenos v síti.
- **Umělý život (Genetické evoluční algoritmy):** Jedná se o okrajově nepochopitelně poutavou variantu AI. Neklonuje logiku lidského neuronu, sleduje biologii a selektivní pravěkou evoluční stavbu u přežití s přirozeným výběrem mutace. K sestrojení aerodynamiky nového čelního okna, letového designu křídla dronu neposlouží lidská nákresová představivost; počítač ze 100 plně vygenerovaných naprostých paskvilních tvarů svede vzdušný matematický pád "Fitness funkcí", vadné vymaže, účinnější splete křížením, přičemž tisícovka evolucí vyplivne z patvarů pro firmu dechberoucí konstrukci se spolehlivou dynamikou lomení odporů, co by inženýrovi nenapadla.
### 33. Chytrá farma a zemědělství 4.0
Vize modernizace prokazatelně čelí stárnoucím kapacitám farmářů i vyšťavené chemicky plošně drcené destrukci pro ornou půdu zaváděním Průmyslu 4.0 pro takzvané "Precizní hospodářství" pomocí analýzy IoT i dronů pro zvýšení výnosů rostlin i efektivit a zaručení zdraví zvířat pod dozorem systémů v reálném pohledu dat, avšak výzvami je cena a investice na experty pro instalace.
1. **Pěstitelské agriboty a drony:** Minulost patřila plošnému postřiku ohromné zasažené toxické dávky po plodině traktorem (ve 3. PR). Moderně letící senzory vytvoří bezkontaktní síť v mapě u plevele a chřadnutí dehydratace, agriboti s automatickým ovládacím řízením obdrží příkaz z AI výpočtu, naběhnou přesně na mikrodávku a postříkají roztok chemie i hnojiv exkluzivně jen po dvou slabých natích pro celkové astronomické a 90% bezbřehé šetření a ekologickou údržbu.
2. **Kvalita chovného dobytku:** Nezávisí z dohledu člověka v bahně. Vpravují se žaludeční monitorující biokompatibilní "bolusy" či chytré vizuální obojky plné 24hodinových čidel srdečních aktivit a přežvykování i pádu. AI zjistí teplotní vychýlení s predikovaným onemocněním ještě než zvířecí strádání vzroste natolik bolestivě s hrozbou infekce, obratem zašle do hodinek SMS upozornění se záchranou o den zrychleného veterináře k cílené dočasné separaci do zdravého návratu chovu zvířat a krav.
3. **Traceability k masu pro zákazníky:** U celkového cyklu logistiky po stůl obchodu má občan klid. Lidé sejmutím kamerou svého smartphonu z QR stopy obalu vytáhnou uzel čipové databáze IoT (dostupnou od pěstírny z farmy k teplotám na jatečním přepravci), prověří tak zdravotní nezávadnost celého cyklu, transparentnost původu, léčiv, chlazení, převozu v kontejneru a jídla pro rodinný garantovaný spokojený stůl v nezávadnosti 4.0.