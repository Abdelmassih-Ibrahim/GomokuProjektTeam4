# Icke-funktionella krav för Gomoku

Vilka egenskaper ett system behöver ha är väldigt viktigt för användarupplevelsen. Kraven är framtagna genom en intervju med kunden. Under intervjun ställdes frågor kring hur snabbt spelet ska fungera, vilka enheter kunden använder men även vad som händer om anslutningen till internet plötsligt försvinner.

# Systemets icke-funktionella krav:

| ID     | KRAV                                                                                                                                                                                                                                    |
| ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NFR-01 | Användarvänlighet: Spelet ska vara enkelt att förstå och använda även för en person utan teknisk kunskap                                                                                                                                |
| NFR-02 | Responsiv design:	Spelplan, knappar och information ska fungera och anpassas till mobil och dator.                                                                                                                                      |
| NFR-03 | Prestanda: Efter att användaren klickar på en giltig position ska stenen visas inom 100 ms under normal användning.                                                                                                                     |
| NFR-04 | Anonym användning: Användaren ska kunna spela utan att skapa konto eller logga in.                                                                                                                                                      |
| NFR-05 | Kompatibilitet: Spelet ska fungera på mobil och dator direkt i webbläsaren utan installation.                                                                                                                                           |
| NFR-06 | Anslutning via länk: Två spelare ska kunna spela tillsammans från samma eller olika platser.                                                                                                                                            |
| NFR-07 | Tillförlitlighet: Spelet ska kunna hantera tillfälligt internetavbrott utan att matchen förloras                                                                                                                                        |
| NFR-08 | Säkerhet och integritet: Personlig information ska inte krävas för att spela och ska inte finnas i inbjudningslänken.                                                                                                                   |
| NFR-09 | Visuell/UI-stabilitet: Spelplanens storlek, position och även rutornas dimensioner ska fortsätta vara oförändrade när en sten placeras. Placera flera stenar och kontrollera att brädet inte krymper, flyttar sig eller ändrar storlek. |
| NFR-10 | Brädans tillstånd ska vara konsekvent för båda spelarna i en match som sker på distans.                                                                                                                                                 |

## BDD-förtydliganden

BDD används här för att förtydliga de icke-funktionella krav som vi tyckte var större eller innehåller flera olika olika beteenden. Alla krav har inte ett eget BDD-scenario för dem kanske var tydliga redan.

# NFR-01 – Användarvänlighet

```gherkin
Scenario 1: Användaren ska kunna förstå hur spelet används
- Given: att användaren öppnar spelet
- When: användaren ska starta och spela en match
- Then: ska det vara tydligt hur spelet startas
- And: ska det vara tydligt hur en sten placeras
- And: ska det vara tydligt vems tur det är
- And: användaren ska kunna förstå spelets grundläggande funktioner utan teknisk kunskap
```

# NFR-02 – Responsiv design

```gherkin
Scenario 1: Spelet används på mobil
- Given: att användaren öppnar spelet på en mobil
- When: spelplanen visas
- Then: ska spelplanen anpassas efter skärmens storlek
- And: knappar ska fungera
- And: information ska vara synlig
- And: användaren ska kunna genomföra ett drag
```

```gherkin
### Scenario 2: Spelet används på dator
- Given: att användaren öppnar spelet på en dator
- When: spelplanen visas
- Then: ska spelplanen anpassas efter skärmens storlek
- And: knappar ska fungera
- And: information ska vara synlig
- And: användaren ska kunna genomföra ett drag
```

# NFR-05 – Kompatibilitet

```gherkin
Scenario 1: Spelet öppnas direkt i webbläsaren
- Given: att användaren använder en mobil eller dator
- When: användaren öppnar spelet i en webbläsare
- Then: ska spelet kunna användas direkt
- And: användaren ska inte behöva installera något
```

# NFR-06 – Anslutning via länk

```gherkin
### Scenario 1: Två spelare spelar tillsammans via en länk
- Given: att en spelare har skapat en match
- And: att spelaren har en giltig spellänk
- When: en annan spelare öppnar länken
- Then: ska den andra spelaren kunna ansluta till samma match
- And: båda spelarna ska kunna spela tillsammans
- And: spelarna ska kunna befinna sig på samma eller olika platser
```

# NFR-07 – Tillförlitlighet

```gherkin
### Scenario 1: Matchen förloras inte vid tillfälligt internetavbrott

- Given: att två spelare befinner sig i en pågående match
- When: en spelares internetanslutning tillfälligt bryts
- Then: ska matchen inte förloras
- And: den senaste giltiga spelstatusen ska finnas kvar
- And: spelaren ska kunna fortsätta matchen efter återanslutning
```

# NFR-08 – Säkerhet och integritet

```gherkin
### Scenario 1: Spelaren kan spela utan personlig information
- Given: att användaren vill spela
- When: användaren startar eller ansluter till en match
- Then: ska personlig information inte krävas
- And: användaren ska inte behöva skapa ett konto
- And: användaren ska inte behöva logga in
```

```gherkin
### Scenario 2: Inbjudningslänken innehåller ingen personlig information
- Given: att systemet har skapat en inbjudningslänk
- When: användaren delar länken
- Then: ska länken inte innehålla personlig information
- And: länken ska kunna användas av den andra spelaren för att ansluta till matchen
```

# NFR-09 – Visuell/UI-stabilitet

```gherkin
Scenario 1: En sten placeras på spelplanen
- Given: att spelplanen visas
- When: användaren placerar en sten
- Then: ska spelplanens storlek vara oförändrad
- And: spelplanens position ska vara oförändrad
- And: rutornas dimensioner ska vara oförändrade
```

### Scenario 2: Flera stenar placeras på spelplanen

```gherkin
- Given: att flera stenar redan finns på spelplanen
- When: användaren placerar ytterligare en sten
- Then: ska brädet inte krympa
- And: brädet ska inte flytta sig
- And: brädet ska inte ändra storlek
```

# NFR-10 – Brädans tillstånd

```gherkin
### Scenario 1: Samma brädstatus visas för båda spelarna
- Given: att två spelare befinner sig i samma match
- And: att båda spelarna är anslutna
- When: en spelare placerar en sten
- Then: ska stenen visas på samma position för båda spelarna
- And: brädans tillstånd ska vara samma för båda spelarna
- And: aktuell tur ska uppdateras
```

## Internetavbrott

| ID     | KRAV                                                                                                                                                                   |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NFR-11 | Ett tillfälligt internetavbrott ska inte automatiskt avsluta en pågående match som sker på distans mellan två spelare                                                  |
| NFR-12 | När spelaren återansluter ska systemet alltid återställa den senaste giltiga spelstatus, tillstånd och turordning. (Om motståndaren inte har valt att avsluta matchen) |


# NFR-11 – Tillfälligt internetavbrott
```gherkin
### Scenario 1: Matchen avslutas inte automatiskt vid internetavbrott
- Given: att två spelare har en pågående match på distans
- When: en spelares internetanslutning tillfälligt bryts
- Then: ska matchen inte automatiskt avslutas
- And: den senaste giltiga spelstatusen ska finnas kvar
- And: matchen ska kunna fortsätta efter återanslutning
```


# NFR-12 – Återställning efter återanslutning
```gherkin
### Scenario 1: Matchen återställs efter återanslutning
- Given: att två spelare har en pågående match på distans
- And: att spelplanen innehåller flera placerade stenar
- And: att en spelares internetanslutning har brutits
- And: att motståndaren inte har avslutat matchen
- When: spelaren återansluter
- Then: ska den senaste giltiga spelstatusen återställas
- And: spelplanens tillstånd ska återställas
- And: rätt spelares tur ska visas
- And: matchen ska kunna fortsättas
```

## Anonymt spelande

| ID     | KRAV                                                                                                       |
| ------ | ---------------------------------------------------------------------------------------------------------- |
| NFR-13 | Spelet ska alltid kunna användas direkt i en webbläsare utan att spelaren behöver installera något program |
| NFR-14 | Spelet ska kunna användas på både datorer och mobiltelefoner                                               |


# NFR-14 – Spelet fungerar på datorer och mobiltelefoner
```gherkin
Scenario 1: Spelet används på dator
- Given: att användaren använder en dator
- When: användaren öppnar spelet
- Then: ska spelet kunna användas
- And: spelets funktioner ska vara tillgängliga
```

```gherkin
Scenario 2: Spelet används på mobiltelefon
- Given: att användaren använder en mobiltelefon
- When: användaren öppnar spelet
- Then: ska spelet kunna användas
- And: spelets funktioner ska vara tillgängliga
```

```mermaid
flowchart TD

    A["Icke-funktionella krav för Gomoku"]

    A --> B["Systemets icke-funktionella krav"]

    B --> NFR01["NFR-01<br/>Användarvänlighet"]
    B --> NFR02["NFR-02<br/>Responsiv design"]
    B --> NFR03["NFR-03<br/>Prestanda"]
    B --> NFR04["NFR-04<br/>Anonym användning"]
    B --> NFR05["NFR-05<br/>Kompatibilitet"]
    B --> NFR06["NFR-06<br/>Anslutning via länk"]
    B --> NFR07["NFR-07<br/>Tillförlitlighet"]
    B --> NFR08["NFR-08<br/>Säkerhet och integritet"]
    B --> NFR09["NFR-09<br/>Visuell stabilitet"]
    B --> NFR10["NFR-10<br/>Konsekvent brädstatus"]

    A --> C["Internetavbrott"]

    C --> NFR11["NFR-11<br/>Tillfälligt internetavbrott ska inte automatiskt avsluta matchen"]
    C --> NFR12["NFR-12<br/>Senaste giltiga spelstatus, tillstånd och turordning återställs vid återanslutning"]

    A --> D["Anonymt spelande"]

    D --> NFR13["NFR-13<br/>Spelet fungerar direkt i webbläsaren utan installation"]
    D --> NFR14["NFR-14<br/>Spelet fungerar på datorer och mobiltelefoner"]

    NFR01 --> T01["Enkel att förstå och använda"]
    NFR02 --> T02["Anpassas till mobil och dator"]
    NFR03 --> T03["Snabb respons på spelarens drag"]
    NFR04 --> T04["Ingen registrering eller inloggning"]
    NFR05 --> T05["Fungerar direkt i webbläsaren"]
    NFR06 --> T06["Två spelare kan spela via länk"]
    NFR07 --> T07["Matchen förloras inte vid tillfälligt internetavbrott"]
    NFR08 --> T08["Ingen personlig information krävs"]
    NFR09 --> T09["Spelplanens storlek och position är oförändrad"]
    NFR10 --> T10["Samma brädstatus för båda spelarna"]

    NFR11 --> T11["Matchen fortsätter efter tillfälligt avbrott"]
    NFR12 --> T12["Matchens senaste giltiga tillstånd återställs"]

    NFR13 --> T13["Ingen programinstallation krävs"]
    NFR14 --> T14["Fungerar på både dator och mobil"]

    style A font-weight:bold
    style B font-weight:bold
    style C font-weight:bold
    style D font-weight:bold
```
