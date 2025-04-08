# Voorwaarden

Soms wil je dat bepaalde code alleen wordt uitgevoerd als aan bepaalde voorwaarden is voldaan.
Deze les leer je hoe dat werkt.

## Doel van deze les
- [ ] Werken met booleaanse waarden.
- [ ] Werken met booleaanse operatoren.
- [ ] Werken met voorwaarden.

## Booleaanse waarden
Booleaanse waarden zijn vernoemd naar de wiskundige George Boole. 
Dit zijn waarden die alleen waar of onwaar kunnen zijn. 
In Python zijn er twee booleaanse waarden: `True` en `False`. Een stelling is waar als deze `True` is en onwaar als deze `False` is.
Dit zijn waardes die je net als getallen en tekst kan gebruiken in je code.
```python
naam = "Emma"
leeftijd = 18
is_volwassen = True
```
In dit voorbeeld is `is_volwassen` een booleaanse waarde die aangeeft of iemand volwassen is of niet.
Toch is dit vrij gelimiteerd zo. We kunnen nu alleen een waarde geven, maar nog niet eentje bepalen.

## Booleaanse operatoren
Met booleaanse operatoren kan je waarden vergelijken. Dit heeft altijd `True` of `False` als resultaat.
Je kent ze misschien al van wiskunde:
- `==` is gelijk aan
- `!=` is niet gelijk aan
- `>` is groter dan
- `<` is kleiner dan
- `>=` is groter dan of gelijk aan
- `<=` is kleiner dan of gelijk aan
- `and` is 'en'. Het checkt of beide voorwaarden `True` zijn.
- `or` is 'of'. Het checkt of een van de voorwaarden `True` is.
- `not` is 'niet'. Dit keert de waarde om. Als het `True` is, wordt het `False` en andersom.

Deze kan je gebruiken om waardes te vergelijken. Ze werken ook met tekst. Bij `<` en `>` wordt de tekst vergeleken op basis van de alfabetische volgorde.

Hier zijn wat voorbeelden van booleaanse operatoren:
```python
leeftijd = 18
is_volwassen = leeftijd >= 18
print(is_volwassen) # True

naam1 = "Emma"
naam2 = "Jan"
dezelfde_naam = naam1 == naam2
print(dezelfde_naam) # False
naam1_komt_eerder = naam1 < naam2
# Hieronder zetten we een komma tussen de tekst en de waarde. 
# Je kan zo meerdere dingen tegelijk printen zonder ze in dezelfde tekst te verwerken.
print("Komt Emma eerder dan Jan?", naam1_komt_eerder) # True

leeftijd1 = 18
leeftijd2 = 25
allebei_volwassen = leeftijd1 >= 18 and leeftijd2 >= 18
print("Allebei volwassen?", allebei_volwassen) # True
```

## Opdracht 1
Vraag drie getallen op bij de gebruiker. Controleer of de eerste twee opgeteld gelijk zijn aan het derde getal.
Controleer ook of de opsomming groter of kleiner is dan het derde getal. Print de uitkomst van de vergelijking.
> **Voorbeeld:**
> 
> **Invoer:**
> ```
> Geef een getal: 1
> Geef een getal: 2
> Geef een getal: 3
> ```
> 
> **Uitvoer:**
> ```
> Opsomming is gelijk aan het derde getal: True
> Opsomming is groter dan het derde getal: False
> Opsomming is kleiner dan het derde getal: True
> ```

## Voorwaarden
Nu we kunnen bepalen of een vergelijking waar of onwaar is, kunnen we ook voorwaarden maken.
Deze zijn heel handig en komen heel vaak voor in programmeren. Hier zijn wat voorbeelden waar je ze voor kan gebruiken:
- Bepaal of iemand volwassen is of niet.
- Controleer of een wachtwoord sterk genoeg is.
- Controleer of een getal even of oneven is.
- Controleer of een getal positief of negatief is.
- Controleer of je gratis verzending hebt bij een bestelling.
- Check of je reservering in het rooster past.
- Controleer of je een geldig e-mailadres hebt ingevoerd.
- Check of je bericht is gelezen op WhatsApp.

Om een voorwaarde te maken, gebruik je speciale woorden in Python. Dit zijn `if`, `elif` en `else`.
`if` is Engels voor 'als'. Dit is de simpelste voorwaarde. Je maakt eigenlijk een zin: `Als dit waar is, dan doe ik het volgende.`.
`elif` is een verkorte vorm van 'else if' en betekent 'anders, als'. Dit is een extra voorwaarde die je kan toevoegen. Dit kan je gebruiken om meerdere voorwaarden te maken.
`elif` wordt alleen gecontroleerd als de voorwaarde van `if` onwaar is. Het werkt dus anders dan twee losse `if`-voorwaarden onder elkaar.
`else` betekent 'anders'. Dit is de laatste optie die je kan gebruiken. Dit wordt uitgevoerd als geen van de andere voorwaarden waar zijn.
Hier is een voorbeeld van hoe je deze woorden kan gebruiken:
```python
leeftijd = 18
if leeftijd >= 18:
    print("Je bent volwassen.")
elif leeftijd >= 12:
    print("Je bent een tiener.")
else:
    print("Je bent een kind.")
```
In dit voorbeeld wordt de leeftijd gecontroleerd. Als de leeftijd groter of gelijk is aan 18, wordt er "Je bent volwassen." geprint.
Als de leeftijd groter of gelijk is aan 12, wordt er "Je bent een tiener." geprint. Als geen van deze voorwaarden waar is, wordt er "Je bent een kind." geprint.
Als je dit zou doen zonder `elif` en `else`, maar met alleen maar `if`, krijg je een ander resultaat:
```python
leeftijd = 18
if leeftijd >= 18:
    print("Je bent volwassen.")
if leeftijd >= 12:
    print("Je bent een tiener.")
if leeftijd < 12:
    print("Je bent een kind.")
```
In dit voorbeeld worden alle voorwaarden gecontroleerd. Dit betekent dat er "Je bent volwassen." en "Je bent een tiener." wordt geprint. Dit is niet wat we willen.

### LET OP
Een `if`, `elif` of `else` moet altijd met een dubbele punt eindigen. Dit is heel belangrijk, want zonder deze dubbele punt werkt de code niet.
Met de dubbele punt geef je aan dat er een nieuwe codeblok begint. Dit is de code die uitgevoerd wordt als de voorwaarde waar is en heeft een extra tab inspringing.

Bij `if` en `elif` **moeten** er voorwaarden gegeven worden tussen de `if`/`elif` en de dubbele punt. Dit zijn de voorwaarden die gecontroleerd worden.
De vaste structuur is dus:
```python
if voorwaarde:
    # Doe iets
elif andere_voorwaarde:
    # Doe iets anders
else:
    # Doe de uitzondering
```

## Opdracht 2
Bol.com geeft je gratis verzending vanaf €20. Maak een programma dat de gebruiker vraagt om het bedrag van hun bestelling. Controleer of ze gratis verzending hebben of niet. Print een samenvatting van hun bestelling.
> **Voorbeeld:**
> 
> **Invoer:**
> ```
> Geef het bedrag van je bestelling: 19
> ```
> 
> **Uitvoer:**
> ```
> Je bestelling is €19.
> Hiervan is €5 verzendkosten.
> Je totale kosten zijn €24.
> ```

## Opdracht 3
Maak een volledige rekenmachine. Vraag 2 getallen en de bewerkingen op bij de gebruiker. Gebruik `if`-voorwaarden om de juiste bewerking uit te voeren.
Probeer maar 1 keer `if` te gebruiken. Gebruik `elif` en `else` voor de andere bewerkingen.
> **Voorbeeld:**
> 
> **Invoer:**
> ```
> Geef een getal: 5
> Geef een getal: 2
> Geef een bewerking (+, -, *, /): +
> ```
> 
> **Uitvoer:**
> ```
> 5 + 2 = 7
> ```

## Opdracht 4
Maak een programma dat de gebruiker voor een gebruikersnaam en wachtwoord vraagt. Check of deze gelijk zijn aan de juiste gebruikersnaam en wachtwoord (jouw keuze).
Als dit zo is, print dan "Welkom [gebruikersnaam]". Als het wachtwoord niet klopt, print dan "Wachtwoord is onjuist". Als de gebruikersnaam niet klopt, print dan "Gebruikersnaam is onjuist".
Uitdaging: Voeg nog 2 gebruikers toe aan je systeem.
> **Voorbeeld:**
> 
> **Invoer:**
> ```
> Geef een gebruikersnaam: Emma
> Geef een wachtwoord: Emma123
> ```
> 
> **Uitvoer:**
> ```
> Welkom Emma
> ```