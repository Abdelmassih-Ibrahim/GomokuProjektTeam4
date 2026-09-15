# UAT -- Gomoku
![alt text](<BILD 1.png>)



## Kundacceptanstest

**System:** Gomoku -- Fem i rad\
**Testtyp:** User Acceptance Test (UAT)\
**Testare:** Kund\
**Datum:** 2026-09-15\
**Testmiljö:** Webbläsare på dator och mobil\
**Syfte:** Kontrollera att systemet fungerar på det sätt jag som kund
förväntar mig efter vår kravintervju.

------------------------------------------------------------------------

## 1. Bakgrund

Jag ville ha ett enkelt sätt att spela Gomoku (fem i rad) direkt i
webbläsaren. Jag ville kunna spela själv mot datorn, spela med en kompis
på samma enhet eller spela med en kompis på distans.

Jag ville framför allt slippa skapa ett konto och slippa göra
installationer. Spelet skulle kännas enkelt att förstå och jag skulle
kunna vinna, förlora eller spela oavgjort.

Det här testet genomförs därför från mitt perspektiv som kund och inte
utifrån hur systemet är byggt bakom kulisserna.

------------------------------------------------------------------------

## 2. Testförutsättningar

Jag utgår från de behov och förväntningar som kom fram under intervjun:

-   Jag vill spela Gomoku direkt i webbläsaren.
-   Jag använder både en Samsung-telefon och en vanlig Windows-laptop.
-   En kompis kan använda iPhone.
-   Jag vill kunna spela mot datorn.
-   Jag vill kunna välja mellan olika svårighetsgrader.
-   Jag vill kunna spela två personer på samma enhet.
-   Jag vill kunna spela mot en kompis på distans genom att dela en
    länk.
-   Jag vill inte behöva skapa ett konto.
-   Jag vill kunna pausa ett pågående parti och fortsätta senare.
-   Om internet tillfälligt försvinner vill jag inte att ett onlinematch
    ska förstöras.
-   Jag vill själv kunna kopiera en länk och skicka den exempelvis i
    WhatsApp.
-   Spelet ska följa de vanliga reglerna för fem i rad.
-   Det ska fungera utan att jag behöver förstå hur tekniken bakom
    spelet fungerar.

------------------------------------------------------------------------

# 3. UAT-scenarier

## UAT-01 -- Öppna spelet

**Förutsättning:** Jag öppnar Gomoku i webbläsaren.

**Jag gör:** 1. Öppnar spelet. 2. Tittar på startsidan.

**Jag förväntar mig:** - Jag direkt förstår vad spelet är. - Jag ser hur
jag kan börja spela. - Jag behöver inte registrera mig.

**Resultat:** PASS

**Kundens kommentar:**\
Det är tydligt direkt vad jag kan göra. Jag behöver inte leta efter
någon registrering eller inloggning.

------------------------------------------------------------------------

## UAT-02 -- Spela mot datorn

**Förutsättning:** Jag är på startsidan.

**Jag gör:** 1. Väljer "Mot datorn". 2. Lägger en sten på spelplanen. 3.
Väntar på datorns drag. 4. Fortsätter spela.

**Jag förväntar mig:** - Jag spelar svart och börjar. - Datorn spelar
vit. - Datorn gör sitt drag efter mitt drag. - Jag kan fortsätta tills
någon vinner eller det blir oavgjort.

**Resultat:** PASS

**Kundens kommentar:**\
Det känns som ett vanligt parti mot datorn och jag behöver inte göra
något extra för att datorn ska spela.

------------------------------------------------------------------------

## UAT-03 -- Svårighetsgrad

**Förutsättning:** Jag spelar mot datorn.

**Jag gör:** 1. Tittar på inställningen för svårighetsgrad. 2. Testar
lätt, medel och svår. 3. Startar nya partier.

**Jag förväntar mig:** - Det finns flera svårighetsgrader. - Jag kan
ändra svårighetsgrad utan att behöva skapa konto eller gå någon
annanstans.

**Resultat:** PASS

**Kundens kommentar:**\
Det är bra att jag kan välja en enklare nivå. Min brorson är väldigt bra
på spelet, så jag vill kunna ha en chans ibland.

------------------------------------------------------------------------

## UAT-04 -- Två personer på samma enhet

**Förutsättning:** Jag sitter bredvid en kompis.

**Jag gör:** 1. Väljer "Två spelare". 2. Jag gör ett drag. 3. Min kompis
gör nästa drag. 4. Vi turas om.

**Jag förväntar mig:** - Svart börjar. - Vi kan turas om på samma
skärm. - En sten kan inte placeras ovanpå en annan.

**Resultat:** PASS

**Kundens kommentar:**\
Det här fungerar på det sätt jag hade tänkt mig när jag spelar med någon
bredvid mig i soffan.

------------------------------------------------------------------------

## UAT-05 -- Skapa en onlinematch

**Förutsättning:** Jag vill spela med en kompis som inte är på samma
plats.

**Jag gör:** 1. Väljer "Online via länk". 2. Väntar på att matchen
skapas. 3. Kopierar länken.

**Jag förväntar mig:** - En match skapas. - Jag får en länk som jag kan
skicka till min kompis. - Jag behöver inte själv skapa något konto.

**Resultat:** PASS

**Kundens kommentar:**\
Jag gillar att jag bara kan kopiera länken själv. Jag behöver inte att
spelet kopplas ihop med WhatsApp eller någon annan app.

------------------------------------------------------------------------

## UAT-06 -- Kompis ansluter via länken

**Förutsättning:** Jag har skickat länken till min kompis.

**Jag gör:** 1. Min kompis öppnar länken. 2. Vi tittar på samma match.
3. Vi gör varsitt drag.

**Jag förväntar mig:** - Min kompis kommer in i samma match. - Min
kompis behöver inte skapa konto. - Vi får varsin färg. - Brädet
uppdateras när den andra personen spelar.

**Resultat:** PASS

**Kundens kommentar:**\
Det är precis den typen av enkel anslutning jag ville ha. Min kompis ska
inte behöva skapa ett konto bara för att spela ett parti.

------------------------------------------------------------------------

## UAT-07 -- Turordning

**Förutsättning:** Ett parti pågår.

**Jag gör:** 1. Försöker spela när det är min tur. 2. Försöker spela
igen direkt när det är motståndarens tur.

**Jag förväntar mig:** - Jag kan spela när det är min tur. - Jag kan
inte göra två drag efter varandra. - I onlinematchen ska jag inte kunna
spela åt motståndaren.

**Resultat:** PASS

------------------------------------------------------------------------

## UAT-08 -- Upptagen ruta

**Förutsättning:** En ruta på brädet innehåller redan en sten.

**Jag gör:** 1. Försöker placera en ny sten på samma plats.

**Jag förväntar mig:** - Den gamla stenen ligger kvar. - Mitt nya drag
accepteras inte.

**Resultat:** PASS

------------------------------------------------------------------------

## UAT-09 -- Vinst med fem i rad

**Förutsättning:** Ett parti pågår.

**Jag gör:** 1. Spelar tills jag eller motståndaren får fem stenar i
rad. 2. Testar vågrät, lodrät och diagonal rad.

**Jag förväntar mig:** - Fem i rad ger omedelbar vinst. - Spelet visar
vem som vann. - Partiet kan inte fortsätta efter vinsten.

**Resultat:** PASS

**Kundens kommentar:**\
Regeln är enkel och tydlig: fem i rad vinner.

------------------------------------------------------------------------

## UAT-10 -- Oavgjort parti

**Förutsättning:** Brädet fylls utan att någon får fem i rad.

**Jag gör:** 1. Spelar tills inga lediga platser finns kvar.

**Jag förväntar mig:** - Spelet visar att det blev oavgjort. - Ingen
spelare utses till vinnare.

**Resultat:** PASS

------------------------------------------------------------------------

## UAT-11 -- Pausa ett parti

**Förutsättning:** Jag har börjat spela ett parti.

**Jag gör:** 1. Trycker på "Pausa". 2. Försöker lägga en sten. 3.
Trycker på "Återuppta".

**Jag förväntar mig:** - Spelet visar att partiet är pausat. - Jag ska
inte kunna göra drag medan det är pausat. - Jag ska kunna fortsätta när
jag väljer "Återuppta".

**Resultat:** PASS

------------------------------------------------------------------------

## UAT-12 -- Fortsätta ett parti senare

**Förutsättning:** Jag har ett pågående parti.

**Jag gör:** 1. Pausar eller lämnar spelet. 2. Öppnar spelet igen
senare.

**Jag förväntar mig:** - Mitt pågående lokala parti finns kvar. - Jag
kan fortsätta där jag slutade.

**Resultat:** PASS

**Kundens kommentar:**\
Det passar bra eftersom jag ibland spelar kanske 20 minuter och sedan
behöver göra något annat.

------------------------------------------------------------------------

## UAT-13 -- Starta nytt parti

**Förutsättning:** Jag spelar eller har avslutat ett parti.

**Jag gör:** 1. Trycker på "Nytt parti" eller "Spela igen".

**Jag förväntar mig:** - Ett nytt tomt bräde visas. - Det gamla partiet
påverkar inte det nya.

**Resultat:** PASS

------------------------------------------------------------------------

## UAT-14 -- Spela utan konto

**Förutsättning:** Jag är en ny användare.

**Jag gör:** 1. Öppnar spelet. 2. Försöker börja spela.

**Jag förväntar mig:** - Jag behöver inte registrera mig. - Jag behöver
inte ange e-postadress. - Jag behöver inte komma ihåg något lösenord.

**Resultat:** PASS

**Kundens kommentar:**\
Det här är viktigt för mig. Jag har tidigare gett upp appar när jag
mötts av en registreringssida.

------------------------------------------------------------------------

## UAT-15 -- Mobiltelefon

**Förutsättning:** Jag använder min Samsung-telefon.

**Jag gör:** 1. Öppnar spelet i Chrome. 2. Startar ett parti. 3. Trycker
på olika positioner på brädet.

**Jag förväntar mig:** - Spelet går att använda på en mindre skärm. -
Brädet är tillräckligt tydligt för att spela på. - Jag behöver inte
installera en app.

**Resultat:** PASS

------------------------------------------------------------------------

## UAT-16 -- Dator

**Förutsättning:** Jag använder min Windows-laptop.

**Jag gör:** 1. Öppnar spelet i Chrome. 2. Startar ett parti. 3. Spelar
flera drag.

**Jag förväntar mig:** - Spelet fungerar i webbläsaren. - Brädet är
tydligt. - Jag kan spela utan installation.

**Resultat:** PASS

------------------------------------------------------------------------

## UAT-17 -- Tillfälligt internetproblem

**Förutsättning:** Jag spelar en onlinematch.

**Jag gör:** 1. Tappar tillfälligt internetanslutningen. 2. Väntar tills
anslutningen kommer tillbaka. 3. Fortsätter spela.

**Jag förväntar mig:** - Matchen ska inte försvinna bara för att
anslutningen tillfälligt bryts. - Spelet ska kunna hämta det senaste
läget när anslutningen kommer tillbaka.

**Resultat:** PASS

**Kundens kommentar:**\
Jag har ibland problem med uppkopplingen hemma, så jag vill inte behöva
börja om ett helt parti bara för att internet strular en stund.

------------------------------------------------------------------------

## UAT-18 -- Enkel användning

**Förutsättning:** Jag har aldrig sett just den här versionen tidigare.

**Jag gör:** 1. Öppnar startsidan. 2. Försöker starta ett parti utan
hjälp.

**Jag förväntar mig:** - Jag förstår vad jag ska trycka på. - Jag
behöver inte känna till tekniska saker. - De viktigaste knapparna är
begripliga.

**Resultat:** PASS

**Kundens kommentar:**\
Jag tycker att upplägget är enkelt nog för att bara öppna och börja
spela.

------------------------------------------------------------------------

# 4. Samlad UAT-bedömning

  Område                                     Resultat
  ------------------------------------------ ----------
  Starta och spela Gomoku                    PASS
  Spela mot datorn                           PASS
  Svårighetsgrader                           PASS
  Två spelare på samma enhet                 PASS
  Online via delad länk                      PASS
  Spela utan konto                           PASS
  Turordning                                 PASS
  Fem i rad                                  PASS
  Oavgjort                                   PASS
  Pausa och återuppta                        PASS
  Starta nytt parti                          PASS
  Mobil användning                           PASS
  Datoranvändning                            PASS
  Hantering av tillfälligt internetproblem   PASS
  Enkel användning                           PASS

------------------------------------------------------------------------

# 5. Avvikelser

Under UAT:n hittades inga avvikelser som hindrar mig från att använda
spelet för det jag bad om.

Det finns funktioner som är tekniska bakom kulisserna, men de behöver
jag som kund egentligen inte märka. För mig är det viktiga att spelet
fungerar utan att jag behöver förstå hur det är byggt.

------------------------------------------------------------------------

# 6. Kundens slutliga kommentar

Jag tycker att systemet motsvarar det vi pratade om under intervjun.

Det viktigaste för mig var att kunna öppna spelet och bara spela. Jag
kan spela mot datorn, spela med någon bredvid mig eller skicka en länk
till en kompis. Jag behöver inte skapa något konto och jag kan pausa ett
parti om jag behöver gå därifrån.

Jag hade inte velat ha en massa extra funktioner som gör spelet
krångligare. Som kund är jag nöjd när jag kan öppna sidan, välja hur jag
vill spela och komma igång direkt.

## UAT-resultat: GODKÄND

**Kundens beslut:** Systemet accepteras för leverans.

------------------------------------------------------------------------

