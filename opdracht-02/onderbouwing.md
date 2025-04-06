# Onderbouwing van het Sequence Diagram

## Inleiding
Het sequence diagram visualiseert de interactie tussen de gebruiker, browser, API en local storage tijdens het inlog- en urenregistratieproces binnen de applicatie. Dit diagram is ontworpen om duidelijk te maken hoe gegevens stromen tussen de componenten van het systeem, en hoe gebruikersinteractie leidt tot acties.

---

## Toelichting van het Proces

### 1. Inlogproces
- De gebruiker voert zijn gebruikersnaam en wachtwoord in via de browserinterface.
- Deze gegevens worden doorgestuurd naar de API.
- Afhankelijk van de juistheid van de inloggegevens zijn er twee paden:
  - **Correcte inloggegevens**:
    - De API stuurt een authenticatietoken terug.
    - De browser bevestigt de login en vraagt vervolgens klant- en projectgegevens op.
    - De API levert deze gegevens aan, waarna de browser ze toont in een tabel.
  - **Incorrecte inloggegevens**:
    - De API retourneert een foutmelding.
    - De browser toont deze foutmelding aan de gebruiker.

### 2. Urenregistratie
- Nadat klanten en projecten geladen zijn, kan de gebruiker uren invoeren.
- Deze uren worden zowel in de browser bijgewerkt als opgeslagen in de local storage.
- De browser update de tabel met de ingevoerde uren.

### 3. Darkmode en Lightmode
- De gebruiker kan wisselen tussen dark- en lightmode.
- Bij activatie van de darkmode wordt `dark-mode = true` opgeslagen in de local storage
- De browser werkt het icoon bij en past de darkmode toe op de interface.
- Hetzelfde proces geldt omgekeerd voor de lightmode (`dark-mode = false`).

---

## Waarom dit diagram?
Dit diagram is opgesteld om inzicht te geven in de logische volgorde van gebeurtenissen binnen de applicatie, met specifieke nadruk op:
- Authenticatie tijdens het inloggen
- Het laten zien van klanten, projecten en uren
- UI-interacties zoals dark/light mode
- Opslag van data in local storage voor behoud van gegevens bij het vernieuwen van de pagina

Door de betrokken componenten (browser, API, local storage) apart weer te geven, wordt duidelijk wie welke verantwoordelijkheid draagt binnen het systeem.

---

## Conclusie
Het sequence diagram ondersteunt de ontwikkeling en documentatie van het systeemontwerp. Het helpt bij het begrijpen van de gebruikerservaring en het gedrag van de applicatie. 