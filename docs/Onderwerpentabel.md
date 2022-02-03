# Onderwerpen

De onderwerpentabel wordt gebruikt voor de onderwerpen van de eisen, bestaande uit de functies, objecttypen, werkzaamheden en informatieproducten. Op de eerste regel staan de kolomnamen. Op de tweede regel staat een korte toelichting; op de derde regel de vertaling / binding naar de NEN2660-2 en andere standaarden. Op de vierde regel staat aangegeven, hoeveel relaties er kunnen voorkomen in dit veld (multipliciteit). Als er meer dan één relatie voorkomt, komen er regels bij in de uitwisseling. 

<p class="note">
De vertaling / binding van Eigenaren naar NEN2660-2 is nog niet bekend. Mogelijk wordt hier de DCTerms ontologie betrokken.
</p>

## Onderwerpentabel

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
<td> In deze kolom staat de unieke naam (URI) van het onderwerp. </td>
<td> In deze kolom staat de code ofwel het nummer van het onderwerp. </td>
<td> In deze kolom staat de naam van het onderwerp. </td>
<td> In deze kolom staat het type van het onderwerp: Objecttype, Functie, Werkzaamheid of Informatieproduct. </td>
<td> In deze kolom staat de definitie van het onderwerp. </td>
<td> In deze kolom staat de URI van een onderliggend onderwerp. </td>
<td> In deze kolom wordt aangegeven wie de eigenaar is van het onderwerp. </td>
</tr>
<tr>
<td> <href>[unieke naam conform W3C](https://www.w3.org/wiki/URI)</href> </td>
<td> skos:notation </td>
<td> skos:prefLabel </td>
<td> rdfs:Class </td>
<td> skos:definition </td>
<td> nen2660:heeftDeel </td>
<td> [dcmi-terms:rightsHolder](https://dublincore.org/specifications/dublin-core/dcmi-terms/#rightsHolder) </td>
</tr>
<tr>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 0:n </td>
<td> 0:n </td>
</tr>
</table>


## Voorbeeldtabel 

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
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldtabel </td>
<td> OBJ-0109 </td>
<td> Voorbeeld onderwerp </td>
<td> InformationObject </td>
<td> Onderwerp van een eis als voorbeeld in de documentatie </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#onderligeendvoorbeeldobject </td>
<td> BIM loket </td></tr>
</table>

### Onderliggend voorbeeldobject
heeftDeel uit de voorbeeldtabel


## Typen Onderwerpen

### Functies

De functies in het contract (Vraagspecificatie Eisendeel) zijn ánders dan de werkzaamheden (Vraagspecificatie Procesdeel / ontwerp- en uitvoeringswerkzaamheden).
De functies geven weer, welke diensten het "systeem" moet vervullen tijdens het gebruik; een voorbeeld is een weg, die als functie "het verkeer moet geleiden".
de objecten in het contract zijn de functievervullers. De activiteiten zijn door mensen uit te voeren werkzaamheden tijdens het ontwerpen, bouwen, beheren en slopen van het object.

<p class="note">
De vertaling / binding van functies naar NEN2660-2 is nog niet bekend. 
</p>

<p class="note">
De vertaling / binding van de relatie tussen functies en objecten naar NEN2660-2 is nog niet bekend.
</p>

[Issue 13](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/13)

### Objecttypen

De objecttypen en objecttypenboom ("decompositie") in het contract (Vraagspecificatie Eisendeel) zijn “FysiekObject” uit NEN2660-2. Dit kan in de kolom Type worden ingevuld.

[Issue 18](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/18)

### Werkzaamheden
De werkzaamheden zijn door mensen uit te voeren activiteiten tijdens het ontwerpen, bouwen, beheren en slopen van het object. 

<p class="note">
De vertaling / binding van activiteiten naar NEN2660-2 is nog niet bekend. 
</p>

[Issue 13](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/13)

### Informatieproducten
De informatieproducten in het contract staan vaak zowel in de Vraagspecificatie Procesdeel als in een separate Informatieleveringsspecificatie. Het betreft de gevraagde levering van 'documenten', dit kunnen alle bestandstypes zijn, ook datasets of geometrische bestanden.

Voorbeelden:

Informatieleveringsspecificatie:

* een rapport over het ontwerp van een weg
* een sterkteberekening van een kunstwerk
* een 3D model van een gebouw
* een linked dataset met attributen van een voetpad

Procesdeel:
* een V&G plan
* een voortgangsrapportage

<p class="note">
De vertaling / binding van informatieproducten naar NEN2660-2 is nog niet bekend. 
</p>

[Issue 12](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/12)

## Details onderwerpentabel

### URI 
In deze kolom staat de unieke naam (URI) van het onderwerp. Zie [URI conform W3C](https://www.w3.org/wiki/URI). 

De URI is unieke naam voor het onderwerp binnen het project; bij de definitie kan worden verwezen naar het type uit een ontologie ofwel objecttypenbibliotheek. 
Als de URI uit een ontologie direct als onderwerp wordt gebruikt, suggereer je daarmee dat de projecteis altijd geldt voor dit onderwerp; dat hoeft echter niet zo te zijn. Vandaar de project-URI.


### Code
In deze kolom staat de code ofwel het nummer van het onderwerp.
Deze code maakt het mogelijk in een gesprek naar het concept te verwijzen, zonder de volledige URI te hoeven benoemen. 


### Naam
In deze kolom staat de naam van het onderwerp.
De naam is de voor mensen leesbare naam van het onderwerp. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.


### Type
In deze kolom staat het type van het onderwerp:
1. FysiekObject  
2. Functie  
3. Werkzaamheid   
4. Informatieproduct



### Definitie
In deze kolom staat de definitie van het onderwerp. Hier staat ofwel een tekst die het onderwerp definieert, ofwel een URI die verwijst naar de definitie in een ontologie (objecttypenbibliotheek).



### heeftDeel
In deze kolom staat de URI van een onderliggend onderwerp.
Hiermee kan een hiërarchie worden aangegeven zoals een objectenboom of functieboom zoals gebruikelijk in contracten. Een concept kan uit meerdere delen bestaan, er komen dan meerdere regels voor in de Onderwerpentabel. 



### Eigenaar
In deze kolom wordt aangegeven wie de eigenaar is van het onderwerp.
Vooral bij objecttypen of individuele objecten is het voor de opdrachtgever handig, te weten wie de eigenaar is. De eigenaar is de persoon of rol bij de opdrachtgever die verantwoordelijk is voor beheer van dit objecttype, en die geconsulteerd moet worden bij afwijking van de eisen.


<p class="note">
De vertaling / binding van eigenaar naar NEN2660-2 is nog niet bekend. 
</p>

[Issue 16](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/16)


