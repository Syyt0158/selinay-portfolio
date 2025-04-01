# Verbeterpunten op Basis van Testresultaten

1. **Foutmeldingen voor ongeldige ureninvoer**  
   - **Probleem**: Bij het invoeren van negatieve uren of uren groter dan 24, wordt geen foutmelding weergegeven.
   - **Oplossing**: Voeg invoerbeperkingen toe voor ureninvoer om negatieve waarden en waarden groter dan 24 te blokkeren. Implementeer daarnaast foutmeldingen voor deze gevallen zodat de gebruiker duidelijk weet wat er mis is.
   - **Prioriteit**: Hoog, omdat dit de gebruiksvriendelijkheid verbetert en de juiste functionaliteit garandeert.

2. **Beperkingen voor invoervelden toevoegen**  
   - **Probleem**: De invoervelden accepteren momenteel elke waarde zonder beperking.
   - **Oplossing**: Beperk de invoer tot geldige getallen, bijvoorbeeld door een maximum van 24 uur per dag in te stellen. Zorg ervoor dat de interface visuele feedback geeft wanneer de invoer buiten het toegestane bereik valt.

3. **Validatie van uren per dag**  
   - **Probleem**: Er is geen controle voor het aantal ingevoerde uren per dag, wat kan leiden tot foutieve gegevensinvoer.
   - **Oplossing**: Implementeer een validatiemechanisme dat controleert of de ingevoerde uren realistisch zijn en binnen de gedefinieerde grenzen vallen (0-24 uur).

---

# Teststrategie Verbeteringen

Op basis van de resultaten kan de teststrategie verder worden aangepast voor toekomstige iteraties van het project:

1. **Toevoegen van gedetailleerdere negatieve testgevallen**:
   - Het testen van invoerwaarden boven de 24 uur moet worden uitgebreid met meerdere negatieve testgevallen. Denk hierbij aan het
   invoeren van niet-numerieke waarden, tekst, en speciale karakters.

2. **Verbeteren van de validatie van ureninvoer**:
    - Testen of de validatie goed werkt bij verschillende invoerscenario’s, zoals het invoeren van lege velden, negatieve getallen, of getallen boven 24 uur, en ervoor zorgen dat foutmeldingen duidelijk en begrijpelijk zijn voor de gebruiker.

3. **Testen van de foutafhandelingslogica voor snellere navigatie**:
    - Voer tests uit waarbij de gebruiker snel achter elkaar op de navigatieknoppen klikt om naar vorige of volgende weken te gaan, en controleer of de applicatie goed omgaat met deze snelle interacties zonder vertragingen of fouten.

---

# Reflectie op het Testproces

De testresultaten zijn over het algemeen positief, maar enkele belangrijke issues moeten worden aangepakt voordat de applicatie als "klaar" kan worden beschouwd. Het niet tonen van foutmeldingen bij ongeldige invoer is een belangrijke bevinding die prioriteit moet krijgen.   

### Aanbevolen vervolgstappen:

- Focus op het verbeteren van de foutmeldingen en validaties in de ureninvoer.
- Test de wijzigingen en validaties opnieuw na implementatie van de verbeteringen.
- Voer extra negatieve testgevallen uit voor de ureninvoer, zoals niet-numerieke waarden of ongeldige tekens, om te verifiëren dat de applicatie correct reageert op ongeldige invoer.

Met deze verbeteringen zou de urenregistratie-app nog gebruiksvriendelijker worden.
