## Uvod - Martin
Dobrý dobrý den já jsem Martin S. a toto je můj kolega Samuel Prudký a mi vám odprezentujeme náš projekt.
V rámci našeho projektu jsme dostaly za úkol vymyslet ERD model pro hororovou  RPG hru tajemný hrad v Karpatech. 
## obsah
V naší prezentaci se budeme zaobírat několika ti body
	V první části probereme problematikou naší týmové spolupráce
	 Dále se budeme zabývat entitami a s nimi spojeným maticovým digramem
	A nakonec se podíváme na samotný ERD 
## **Spolupráce** - Samuel
Prvním krokem při zpracování našeho projektu bylo to že jsem se museli domluvit na tom jak budeme  fungovat jako tým. Jelikož nebydlíme ve stejném městě, rozhodli jsme se že veškerou naši týmovou komunikaci budeme řešit online VIA aplikaci discord, kde jsem buď přes audio hovory či chat řešili vše ohledně projektu.  
## Maticový diagram
Po přečtení zadání a nalezení entit které z něj vyplívaly, jsem si potřebovali nějak udělat pořádek v entitách a vtazích mezi nimi. Pro jsme se rozhodli zpracovat Maticový diagram, který jsem vypracovaly za pomoci aplikace Microsoft Exel.
**Samuel**
## ERD - Martin
Když jsem měli již nějakou představu toho jak jednotlivé entity spolu souvisí mohli jsem se pustit do ERD.  
Jelikož zadaní jako takové nám připadalo dosti komplexní tak jsem se rozhodli že celí problém rozdělíme na menší celky.
## Klik 
Prvním takovým celkem je Entita úroveň a entity sní spojené. Ta představuje jednotlivá kola hry, každá úroveň má jednu nebo více místností z toho jedna je v té úrovni poslední a nachází se v ní boss. Samotná místnost má nějaký typ prostředí který definuje její vzhled, muže se v ní nacházet nějaká nástraha určitého typu. Dále se v místnosti nachází nějaká kořist která může obsahovat nějaké peníze, léčiva či artefakty. Každá míst má jeden klíč do další místnosti, avšak tento klíč vlastní jedno ze strašidel v ni, tuto skutečnost řešíme přes tabulku klíč k místnosti, která zaznamenává které strašidlo to je. 
## Klik - Samuel
To nás přesouvá k entitě strašidlo ta představuje to určité strašidlo v místnosti každé strašidlo má svůj druh který ho specifikuje. Jelikož strašidlo může být boss, což je strašidlo s výší odolností tak druh má atribut je boss. 
Každé strašidlo má své dvě specifické schopnosti. tyto specifické schopnosti slouží k tomu, že pokud postava, která má 3 specifické schopnosti, má nějaké společné se strašidlem tak se mu sníží jeho odolnost.  U bosse je omezení že mohou mít pouze 1 společnou specifickou schopnost. Což nás přivádí k samotné postavě. 
## Klik - Martin
Hratelná postava je taková šablonová entita, která v sobě drží maximální hodnoty atributů hráče které mohu být postupem času ovlivněny jejími zkušenostmi. Dále je tu entita hráč,, která představuje samotného hráče, který může mít více postav. Každá postava má nějakou třídu, která určuje její herní styl. Zároveň je postava spojena přes entitu souboj se strašidlem , která představuje záznam o tom že spolu postava a strašidlo bojovali. **Martin**
## Klik
V zadání bylo také zmíněno, že si potřebujeme ukládat údaje o postavě na začátku a konci kola. Což řešíme přes entitu uložení. Ta má atributy kolo uložení a fáze kola, které určují blížíš informace. Dále uložení má nějaký stav postavy, kde si ukládáme stav postavy v dané chvíli. taktéž má i  stav inventáře, kde je například množství dukátů, artefakty, či léčiva.  
## Klik - Samuel
Dále máme entitu artefaktu, která má nějakou schopnost,  v zadání zmíněno že artefakt můžeme na konci kola prodat na trhu proto má artefakt atribut určující jeho hodnotu. Specifická pro tuto entitu je zde oblouková vazba, která říká, že buď je artefakt v kořisti a nebo v inventáři. Dále je v zadání specifikováno to, že v místnosti se mohou nacházet lékárničky či si ve špitálu můžeme nakoupit další léčiva, co že řešeno přes atribut cena. zároveň léčivo má atribut účinnost která specifikuje jeho schopno zlepšovat zdravotní stav. Specifická léčiva jsou ukládána do balíčku s léčivem neboť můžeme mít víc léčiv stejného druhu, na rozdíl od artefaktů. A balíček má také obloukovou vazbu které specifikuje jeho příslušnost buď k inventáři nebo kořisti. **Samuel**
## Klik
Tímto jsem se dostaly k závěru naší prezentace, myslíme si že nám projekt pomohl k lepšímu pochopení toho jak tvořit ERD.  Poluď máte nějaké dotazy?


