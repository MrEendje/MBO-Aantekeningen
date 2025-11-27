## Inleiding

Een switch case is te vergelijken met een if, else if, else statement. Het is een **conditional statement** dat gebruikt wordt om een variabele te vergelijken met meerdere mogelijke waarden.

## Syntax

- Keyword: `switch` gevolgd door een **value** (bijvoorbeeld een variabele).
    
- Voor elke mogelijke waarde schrijf je een **case**:
    
    ```javascript
    switch(i) {
        case 1:
            task1();
            break;
        case 2:
            task2();
            break;
        default:
            defaultTask();
            break;
    }
    ```
    
- **default** werkt als een else: wordt uitgevoerd als geen enkele case matcht.
    
- Je kunt meerdere cases dezelfde taak laten uitvoeren:
    
    ```javascript
    switch(i) {
        case 1:
        case 2:
            task();
            break;
        default:
            defaultTask();
            break;
    }
    ```
    

## Werking

- De switch kijkt welke case overeenkomt met de waarde.
    
- Wanneer een match wordt gevonden, wordt de bijbehorende taak uitgevoerd.
    
- `break` voorkomt dat volgende cases ook uitgevoerd worden.
    
- Als geen case matcht, wordt de **default** uitgevoerd.
    

## Voorbeeld

```javascript
let i = 2;
switch(i) {
    case 1:
        console.log('Case 1');
        break;
    case 2:
        console.log('Case 2'); // Dit wordt uitgevoerd
        break;
    default:
        console.log('Geen match');
        break;
}
```