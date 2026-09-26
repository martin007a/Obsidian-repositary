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