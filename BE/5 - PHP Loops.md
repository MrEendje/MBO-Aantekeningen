## 1. Wat is een loop?

- Een loop is een manier om **code meerdere keren uit te voeren** zonder alles opnieuw te schrijven.
    
- Handig voor **herhaling, efficiëntie en flexibiliteit**.
    

### Voorbeelden in het dagelijks leven

- For-loop: tel van 1 tot 10 en schrijf elk getal op.
    
- While-loop: blijf doorgaan totdat je moe bent.
    
- Foreach-loop: pak elk item uit een lijst en verwerk het.
    

## 2. Soorten loops in PHP

### 2.1 For-loop

- Gebruik als je weet hoe vaak de code herhaald moet worden.
    
- Syntax:
    

```php
for ($i = 0; $i < 5; $i++) {
    echo "Getal: $i<br>";
}
```

- Uitleg:
    
    - `$i = 0`: startwaarde
        
    - `$i < 5`: voorwaarde
        
    - `$i++`: teller verhogen per iteratie
        
- Voorbeeld stap voor stap:
    
    - Start: $i=0 → check → uitvoer
        
    - Stop als $i=5
        

### Opdrachten

1. Print de tafel van 7.
    
2. Sterrenpatroon:
    

```
*
**
***
****
*****
```

- Gebruik `str_repeat('*', $i)` in een for-loop.
    

### 2.2 Foreach-loop

- Loop door **alle elementen van een array**.
    
- Syntax voor gewone array:
    

```php
$dieren = ['hond', 'kat', 'vis'];
foreach ($dieren as $dier) {
    echo "Huisdier: $dier<br>";
}
```

- Output:
    
    - Huisdier: hond
        
    - Huisdier: kat
        
    - Huisdier: vis
        

#### Foreach met associatief array

- Syntax:
    

```php
$leeftijden = ['Sarah' => 25, 'Sieben' => 30, 'Leontien' => 17];
foreach ($leeftijden as $naam => $leeftijd) {
    echo "Mijn naam is $naam en ik ben $leeftijd jaar oud.<br>";
}
```

- Output:
    
    - Mijn naam is Sarah en ik ben 25 jaar oud.
        
    - Mijn naam is Sieben en ik ben 30 jaar oud.
        
    - Mijn naam is Leontien en ik ben 17 jaar oud.
        

### 2.3 While-loop

- Blijft herhalen zolang de conditie waar is.
    
- Syntax:
    

```php
$x = 0;
while ($x < 5) {
    echo $x;
    $x++;
}
```

### 2.4 Do...while-loop

- Wordt **minstens één keer uitgevoerd**, ongeacht de conditie.
    
- Syntax:
    

```php
$x = 5;
do {
    echo $x;
    $x++;
} while ($x < 5);
```

### 2.5 Break en Continue

- **break**: stopt de hele loop.
    
- **continue**: slaat de huidige iteratie over en gaat verder met de volgende.
    

## 3. Samengevat

- **For-loop**: gebruik als aantal herhalingen bekend is.
    
- **Foreach-loop**: ideaal voor arrays en associatieve arrays.
    
- **While-loop**: herhaal zolang iets waar is.
    
- **Do...while-loop**: herhaal minimaal één keer.
    
- **Break/Continue**: controle over de loop.
    

### Opdrachten

1. Indexed array van 7 chocoladebars en doorloop met foreach.
    
2. Associatieve array van mensen met leeftijden en doorloop met foreach.