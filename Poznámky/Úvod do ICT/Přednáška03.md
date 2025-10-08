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
- 0