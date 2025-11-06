### Datový typ **void**
- „prázdný“ typ, nemá žádné hodnoty
#### Podprogram
Pojmenované logické části programu; často jako metody objektů, součásti knihoven
- Procedura -  
- Funkce
## Výstupní manipulátory
<< operátor výstupního proudu
- showpos / noshowpos - zobrazí / nezobrazí znaménko
- endl
- left/right - zarovnání vlevo/vpravo
- dec/oct/hex - cislo v dek./okt,
- fixed/scientific - zobrazení reálných čísel
- uppercase/nouppercase - zobrazení velkých čísel
nPro následující manipulátory je nutné použít knihovnu: 
`#include`
`<iomanip>`
- nsetprecision(p) – přesnost rac. čísel
- nsetw(n) – šířka výstupu na n znaků
- nsetfill(c) – výplňový znak c místo mezer
13.5e<sup>-10</sup>
### Vstupy
- **cin.get(c)** – čtení jednoho znaku bez přeskakování bílých znaků
- **cin.getline(S, 10)** – čtení řetězce (ne typ string!)
- **cin.getline(S, 10, ':')** – čtení řetězce po oddělovač
- **cin.eof()** – test konce vstupu
- **cin.setf(ios::boolalpha)** – vstup true/false(totéž lze i u cout)
- **cin.unsetf(ios::skipws)** – nepřeskakování bílých znaků ve vstupu