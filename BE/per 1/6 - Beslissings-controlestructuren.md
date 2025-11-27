## Wat is een beslissings-controlestructuur?
- Een **beslissings-controlestructuur** bepaalt welke code wordt uitgevoerd op basis van een **voorwaarde**.
- Het programma kan hierdoor **kiezen tussen meerdere mogelijkheden**.
- Zonder beslissingsstructuur zou een PHP-script altijd dezelfde instructies uitvoeren, ongeacht de situatie.
- Voorbeelden van beslissingen die een programma kan nemen:
  - Is de gebruiker ingelogd?
  - Heeft iemand genoeg saldo?
  - Welke optie heeft de gebruiker gekozen?

> Belangrijk: beslissingsstructuren maken een programma **dynamisch en interactief**.

---

## Waarom gebruiken we beslissingsstructuren?
- Software moet **intelligent gedrag** vertonen; het moet kunnen reageren op de situatie.
- Het laat de code **beslissingen nemen**.
- Voorkomt **onnodige of foutieve acties**. Bijvoorbeeld: je wilt geen bestelling plaatsen als het saldo te laag is.
- Maakt een programma **flexibel** en bruikbaar in verschillende omstandigheden.
- Zonder beslissingsstructuren is een programma **lineair**, het voert gewoon van boven naar beneden uit zonder logica of keuze.

---

## Belangrijke concepten
- **Voorwaarde (condition):** Een logische uitspraak die `true` of `false` kan zijn.
- **True:** De voorwaarde is waar → code in de structuur wordt uitgevoerd.
- **False:** De voorwaarde is niet waar → code in de structuur wordt overgeslagen.
- **Boolean waarden:** `true` en `false` zijn essentieel bij beslissingen.

---

## Beslissingsstructuren in PHP

### 1. if – elseif – else
- Basisvorm om een **voorwaarde te controleren**.
- Voorbeeld:

```php
$leeftijd = 20;

if ($leeftijd >= 18) {
    echo "Je bent volwassen.";
} elseif ($leeftijd >= 13) {
    echo "Je bent een tiener.";
} else {
    echo "Je bent een kind.";
}
