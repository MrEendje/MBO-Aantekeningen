## Inleiding

If statements zijn veelgebruikt in programmeren. Ze beantwoorden de vraag: "Als deze conditie van toepassing is, doe dan de volgende taak." Structuur: `if -> conditie -> taak`.

## Voorbeeld

```javascript
if (x > 10) {
    stop();
}
```

- Als `x` groter is dan 10, wordt `stop()` uitgevoerd.
    
- **Curly brackets { }** geven het codeblok aan.
    

## Else statements

- Een `else` wordt uitgevoerd als de `if` conditie niet klopt.
    

```javascript
if (x > 10) {
    stop();
} else {
    go();
}
```

- Logica: Als `x > 10` doe `stop()`, anders doe `go()`.
    

## Else if statements

- Combineert meerdere condities.
    
- Meerdere `else if` statements zijn mogelijk, gevolgd door een `else`.
    

```javascript
if (x > 10) {
    stop();
} else if (x > 8) {
    goSlowly();
} else {
    go();
}
```

- Logica: eerst check `x > 10`, anders check `x > 8`, anders voer `go()` uit.
    

## Comparison Operators

|Operator|Betekenis|
|---|---|
|`==`|gelijk aan|
|`===`|gelijk aan **en** datatype gelijk|
|`!=`|niet gelijk aan|
|`!==`|niet gelijk aan **of** datatype niet gelijk|
|`>`|groter dan|
|`<`|kleiner dan|
|`>=`|groter dan of gelijk aan|
|`<=`|kleiner dan of gelijk aan|

## Logical Operators

|Operator|Betekenis|
|---|---|
|`&&`|beide statements moeten waar zijn|
|`||
|`!`|negatie van de conditie|

- Logical operators combineren meerdere condities binnen een `if` statement.