# Kompletterande Krav

## Välj svårighetsgrad

| ID      | Krav                                                                                                                  |
| ------- | --------------------------------------------------------------------------------------------------------------------- |
| FR-03.1 | Systemet ska visa en meny med svårighetsgraderna "lätt", "medel" och "svår" när spelaren väljer att spela mot datorn. |
| FR-03.2 | Systemet ska låta spelaren välja en av svårighetsgraderna.                                                            |
| FR-03.3 | Systemet laddar ett spel mot datorns AI med den valda svårighetsgraden.                                               |

## Spela anonymt utan konto

| ID      | Krav                                                                                                              |
| ------- | ----------------------------------------------------------------------------------------------------------------- |
| FR-04.1 | Systemet ska låta en ny användare öppna Gomoku i en webbläsare.                                                   |
| FR-04.2 | Systemet ska låta användaren starta ett spel utan registrerat konto.                                              |
| FR-04.3 | Systemet ska låta användaren starta ett spel utan att användaren behöver vara inloggad.                           |
| FR-04.4 | Systemet ska tillåta användaren att välja spelläge utan att samla in personlig information.                       |
| FR-04.5 | Systemet ska tillåta användaren att starta ett spel utan att kräva personlig information.                         |
| FR-04.6 | Systemet ska tillåta användaren att spela ett parti från start till slut utan att samla in personlig information. |

## Användaren hanterar Cookies

| ID      | Krav                                                                                        |
| ------- | ------------------------------------------------------------------------------------------- |
| FR-05.1 | Systemet ska tillåta att en användare öppnar Gomoku via en webbläsare.                      |
| FR-05.2 | Systemet ska kunna informera om hemsidan använder cookies eller annan typ av spårning.      |
| FR-05.3 | Systemet ska inte automatiskt samla in information om användaren utan samtycke.             |
| FR-05.4 | Systemet ska låta användaren godkänna eller neka cookies samt annat som kräver godkännande. |
| FR-05.5 | Systemet ska låta användaren spela Gomoku även när cookies nekats.                          |

## Återanslut till spel

| ID      | Krav                                                                                                             |
| ------- | ---------------------------------------------------------------------------------------------------------------- |
| FR-08.1 | Systemet ska kunna hantera att en spelare tillfälligt tappar internetanslutningen under ett pågående onlinespel. |
| FR-08.2 | Systemet ska återuppta ett pågående spel när spelaren återansluter.                                              |

## Pausa och gå tillbaka till ett spel mot datorn

| ID      | Krav                                                                                 |
| ------- | ------------------------------------------------------------------------------------ |
| FR-09.1 | Systemet ska kunna spara ett pågående spel så att spelaren kan fortsätta det senare. |
| FR-09.2 | Systemet ska kunna återuppta ett tidigare avbrutet spel.                             |

# BDD-förtydliganden

BDD används här för att förtydliga de kompletterande krav som innehåller större eller flera olika beteenden. Alla krav har inte ett eget BDD-scenario eftersom vissa krav redan är tydliga.

# FR-03 – Välj svårighetsgrad

```gherkin
Scenario 1: Användaren väljer svårighetsgrad
- Given: att användaren har valt att spela mot datorn
- When: användaren öppnar menyn för svårighetsgrad
- Then: ska alternativen "Lätt", "Medel" och "Svår" visas
- And: användaren ska kunna välja en av svårighetsgraderna
- And: spelet ska startas med den valda svårighetsgraden
```

# FR-04 – Spela anonymt utan konto

```gherkin
Scenario 1: Användaren spelar utan konto
- Given: att användaren öppnar Gomoku
- When: användaren väljer ett spelläge och startar ett spel
- Then: ska användaren kunna spela utan att skapa ett konto
- And: användaren ska inte behöva logga in
- And: användaren ska inte behöva lämna personlig information
```

# FR-05 – Användaren hanterar Cookies

```gherkin
Scenario 1: Användaren nekar cookies
- Given: att användaren öppnar Gomoku
- When: information om cookies visas
- Then: ska användaren kunna neka cookies
- And: användaren ska fortfarande kunna spela Gomoku
```

# FR-08 – Återanslut till spel

```gherkin
Scenario 1: Spelaren tappar internetanslutningen
- Given: att två spelare har en pågående match online
- When: en spelare tillfälligt tappar internetanslutningen
- Then: ska matchen inte avslutas
- And: den senaste giltiga spelstatusen ska finnas kvar
- And: spelaren ska kunna fortsätta matchen när anslutningen återkommer
```

# FR-09 – Pausa och gå tillbaka till ett spel mot datorn

```gherkin
Scenario 1: Spelaren återupptar ett tidigare spel
- Given: att användaren har ett pågående spel mot datorn
- When: användaren lämnar spelet och öppnar Gomoku igen
- Then: ska det tidigare spelet finnas kvar
- And: användaren ska kunna fortsätta spelet där det avbröts
```
