# 1. Přesun do složky projektu

```
cd "C:/cesta/k/projektu"
```
# 2. Inicializace a první commit (nutné před nahráním!)

```
git init
```
```
git add .
```
```
git commit -m "Initial commit"
```
# 3. Založení repozitáře na GitHubu a okamžitý push
```
gh repo create nazev-projektu --public --source=. --push
```
* popř. --source="cesta"
### Zjištění stavu (co je změněno / nepřidáno)
```
git status
```
### Příprava souborů k uložení
```
git add .                  # Přidá vše
```
```
git add cesta/k/souboru    # Přidá jen konkrétní soubor
```

### Uložení snímku do historie
```
git commit -m "Popis provedených změn"
```
### Odeslání do vzdáleného repozitáře na GitHub
```
git push origin main
```
### Vytvoření nové větve a rovnou přepnutí do ní
```
git switch -c nova-funkce
```
### Přepnutí do existující větve
```
git switch main
```

### Výpis všech lokálních větví
```
git branch
```

### Odeslání nové větve na GitHub (poprvé)
```
git push -u origin nova-funkce
```
# 5.Stažení nejnovějších změn z GitHubu do tvého PC

```
git pull
```

### Naklonování cizího/existujícího repozitáře k sobě na disk
```
git clone https://github.com/uzivatel/repo.git
```

### Stažení do konkrétně pojmenované složky
```
git clone https://github.com/uzivatel/repo.git moje-slozka
```
# Užitečná nastavení a řešení zádrhelů
```
gh auth login
```
# Ruční propojení na GitHub (pokud nepoužiješ `gh repo create`)
```
git branch -M main
```
```
git remote add origin https://github.com/uzivatel/repo.git
```
```
git push -u origin main
```
# Miltiplatform prace na projektu v C++
### Varianta A: Když projekt stahuješ z GitHubu (Doporučeno)
1. **Otevři terminál na Macu** a přejdi do složky, kam chceš projekt umístit:
    Bash:
    ```
    cd ~/Documents
    ```
2. **Naklonuj repozitář:**
    Bash:
    ```
    git clone https://github.com/tve-jmeno/Fotbalek.git
    cd Fotbalek
    ```
3. **Vygeneruj Xcode projekt přímo vedle zdrojáků:**
    Bash:
    ```
    cmake -G Xcode .
    ```
4. **Otevři projekt:**
    Bash:
    ```
    open Fotbalek.xcodeproj
    ```
### Varianta B: Když máš projekt jako ZIP soubor
1. **Rozbal ZIP archiv** (dvojklikem ve Finderu).
2. **Otevři terminál** v dané rozbalené složce:
    - Nejjednodušší: do terminálu napiš `cd` (s mezerou) a přetáhni rozbalenou složku z Finderu přímo do okna terminálu, pak stiskni `Enter`.
3. **Zkontroluj přítomnost `CMakeLists.txt`:**
    Bash:
    ```
    ls
    ```
    _(Pokud soubor vidíš ve výpisu, stojíš ve správném kořenu)._
4. **Vygeneruj a otevři Xcode projekt:**
    Bash
    ```
    cmake -G Xcode .
    open Fotbalek.xcodeproj
    ```
### Co udělat v Xcode (platí pro obě varianty)
Jakmile se Xcode otevře:
1. **Přepni cíl (schéma):**
    Nahoře uprostřed v okně Xcode je vedle tlačítek Play a Stop rozbalovací nabídka. Zřejmě tam bude svítit `ALL_BUILD`.
    - **Klikni na ni a vyber `Fotbalek`.**
2. **Spusť aplikaci:**
    - Klikni na tlačítko **Play** (nebo stiskni klávesovou zkratku `Cmd + R`).
    - Aplikace se zkompiluje a výstup (konzole) se zobrazí ve spodním panelu Xcode.