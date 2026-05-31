---
tags: [IoT, zkouska, internet_veci, skripta]
aliases: [Okruhy ke zkoušce IoT]
---

# Okruhy ke zkoušce: Internet věcí (IoT)

# 1. Trendy digitalizace a řízení, automatizace a sítě kolem nás
### 1. Sítě a systémy kolem nás
Koncepce internetu věcí (IoT) se postupně rozšiřuje do ještě komplexnější podoby, takzvaného Internetu všeho (Internet of Everything - IoE). Jde o dynamickou síťovou infrastrukturu, která inteligentně propojuje čtyři hlavní pilíře: lidi, procesy, data a věci. Tyto vzájemně propojené systémy nás dnes obklopují v mnoha aplikačních oblastech, mezi které patří například:
- **Smart Home**inteligentní budovy a domácnosti),
- **Smart City** (chytrá města s inteligentní dopravou či parkováním),
- **Smart Grids** (chytré energetické sítě),
- **Průmysl 4.0 a Zemědělství 4.0** (Smart Farming, flotily agribotů).
Základem fungování těchto sítí je komunikace, která probíhá na několika úrovních interakce: M2M (Machine to Machine – komunikace přímo mezi stroji bez manuální pomoci člověka), M2P (Machine to People) a P2P (People to People).
### 2. Digitalizace
Digitalizace neznamená jen prosté převedení starých analogových úloh do počítače. Jedná se o komplexní proces, při kterém se celé fyzické a provozní činnosti převádějí do digitálních modelů, čímž se podnikání stává rychlejším a efektivnějším. Klíčovými technologickými trendy, které tuto transformaci pohánějí, jsou:
- Cloud computing a mobilní platformy.
- Zpracování velkých dat (Big Data).
- Umělá inteligence (AI) a strojové učení.
- Samotný Internet věcí (IoT).
Zásadním trendem a nutností pro úspěšnou digitalizaci průmyslu je **konvergence informačních technologií (IT) a operačních technologií (OT)**. Zatímco operační technologie (OT) představují hardware a software pro přímé monitorování a řízení průmyslové infrastruktury a výrobních strojů, IT zajišťuje zpracování informací a komunikační sítě. Jejich bezproblémové sloučení do jednoho modelu snižuje náklady, zvyšuje bezpečnost a zefektivňuje výrobní procesy.
### 3. Řízení a automatizace
Z pohledu kybernetiky a Průmyslu 4.0 je moderní řízení charakteristické nasazením **Kyberneticko-fyzikálních systémů (CPS)**. Tyto systémy propojují fyzické výrobní zařízení s jeho digitálním modelem (digitálním dvojčetem) a neustále se aktualizují v průběhu celého životního cyklu.
Automatizace a řízení těží z několika principů:
- **Zpětná vazba v kybernetice:** Řízení systému pomocí porovnávání dat ze senzorů s požadovanou hodnotou; na základě zjištěné odchylky pak algoritmus vydává pokyny akčním členům.
- **Distribuované a kolaborativní řízení:** Přesun od centrálního řízení k multiagentním systémům (MAS). Autonomní prvky vnímají okolí, sdílejí cíle a aktivně mezi sebou spolupracují (např. roje dronů).
- **Komunikace D2D (Device to Device):** Obrovský trend posunu k senzorovým sítím sloužícím výhradně pro přímou komunikaci mezi chytrými stroji bez lidského rozhraní.
### 4. Disruptivní technologie a vývojové třídy automatizace
K trendům digitalizace nepatří jen samotné technologie, ale to, jak radikálně narušují stávající trhy (disruptivní technologie). Do řízení a automatizace vstupují inovace jako blockchain a inteligentní smlouvy (smart contracts), které směřují k tzv. programovatelné ekonomice.
U samotného řízení procesů a automatizace rozeznáváme 3 vývojové třídy:
- **RPA (Robotic Process Automation):** Nasazení takzvaných "digitálních pracovníků" (softwarových botů) na vysoce objemové, rutinní administrativní a transakční práce.
- **EPA (Enhanced Process Automation):** Rozšířená automatizace pracující s nestrukturovanými daty a databázemi znalostí.
- **Kognitivní automatizace:** Plné nasazení prvků umělé inteligence, strojového učení, analýzy velkých dat a zpracování přirozeného jazyka (NLP) k samostatnému rozhodování bez zásahu člověka.
# 2. Průmyslové revoluce z pohledu kybernetiky a řízení
#### 1. Vývoj průmyslových revolucí a způsobů řízení
Abychom pochopili 4. průmyslovou revoluci, je nutné se podívat, jak se historicky měnila míra komplexity a přístup k řízení procesů:
- **1. průmyslová revoluce (konec 18. stol.):** Přinesla mechanizaci výroby pomocí vodní a parní energie. Řízení bylo čistě mechanické bez inteligence. 
- **2. průmyslová revoluce (začátek 20. stol.):** Typická zaváděním elektrické energie a specializovanou masovou výrobou (např. montážní linky Ford).
- **3. **průmyslová revoluce:** Zásadní zlom – nástup IT a prvních PLC (Programovatelné logické automaty – průmyslové počítače). Vznikají ASŘ (Automatizované systémy řízení). Problém 3. revoluce spočíval v tom, že linky sice byly automatické, ale vysoce rigidní (nepružné) a centralizované. Stroj uměl provádět pouze jednu pevně naprogramovanou činnost.
- **4. průmyslová revoluce (Průmysl 4.0 - současnost):** Dnešní stav, který staví na CPS (Kyberneticko-fyzikálních systémech). Pevné výrobní linky se mění na flexibilní sítě. Stroje a produkty jsou připojeny k internetu věcí a dokážou se mezi sebou domlouvat.
#### 2. Kybernetika jako základ moderního řízení
Z pohledu kybernetiky (vědy o řízení a komunikaci, kterou definoval Norbert Wiener) fungují všechny tyto automatizované systémy na principu takzvané zpětné vazby (feedback loop). Ta se skládá přesně ze 3 na sebe navazujících kroků:
1. **Senzorický podsystém:** Nejprve musí systém změřit aktuální stav fyzického prostředí (např. senzor zjistí, že teplota v místnosti klesla na 15 °C).
2. **Řídicí podsystém (Controller):** Tento mozek (počítač) přijme naměřenou hodnotu, porovná ji s požadovanou hodnotou (chceme 22 °C) a spočítá, že je nutné topit. Vygeneruje tedy povel.
3. **Akční podsystém (Aktuátor):** Na základě povelu provede fyzickou změnu v prostředí (např. sepne kotel a začne topit). Prostředí se ohřeje, senzor to znovu změří a smyčka se uzavírá.
**Úrovně řízení (zpětné vazby):
- **Operační ZV:** Nejnižší úroveň, představuje přímé technologické řízení (senzor naměří hodnotu, aktuátor provede okamžitou akci).
- **Programová ZV a Symbolická ZV (1 a 2):** Vyšší úrovně řízení pracující s predikcí, plánováním, zpracováním dat a softwarovými modely.
- **Sociální ZV:** Nejvyšší vrstva zpětné vazby, která odráží chování společnosti, ekonomické modely a interakci technologií s lidmi a trhem.
# 3. Přehled problematiky IoT, kořeny IoT a další rozvoj

Pojem **Internet of Things (IoT)** poprv´e pouˇzil v roce 1999 **Kevin Ashton** ve společnosti Procter & Gamble (a později v Auto-ID Center na MIT) v souvislosti s propojováním technologie RFID s internetem.
- Ashton si uvědomil obrovský problém: do té doby byly počítače závislé na datech, která zadávali lidé (téměř všech tehdejších 50 petabytů dat vytvořili lidé psaním, skenováním atd.). Lidé mají ale omezený čas, pozornost a přesnost.
- **Ashtonova vize:** Pokud vybavíme počítače senzory a RFID, aby o věcech věděly vše samy bez lidské pomoci, budeme moci přesně sledovat a počítat fyzické objekty, čímž se radikálně sníží plýtvání, ztráty a náklady.

K rozvoji IoT teoreticky přispěl i **William Nelson Joy (Bill Joy)**, který definoval tzv. "6 webů" vývoje internetu. Pro IoT je z nich nejdůležitější posun k **D2D (Device to Device)**, což je komunikace sítě senzorů rozmístěných v prostředí bez nutnosti lidského uživatelského rozhraní.

2. Přehled problematiky: Co je IoT dnes?

Dnes se IoT chápe jako síť jednoznačně identifikovatelných fyzických objektů a jejich virtuálních reprezentací ve struktuře internetu. Tyto "věci" používají senzory, aby vnímaly události ve fyzickém světě, a na základě těchto dat dokážou samy aktivovat akce.

V praxi se dnes IoT rozděluje do dvou hlavních směrů:

1. **Spotřebitelský internet věcí (CIoT - Consumer IoT):** Zaměřuje se na koncové uživatele, chytrou domácnost, nositelnou elektroniku (wearables) a chytré spotřebiče. Cílem je zvýšit uživatelský komfort a zjednodušit každodenní život.
2. **Průmyslový internet věcí (IIoT - Industrial IoT / Industry 4.0):** Zaměřuje se na kritické úkoly ve výrobě, energetice (Smart Grids), zdravotnictví nebo logistice. Jeho cílem je zefektivnění využívání zdrojů, prediktivní údržba, snížení provozních nákladů a zvýšení produktivity. Tento segment má do budoucna největší ekonomický potenciál.

3. Další rozvoj: Od IoT k IoE a výzvy do budoucna

Rozvoj IoT neznamená jen přidávání dalších senzorů, ale strukturální změnu celých sítí a ekonomik.

**Internet všeho (IoE - Internet of Everything) a Konvergence IT/OT:** Společnost Cisco a další lídři trhu posouvají pojem IoT k **IoE (Internet of Everything)**, který inteligentně propojuje čtyři základní pilíře: **Lidi, Procesy, Data a Věci**. Aby tento systém mohl fungovat v průmyslu, musí nutně dojít ke **konvergenci IT a OT**. To znamená spojení informačních technologií (IT – sítě, telekomunikace, servery) s operačními technologiemi (OT – hardware a software pro přímé řízení výrobních strojů a senzorů) do jedné infrastruktury.

**Technologické předpoklady a budoucí rozvoj:**

- **Adresný prostor a IPv6:** Vzhledem k odhadům, že k sítím budou připojeny desítky miliard zařízení (podle Cisca až 50 miliard), je pro další rozvoj naprostou nutností protokol **IPv6**, který poskytuje dostatečný adresní prostor (3,4×1038 adries) pro připojení jakéhokoliv předmětu na Zemi.
- **Decentralizace zpracování dat (Fog/Edge Computing):** Věci v IoT generují enormní objem tzv. Big Data. Rozvoj směřuje k tomu, že se všechna data nebudou posílat centrálně do Cloudu, ale budou se předzpracovávat lokálně přímo u zařízení (Edge computing) nebo na úrovni lokálních uzlů (Fog computing). Zabrání se tak přetížení sítí a sníží se doba odezvy.

**Klíčové výzvy dalšího rozvoje:**

- **Bezpečnost (Security):** Představuje největší výzvu. Podle průzkumů je bezpečnost hlavní obavou (téměř 57 % organizací). Zařízení IoT se často stávají snadnými terči kyberútoků (např. botnet Mirai), což si vyžádá obrovské investice do zabezpečení komunikace a identity zařízení.
- **Standardizace a interoperabilita:** Dalším problémem pro další rozvoj je, jak integrovat miliony různých zařízení od různých dodavatelů, z nichž každý používá vlastní komunikační protokoly a platformy. Neexistuje jeden univerzální standard, ale mnoho soupeřících platforem