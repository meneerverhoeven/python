# Foutcodes

Deze les gaat over foutcodes. Je leert wat ze zijn, hoe je ze kunt lezen en hoe je ze oplost.

## Doel van deze les

- [ ] Begrijpen wat **foutmeldingen** zijn en de meest voorkomende soorten.
- [ ] Leren hoe je **foutmeldingen** kunt oplossen en voorkomen.

## Wat zijn foutmeldingen?
Foutmeldingen, in Python ook wel "Errors" genoemd, geven aan wanneer iets niet heeft gewerkt in je code. 
Dit kan zijn omdat je een fout hebt gemaakt, zoals het verkeerd typen van een variabele naam, 
of omdat je iets probeert te doen dat niet mogelijk is, zoals delen door nul. 
Foutmeldingen zijn belangrijk omdat ze je helpen om problemen in je code te vinden en op te lossen.

Een foutmelding is eigenlijk niks anders dan je computer die zegt "Hey, ik snap dit niet, kun je het iets duidelijker maken?".
**Zelfs de beste ontwikkelaars maken fouten en krijgen errors**. Het is een normaal onderdeel van het programmeren.
Het is belangrijk om te leren hoe je deze foutmeldingen kunt lezen en begrijpen, zodat je ze zelf kunt oplossen.

## Soorten foutmeldingen
Er zijn veel verschillende soorten foutmeldingen. Een deel daarvan komen van Python zelf, maar je kan ze ook zelf ontwikkelen om een foutmelding te geven.
Hieronder staan de meest voorkomende foutmeldingen die je tegen kunt komen:
- **SyntaxError**: Dit betekent dat er een fout in de opbouw van je code zit. Bijvoorbeeld, als je een haakje vergeet te sluiten of een dubbele punt mist.
- **IndentationError**: Dit betekent dat je code niet goed is ingesprongen. Python gebruikt inspringen (4 spaties) om te begrijpen welke code bij elkaar hoort.
- **NameError**: Dit betekent dat je een variabele probeert te gebruiken die nog niet is gedefinieerd. Bijvoorbeeld, als je een variabele probeert te printen voordat je deze hebt aangemaakt.
- **TypeError**: Dit betekent dat je een functie probeert te gebruiken met een verkeerd datatype. Bijvoorbeeld, als je probeert een string op te tellen bij een integer.
- **ValueError**: Dit betekent dat je een functie probeert te gebruiken met een waarde die niet geldig is. Bijvoorbeeld, als je probeert een string om te zetten naar een integer, maar de string bevat geen getal.

Meestal geeft de naam van de foutmelding al een hint wat het probleem is. Bijvoorbeeld de `ZeroDivisionError` geeft aan dat je probeert te delen door nul.

## Formaat van een foutmelding
Foutmeldingen hebben altijd een bepaald formaat. Dit helpt je om snel te begrijpen wat er aan de hand is.
Hier is een voorbeeld van een foutmelding:
```Traceback (most recent call last):
  File "script.py", line 1, in <module>
    print(naam)
NameError: name 'naam' is not defined
```
In dit voorbeeld zie je dat de foutmelding begint met `Traceback`, wat betekent dat Python je laat zien waar de fout is opgetreden.
De traceback laat zien welke regels code zijn uitgevoerd voordat de fout optrad. Het geeft ook exact aan op welk regelnummer de fout is opgetreden.
De foutmelding zelf staat altijd onderaan en geeft aan wat er mis is gegaan. In dit geval is de foutmelding `NameError`, wat betekent dat er geen variabel 'naam' is gedefinieerd.

## Hoe los je foutmeldingen op?
Om foutmeldingen op te lossen, moet je eerst begrijpen wat de foutmelding betekent. Kijk dus eerst onderaan de foutmelding naar het soort foutmelding en de regel waar de fout is opgetreden.
Ga naar de genoemde regel in je code en vergelijk dit met de genoemde foutmelding. Is het duidelijk wat er mis is?
Als je het probleem niet kunt vinden, probeer dan de volgende stappen:
1. **Lees de foutmelding aandachtig**: Kijk goed naar de foutmelding en probeer te begrijpen wat er mis is.
2. **Controleer de regel waar de fout is opgetreden**: Kijk goed naar de regel die in de foutmelding staat en vergelijk deze met de foutmelding.
3. **Zoek naar typfouten**: Kijk goed of je geen typfouten hebt gemaakt in je code. Dit is de meest voorkomende oorzaak van foutmeldingen.
4. **Controleer de variabelen**: Kijk goed of je geen variabelen probeert te gebruiken die nog niet zijn gedefinieerd. Je kan je variabelen ook tijdelijk printen om te kijken wat er in staat.
5. **Zoek online**: Als je er niet uitkomt, zoek dan online naar de foutmelding. Vaak zijn er al oplossingen te vinden op forums of StackOverflow.
6. **Vraag om hulp**: Als je er echt niet uitkomt, vraag dan om hulp aan een medeleerling of docent. Het is helemaal niet erg om hulp te vragen!

## Oefenen
Hieronder staan wat stukken code die een foutmelding geven. Kopieer een stuk code naar Thonny en bekijk de fout. Los de fout daarna op.

```python
naam = "Emma"
print(naan)
```

```python
leeftijd = input("Hoe oud ben je? ")
leeftijd_volgend_jaar = leeftijd + 1
print("Volgend jaar ben je " + leeftijd_volgend_jaar + " jaar oud.")
```

```python
naam = "Emma"
leeftijd = int(naam)
print("Je naam is " + naam + " en je leeftijd is " + leeftijd)
```

```python
print((1 + 2 * 3) # = 6
```

```python
getal = int(input("Geef een getal: "))
getal = getal / 0
print("Het getal is " + str(getal))
```

```python
getal = int(input("Geef een getal: "))
getal = getal * getal Bereken het kwadraat!
print("Het getal is " + str(getal))
```

```python
getal1 = 4
getal2 = 
print(getal1 + getal2)
```

```python
1getal = 4
getal2 = 5
print(1getal + getal2)
```
