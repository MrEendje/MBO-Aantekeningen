## 1. Introductie HTML

HTML is de basis van alle webpagina’s. Het is een oudere taal, maar nog steeds actueel en belangrijk voor webdevelopers. Tegenwoordig wordt HTML vaak gegenereerd met tools of systemen, maar het is belangrijk om eerst de basis te begrijpen.

### Wat is HTML?
HTML staat voor **Hypertext Markup Language**.

- Hyper = Hypertext  
- T = Text  
- M = Markup  
- L = Language  

### Soort taal
- HTML is een **Markup Language** (opmaakt taal).  
- Het vertelt de browser wat er op de pagina moet komen te staan.  
- HTML kan zelf geen logica uitvoeren; daar zijn andere talen zoals JavaScript voor nodig.

### HTML-elementen
- Een **element** is een bouwsteen van een webpagina.  
- De meeste elementen bestaan uit een **start-tag** en een **closing-tag**.  
- Tags beginnen met `<` en eindigen met `>`.  
- Een closing tag heeft een `/` voor de naam: `</element>`.  
- Sommige elementen hebben geen closing tag (bijvoorbeeld `<img>`).

### HTML-attributen
- Attributen geven extra informatie over een element.  
- Ze worden altijd in de start-tag gezet.  
- Attributen komen vaak in naam-waardeparen voor, sommige attributen hebben geen waarde nodig.

### Basisstructuur HTML-pagina
Een correcte HTML-pagina bevat altijd:

1. **DOCTYPE declaration**  
   Vertelt de browser welke HTML-versie gebruikt wordt (meestal HTML5).  
   Voorbeeld: `<!DOCTYPE html>`

2. **HTML-element**  
   Omvat de hele pagina, ook wel het **root element** genoemd.

3. **HEAD-element**  
   Staat bovenaan, bevat meta-data (informatie die niet zichtbaar is).  
   Voorbeelden: titel, auteur, beschrijving, CSS links.

4. **TITLE-element**  
   Staat in HEAD. Dit is de titel die in de browser bovenaan te zien is.

5. **BODY-element**  
   Bevat alle zichtbare inhoud: tekst, afbeeldingen, formulieren.

---

## 2. Introductie CSS

CSS wordt gebruikt om HTML-elementen vorm te geven. Zonder CSS is een pagina alleen wit met zwarte tekst.

### Wat is CSS?
CSS staat voor **Cascading Style Sheets**.  

- Het is geen programmeertaal; het voegt geen logica toe.  
- CSS is een **stylesheet language**, bedoeld voor styling.

### Manieren om CSS toe te passen

1. **Inline**  
   - Styling wordt direct op het element toegepast via het `style`-attribuut.  
   - Niet geschikt voor veel elementen, moeilijk te onderhouden.

2. **Internal**  
   - CSS staat in een `<style>` element in hetzelfde HTML-bestand.  
   - Gemakkelijk voor één pagina, maar niet voor meerdere pagina’s.

3. **External**  
   - CSS staat in een apart bestand (`.css`) en wordt gekoppeld via `<link>`.  
   - Meest gebruikt, makkelijk onderhoudbaar voor meerdere pagina’s.

### CSS-opbouw
CSS bestaat uit:
1. **Selector** – selecteert het HTML-element.  
2. **Property** – wat je wilt aanpassen (bijv. kleur, grootte).  
3. **Value** – waarde van de property (bijv. rood, 18px).

### CSS Selectors

- **Element selector** – selecteert alle elementen van dat type.  
- **Class selector** – selecteert elementen met een specifieke class (`.classname`).  
- **ID selector** – selecteert één uniek element met een ID (`#idname`).

---

## 3. Veelgebruikte HTML-elementen

- Koppen: `<h1>` t/m `<h6>`  
- Paragraaf: `<p>`  
- Afbeelding: `<img>`  
- Link: `<a href="...">...</a>`  
- Lijsten: `<ul>`, `<li>`  
- Vetgedrukt: `<strong>`  
- Figure + caption: `<figure><img ...><figcaption>...</figcaption></figure>`  
- Dialog / details: `<dialog>` en `<details><summary>...</summary></details>`  

---

## 4. Belangrijke punten

- HTML-structuur is belangrijk voor zoekmachines en toegankelijkheid.  
- Browsers corrigeren veel fouten, maar correcte HTML is altijd beter.  
- CSS zorgt voor vormgeving en positionering van elementen.  
- Gebruik externe stylesheets voor onderhoudbare styling.  
- Goede selectors maken CSS korter en overzichtelijker.  
- Elk HTML-element kan gestyled worden met CSS-properties zoals kleur, grootte, lettertype, positie, etc.  
