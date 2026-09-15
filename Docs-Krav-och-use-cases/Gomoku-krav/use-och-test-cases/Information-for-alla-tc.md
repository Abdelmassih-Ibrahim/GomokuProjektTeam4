# USE CASES >> TEST CASES >> KVALITE. 
 Vi skapade olika testfall från våra användningsfall frö att säkerställa att systemet faktist fungerar som det är tankt ur användarens perspektiv. Våra användningsfall beskriver ett tydligt mål med steg för att nå det. Detta är en perfekt mall för oss
 att utgå ifrån för att verifiera systemets funktionalitet och kontrollera kvalitet. 

# översikt för alla TC:
| ID            |Relaterat-UC    |
|-------------------|--------------------------------|
| TC-01 – Starta en match  |UC-01 |
| TC-02 – Spela mot dator plats. |UC-02 |
| TC-03 – Ogiltigt drag på upptagen position| UC-02 |
| TC-04 – Spelare kan bara spela på sin tur| UC-02+UC.07 |
| TC-05 – Fem i rad horisontellt| UC02 + UC.10 |
| TC-06 – Fem i rad vertikalt|UC-02 / UC-10|
| TC-07 – Fem i rad diagonalt|UC-02 / UC-10|
| TC-08 – Inga drag efter en vinst|UC-10|
| TC-09 – Oavgjort|UC-10|
|TC-10 – Starta ny match efter avslutad match|UC-10|
| TC-11 – Välja svårighetsgrad|UC-03|
| TC-12 – Spela anonymt|UC-04|
| TC-13 – Hantera cookies|UC-05|
| TC-14 – Skapa och kopiera spellänk|UC-06|
|TC-15 – Ansluta till match via länk|UC-07|
|TC-16 – Ansluta till ogiltig eller full match|UC-07|
|TC-17 – Spela från samma plats|UC-13|
|TC-18 – Bevara matchens state|UC-09 / UC-12|
|TC-19 – Internetavbrott|UC-11|
|TC-20 – Samma state hos båda online-spelarna |UC-12|

# Icke-funktionella testfall
| ID            |Relaterat-UC    |
|-------------------|--------------------------------|
| TC-21 – Responsiv design|NFR-02, NFR-15|
|TC-22–Webbläsare utan installation|NFR-05, NFR-14|
| TC-23–Visuell stabilitet|NFR-09|
|TC-24–Ingen personlig information i spellänk |NFR-08, NFR-10|
