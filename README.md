# GomokuProjektTeam4

Detta är ett Gomoku-spel (fem i rad) utvecklat som ett skolprojekt med fokus på kravfångst, systemanalys, use cases, modellering och testning.

Repositoryt innehåller projektets dokumentation och övriga filer som användes under utvecklingsprocessen.

## Innehåll

* [Om hela projektet](#om-hela-projektet)
* [Dokumentation](#dokumentation)
* [Användningsfall](#användningsfall)
* [Test Cases](#test-cases)
* [UML och modeller](#uml-och-modeller)
* [Utvecklingsprocess](#utvecklingsprocess)
* [Projektstruktur](#projektstrukturen)

---

## Om hela projektet
Gomoku är ett brädspel för två spelare där målet är att få fem egna stenar i rad – horisontellt, vertikalt eller diagonalt.
I projektet har vi arbetat med hur ett system kan analyseras och dokumenteras före och under utveckling. Fokus ligger därför inte bara på själva spelet, utan även på att beskriva:
* vad användaren behöver kunna göra (FR),
* hur användaren interagerar med systemet,
* vilka regler systemet måste följa (BR),
* vilka alternativa scenarier som kan uppstå (UC),
* vilka egenskaper systemet behöver ha (FR/NFR),
* och hur dessa scenarier kan testas (TC).
Projektet innehåller även delar om spel mot dator, spel med en annan person, spel via länk, anonymt spelande, hantering av internetavbrott och stöd för olika enheter.

# Dokumentation
All dokumentation som har skapats under arbetet finns i **[Docs-Krav-och-use-cases](Docs-Krav-och-use-cases/)**.
# Krav och systemanalys
| Dokument                                                                                        | Beskrivning                                                                                      |
| ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| [01 – Inledning](Docs-Krav-och-use-cases/Gomoku-krav/01-inledning.md)                           | Systemets syfte, användare, problemområde och dokumentstruktur                                   |
| [02 – Funktionella krav](Docs-Krav-och-use-cases/Gomoku-krav/02-funktionella-krav.md)           | Funktioner och beteenden som systemet ska stödja                                                 |
| [03 – Kompletterande krav](Docs-Krav-och-use-cases/Gomoku-krav/03-kompletterande-krav.md)       | Krav för bland annat anonymt spelande, cookies, återanslutning och pausning                      |
| [04 – Icke-funktionella krav](Docs-Krav-och-use-cases/Gomoku-krav/04-icke-funktionella-krav.md) | Krav på bland annat användarvänlighet, responsivitet, prestanda, tillförlitlighet och integritet |
| [05 – Begreppsmodell](Docs-Krav-och-use-cases/Gomoku-krav/05-begreppsmodell.md)                 | Viktiga begrepp och deras relationer i systemet                                                  |
| [06 – User Journey](Docs-Krav-och-use-cases/Gomoku-krav/06-user-journey.md)                     | Användarens flöde och upplevelse genom systemet                                                  |
| [07 – Use Cases Overview](Docs-Krav-och-use-cases/Gomoku-krav/07-use-cases-overview.md)         | Översikt över projektets use cases                                                               |
| [08 – Business Rules](Docs-Krav-och-use-cases/Gomoku-krav/08-business%20rules.md)               | Regler som systemet ska följa under en Gomoku-match                                              |
| [09 – Traceability Matrix](Docs-Krav-och-use-cases/Gomoku-krav/09-traceability-matrix.md)       | Spårbarhet mellan krav, use cases och testfall                                                   |

Övrig dokumentation finns i:

* Begreppslista: [Begreppslista](Docs-Krav-och-use-cases/Gomoku-krav/Begreppslista/)
* Intervju och krav: [Intervju med kund och krav](Docs-Krav-och-use-cases/Gomoku-krav/intervju-krav-for-icke-funktionella/)
* Kundacceptanstest: [Gomoku Kundacceptanstest](Docs-Krav-och-use-cases/Gomoku-Kundacceptanstest/)
* AC-test och bevis: [AC-test och bevis](Docs-Krav-och-use-cases/ACtest-och-bevis/)

---

# Användningsfall

Use cases beskriver olika mål och scenarier där en aktör interagerar med Gomoku.

**[Öppna mappen med alla use cases](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/)**

| ID                                                                                                                 | Use Case                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------- |
| [UC-01](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-01-starta-en-match.md)                               | Starta en match                 |
| [UC-02](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-02-spela-mot-en-dator.md)                            | Spela mot en dator              |
| [UC-03](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-03-valja-svarighetsgrad.md)                          | Välja svårighetsgrad            |
| [UC-04](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-04-anvandaren-spelar-anonym-gdpr.md)                 | Spela anonymt utan konto        |
| [UC-05](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-05-anvandare-for-inget-cookies.md)                   | Hantera cookies                 |
| [UC-06](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-06-anvandaren-bjuder-in-med-lank.md)                 | Bjuda in en vän via länk        |
| [UC-07](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-07-spelaren-ansluta-till-en-match.md)                | Ansluta till en match           |
| [UC-08](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-08-avsluta-pagaande-match.md)                        | Avsluta en pågående match       |
| [UC-09](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-09-spelaren-vill-fortsatta-pagaande-match.md)        | Fortsätta en pågående match     |
| [UC-10](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-10-spelaren-vill-se-match-resultat.md)               | Se matchresultat                |
| [UC-11](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-11-spelaren-vill-fortsätta-efter-internetavgrott.md) | Fortsätta efter internetavbrott |
| [UC-12](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-12–Spela-samma-plats.md)                           | Spela på samma plats            |
| [UC-13](Docs-Krav-och-use-cases/Anvandningsfall-for-Gomoku/UC-13-spela-hot-seat-multiplayer.md)                    | Spela hot-seat multiplayer      |

---

# Test Cases

Projektet innehåller **26 testfall (TC-01–TC-26)**. De täcker både funktionella och icke-funktionella scenarier.

**[Här hittar du alla testfall](Docs-Krav-och-use-cases/Gomoku-krav/use-och-test-cases/Information-for-alla-tc.md)**
## (:
## (:
## (:
# UML och modeller
Projektet innehåller **4 UML-diagram/dokument** som används för att beskriva systemets beteende och olika delar av spelprocessen.
**[Här hittar du UML-översikten](Docs-Krav-och-use-cases/Gomoku-krav/UML/00-oversikt-Gomoku.md)**

| Diagram                                                                                     | Syfte                                                       |
| ------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| [UML-översikt](Docs-Krav-och-use-cases/Gomoku-krav/UML/00-oversikt-Gomoku.md)               | Översikt över projektets modeller                           |
| [Sekvensdiagram](Docs-Krav-och-use-cases/Gomoku-krav/UML/01-sekvensdiagram-Gomoku.md)       | Visar kommunikationen mellan systemets delar under ett drag |
| [Aktivitetsdiagram](Docs-Krav-och-use-cases/Gomoku-krav/UML/02-aktivitetsdiagram-Gomoku.md) | Visar spelomgångens arbetsflöde och alternativa vägar       |
| [Tillståndsdiagram](Docs-Krav-och-use-cases/Gomoku-krav/UML/03-tillstandsdiagram-Gomoku.md) | Visar hur spelets olika tillstånd förändras under en match  |

---

# Utvecklingsprocess

Dokumentationen visar flera delar av den process som använts under projektet:

```text
Kundintervju
     │
     ▼
Kravfångst
     │
     ▼
Use Cases / user stories
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

* Krav = vad systemet behöver uppfylla (FR och NFR)
* Use Cases = hur användaren interagerar med systemet
* Business Rules = vilka regler systemet måste följa
* User Journey = hur användaren upplever processen
* UML = hur olika beteenden och flöden kan modelleras
* Test Cases = hur scenarier kan verifieras

---

# Projektstrukturen 

```text
GomokuProjektTeam4/
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── Docs-Krav-och-use-cases/
│   ├── ACtest-och-bevis/
│   │   ├── AC-testare.md
│   │   └── 15 PNG-bilder med testbevis
│   │
│   ├── Anvandningsfall-for-Gomoku/
│   │   ├── UC-01-starta-en-match.md
│   │   ├── UC-02-spela-mot-en-dator.md
│   │   ├── UC-03-valja-svarighetsgrad.md
│   │   ├── UC-04-anvandaren-spelar-anonym-gdpr.md
│   │   ├── UC-05-anvandare-for-inget-cookies.md
│   │   ├── UC-06-anvandaren-bjuder-in-med-lank.md
│   │   ├── UC-07-spelaren-ansluta-till-en-match.md
│   │   ├── UC-08-avsluta-pagaande-match.md
│   │   ├── UC-09-spelaren-vill-fortsatta-pagaande-match.md
│   │   ├── UC-10-spelaren-vill-se-match-resultat.md
│   │   ├── UC-11-spelaren-vill-fortsätta-efter-internetavgrott.md
│   │   ├── UC-12 – Spela-samma-plats.md
│   │   └── UC-13-spela-hot-seat-multiplayer.md
│   │
│   ├── Gomoku-Kundacceptanstest/
│   │   ├── Gomoku-Kundacceptanstest.md
│   │   └── BILD 1.png
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
│   │   │   └── TC-01 till TC-26
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
