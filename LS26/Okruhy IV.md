---
tags: [IoT, zkouska, internet_veci, skripta]
aliases: [Okruhy ke zkoušce IoT]
---

# Okruhy ke zkoušce: Internet věcí (IoT)

## 1. Trendy digitalizace a řízení, automatizace a sítě kolem nás
**1. Sítě a systémy kolem nás** Koncepce internetu věcí (IoT) se postupně rozšiřuje do ještě komplexnější podoby, takzvaného **Internetu všeho (Internet of Everything - IoE)**. Jde o dynamickou síťovou infrastrukturu, která inteligentně propojuje čtyři hlavní pilíře: **lidi, procesy, data a věci**.

Tyto vzájemně propojené systémy nás dnes obklopují v mnoha aplikačních oblastech, mezi které patří například:

- **Smart Home** (inteligentní budovy a domácnosti),
- **Smart City** (chytrá města s inteligentní dopravou či parkováním),
- **Smart Grids** (chytré energetické sítě),
- **Průmysl 4.0** a **Zemědělství 4.0** (Smart Farming, flotily agribotů).

Základem fungování těchto sítí je komunikace, která probíhá na několika úrovních interakce: **M2M** (Machine to Machine – komunikace přímo mezi stroji bez manuální pomoci člověka), **M2P** (Machine to People) a **P2P** (People to People).

**2. Trendy digitalizace a digitální ekonomika** Digitalizace a **digitální transformace (DX)** představují proces, při kterém dochází k zásadnímu přepracování produktů, procesů a strategií uvnitř organizací s využitím moderních technologií. Nejde pouze o převedení starých analogových úloh do počítače. Digitalizace umožňuje dělat věci rychleji, lépe a zcela novými způsoby, čímž vzniká tzv. **digitální ekonomika**.

Klíčovými technologickými trendy, které tuto transformaci pohánějí, jsou:

- **Cloud computing a mobilní platformy**.
- **Zpracování velkých dat (Big Data)**.
- **Umělá inteligence (AI) a strojové učení**.
- Samotný **Internet věcí (IoT)**.

Zásadním trendem a nutností pro úspěšnou digitalizaci průmyslu je **konvergence informačních technologií (IT) a operačních technologií (OT)**. Zatímco operační technologie (OT) představují hardware a software pro přímé monitorování a řízení průmyslové infrastruktury a výrobních strojů, IT zajišťuje zpracování informací a komunikační sítě. Jejich bezproblémové sloučení do jednoho modelu snižuje náklady, zvyšuje bezpečnost a zefektivňuje výrobní procesy.

**3. Řízení a automatizace** Z pohledu kybernetiky a Průmyslu 4.0 je moderní řízení charakteristické nasazením **Kyberneticko-fyzikálních systémů (CPS)**. Tyto systémy propojují fyzické výrobní zařízení s jeho digitálním modelem (digitálním dvojčetem) a neustále se aktualizují v průběhu celého životního cyklu.

Automatizace a řízení těží z několika principů:

- **Zpětná vazba v kybernetice:** Řízení dynamických systémů vychází ze zpětné vazby, kdy se signál ze senzorů porovná s požadovanou hodnotou a řídicí algoritmus (Controller) na základě odchylky vydá pokyn akčnímu členu. Ukázkou je chytrá farma, kde senzory měří vlhkost půdy a systém na základě těchto dat (a případně i předpovědi počasí z internetu) automaticky rozhodne, kdy a kolik zalévat.
- **Vývoj úrovní automatizace:** Automatizace se vyvíjí od **RPA (Robotic Process Automation)**, což je nasazení softwaru pro rutinní a opakující se úkoly, přes pokročilou automatizaci zpracovávající nestrukturovaná data, až po **kognitivní automatizaci**, která využívá umělou inteligenci a adaptivní algoritmy k samostatnému a komplexnímu rozhodování bez zásahu člověka.
- **Distribuované a kolaborativní řízení:** Řízení se přesouvá od centralizovaných systémů k distribuovaným **multiagentním systémům (MAS)**. Využívají se autonomní prvky (agenti či **holony**), které dokážou vnímat své prostředí, uvažovat v kontextu, sdílet společné cíle, delegovat podúlohy a aktivně spolupracovat (kooperovat) s ostatními stroji. Příkladem v praxi mohou být koordinované roje dronů nebo flotily agribotů pracující na poli.
**1. Specifické dělení moderních „Webů“ a sítí** V trendech sítí kolem nás skripta dělí vývoj internetu a přístupu k němu do několika vývojových fází:

- **Blízký Web (Near web):** Internet, který vidíme a ovládáme přes běžné obrazovky, jako jsou počítače a notebooky.
- **Všudypřítomný Web (Here web):** Internet, který je neustále s námi, typicky v mobilních telefonech a nositelné elektronice.
- **Vzdálený Web (Far web):** Obsah zobrazený na velkoplošných obrazovkách nebo informačních kioscích.
- **Podivný Web (Weird web):** Internet, který umožňuje přístup a ovládání prostřednictvím hlasu a umělé inteligence, například v chytrých systémech aut.
- Z hlediska komunikace sítí je obrovským trendem posun k sítím **D2D (Device to Device)**, což jsou senzorové sítě sloužící výhradně komunikaci mezi chytrými stroji bez lidského rozhraní.

**2. Trendy ve výpočetních sítích: Od Cloudu k Fog a Edge computingu** Zatímco dříve se v digitalizaci data z IoT posílala výhradně do centralizovaných datacenter (**Cloud computing**), dnešním trendem je decentralizace. Důvodem je to, aby sítě nebyly přetížené a řídicí systémy mohly reagovat okamžitě:

- **Fog computing:** Přesouvá výpočetní infrastrukturu blíž k okraji sítě, přímo k zařízením. Zařízení komunikují peer-to-peer a řeší data lokálně (např. chytré semafory si samy analyzují kamerový záznam dopravy na křižovatce a nezatěžují centrální server posíláním videa).
- **Edge computing:** Samotné zpracování a filtrace dat probíhá přímo na koncových zařízeních nebo lokálních senzorových sítích (WNS).

**3. Hlubší kybernetický pohled na řízení (Hierarchie zpětných vazeb)** Ačkoliv jsme zmínili, že řízení stojí na kybernetické zpětné vazbě, přednášky v rámci Průmyslu 4.0 hierarchizují tuto zpětnou vazbu (ZV) do několika úrovní:

- **Operační zpětná vazba:** Základní technologické řízení systémem senzor-akční člen (např. senzor naměří suchou půdu a automaticky sepne zavlažování).
- **Programová a Symbolická zpětná vazba:** Složitější prediktivní řízení (např. chytrá farma zjistí z předpovědi počasí na internetu, že zítra bude pršet, a proto zavlažování chytře odloží).
- **Sociální zpětná vazba:** Nejvyšší úroveň komplexity, která zohledňuje fungování lidské společnosti a ekonomiky.

**4. Disruptivní technologie a vývojové třídy automatizace** K trendům digitalizace nepatří jen samotné technologie, ale to, jak radikálně narušují stávající trhy (**disruptivní technologie**). Do řízení a automatizace vstupují inovace jako _blockchain_ a _inteligentní smlouvy (smart contracts)_, které směřují k tzv. programovatelné ekonomice. U samotného řízení procesů a automatizace rozeznáváme 3 vývojové třídy:

1. **RPA (Robotic process automation):** Nasazení takzvaných "digitálních pracovníků" (softwarových botů) na vysoce objemové, rutinní administrativní a transakční práce.
2. **EPA (Enhanced process automation):** Rozšířená automatizace pracující s nestrukturovanými daty a databázemi znalostí.
3. **Kognitivní automatizace:** Plné nasazení prvků umělé inteligence, strojového učení, analýzy velkých dat a zpracování přirozeného jazyka (NLP).

Pokud si propojíte můj předchozí výstup s těmito čtyřmi doplňky, máte první okruh z vašich skript a přednášek pokrytý zcela komplexně.