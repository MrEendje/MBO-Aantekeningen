## 3.1 Introductie

CRUD staat voor:

- **Create** → Gegevens toevoegen
    
- **Read** → Gegevens ophalen / bekijken
    
- **Update** → Gegevens aanpassen
    
- **Delete** → Gegevens verwijderen
    

De **Read**-operatie wordt gebruikt om gegevens uit een database op te vragen, meestal via een `SELECT`-statement. Het is essentieel voor vrijwel elke applicatie: gebruikers willen data bekijken, zoeken, filteren of sorteren.

Met `SELECT` kun je precies aangeven:

- Welke kolommen je wilt zien
    
- Uit welke tabel de gegevens komen
    
- Welke voorwaarden gelden voor specifieke rijen
    

## 3.2 Leerdoelen

Na deze les kun je:

- Uitleggen wat een `SELECT`-statement doet
    
- Gegevens opvragen uit een tabel met `SELECT` en specifieke kolommen kiezen
    
- Resultaten filteren met `WHERE`
    
- Resultaten sorteren met `ORDER BY`
    
- Groepsfuncties zoals `COUNT()` en `AVG()` gebruiken
    
- Resultaten groeperen met `GROUP BY`
    

## 3.3 Basisbegrip van SELECT

- Alle informatie uit een tabel tonen
    
- Alleen enkele kolommen tonen
    
- Gebruik van één voorwaarde in `SELECT`
    
- Gegevens gesorteerd tonen
    
- Alleen unieke gegevens tonen
    

### Syntax: Alle gegevens ophalen

```sql
SELECT *
FROM <Naam_tabel>;
```

**Voorbeeld:**

```sql
SELECT *
FROM Student;
```

Dit toont alle kolommen van de tabel `Student`.

## 3.4 Kolommen selecteren

Vaak wil je niet alle velden tonen. Specificeer de kolommen die je wilt zien.

### Syntax: Specifieke kolommen

```sql
SELECT Kolom1, Kolom2, Kolom3
FROM Tabel_Naam;
```

**Voorbeeld:**

```sql
SELECT Id, Naam, Vak, Cijfer
FROM Student;
```

## 3.5 Filteren van data (WHERE)

Gebruik `WHERE` om specifieke rijen te filteren.

### Vergelijkingsoperatoren

|Operator|Betekenis|
|---|---|
|=|Is gelijk aan|
|!= of <>|Is verschillend van|
|<|Is kleiner dan|
|>|Is groter dan|
|<=|Is kleiner of gelijk aan|
|>=|Is groter of gelijk aan|

### Syntax: Filteren

```sql
SELECT Kolom1, Kolom2, Kolom3
FROM Tabel_Naam
WHERE KolomX = Waarde;
```

**Voorbeeld:**

```sql
SELECT Id, Naam, Vak, Cijfer
FROM Student
WHERE Cijfer > 7.0;
```

## 3.6 Sorteren van resultaten (ORDER BY)

Gebruik `ORDER BY` om resultaten te sorteren.

- **ASC**: oplopend (standaard)
    
- **DESC**: aflopend
    

### Syntax: Sorteren

```sql
SELECT Kolom1, Kolom2
FROM Tabel_Naam
ORDER BY KolomNaam ASC|DESC;
```

**Voorbeelden:**

```sql
-- Oplopend
SELECT Id, Naam, Vak, Cijfer
FROM Student
ORDER BY Naam ASC;

-- Aflopend
SELECT Id, Naam, Vak, Cijfer
FROM Student
ORDER BY Naam DESC;
```

**Meerdere kolommen sorteren:**

```sql
SELECT Kolom1, Kolom2
FROM Tabel_Naam
ORDER BY Kolom1, Kolom2;
```

## 3.7 Resultaten groeperen (GROUP BY)

Gebruik `GROUP BY` om rijen met gelijke waarden samen te voegen.

### Syntax: Groeperen

```sql
SELECT Kolom1, Kolom2, Kolom3
FROM Tabel_Naam
GROUP BY KolomNaam;
```

**Voorbeeld:**

```sql
SELECT Id, Klant, Product, Hoeveelheid, Prijs
FROM Bestelling
GROUP BY Product;
```

**Meerdere kolommen groeperen:**

```sql
SELECT Kolom1, Kolom2, Kolom3
FROM Tabel_Naam
GROUP BY Kolom1, Kolom2;
```

---

**Tip voor studenten:** Probeer de queries zelf uit met verschillende `WHERE`, `ORDER BY` en `GROUP BY` combinaties om het effect te zien op de resultaten.