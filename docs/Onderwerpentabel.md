# Onderwerpen

De onderwerpentabel wordt gebruikt voor de onderwerpen van de eisen, bestaande uit de functies, objecttypen, werkzaamheden en informatieproducten. Op de eerste regel staan de kolomnamen. Op de tweede regel staat een korte toelichting; op de derde regel de vertaling / binding naar de NEN2660-2 en andere standaarden. Op de vierde regel staat aangegeven, hoeveel relaties er kunnen voorkomen in dit veld (multipliciteit). Als er meer dan één relatie voorkomt, komen er regels bij in de uitwisseling.

## Onderwerpenformat

<table class="data">
<thead>
	<th> [=OnderwerpURI=]
	<th> [=OnderwerpCode=]
	<th> [=OnderwerpNaam=]
	<th> [=OnderwerpType=]
	<th> [=OnderwerpDefinitie=]
	<th> [=OnderwerpheeftDeel=]
</thead>
<tr class="def">
	<td> In deze kolom staat de unieke naam (URI) van het onderwerp.
	<td> In deze kolom staat de code ofwel het nummer van het onderwerp.
	<td> In deze kolom staat de naam van het onderwerp.
	<td> In deze kolom staat het type van het onderwerp: Objecttype, Functie, Werkzaamheid of Informatieproduct.
	<td> In deze kolom staat de definitie van het onderwerp.
	<td> In deze kolom staat de URI van een onderliggend onderwerp.
</tr>
<tr class="example">
	<td> `https://www.example.org/id/Voorbeeld-Object1`
	<td> OBJ-0109
	<td> Voorbeeld onderwerp
	<td> InformationObject
	<td> Onderwerp van een eis als voorbeeld in de documentatie
	<td> `https://www.example.org/id/Voorbeeld-Object2`
</tr>
</table>

## Details onderwerpentabel

### <dfn>OnderwerpURI

De URI is de unieke identifier voor het onderwerp binnen het project ("Brug15"). Zie [URI conform W3C](https://www.w3.org/wiki/URI).

Als de URI uit een ontologie ("Een brug") direct als onderwerp wordt gebruikt, suggereer je daarmee dat de projecteis altijd geldt voor dit onderwerp; dat hoeft echter niet zo te zijn. Vandaar dat hier altijd een project-URI wordt gebruikt; in een project stel je de projecteisen aan de instaties van het onderwerp waarvan het type gedefinieerd is in je ontologie ("objecttypenbibliotheek"). Gezien de eenvoud van dit uitwisselformaat, is geen verwijzing naar een ontologie opgenomen.

[URI](https://www.w3.org/wiki/URI); Voor het opstellen van URI's heeft de NEN 2660-2 een URI-strategie die je moet volgen.

| Taalbinding | Kardinaliteit | Datatype                                               |
| ----------- | ------------- | ------------------------------------------------------ |
| n.v.t.      | 1:1           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

> Een URI maakt het meteen "linked data proof"

### <dfn>OnderwerpCode

De OnderwerpCode is een nummer van het onderwerp in spreektaal, vaak een voor mensen herkenbare code of projectnummer. Deze meestal eenvoudige en soms logisch genummerde Code maakt het mogelijk om in een gesprek naar het onderwerp te verwijzen, zonder de volledige URI te hoeven benoemen.

| Taalbinding                                                                   | Kardinaliteit | Datatype                                               |
| ----------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [skos:notation](https://www.w3.org/2009/08/skos-reference/skos.html#notation) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def } |

### <dfn>OnderwerpNaam

De OnderwerpNaam is de voor mensen leesbare naam van het onderwerp. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.

| Taalbinding                                                                     | Kardinaliteit | Datatype                                               |
| ------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def } |

### <dfn>OnderwerpType

Dit is een enumeratie. Het type van het onderwerp kan in het format uit een van deze vier concepten bestaan:

1. [=FysiekObject=]
2. [=Functie=]
3. [=Werkzaamheid=]
4. [=Informatieproduct=]

| Taalbinding                                              | Kardinaliteit | Datatype                                               |
| -------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [rdfs:Class](https://www.w3.org/TR/rdf-schema/#ch_class) | 1:1           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

<dl>
<dt><dfn>FysiekObject
	<dd>De objecttypen en objecttypenboom ("decompositie") in het contract (Vraagspecificatie Eisendeel) zijn in NEN2660-2 een <a href="https://w3id.org/nen2660/def#PhysicalObject">nen2660:PhysicalObject</a>. Dit kan in de kolom Type worden ingevuld.
	
<dt><dfn>Functie
	<dd>De functies in het contract (Vraagspecificatie Eisendeel) zijn ánders dan de werkzaamheden (Vraagspecificatie Procesdeel / ontwerp- en uitvoeringswerkzaamheden). De functies geven weer, welke diensten het "systeem" moet vervullen tijdens het gebruik; een voorbeeld is een weg, die als functie "het verkeer moet geleiden". De objecten in het contract zijn de functievervullers. De activiteiten zijn door mensen uit te voeren werkzaamheden tijdens het ontwerpen, bouwen, beheren en slopen van het object. In de NEN-2660 is een functie, bijvoorbeeld "Afwikkelen wegverkeer" ZOWEL een <a href="https://w3id.org/nen2660/def#Activity">nen2660:Activity</a>  ALS een <a href="https://w3id.org/nen2660/def/#FunctionalEntity">nen2660:FuntionalEntity</a>.

<dt><dfn>Werkzaamheid
	<dd>De werkzaamheden zijn door mensen uit te voeren activiteiten tijdens het ontwerpen, bouwen, beheren en slopen van het object. In de NEN2660 is een werkzaamheid, zoals "Opstellen Maandrapportage" een <a href="https://w3id.org/nen2660/def#Activity">nen2660:Activity</a>.

<dt><dfn>Informatieproduct
	<dd>De informatieproducten in het contract staan vaak zowel in de Vraagspecificatie Procesdeel als in een separate Informatieleveringsspecificatie. Het betreft de gevraagde levering van 'documenten', dit kunnen alle bestandstypes zijn, ook datasets of geometrische bestanden. In de NEN2660 is een InformationObject onderscheiden. Binnen contractspecificaties wordt deze gespecialiseerd naar een <a href="https://data.crow.nl/contractspecificaties/def/Document">cs:Document</a>.Voorbeelden:<ul>
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

De definitie van het onderwerp is een vrij tekstveld die het onderwerp definieert.

| Taalbinding                                                                      | Kardinaliteit | Datatype                                               |
| -------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [skos:definition](https://www.w3.org/2009/08/skos-reference/skos.html#defintion) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def } |

### <dfn>OnderwerpheeftDeel

In deze kolom staat de URI van een onderliggend onderwerp.
Hiermee kan een hiërarchie worden aangegeven zoals een objectenboom of functieboom zoals gebruikelijk in contracten. Een concept kan uit meerdere delen bestaan, er komen dan meerdere regels voor in de Onderwerpentabel.

| Taalbinding                                                        | Kardinaliteit | Datatype                                               |
| ------------------------------------------------------------------ | ------------- | ------------------------------------------------------ |
| [nen2660:hasPart](https://bimloket.github.io/nen2660/term#hasPart) | 0:n           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

<p class="note">
Net als bij de eisen, is de "eigenaar" van het onderwerp vaak een interne rolhouder. In het contract gelden hiervoor de projectafspraken en kan de eigenaar vertegenwoordigd zijn door een andere rolhouder. Een eigenaar kan intern bijvoorbeeld de objectbeheerder zijn, maar in het contract is de technisch manager eerste aanspreekpunt voor het object. Meestal wordt de eigenaar niet benoemd in de vraagspecificaties. Daarom is "eigenaarschap" niet opgenomen in de onderwerpentabel.
</p>
