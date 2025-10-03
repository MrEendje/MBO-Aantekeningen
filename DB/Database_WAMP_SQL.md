# Database maken ([[WAMP]] localhost + SQL)

## Wat is een database?
Een **database** is een plek waar je informatie bewaart.  
Met **MySQL** kun je zulke databases maken en beheren.

👉 Zie ook: [[Database]]

---

## Flow van database tot data
1. **Database maken** → kies een naam en maak hem aan.  
2. **Tabel maken** → definieer kolommen, types en sleutels.  
3. **Data toevoegen** → voer rijen in.  
4. **Data bekijken/bewerken** → `SELECT`, `UPDATE`, `DELETE`.

---

## 1. Database maken via SQL
```sql
-- Maak een nieuwe database
CREATE DATABASE MijnDatabase;
				
-- Gebruik de database
USE MijnDatabase;
```
💡 Tip: kies altijd een logische naam, bijvoorbeeld `school`, `winkel` of `spel`.

---

## 2. Tabel maken (sjabloon)
```sql
CREATE TABLE TabelNaam (
    id INT AUTO_INCREMENT PRIMARY KEY,
    kolom1 VARCHAR(100) NOT NULL,
    kolom2 INT NULL,
    kolom3 DATE NOT NULL,
    opmerking VARCHAR(250) NULL,
    datum_aangemaakt DATETIME DEFAULT NOW()
);
```
💡 Tip: gebruik altijd een **id** als primaire sleutel.  

---

## 3. Data toevoegen
```sql
INSERT INTO TabelNaam (kolom1, kolom2, kolom3)
VALUES ('waarde1', 123, '2025-10-02');
```

---

## 4. Data bekijken
```sql
SELECT * FROM TabelNaam;
```
💡 Tip: `SELECT kolom1, kolom2 FROM TabelNaam;` toont alleen die kolommen.

---

## 5. Data wijzigen
```sql
UPDATE TabelNaam
SET kolom1 = 'NieuweWaarde'
WHERE id = 1;
```

---

## 6. Data verwijderen
```sql
DELETE FROM TabelNaam
WHERE id = 1;
```

---

## 7. Constraints en Keys
- **PRIMARY KEY** → unieke sleutel per rij.  
- **FOREIGN KEY** → koppelt tabellen aan elkaar.  
- **UNIQUE** → waarde moet uniek zijn.  
- **NOT NULL** → waarde verplicht.  
- **DEFAULT** → standaardwaarde (bv. `NOW()`).

Voorbeeld:
```sql
CREATE TABLE Bestelling (
    id INT AUTO_INCREMENT PRIMARY KEY,
    klant_id INT NOT NULL,
    datum DATE NOT NULL,
    FOREIGN KEY (klant_id) REFERENCES Klant(id)
);
```

---

## 8. Belangrijke datatypes
- `VARCHAR(n)` → tekst, max. lengte **n**.  
- `INT` → getallen.  
- `DATE` → datum (jjjj-mm-dd).  
- `DATETIME` → datum + tijd.  
- `BIT` → true/false (1 of 0).  
kijk ook:
[[mysql_datatypes]]

---

## 9. Handige queries

### Sorteren
```sql
SELECT * FROM TabelNaam
ORDER BY kolom1 ASC;
```

### Zoeken
```sql
SELECT * FROM TabelNaam
WHERE kolom1 = 'waarde';
```

### Meerdere voorwaarden
```sql
SELECT * FROM TabelNaam
WHERE kolom2 > 100 AND kolom3 = '2025-01-01';
```

### Aantal rijen tellen
```sql
SELECT COUNT(*) FROM TabelNaam;
```

### Groeperen
```sql
SELECT kolom2, COUNT(*)
FROM TabelNaam
GROUP BY kolom2;
```

### Tabellen koppelen (JOIN)
```sql
SELECT k.naam, b.datum
FROM Klant k
JOIN Bestelling b ON k.id = b.klant_id;
```

---

## [OBSIDIAN Tips]
- Gebruik `[[...]]` om notities te linken.  
- Maak aparte notities voor grote onderwerpen zoals:  
  - [[Database]] (wat is een database)  
  - [[SQL Queries]] (query voorbeelden)  
  - [[Constraints en Keys]] (uitleg sleutels)  
- Gebruik kopjes (#, ##, ###) om je notities overzichtelijk te houden.  

