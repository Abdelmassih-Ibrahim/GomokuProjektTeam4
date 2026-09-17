# Traceability Matrix

## Funktionella krav ---> Användningsfall

| FR ID | Krav (kortfattat) | Förverkligad av UC | 
|-------|-------------------|--------------------|
| FR-01.1 | Spelaren ska kunna gå med i spelet | UC-01 |
| FR-01.2 | Identifiera typ av spel | UC-01 |
| FR-01.3 | Ladda spelplan av förvald storlek | UC-01 |
| FR-01.4 | Tilldela korrekt markör | UC-01 |
| FR-01.5 | Avgöra vem som börjar | UC-01 |
| FR-02.1 | Spel mot datorns AI | UC-02 |
| FR-02.4 | Ladda spelplan av förvald storlek (spel mot datorn) | UC-02 |
| FR-02.5 | Tilldela korrekt markör | UC-02 |
| FR-02.6 | Avgöra vem som börjar (spel mot datorn) | UC-02 |
| FR-02.7 | Placera markör på tom punkt på spelplanen | UC-02 |
| FR-02.8 | Hantera turordning (spel mot datorn) | UC-02 |
| FR-02.9 | Identifiera fem i rad (spel mot datorn)| UC-02 |
| FR-02.10 | Avsluta spel vid vinst (spel mot datorn)| UC-02 |
| FR-02.11 | Identifiera full spelplan | UC-02 |
| FR-02.12 | Avsluta och deklarera oavgjort (spel mot datorn) | UC-02 |
| FR-06.1  | Skapa unikt match-ID vid start av match | UC-06 |
| FR-06.2  | Visa "kopiera länk" | UC-06 |
| FR-06.3  | Kunna kopiera länken | UC-06 |
| FR-06.4  | Skicka länken | UC-06 |
| FR-06.5  | Omdirigera användaren | UC-07 |
| FR-06.6  | Ladda spel via länk | UC-07 |
| FR-06.9  | Spela utan befintligt konto eller inloggning | UC-07 | 
| FR-07.1  | Hot-seat multiplayer | UC-13 |
| FR-07.2  | Spela online via länk | UC-06, UC-07 |
| FR-07.3  | Skapa online match via länk | UC-06 |
| FR-07.4  | Hantera turordningen (multiplayerspel) | Tydlig beskrivning gällande turordning saknas i UC-06 och UC-07 |
| FR-10.1  | Identifiera fem i rad (vinst) | UC-10 |
| FR-10.2  | Identifiera markeringar och spelare | UC-10 |
| FR-10.3  | Identifiera vinnare utifrån markeringar | UC-10 |
| FR-10.4  | Avslutning vid vinst | UC-08, UC-10 | 
| FR-10.5  | Vinstsskärm dyker upp | UC-10 |
| FR-10.6  | Återgå till huvudmeny (vinst/förlust) | UC-08, UC-10 |
| FR-10.7  | Ny match efter avslutat spel (vinst/förlust)| UC-08, UC-10 |
| FR-11.1  | Identifiera fullt bräde (oavgjort) | UC-10 |
| FR-11.2  | Avsluta spel vid fullt bräde (oavgjort) | UC-08, UC-10 |
| FR-11.3  | Oavgjort skärm dyker upp | UC-10 |
| FR-11.4  | Återgå till startmeny (oavgjort) | UC-08, UC-10 |
| FR-11.5  | Nytt parti efter avslutat spel (oavgjort) | UC-08, UC-10 |

## Användningsfall ---> Funktionella krav

| UC ID | Användningsfall | Förverkligad av FR |
|-------|-----------------|--------------------|
| UC-01 | Starta en match | FR-01.1, FR-01.2, FR-01.3, FR-01.4, FR-01.5 |
| UC-02 | Spela mot en dator | FR-02.1, FR-02.4, FR-02.5, FR-02.6, FR-02.7, FR-02.8, FR-02.9, FR-02.10, FR-02.11, FR-02.12 |
| UC-03 | Välja svårighetsgrad | FR-03.1, FR-03.3, FR-03.3 |
| UC-04 | Användaren spelar anonymt utan konto | FR-04.2, FR-04.3, FR-04.4, FR-04.5, FR-04.6 |
| UC-06 | Användaren bjuder in sin vän via länk | FR-06.1, FR-06.2, FR-06.3, FR-06.4, FR-07.2, FR-07.3 |
| UC-07 | Ansluta till en match | FR-06.5, FR-06.6, FR-06.9, FR-07.2 |
| UC-08 | Avsluta pågående match | FR-10.4, FR-10.6, FR-10.7, FR-11.2, FR-11.4, FR-11.5 |
| UC-09 | Fortsätta pausad match | FR-09.1, FR-09.2 |
| UC-10 | Se matchresultat | FR-10.1, FR-10.2, FR-10.3, FR-10.4, FR-10.5, FR-10.6, FR-10.7, FR-11.1, FR-11.2, FR-11.3, FR-11.4, FR-11.5 |
| UC-11 | Fortsätta efter internetavbrott |  FR-08.1, FR-08.2 |
| UC-12 | Bevara spelstatus | FR-09.1, FR-09.2 |
| UC-13 | Spela hot-seat multiplayer | FR-07.1 |

## Kompletterande krav ---> Användningsfall

                       
|CR ID (står som FR) | Kompletterande krav (kort) | Förverkligad av UC          |
|-----------------------------|----------------------------|--------------------|
| FR-03.1 | Visa meny med svårighetsgrader | UC-03 |
| FR-03.2 | Välj svårighetsgrad            | UC-03 |
| FR-03.3   | Ladda spel mot datorn med vald svårighetsgrad | UC-03 |
| FR-04.1 | Öppna Gomoku i en webbläsare | UC-04 |
| FR-04.2 | Starta spel utan registrerat konto   | UC-04, UC-06, UC-07 |
| FR-04.3 | Starta spel utan att vara inloggad   | UC-04, UC-06, UC-07 |
| FR-04.4 | Välja spelläge utan att ange personlig information | UC-04 |
| FR-04.5 | Starta spel utan att ange personlig information    | UC-04, UC-06, UC-07 |
| FR-04.6 | Spela helt parti utan att ange personlig information | UC-04, UC-06, UC-07 |
| FR-05.1 | Öppna Gomoku i en webbläsare | UC-05 |
| FR-05.2 | Hemsidan informerar om cookies | UC-05 |
| FR-05.3 | Samla inte in information automatiskt | UC-05 |
| FR-05.4 | Godkänn/neka cookies | UC-05 |
| FR-05.5 | Tillåta spel vid nekande av cookies | UC-05 |
| FR-08.1 | Hantera tillfälligt internetavbrott | UC-11 |
| FR-08.2 | Återuppta pågående spel | UC-11 |
| FR-09.1 | Spara pågående spel mot datorn | UC-09 |
| FR-09.2 | Återuppta pausat spel mot datorn | UC-09 |

## Användningsfall ---> Kompletterande krav

| UC ID | Användningsfall | Förverkligad av CR |
|-------|-----------------|--------------------|
| UC-03 | Välja svårighetsgrad | CR-03.1, CR-03.2, CR-03.3 |
| UC-04 | Användaren spelar anonymt utan konto | CR-04.1, CR-04.2, CR-04.3, CR-04.4, CR-04.5, CR-04.6 |
| UC-05 | Användaren hanterar cookies | CR-05.1, CR-05.2, CR-05.3, CR-05.4, CR-05.5 |
| UC-06 | Användaren bjuder in sin vän via länk | CR-04.2, CR-04.3, CR-04.5, CR-04.6 |
| UC-07 | Ansluta till en match | CR-04.2, CR-04.3, CR-04.5, CR-04.6 |
| UC-09 | Fortsätta pausad match | CR-09.1, CR-09.2 |
| UC-11 | Fortsätta efter internetavbrott | CR-08.1, CR-08.2 |

## Icke-funktionella krav ---> Användningsfall

| NFR ID | Icke-funktionella krav (kort) | Förverkligad av UC |
|--------|-------------------------------|--------------------|
| NFR-01 | Användarvänlighet             | UC-01, UC-02, UC-03, UC-07, UC-09, UC-10, UC-12 |
| NFR-02 | Responsiv design              | UC-12 |
| NFR-03 | Prestanda                     | UC-01, UC-02, UC-09, UC-10, UC-11 |
| NFR-04 | Anonym användning             | UC-04 |
| NFR-05 | Kompabilitet                  | UC-05, UC-07 |
| NFR-06 | Anslutning via länk           | UC-06, UC-07 |
| NFR-07 | Tillförlitlighet              | UC-11 |
| NFR-08 | Säkerhet och integritet (inbjudningslänk) | UC-04, UC-05, UC-06, UC-07, UC-11 |
| NFR-10 | Säkerhet och integritet (Delta i match) | UC-10 |

## Användningsfall ---> Icke-funktionella krav

| UC-ID | Användningsfall | Förverkligad av NFR |
|-------|-----------------|---------------------|
| UC-01 | Starta en match | NFR-01, NFR-03 |
| UC-02 | Spel mot datorns AI | NFR-01, NFR-03 |
| UC-03 | Välja svårighetsgrad | NFR-01 |
| UC-04 | Spela anonymt utan konto | NFR-04, NFR-08 |
| UC-05 | Hantera cookies | NFR-05, NFR-08 |
| UC-06 | Bjud in vän via länk | NFR-06, NFR-08 |
| UC-07 | Anslut till match via länk | NFR-01, NFR-05, NFR-06, NFR-08 |
| UC-09 | Återuppta sparad match | NFR-01, NFR-03 |
| UC-10 | Se matchresultat | NFR-01, NFR-03, NFR-10 |
| UC-11 | Fortsätta efter internetavbrott | NFR-03, NFR-07, NFR-08 |
| UC-12 | Spela på samma plan som vän | NFR-01, NFR-02 |

## Test case ---> Användningsfall

| TC-ID | Test case | Förverkligad av UC |
|-------|-----------|--------------------|
| TC-01 | Starta en match | UC-01 |
| TC-02 | Spela mot datorns AI | UC-02 |
| TC-03 | Hantera ogiltigt drag | UC-02 |
| TC-04 | Spela på sin tur | UC-02, UC-07 |
| TC-05 | Fem i rad horisontellt | UC-02, UC-10 |
| TC-06 | Fem i rad vertikalt | UC-02, UC-10 |
| TC-07 | Fem i rad diagonalt | UC-02, UC-10 |
| TC-08 | Inga drag efter vinst | UC-10 |
| TC-09 | Oavgjort | UC-10 |
| TC-10 | Starta ny match | UC-10 |
| TC-11 | Välj svårighetsgrad | UC-03 |
| TC-12 | Spela anonymt | UC-04 |
| TC-13 | Hantera cookies | UC-05 |
| TC-14 | Skapa och kopiera spellänk | UC-06 |
| TC-15 | Ansluta till match via länk | UC-07 |
| TC-16 | Hantera anslutning till ogiltig match | UC-07 |
| TC-17 | Spela hot-seat multiplayer | UC-12 |
| TC-18 | Bevara matchens state | UC-09, UC-12 |
| TC-19 | Hantera tillfälligt internetavbrott | UC-11 |
| TC-20 | Samma state hos båda onlinespelarna | UC-12
| TC-25 | Avsluta, state sparas | UC-08 |
| TC-26 | Avsluta state sparas inte | UC-08 |

## Användningsfall ---> Test Case

| UC-ID | Användningsfall | Förverkligad av TC |
|-------|-----------------|--------------------|
| UC-01 | Starta en match | TC-01 |
| UC-02 | Spel mot datorns AI | TC-02, TC-03, TC-04, TC-05, TC-06, TC-07 |
| UC-03 | Välja svårighetsgrad | TC-11 |
| UC-04 | Spela anonymt utan konto | TC-12 |
| UC-05 | Hantera cookies | TC-13 |
| UC-06 | Bjud in vän via länk | TC-14 |
| UC-07 | Anslut till match via länk | TC-04, TC-15, TC-16 |
| UC-08 | Avsluta pågående match | TC-25, TC-26 | 
| UC-09 | Återuppta sparad match | TC-18 |
| UC-10 | Se matchresultat | TC-05, TC-06, TC-07, TC-08, TC-09, TC-10 |
| UC-11 | Fortsätta efter internetavbrott | TC-19 |
| UC-12 | Spela på samma plan som vän | TC-17, TC-18, TC-20 |


