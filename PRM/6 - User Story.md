# 6.1 Introductie — Wat is een User Story

Een **User Story** is een korte, eenvoudige beschrijving van een functie of eigenschap  
die een gebruiker nodig heeft in een product.  

Het doel van een User Story is:
- Teams helpen te begrijpen **wat** de gebruiker wil.  
- Inzicht geven in **waarom** de gebruiker dat wil.  
- Zich te richten op het leveren van **waardevolle functionaliteiten**.  

---

# 6.3 Big Picture

## Definitie
Een **User Story** is een korte beschrijving van een eindgebruikersbehoefte, geschreven vanuit hun perspectief.

## Doel
Een User Story verduidelijkt **wat** en **waarom** iets nodig is voor de eindgebruiker, zonder in technische details te treden.

## Product Backlog
User Stories worden geschreven door de **Product Owner** en zijn onderdeel van de **Product Backlog**,  
de geprioriteerde lijst van werk die het team uitvoert.

## Waardecreatie
Ontwikkelaars werken de User Stories uit de backlog uit, wat **waarde oplevert voor de eindgebruiker**.  
Samen vertegenwoordigen alle User Stories de totale waarde die een project levert.

---

# 6.4 Waarom zijn User Stories nuttig?

## Duidelijkheid
User Stories maken duidelijk wat de gebruiker nodig heeft en waarom.

## Focus
Ze helpen het team zich te concentreren op wat echt belangrijk is voor de gebruiker.

## Communicatie
Ze bevorderen goede communicatie tussen teamleden en belanghebbenden.

---

## Hoe gebruik je User Stories?

1. **Schrijf de verhalen**  
   Noteer de wensen en behoeften van de gebruikers in de juiste structuur.

2. **Bespreek ze**  
   Zorg dat iedereen begrijpt wat elke User Story betekent.

3. **Prioriteer ze**  
   Bepaal welke User Stories het belangrijkst zijn en werk daar eerst aan.

4. **Werk ze uit**  
   Breek de User Stories op in kleinere, uitvoerbare en testbare taken.

---

# 6.5 Structuur van een User Story

## Algemene structuur
Een User Story bestaat uit drie vaste onderdelen:

> Als **[rol/gebruiker]**  
> wil ik **[actie of doel]**  
> zodat **[reden of voordeel]**

## Voorbeeld
**Feature:** Zoek een boek in de bibliotheek

> Als lid van de bibliotheek  
> wil ik boeken kunnen zoeken  
> zodat ik snel een boek kan vinden om te lenen.

**Bijbehorende taken:**
- Zoekfunctie toevoegen aan de app  
- Lijst met resultaten tonen  
- Detailpagina voor elk boek maken  

Deze User Story maakt duidelijk **wat** er gebouwd moet worden, **voor wie** en **waarom**.

---

# 6.6 Foutieve User Stories en verbeterde versies

Het is belangrijk om User Stories op te splitsen als ze te breed of te complex zijn.  
Hieronder zie je voorbeelden van foutieve en verbeterde User Stories.

---

## Foutieve User Story 1
> Als praktijkmanager  
> wil ik inzicht in de statistieken over het aantal afspraken en omzet  
> zodat ik de praktijkprestaties kan monitoren.

### Verbeterde versie:
**User Story 1:**  
> Als praktijkmanager  
> wil ik inzicht in de statistieken over het aantal afspraken  
> zodat ik kan zien hoe druk de praktijk is en waar verbeteringen nodig zijn.

**User Story 2:**  
> Als praktijkmanager  
> wil ik inzicht in de statistieken over de omzet  
> zodat ik de financiële prestaties van de praktijk kan monitoren.

---

## Foutieve User Story 2
> Als verkoper  
> wil ik kunnen kiezen of ik een stand voor één of twee dagen wil huren  
> zodat ik flexibel kan deelnemen aan het evenement.

### Verbeterde versie:
**User Story 1:**  
> Als verkoper  
> wil ik een stand voor één dag kunnen huren  
> zodat ik kan deelnemen op een specifieke dag.  

**User Story 2:**  
> Als verkoper  
> wil ik een stand voor twee dagen kunnen huren  
> zodat ik de volledige duur van het evenement kan benutten.

---

## Foutieve User Story 3
> Als organisator  
> wil ik het aantal beschikbare tickets per entreetijd kunnen instellen en beheren  
> zodat ik de capaciteit kan controleren.

### Verbeterde versie:
**User Story 1:**  
> Als organisator  
> wil ik het aantal beschikbare tickets per entreetijd kunnen instellen  
> zodat ik de capaciteit kan controleren.

**User Story 2:**  
> Als organisator  
> wil ik het aantal beschikbare tickets per entreetijd kunnen wijzigen  
> zodat ik de capaciteit kan bijwerken.

**User Story 3:**  
> Als organisator  
> wil ik het aantal beschikbare tickets per entreetijd kunnen verwijderen  
> zodat ik de capaciteit kan opruimen.

---

# 6.7 Acceptatiecriteria

## Wat zijn Acceptatiecriteria?
Acceptatiecriteria zijn specifieke **voorwaarden** die bepalen wanneer een User Story  
als **voltooid en succesvol** kan worden beschouwd.  

Ze zorgen voor duidelijkheid over **wat er precies geleverd moet worden**  
en **hoe het resultaat beoordeeld zal worden**.

---

## Waarom zijn Acceptatiecriteria belangrijk?

- **Duidelijkheid:** Iedereen weet wat er verwacht wordt.  
- **Controle:** Ze vormen de basis voor het testen van functionaliteit.  
- **Beheersbaarheid:** Ze maken werk opdeelbaar en testbaar.  
- **Transparantie:** Belanghebbenden weten wanneer een story voltooid is.  

---

## Hoe schrijf je Acceptatiecriteria?

Acceptatiecriteria kunnen worden opgesteld als:
- Een lijst met voorwaarden  
- Of in de vorm van **scenario’s**

---

### Voorbeeld User Story
**Feature:** Product zoeken  
> Als klant  
> wil ik een product kunnen zoeken  
> zodat ik snel vind wat ik nodig heb.

---

### Scenario’s

**Scenario 1: Zoeken met geldige invoer**  
**Gegeven:** Ik ben op de startpagina  
**Wanneer:** Ik voer "laptop" in de zoekbalk in en klik op de zoekknop  
**Dan:** Worden alle beschikbare laptops weergegeven  

**Scenario 2: Zoeken met ongeldige invoer**  
**Gegeven:** Ik ben op de startpagina  
**Wanneer:** Ik voer "xyz123" in de zoekbalk in en klik op de zoekknop  
**Dan:** Wordt een melding weergegeven met “Geen resultaten gevonden.”

---

# 6.8 Tips voor het schrijven van Unhappy Scenario’s

Unhappy scenario’s beschrijven **wat er gebeurt als iets misgaat** of **onjuiste input** wordt gegeven.  
Ze helpen om fouten en uitzonderingen te testen.

---

## Soorten validatie

### Technische validatie (geen unhappy scenario’s)
- Controle op verplichte velden  
- Controle op datatypes van invoervelden  

### Functionele validatie (wel unhappy scenario’s)
- Logische controles  
  - De begindatum mag niet na de einddatum liggen  
  - De einddatum mag niet vóór de begindatum liggen  

### Conceptuele validatie
- Scores mogen niet hoger zijn dan 300 punten  
- Het maximumaantal verlofdagen is 24 per jaar  

---

**Samenvatting:**  
User Stories helpen teams om waarde te leveren vanuit het perspectief van de gebruiker.  
Door duidelijke acceptatiecriteria en unhappy scenario’s toe te voegen, wordt het product betrouwbaarder, beter getest en beter afgestemd op de behoeften van de gebruiker.
