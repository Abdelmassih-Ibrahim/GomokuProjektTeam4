# Business Rules för Gomoku
Nedan finns regler och villkor som systemet alltid ska följa under en Gomoku match. Reglerna gäller oavsett om spelaren spelar mot en dator, lokalt eller mot en annan spelare eller på distans. 

## Match och spelare regler:

| ID | Regler |
|-------|-------|
|BR-01|En Gomoku match ska alltid bestå av två motståndare. Motståndaren kan vara en riktig person eller en dator.|
|BR-02|En pågående gomoku match ska ha ett tillstånd som visar spelbräde, placerade stenar och vilken spelares tur det är|

## Spelbräde och position regler
| ID | Regler |
|-------|-------|
|BR-3|Ett drag får endast placera en sten från sin plats till en ledig position|
|BR-4|En position som är upptagen får inte användas för ett nytt drag|
|BR-5|Ett drag kan bara utföras på en position som finns på spelbrädet|
|BR-6|En sten kan inte flyttas efter att den har placerats på en ledig position|
|BR-7|Varje drag ändrar matchens aktuella tillstånd tills någon vinner|


## Turordningen regler
| ID | Regler |
|-------|-------|
|BR-8|Endast när det är spelarens tur som hen får göra ett drag|
|BR-9|Spelarna ska alltid turas om att göra ett drag |
|BR-10|När ett giltigt drag blir gjort så ska turen alltid gå vidaren till motståndaren, om matchen inte har avslutats. |
|BR-11|Ett ogiltigt drag av en spelare får inte ändra turordningen|

## Vinst, förlust och oavgjort
| ID | Regler |
|-------|-------|
|BR-12|En spelare vinner matchen när hen får fem egna stenar i rad horisontellt, vertikalt eller diagonalt|
|BR-13|När en spelare får fem i rad avslutas matchen direkt. Motståndaren förlorar mot den som får fem i rad|
|BR-14|Om hela spelbrädet blir fullt innan någon spelare får fem i rad blir matchen oavgjord |
|BR-15|När en match avslutas genom vinst eller oavgjort får inga fler drag göras i matchen|

## Regler för-Spela mot datorn 
| ID | Regler |
|-------|-------|
|BR-16|När en spelare kör mot dator ska matchen fungera precis som en motståndare och endast göra drag när det är datorns tur|
|BR-17|Datorn ska alltid följa grundläggande spelregler precis som en mänsklig spelare|

## Pausa och återuppta en match 
| ID | Regler |
|-------|-------|
|BR-18|En avslutad match ska inte kunna återupptas som en pågående match|


