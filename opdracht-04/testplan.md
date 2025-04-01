**Testplan**

### 1. Inleiding  
Dit testplan beschrijft de handmatige teststrategie voor de urenregistratie-website. De testen zijn gebaseerd op de opgestelde user stories en hebben als doel de correcte werking van de applicatie te verifiëren.

### 2. Teststrategie  
De testen worden handmatig uitgevoerd en richten zich op functionele aspecten zoals het invoeren van uren, het wisselen tussen weken en het inloggen. Er wordt getest op verschillende invoerscenario's, zowel positief als negatief.

### 3. Te testen functionaliteiten  
De volgende functionaliteiten worden getest:  
1. **Urenregistratie per dag** (User Story 1)  
2. **Inloggen met een Clockwise account** (User Story 2)  
3. **Navigatie tussen verschillende weken** (User Story 4)  

## Testscenario’s

### **Scenario 1: Urenregistratie per dag**  
**Beschrijving:** De gebruiker moet in staat zijn om uren in te voeren en op te slaan per dag.  

#### Testdata:  
- Geldige invoer: 8 uur, 4.5 uur  
- Ongeldige invoer: -3 uur, 25 uur, leeg veld  

#### Stappen:  
1. Open de urenregistratiepagina.  
2. Klik op een invoerveld en voer een aantal uren in.  

#### Verwachte resultaten:  
- Geldige invoer wordt correct opgeslagen en weergegeven.  
- Ongeldige invoer (negatief/getal > 24/leeg) resulteert in een foutmelding.  

### **Scenario 2: Inloggen met een Clockwise account**  
**Beschrijving:** De gebruiker moet kunnen inloggen met een geldig account en foutmeldingen ontvangen bij ongeldige invoer.  

#### Testdata:  
- Geldige inloggegevens: [gebruikersnaam] / [wachtwoord]  
- Ongeldige inloggegevens: [ongeldig e-mailadres] / [ongeldig wachtwoord]  

#### Stappen:  
1. Open de inlogpagina.  
2. Voer e-mailadres en wachtwoord in.  
3. Klik op de inlogknop.  

#### Verwachte resultaten:  
- Bij correcte inloggegevens wordt de gebruiker doorgestuurd naar de urenregistratiepagina.  
- Bij incorrecte gegevens verschijnt een foutmelding.  

### **Scenario 3: Navigatie tussen verschillende weken**  
**Beschrijving:** De gebruiker moet kunnen navigeren tussen weken zonder fouten.  

#### Testdata:  
- Navigeren naar vorige/volgende week  
- Snel meerdere keren op navigatieknoppen klikken  

#### Stappen:  
1. Open de urenregistratiepagina.  
2. Klik op de knop om naar de vorige week te navigeren.  
3. Controleer of de juiste week wordt weergegeven.  

#### Verwachte resultaten:  
- De juiste week wordt correct weergegeven.  
- Bij te snel klikken blijft de interface correct functioneren.  

### **Scenario 4: Weergave van het totaal aantal uren per week**  
**Beschrijving:** De gebruiker moet het totaal aantal uren van de huidige week kunnen zien.  

#### Testdata:  
- Uren per dag: 8 uur, 6 uur, 7 uur, etc.  

#### Stappen:  
1. Open de urenregistratiepagina.  
2. Voer uren in voor elke dag van de week.  
3. Controleer of het totaal aantal uren correct wordt weergegeven in de kalender.  

#### Verwachte resultaten:  
- Het totaal aantal uren per week wordt correct berekend en weergegeven in de kalender.  

### **Scenario 5: Schakelen tussen lichte en donkere modus**  
**Beschrijving:** De gebruiker moet de applicatie kunnen schakelen tussen lichte en donkere modus.  

#### Testdata:  
- Lichte modus is ingeschakeld bij de start.  
- Donkere modus is ingeschakeld door de gebruiker.  

#### Stappen:  
1. Open de urenregistratiepagina.  
2. Schakel tussen lichte en donkere modus via de knop in de interface.  
3. Controleer of de stijl correct wordt aangepast.  

#### Verwachte resultaten:  
- De interface verandert van licht naar donker en vice versa, zonder visuele fouten.  

## **Testrapport**

### 1. **Testresultaten**  
De tests zijn uitgevoerd op [01-04-2025]. Hieronder de resultaten:

| Testscenario | Verwacht resultaat | Werkelijk resultaat | Status |
|-------------|--------------------|---------------------|--------|
| Uren invoeren | Uren worden opgeslagen | Uren correct opgeslagen | Geslaagd |
| Negatief getal invoeren | Foutmelding verschijnt | Geen foutmelding | Mislukt |
| Meer dan 24 uur invoeren | Foutmelding verschijnt | Geen foutmelding | Mislukt |
| Geldig inloggen | Gebruiker wordt ingelogd | Gebruiker wordt ingelogd | Geslaagd |
| Verkeerd inloggen | Foutmelding verschijnt | Foutmelding verschijnt | Geslaagd |
| Navigeren naar vorige week | Correcte week wordt weergegeven | Correcte week weergegeven | Geslaagd |

### 2. **Conclusie**  
De meeste testen zijn succesvol verlopen. Er is een probleem met de invoer van meer dan 24 uur, wat opgelost moet worden door een invoerbeperking toe te voegen. Over het algemeen functioneert de applicatie zoals verwacht.
