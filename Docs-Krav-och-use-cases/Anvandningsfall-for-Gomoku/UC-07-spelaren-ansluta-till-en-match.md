# Användingsfall 07 - Spelaren ansluter till en match
| Namn  | Värde |
|-------|-------|
|User case ID | UC-07 |
|Namn på filen| Spelaren ansluter till en Gomoku match |
|Version | 1.0 | 
|Aktör|Gäst spelare/Registrerad spelare|
|Sekundär aktör | En-vän |
|Relaterade FR | FR-04.2, FR-04.3, FR-04.5, FR-04.6, FR-06.5, FR-06.6, FR-06.9, FR-07.2, FR-07.4|
|Relaterade NFR | NFR-01, NFR-05, NFR-06, NFR-08|

## Aktör: 
En spelare 

## Mål: 
Spelaren vill kunna ansluta till en Gomoku match genom en länk utan att behöva skapa ett konto eller lämna känsliga personuppgifter.

### Förutsättningar:
- Ena spelaren har fått en giltig länk till en pågående Gomoku match.
- Matchen finns och är möjlig att ansluta till med en länk.
- Båda spelarna har internetanslutning.
- Matchen har en ledig plats för spelaren som fick länken.

# Huvudflöde för testet:
1. Ena spelaren har fått en inbjdningslänk från den andra spelaren.
2. Spelaren klickar på länken som hen fått.
3. Systemet identifierar matchen som länken tillhör.
4. Systemet kontrollerar först att matchen är aktiv och att den finns en ledig plats.
5. Spelaren ansluter till matchen utan att behöva skapa ett konto eller lämna personliga uppgifter.
6. Systemet visar spelplanen för Gomoku med matchens aktuella tillstånd.
7. Systemet kopplar båda spelarna i samma match.
8. Spelarna kan börja spela mot varandra.

# Alternativa flöden:
- Om matchen redan har två spelare så meddelar systemet att matchen är full.
- Spelaren som klickar på länken får inte ansluta till matchen och får möjlighet att återgå till startsidan.
- Om matchen är avslutad så visar systemet att matchen inte längre är aktiv att ansluta till.
- Om spelaren inte vill skapa konto ska spelaren ändå kunna ansluta till matchen.
- Om länken inte är giltig så visar systemet att länken inte är giltig att använda.

# Förväntad resultat:
Spelaren ansluter till Gomoku matchen via inbjudningslänk. Spelaren behöver inte skapa konto eller lämna personuppgifter till systemet för att spela. Systemet visar matchens aktuella spelplan.  

Om matchen inte längre är tillgänglig, full eller om länken inte funkar ska systemet informera spelaren och inte släppa in spelaren i matchen.
