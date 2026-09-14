# UC-08 – Avsluta pågående match

| Fält           | Värde                                                |
| -------------- | ---------------------------------------------------- |
| Use Case ID    | UC-08                                                |
| Namn           | Avsluta pågående match                               |
| Version        | 1.0                                                  |
| Primär aktör   | Spelare                                              |
| Sekundär aktör | Systemet                                             |
| Relaterade FR  | FR-10.4, FR-10.6, FR-10.7, FR-11.2, FR-11.4, FR-11.5 |
| Relaterade NFR | NFR-01, NFR-03                                       |


## Aktör

En spelare.

## Mål

Spelaren vill få ett tydligt resultat när matchen är färdig och kunna välja vad som ska hända efter matchens slut.

## Förutsättningar

* En Gomoku-match pågår redan..
* Spelarna kan göra giltiga drag under matchen
* Matchens spelstatus är aktiv/pågående

## Huvudflöde – En spelare vinner

1. Spelaren gör ett giltigt drag.
2. Systemet kontrollerar spelplanen.
3. Systemet identifierar att spelaren har fått fem stenar i rad.
4. Systemet registrerar spelaren som vinnare.
5. Systemet avslutar matchen.
6. Systemet förhindrar ytterligare drag.
7. Systemet visar matchresultatet.
8. Spelaren kan välja att starta ett nytt parti.
9. Spelaren kan återgå till huvudmenyn.


## Alternativt flöde – Matchen blir oavgjord

1. Spelaren gör ett giltigt drag.
2. Systemet kontrollerar spelplanen.
3. Ingen spelare har fått fem i rad.
4. Systemet identifierar att spelplanen är full.
5. Systemet avslutar matchen som oavgjord.
6. Systemet förhindrar ytterligare drag.
7. Systemet visar att matchen är oavgjord.
8. Spelaren kan välja att starta ett nytt parti.
9. Spelaren kan återgå till huvudmenyn.


## Alternativt flöde – Ingen match har avslutats

1. Matchen har fortfarande minst en ledig position.
2. Ingen spelare har fått fem i rad.
3. Systemet avslutar inte matchen.
4. Nästa spelare får fortsätta spela.


## Förväntat resultat

Matchen avslutas automatiskt när en spelare får fem stenar i rad eller när spelplanen är helt full.
När matchen avslutas ska systemet tydligt visa resultatet och förhindra fler drag i den avslutade matchen. 
Spelaren ska kunna starta ett nytt parti efter avslutad match och, där systemet erbjuder visar  "återgå till huvudmenyn."

