
## Wat is een functie?

- Een **functie** is een stukje code dat je **één keer schrijft** en daarna **zo vaak als je wilt kunt gebruiken**.
    
- Voert een specifieke taak uit, bijvoorbeeld:
    
    - Berekeningen uitvoeren
        
    - Gegevens tonen
        
    - Tekst verwerken
        
- Voorbeeld: een functie die BTW berekent over een bedrag:
    

```php
function berekenBtw($bedrag) {
    return $bedrag * 0.21;
}

echo berekenBtw(100); // Output: 21
```

**Voordelen van functies:**

- **Herbruikbaar:** dezelfde code op meerdere plekken gebruiken
    
- **Overzichtelijk:** code wordt leesbaar en onderhoudbaar
    
- **Fouten verminderen:** wijzig je de functie, dan werkt alles overal
    
- **Logica bundelen:** kleine, duidelijke taken maken je programma overzichtelijk
    

---

## 7.2 Leerdoelen van deze les

Na deze les kun je:

1. Uitleggen wat een functie is en voorbeelden geven van situaties waarin functies handig zijn.
    
2. Eenvoudige functies schrijven in PHP met parameters en return-waarde.
    
3. Functies op de juiste manier aanroepen in een PHP-script.
    
4. Functies toepassen om code overzichtelijker en herbruikbaar te maken.