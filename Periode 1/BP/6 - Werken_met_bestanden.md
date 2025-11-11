#  6.1 Werken met bestanden

In veel programma’s moet je gegevens **opslaan** of **inlezen** (zoals namen of cijfers).

---

##  Tekstbestand lezen

**Hele bestand in één keer:**
```python
with open("namen.txt", "r", encoding="utf-8") as bestand:
    inhoud = bestand.read()
print(inhoud)
```
👉 Leest alles tegelijk in.

**Regel per regel:**
```python
with open("namen.txt", "r", encoding="utf-8") as bestand:
    for regel in bestand:
        print(regel.strip())   # verwijdert \n
```

---

##  Bestanden vinden

Als het bestand niet gevonden wordt, kan Python op de verkeerde plek zoeken.

Gebruik dit om het pad automatisch te bepalen:
```python
import os

script_dir = os.path.dirname(os.path.abspath(__file__))
bestand_pad = os.path.join(script_dir, "namen.txt")
```

---

##  Tekstbestand schrijven

**Overschrijven (write):**
```python
with open("uitkomst.txt", "w") as bestand:
    bestand.write("Dit is de eerste regel\n")
    bestand.write("En dit is de tweede regel\n")
```

**Toevoegen (append):**
```python
with open("uitkomst.txt", "a") as bestand:
    bestand.write("Nog een regel\n")
```

---

##  CSV-bestanden lezen

```python
import csv

with open("cijfers.csv", "r") as bestand:
    reader = csv.reader(bestand)
    for rij in reader:
        print(rij)
```

**Voorbeeld invoer:**
```
naam,cijfer
Ali,8
Sophie,7
Eva,9
```

**Uitvoer:**
```
['naam', 'cijfer']
['Ali', '8']
['Sophie', '7']
['Eva', '9']
```

---

##  CSV-bestanden schrijven

```python
import csv

with open("resultaten.csv", "w", newline="") as bestand:
    writer = csv.writer(bestand)
    writer.writerow(["naam", "gemiddelde"])
    writer.writerow(["Ali", 7.5])
    writer.writerow(["Sophie", 8.0])
```

 Maakt een nieuw bestand met tabellenstructuur.

---

##  Fouten afvangen

Gebruik `try/except` om fouten netjes te behandelen:

```python
try:
    with open("onbestaand.txt", "r") as bestand:
        inhoud = bestand.read()
        print(inhoud)
except FileNotFoundError:
    print("Bestand niet gevonden!")

print("Programma gaat verder...")
```

 Programma crasht niet bij fouten.

---

##  Samenvatting

| Symbool | Betekenis |
|----------|------------|
| `"r"` | lezen (read) |
| `"w"` | schrijven (write, overschrijft) |
| `"a"` | toevoegen (append) |
| `csv.reader` | lezen als lijstjes |
| `csv.writer` | schrijven van tabellen |
| `try/except` | voorkomt crashes bij fouten |

---

##  Extra tip

Wil je zeker weten dat Python je bestand vindt?  
Gebruik altijd een **relatief pad** via `os.path` zoals:
```python
os.path.join(os.path.dirname(__file__), "bestand.txt")
```

---

** Klaar:** je kunt nu veilig bestanden lezen, schrijven en foutloos verwerken in Python.
