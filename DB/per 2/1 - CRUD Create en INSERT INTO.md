## CRUD Betekenis

- **Create** → gegevens toevoegen
    
- **Read** → gegevens ophalen/bekijken
    
- **Update** → gegevens aanpassen
    
- **Delete** → gegevens verwijderen
    

## Create

- Eerste bewerking binnen CRUD.
    
- Gebruik `INSERT INTO` om rijen toe te voegen aan een tabel.
    
- Ingevoerde gegevens moeten voldoen aan tabelregels: datatypes, verplichte velden, relaties (constraints).
    

## Leerdoelen

- De rol van Create binnen CRUD uitleggen.
    
- Een tabel aanmaken met `CREATE TABLE`.
    
- Passende datatypes kiezen: INT, VARCHAR, DATE, DECIMAL.
    
- Velden verplicht maken met `NOT NULL` en standaardwaarden met `DEFAULT` instellen.
    

## INSERT INTO - toevoegen

1. Hele rij toevoegen.
    
2. Gedeelte van een rij toevoegen.
    
3. Werken met verschillende datatypes.
    
4. Foutmeldingen begrijpen.
    

### Syntax

```sql
INSERT INTO Naam_tabel (
    kolom1, kolom2, kolom3
)
VALUES (
    waarde1, waarde2, waarde3
);
```

### Voorbeeld: één rij

```sql
INSERT INTO Medewerker (
     Voornaam,
     Tussenvoegsel,
     Achternaam,
     Geboortedatum,
     MedewerkerNummer
)
VALUES ('Alice', NULL, 'Sanders', '1970-04-14', 123456);
```

### Voorbeeld: meerdere rijen

```sql
INSERT INTO Medewerker (
     Voornaam,
     Tussenvoegsel,
     Achternaam,
     Geboortedatum,
     MedewerkerNummer
)
VALUES
  ('Alice', NULL, 'Sanders', '1970-04-14', 123456),
  ('Hans', 'van', 'Odijk', '1960-09-10', 987654);
```

### Datatype regels

|Type|Formaat|Voorbeeld|
|---|---|---|
|DATETIME(6)|'YYYY-MM-DD HH:MM-SSssssss'|'2019-09-24 11:15:04:987654'|
|DATE|'YYYY-MM-DD'|'2019-09-24'|
|TIME|'HH:MM:SS'|'11:15:04'|
|CHAR/VARCHAR|'Tekst'|'Arjan'|
|BIT|1 of 0|1|
|DECIMAL(6,2)|getal|1234.56|
|TINYINT, SMALLINT, MEDIUMINT, INT|hele getal|123|

## Veelvoorkomende fouten

### Error 1136: aantal kolommen klopt niet

- Tabel heeft 5 kolommen, maar je vult er 4 in.
    

```sql
INSERT INTO Medewerker (
    Voornaam,
    Tussenvoegsel,
    Achternaam,
    Geboortedatum
)
VALUES ('Alice', NULL, 'Sanders', '1970-04-14'); -- FOUT
```

### Error 1265: datum fout

- Quotes vergeten bij datum.
    

```sql
INSERT INTO Medewerker (
    Voornaam,
    Tussenvoegsel,
    Achternaam,
    Geboortedatum,
    MedewerkerNummer
)
VALUES ('Alice', NULL, 'Sanders', 1970-04-14, 123456); -- FOUT
```

### Error 1366: verkeerd datatype

- Tekst invoeren in een getal-kolom.
    

```sql
INSERT INTO Medewerker (
    Voornaam,
    Tussenvoegsel,
    Achternaam,
    Geboortedatum,
    MedewerkerNummer
)
VALUES ('Alice', NULL, 'Sanders', '1970-04-14', 'Sam'); -- FOUT
```