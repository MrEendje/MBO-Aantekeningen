## 1. Inleiding

Websites bestaan uit drie hoofdtypen elementen:  

1. **Tekst elementen** – voor alle tekst op de pagina.  
2. **Formulier elementen** – voor interactieve onderdelen zoals knoppen en zoekvelden.  
3. **Block elementen** – voor positionering en structuur van de pagina.  

In deze module ligt de focus op **tekst elementen** en hoe deze correct ingezet moeten worden.

---

## 2. Wat zijn tekst elementen?

- Ieder HTML-element kan tekst bevatten, maar sommige zijn specifiek bedoeld voor tekst.  
- Correct gebruik van tekst-elementen verbetert **toegankelijkheid**, bijvoorbeeld voor screenreaders.  

### Veelgebruikte tekst-elementen:
- `h1` t/m `h6` – headings  
- `p` – paragrafen  
- `span` – inline tekst  
- `strong` – belangrijke/dikgedrukte tekst  
- `blockquote` – citaten  

---

## 3. Heading elementen

- Heading elementen (`h1` t/m `h6`) worden gebruikt voor **titels en structuur** van de tekst.  
- `h1` is de grootste en belangrijkste heading; een pagina mag **maar één `h1`** hebben.  
- `h2` t/m `h6` worden gebruikt voor subkoppen of secties.  

**Belangrijk voor toegankelijkheid:**  
Screenreaders gebruiken headings om de pagina te structureren en navigatie te vergemakkelijken.

**Tip:** Gebruik heading elementen om de pagina op te delen in logische "hoofdstukken".

---

## 4. Paragraph elementen

- Paragraph (`p`) elementen bevatten normaal gesproken **tekst in volledige zinnen**.  
- Ze nemen de volledige breedte van de container in beslag, tenzij CSS dit aanpast.  
- Browsers voegen standaard **marge boven en onder** toe.  

**Gebruik:**  
- Voor gewone tekstblokken.  
- Niet voor titels of labels; daarvoor zijn headings of andere elementen beter geschikt.

---

## 5. Text formatting

Text formatting betekent de **vormgeving van tekst**.  

- Denk aan: dikgedrukt, cursief, onderstreept, gemarkeerd, subscript, superscript, doorstreept.  
- Gebruik **semantische formatting-elementen** in plaats van alleen visuele tags (`b`, `i`) om toegankelijkheid te waarborgen.  

| HTML | Uitwerking | Uitleg |
|------|-----------|--------|
| `<b>` | Dikgedrukt | Oude manier; niet goed voor screenreaders. Gebruik `<strong>`. |
| `<strong>` | Belangrijke tekst | Geeft aan dat tekst belangrijk is. Goed voor intro’s of belangrijke woorden. |
| `<i>` | Schuingeschreven | Oude manier; gebruik `<em>` voor nadruk. |
| `<em>` | Benadrukte tekst | Tekst die benadrukt moet worden, bijvoorbeeld namen of belangrijke woorden. |
| `<mark>` | Gemarkeerde tekst | Om tekst te markeren; wordt niet vaak gebruikt. |
| `<small>` | Kleine tekst | Voor onderschriften of tips. |
| `<del>` | Doorstreepte tekst | Geeft aan dat tekst is verwijderd of vervangen. |
| `<ins>` | Onderstreepte tekst | Tekst die later is toegevoegd; vaak in combinatie met `<del>`. |
| `<sub>` | Subscript | Tekst onder de basislijn, bijvoorbeeld H₂O. |
| `<sup>` | Superscript | Tekst boven de basislijn, bijvoorbeeld 15m². |

**Tip:** Gebruik formatting-elementen binnen `p` of heading-elementen (`h1` t/m `h6`) voor een correcte structuur en toegankelijkheid.

---

## 6. Extra aandachtspunten

- Heading-elementen bepalen de **structuur en hiërarchie** van de tekst.  
- Formatting-elementen verbeteren **semantiek en toegankelijkheid**, niet alleen de visuele weergave.  
- Paragraph-elementen zijn de basis voor gewone tekst, headings voor structuur, formatting-elementen voor nadruk.  
- Vermijd inline styling of verouderde tags zoals `<b>` en `<i>` voor semantische doeleinden.

---

## 7. Overzicht belangrijke tekst-elementen

- **Headings:** `<h1>` – `<h6>`  
- **Paragraaf:** `<p>`  
- **Inline tekst:** `<span>`  
- **Belangrijk/dikgedrukt:** `<strong>`  
- **Benadrukt/italic:** `<em>`  
- **Gemarkeerd:** `<mark>`  
- **Kleine tekst:** `<small>`  
- **Doorstreept:** `<del>`  
- **Onderstreept:** `<ins>`  
- **Subscript:** `<sub>`  
- **Superscript:** `<sup>`  
- **Citaten:** `<blockquote>`  

---

Dit document bevat alle kernpunten over **tekst-elementen in HTML**, inclusief semantiek, accessibility en text formatting.
