## 4.1 Naming Conventions

Een **naming convention** is een standaard voor het benoemen van stukjes code zodat het duidelijk is wat je ermee doet. Elke taal of organisatie kan eigen regels hebben.

### Veelvoorkomende stijlen

- **camelCase**: meerdere woorden aan elkaar, eerste woord lowercase, de rest hoofdletters (meestal variabelen of functies).
    
- **PascalCase**: meerdere woorden aan elkaar, alle woorden beginnen met hoofdletter (meestal classes).
    
- **snake_case**: meerdere woorden met underscore gescheiden (variabelen, functies, modules).
    
- **CONSTANTS_LIST**: hoofdletters met underscore (constants).
    

### Python naming conventions

- Variabelen en functies → snake_case
    
- Constants → UPPERCASE
    

> [!tip] Tip: Volg altijd de naming conventions van de plek waar je werkt voor consistentie.

---

## 4.2 Comments

**Comments** zijn stukjes uitleg in je code die genegeerd worden door de computer.

### Waarom comments?

- Helpen jou en anderen de code te begrijpen.
    
- Documenteren logica zonder dat het effect heeft op de uitvoering.
    

### Single-line comments

```python
# Dit is een single-line comment
print("Hallo, wereld!")  # Dit is een inline comment
```

### Multi-line comments

```python
# Dit is een multi-line comment
# die meerdere regels beslaat
# om uitleg te geven over de code.
```

Of met triple quotes:

```python
"""
Dit is een multi-line string
die vaak wordt gebruikt als
documentatie of uitleg.
"""
```

> [!tip] Tip: Gebruik comments spaarzaam en duidelijk, vooral bij complexe code.

---

## 4.3 Errors

Een **error** ontstaat wanneer code niet kan uitvoeren.

### Omgaan met errors

- Ctrl + S om code op te slaan.
    
- Check altijd op errors voordat je code runt.
    
- Lees error messages: ze geven vaak precies aan wat fout gaat.
    

### Voorbeeld error

```
console.Log is not a function at BlankaBestCharacter.js:1:9
```

- Fout: 'Log' moet lowercase → 'console.log'.
    

### Try catch

Gebruik een try catch voor error handling:

```javascript
try {
    // code die kan falen
} catch (error) {
    console.log("Er ging iets mis:", error);
}
```

- `try` voert code uit.
    
- `catch` vangt errors op en laat jou bepalen wat ermee gebeurt.
    

> [!tip] Tip: Gebruik try catch bij data die je naar een database stuurt of bij externe requests.

---

## 4.4 Switch Cases

Een **switch case** is vergelijkbaar met if / else if / else statements.

```javascript
let i = 2;
switch(i) {
    case 1:
        console.log("Case 1");
        break;
    case 2:
        console.log("Case 2");
        break;
    default:
        console.log("Geen case match");
        break;
}
```

- `switch` neemt een waarde om te vergelijken.
    
- `case` definieert mogelijke waarden.
    
- `default` is zoals else, als geen case matcht.
    
- Meerdere cases kunnen dezelfde taak uitvoeren:
    

```javascript
switch(i) {
    case 1:
    case 2:
        console.log("Case 1 of 2");
        break;
}
```

> [!tip] Tip: Gebruik switch cases voor duidelijke keuzes tussen meerdere mogelijke waarden, vooral als je veel else if statements zou hebben.