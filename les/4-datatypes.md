# Datatypes

In deze les leer je hoe wat datatypes zijn, waarom we ze gebruiken, en hoe je de een in de ander om kan zetten.

## Doel van deze les
- [ ] Begrijpen wat **datatypes** zijn en waarom ze belangrijk zijn.
- [ ] Werken met verschillende **datatypes** in Python.
- [ ] Casten van datatypes in Python.


## Datatypes

Datatypes zijn, zoals de naam al verklapt, de types van je data. Data is alles wat je in je programma gebruikt, 
zoals getallen, tekst, lijsten, en meer. Elk datatype heeft zijn eigen eigenschappen en 
manieren waarop je ermee kunt werken. Met getallen kun je bijvoorbeeld rekenen, maar niet met tekst.
Het is belangrijk om te weten welk datatype je gebruikt, 
omdat dit invloed heeft op hoe je data kunt manipuleren en welke functies je kunt toepassen.

### Waarom zijn datatypes belangrijk?
Datatypes zijn belangrijk, omdat het bepaalt wat je kan doen met een bepaald stuk data.
Computers zijn nog steeds best dom. De computer moet exact weten om wat voor data het gaat, om te weten wat mogelijk is.
Python is hier gelukkig wat slimmer mee, en kan zelf de meeste datatypes herkennen en dit aanpassen als je dat vraagt.
Als je ooit andere talen gaat gebruiken, zoals C of Java, moet je zelf het datatype aangeven en kan je vaak niet het datatype van een variabel zomaar veranderen.

### Soorten datatypes
De meest voorkomende datatypes in Python zijn: tekst en getallen. Er zijn er nog veel meer, maar die laten we nu even achterwege.
De datatypes hebben wel allemaal andere namen. Deze namen worden in de meeste programmeertalen gebruikt, dus het is handig om de termen nu al te leren.
- **String**: Dit is tekst. In Python gebruik je hiervoor altijd enkele of dubbele aanhalingstekens. Bijvoorbeeld: `"Hallo wereld!"` of `'Hallo wereld!'`
- **Integer**: Dit is een heel getal. Er zijn hier geen aanhalingstekens nodig. Bijvoorbeeld: `42` of `-7`
- **Float**: Dit is een kommagetal. Ook hier zijn geen aanhalingstekens nodig. Wel moet je een punt `.` gebruiken i.p.v. een komma `,`.  Bijvoorbeeld: `3.14` of `-0.5`

### Casten van datatypes

Casten is het omzetten van het ene datatype naar het andere datatype. Dit kan handig zijn als je bijvoorbeeld een getal wilt optellen bij een tekst, of als je een tekst wilt omzetten naar een getal.
In Python kun je dit doen met de functies `int()`, `float()` en `str()`. Deze zijn afgeleid van de namen van de datatypes in Python. Je zult ze soms zien in foutcodes.

Voorbeeld:
```python
leeftijd = 16
leeftijd_str = str(leeftijd)
print("Je leeftijd is " + leeftijd_str)
```
Geeft de output:
> Je leeftijd is 16

Hier hebben we de integer `leeftijd` omgezet naar een string met de functie `str()`, zodat we het kunnen combineren met andere tekst.

### Opdracht
Vraag de gebruiker om twee getallen in te voeren. Zet deze om naar het juiste datatype en tel ze bij elkaar op. Print het resultaat.
Probeer ook te vermenigvuldigen (met `*`), delen (met `/`), en minnen (met `-`).

> **Voorbeeld:**
>
> **Invoer:**
> ```
> Geef het eerste getal: 5
> Geef het tweede getal: 4.5
> ```  
>
> **Uitvoer:**
> ```
> Het resultaat is: 9.5
> ```

> [!TIP]
> Gebruik `input()` om de gebruiker te vragen naar deze gegevens. De vraag komt
> in de shell te staan en daar kan je ook het antwoord typen.

## Variabelen bewerken
We kunnen variabelen bewerken op meerder manieren. Bij getallen kunnen we bijvoorbeeld:
- Optellen met `+`
- Aftrekken met `-`
- Vermenigvuldigen met `*`
- Delen met `/`
- Tot de macht doen met `**`

Dit soort aanpassingen kunnen we ook doen met tekst. We kunnen natuurlijk `+` gebruiken om tekst aan elkaar te plakken.
Ook hebben we de `*` operator, waarmee we een tekst een aantal keer kunnen herhalen. Daarnaast hebben we ook drie handige functies.
- `len()`: Hiermee kan je de lengte van een tekst opvragen. Dit is het aantal tekens in de tekst.
- `upper()`: Hiermee kan je de tekst in hoofdletters zetten.
- `lower()`: Hiermee kan je de tekst in kleine letters zetten.
Hieronder zie je een klein voorbeeld van hoe deze functies werken.
```python
naam = "Emma"
print("Hallo " + naam)
print("Hallo " + naam * 3)
print("Hallo " + naam.upper())
print("Hallo " + naam.lower())
print("De naam is " + str(len(naam)) + " letters")
```
Dit geeft als uitvoer het volgende:
> Hallo Emma
> Hallo EmmaEmmaEmma
> Hallo EMMA
> Hallo emma
> De naam is 4 letters

Zie je dat de functies `upper()` en `lower()` anders werken dan `len()`? 
`len()` werkt net zoals `print()` en `input()`. We zetten de tekst die we aan de functie willen geven tussen de haakjes.
Bij `upper()` en `lower()` zetten we de tekst voor de functie, met een `.` ertussen. 
Dit is een andere manier van functies aanroepen. We gaan er nu nog niet op in hoe dit werkt, maar onthoud dit verschil goed!

## Opdrachten
[Maak eerst de opdrachten van Fundament](https://fundament-online.nl/leeromgeving/content.php?paragraaf_id=114950)
Daarna maak je een programma dat de leeftijd van de gebruiker vraagt. We nemen even aan dat de gebruiker vandaag jarig is.
Print dan voor ieder jaar oud een keer "Hieperdepiep, hoera!".
>**Voorbeeld:**
> 
> **Invoer:**
> ```
> Hoe oud ben je? 5
> ```
> **Uitvoer:**
> ```
> Hieperdepiep, hoera! Hieperdepiep, hoera! Hieperdepiep, hoera! Hieperdepiep, hoera! Hieperdepiep, hoera! 
> ```