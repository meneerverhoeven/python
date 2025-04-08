# While-loops
Lees hiervoor eerst de paragraaf op [Fundament](https://fundament-online.nl/leeromgeving/content.php?paragraaf_id=114960)
en maak de bijbehorende opdrachten. Daarna kan je hier verder.

## Opdracht
We gaan getallen raden! Je gaat je gebruiker vragen om een getal tussen de 1 en de 100 te raden.
Natuurlijk willen we niet dat het getal altijd hetzelfde is, dus je krijgt hier de code voor een willekeurig integer cadeau.
Later ga je hier ook zelf mee werken!
```python
# Importeer de bibliotheek die willekeurige getallen kan maken
from random import randint
# Laat deze bibliotheek een willekeurige integer kiezen tussen 1 en 100 (1 en 100 tellen mee)
willekeurig_getal = randint(1, 100)
```

Je kan nu met behulp van een while loop en if-statements de gebruiker vragen een gok te doen.
Is de gok goed? Dan print je dat de gebruiker gewonnen heeft en stop je het programma.
Is de gok fout? Dan kijk je eerst of de gebruiker hoger of lager moet gokken.
Is de gok lager dan het getal? Dan print je dat de gok te laag is.
Is de gok hoger dan het getal? Dan print je dat de gok te hoog is.

**Let op:** Je moet bij while-loops en if-statements altijd met een tab inspringen. Hierdoor weet Python of de code bij de if-statement of while-loop hoort.
```python
# Dit zit buiten de while-loop
while 0 < 1:
    # Dit zit in de while-loop
    print("Dit gaat even duren...")
    if 0 < 1:
        # Dit zit in de if-statement, die in de while-loop zit
        print("Wow!")
    
    # Dit zit wel in de while-loop, maar niet in de if-statement
    print("En de loop begint opnieuw...")
```
Zie je dat het aantal tabjes telkens verschilt? Dit is hoe Python weet waar de code bij hoort. En jij nu dus ook!

> **Voorbeeld van de shell:**
> ```
> Geef een getal tussen de 1 en de 100: 50
> Je gok is te laag.
> Geef een getal tussen de 1 en de 100: 75
> Je gok is te hoog.
> Geef een getal tussen de 1 en de 100: 65
> Je hebt gewonnen!
> ```