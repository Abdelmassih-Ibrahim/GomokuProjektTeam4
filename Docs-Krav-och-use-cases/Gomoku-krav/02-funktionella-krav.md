# Funktionella krav

## User Story

Som en användare vill jag spela Gomoku mot en motståndare så att en av oss får fem i rad eller tills spelet slutar i oavgjort.

---

# Spelet laddas

| ID          | Krav                                                                                                                   |
| ----------- | ---------------------------------------------------------------------------------------------------------------------- |
| **FR-01.1** | Systemet ska tillåta att en spelare går med i spelet.                                                                  |
| **FR-01.2** | Systemet ska kunna identifiera vilket spelläge som används: mot datorn, hot-seat multiplayer eller online multiplayer. |
| **FR-01.3** | Systemet ska kunna ladda en spelplan av förvald storlek.                                                               |
| **FR-01.4** | Systemet ska kunna tilldela korrekt markör till varje spelare.                                                         |
| **FR-01.5** | Systemet ska automatiskt avgöra vilken spelare som börjar utifrån den tilldelade markören.                             |

# BDD-förtydligande för FR-01.2

Eftersom FR-01.2 innehåller tre olika spellägen kan kravet förtydligas med:

```gherkin
Scenario: Spelaren väljer att spela mot datorn
  Given: att spelaren befinner sig på startsidan
  When: spelaren väljer "Mot datorn"
  Then: ska systemet starta ett spel mot datorns AI
```

```gherkin
Scenario 2: Spelaren väljer två spelare
- Given: att spelaren befinner sig på startsidan
- When: spelaren väljer "Två spelare"
- Then: ska systemet starta ett hot-seat-spel
```

```gherkin
Scenario 3: Spelaren väljer online-spel
- Given: att spelaren befinner sig på startsidan
- When: spelaren väljer "Online via länk"
- Then: ska systemet starta ett online-spel
```

---

# Spel mot datorns AI

| ID           | Krav                                                                                                   |
| ------------ | ------------------------------------------------------------------------------------------------------ |
| **FR-02.1**  | Systemet ska tillåta att en spelare startar ett spel mot datorns AI.                                   |
| **FR-02.4**  | Systemet ska kunna ladda en spelplan av förvald storlek.                                               |
| **FR-02.5**  | Systemet ska kunna tilldela korrekt markör till spelaren.                                              |
| **FR-02.6**  | Systemet ska automatiskt avgöra om spelaren eller datorns AI börjar utifrån den tilldelade markören.   |
| **FR-02.7**  | Systemet ska tillåta spelaren att placera sin markör på en tom position på spelplanen.                 |
| **FR-02.8**  | Systemet ska hantera turordningen mellan spelaren och datorns AI.                                      |
| **FR-02.9**  | Systemet ska automatiskt identifiera när spelaren eller datorns AI får fem i rad.                      |
| **FR-02.10** | Systemet ska automatiskt avsluta spelet när spelaren eller datorns AI får fem i rad och utse vinnaren. |
| **FR-02.11** | Systemet ska automatiskt identifiera när spelplanen är full utan att någon spelare har fått fem i rad. |
| **FR-02.12** | Systemet ska automatiskt avsluta spelet när spelplanen är full och deklarera matchen som oavgjord.     |

# BDD-förtydligande för FR-02.8

```gherkin
Scenario 1: Spelaren gör ett drag
- Given: att ett spel mot datorn pågår
- And: det är spelarens tur
- When: spelaren placerar en markör på en tom position
- Then: ska draget registreras
- And: turen ska gå över till datorns AI
```

```gherkin
Scenario 2: Datorn gör sitt drag
- Given: att det är datorns AI:s tur
- When: datorn gör sitt drag
- Then: ska datorns markör placeras på en tom position
- And: turen ska gå tillbaka till spelaren
```

```gherkin
Scenario 3: Spelaren försöker göra ett drag när det är datorns tur
- Given: att det är datorns AI:s tur
- When: spelaren försöker placera en markör
- Then: ska draget nekas
```

# BDD-förtydligande för FR-02.9

```gherkin
Scenario 1: Spelaren får fem i rad
- Given: att spelaren har fyra markörer i rad
- When: spelaren placerar den femte markören
- Then: ska systemet identifiera fem i rad
```

```gherkin
Scenario 2: Datorns AI får fem i rad
- Given: att datorns AI har fyra markörer i rad
- When: datorn placerar den femte markören
- Then: ska systemet identifiera fem i rad
```

---

# Bjud in vän via länk

| ID          | Krav                                                                                      |
| ----------- | ----------------------------------------------------------------------------------------- |
| **FR-06.1** | Systemet ska skapa ett unikt match-ID när användaren startar en ny match.                 |
| **FR-06.2** | Systemet ska visa alternativet "Kopiera länk" efter att användaren har skapat en match.   |
| **FR-06.3** | Systemet ska låta användaren kopiera spellänken.                                          |
| **FR-06.4** | Systemet ska låta användaren dela spellänken med en annan spelare.                        |
| **FR-06.5** | Systemet ska omdirigera användaren till matchen när hen öppnar en giltig inbjudningslänk. |
| **FR-06.6** | Systemet ska ladda matchen när användaren öppnar en giltig inbjudningslänk.               |
| **FR-06.9** | Systemet ska låta användaren spela utan att skapa ett konto eller logga in.               |

# BDD-förtydligande för FR-06.5 och FR-06.6

```gherkin
Scenario 1: Spelaren ansluter via en giltig spellänk
- Given: att en aktiv match har skapats
- And: spelaren har fått en giltig spellänk
- When: spelaren öppnar länken
- Then: ska systemet identifiera matchen
- And: ladda den aktuella matchen
- And: spelaren ska kunna ansluta till matchen
```

---

# Multiplayer-spel

| ID          | Krav                                                                                           |
| ----------- | ---------------------------------------------------------------------------------------------- |
| **FR-07.1** | Systemet ska tillåta två spelare att spela mot varandra på samma enhet (hot-seat).             |
| **FR-07.2** | Systemet ska tillåta två spelare att spela mot varandra via en delad spellänk.                 |
| **FR-07.3** | Systemet ska låta en spelare skapa en match som en annan spelare kan ansluta till via en länk. |
| **FR-07.4** | Systemet ska hantera turordningen mellan två spelare i ett onlinespel.                         |

# BDD-förtydligande för FR-07.4

```gherkin
Scenario 1: Spelare 1 gör ett drag i ett onlinespel
- Given: att två spelare befinner sig i samma aktiva onlinematch
- And: det är spelare 1:s tur
- When: spelare 1 placerar en markör på en tom position
- Then: ska draget registreras
- And: turen ska gå över till spelare 2
- And: spelare 1 ska inte kunna göra ytterligare ett drag
```

```gherkin
Scenario 2: Spelare 2 gör nästa drag
- Given: att det är spelare 2:s tur
- When: spelare 2 placerar en markör på en tom position
- Then: ska draget registreras
- And: turen ska gå tillbaka till spelare 1
```

---

# Vinst

| ID          | Krav                                                                                                   |
| ----------- | ------------------------------------------------------------------------------------------------------ |
| **FR-10.1** | Spelet ska kunna identifiera när fem markeringar från samma spelare ligger i rad.                      |
| **FR-10.2** | Systemet ska kunna identifiera vilken spelare som varje markering tillhör.                             |
| **FR-10.3** | Systemet ska identifiera vinnaren utifrån vilken spelare som fått fem i rad.                           |
| **FR-10.4** | Spelet ska avslutas automatiskt när en spelare har vunnit.                                             |
| **FR-10.5** | En resultatskärm ska visa vilken spelare som vann och innehålla alternativ för huvudmeny och ny match. |
| **FR-10.6** | Spelaren ska kunna återgå till huvudmenyn efter avslutat spel.                                         |
| **FR-10.7** | Spelaren ska kunna starta en ny match efter avslutat spel.                                             |

# BDD-förtydligande för FR-10.1

Eftersom fem i rad kan uppstå i olika riktningar förtydligas kravet med tre scenarier:

```gherkin
Scenario 1: Fem markeringar ligger horisontellt
- Given: att en spelare har fyra markeringar i rad horisontellt
- When: spelaren placerar den femte markeringen
- Then: ska systemet identifiera fem i rad
```

```gherkin
Scenario 2: Fem markeringar ligger vertikalt
- Given: att en spelare har fyra markeringar i rad vertikalt
- When: spelaren placerar den femte markeringen
- Then: ska systemet identifiera fem i rad
```

```gherkin
Scenario 3: Fem markeringar ligger diagonalt
- Given: att en spelare har fyra markeringar i rad diagonalt
- When: spelaren placerar den femte markeringen
- Then: ska systemet identifiera fem i rad
```

# BDD-förtydligande för FR-10.5

```gherkin
Scenario 1: Resultatskärmen visas efter vinst
- Given: att en spelare har vunnit matchen
- When: matchen avslutas
- Then: ska resultatskärmen visas
- And: vinnaren ska visas
- And: spelaren ska kunna välja huvudmeny
- And: spelaren ska kunna starta en ny match
```

---

# Oavgjort

| ID          | Krav                                                                                                       |
| ----------- | ---------------------------------------------------------------------------------------------------------- |
| **FR-11.1** | Spelet ska kunna identifiera när spelplanen är full och ingen spelare har fått fem i rad.                  |
| **FR-11.2** | Spelet ska avslutas när spelplanen är full och ingen spelare har fått fem i rad.                           |
| **FR-11.3** | En resultatskärm ska visa att matchen blev oavgjord och innehålla alternativ för huvudmeny och nytt parti. |
| **FR-11.4** | Spelaren ska kunna återgå till huvudmenyn efter avslutat spel.                                             |
| **FR-11.5** | Spelaren ska kunna starta ett nytt parti efter avslutat spel.                                              |

# BDD-förtydligande för FR-11.1 och FR-11.2

```gherkin
Scenario 1: Matchen blir oavgjord
- Given: att spelplanen är full
- And: ingen spelare har fått fem i rad
- When: den sista lediga positionen fylls
- Then: ska systemet identifiera matchen som oavgjord
- And: matchen ska avslutas
```

# BDD-förtydligande för FR-11.3

```gherkin
Scenario 1: Resultatskärmen visas efter oavgjort
- Given: att matchen har slutat oavgjort
- When: matchen avslutas
- Then: ska resultatskärmen visas
- And: det ska stå att matchen blev oavgjord
- And: spelaren ska kunna välja huvudmeny
- And: spelaren ska kunna starta ett nytt parti
```
