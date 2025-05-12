# Functies gebruiken en maken

In deze les leer je hoe je functies in Python gebruikt en zelf maakt. Functies zijn stukjes herbruikbare code die iets doen. Bijvoorbeeld `print()` en `input()` zijn functies.

## Doel van deze les
- [ ] Standaardfuncties gebruiken, zoals `print`, `input`, `len`, `range`, `int`, `float`, en `str`.
- [ ] Methoden gebruiken zoals `.upper()`, `.lower()` en `datetime.now()`.
- [ ] Werken met parameters in functies.
- [ ] Zelf functies schrijven en gebruiken.

## Standaardfuncties

Python heeft een heleboel functies die je meteen kunt gebruiken. Hier zijn er een paar die je vaak nodig hebt:

```python
print("Hallo!")  # Laat iets zien op het scherm
naam = input("Wat is je naam? ")  # Vraagt iets aan de gebruiker
getal = int("42")  # Zet tekst om naar een geheel getal
kommagetal = float("3.14")  # Zet tekst om naar een kommagetal
tekst = str(100)  # Zet getal om naar tekst
lijst = range(5)  # Maakt een lijst van getallen: 0 t/m 4
print(len("Hallo"))  # Geeft het aantal tekens in een string
```

Let op: `range()` kan meerdere parameters hebben. Zie opdracht 2.

## Methoden

Sommige functies werken alleen op een bepaald soort datatype. Deze noem je **methoden**. Je schrijft ze met een punt achter het datatype:

```python
naam = "emma"        # Datatype: string
print(naam.upper())  # Geeft: EMMA
print(naam.lower())  # Geeft: emma
```

Sommige methoden komen uit bibliotheken. Bijvoorbeeld: `datetime.now()` komt uit de `datetime`-bibliotheek en is voor het datatype `datetime`:

```python
from datetime import datetime
nu = datetime.now()
print(nu)
```

## Zelf functies maken

Soms wil je je eigen functie maken. Dat doe je zo:

```python
def begroet(naam):
    print("Hallo", naam)
```

- `def` is kort voor definitie. Hiermee geven we aan dat we een functie gaan maken
- Daarna volgt de naam van de functie, deze heeft dezelfde regels voor de naam als een variabel. Hiermee roep je ook de functie aan, bijvoorbeeld `begroet("Emma")`
- Daarna volgen haakjes, met daar tussen de parameters. In het voorbeeld `begroet("Emma")` is `"Emma"` het variabel dat we doorgeven voor de parameter `naam`
- Als laatste op de eerste regel is een dubbele punt, zoals ook bij if-statements en loops
- De code van een functie moet daarna worden ingesprongen, net zoals bij if-statements en loops



Je gebruikt de functie door hem aan te roepen:

```python
begroet("Emma")
```

Een functie kan ook iets **teruggeven** met `return`:

```python
def verdubbel(getal):
    return getal * 2

antwoord = verdubbel(5)
print(antwoord)  # Geeft: 10
```

## Opdracht 1 – Tekstbewerking

Schrijf een functie die het volgende doet:
- vraag de gebruiker om een tekst
- print de tekst in hoofdletters en kleine letters
- print ook hoeveel tekens de tekst heeft

Roep de functie aan onderaan je script.

> **Voorbeeld:**
> ```
> Geef een tekst: Hallo Wereld
> Hoofdletters: HALLO WERELD
> Kleine letters: hallo wereld
> Aantal tekens: 12
> ```

## Opdracht 2 – Werken met `range`

Schrijf een functie die `range()` gebruikt om een lijst van getallen te maken.

1. Vraag het begingetal, eindgetal en stapgrootte aan de gebruiker.
2. Print de getallen in de lijst d.m.v. een `for`-loop
3. Extra uitdaging: maak het begingetal en de stapgrootte optioneel


> **Voorbeeld:**
> ```
> Geef een begingetal: 2
> Geef een eindgetal: 10
> Geef een stapgrootte: 2
> 2
> 4
> 6
> 8
> ```

## Opdracht 3 – Eigen functie schrijven

Schrijf een functie `maak_groet(naam)` die een tekst teruggeeft zoals: `"Hallo Emma!"`. Gebruik de return-waarde om het te printen.

> **Voorbeeld:**
> ```
> Geef je naam: Emma
> Hallo Emma!
> ```

## Opdracht 4 – Rekenfunctie

Schrijf een functie `bereken_btw(prijs)` die 21% btw bij de prijs optelt en het totaal teruggeeft. Vraag de gebruiker om een bedrag en print het totaal.

> **Voorbeeld:**
> ```
> Geef het bedrag: 100
> Bedrag inclusief btw: 121.0
> ```

## Opdracht 5 – Extra: meervoudige parameters

Schrijf een functie `herhaal(tekst, aantal)` die een tekst meerdere keren onder elkaar print.

> **Voorbeeld:**
> ```
> Geef een tekst: Hoi
> Hoe vaak?: 3
> Hoi
> Hoi
> Hoi
> ```
