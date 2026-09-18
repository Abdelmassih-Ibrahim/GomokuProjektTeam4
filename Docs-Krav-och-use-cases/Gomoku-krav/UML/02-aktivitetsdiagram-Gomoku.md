# Aktivitetsdiagram för gomoku

#### Här är det viktigt att visa både ogiliga och giltiga drag men även vinst,oavgjort och nästa tur. 
#### Use case > testfall: verifierar att systemets funktion uppfyller kravet/scenariot som finns i dem olika UC.
#### Aktivitetsdiagram > testfall: Hjälpte oss hitta flöden/alternativa vägar som kanske inte är tydliga i våra UC

```mermaid
flowchart TD
    A([Start]) --> B[Gomoku-spelet startas]
    B --> C[Visa spelbrädet]
    C --> D[Spelaren väljer en ruta]

    D --> E[SPELETS logik kontrollerar rutan]

    E --> F{Är rutan ledig?}

    F -- Nej --> G[Visa felmeddelande]
    G --> D

    F -- Ja --> H[Placera spelpjäs på Spelbrädet]

    H --> I[SPELETS logik kontrollerar fem i rad]

    I --> J{Finns fem i rad?}

    J -- Ja --> K[Visa vinnare]
    K --> L([Spelet avslutas])

    J -- Nej --> M[SPELETS logik kontrollerar om brädet är fullt]

    M --> N{Är Spelbrädet fullt?}

    N -- Ja --> O[Visa oavgjort]
    O --> L

    N -- Nej --> P[Byt spelare]
    P --> C
```
