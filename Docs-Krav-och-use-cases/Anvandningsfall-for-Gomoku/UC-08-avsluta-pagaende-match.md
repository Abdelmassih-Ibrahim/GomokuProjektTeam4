# Användningsfall - 08 - Gomoku

## UC - 08 - Avsluta pågående match

| Fält | Värde |
|------|-------|
| Use Case ID | UC-08 |
| Namn | Avsluta pågående match |
| Version | 2.0 |
| Primär aktör | Gäst användare, Registrerad användare |
| Sekundär aktör | Gäst användare, Registrerad användare, Datorns AI |
| Relaterade FR | FR-10.4, FR-10.6, FR-10.7, FR-11.2, FR-11.4, FR-11.5 |
| Relaterad NFR |  |

## Aktör

Gäst användare, Registrerad användare

## Mål

Spelaren vill avsluta den pågående matchen mot datorn eller en annan spelare.

### Förutsättningar

Spelaren befinner sig i en pågående match mot datorn eller en annan spelare.

# Huvudflöde

1. Spelaren befinner sig i en pågående match.
2. Spelaren går till menyn.
3. Spelaren klickar på "Spara och avsluta".
4. Systemet sparar och avslutar det pågående partiet. 

# Förväntat resultat

Brädet fryser för både spelarna när en spelare väljer att "Spara och avsluta". Senaste läget sparas (om användaren har godkänt cookies) och spelet avslutas.
