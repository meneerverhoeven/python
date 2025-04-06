# Datums en Tijden

In deze les leer je hoe je met datums en tijden kunt werken in Python. 
Dit is handig voor het maken van programma's die met tijd en data werken, zoals agenda-apps of timers.

## Doel van deze les
- [ ] Werken met datums en tijden in Python.
- [ ] Het gebruik van de `datetime` module.
- [ ] Het maken van een timer met de `time` module.

## Hoe werken datums en tijden in Python?
Python heeft een ingebouwde module genaamd `datetime` die je helpt om met datums en tijden te werken.
Met deze module kun je datums en tijden maken, bewerken en formatteren. Het is een aparte module, omdat je het niet altijd nodig hebt.
Om met modules te werken, moet je ze eerst importeren. Dit doe je met het `import`-commando.
```python
import datetime
```
Hierdoor krijg je toegang tot de functionaliteit van de `datetime` module. Deze `import`-regels staan altijd bovenaan je bestand.
Meestal importeren we alleen het datatype `datetime` uit de module, omdat we dat het meest gebruiken. Hier zit ook de meeste functionaliteit in.
```python
from datetime import datetime
```

## De `datetime` module
De `datetime` module heeft verschillende functionaliteiten. Je kan bijvoorbeeld de huidige datum en tijd ophalen, datums en tijden vergelijken, en datums en tijden formatteren.
Hier zijn een paar voorbeelden van wat je met de `datetime` module kunt doen:
```python
from datetime import datetime
# Huidige datum en tijd
nu = datetime.now()
print("Huidige datum en tijd:", nu)
# Specifieke datum en tijd
specifieke_datum = datetime(2023, 10, 1, 12, 0, 0)
print("Specifieke datum en tijd:", specifieke_datum)
# Verschil tussen twee datums
verschil = nu - specifieke_datum
print("Verschil in dagen:", verschil.days)
```
Je kan ook een datum aanmaken zonder tijd, of de datum pakken van een `datetime` variabel. Dit kan handig zijn als de tijd niet belangrijk is. De tijd wordt dan standaard op 00:00:00 gezet.
```python
from datetime import datetime
# Huidige datum
nu = datetime.now()
specifieke_datum = datetime(2023, 10, 1)
print("Huidige datum:", nu.date())
print("Specifieke datum:", specifieke_datum.date())
```

Je kan de meeste onderdelen wel uit een datum halen:
```python
from datetime import datetime
nu = datetime.now()
jaar = nu.year
maand = nu.month # geeft 1 voor januari, 2 voor februari, etc.
dag = nu.day
uren = nu.hour
minuten = nu.minute
seconden = nu.second
milliseconden = nu.microsecond
dag_van_de_week = nu.weekday() # geeft 0 voor maandag, 1 voor dinsdag, etc.
```
Wat je verder allemaal met de `datetime` module kan doen, is te vinden in de [documentatie](https://docs.python.org/3/library/datetime.html#datetime.datetime.min).

## De `time` module
De `datetime` module is voornamelijk bedoeld om te werken met vaste datums en tijden. De `time` module stelt je in staat om met tijd te werken, zoals timers, stopwatches en pauzes in je code.

Je kan bijvoorbeeld tellen hoe lang het duurt voor je code om uit te voeren:
```python
import time
start_tijd = time.time() # tijd in seconden
# Hier komt je code, bijvoorbeeld
print("Hallo wereld!")
print("Dit duurt even...")
print("Nog even wachten...")
eind_tijd = time.time() # tijd in seconden
tijdsverschil = eind_tijd - start_tijd
print("Tijdsverschil:", tijdsverschil, "seconden")
```
Je kan ook een pauze inlassen in je code met de `sleep` functie. Dit kan handig zijn als je een timer wilt maken of als je wilt wachten op een bepaalde tijd.
```python
import time
print("Hallo wereld!")
time.sleep(2) # wacht 2 seconden
print("Dit duurt even...")
```

## Opdracht
Vraag de gebruiker om hun geboortedatum in te voeren. Zet dit om naar een `datetime` object en 
**bereken** hun leeftijd in jaren, maanden en dagen. Print het resultaat. Print ook hoe lang het duurt om de code uit te voeren.
Bedenk goed hoe je de geboortedatum op moet vragen en welke datatype(s) je hiervoor nodig hebt. Bekijk de documentatie van de `datetime` module om te zien wat mogelijk is.
Voor een extra uitdaging: bepaal hoeveel seconden de gebruiker al leeft.
> **Voorbeeld:**
> 
> **Invoer:**
> ```
> Wat is je geboortedatum? 01-10-2005
> ```
> 
> **Uitvoer:**
> ```
> Je bent 19 jaar, 6 maanden en 10 dagen oud.
> Je leeft al 615663110 seconden.
> ```
