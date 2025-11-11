 ## Wat is het boxmodel?

Het boxmodel is de basis van alle HTML elementen. Je kunt elk HTML element zien als een "doos" of vierkant. Het boxmodel bestaat uit 4 onderdelen (van buiten naar binnen):

- **Margin:** ruimte om het element heen (transparant)
    
- **Border:** de rand van het element
    
- **Padding:** ruimte vanaf de rand tot de content
    
- **Content:** de inhoud van het element, zoals tekst of afbeeldingen
    

## Content-box vs Border-box

Met CSS kun je aangeven of een element zich moet gedragen als `content-box` of `border-box`.

- **content-box:** de opgegeven width geldt alleen voor de content. Padding en border worden daar bovenop geteld.
    

```css
.content-box {
  box-sizing: content-box;
  width: 500px;
  height: auto;
  padding: 10px;
  border: 2px solid red;
  margin: 10px;
}
/* Totale breedte = 500 + (10*2) + (2*2) + (10*2) = 544px */
```

- **border-box:** de opgegeven width geldt inclusief padding en border.
    

```css
.border-box {
  box-sizing: border-box;
  width: 500px;
  height: auto;
  padding: 10px;
  border: 2px solid red;
  margin: 10px;
}
/* Totale breedte = 500 + (10*2) = 520px */
```

**Handige tip:** het is handig om alle elementen `border-box` te geven, bijvoorbeeld:

```css
body * {
  box-sizing: border-box;
}
```

Dit maakt het positioneren van elementen eenvoudiger en voorkomt onverwachte verschuivingen.

## CSS Eenheden

CSS eenheden worden gebruikt om bijvoorbeeld grootte van elementen of tekst aan te geven. Er zijn absolute en relatieve eenheden. Absolute eenheden schalen slecht mee met schermgroottes, daarom worden relatief vaak deze eenheden gebruikt:

|Eenheid|Uitleg|
|---|---|
|px|Pixels, handig voor borders of root font-size. Absolute eenheid.|
|%|Percentage van het parent-element.|
|em|Schaal van de font-size van het element.|
|rem|Schaal van de font-size van het root (html) element.|
|vh|1% van de hoogte van de viewport.|
|vw|1% van de breedte van de viewport.|

**Voorbeelden:**

```html
<div class="container">
  <div class="column"></div>
</div>
.container {
  width: 1024px;
}
.column {
  width: 50%; /* 50% van container = 512px */
}
```

```html
<article>
  <h1>Lorem Ipsum</h1>
</article>
article {
  font-size: 15px;
}
article h1 {
  font-size: 3em; /* 3 * 15px = 45px */
}
```

```html
<div class="banner">
  <img src="banner-img.jpeg" alt="Welcome"/>
</div>
html {
  font-size: 20px;
}
.banner {
  width: 100%;
  height: 20rem; /* 20 * 20px = 400px */
}
```

- **vh:** 100vh = volledige hoogte viewport
    
- **vw:** 100vw = volledige breedte **viewport**