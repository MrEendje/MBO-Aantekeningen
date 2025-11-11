## 1. Tekst op het scherm zetten

- Gebruik **PHP** om tekst in je browser te laten zien.
    
- PHP-code staat tussen `<?php` en `?>`.
    
- Om iets te laten zien gebruik je `echo`.
    

```php
<?php
echo "Hallo, wereld!";
?>
```

### Variabelen

- Een variabele is een stukje geheugen waarin je data opslaat.
    
- Begin altijd met `$`.
    
- Strings en variabelen kun je aan elkaar plakken met een `.`
    

```php
$voornaam = "Ali";
echo "Hallo " . $voornaam . "!";
```

## 2. Commentaar in PHP

- Commentaar is tekst in je code die **niet wordt uitgevoerd**.
    

### Manieren om commentaar te schrijven in PHP

1. **Single-line comment met #**
    

```php
# Dit is een commentaar
```

2. **Single-line comment met //**
    

```php
// Dit is ook een commentaar
```

3. __Multi-line comment met /_ _/__
    

```php
/* Dit is een commentaar
   dat meerdere regels beslaat */
```

4. **Doc-block met /** _/_*
    

```php
/**
 * Dit is een doc-block
 * wordt vaak gebruikt voor uitleg van functies
 */
```

### Commentaar in HTML

- Voor tekst die niet zichtbaar is in de browser:
    

```html
<!-- Deze tekst zie je niet in je browser -->
```

## 3. Projectstructuur

- Maak een map **app** met bestand **lesweek1.php**.
    
- Maak een map **css** met bestand **style.css**.
    
- Verbind **index.html** met **style.css** en **lesweek1.php**.
    
- Voeg een HTML5 startertemplate toe in **lesweek1.php**.
    

## 4. Praktijk opdrachten

1. Zet je NAW-gegevens in meerdere variabelen en geef ze weer op het scherm met `echo`.
    
2. Voeg bij je code commentaar toe met **alle 4 manieren** ( `#`, `//`, `/* */`, `/** */` ) en HTML commentaar als extra.
    

> [!tip] Tip: Variabelen en echo samen gebruiken is de basis van dynamische inhoud in PHP.