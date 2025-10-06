# Wat is een dictionary?

Een **dictionary** (dict) slaat **waardes op gekoppeld aan sleutels**.

```python
student = {
    "naam": "Thijmen",
    "leeftijd": 16,
    "opleiding": "Software Development"
}
```

## Waarden ophalen

```python
print(student["naam"])  # Thijmen
```

## Toevoegen / aanpassen

```python
student["jaar"] = 1      # nieuw item
student["leeftijd"] = 17 # aanpassen
```

## Verwijderen

```python
del student["opleiding"]
age = student.pop("leeftijd")
```

## Itereren

```python
for key, value in student.items():
    print(key, value)
```

## Handige methodes

- `dict.keys()` → lijst van sleutels
    
- `dict.values()` → lijst van waarden
    
- `dict.items()` → lijst van (sleutel, waarde) tuples
    
- `dict.get(key, default)` → waarde of default
    
- `dict.update(other_dict)` → voeg andere dict toe