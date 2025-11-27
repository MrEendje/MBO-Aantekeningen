# Ultimate Git Guide – Beginners tot Advanced

Git is een versiebeheersysteem waarmee je code kunt bijhouden, samenwerken en fouten terugdraaien.

---

## 1. Basis Git Concepten

- **Repository (repo)**: De map met je project waar Git alles bijhoudt.
    
- **Commit**: Een momentopname van je project.
    
- **Branch**: Een aparte versie van je code om te experimenteren zonder de hoofdcode te breken.
    
- **Merge**: Het samenvoegen van branches.
    
- **Remote**: Externe repository (bijv. GitHub).
    
- **Clone**: Kopie van een remote repository op je lokale computer.
    

> [!tip] Tip: Denk aan Git als een tijdmachine voor je code. Elke commit is een checkpoint.

---

## 2. Basis Commando's

### Repository maken

```bash
git init
```

- Maakt een nieuwe Git repository in de huidige map.
    

### Huidige status bekijken

```bash
git status
```

- Laat zien welke bestanden veranderd zijn en welke nog gecommit moeten worden.
    

### Wijzigingen toevoegen

```bash
git add bestandsnaam
git add .
```

- `git add bestandsnaam`: voegt één bestand toe.
    
- `git add .`: voegt alle gewijzigde bestanden toe.
    

### Committen

```bash
git commit -m "Commit message"
```

- Slaat de veranderingen op met een beschrijving.
    

> [!tip] Tip: Gebruik duidelijke commit messages, bv. `Change: login functie toegevoegd`.

### Log bekijken

```bash
git log
```

- Toont alle commits van de huidige branch.
    
- Gebruik `q` om te stoppen met log bekijken.
    

### Branches maken en wisselen

```bash
git branch nieuwe-branch
git checkout nieuwe-branch
```

- `branch`: maakt een nieuwe branch.
    
- `checkout`: switcht naar een andere branch.
    

> [!tip] Shortcut: `git checkout -b nieuwe-branch` maakt én switcht in één keer.

### Branch samenvoegen (Merge)

```bash
git checkout main
git merge nieuwe-branch
```

- Merged de wijzigingen van `nieuwe-branch` naar `main`.
    

### Remote repository koppelen

```bash
git remote add origin URL
```

- Koppelt je lokale repo aan een remote repo (bijv. GitHub).
    

### Pushen naar remote

```bash
git push -u origin main
```

- Stuurt je lokale commits naar de remote repository.
    

### Pullen van remote

```bash
git pull
```

- Haalt de laatste wijzigingen van de remote branch binnen.
    

---

## 3. Handige Trucs & Tips

### Wijzigingen ongedaan maken

```bash
git checkout -- bestandsnaam
git reset HEAD bestandsnaam
```

- `checkout --`: zet een bestand terug naar de laatste commit.
    
- `reset HEAD`: verwijdert het bestand uit de staging area.
    

### Wijzigingen samenvoegen met rebase

```bash
git rebase main
```

- Zet je branch bovenop de laatste commit van main.
    
- Houdt de geschiedenis overzichtelijk.
    

### Stash gebruiken

```bash
git stash
git stash apply
```

- Tijdelijk je wijzigingen opslaan zonder te committen.
    
- `apply` brengt ze terug.
    

### Verwijderen van bestanden uit Git

```bash
git rm bestandsnaam
git commit -m "Verwijderd bestandsnaam"
```

### Diff bekijken

```bash
git diff
```

- Laat zien wat er veranderd is sinds de laatste commit.
    

### Reset naar vorige commit

```bash
git reset --hard HEAD~1
```

- Zet je project terug naar de vorige commit.
    

> [!tip] Tip: Gebruik `git reset --hard` voorzichtig, want veranderingen gaan verloren.

### Tags maken

```bash
git tag v1.0
git push origin v1.0
```

- Voor het markeren van releases of belangrijke punten.
    

### Shortcuts & Tips

- `git checkout -b <branch>` → maakt en switcht tegelijk.
    
- `git add .` → alles toevoegen.
    
- `git log --oneline --graph --all` → compacte en visuele commit geschiedenis.
    
- `git commit --amend` → laatste commit aanpassen.
    
- `git diff` → veranderingen bekijken voor commit.
    
- Altijd regelmatig committen, kleine stappen zijn beter dan grote.
    

---

> [!tip] Tip: Denk aan Git als een superkracht voor samenwerking. Zelfs als je alleen werkt, helpt het om fouten te herstellen en geschiedenis bij te hou