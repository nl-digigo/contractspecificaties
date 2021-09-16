# Onderwerpentabel


Voorstel is om de volgende tabel te gebruiken voor het onderwerp van de eis, bestaande uit de functies, objecten, activiteiten en informatieproducten. Op de tweede regel staat de vertaling / binding naar de NEN 2660.


<table class="wikitable" style="text-align:left; valign:top">
<tr>
<th> URI
</th>
<th> Code
</th>
<th> Naam
</th>
<th> Type
</th>
<th> Definitie
</th>
<th> heeftDeel
</th>
<th> Eigenaar
</th></tr>
<tr>
<td> [unieke naam conform W3C](https://www.w3.org/wiki/URI) </td>
<td> skos:Notation </td>
<td> skos:prefLabel </td>
<td> rdfs:Class </td>
<td> skos:definition </td>
<td> nen2660:heeftDeel </td>
</td></tr>
</table>

## Toelichting op de kolommen in de tabel

### URI
Met URI wordt bedoeld: de unieke naam van het concept. Zie [URI conform W3C](https://www.w3.org/wiki/URI). 



### Code
In de code kan een in het project gebruikte code staan, die heeft mogelijk maakt in een gesprek naar de eis te verwijzen, zonder de volledige URI te hoeven benoemen. 



### Naam
De naam is de voor mensen leesbare naam van het concept. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.



### Type
Bij "Type" staan de onderwerpen van de eisen:
1. FysiekObject  
2. Functie  
3. Activiteit   
4. Informatieproducten



### Definitie
Bij "definitie" staat ofwel een tekst die het concept definieert, ofwel een URI die verwijst naar de definitie in een ontologie (objecttypenbibliotheek).



### HeeftDeel
Bij HeeftDeel kan een hiërarchie worden aangegeven zoals een objectenboom of functieboom zoals gebruikelijk in contracten. Een concept kan uit meerdere delen bestaan, er komen dan meerdere regels voor in de eisentabel. 



### Eigenaar
Vooral bij objecten is het voor de opdrachtgever handig, te weten wie de eigenaar is. De eigenaar is de persoon of rol bij de opdrachtgever die verantwoordelijk is voor beheer van dit objecttype, en die geconsulteerd moet worden bij afwijking van de eisen.



De taalbinding van eigenaar naar NEN 2660 is nog niet bekend. 

[Issue 16](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/16)



### Voorbeeldtabel



## Typen concepten in de tabel

### Functies

De functies in het contract (Vraagspecificatie Eisendeel) zijn ánders dan de activiteiten (Vraagspecificatie Procesdeel / ontwerp- en uitvoeringswerkzaamheden).
De functies geven weer, welke diensten het "systeem" moet vervullen tijdens het gebruik; een voorbeeld is een weg, die als functie "het verkeer moet geleiden".
de objecten in het contract zijn de functievervullers. De activiteiten zijn door mensen uit te voeren werkzaamheden tijdens het ontwerpen, bouwen, beheren en slopen van het object.

De taalbinding van functies naar NEN 2660 is nog niet bekend. 

De taalbinding van de relatie tussen functies en objecten naar NEN 2660 is nog niet bekend.

[Issue 13](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/13)

### Objecten

De objecten en objectenbomen in het contract (Vraagspecificatie Eisendeel) zijn “FysiekObject” uit NEN 2660. Dit kan in de kolom Type worden ingevuld.


### Activiteiten

De taalbinding van activiteiten naar NEN 2660 is nog niet bekend. 

[Issue 13](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/13)

### Informatieproducten
De informatieproducten in het contract staan vaak zowel in de Vraagspecificatie Procesdeel als in een separate Informatieleveringsspecificatie. 

Voorbeelden:

Informatieleveringsspecificatie
een rapport over het ontwerp van een weg
een sterkteberekening van een kunstwerk
een 3D model van een gebouw
een linked dataset met attributen van een voetpad.
Procesdeel
een V&G plan
een voortgangsrapportage

De taalbinding van informatieproducten naar NEN 2660 is nog niet bekend:

[Issue 12](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/12)
