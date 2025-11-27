
## Wat zijn MySQL Constraints?

MySQL constraints (beperkingen) zijn regels die je toevoegt aan een database om ervoor te zorgen dat de gegevens betrouwbaar, consistent en correct zijn. Ze fungeren als een soort "bewaker" die bepaalt welke gegevens wel of niet in een tabel mogen worden opgeslagen. Stel je voor dat je een database hebt voor een webshop: zonder constraints zou iemand bijvoorbeeld een bestelling kunnen plaatsen zonder klantgegevens, of een negatieve leeftijd kunnen invoeren. Constraints voorkomen dit soort fouten en zorgen ervoor dat je database logisch en bruikbaar blijft.

### Waarom zijn constraints belangrijk?

- **Datakwaliteit**: Ze zorgen ervoor dat de gegevens in je database kloppen (bijvoorbeeld geen lege velden waar een waarde verplicht is).
    
- **Betrouwbaarheid**: Ze voorkomen ongeldige of inconsistente gegevens (zoals een bestelling die verwijst naar een niet-bestaande klant).
    
- **Efficiëntie**: Ze maken je database gemakkelijker te onderhouden door regels automatisch af te dwingen.
    
- **Relaties**: Ze helpen relaties tussen tabellen te beheren, zoals het koppelen van een bestelling aan een klant.
    

In deze aantekening bespreken we:

- De verschillende soorten constraints in MySQL (zoals PRIMARY KEY, FOREIGN KEY, NOT NULL, enz.).
    
- Hoe je deze constraints kunt toevoegen bij het maken of aanpassen van tabellen.
    
- Hoe constraints relaties tussen tabellen beheren.
    
- Hoe je fouten kunt herkennen en oplossen als een constraint wordt geschonden.
    

## Soorten Constraints in MySQL

Hieronder bespreken we de meest gebruikte constraints in MySQL. Voor elke constraint geven we een eenvoudige uitleg, een voorbeeld en waarom deze nuttig is.

### 1. PRIMARY KEY

De PRIMARY KEY is een unieke identificatie voor elke rij in een tabel. Het is als een burgerservicenummer: geen twee rijen in dezelfde tabel kunnen dezelfde waarde hebben voor de primaire sleutel. Dit zorgt ervoor dat je altijd een specifieke rij kunt vinden.

**Waarom gebruiken?** Om ervoor te zorgen dat elke rij uniek is en gemakkelijk te identificeren.

**Voorbeeld:**

```sql
CREATE TABLE Klant (
    Id INT,
    Code CHAR(3),
    Naam VARCHAR(100),
    Leeftijd TINYINT,
    Email VARCHAR(100),
    Opmerking VARCHAR(250),
    PRIMARY KEY (Id)
);
```

In dit voorbeeld is Id de primaire sleutel. Elke klant krijgt een unieke Id, en MySQL zorgt ervoor dat geen twee klanten dezelfde Id kunnen hebben.

### 2. AUTO_INCREMENT

Met AUTO_INCREMENT laat je MySQL automatisch een uniek nummer genereren voor een kolom (meestal de primaire sleutel) telkens wanneer je een nieuwe rij toevoegt. Dit is handig omdat je niet zelf unieke ID’s hoeft te bedenken.

**Waarom gebruiken?** Om het toevoegen van nieuwe records eenvoudiger te maken door automatisch unieke ID’s te genereren.

**Voorbeeld:**

```sql
CREATE TABLE Klant (
    Id INT AUTO_INCREMENT,
    Code CHAR(3),
    Naam VARCHAR(100),
    Leeftijd TINYINT,
    Email VARCHAR(100),
    Opmerking VARCHAR(250),
    PRIMARY KEY (Id)
);
```

Hier begint Id bij 1 en wordt automatisch verhoogd (2, 3, 4, enz.) bij elke nieuwe klant.

### 3. FOREIGN KEY

Een FOREIGN KEY (vreemde sleutel) maakt een verbinding tussen twee tabellen. Het zorgt ervoor dat een waarde in een kolom van de ene tabel overeenkomt met een waarde in de primaire sleutel van een andere tabel. Bijvoorbeeld: een bestelling moet altijd gekoppeld zijn aan een bestaande klant.

**Waarom gebruiken?** Om relaties tussen tabellen te waarborgen en te voorkomen dat je verwijst naar niet-bestaande records.

**Voorbeeld:**

```sql
CREATE TABLE Order (
    Id INT AUTO_INCREMENT,
    KlantId INT,
    Datum DATE,
    PRIMARY KEY (Id),
    FOREIGN KEY (KlantId) REFERENCES Klant(Id)
);
```

In dit voorbeeld verwijst KlantId in de Order-tabel naar de Id in de Klant-tabel. MySQL zorgt ervoor dat je alleen een KlantId kunt invoeren die al bestaat in de Klant-tabel.

### 4. UNSIGNED

Met UNSIGNED voorkom je dat een numerieke kolom negatieve waarden bevat. Dit is handig voor waarden die nooit negatief kunnen zijn, zoals een leeftijd of een voorraad.

**Waarom gebruiken?** Om te garanderen dat alleen positieve getallen (inclusief 0) worden opgeslagen.

**Voorbeeld:**

```sql
CREATE TABLE Klant (
    Id INT UNSIGNED AUTO_INCREMENT,
    Code CHAR(3),
    Naam VARCHAR(100),
    Leeftijd TINYINT UNSIGNED,
    Email VARCHAR(100),
    Opmerking VARCHAR(250),
    PRIMARY KEY (Id)
);
```

Hier kan Leeftijd alleen 0 of een positief getal zijn (bijvoorbeeld 25), geen -25.

### 5. NOT NULL

De NOT NULL-constraint zorgt ervoor dat een kolom altijd een waarde moet hebben. Een lege waarde (NULL) is niet toegestaan.

**Waarom gebruiken?** Om te garanderen dat essentiële gegevens altijd worden ingevuld, zoals een naam of e-mailadres.

**Voorbeeld:**

```sql
CREATE TABLE Klant (
    Id INT UNSIGNED NOT NULL AUTO_INCREMENT,
    Code CHAR(3) NOT NULL,
    Naam VARCHAR(100) NOT NULL,
    Leeftijd TINYINT UNSIGNED NOT NULL,
    Email VARCHAR(100) NOT NULL,
    Opmerking VARCHAR(250) NULL,
    PRIMARY KEY (Id)
);
```

Hier moeten Code, Naam, Leeftijd en Email altijd een waarde hebben, maar Opmerking mag leeg (NULL) zijn.

### 6. DEFAULT

Met de DEFAULT-constraint geef je een standaardwaarde aan een kolom als er bij het invoeren geen waarde wordt opgegeven.

**Waarom gebruiken?** Om een logische standaardwaarde te gebruiken als de gebruiker geen waarde invult.

**Voorbeeld:**

```sql
CREATE TABLE Klant (
    Id INT UNSIGNED NOT NULL AUTO_INCREMENT,
    Code CHAR(3) NOT NULL,
    Naam VARCHAR(100) NOT NULL,
    Leeftijd TINYINT UNSIGNED NOT NULL,
    Email VARCHAR(100) NOT NULL,
    Opmerking VARCHAR(250) NULL DEFAULT 'Geen opmerkingen',
    PRIMARY KEY (Id)
);
```

Als je een klant toevoegt zonder een opmerking, krijgt de kolom Opmerking automatisch de waarde 'Geen opmerkingen'.

### 7. UNIQUE

De UNIQUE-constraint zorgt ervoor dat alle waarden in een kolom uniek zijn. Dit lijkt op een PRIMARY KEY, maar een tabel kan meerdere UNIQUE-kolommen hebben.

**Waarom gebruiken?** Om te voorkomen dat dubbele waarden worden opgeslagen, zoals unieke e-mailadressen of codes.

**Voorbeeld:**

```sql
CREATE TABLE Klant (
    Id INT UNSIGNED NOT NULL AUTO_INCREMENT,
    Code CHAR(3) NOT NULL UNIQUE,
    Naam VARCHAR(100) NOT NULL,
    Leeftijd TINYINT UNSIGNED NOT NULL,
    Email VARCHAR(100) NOT NULL UNIQUE,
    Opmerking VARCHAR(250) NULL DEFAULT 'Geen opmerkingen',
    PRIMARY KEY (Id)
);
```

Hier mag elke Code en Email maar één keer voorkomen in de tabel.

### 8. CHECK

Met de CHECK-constraint kun je specifieke regels instellen waaraan de waarden in een kolom moeten voldoen. Bijvoorbeeld: een leeftijd moet altijd 18 of hoger zijn.

**Waarom gebruiken?** Om extra controle toe te voegen aan de waarden die in een kolom worden opgeslagen.

**Voorbeeld:**

```sql
CREATE TABLE Klant (
    Id INT UNSIGNED NOT NULL AUTO_INCREMENT,
    Code CHAR(3) NOT NULL UNIQUE,
    Naam VARCHAR(100) NOT NULL,
    Leeftijd TINYINT UNSIGNED NOT NULL,
    Email VARCHAR(100) NOT NULL UNIQUE,
    Opmerking VARCHAR(250) NULL DEFAULT 'Geen opmerkingen',
    PRIMARY KEY (Id),
    CHECK (Leeftijd >= 18)
);
```

Hier zorgt de CHECK-constraint ervoor dat de Leeftijd altijd 18 of hoger is. Als je probeert een klant toe te voegen met een leeftijd van 17, geeft MySQL een foutmelding.

### 9. INDEX

Een INDEX is geen echte constraint, maar een hulpmiddel om zoekopdrachten en het ophalen van gegevens sneller te maken. Het is als een inhoudsopgave in een boek: het helpt MySQL sneller de juiste gegevens te vinden.

**Waarom gebruiken?** Om de prestaties van je database te verbeteren, vooral bij grote tabellen.

**Voorbeeld:**

```sql
CREATE INDEX idx_naam ON Klant (Naam);
```

Dit maakt een index op de Naam-kolom, zodat zoekopdrachten op naam sneller worden uitgevoerd.

## Constraints Toevoegen met CREATE TABLE en ALTER TABLE

Je kunt constraints toevoegen wanneer je een tabel maakt (met CREATE TABLE) of achteraf aanpassen (met ALTER TABLE).

### Voorbeeld met CREATE TABLE

Het bovenstaande voorbeeld van de Klant-tabel laat zien hoe je constraints toevoegt bij het maken van een tabel.

### Voorbeeld met ALTER TABLE

Als je een bestaande tabel wilt aanpassen, kun je constraints toevoegen met ALTER TABLE. Bijvoorbeeld, om een UNIQUE-constraint toe te voegen aan de Email-kolom:

```sql
ALTER TABLE Klant
ADD CONSTRAINT unique_email UNIQUE (Email);
```

## Relaties Tussen Tabellen met FOREIGN KEY

De FOREIGN KEY is cruciaal voor het maken van relaties tussen tabellen. Bijvoorbeeld, in een webshop wil je dat elke bestelling (Order) gekoppeld is aan een bestaande klant (Klant). De FOREIGN KEY zorgt ervoor dat je geen bestelling kunt toevoegen voor een klant die niet bestaat.

**Voorbeeld:**

```sql
CREATE TABLE Klant (
    Id INT UNSIGNED NOT NULL AUTO_INCREMENT,
    Naam VARCHAR(100) NOT NULL,
    PRIMARY KEY (Id)
);

CREATE TABLE Order (
    Id INT AUTO_INCREMENT,
    KlantId INT,
    Datum DATE,
    PRIMARY KEY (Id),
    FOREIGN KEY (KlantId) REFERENCES Klant(Id)
);
```

Als je nu een bestelling probeert toe te voegen met een KlantId die niet in de Klant-tabel staat, geeft MySQL een foutmelding.

## Fouten door Constraints Herkennen en Oplossen

Als je een constraint schendt, geeft MySQL een foutmelding. Hier zijn enkele veelvoorkomende fouten en hoe je ze oplost:

1. **PRIMARY KEY fout**: Je probeert twee rijen met dezelfde Id in te voegen.
    
    - **Oplossing**: Zorg ervoor dat de Id uniek is of gebruik AUTO_INCREMENT.
        
2. **FOREIGN KEY fout**: Je probeert een KlantId in de Order-tabel in te voegen die niet bestaat in de Klant-tabel.
    
    - **Oplossing**: Controleer of de klant bestaat voordat je de bestelling toevoegt.
        
3. **NOT NULL fout**: Je probeert een rij toe te voegen zonder een waarde in te vullen voor een NOT NULL-kolom.
    
    - **Oplossing**: Geef een waarde op voor de verplichte kolom.
        
4. **CHECK fout**: Je probeert een waarde in te voegen die niet voldoet aan de CHECK-regel (bijvoorbeeld een leeftijd van 15 terwijl Leeftijd >= 18 vereist is).
    
    - **Oplossing**: Zorg ervoor dat de waarde voldoet aan de regel.
        

**Voorbeeld van een foutmelding:**

```sql
INSERT INTO Klant (Id, Naam, Leeftijd) VALUES (1, 'Jan', 15);
```

Als er een CHECK (Leeftijd >= 18) is, geeft MySQL een foutmelding zoals: CHECK constraint failed.

## Samenvatting

MySQL constraints zijn essentieel voor het beheren van de integriteit en consistentie van je database. Ze zorgen ervoor dat je gegevens betrouwbaar zijn en dat je database logisch blijft werken, zelfs als er fouten worden gemaakt bij het invoeren van gegevens. Door constraints zoals PRIMARY KEY, FOREIGN KEY, NOT NULL, UNIQUE, CHECK, DEFAULT en AUTO_INCREMENT te gebruiken, kun je je database robuuster en efficiënter maken.