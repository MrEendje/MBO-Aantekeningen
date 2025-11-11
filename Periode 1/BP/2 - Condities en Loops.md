
## Condities

```python
if knop_ingedrukt:
    beweeg_rechts()
else:
    blijf_staan()
```

- Conditie: knop_ingedrukt
    
- Als waar → beweeg_rechts()
    
- Als niet waar → blijf_staan()
    

### Voordelen van condities

- Programma’s kunnen beslissingen nemen
    
- Maken programma’s dynamisch en interactief
    
- Maken code leesbaar en overzichtelijk
    

### ASCII-diagram conditie

```
[knop_ingedrukt?]
     |
  +--+--+
  |     |
Ja     Nee
 |      |
beweeg  blijf
rechts  staan
```

## Loops

```python
for i in range(5):
    beweeg_vooruit()
```

- Herhaalt beweeg_vooruit() vijf keer
    

### Voordelen van loops

- Vermindert herhaling in code
    
- Maakt programma’s efficiënt
    
- Kan taken automatisch herhalen
    

### ASCII-diagram loop

```
[Start loop]
     |
     v
beweeg_vooruit()
     |
     v
beweeg_vooruit()
     |
    ...
     |
     v
[Stop na 5x]
```

## Combinatie: Condities + Loops

Conceptueel voorbeeld:

```
Herhaal totdat je de finish bereikt:
    als er een muur is:
        draai naar rechts
    anders:
        beweeg naar voren
```

### ASCII-diagram combinatie

```
[Finish bereikt?]
     |
  +--+--+
  |     |
Nee    Ja
 |      |
[Is er een muur?]   -> Stop
     |
  +--+--+
  |     |
Ja     Nee
 |      |
draai  beweeg
rechts  vooruit
```

## If-statements

```python
leeftijd = 18
if leeftijd >= 18:
    print("Je bent volwassen.")
else:
    print("Je bent minderjarig.")
```

- if → als de voorwaarde waar is
    
- else → alle andere gevallen
    
- Inspringing bepaalt welke regels bij if en else horen
    

### Voordelen van if-statements

- Besturing van stroom van programma (control flow)
    
- Programma kan verschillende uitkomsten hebben afhankelijk van input
    
- Essentieel voor interactieve toepassingen en beslissingslogica
    

## Samenvatting

|Concept|Functie|Voordeel|
|---|---|---|
|Conditie|Checkt waar/niet waar|Dynamisch, beslissingen, interactief|
|Loop|Herhaalt code automatisch|Efficiënt, minder herhaling, automatisch herhalen|
|If-statement|Laat programma keuzes maken|Control flow, interactieve uitkomsten|
|Combinatie|Loops + condities|Complexe, dynamische acties|