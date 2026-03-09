## Uvod
Dobrý dobrý den já jsem Martin S. a toto je můj kolega Samuel Prudký a mi vám odprezentujeme náš projekt.
V rámci našeho projektu jsme dostaly za úkol vymyslet ERD model pro hororovou  RPG hru tajemný hrad v Karpatech. 
## obsah
V naší prezentaci se budeme zaobírat několika ti body
	V první části probereme problematikou naší týmové spolupráce
	 Dále se budeme zabývat entitami a s nimi spojeným maticovým digramem
	A nakonec se podíváme na samotný ERD 
**Spolupráce**
Prvním krokem při zpracování našeho projektu bylo to že jsem se museli domluvit na tom jak budeme  fungovat jako tým. Jelikož nebydlíme ve stejném městě, rozhodli jsme se že veškerou naši týmovou komunikaci budeme řešit online VIA aplikaci discord, kde jsem buď přes audio hovory či chat řešili vše ohledně projektu.  
## Maticový diagram
Po přečtení zadání a nalezení entit které z něj vyplívaly, jsem si potřebovali nějak udělat pořádek v entitách a vtazích mezi nimi. Pro jsme se rozhodli zpracovat Maticový diagram, který jsem vypracovaly za pomoci aplikace Microsoft Exel.
## ERD
Když jsem měli již nějakou představu toho jak jednotlivé entity spolu souvisí mohli jsem se pustit do ERD.  
Jelikož zadaní jako takové nám připadalo dosti komplexní tak jsem se rozhodli že celí problém rozdělíme na menší celky.
## Klik
Prvním takovým celkem je Entita úroveň a entity sní spojené. Ta představuje jednotlivá kola hry, každá úroveň má jednu nebo více místností z toho jedna je v té úrovni poslední a nachází se v ní boss. Samotná místnost má nějaký typ prostředí který definuje její vzhled, muže se v ní nacházet nějaká nástraha určitého typu. Dále se v místnosti nachází nějaká kořist která může obsahovat nějaké peníze, léčiva či artefakty. Každá míst má jeden klíč do další místnosti, avšak tento klíč vlastní jedno ze strašidel v ni, tuto skutečnost řešíme přes tabulku klíč k místnosti, která zaznamenává které strašidlo to je.
## Klik
To nás přesouvá k entitě strašidlo ta představuje to určité strašidlo v místnosti každé strašidlo má svůj druh který ho specifikuje. Jelikož strašidlo může být i boss


* Tvorba maticového diagramu Samuel
* začátek se ERD Martin
	* rozdělení na menší celky Samuel/ Martin ?
* Problémy kterým jsem musely čelit. Samuel
* závěr, co jsem si odnesly z tvorby tohoto projektu Samuel