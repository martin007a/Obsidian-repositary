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
