# Onderwerpen

Het onderwerpenformat wordt gebruikt om de onderwerpen van de eisen te kunnen uitwisselen als data. Een onderwerp is een [=FysiekObject=], [=Werkzaamheid=],  [=Functie=] of [=Informatieproduct=]. 


## Onderwerpenformat
Het format wordt rijen getoond in plaats van in kolommen, om de leesbaarheid te bevorderen. Bij uitwisseling is de tabel horizontaal waarbij een of meerdere regels gebruikt kunnen worden per onderwerp. 

<table class="data">
<thead>
	<th>Kolomnaam
	<th>Definitie
	<th>Voorbeeld
</thead>
<tr>
	<td scope="row">  [=onderwerpURI=]
	<td class="def">In deze kolom staat de unieke naam (URI) van het onderwerp.
	<td class="example">`https://www.example.org/id/Voorbeeld-Object1`
</tr>
<tr>
	<td scope="row"> [=onderwerpCode=]
	<td class="def">In deze kolom staat de code ofwel het nummer van het onderwerp.
	<td class="example">OBJ-0109
</tr>
<tr>
	<td scope="row"> [=onderwerpNaam=]
	<td class="def">In deze kolom staat de naam van het onderwerp.
	<td class="example">Bushalte Ede-Zuid
</tr>
<tr>
	<td scope="row">  [=onderwerpTypeURI=]
	<td class="def">In deze kolom staat de URI type van het onderwerptype.
	<td class="example"> https://data.crow.nl/contractspecificaties/def/InformationProduct
</tr>
<tr>
	<td scope="row">  [=onderwerpTypeNaam=]
	<td class="def">In deze kolom staat de voor mensen leesbare naam van het onderwerptype: FysiekObject, Functie, Werkzaamheid of InformatieProduct.
	<td class="example"> InformationInformatieProductObject
</tr>
<tr>
	<td scope="row"> [=onderwerpDefinitie=]
	<td class="def"> In deze kolom staat de definitie van het onderwerp.
	<td class="example"> Onderwerp van een eis als voorbeeld in de documentatie
</tr>
<tr>
	<td scope="row"> [=onderwerpIsDeelVan=]
	<td class="def">In deze kolom staat de URI van een bovenliggend onderwerp.
	<td class="example">`https://www.example.org/id/Voorbeeld-Object2`
</tr>
</table>

## Details onderwerpentabel

### <dfn>onderwerpURI

De URI is de unieke identifier voor het onderwerp binnen het project ("Brug15"). Zie [URI conform W3C](https://www.w3.org/wiki/URI).

Als de URI uit een ontologie ("Een brug") direct als onderwerp wordt gebruikt, suggereer je daarmee dat de projecteis altijd geldt voor dit onderwerp; dat hoeft echter niet zo te zijn. Vandaar dat hier altijd een project-URI wordt gebruikt; in een project stel je de projecteisen aan de instaties van het onderwerp waarvan het type gedefinieerd is in je ontologie ("objecttypenbibliotheek"). Gezien de eenvoud van dit uitwisselformaat, is geen verwijzing naar een ontologie opgenomen.

Voor het opstellen van URI's heeft de [[NEN_2660_2_2022]] een URI-strategie die je MOET volgen.

| Taalbinding | Kardinaliteit | Datatype                                               |
|-------------|---------------|--------------------------------------------------------|
| n.v.t.      | 1:1           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

<aside class="note" title="LinkedData Proof">
Een URI maakt het meteen "linked data proof"
</aside>


### <dfn>onderwerpCode


De OnderwerpCode is een nummer van het onderwerp in spreektaal, vaak een voor mensen herkenbare code of projectnummer. Deze meestal eenvoudige en soms logisch genummerde Code maakt het mogelijk om in een gesprek naar het onderwerp te verwijzen, zonder de volledige URI te hoeven benoemen. Omdat deze code het onderwerp identificeert, MOET de code binnen het project uniek zijn.

| Taalbinding                                                                   | Kardinaliteit | Datatype                                               | Geadviseerd maximaal aantal tekens |
|-------------------------------------------------------------------------------|---------------|--------------------------------------------------------|------------------------------------|
| [skos:notation](https://www.w3.org/2009/08/skos-reference/skos.html#notation) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 255                                |
| { .def } |

### <dfn>onderwerpNaam

De OnderwerpNaam is de voor mensen leesbare naam van het onderwerp. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.

| Taalbinding                                                                     | Kardinaliteit | Datatype                                               | Geadviseerd maximaal aantal tekens |
|---------------------------------------------------------------------------------|---------------|--------------------------------------------------------|------------------------------------|
| [skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 255                                |
| { .def } |

### <dfn>onderwerpTypeURI

In deze kolom staat de URI type van het onderwerptype, zodat deze tabel geautomatiseerd verwerkt kan worden:

1. https://data.crow.nl/contractspecificaties/def/PhysicalObject
2. https://data.crow.nl/contractspecificaties/def/Function
3. https://data.crow.nl/contractspecificaties/def/Work
4. https://data.crow.nl/contractspecificaties/def/InformationProduct



### <dfn>onderwerpTypeNaam

Het type van het onderwerp kan in het format uit een van deze vier concepten bestaan:

1. [=FysiekObject=]
2. [=Functie=]
3. [=Werkzaamheid=]
4. [=InformatieProduct=]

Een Eis kan betrekking hebben op een Object (Galecopperbrug), maar ook op een Objecttype (brug, of alle bruggen <i>in dit project</i>); op een Functie (keren water Nederrijn bij Driel), of juist op een Functietype (Keren water in een rivier op een locatie) enz. Algemeen: eisen kunnen zowel betrekking op Type als op Individueel-niveau. In het project bedoel je altijd "de individuele Fysieke objecten van het type "weg" <i>in dit project</i>" als het onderwerp de naam "Weg" heeft; of als er maar een weg is is het beter de naam van het onderwerp specifieker te maken: "N224".


| Taalbinding                                              | Kardinaliteit | Datatype                                               |
|----------------------------------------------------------|---------------|--------------------------------------------------------|
| [rdfs:Class](https://www.w3.org/TR/rdf-schema/#ch_class) | 1:1           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

<dl>
<dt><dfn>FysiekObject
	<dd>De objecttypen en objecttypenboom ("decompositie") in het contract (Vraagspecificatie Eisen met eisen aan het Bouwwerk) zijn in NEN2660-2 een <a href="https://w3id.org/nen2660/def#PhysicalObject">nen2660:PhysicalObject</a>. Dit kan in de kolom Type worden ingevuld.
	
<dt><dfn data-lt="Functie|Functies">Functie</dfn>
	<dd>In de [[NEN_2660_1_2022]], par. 8.5.3, opmerking 2 wordt functie gedefinieerd als "De functie van een object is de activiteit die het (object) uitvoert of kan uitvoeren, zodanig dat de output van die activiteit bijdraagt aan het doel dat de betrokken stakeholder wil bereiken." De functies staan meestal in de Vraagspecificatie Eisen met eisen aan het Bouwwerk. Daarom maken wij een specifiekere klasse: <a href="https://data.crow.nl/contractspecificaties/def/Function">cs:Function</a>
	<dd>In de [[NEN_2660_2_2022]] is een functie, bijvoorbeeld "Afwikkelen wegverkeer" ZOWEL een <a href="https://w3id.org/nen2660/def#Activity">nen2660:Activity</a>  ALS een <a href="https://w3id.org/nen2660/def/#FunctionalEntity">nen2660:FuntionalEntity</a>.
	<dd>Ook mensen kunnen volgens de gegeven definitie in de [[NEN_2660_1_2022]] functies uitvoeren, zoals "De door mensen uit te voeren werkzaamheden tijdens het ontwerpen, bouwen, beheren en slopen van het object". In dit uitwisselformaat en in hedendaagse Vraagspecificaties (Vraagspecificatie Eisen met eisen aan het Bouwwerk) worden functies specifiek alleen meegegeven om aan te duiden, welke diensten het "systeem" moet vervullen tijdens het gebruik; een voorbeeld is een weg, die als functie "het verkeer moet geleiden". De objecten in het contract zijn de functievervullers. De werkzaamheden van mensen tijdens het project, waaronder die beschreven worden in Vraagspecificatie Procesdeel en de ontwerp- en uitvoeringswerkzaamheden, worden in dit uitwisselformaat <b>niet</b> beschreven als functies.

<dt><dfn data-lt="Werkzaamheid|Werkzaamheden">Werkzaamheid</dfn>
	<dd>De werkzaamheden zijn door mensen uit te voeren activiteiten tijdens het ontwerpen, bouwen, beheren en slopen van het object, met name die werkzaamheden die in een contract in de Vraagspecificatie Procesdeel staan. 
	<dd>In de [[NEN_2660_2_2022]] bestaat een <a href="https://w3id.org/nen2660/def#Activity">nen2660:Activity</a>. Wij maken die specifieker naar <a href="https://data.crow.nl/contractspecificaties/def/Worky">cs:Work</a>

<dt><dfn data-lt="InformatieProduct|InformatieProducten">InformatieProduct</dfn>
	<dd>De informatieproducten in het contract staan vaak zowel in de Vraagspecificatie Procesdeel als in een separate Informatieleveringsspecificatie. Het betreft de gevraagde levering van 'documenten', dit kunnen alle bestandstypes zijn, ook datasets of geometrische bestanden. In de NEN2660 is een InformationObject onderscheiden. Binnen contractspecificaties maken wij een specifieke klasse <a href="https://data.crow.nl/contractspecificaties/def/InformationProduct">cs:InformationProduct</a>.Voorbeelden:<ul>
<li>Informatieleveringsspecificatie:</li><ul>
<li>Een rapport over het ontwerp van een weg</li>
<li>Een sterkteberekening van een kunstwerk</li>
<li>Een 3D model van een gebouw</li>
<li>Een linked dataset met attributen van een voetpad</li></ul>
<li>Procesdeel:</li><ul>
<li>Een V&G plan</li>
<li>Een voortgangsrapportage</li></ul></ul>
</dl>

### <dfn>onderwerpDefinitie

De definitie van het onderwerp is een vrij tekstveld die het onderwerp definieert.

| Taalbinding                                                                      | Kardinaliteit | Datatype                                               | Geadviseerd maximaal aantal tekens |
|----------------------------------------------------------------------------------|---------------|--------------------------------------------------------|------------------------------------|
| [skos:definition](https://www.w3.org/2009/08/skos-reference/skos.html#defintion) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 2000                               |
| { .def } |

### <dfn>onderwerpIsDeelVan

In deze kolom staat de URI van een bovenliggend onderwerp.
Hiermee kan een hiërarchie worden aangegeven zoals een objectenboom of functieboom zoals gebruikelijk in contracten. Een concept kan uit meerdere delen bestaan, er komen dan meerdere regels voor in de Onderwerpentabel.
De inverse van de `nen2660:hasPart` relatie wordt hier gebruikt: `nen2660:isPartOf`. Deze relatie kan dan transitief gelezen worden.

| Taalbinding                                                        | Kardinaliteit | Datatype                                               |
|--------------------------------------------------------------------|---------------|--------------------------------------------------------|
| [nen2660:hasPart](https://nl-digigo.github.io/nen2660/def#hasPart) | 0:n           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

<p class="note">
Net als bij de eisen, is de "eigenaar" van het onderwerp vaak een interne rolhouder. In het contract gelden hiervoor de projectafspraken en kan de eigenaar vertegenwoordigd zijn door een andere rolhouder. Een eigenaar kan intern bijvoorbeeld de objectbeheerder zijn, maar in het contract is de technisch manager eerste aanspreekpunt voor het object. Meestal wordt de eigenaar niet benoemd in de vraagspecificaties. Daarom is "eigenaarschap" niet opgenomen in de onderwerpentabel.
</p>
