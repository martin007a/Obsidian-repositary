# Vnitřní reprezentace dat I
### Binární řádová mřížka
![[Pasted image 20251008151825.png]]
- **jednotka** jde zobrazit
- **modul** nejde zobrazit
![[Pasted image 20251008152055.png]]
### Přetečení a podtečení
Pokud je délka mřížky menší než počet cifer čísla 𝐴, číslo nebude zobrazitelné.
- do mřížky nebude možné uložit všechny číslice čísla 𝐴 
- řády, které se nevejdou, budou ignorovány
Dojde k **přetečení** a následné ztrátě přesnosti v reprezentaci čísla
![[Pasted image 20251008152500.png]]
### Ztráta přesnosti v praxi
![[Pasted image 20251008152638.png]]
### Terminologie
![[Pasted image 20251008152713.png]]
## Celá čísla
- Operační paměť počítače je rozdělena do adresovatelných jednotek velikosti slabiky (bajtu)
2 Ve dvojkové soustavě = 10.
Pozor v pc potřebuji vědět na kolika Bitech je zobrazeno
![[Pasted image 20251008152801.png]]
## Celočíselné datové typy
![[Pasted image 20251008153019.png]]
![[Pasted image 20251008153056.png]]
### Celá čísla bez znaménka
Zobrazení bez úprav na vymezeném prostoru 𝑛 bitů
![[Pasted image 20251008153146.png]]
### Celá čísla se znaménkem
Standardní polyadické číselné soustavy pouze pro zobrazení nezáporných čísel
Zobrazení záporných čísel pomocí **číselných kódů**
- přímý kód (sign magnitude) 
- inverzní kód (one’s complement) 
- doplňkový kód (two’s complement) 
- aditivní kód (biased)
Prakticky všechny operace na moderních počítačích založeny na reprezentaci doplňkovým kódem
- hardware je rychlejší 
- hardware je jednodušší (a tím i rychlejší)
### Přímý kód
Pro člověka jediná čitelná forma rozlišování mezi kladnými a zápornými čísly
- Hardware by byl ale pomalý a zbytečně složitý
**Princip**: použití nejvyššího řádu mřížky pro reprezentaci znaménka (tzv. znaménkový bit)
- 0 reprezentuje kladné číslo
- 1 reprezentuje záporné číslo
![[Pasted image 20251008153641.png]]
![[Pasted image 20251008153654.png]]
problémy 0 != -0
### Inverzní kód
Z historického hlediska velmi důležitý kód
Dnes neexistuje stroj pracující v tomto kódu  
- ale potřebujeme jej při zobrazení v doplňkovém kódu
#### Princip
- kladná čísla reprezentujeme beze změny 
- u záporných čísel najdeme doplněk všech řádů do jedničky (**doplňkem** 0 je 1, doplňkem 1 je 0)
![[Pasted image 20251008153949.png]]
### Doplňkový kód
Varianta inverzního kódu bez dvojí reprezentace nuly – hardware proto může pracovat rychleji
#### Princip
- kladná čísla reprezentujeme beze změny 
- u záporných čísel nalezneme jedničkový doplněk a k výsledku přičteme 1
![[Pasted image 20251008154101.png]]
### Aritmetické operace v doplňkovém kódu
![[Pasted image 20251008154424.png]]
![[Pasted image 20251008154434.png]]
-26 = 230
		256 - 26
			2<sup>8</sup>
-128 __ 127
### Aditivní kód
![[Pasted image 20251008155057.png]]
