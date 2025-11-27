# Arrays in JavaScript

## Wat is een array?

- Een array is een **geordende rij van waarden**.
    
- Voorbeelden: rij zonnepanelen, spelers in een team, soorten chips.
    
- Virtueel elke programmeertaal ondersteunt arrays.
    

## Waarom een array gebruiken?

- Handig om meerdere waarden in één variabele op te slaan.
    
- Voorbeeld: alle personen in regio Utrecht opslaan in één array in plaats van 100+ variabelen.
    

## Syntax in JavaScript

- Arrays gebruik je met **square brackets [ ]**.
    

```javascript
let fruits = ["Apple", "Banana", "Lemon", "Orange", "Grape"];
```

- Je kunt meerdere datatypes in één array hebben (JavaScript is dynamic typed).
    

## Array Indexing

- Elke waarde in een array heeft een **index**, beginnend bij 0.
    
- Voorbeeld met `fruits`:
    

```
0: Apple
1: Banana
2: Lemon
3: Orange
4: Grape
```

- Toegang tot een waarde via index:
    

```javascript
console.log(fruits[2]); // Lemon
```

## Array.length

- Geeft het aantal items in de array.
    

```javascript
console.log(fruits.length); // 5
```

- Handig voor loops:
    

```javascript
for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
```

## Array.sort

- Sorteert de items in een array.
    

```javascript
fruits.sort();
console.log(fruits); // ["Apple", "Banana", "Grape", "Lemon", "Orange"]
```

- Je kunt ook een custom sortering meegeven via een functie.
