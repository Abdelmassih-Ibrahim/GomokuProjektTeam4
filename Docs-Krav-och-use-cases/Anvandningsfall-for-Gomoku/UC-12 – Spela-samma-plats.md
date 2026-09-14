# UC-12 – Spela på samma plat med en vän

| Fält              | Värden                         |
|-------------------|--------------------------------|
| Use Case ID       | UC-13                        |
| Namn              | Spela på samma plats. |
| Version           | 1.0                            |
| Preliminär Aktör  | en spelare |
| Sekundär Aktör    | en annan spelare|
| Relaterad FR      | FR-07.1|
| Relaterad NFR     | NFR-01, NFR-02|

## Syfte

Två spelare ska kunna spela Gomoku mot varandra utan problem på samma enhet.

## Aktör

Två spelare.

## Förutsättningar

Användaren har valt att spela mot sin vän på samma enhet.

## Huvudflöde

1. Spelaren väljer multiplayer.
2. Systemet startar en ny match.
3. Systemet tilldelar en markör till varje spelare.
4. Systemet visar tydligt vilken spelare som börjar.
5. Spelare 1 placerar sin markör på en ledig position.
6. Systemet byter tur till den andra spelaren.
7. Spelare 2 placerar sin markör på en ledig position.
8. Systemet byter tillbaka till spelare 1.
9. steg 5 till 8 fortsätter tills någon vinner eller att det blir oavgjort.

## Alternativa flöden

### Spelaren väljer en upptagen position

1. Systemet nekar draget.
2. Spelaren får försöka igen.
3. Turordningen ändras inte.

### Spelaren försöker spela när det inte är hens tur

1. Systemet nekar också draget.
2. Den andra spelaren behåller sin tur.


### Spelplanen blir full

1. Systemet identifierar att spelplanen är full.
2. Ingen spelare har fått fem i rad.
3. Matchen avslutas som oavgjord.

# Förväntad resultat: 
Två spelare kan spela en hel gomoku match mot varandra på samma enhet. Systemet hanterar även turordningen korrekt och visar tydlgit vilken spelares tur det är. Spelare kan endast placera sina markörer på lediga positioner och ett ogiltigt drag påverkar inte spelets turordning. 

Matchen ska även fortsätta tills någon får fem i rad eller att spelplanne blir full. När en spelare vinner avslutas matchen och systemet visar vem som vann. 
