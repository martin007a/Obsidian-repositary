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



/// MATROŠ dokument,

### 11. Výhody a nevýhody OPC UA a MQTT v IoT
Tyto dva komunikační protokoly slouží k výměně dat mezi zařízeními, každý se ale hodí na něco jiného.
- **Protokol MQTT:** je lehký, rychlý a jednoduchý komunikační protokol, který se používá hlavně v IoT systémech pro přenos zpráv mezi zařízeními.
    - _Výhody:_ Extrémně datově nenáročný (šetří šířku pásma), spolehlivý i na špatných sítích (senzory na poli) a má nízkou spotřebu energie.
    - _Nevýhody:_ Přenáší pouze raw data ("holý text"). Neřeší strukturu – systém nepozná, zda jde o Celsius či Fahrenheit. Má omezenou škálovatelnost.
- **Protokol OPC UA:** je moderní standard pro komunikaci v průmyslové automatizaci, který slouží k bezpečné a strukturované výměně dat mezi zařízeními a systémy.
    - _Výhody:_ Je univerzální, nezávislý na platformě (Windows, Linux, Cloud), a především řeší sémantiku a rozšířená metadata. Nepošle jen číslo "22", ale strukturovaný balíček ("22 °C, čidlo 5, robot KUKA"). Má zabudovanou velmi silnou kybernetickou bezpečnost (šifrování).
    - _Nevýhody:_ Je to "těžký" a komplexní protokol náročný na výpočetní výkon, paměť i datovou propustnost, který se nehodí pro bateriové levné čipy.
### 12. Průmyslový internet věcí (IIoT)
Rozdíl mezi běžným spotřebitelským IoT a IIoT (Industrial Internet of Things) je propastný. U běžného IoT (chytré hodinky, ledničky) výpadek internetu nezpůsobí tragédii. IIoT představuje implementaci do kritické infrastruktury, propojující průmyslová zařízení, senzory a systémy např. v chemických továrnách či elektrárnách.
**Zásadní požadavky a rozdíly IIoT:**
- **Kritičnost a Safety:** Jakékoliv selhání ohrožuje lidské životy (výbuch) nebo nese obří finanční ztráty. Kybernetická bezpečnost vyžaduje autentizaci a šifrování.
- **Extrémní podmínky:** Hardware musí odolávat silným vibracím, žáru, prachu a agresivním chemikáliím.
- **Životnost:** Zařízení se do linek instalují s očekáváním spolehlivého chodu 15 až 20 let (oproti 3 letům u telefonu).
- **Výsledek:** Integrací s AI a Big Data zavádí prediktivní údržbu – stroj dokáže analyzovat vzorce, předpovídat chování a nahlásit budoucí poruchu dříve, než se skutečně rozbije.
### 15. Logistika věcí (Supply chain), automatická identifikace (AutoID)
- **Logistika věcí** – plánování, provádění a řízení toku materiálů, informací a služeb od dodavatelů k zákazníkům. Mnoho procesů jako je nákup, výroba, skladování, distribuce a správa inventáře. Cílem je zajištění správnosti zboží ve správném čase a za správnou cenu. Díky IOT můžeme zaznamenávat např. polohu (GPS, RFID), teplotu… 
- **Automatická Identifikace** – identifikace a sběr dat o objektech a lidí, bez manuální práce. Zahrnuje různé metody jako – čárové kódy, RFID, QR kódy, biometrie a další. Automatické sledování a identifikace osob a objektů v logistickém řetězci. Např. pás se skenem čárových kódů.
- **Traceability (Sledovatelnost):** Hlavním cílem logistiky. V potravinářství lze díky AutoID zkažené maso v supermarketu do vteřiny zpětně vytrasovat ke konkrétnímu kamionu, jatkám i přesné krávě na farmě.

### 20. Aktivní a pasivní tagy, transpondéry
- **Pasivní tagy** – neobsahují zdroj napájení, energii získávají z rádiových vln čtečky. Jednoduchá konstrukce, menší a levnější než aktivní. Mají omezený dosah, protože jejich výkon závisí na poskytnuté energii čtečkou. Dosah běžně v centimetrech až několika metrech. Využívány třeba ve sledování a identifikaci výrobků, palet, zásob atd. ISIC 
- **Aktivní tagy** – mají vlastní napájení, většinou baterie. Jsou schopny generovat vlastní rádiové signály, mají vyšší dosah a výkon než pasivní tagy. Fungují na větší vzdálenost a mají spolehlivější komunikaci. Využívány v situacích, kde je potřeba větší vzdálenost – doprava, logistika, bezpečnost. • 
- **Transpondéry** – elektronická zařízení, která automaticky přijímají, zpracovávají a odpovídají na rádiové nebo jiné signály. Je to zařízení, které reaguje na signál a většinou odpovídá nějakou informací – automaticky a bez zásahu člověka. Např. RFID TAG – reaguje na čtečku signálu a posílají uložené informace
### 21. Principy komunikace FFC a NFC
Tyto komunikační technologie se dělí podle toho, s jakou zónou – blízkou, nebo dalekou – pracují.
- **FFC** – Používá elektromagnetické vlny, které se šíří vzduchem na delší vzdálenosti (typicky **UHF RFID – 860–960 MHz**). Komunikace probíhá pomocí odražených vln – čtečka vyšle signál, tag ho moduluje zpět (tzv. backscatter). Dosah je až 10 metrů. Využití např ve skladech, logistice 
- **NFC** – near field communication je bezdrátová komunikační technologie na výměnu dat na krátkou vzdálenost. Princip založen na elektromagnetickém poli. Využívá princip indukčního a rezonančního přenosu dat, má dva režimy: aktivní a pasivní. V aktivním režimu jsou obě zařízení schopny vzájemně vysílat a přijímat data. V pasivním je jedno aktivní a druhé pasivní, to získá energii z el.mag. pole k provádění komunikace. Často využíváno pro mobilní platby, sdílení souborů, připojování…
### 22. EPC, standardy a systémy AutoID, EPCIS
- EPC (Electronic Product Code): Nový standard. Je to dlouhé číslo pro UHF tagy, absolutně unikátní pro každičký jednotlivý specifický kus zboží na světě. Standardy rozvíjí globální organizace EPC Global. 
- EPCIS (EPC Information Services): Když RFID čtečky vygenerují obrovská data pohybu, všechno se propojí v EPCIS – standardizované sdílené databázi. To umožňuje dokonalou sledovatelnost a transparentnost (Traceability).

| **Událost (Event)** | **Popis v EPCIS databázi**                                         |
| ------------------- | ------------------------------------------------------------------ |
| **Create**          | Výrobce vytvořil krabici a zaznamenal do ní unikátní EPC.          |
| **Ship**            | Zboží opustilo sklad – EPCIS uloží událost jako odeslanou.         |
| **Receive**         | Distributor krabici přijal a přečetl – zaznamenáno.                |
| **Cold chain**      | Napojený senzor během logistiky potvrdí, že teplota se nezhoršila. |
- **AutoID standarty** – Mezi tyto patří GS1, který zahrnuje kódování dat pomocí čárových/QR kódu pro identifikaci výrobků. Dalšími jsou třeba ISO/IEC 18000 pro RFID, ISO/IEC 15418 pro čárové kódy…
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
- **dB (Decibel):** poměr vyslaného signálu k přijatému, je to logaritmická veličina 
- **dBm (Decibel-milliwatt):** Síla aktuálního signálu.
- **dBi (Decibel-izotropní):** Porovnání antény s ideální hodnotou.
### 28. Kyberneticko-fyzikální systémy (CPS) a principy kolaborace
Ve 4. průmyslové revoluci nevévodí pasivní stroje nýbrž silné CPS systémy propojující fyzický svět s digitálním mozkem. CPS je tvořen reálným připojeným přístrojem, softwarovým řízením a hlavně trvalým zrcadlovým AI obrazem nahoře na webu jako Digitální dvojče (což dovoluje naprostou synchronizaci informovanosti).
**Vzájemná závislost a distribuované rozhodování:** Složky mají přímou provázanost. V minulé éře musel poruchu na výrobním opasku přenastavit a vyřešit stopnutím centrální lidský operátor. V Průmyslu 4.0 řeší CPS agendu s metodou přímé síťové decentralizace M2M (Machine to Machine) pro vzájemnou efektivní Kolaboraci napřímo. Zjistí-li linkový stroj závadu na vlastním ložisku rotoru, síťovým oknem pošle informativní hlášení přímo všem následným opaskovým strojům ve výrobě. Obdržené upozornění ("zpomaluji proces") automatizovaně a s naprostou elegancí odstartuje balanční rekonfiguraci napříč celou linkou – aniž by člověk sahal na ovládání a celková fabrika jakkoliv kolabovala či zastavila chod.
### 29. Agent a multiagentní systémy, autonomní systémy
Autonomní rozhodování z okruhu 28. řídí zóna "Softwarových Agentů" postavených na systému MAS.
Agent – entita která vnímá své okolí, rozhoduje se na základě získaných informací a provádí akce s cílem dosáhnutí určitých cílů.
- **Multi-agentní systémy (MAS):** Tímto termínem označujeme mraveniště plné spolupracujících entit agentů a to buď pro montáž nebo sborové kooperace harvestorů u lánu obilí. Agentem však není zprostředkován exkluzivně svářeč robota, ale zastupuje i vrtačku či neúplný svařovaný Produkt.
    - **Klíčové vyjednávání v Aukci:** Fabrika MAS je geniálně efektivní. Rám vyráběného automobilu (identifikovaný Agent) sjede z pásu a rozezná úkol upnout a namontovat kola. Namísto pasivního naprogramování na pevnou dráhu k jedné pozici vypíše rám bez zaváhání napříč Wi-Fi síti Aukci: „Kdo mi ihned, přesně a lacino sešroubuje kola?“. Dostupní opaskoví roboti začnou dohadovat časové kvóty (vyjednávání). Výrobek analyzuje tu ekonomicky nejbrilantnější odpověď a vydá se v továrně s flexibilním směrováním rovnou k vítěznému stroji.
**Autonomní systémy** – systémy které mají schopnost se samostatně rozhodovat a provádět akce bez lidského řízení. Využívají různé systémy jako senzory, AI, řídící algoritmy, aby mohly vnímat své okolí, analyzovat data, rozhodovat se a provádět akce. Často jsou využívány v autonomních vozidlech, robotice, průmyslové automatizaci nebo řízení budov. 
### 30. Umělá inteligence (AI) a její aplikace kolem nás
- **Umělá inteligence** - je obor informatiky, který se zabývá tvorbou programů a strojů schopných vykonávat činnosti, které by jinak vyžadovaly lidskou inteligenci. 
- **Personalizované reklamy a doporučení AI** – používá se pro analýzu chování a preferenci uživatelů na základě reklam, produktů nebo služeb. 
- **Zpracování přirozeného jazyka** – AI se používá pro rozpoznávání, porozumění a generování lidského jazyka. Příklady – virtuální asistenti, překladače, chatboti. 
- **Diagnostika a lékařské aplikace** – AI se také využívá pro analýzu medicínských dat, rozpoznávání obrazu a diagnostiky různých onemocnění. 
- **Autonomní vozidla** – klíčová součást, AI rozpoznává překážky, rozhoduje se a plánuje trasy. 
- **Průmyslová automatizace** – AI se využívá k řízení a optimalizaci průmyslových procesů. Pomáhá k předpovídání poruch, optimalizaci a řízení. 
- **Finanční predikce a obchodování** – analýza finančního trhu, predikce cen, obchodování na burze. 
- **Bezpečnost a kybernetická ochrana** – detekce a analýza kybernetických hrozeb, prevence podvodů, zajištění sítě a systému proti útokům.
### 31. Expertní systémy a neuronové sítě (induktivní učení) v IoT
Aplikace znalostí má dva odlišné přístupy v metodě rozuzlení AI.
- **Expertní systémy** - založeny na získávání a reprezentaci znalostní od odborníků v daném oboru. Systémy využívají logická pravidla a inferenční mechanismy k provádění analýz a rozhodování na základě dat. V rámci IoT mohou pomáhat při diagnostice a řešení problémů, rozhodování a optimálních akcí.
- **Neuronové sítě** - metoda induktivního učení, inspirována lidským mozkem a zpracováním informací pomocí neuronů. Jsou schopné se učit ze zkušeností a adaptovat se na nové situace. Mohou být využity pro analýzu a předpovídání dat, detekci vzorců, klasifikaci, rozpoznávání obrazu, optimalizaci systému atd.
- **V kombinace s IoT** – expertní systémy a neuronové sítě mohou poskytovat inteligentní rozhodování, analýzu a řízení v reálném čase. Expertní systémy mohou využívat neuronové sítě k učení a získávání znalostí, mezitím co neuronové sítě mohou díky vstupem z IoT mohou poskytovat predikce a adaptivní řízení na základě dat.
### 32. Aplikace prvků umělé inteligence, umělý život, AIoT
### 1. Praktické aplikace v praxi
- **Chytrá domácnost** – AI může být použito k rozpoznávání hlasových příkazů, automatizaci zařízení v domácnosti, správu spotřeby energie, optimalizace osvětlení, topení a dále. 
- **Průmyslová automatizace** – AI v AIoT může zlepšit automatizaci v průmyslových prostředích díky rozpoznávání vzorců, předpovídáním poruch, optimalizaci procesů a řízení chytrých továren. 
- **Inteligentní doprava** – může být využito také pro řízení a optimalizaci dopravního systému, predikce dopravních situací, správa parkování, poskytnutí personalizovaných informacích o dopravě.
##### Koncept AIoT
AIoT představuje fúzi dvou špičkových technologií, která zásadně mění dosavadní fungování sítí. Klasické „primitivní“ senzory dříve pouze sbíraly data a kompletně spoléhaly na obrovský výkon vzdálených centralizovaných cloudů, kam musely vše odesílat.
Díky konceptu **Edge computingu** se však výkonný AI čip integruje přímo do koncových zařízení na okraji sítě (např. do bezpečnostních kamer).
##### Umělý život
Jedná se o fascinující a specifickou odnož umělé inteligence. Na rozdíl od běžné AI nekopíruje logiku lidského neuronu, ale inspiruje se biologií – konkrétně principy přirozeného výběru, mutace a evolučního přežití.

Tento přístup se využívá tam, kde lidská představivost nestačí, například při navrhování aerodynamiky nového čelního skla nebo tvaru křídla dronu.
### 33. Chytrá farma a zemědělství 4.0
Vize modernizace prokazatelně čelí stárnoucím kapacitám farmářů i vyšťavené chemicky plošně drcené destrukci pro ornou půdu zaváděním Průmyslu 4.0 pro takzvané "Precizní hospodářství" pomocí analýzy IoT i dronů pro zvýšení výnosů rostlin i efektivit a zaručení zdraví zvířat pod dozorem systémů v reálném pohledu dat, avšak výzvami je cena a investice na experty pro instalace.
1. **Pěstitelské agriboty a drony:** Minulost patřila plošnému postřiku ohromné zasažené toxické dávky po plodině traktorem (ve 3. PR). Moderně letící senzory vytvoří bezkontaktní síť v mapě u plevele a chřadnutí dehydratace, agriboti s automatickým ovládacím řízením obdrží příkaz z AI výpočtu, naběhnou přesně na mikrodávku a postříkají roztok chemie i hnojiv exkluzivně jen po dvou slabých natích pro celkové astronomické a 90% bezbřehé šetření a ekologickou údržbu.
2. **Kvalita chovného dobytku:** Nezávisí z dohledu člověka v bahně. Vpravují se žaludeční monitorující biokompatibilní "bolusy" či chytré vizuální obojky plné 24hodinových čidel srdečních aktivit a přežvykování i pádu. AI zjistí teplotní vychýlení s predikovaným onemocněním ještě než zvířecí strádání vzroste natolik bolestivě s hrozbou infekce, obratem zašle do hodinek SMS upozornění se záchranou o den zrychleného veterináře k cílené dočasné separaci do zdravého návratu chovu zvířat a krav.
3. **Traceability k masu pro zákazníky:** U celkového cyklu logistiky po stůl obchodu má občan klid. Lidé sejmutím kamerou svého smartphonu z QR stopy obalu vytáhnou uzel čipové databáze IoT (dostupnou od pěstírny z farmy k teplotám na jatečním přepravci), prověří tak zdravotní nezávadnost celého cyklu, transparentnost původu, léčiv, chlazení, převozu v kontejneru a jídla pro rodinný garantovaný spokojený stůl v nezávadnosti 4.0.