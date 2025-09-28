Základní práce se soubory a adresáři 

|        |                                                                        |                                             |
| ------ | ---------------------------------------------------------------------- | ------------------------------------------- |
| Příkaz | Popis                                                                  | Příklad                                     |
| ls     | vypíše obsah adresáře                                                  | ls -l (detailní výpis)                      |
| pwd    | ukáže aktuální cestu                                                   | pwd                                         |
| cd     | změní adresář                                                          | cd /home/xslavice                           |
| mkdir  | vytvoří nový adresář                                                   | mkdir projekty                              |
| rmdir  | smaže prázdný adresář                                                  | rmdir staradir                              |
| tree   | zobrazí strom adresářů (musí být nainstalováno: sudo apt install tree) | tree ~/Dokumenty                            |
| find   | hledání souborů                                                        | find . -name "*.txt" (v aktuálním adresáři) |

Práce se soubory 

| Příkaz | Popis                    | Příklad                   |
| ------ | ------------------------ | ------------------------- |
| touch  | vytvoří prázdný soubor   | touch poznámky.txt        |
| cp     | kopírování               | cp poznámky.txt /tmp/     |
| mv     | přesun nebo přejmenování | mv poznámky.txt notes.txt |
| rm     | smaže soubor             | rm notes.txt              |

Síťové příkazy (pro připojení na server) 

|   |   |   |
|---|---|---|
|Příkaz|Popis|Příklad|
|ssh|připojení na vzdálený server|ssh [xslavice@kiwi.mendelu.cz](mailto:xslavice@kiwi.mendelu.cz)|
|scp|kopírování souborů mezi PC a serverem|scp soubor.txt [xslavice@kiwi.mendelu.cz:~/](mailto:xslavice@kiwi.mendelu.cz:~/) (pošle soubor na server do domovského adresáře)|

Připojení disku na virtuální PC (asi) 

PuTTY 

[xslavice@.kiwi.mendelu.cz](mailto:Xslavice@.kiwi.mendelu.cz) 

odhlášení  

www.thala.cz/navody/joe/civiceni-joe-navod.pdf