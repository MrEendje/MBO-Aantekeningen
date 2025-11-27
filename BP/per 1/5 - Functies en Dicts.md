## 5.1 Functies

Functies zijn blokken code die je kunt hergebruiken. Hierdoor hoef je dezelfde code niet meerdere keren te schrijven.

### Functie zonder parameters

```python
def begroet():
    print("Hallo student!")
    
begroet()   # roept de functie aan
```

- **Voordeel:** als je 10 keer iemand wilt begroeten, hoef je de code maar één keer te schrijven.
    

### Functie met parameters

Parameters zijn waarden die je meegeeft aan een functie.

```python
def begroet_persoon(naam):
    print("Hallo " + naam + "!")
    
begroet_persoon("Ali")
begroet_persoon("Sophie")
```

- `naam` is de parameter. Elke keer dat je de functie aanroept, kun je een andere waarde meegeven.
    

### Functie met return value

Met `return` kun je een waarde teruggeven die je verder kunt gebruiken.

```python
def bereken_oppervlakte(breedte, hoogte):
    return breedte * hoogte

uitkomst = bereken_oppervlakte(5, 10)
print("Oppervlakte =", uitkomst)
```

- De functie geeft een waarde terug die je kunt opslaan in een variabele.
    

> [!tip] Tip: Gebruik functies om je code overzichtelijk en herbruikbaar te maken.

---

## 5.2 Dictionaries

Een dictionary is een soort lijst, maar met **sleutel–waarde paren**.

### Voorbeeld

```python
student = {
    "naam": "Eva",
    "leeftijd": 20,
    "opleiding": "Informatica"
}

print(student["naam"])       # Eva
print(student["leeftijd"])   # 20
```

- Je gebruikt **sleutels** om de juiste waarde te vinden.
    

### Dictionary aanpassen

```python
student["leeftijd"] = 21      # waarde wijzigen
student["cijfer"] = 8.5       # nieuwe sleutel + waarde toevoegen

print(student)
```

### Functies en Dictionaries combineren

Functies zijn handig om dictionaries te bewerken.

```python
def voeg_cijfer_toe(student, vak, cijfer):
    student[vak] = cijfer
    return student

leerling = {"naam": "Ali"}
leerling = voeg_cijfer_toe(leerling, "wiskunde", 7.5)

print(leerling)
```

- De functie voegt een vak en cijfer toe aan de dictionary en geeft de nieuwe dictionary terug.
    

### Gemiddelde berekenen met een functie

```python
def gemiddelde(student):
    totaal = 0
    aantal = 0
    for vak, cijfer in student.items():
        if vak != "naam":   # naam overslaan
            totaal += cijfer
            aantal += 1
    return totaal / aantal

leerling = {"naam": "Sophie", "wiskunde": 8, "engels": 7}
print("Gemiddelde =", gemiddelde(leerling))
```

- De functie doorloopt alle cijfers en geeft het gemiddelde terug.
    

> [!tip] Tip: Combineer functies met dictionaries om data efficiënt te verwerken en herbruikbare code te schrijven.