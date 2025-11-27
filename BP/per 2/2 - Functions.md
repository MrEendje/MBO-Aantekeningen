# Functions in JavaScript

## Wat is een function?

- Een function is een stuk code dat een taak uitvoert.
    
- Ook wel 'method' genoemd.
    
- Functies zorgen ervoor dat je code netjes opgedeeld wordt in kleine taken.
    

## Callen van een function

- Je roept een function aan met de syntax: `functieNaam()`
    
- Gebruik camelCase voor function namen.
    
- Voeg altijd haakjes `()` toe.
    

Voorbeeld:

```javascript
moveForward();
jump();
playSFX();
```

## Parameters en arguments

- **Parameters:** variabelen die een function kan gebruiken.
    
- **Arguments:** waarden die je meegeeft bij het aanroepen.
    

Voorbeeld:

```javascript
moveForward(3);
jump(jumpHeight);
playSFX("explosion1.ogg");
```

- Meerdere parameters scheid je met een **komma (,)**
    

## Functions maken

- Keyword **function** gevolgd door naam en **()**
    
- Taken staan tussen **{ }**
    
- Functie kan een **return** value hebben
    

Voorbeeld met return:

```javascript
function testFunction(a, b) {
    return a * b;
}
let result = testFunction(5, 10);
console.log(result); // 50
```

## Parameters binnen functions

- Parameters zijn variabelen die alleen binnen de functie gebruikt worden.
    
- Meerdere parameters scheid je met een komma.
    

Voorbeeld:

```javascript
function gebruikInvoer(a, b, c) {
    console.log(a+b);
    console.log(b-c);
    console.log(a*c);
}
```