### K čemu slouží datové typy?
Datový typ je specifikace povolených hodnot a povolených operací, které lze s těmito hodnotami provádět.
### Jaké datové typy jsou k dispozici pro číselné hodnoty?
![[Pasted image 20251107173224.png]]
![[Pasted image 20251107173304.png]]
#### Jaké aritmetické operace jsou k dispozici u číselných datových typů?
- sčítání (+), 
- odčítání (-), 
- násobení (*), 
- dělení (/), 
- celočíselné dělení (div), 
- zbytek po dělení (mod)

Datový typ => povolené hodnoty, povolené operace
##### povolený rozsah 
- **int** - 4B = 32b <-2<sup>31</sup>; 2<sup>32</sup>-1> **(Povolené hodnoty INT)**
#### Povolené operace
- int a,b ->a/b (/) **má význam celočíselného dělení**
- float (a)/b <- desetinný podíl
**Aritmetika**
- bitové operátory  & | ~ xor >> <<
### Celočíselné datové tipy
- char - 1B
- short int - 2B
- int - 4B
- long int - 4B
- long long int - 8B
**unsigned** - možnost zakázat záporná čísla
### Znakový tip
char jako chameleon někdy znakový někdy celo číselný
![[Pasted image 20251009115308.png]]
**Kiwi je nastaven na kódování UTF8**
Pro **char** = 'ahoj';
### Řídicí znaky: nemají svůj obraz, musí se zapsat náhradním způsobem:
- \n - nový řádek
- \r - první polovina konce řádku
- \t - tabulátor
Zápis čísel soustav:
- 017 - osmičková - 15
- x1a - hexa - 26
### Vstup a výstup znaků
##### Konverze
cin >> -ty >> jsou konverze, konvertují ten input 
cin.get(Z) - přečtení všech znaků na vstupu
"#" = zahrádka
##### Bool
- Logické hodnoty
- putině nečum sem
**String** - Nejedná se o klíčové slovo, jedná se o nějakou knihovnu, není int, float atd.
- string S
	-  S je to objekt ale, může se chovat jako prměná
	Řetězce se zapisují v "ahoj";
![[Pasted image 20251009121627.png]]
