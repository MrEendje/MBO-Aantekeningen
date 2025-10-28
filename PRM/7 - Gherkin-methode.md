	# Gherkin-methode

## 7.1 Introductie

**Wat is de Gherkin-methode?**

De Gherkin-methode is een gestructureerde taal om tests en softwaregedrag te beschrijven.  
Ze wordt gebruikt in Behavior-Driven Development (BDD) om verwachtingen over functionaliteit duidelijk vast te leggen.  
Het doel: iedereen (ontwikkelaars, testers en niet-technische stakeholders) begrijpt wat een systeem moet doen.

---

## 7.2 Leerdoelen

In deze les leer je:

- Wat de Gherkin-methode is  
- De structuur van Gherkin  
- De belangrijkste elementen  
- Voorbeelden van Gherkin-scenario’s  

---

## 7.3 Waarom Gherkin-methode?

**Waar zorgt de Gherkin-methode voor?**

- Minder risico op foute analyse  
- Acceptatiecriteria snel implementeerbaar  
- Alleen de juiste dingen testen  
- Duidelijk commitment van stakeholders  
- Sneller testen  
- Ondersteuning bij beslissingen  

**Waarom Gherkin gebruiken?**

### Duidelijkheid
Gherkin gebruikt natuurlijke taal, dus het is begrijpelijk voor iedereen.

### Samenwerking
Het bevordert samenwerking tussen ontwikkelaars, testers en zakelijke belanghebbenden.

### Automatisering
Scenario’s kunnen worden omgezet in geautomatiseerde tests, wat het testproces versnelt.

---

## 7.4 User Story elementen van Gherkin

**Feature (User Story - max 5 regels)**  
Een feature heeft een titel en een beschrijving.  
Deze worden gebruikt voor documentatie.

### Engels voorbeeld:
```
As a <role>
I want to <action>
So that <benefit / business value>
```

### Nederlands voorbeeld:
```
Als een <Rol: eindgebruiker, manager …> (wie)
Wil ik <Actie / functionaliteit> (wat)
Zodat <Voordeel / toegevoegde waarde> (waarom)
```

---

## 7.5 Scenario elementen van Gherkin

Een feature bevat één happy scenario en één of meer unhappy scenario’s.

### Belangrijke sleutelwoorden:
- **Feature** – beschrijft een functie of eigenschap  
- **Scenario** – beschrijft een specifiek gebruiksgeval  
- **Gegeven (Given)** – stelt de beginsituatie vast  
- **Wanneer (When)** – beschrijft de actie  
- **Dan (Then)** – beschrijft het verwachte resultaat  
- **En (And)** – voegt extra context of acties toe  
- **Maar (But)** – beschrijft uitzonderingen  
- **Achtergrond (Background)** – gedeelde context  
- **Scenario Outline** – herbruikbaar scenario met variaties  
- **Voorbeelden (Examples)** – data voor Scenario Outlines

### Engels structuur:
```
Title
Given
And
When
And
Then 
And 
But 
Background 
Scenario Outline
Examples
```

### Nederlands structuur:
```
Titel
Gegeven
En
Wanneer
En
Dan
En
Maar
Achtergrond
Scenario Outline
Voorbeelden
```

---

## 7.6 Engels voorbeeld van Gherkin

```
Feature: Create an account in Facebook for a user.
As a general user
I want to create an account in Facebook
So that I can expand my network in social media.

Scenario: Successful creation of a Facebook account
Given I am signing up for Facebook
When I enter the required details
And submit my request
Then a Facebook account is created
And the account name is set as my email address
And a confirmation email is sent to me

Scenario: Unsuccessful creation of a Facebook account
Given I am signing up for Facebook
When I enter invalid details
And submit my request
Then I get an error message “Your password does not meet the requirements”
```

---

## 7.7 Nederlands voorbeeld van Gherkin

```
Feature: Winkelwagentje vullen in webshop
Als een digitale klant
Wil ik items in mijn winkelwagentje stoppen
Zodat ik al mijn items heb verzameld voordat ik betaal

Scenario: Het toevoegen van een item aan het winkelwagentje is succesvol
Gegeven ik ben op de homepagina
Wanneer ik een item kies van de productpagina
En ik klik op “Toevoegen” om het item in mijn winkelwagentje te stoppen
Dan neemt het aantal items in mijn winkelwagentje toe
En het subtotaal neemt toe
En de magazijnvoorraad wordt verlaagd

Scenario: Het toevoegen van een item aan het winkelwagentje is niet succesvol
Gegeven ik ben op de homepagina
Wanneer ik een item kies van de productpagina
En ik klik op “Toevoegen” om het item in mijn winkelwagentje te stoppen
Dan krijg ik een foutmelding “Het gekozen artikel is niet op voorraad”
```

---

## 7.8 Extra voorbeeld van Gherkin

```
Feature: De leerkracht wil een boek zoeken
Als een leerkracht
Wil ik zoeken naar een boek met de titel als trefwoord
Zodat ik de prijs en de beschikbaarheid van het boek kan controleren

Scenario: Het opzoeken van een boek lukt
Gegeven ik sta in het startscherm
Wanneer ik een titel invoer van een boek dat op voorraad is
En ik druk op de Zoeken-knop
Dan zie ik een lijst van alle gevonden boeken op titel
En de lijst wordt alfabetisch (A-Z) weergegeven
En per resultaat zie ik de prijs en de voorraad

Scenario: Het lukt niet om een boek op te zoeken
Gegeven ik sta in het startscherm
Wanneer ik een verkeerde titel invoer
En ik druk op de Zoeken-knop
Dan krijg ik een foutmelding “Het gezochte boek is niet gevonden.”
```

---

	## 7.9 Andere variant van Gherkin

```
Feature: Account maken
Als een gebruiker
Wil ik een nieuw account op de website aanmaken
Zodat ik mijn privéomgeving kan gebruiken

Scenario: Registreer de gebruiker en controleer of de gebruiker ingelogd is
Gegeven ik open de ontwikkelwebsite
Wanneer ik klik op de registratielink
En ik voer <gebruikersnaam>, <wachtwoord> en <bevestigen wachtwoord> in
Dan zie ik de site als ingelogd met de gebruikersnaam

Voorbeelden:
| Gebruikersnaam | Wachtwoord  | Bevestigen wachtwoord |
|-----------------|-------------|------------------------|
| Jan             | testuser@123| testuser@123          |
| Sam             | testuser@567| testuser@567          |

Scenario: Registreer de gebruiker kan niet inloggen
Gegeven ik open de ontwikkelwebsite
Wanneer ik klik op de registratielink
En ik voer <gebruikersnaam>, <wachtwoord> en <bevestigen wachtwoord> in
Dan krijg ik een <foutmelding> te zien

Voorbeelden:
| Gebruikersnaam | Wachtwoord  | Bevestigen wachtwoord | Foutmelding |
|-----------------|-------------|------------------------|-------------|
| Jan             | testuser@123| testuser@123          | Ongeldige gebruikersnaam of wachtwoord |
| Sam             | testuser@567| testuser@567          | Ongeldige gebruikersnaam of wachtwoord |
```
