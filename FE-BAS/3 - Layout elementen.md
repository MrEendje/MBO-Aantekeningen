
Veel websites hebben tegenwoordig een vergelijkbare indeling:
- Menu bovenaan
- Banner daaronder
- Inhoud van de pagina
- Footer onderaan

Binnen HTML zijn er speciale elementen om deze indeling duidelijk te maken.

---

## Semantic Elements

**Semantic Elements** zijn elementen die duidelijk zeggen waarvoor ze gebruikt worden.  
Voorbeelden:
- `<nav>`: voor navigatie
- `<article>`: voor artikelen of hoofdinhoud van een pagina

### Voorbeelden van Semantic Elements

| HTML Element | Gebruik |
|--------------|---------|
| `<header>`   | Staat bovenaan “iets” (pagina of artikel). Bevat vaak titels. |
| `<nav>`      | Navigatie menu’s of submenu’s. Kan meerdere keren voorkomen. |
| `<main>`     | Algemene inhoud van de pagina. Meestal maar 1 per pagina. |
| `<aside>`    | Inhoud “naast” iets zetten, zoals zijmenu’s. Vaak naast `<article>`. |
| `<article>`  | Zelfstandige inhoud of artikel. Meerdere per pagina mogelijk. |
| `<section>`  | Verdeel pagina of artikel in secties. Vaak met een heading (`h2`, `h3`). |
| `<footer>`   | Staat onderaan “iets” (pagina of artikel). Meerdere keren mogelijk. |

> Let op: Dit zijn de elementen die gebruikt worden om de structuur van een pagina duidelijk te maken. Er zijn meer semantic HTML elementen.

---

## Moet je semantic elements altijd gebruiken?

Nee, je kunt ook met `<div>` een pagina maken, maar dat maakt code:
- Minder overzichtelijk
- Moeilijker te onderhouden
- Lastiger uit te leggen aan andere developers  

**Voorbeeld moeilijk uitleggen:**  
> "Je moet de titel in de div met de klasse content in het div element met het ID banner in het div element onder het body element zetten."  

**Makkelijker met semantic elements:**  
> "Het eerste `<header>` element bevat een `<h1>` element waarvan de titel veranderd moet worden."

Duidelijke code = gemakkelijker onderhouden + bespreken.

---

## Zien semantic elements er anders uit?

Nee.  
- Ze hebben geen visueel verschil  
- Doel: code overzichtelijk houden  
- Voordeel: je kan ze makkelijk stylen en selecteren
