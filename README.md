# GomokuProjektTeam4

Detta är en gomoku-spel(fem i rad) utvecklad som en del av ett skolprojekt med stark fokus på kravfångst, systemanalys, use-cases, modellering och testning.

Repositoryt innehåller projekets dokumentation men även övriga filer som användes under hela utvecklingsprocessen.
## Innehåll som finns:

* [Om hela projektet](#om-hela-projektet)
* [Dokumentation](#dokumentation)
* [Användningsfall](#användningsfall)
* [Test Cases](#test-cases)
* [UML och modeller](#uml-och-modeller)
* [User Journey](#user-journey)
* [Begreppslista för hela projektet](#begreppslista-för-hela-projektet)
* [Business Rules](#business-rules)
* [Kundintervju och icke-funktionella krav](#kundintervju-och-icke-funktionella-krav)
* [Utvecklingsprocess](#utvecklingsprocess)
* [Projektstruktur](#projektstruktur)


---

## Om hela projektet
Gomoku är ett brädspel för två spelare kör mot varandra och målet är att få fem egna stenar i rad – horisontellt, vertikalt eller diagonalt.
I projektet har vi arbetat med hur ett system kan analyseras och dokumenteras innan och under utveckling. Fokus ligger därför inte bara på själva spelet, utan även på att beskriva:
* vad användaren behöver kunna göra(FR),
* hur användaren interagerar med systemet,
* vilka regler som systemet måste följa (BR),
* vilka alternativa scenarier som kan uppstå (UC),
* vilka egenskaper systemet behöver ha(FR,NFR),
* och hur dessa scenarier kan testas(TC).
  
Projektet har även delar om att spel mot dator, spel med en annan person, spel via länk, anonymt spelande, hantering av internetavbrott och stöd för olika enheter. Ingen kod har skrivits utan fokuset var främst att lära sig om hur krav dokumenteras/testas.

---

## Dokumentation
All dokumentation som har skapats under arbetet finns nedan:
**[Docs-Krav-och-use-cases](Docs-Krav-och-use-cases/)**
### Krav och systemanalys
| Dokument                                                                                        | Beskrivning                                                                                      |
| ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| [01 – Inledning](Docs-Krav-och-use-cases/Gomoku-krav/01-inledning.md)                           | Systemets syfte, användare, problemområde och dokumentstruktur                                   |
| [03 – Kompletterande krav](Docs-Krav-och-use-cases/Gomoku-krav/03-kompletterande-krav.md)       | Kompletterande krav för till exempel anonymt spelande, cookies, återanslutning och pausning      |
| [04 – Icke-funktionella krav](Docs-Krav-och-use-cases/Gomoku-krav/04-icke-funktionella-krav.md) | Krav på bland annat användarvänlighet, responsivitet, prestanda, tillförlitlighet och integritet |
| [05 – Begreppsmodell](Docs-Krav-och-use-cases/Gomoku-krav/05-begreppsmodell.md)                 | Flera viktiga begrepp och deras relation till systemet                                           |
| [08 – Business Rules](Docs-Krav-och-use-cases/Gomoku-krav/08-business-rules.md)                 | Regler som systemet ska följa under en Gomoku-match oavsett state                                |

---

# Användningsfall
Use cases beskriver olika mål för scenarier där aktör interagerar med gomoku.
**[Öppna mappen för hitta alla Use Cases](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/)**
### UC som har skapats under projektet
| ID                                                                                                                 | Use Case                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------- |
| [UC-01](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-01-starta-en-match.md)                               | Starta en match                 |
| [UC-02](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-02-spela-mot-en-dator.md)                            | Spela mot en dator              |
| [UC-03](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-03-valja-svarighetsgrad.md)                          | Välja svårighetsgrad            |
| [UC-04](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-04-anvandaren-spelar-anonym-gdpr.md)                 | Spela anonymt utan konto        |
| [UC-05](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-05-anvandare-for-inget-cookies.md)                   | Hantera cookies                 |
| [UC-06](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-06-anvandaren-bjuder-in-med-lank.md)                 | Bjuda in en vän via länk        |
| [UC-07](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-07-spelaren-ansluta-till-en-match.md)                | Ansluta till en match           |
| [UC-09](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-09-spelaren-vill-fortsatta-pagaande-match.md)        | Fortsätta en pågående match     |
| [UC-10](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-10-spelaren-vill-se-match-resultat.md)               | Se matchresultat                |
| [UC-11](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-11-spelaren-vill-fortsätta-efter-internetavgrott.md) | Fortsätta efter internetavbrott |


---

# Test Cases
Projektet innehåller 24 testfall som täcker både funktionella och icke-funktionella scenarier, men inte allt i systemet. Med mer tid/resurser hade större täckning av systemet varit möjligt att uppfylla
**[Här hittar du alla testfall](Docs-Krav-och-use-cases/Gomoku-krav/use-och-test-cases/Information-for-alla-tc.md)**
### Funktionella testfall
Testfallen **TC-01–TC-20** behandlar bland annat:

* start av match,
* spel mot dator,
* ogiltiga drag,
* turordning,
* fem i rad,
* oavgjort,
* nya matcher,
* svårighetsgrader,
* anonymt spelande,
* cookies,
* spellänkar,
* anslutning till matcher,
* lokalt spel,
* matchens state,
* och internetavbrott.

### Icke-funktionella testfall
Testfallen **TC-21–TC-24** behandlar bland annat:
* responsiv design,
* webbläsaranvändning utan installation,
* visuell stabilitet,
* och personlig information i spellänkar.

---

# UML och modeller
Projektet innehåller flera diagram som används för att beskriva systemets beteende och olika delar av spelprocessen som går att verifiera.
**[Här hittar du dom, läs översikt först!](Docs-Krav-och-use-cases/Gomoku-krav/UML/00-oversikt-Gomoku.md)**
| Diagram                                                                                     | Syfte                                                       |
| ------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| [UML-översikt](Docs-Krav-och-use-cases/Gomoku-krav/UML/00-oversikt-Gomoku.md)               | Översikt över projektets modeller                           |
| [Sekvensdiagram](Docs-Krav-och-use-cases/Gomoku-krav/UML/01-sekvensdiagram-Gomoku.md)       | Visar kommunikationen mellan systemets delar under ett drag |
| [Aktivitetsdiagram](Docs-Krav-och-use-cases/Gomoku-krav/UML/02-aktivitetsdiagram-Gomoku.md) | Visar spelomgångens arbetsflöde och alternativa vägar       |
| [Tillståndsdiagram](Docs-Krav-och-use-cases/Gomoku-krav/UML/03-tillstandsdiagram-Gomoku.md) | Visar hur spelets olika tillstånd förändras under en match  |

Diagrammen används som stöd för att förstå systemets beteende och för att identifiera olika scenarier som senare kan verifieras genom testfall.

# Utvecklingsprocess
Dokumentationen visar flera delar av den process som använts under projektet:

```text
 Kundintervju
       │
       ▼
 Kravfångst
       │
       ▼
Use Cases/userstory
       │
       ▼
 Business Rules
       │
       ▼
 User Journey
       │
       ▼
 UML-modellering
       │
       ▼
 Test Cases
```

På så sätt används olika dokumentationsformer för att beskriva samma system ur olika perspektiv:

**Krav** = vad systemet behöver uppfylla (Fr och NFR)

**Use Cases** = hur en användaren interagerar med systemet (Gomoku)

**Business Rules** = vilka regler som systemet måste följa

**User Journey** = hur användaren upplever processen

**UML** = hur olika beteende och flöden kan modelleras

**Test Cases** = hur scenarier kan verifieras

---

# Projektstruktur
Repositoryts struktur ser ut så här:
```text
GomokuProjektTeam4/
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── Docs-Krav-och-use-cases/
│   │
│   ├── Anvandningsfall-for-Gomoku/
│   │   ├── UC-01-starta-en-match.md
│   │   ├── UC-02-spela-mot-en-dator.md
│   │   ├── UC-03-valja-svarighetsgrad.md
│   │   ├── UC-04-anvandaren-spelar-anonym-gdpr.md
│   │   ├── UC-05-anvandare-for-inget-cookies.md
│   │   ├── UC-06-anvandaren-bjuder-in-med-lank.md
│   │   ├── UC-07-spelaren-ansluta-till-en-match.md
│   │   ├── UC-09-spelaren-vill-fortsatta-pagaande-match.md
│   │   ├── UC-10-spelaren-vill-se-match-resultat.md
│   │   ├── UC-11-spelaren-vill-fortsätta-efter-internetavgrott.md
│   │   └── UC-12 ... Spela-samma-plats.md
│   │
│   ├── Gomoku-krav/
│   │   ├── Begreppslista/
│   │   │   └── begreppslista-for-gomoku.md
│   │   │
│   │   ├── UML/
│   │   │   ├── 00-oversikt-Gomoku.md
│   │   │   ├── 01-sekvensdiagram-Gomoku.md
│   │   │   ├── 02-aktivitetsdiagram-Gomoku.md
│   │   │   └── 03-tillstandsdiagram-Gomoku.md
│   │   │
│   │   ├── intervju-krav-for-icke-funktionella/
│   │   │   └── Intervju-med-kund-och-krav.md
│   │   │
│   │   ├── use-och-test-cases/
│   │   │   ├── Information-for-alla-tc.md
│   │   │   └── TC-01 ... TC-24
│   │   │
│   │   ├── 01-inledning.md
│   │   ├── 02-funktionella-krav.md
│   │   ├── 03-kompletterande-krav.md
│   │   ├── 04-icke-funktionella-krav.md
│   │   ├── 05-begreppsmodell.md
│   │   ├── 06-user-journey.md
│   │   ├── 07-use-cases-overview.md
│   │   ├── 08-business rules.md
│   │   └── 09-traceability-matrix.md
│   │
│   └── readme.md
│
├── .gitignore
├── LICENSE
└── README.md
```

---

