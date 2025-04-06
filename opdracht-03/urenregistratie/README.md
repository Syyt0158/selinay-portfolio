# Urenregistratie Project

Dit is een frontend urenregistratie-tool waarin je jouw gewerkte uren per project en per week kunt bijhouden. Het project ondersteunt weeknavigatie, automatische opslag via `localStorage`, en een dark mode. 

## Features

- Selecteerbare weken (1 t/m 52) met dynamische datums
- Ureninvoer per dag en project
- Automatische berekening van totaaluren per project
- Opslaan van gegevens per week in `localStorage`
- Dark mode toggle
- Live projectgegevens ophalen via API (vereist geldige token in `localStorage`)
- Week navigatie (volgende/vorige/today)
- Logout functionaliteit
- **HTTPS hosting via Vite**


## Installatie en Setup

### 1. Installeer Node.js

Als je Node.js nog niet hebt geïnstalleerd, download en installeer het via:  
- [https://nodejs.org/](https://nodejs.org/)

### 2. Open de juiste map

Open je terminal (of cmd/PowerShell) en ga naar de map van het project, bijvoorbeeld:

```bash
cd urenregistratie
```

Zorg dat je je bevindt in de map die `index.html` bevat.

### 3. Installeer npm packages

Voer dit uit om alle benodigde packages (zoals Vite) te installeren:

```bash
npm install
```

### 4. Start de ontwikkelserver via Vite (met HTTPS)

Gebruik dit commando om de server te starten:

```bash
npm run dev
```

Na enkele seconden zie je een link zoals:

```
Local: https://localhost:5173/
```

- Houd `Ctrl` ingedrukt en klik op de link  
of  
- Kopieer en plak de link in je browser.

> Je moet **inlog.html** gebruiken als startpunt voor de login.

## Inloggen

Na het inloggen kom je in de urenregistratie pagina terecht waar je je uren kunt loggen. De uren worden erna opgeslagen in de localstorage.

## Dark Mode

Klik op het maantje/zonnetje icoon om te schakelen tussen light en dark mode. Je voorkeur wordt automatisch opgeslagen.

## Uitloggen

Gebruik de `Logout` knop om alle opgeslagen gegevens in `localStorage` en `sessionStorage` te wissen en terug te keren naar de inlogpagina.

---

Gemaakt door Selinay Yigit
