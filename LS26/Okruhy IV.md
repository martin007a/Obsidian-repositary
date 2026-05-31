---
tags: [IoT, zkouska, internet_veci, skripta]
aliases: [Okruhy ke zkoušce IoT]
---

# Okruhy ke zkoušce: Internet věcí (IoT)

## 1. Trendy digitalizace a řízení, automatizace a sítě kolem nás
* Očekává se, že do roku 2020 bude v síti IoT připojeno téměř 26 miliard zařízení, přičemž některá data uvádí i více než 30 miliard bezdrátově připojených zařízení[cite: 2].
* Digitalizace (neboli digitální transformace) je proces, při kterém se celá organizace stává digitální a dochází k přesunu všech operací a procesů do digitálního provozního modelu[cite: 2].
* Sítě tvoří absolutní základ pro IoT, přičemž se vyvíjejí od jednoduchých domácích sítí pro sdílení prostředků až po obrovské podnikové či globální konvergované sítě[cite: 2].
* Konvergované sítě jsou schopné na jedné platformě přenášet hlas, video, text i grafiku[cite: 2].
* Automatizace domácnosti (domotics) má 5 úrovní: od domů s izolovanými chytrými objekty, přes komunikující objekty, připojené domy s vnější sítí, učící se domy (predikce chování na základě dat) až po pozorný dům, který neustále registruje aktivity osob[cite: 2].

## 2. Průmyslové revoluce z pohledu kybernetiky a řízení
* První průmyslová revoluce (18. a 19. století) znamenala změnu z agrární společnosti na industrializovanou, a to především díky vynálezu parního stroje[cite: 2].
* Druhá průmyslová revoluce byla poháněna elektřinou a zahrnovala rozšiřování průmyslu a masové výroby[cite: 2].
* Třetí průmyslová revoluce (tzv. digitální revoluce) odstartovala v polovině 20. století a zahrnovala vývoj počítačů a informačních technologií (IT)[cite: 2].
* Čtvrtá průmyslová revoluce (Industry 4.0) je současná éra, ve které technologie jako IoT, robotika, umělá inteligence (AI) a virtuální realita od základu mění způsob života a práce[cite: 2].
* Čtvrtá revoluce roste ze třetí, ale odlišuje se obrovskou rychlostí technologických průlomů a všudypřítomností obrovských systémů[cite: 2].

## 3. Přehled problematiky IoT, kořeny IoT a další rozvoj
* Termín "Internet věcí" (IoT) byl poprvé navržen Kevinem Ashtonem v roce 1999[cite: 2].
* Bill Joy popsal komunikaci D2D (Device to Device) jako "Internet senzorů" rozmístěných v systémech pro maximální účinnost a strojovou inteligenci v běžném životě[cite: 2].
* Kořeny IoT leží primárně v telemetrii (technologie pro měření na dálku a bezdrátový přenos dat) a telematice (spojení telekomunikací a informatiky pro přenos dat v reálném čase)[cite: 2].
* Základní koncept "Internet of Everything" (IoE) se skládá ze čtyř vzájemně propojených prvků: Lidé (People), Procesy (Process), Data (Data) a Věci (Things)[cite: 2].

## 4. Porovnání struktury IoT (4.PR) a struktury ASŘ (3.PR)
* Tradiční systémy (tzv. operační technologie - OT) představovaly průmyslovou infrastrukturu kontroly a automatizace, kde probíhala komunikace převážně mezi stroji[cite: 2].
* S nástupem IoT dochází k nutné konvergenci operačních technologií (OT) s informačními systémy (IT), což umožňuje vznik čtvrté průmyslové revoluce[cite: 2].
* Konvergence IT a OT umožňuje organizacím zjednodušit infrastrukturu (snížení provozních nákladů) a vytvořit inteligenci a agilitu pomocí analytických nástrojů[cite: 2].
* Integrace obou struktur vyžaduje řešení komplexní bezpečnosti, protože konvergovaná infrastruktura musí chránit jak fyzické stroje, tak data před kybernetickými útoky[cite: 2].

## 5. Signály, jejich typy, vzorkování a kvantování
* Senzor převádí sledovanou fyzikální, chemickou nebo biologickou veličinu na měřitelnou výstupní veličinu, kterou je nejčastěji analogový nebo digitální elektrický signál[cite: 2].
* Získaný signál je nutné upravit pro optimalizaci přenosu informace, což zahrnuje kroky: zesílení (zvýšení amplitudy), filtrování (odstranění nevýznamných částí a šumu), modulaci a demodulaci[cite: 2].
* Analogový signál je následně transformován na digitální pomocí AD (analogově-číslicového) převodníku, který je součástí měřicího řetězce[cite: 2].
* Pokud systém zpracovává více signálů ze sítě senzorů, využívá se multiplexování, například prostorový multiplex (SDM) nebo časový multiplex (TDM), kdy je jeden AD převodník společný pro všechny senzory[cite: 2].
* Ke správnému časovému sladění signálů při vzorkování se využívá funkce zádrže (sample-hold), která naměřená data krátkodobě uloží do analogové paměti (např. kondenzátoru)[cite: 2].

## 6. Senzory a senzorové klastry v IoT
* Z hlediska abstrakce IoT je senzor označován jako "Primitivum 1", přičemž jeho úkolem je generovat data (např. o teplotě, váze, přítomnosti) z fyzikálního prostředí[cite: 2].
* Senzory mohou disponovat pouze omezeným výpočetním výkonem, avšak mohou mít přidělenou identitu (Device_ID) a sledovat informace o svém vlastníkovi a poloze[cite: 2].
* Klastr (Senzorový klastr) je abstraktní seskupení senzorů, které mohou vznikat ad-hoc nebo podle pevných pravidel a sdílejí výstupní data[cite: 2].
* Jeden klastr ($C_{i}$) sestává z dat od mnoha různých (i nehomogenních) senzorů, přičemž jeden senzor může teoreticky sdílet svá data s vícero klastry současně[cite: 2].
* Data ze senzorových klastrů jsou odesílána "agregátorům", což je Primitivum 2, které data komprimuje, průměruje a jinak zpracovává[cite: 2].
* 