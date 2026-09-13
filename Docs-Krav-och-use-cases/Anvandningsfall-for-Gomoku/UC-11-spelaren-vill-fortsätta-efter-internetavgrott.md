Spelaren vill återuppta en pågående match efter att ha förlorat internetuppkopplingen
# UC-11-spelaren-vill-fortsätta-efter-internetavbrott

| Namn | Värde |
|-------|-------|
| User case ID | UC-11 |
| Namn på filen | Spelaren vill fortsätta efter internet avbrott |
| Version | 1.0 |
| Aktör | Spelare |
| Sekundär aktör | Ingen. |
| Relaterade FR | FR-08.1, FR-08.2 |
| Relaterade NRF | NFR-03, NFR-07, NFR-08 |

## Aktör:
En spelare

## Mål: 
Spelaren ska kunna frtsätta en match efter att internet har försvunnit.

## Förutsättningar:
* Spelaren är redan inne i en match.
* internetanslutningen försvinner.
* Spelaren återfår internetuppkoppling
* Matchen är fortfarande aktiv (motståndaren har inte lämnat eller matchen avslutats)

# Huvudflöde:
1. Spelaren tappar internetuppkopplingen under en matchen.
2. Systemet upptäcker att spelaren har blivit frånkopplad.
3. Systemet pausar matchen och väntar på att spelaren śka ansluta igen.
4. Spelaren anslutar igen och öppnar spelet.
5. Systemet kontrollear spelarens identitet.
6. śpelarn ansluts till den pågående matchen.
7. Systemet visar spelplanen med senaste sparade tillstånd.
8. Matchen fortsätter från samma punkt.

## Alternativa flöden
* 3a. Timeout: Om spelaren inte ansluter igen inom tidsgränsen avslutas matchen och motståndaren vinner genom walkover.
* 5a. Misslyckad identitetsverifiering: Om systemet inte kan verifiera att det är rätt spelare som återansluter, nekas åtkomst till matchen och spelaren ombeds logga in på nytt.
* 6a. Motståndaren har lämnat matchen: Om motståndaren avbröt matchen under tiden spelaren var frånkopplad, meddelar systemet spelaren att matchen redan är avslutad och visar resultatet.
* 6b. Match mot dator: Om spelaren spelade mot datorn, återupptas matchen automatiskt utan väntetid eftersom motståndaren (datorn) inte påverkas av avbrottet.


# Förväntat resultat:
Spelaren kommer tillbaka till samma match och kan fortsätta spela. om spelaren inte kommer tillbaka i tid avslutas matchen 

