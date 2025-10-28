# MySQL datatypes - Les 5.2
## Wat is een database?
Een **database** is een plek waar je informatie bewaart.  
Met **MySQL** kun je zulke databases maken en beheren.

👉 Zie ook: [[2 Database]]


## Leerdoelen

In deze les behandelen we:
- Verschillende MySQL datatypes
- Opslaan van verschillende soorten gegevens
- Tekstuele datatypes
- Numerieke datatypes
- Datum- en tijdtypes
- Speciale datatypes
- Specificatie tabellen

---

## Numerieke Datatypes

### Exact Numerieke Gegevens (Gehele Getallen)

| Type        | Omschrijving                 | Waardenbereik                                                                     | Geheugen |
| ----------- | ---------------------------- | --------------------------------------------------------------------------------- | -------- |
| `TINYINT`   | Zeer klein geheel getal      | Zonder teken: 0 tot 255<br>Met teken: -128 tot +127                               | 1 Byte   |
| `SMALLINT`  | Klein geheel getal           | Zonder teken: 0 tot 65.535<br>Met teken: -32.768 tot +32.767                      | 2 Byte   |
| `MEDIUMINT` | Middelgroot geheel getal     | Zonder teken: 0 tot 16.777.215<br>Met teken: -8.388.608 tot +8.388.607            | 3 Byte   |
| `INT`       | Geheel getal normale grootte | Zonder teken: 0 tot 4.294.967.295<br>Met teken: -2.147.483.648 tot +2.147.483.647 | 4 Byte   |
| `BIGINT`    | Groot geheel getal           |                                                                                   | 8 Byte   |

> [!tip] Unsigned
> Gebruik `UNSIGNED` om alleen positieve getallen toe te staan en het bereik te verdubbelen.

### Kommagetallen (Floating Point)

| Type | Omschrijving | Waardenbereik | Nauwkeurigheid | Toepassing | Geheugen |
|------|--------------|---------------|----------------|------------|----------|
| `FLOAT(M,D)` | Enkel precisie drijvend kommagetal | -3.402823466E+38 tot 3.402823466E+38 | ~7 cijfers | Snel, minder precies | 4 Byte |
| `DOUBLE(M,D)` | Dubbele precisie drijvend kommagetal | -1.7976931348623157E+308 tot 1.7976931348623157E+308 | ~15-16 cijfers | Algemeen, wetenschappelijk | 8 Byte |
| `DECIMAL(M,D)` | Exact decimaal getal | -7.9 × 10²⁸ tot +7.9 × 10²⁸ | 28-29 cijfers | **Financieel, exacte berekeningen** | 16 Byte |

> [!important] DECIMAL voor geld
> Gebruik altijd `DECIMAL` voor financiële berekeningen om afrondingsfouten te voorkomen!
> 
> **M** = totaal aantal cijfers, **D** = aantal decimalen
> Bijvoorbeeld: `DECIMAL(10,2)` voor bedragen tot 99.999.999,99

---

## String Datatypes

| Type            | Omschrijving                | Waardenbereik                 | Geheugen          |
| --------------- | --------------------------- | ----------------------------- | ----------------- |
| `CHAR(M)`       | Tekenreeks vaste lengte     | M: 0 tot 255 tekens           | M tekens (altijd) |
| `VARCHAR(M)`    | Tekenreeks variabele lengte | M: 0 tot 65.535 tekens        | M + 2 Byte        |
| `TINYTEXT(M)`   | Zeer kleine tekst variabel  | M: 0 tot 255 tekens           | M + 1 Byte        |
| `TEXT(M)`       | Tekst variabel              | M: 0 tot 65.535 tekens        | M + 2 Byte        |
| `MEDIUMTEXT(M)` | Middelgrote tekst variabel  | M: 0 tot 16.777.215 tekens    | M + 3 Byte        |
| `LONGTEXT(M)`   | Lange tekst variabel        | M: 0 tot 4.294.967.295 tekens | M + 4 Byte        |

> [!tip] CHAR vs VARCHAR
> - **CHAR**: Gebruik voor velden met altijd dezelfde lengte (bijv. landcodes: "NL", "BE")
> - **VARCHAR**: Gebruik voor velden met wisselende lengte (bijv. namen, adressen)

---

## Datum en Tijd Datatypes

| Type | Omschrijving | Waardenbereik | Geheugen |
|------|--------------|---------------|----------|
| `TIME` | Tijdweergave: HH:MM:SS.ssssss | -838:59:59.999999 tot +838:59:59.999999 | 3 Byte |
| `YEAR` | Jaarweergave: YYYY | 1901 tot 2155 en 0000 | 1 Byte |
| `DATE` | Datumweergave: YYYY-MM-DD | 1001-01-01 tot 9999-12-31 | 3 Byte |
| `DATETIME` | Datum + Tijd: YYYY-MM-DD HH:MM:SS.ssssss | 1000-01-01 00:00:00 tot 9999-12-31 23:59:59.999999 | 8 Byte |
| `TIMESTAMP` | Datum + Tijd (UTC): YYYY-MM-DD HH:MM:SS.ssssss | 1970-01-01 00:00:01 tot 2038-01-09 05:14:07 | 4 Byte |

> [!important] DATETIME vs TIMESTAMP
> - **DATETIME**: Slaat exacte datum/tijd op zoals ingevoerd
> - **TIMESTAMP**: Converteert naar UTC, ideaal voor internationale applicaties
> - **TIMESTAMP** heeft Y2038 probleem (max 2038-01-09)

---

## Speciale Datatypes

| Type         | Omschrijving                            | Waardenbereik            | Geheugen   |
| ------------ | --------------------------------------- | ------------------------ | ---------- |
| `UUID`       | Universally Unique Identifier           | VARCHAR(36) formaat      | 16 Byte    |
| `BIT`        | Boolean waarde                          | 1 = True, 0 = False      | 1 Byte     |
| `TINYBLOB`   | Klein binair object                     | Max. 255 bytes           | M + 1 Byte |
| `BLOB`       | Binair object (afbeeldingen, audio)     | Max. 65.535 bytes        | M + 2 Byte |
| `MEDIUMBLOB` | Middelgroot binair object               | Max. 16.777.215 bytes    | M + 3 Byte |
| `LONGBLOB`   | Groot binair object                     | Max. 4.294.967.295 bytes | M + 4 Byte |
| `ENUM`       | Opsomming met voorgedefinieerde waarden | Max. 65.535 waarden      | 2 Byte     |

> [!info] UUID
> UUID's zijn handig in gedistribueerde systemen waar meerdere computers/databases samenwerken.
> 
> Voorbeeld: `550e8400-e29b-41d4-a716-446655440000`

> [!warning] BLOB voor binaire data
> BLOB is voor binaire bestanden (plaatjes, PDF's). Voor tekst gebruik TEXT types!

---

## Specificatie Tabel

### Waarom een Specificatie Tabel?

Een tabelspecificatie helpt bij:
- ✅ Fouten voorkomen tijdens database aanmaak
- ✅ Consistentie tussen ontwikkelaars
- ✅ Snel overzicht van kolom bedoelingen

### Onderdelen Specificatie Tabel

| Onderdeel | Beschrijving |
|-----------|--------------|
| **Kolomnaam** | Naam van de kolom (bijv. `Id`, `StudentId`, `Email`) |
| **Datatype** | Gegevenstype (`INT`, `VARCHAR`, `DATE`, `BIT`, etc.) |
| **Lengte** | Maximale lengte of precisie (bijv. `VARCHAR(50)`) |
| **Nullable** | Mag de kolom leeg zijn? (`YES`/`NO`) |
| **Opmerking** | Extra info: Primary Key, Unique, Foreign Key, Default waarde, etc. |

### Voorbeeld Specificatie Tabel: Klant

| Kolomnaam | Datatype | Lengte | Nullable | Opmerking |
|-----------|----------|--------|----------|-----------|
| `Id` | INT | - | Nee | UNSIGNED, AUTO_INCREMENT, PRIMARY KEY |
| `Voornaam` | VARCHAR | 50 | Nee | |
| `Tussenvoegsel` | VARCHAR | 10 | Ja | DEFAULT NULL |
| `Achternaam` | VARCHAR | 50 | Nee | |
| `Nummer` | MEDIUMINT | - | Nee | UNSIGNED |
| `IsActief` | BIT | - | Nee | DEFAULT 1 |
| `Opmerking` | VARCHAR | 250 | Ja | DEFAULT NULL |
| `DatumAangemaakt` | DATETIME | 6 | Nee | DEFAULT NOW(6) |
| `DatumGewijzigd` | DATETIME | 6 | Nee | DEFAULT NOW(6), ON UPDATE NOW(6) |

> [!example] SQL Create Statement
> ```sql
> CREATE TABLE Klant (
>     Id INT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
>     Voornaam VARCHAR(50) NOT NULL,
>     Tussenvoegsel VARCHAR(10) DEFAULT NULL,
>     Achternaam VARCHAR(50) NOT NULL,
>     Nummer MEDIUMINT UNSIGNED NOT NULL,
>     IsActief BIT NOT NULL DEFAULT 1,
>     Opmerking VARCHAR(250) DEFAULT NULL,
>     DatumAangemaakt DATETIME(6) NOT NULL DEFAULT NOW(6),
>     DatumGewijzigd DATETIME(6) NOT NULL DEFAULT NOW(6) ON UPDATE NOW(6)
> );
> ```

---

## Belangrijke Concepten

### UNSIGNED
- Alleen positieve getallen
- Verdubbelt het maximale bereik
- Gebruik voor ID's, aantallen, leeftijden

### AUTO_INCREMENT
- Automatische ophoging van waarde
- Meestal gebruikt voor PRIMARY KEY
- Start standaard bij 1

### DEFAULT
- Standaardwaarde als geen waarde wordt opgegeven
- `DEFAULT NULL` - lege waarde
- `DEFAULT NOW()` - huidige datum/tijd
- `DEFAULT 1` - numerieke waarde

### NOT NULL
- Kolom MAG NIET leeg zijn
- Altijd een waarde vereist

---

## Tips & Best Practices

> [!tip] Datatypes kiezen
> 1. Kies het kleinste datatype dat je data kan bevatten
> 2. Gebruik `UNSIGNED` waar mogelijk voor positieve getallen
> 3. Gebruik `DECIMAL` voor financiële berekeningen
> 4. Gebruik `VARCHAR` in plaats van `TEXT` als je de maximale lengte weet

> [!warning] Veelgemaakte fouten
> - ❌ `FLOAT/DOUBLE` gebruiken voor geld (afrondingsfouten!)
> - ❌ `VARCHAR(255)` voor alles gebruiken (verspilling!)
> - ❌ Geen `NOT NULL` constraints gebruiken
> - ❌ `TEXT` gebruiken voor korte strings

---

## Gerelateerde Concepten

- [[Database Normalisatie]]
- [[4 Database en Tabellen]]
- [[6 MySQL constraints]]
- [[Database Design Patterns]]

---

#database #mysql #datatypes #sql #datamodellering