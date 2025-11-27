## Inleiding

Een loop is een stuk code dat zichzelf herhaaldelijk uitvoert. Loops zijn handig wanneer je een taak meerdere keren wilt uitvoeren zonder veel regels code te schrijven.

Voorbeeld: meerdere enemies spawnen in een game

```javascript
spawnEnemy();
spawnEnemy();
spawnEnemy();
```

- Oplossing: gebruik een loop om dit herhaaldelijk uit te voeren.
    

## While Loop

- De while loop voert een taak uit **tot de conditie false wordt**.
    
- **Belangrijk:** zonder een veranderende conditie kan de loop oneindig doorgaan.
    

Structuur:

```javascript
while (conditie) {
    // taak
}
```

Voorbeeld:

```javascript
let counter = 1;
while (counter <= 10) {
    console.log("I'm Mr. Meeseeks, look at me!");
    counter++;
}
console.log("Loop is afgelopen");
```

- Conditie moet uiteindelijk false worden.
    
- Variabele aanpassen in de loop voorkomt oneindige loops.
    

## For Loop

- Slimmere en veiligere versie van while.
    
- Combineert variabele, conditie en increment in één regel.
    

Structuur:

```javascript
for (let i = 1; i <= 10; i++) {
    // taak
}
```

Uitleg:

1. **Keyword:** `for`
    
2. **Variabele aanmaken:** bijvoorbeeld `let i = 1`
    
3. **Conditie:** wanneer stopt de loop? `i <= 10`
    
4. **Variabele aanpassen:** `i++`, `i--`, of `i += 3`
    
5. **Taak:** code die herhaald wordt
    

De loop gaat in volgorde: variabele aanmaken -> conditie checken -> taak uitvoeren -> variabele aanpassen -> conditie checken -> taak uitvoeren ...