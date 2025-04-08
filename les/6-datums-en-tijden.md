# Datums en Tijden

In deze les leer je hoe je met datums en tijden kunt werken in Python. 
Dit is handig voor het maken van programma's die met tijd en data werken, zoals agenda-apps of timers.

## Doel van deze les
- [ ] Werken met datums en tijden in Python.
- [ ] Het gebruik van de `datetime` bibliotheek.
- [ ] Het maken van een timer met de `time` bibliotheek.

## Hoe werken datums en tijden in Python?
Python heeft een ingebouwde bibliotheek genaamd `datetime` die je helpt om met datums en tijden te werken.
'Bibliotheek' is een term die je vaak tegenkomt in programmeren. Het zijn eigenlijk een soort bouwstenen die je kunt gebruiken om niet alles zelf te hoeven ontwikkelen. Het is een verzameling van functies en andere code die je kunt gebruiken in je eigen programma's.
Met deze bibliotheek kun je datums en tijden maken, bewerken en formatteren. Het is een aparte bibliotheek, omdat je het niet altijd nodig hebt.
Om met bibliotheken te werken, moet je ze eerst importeren. Dit doe je met het `import`-commando.
```python
import datetime
```
Hierdoor krijg je toegang tot de functionaliteit van de `datetime` bibliotheek. Deze `import`-regels staan altijd bovenaan je bestand.
Meestal importeren we alleen het datatype `datetime` uit de bibliotheek, omdat we dat het meest gebruiken. Hier zit ook de meeste functionaliteit in.
```python
from datetime import datetime
```

## De `datetime` bibliotheek
De `datetime` bibliotheek heeft verschillende functionaliteiten. Je kan bijvoorbeeld de huidige datum en tijd ophalen, datums en tijden vergelijken, en datums en tijden formatteren.
Hier zijn een paar voorbeelden van wat je met de `datetime` bibliotheek kunt doen:
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
Wat je verder allemaal met de `datetime` bibliotheek kan doen, is te vinden in de [documentatie](https://docs.python.org/3/library/datetime.html#datetime.datetime.min).

## De `time` bibliotheek
De `datetime` bibliotheek is voornamelijk bedoeld om te werken met vaste datums en tijden. De `time` bibliotheek stelt je in staat om met tijd te werken, zoals timers, stopwatches en pauzes in je code.

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
Bedenk goed hoe je de geboortedatum op moet vragen en welke datatype(s) je hiervoor nodig hebt. Bekijk de documentatie van de `datetime` bibliotheek om te zien wat mogelijk is.
**Let op:** wanneer je twee datums van elkaar aftrekt, krijg je geen `datetime` object terug, maar een `timedelta` object. Dit is een speciaal datatype dat het verschil tussen twee datums of tijden weergeeft. Je kan hier alleen de `days`, `seconds`, en `microseconds` van ophalen. Je moet dus zelf uitrekenen hoeveel jaren, maanden en dagen dit zijn.
Voor een extra uitdaging: bepaal hoeveel seconden de gebruiker al leeft.
> **Voorbeeld:**
> 
> **Invoer:**
> ```
> In welk jaar ben je geboren? 2005
> In welke maand ben je geboren? 10
> Op welke dag van de maand ben je geboren? 1
> ```
> 
> **Uitvoer:**
> ```
> Je bent 19 jaar, 6 maanden en 10 dagen oud.
> Je leeft al 615663110 seconden.
> ```
