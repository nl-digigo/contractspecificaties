# Onderwerpen

De onderwerpentabel wordt gebruikt voor de onderwerpen van de eisen, bestaande uit de functies, objecttypen, werkzaamheden en informatieproducten. Op de eerste regel staan de kolomnamen. Op de tweede regel staat een korte toelichting; op de derde regel de vertaling / binding naar de NEN2660-2 en andere standaarden. Op de vierde regel staat aangegeven, hoeveel relaties er kunnen voorkomen in dit veld (multipliciteit). Als er meer dan één relatie voorkomt, komen er regels bij in de uitwisseling. 

<p class="note">
De vertaling / binding van Eigenaren naar NEN2660-2 is nog niet bekend. Mogelijk wordt hier de DCTerms ontologie betrokken.
</p>

## Onderwerpenformat

<table class="wikitable" style="text-align:left; valign:top">
<tr>
<th> [=OnderwerpURI=]
</th>
<th> [=OnderwerpCode=]
</th>
<th> [=OnderwerpNaam=]
</th>
<th> [=OnderwerpType=]
</th>
<th> [=OnderwerpDefinitie=]
</th>
<th> [=Onderwerp.heeftDeel=]
</th>
</tr>
<tr>
<td> In deze kolom staat de unieke naam (URI) van het onderwerp. </td>
<td> In deze kolom staat de code ofwel het nummer van het onderwerp. </td>
<td> In deze kolom staat de naam van het onderwerp. </td>
<td> In deze kolom staat het type van het onderwerp: Objecttype, Functie, Werkzaamheid of Informatieproduct. </td>
<td> In deze kolom staat de definitie van het onderwerp. </td>
<td> In deze kolom staat de URI van een onderliggend onderwerp. </td>
</tr>
<tr>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldtabel </td>
<td> OBJ-0109 </td>
<td> Voorbeeld onderwerp </td>
<td> InformationObject </td>
<td> Onderwerp van een eis als voorbeeld in de documentatie </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#onderligeendvoorbeeldobject </td></tr>
</table>

## Details onderwerpentabel

### <dfn>OnderwerpURI 
De URI is de unieke identifier voor het onderwerp binnen het project ("Brug15"). Zie [URI conform W3C](https://www.w3.org/wiki/URI). 

Bij de definitie kan worden verwezen naar het type onderwerp uit een ontologie ofwel objecttypenbibliotheek ("Een brug"). 
Als de URI uit een ontologie direct als onderwerp wordt gebruikt, suggereer je daarmee dat de projecteis altijd geldt voor dit onderwerp; dat hoeft echter niet zo te zijn. Vandaar de project-URI.

[URI](https://www.w3.org/wiki/URI)

Cardinaliteit: 1:1

> Een URI maakt het meteen "linked data proof"

### <dfn>OnderwerpCode
De OnderwerpCode is een nummer van het onderwerp in spreektaal, vaak een voor mensen herkenbare code of projectnummer. Deze meestal eenvoudige en soms logisch genummerde Code maakt het mogelijk om in een gesprek naar het onderwerp te verwijzen, zonder de volledige URI te hoeven benoemen.

[skos:notation](https://www.w3.org/2009/08/skos-reference/skos.html#notation)

Cardinaliteit: 1:1

### <dfn>OnderwerpNaam
De OnderwerpNaam is de voor mensen leesbare naam van het onderwerp. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.

[skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel)

Cardinaliteit: 1:1

### Enum <dfn>OnderwerpType
Het type van het onderwerp kan in het format uit een van deze vier concepten bestaan:
1. [=FysiekObject=]  
2. [=Functie=] 
3. [=Werkzaamheid=]   
4. [=Informatieproduct=]

[rdfs:Class](https://www.w3.org/TR/rdf-schema/#ch_class)

Cardinaliteit: 0:n

<dl>
<dt><dfn>FysiekObject
	<dd>De objecttypen en objecttypenboom ("decompositie") in het contract (Vraagspecificatie Eisendeel) zijn “FysiekObject” uit NEN2660-2. Dit kan in de kolom Type worden ingevuld.
	
<dt><dfn>Functie
	<dd>De functies in het contract (Vraagspecificatie Eisendeel) zijn ánders dan de werkzaamheden (Vraagspecificatie Procesdeel / ontwerp- en uitvoeringswerkzaamheden). De functies geven weer, welke diensten het "systeem" moet vervullen tijdens het gebruik; een voorbeeld is een weg, die als functie "het verkeer moet geleiden". De objecten in het contract zijn de functievervullers. De activiteiten zijn door mensen uit te voeren werkzaamheden tijdens het ontwerpen, bouwen, beheren en slopen van het object.

<dt><dfn>Werkzaamheid
	<dd>De werkzaamheden zijn door mensen uit te voeren activiteiten tijdens het ontwerpen, bouwen, beheren en slopen van het object. 

<dt><dfn>Informatieproduct
	<dd>De informatieproducten in het contract staan vaak zowel in de Vraagspecificatie Procesdeel als in een separate Informatieleveringsspecificatie. Het betreft de gevraagde levering van 'documenten', dit kunnen alle bestandstypes zijn, ook datasets of geometrische bestanden. Voorbeelden:<ul>
<li>Informatieleveringsspecificatie:</li><ul>
<li>Een rapport over het ontwerp van een weg</li>
<li>Een sterkteberekening van een kunstwerk</li>
<li>Een 3D model van een gebouw</li>
<li>Een linked dataset met attributen van een voetpad</li></ul>
<li>Procesdeel:</li><ul>
<li>Een V&G plan</li>
<li>Een voortgangsrapportage</li></ul></ul>
</dl>

### <dfn>OnderwerpDefinitie
De definitie van het onderwerp is ofweleen tekst die het onderwerp definieert, ofwel een URI die verwijst naar de definitie in een ontologie (objecttypenbibliotheek).

[skos:definition](https://www.w3.org/2009/08/skos-reference/skos.html#definition)


### <dfn>Onderwerp.heeftDeel
In deze kolom staat de URI van een onderliggend onderwerp.
Hiermee kan een hiërarchie worden aangegeven zoals een objectenboom of functieboom zoals gebruikelijk in contracten. Een concept kan uit meerdere delen bestaan, er komen dan meerdere regels voor in de Onderwerpentabel. 

[nen2660:hasPart](https://bimloket.github.io/nen2660/term#hasPart)

Cardinaliteit: 0:n


<p class="note">
Net als bij de eisen, is de "eigenaar" van het onderwerp vaak een interne rolhouder. In het contract gelden hiervoor de projectafspraken en kan de eigenaar vertegenwoordigd zijn door een andere rolhouder. Een eigenaar kan intern bijvoorbeeld de objectbeheerder zijn, maar in het contract is de technisch manager eerste aanspreekpunt voor het object. Meestal wordt de eigenaar niet benoemd in de vraagspecificaties. Daarom is "eigenaarschap" niet opgenomen in de onderwerpentabel.
</p>



