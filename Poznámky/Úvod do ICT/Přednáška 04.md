### Vnitřní reprezentace dat II
#### Znaky v Pc 
Každému znaku je přiřazeno jedno číslo

**Znakům je nutné přidělit číselné kódy podle tabulek** 
- **jednobajtové** – EBCDIC, ASCII 
- **vícebajtové** – UCS, Unicode, UTF
**Zobrazitelné znaky** 
- slouží pro zápis textové informace 
- písmena, číslice, interpunkční znaménka, matematické symboly a další znaky vyjádřené textově
**Řídicí znaky** 
- netisknutelné znaky (enter. atd.)
- slouží k ovládání přídavných zařízení nebo programu 
- přechod na nový řádek, tabulátor apod.
### ASCII
**American Standard Code for Information Interchange (1968)**
- Kódovací prostor 8 bitů – lze rozlišit 256 znaků
- původně 7 bitů + 1 paritní bit pro kontrolu 
- každý znak je uložen na 8 bitech
**Rozložení Kódu**
- **řídicí znaky** – #0 až #31, #127 
- **zobrazitelné znaky** – #32 až #126, #128 až #255
![[Pasted image 20251015152725.png]]
![[Pasted image 20251015152942.png]]
### ASCII – rozšířená část
- národní znaky
![[Pasted image 20251015153245.png]]
## Varianty kódování českých nár. znaků
### Kód bratrů Kamenických
- jiné označení: MJK, KEYBCS2, CP895 
- pro osobní počítače s operačním systémem MS-DOS 
- využití sady CP437 z IBM PC 
- náhrada pozic #128 až #171 českými a slovenskými národními znaky
#### PC Latin 2
- jiné označení: IBM Latin 2, CP852 
- pro osobní počítače s operačním systémem MS-DOS 
- podpora středoevropských jazyků používajících latinku (albánština, čeština, slovenština, polština, rumunština, maďarština, srbochorvatština aj.)
#### KOI-8 ČS2
- Код Обмена Информацией, 8 бит 
- vyvinut v SSSR v rámci RVHP, ČSN 36 9103
### ISO Latin 2
- jiné označení: ISO 8859-2 
- podpora středoevropských a východoevropských jazyků psaných latinkou nebo latinskou transkripcí 
- použitelné i pro němčinu a finštinu
- Standart pro Unixové servery (historicky)
Windows-1250
- jiné označení: CP1250 
- pro operační systém Windows 
- podpora středoevropských jazyků a němčiny 
- velmi podobné kódu ISO 8859-2
 ![[Pasted image 20251015153827.png]]
### Když ASCII přestává stačit
Ke konci 80. let 20. století přichází první potíže - 256 nestačí
### Hledání nových možností
- Standard **USC** (ISO 10646)
	- 31 bitů
	- většina používaných znaků je umístěna na prvních 65 536 pozicích (16 bitů) – Basic Multilingual Plane
- Standard **Unicode**
### Kompatibilita
U+0000 až U+007F ∼ základní kód ASCII 
U+0000 až U+00FF ∼ ISO 8859-1
![[Pasted image 20251015154452.png]]
## UTF
- 32 bit
	-  každý znak reprezentován 32bitovým číslem
	- nevýhoda velká neuspornost
* 16bit
	* v C
- 8bit
	- velikost proměnlivá, znak zabere tolik kolik potřebuje
	- každý znak zabere 2B, slováci - 3B jen kvůli euru 
	- Odstraňuje nevýhody kódu Unicode 
	- zpětná kompatibilita s ASCII 
	- nejsou problémy s endianitou
**BOM – Byte Order Mark**
![[Pasted image 20251015155316.png]]
- u UTF-8 je nepovinná
![[Pasted image 20251015155340.png]]

