## 1. Basisdatatypes in PHP

- **String**: tekst, bijv. `"Hallo"`
    
- **Integer**: gehele getallen, bijv. `10` of `-5`
    
- **Float/Double**: kommagetallen, bijv. `3.14` (punt gebruiken, geen komma)
    
- **Boolean**: true of false (1 of 0)
    
    - Bij `echo`: `false` → lege string, `true` → 1
        

### Voorbeeld

```php
<?php
$naam = "Ali"; // string
$leeftijd = 20; // integer
$prijs = 9.99; // float
$actief = true; // boolean

echo $naam;
echo $leeftijd;
echo $prijs;
echo $actief;
?>
```

## 2. Indexed Arrays

- Een **indexed array** kan meerdere waarden bevatten.
    
- Elke waarde heeft een index (nummer) die begint bij 0.
    

### Voorbeeld

```php
$snoep = array("Mars", "Snicker", "Galaxy");

echo $snoep[0]; // Mars
echo $snoep[2]; // Galaxy
```

### Opdracht idee

- Maak een array met je 5 favoriete games.
    
- Gebruik `echo` en de index om een top 5 lijst op het scherm te zetten.
    

## 3. Associatieve Arrays

- Een **associatieve array** koppelt elke waarde aan een sleutel (key) in plaats van een nummer.
    

### Voorbeeld

```php
$persoonsgegevens = array(
  'naam' => 'Arjan',
  'huisnummer' => 47
);

echo $persoonsgegevens['naam']; // Arjan
echo $persoonsgegevens['huisnummer']; // 47
```

- Binnen dubbele quotes: `echo "Mijn naam is: {$persoonsgegevens['naam']}";`
    

### Opdracht ideeën

1. Top 5 snelste auto's ter wereld:
    

```php
$autos = array(
  'Bugatti Veyron' => 456,
  'Fiat Diablo' => 234
);
```

2. 8 favoriete sneakers met prijs:
    

```php
$sneakers = array(
  'Adidas Galaxy 7' => 231.45,
  'Nike Vaporfly' => 187.67
);
```

- Gebruik `foreach` om alle items netjes te printen.
    

> [!tip] Tip: Associatieve arrays zijn handig als je een waarde wilt opzoeken op naam, niet op nummer.