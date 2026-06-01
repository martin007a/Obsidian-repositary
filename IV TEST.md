Blok 1 - základní pojmy

> **Komentář vyučujícího:** Otázky 1/10 až 1/14 jsou v rámci cvičení 1 jako samostudium. Je potřeba se naučit, co jednotlivé pojmy znamenají, a znát jejich "aplikace".
- **1/1: IoT je zkratka pro:**
    - _Odpověď:_ Internet of Things (Internet věcí).
- **1/2: Mezi IoT zařízení nepatří:**
    - _Odpověď:_ Běžné pasivní předměty bez senzorů a síťové konektivity (např. obyčejný stůl, klasická žárovka bez Wi-Fi).
- **1/3: Co musí obsahovat každé IoT zařízení?**
    - _Odpověď:_ Výpočetní jednotku (mikrokontrolér), komunikační rozhraní (připojení k síti) a senzor nebo aktor.
- **1/4: Kdy se může stát pasivní prvek, jako krabice s QR kódem, součástí IoT ekosystému?**
    - _Odpověď:_ V momentě, kdy je naskenován aktivním zařízením (např. čtečkou nebo chytrým telefonem), které data o objektu přenese do sítě.
- **1/5: Co je embedded systém?**
    - _Odpověď:_ Jednoúčelový počítačový systém (hardware i software) zabudovaný do většího zařízení, který řídí jeho specifické funkce.
- **1/6: Jaký je rozdíl mezi vývojovou deskou (např. Arduino) a jednoúčelovým embedded zařízením?**
    - _Odpověď:_ Vývojová deska je univerzální a slouží k prototypování, zatímco jednoúčelové zařízení je hardwarově i softwarově optimalizované (velikost, cena, spotřeba) pro finální produkt.
- **1/7: Jaká jsou omezení pro paměť při vývoji embedded zařízení?**
    - _Odpověď:_ Extrémně nízká kapacita (často jen v řádech kilobajtů RAM a flash paměti), což vyžaduje vysoce optimalizovaný kód.
- **1/8: Jaká jsou omezení pro využití energie při vývoji embedded zařízení?**
    - _Odpověď:_ Zařízení často běží na baterie, musí na ně vydržet i roky, a proto se hojně využívají tzv. režimy spánku (sleep modes).
- **1/9: Proč omezujeme v komunikačních protokolech pro IoT zařízení množství přenesených dat?**
    - _Odpověď:_ Kvůli úspoře energie (vysílání stojí nejvíce proudu) a kvůli omezené šířce pásma v IoT sítích (např. LoRaWAN).
- **1/10: Co je digitalizace?**
    - _Odpověď:_ Proces převodu fyzických objektů, procesů a informací do digitální podoby, kterou mohou zpracovávat počítače.
- **1/11: Co je digitální reprezentace?**
    - _Odpověď:_ Datový model nebo struktura, která v počítačovém systému popisuje a zastupuje reálný fyzický objekt.
- **1/12: Čím se vyznačuje digitální dvojče?**
    - _Odpověď:_ Je to virtuální model reálného objektu, který je s ním propojen a synchronizuje se v reálném čase pomocí dat ze senzorů.
- **1/13: Z čeho nevytvořím aktor?**
    - _Odpověď:_ Z čistě vstupního hardwaru (například ze senzoru, teploměru nebo z tlačítka). Aktor musí vykonávat fyzickou akci.
- **1/14: Co není součástí senzoru?**
    - _Odpověď:_ Komponenty provádějící fyzickou změnu prostředí (motory, serva, relé) – ty patří aktorům.
Blok 2 - elektronika
> **Komentář vyučujícího:** Celý blok není pro informatiky komfortní, pro odpovědi stačí znát teorii z 2. cvičení. Výjimku tvoří otázky 2/9 až 2/11, kde je znalost digitálních a analogových vstupů/výstupů pro informatiky klíčová. U nich je nutné znát i aplikaci a důsledky.
- **2/1: Rezistor je pasivní součástka, která slouží pro:**
    - _Odpověď:_ Omezení protékajícího elektrického proudu a úpravu úrovně napětí v obvodu.
- **2/2: V čem se udává hodnota rezistoru?**
    - _Odpověď:_ V ohmech (Ω).
- 2/3: Potenciometr je proměnný odpor. Jak se nastavuje?
    - _Odpověď:_ Mechanickým zásahem (otáčením hřídelky nebo posuvem jezdce), čímž se mění délka odporové dráhy.
- 2/4: Tlačítko je spínač, který při stisku spojí 2 kontakty. Jak jej propojíme s digitálním vstupem?
    - _Odpověď:_ Pomocí pull-up nebo pull-down rezistoru, aby byl na vstupu stabilní a jasně definovaný logický stav, když tlačítko není stisknuté.
- **2/5: Fotorezistor je součástka, která:**
    - _Odpověď:_ Mění svůj elektrický odpor v závislosti na intenzitě světla, které na ni dopadá.
- **2/6: Teplotní čidlo mění výstupní napětí podle teploty v tomto zapojení:**
    - _Odpověď:_ V zapojení jako dělič napětí.
- **2/7: Jak poznám katodu LED?**
    - _Odpověď:_ Je to obvykle kratší nožička, případně je na straně katody pouzdro diody mírně seříznuté (zploštělé).
- **2/8: Při jakém zapojení propouští LED proud?**
    - _Odpověď:_ V propustném směru (anoda je připojena na kladný pól, katoda na záporný).
- **2/9: Co je digitální vstup zařízení?**
    - _Odpověď:_ Vstupní pin, který dokáže rozeznat pouze dva stavy napětí: logickou 1 (HIGH) a logickou 0 (LOW).
- **2/10: Jak se liší analogový vstup od digitálního?**
    - _Odpověď:_ Analogový vstup umí měřit spojité rozmezí hodnot (např. různé úrovně napětí od 0 do 5V převede na číslo), zatímco digitální rozezná jen dva extrémy (vypnuto/zapnuto).
- **2/11: Jaký je rozdíl mezi digitálním vstupem a výstupem pro napětí 0-5V?**
    - _Odpověď:_ Digitální _vstup_ napětí čte (detekuje, zda je přítomno ~5V nebo ~0V). Digitální _výstup_ napětí naopak fyzicky generuje a nastavuje (vysílá buď 5V, nebo 0V).

Blok 3 - základ komunikac
> **Komentář vyučujícího:** Standardní otázky. Je potřeba znát jak teorii, tak její aplikaci
- **3/1: Co je komunikační protokol?**
    - _Odpověď:_ Soubor formálních pravidel a standardů definujících formát, řízení a způsob přenosu dat mezi zařízeními.
- **3/2: Která z následujících oblastí není typicky řešena komunikačním protokolem?**
    - _Odpověď:_ Vnitřní aplikační logika programů nebo fyzický design hardwarových konektorů (záleží na vrstvě OSI, ale protokol řeší primárně přenos).
- **3/3: Co neobsahuje komunikační protokol?**
    - _Odpověď:_ Neobsahuje konkrétní uživatelská data (payload je jen přenášen, není součástí definice protokolu) ani samotnou implementaci v programovacím jazyce.
- **3/4: Kde je komunikační protokol zapsán a kde je aplikován?**
    - _Odpověď:_ Zapsán je ve standardech a specifikacích (např. RFC dokumentech), aplikován je v softwarových a firmwarových síťových stackách zařízení.
- **3/5: Co je API?**
    - _Odpověď:_ Application Programming Interface. Je to rozhraní, které umožňuje dvěma různým softwarovým aplikacím vzájemně komunikovat.
- **3/6: Co je to MQTT?**
    
    - _Odpověď:_ Message Queuing Telemetry Transport. Extrémně lehký komunikační protokol typu publish/subscribe, navržený přímo pro IoT.
        
- **3/7: Jaké role definuje MQTT protokol?**
    - _Odpověď:_ Klienta (Publisher a/nebo Subscriber) a centrální uzel, tzv. Broker.
- **3/8: Proč se využívá MQTT v IoT?**
    - _Odpověď:_ Má minimální datovou režii (malé hlavičky), šetří baterii a je velmi spolehlivý i v nestabilních sítích.
- **3/9: Jak se liší UART od paralelní komunikace?**
    - _Odpověď:_ UART přenáší data sériově (bit po bitu za sebou po jednom drátě), paralelní komunikace přenáší více bitů současně po několika drátech. 
- **3/10: Proč musí být Baud Rate nastaven stejně na obou stranách komunikace?**
    - _Odpověď:_ Aby obě zařízení věděla, jak dlouho trvá jeden bit. Jinak by docházelo ke špatnému čtení hodnot a k poškození přenášených dat.

Blok 4 - software

> **Komentář vyučujícího:** Tato témata jsme sice teoreticky neprobírali, ale jako informatici byste je měli perfektně zvládat. Jedná se o nejtěžší typy odpovědí. Je třeba dávat pozor na pasti a jemné nuance v možnostech.

- **4/1: Co je Frontend v kontextu webové aplikace?**
    - _Odpověď:_ Klientská (uživatelská) část aplikace, která běží v prohlížeči (UI, grafika, interakce).
- **4/2: Co je Backend v kontextu webové aplikace?*
    - _Odpověď:_ Serverová část aplikace, která řeší obchodní logiku, přístup k databázi a poskytuje data frontendu (např. přes API).
- **4/3: Co je Backend?**
    - _Odpověď:_ Obecně neviditelná vrstva jakéhokoliv systému, která zajišťuje zpracování dat, ukládání a komplexní výpočty.
- **4/4: Co je Software?*sss
    - _Odpověď:_ Nehmotná část počítače – sada instrukcí, dat nebo programů, která říká hardwaru, jak má pracovat.
- **4/5: Co je Firmware?**
    - _Odpověď:_ Specifický typ softwaru, který je nízkoúrovňově a trvale svázán s konkrétním hardwarem, aby řídil jeho základní funkce.
- **4/6: Jak se liší Software od Firmwaru?**
    - _Odpověď:_ Firmware je uložen v nevolatilní paměti zařízení, je nezbytný pro jeho běh a zřídka se aktualizuje. Běžný software (např. aplikace) je nadstavba, kterou si uživatel snadno instaluje nebo maže.

Blok 5 - Komunikační protokoly
> **Komentář vyučujícího:** Standardní otázky na teorii i aplikaci
- **5/1: Co není komunikační protokol?**
    - _Odpověď:_ Například formáty a jazyky jako JSON, XML, HTML nebo CSV (ty definují strukturu dat, nikoliv pravidla přenosu).
- **5/2: Jaká je struktura HTTP požadavku?**
    - _Odpověď:_ Metoda (GET, POST, atd.), cíl (URL), verze HTTP, hlavičky (Headers) a případně tělo (Body).
- **5/3: Jaká je struktura HTTP odpovědi?**
    - _Odpověď:_ Verze HTTP, stavový kód (např. 200 OK), hlavičky (Headers) a tělo zprávy (Body).
- **5/4: Co znamená zkratka REST?**
    - _Odpověď:_ Representational State Transfer.
- **5/5: Které z níže uvedených REST API je správně zadáno?**
    - _Odpověď:_ Správné REST API používá jako URL podstatná jména reprezentující zdroje, nikoliv slovesa (např. správně je `GET /users/1`, špatně je `POST /getUser`).
- **5/6: Co je Endpoint?*
    - _Odpověď:_ Specifická adresa (URL) na serveru, na kterou směřuje požadavek a kde je dostupný konkrétní zdroj API.
- **5/7: Co musí obsahovat JSON?**
    - _Odpověď:_ Klíče a hodnoty. Názvy klíčů přitom musí být vždy vloženy do dvojitých uvozovek.
- **5/8: Která HTTP metoda se používá pro získání reprezentace zdroje?**
    - _Odpověď:_ Metoda `GET`.
- **5/9: Která HTTP metoda se používá pro vytvoření nového zdroje, nebo provedení akce?**
    - _Odpověď:_ Metoda `POST`.
        
- **5/10: Co znamená, že REST je bezstavový?**
    - _Odpověď:_ Server si neukládá žádný kontext o klientovi mezi jednotlivými požadavky. Každý dotaz klienta musí obsahovat všechny informace potřebné k jeho odbavení.
- **5/11: Co je hlavní rozdíl mezi API a jeho implementací?*
    - _Odpověď:_ API je pouhý „kontrakt“ nebo rozhraní (popisuje, jak má komunikace vypadat). Implementace je reálný výkonný kód na straně serveru, který API požadavek zpracuje.
- **5/12: Jaký je správný způsob zápisu pole v JSON formátu?**
    - _Odpověď:_ Pomocí hranatých závorek. (Příklad: `["hodnota1", "hodnota2"]`).