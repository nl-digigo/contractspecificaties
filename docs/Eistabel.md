# Eisen

Het eisenformat wordt gebruikt om de eisen te kunnen uitwisselen als data. 

Een eis is een [NEN2660:Requirement](https://bimloket.github.io/nen2660/def#Requirement) volgens NEN 2660.

## Eisenformat

Het format wordt rijen getoond in plaats van in kolommen, om de leesbaarheid te bevorderen. Bij uitwisseling is de tabel horizontaal waarbij een of meerdere regels gebruikt kunnen worden per eis. 



<table class="data">
<thead>
	<th>Kolomnaam
	<th>Definitie
	<th>Voorbeeld
</thead>
<tr>
	<td scope="row"> [=eisURI=]
	<td class="def">In deze kolom staat de unieke identifier (URI) van de eis.
	<td class="example">`https://www.example.org/id/Voorbeeld-Eis1`
</tr>
<tr>
	<td scope="row"> [=eisCode=]
	<td class="def">In deze kolom staat de code of het nummer van de eis.
    <td class="example">EIS1099
</tr>
	<td scope="row"> [=eisTitel=]
	<td class="def">In deze kolom staat de de naam oftewel de titel van de eis.
	<td class="example">Voorbeeldeis
</tr>
	<td scope="row"> [=eisTekst=]
	<td class="def">In deze kolom staat de eistekst.
	<td class="example">Dit is de tekst van de voorbeeldeis
</tr>
<tr>	
	<td scope="row"> [=eisToelichting=]
	<td class="def">In deze kolom staat de toelichting op de eis.
	<td class="example">Dit is de toelichting van de voorbeeldeis, om achtergrond / doel en reden van de eis te kunnen verduidelijken
</tr>
<tr>
	<td scope="row"> [=eisHeeftDeel=]
	<td class="def">In deze kolom staat de URI van een onderliggende eis. 
	<td class="example"> `https://www.example.org/id/Voorbeeld-Eis2`
</tr>
<tr>
	<td scope="row"> [=eisBron=]
	<td class="def"> In deze kolom staat de URI van een bron van de eis in een eisenbibliotheek of brondocument. 
	<td class="example"> `https://www.example.org/id/Voorbeeld-Document1`
</tr>
<tr>
	<td scope="row"> [=documentNaam=]
	<td class="def"> In deze kolom staat de DocumentNaam van een bron van de eis in een eisenbibliotheek of brondocument. 
	<td class="example"> Omgevingsvisie Ede
</tr>
<tr>
	<td scope="row"> [=eisReferentiedocument=]
	<td class="def"> In deze kolom staat de URI van een gerefereerd document waarin aanvullende eisen staan 
	<td class="example"> `https://www.example.org/id/Voorbeeld-Document2`
</tr>
<tr>
	<td scope="row"> [=documentNaam=]
	<td class="def"> In deze kolom staat de documentnaam van een gerefereerd document waarin aanvullende eisen staan 
	<td class="example"> Handboek Wegontwerp
</tr>
<tr>
	<td scope="row"> [=eisType=]
	<td class="def"> In deze kolom staat het eistype. 
	<td class="example"> `https://data.crow.nl/contractspecificaties/id/Proceseis` 
</tr>
<tr>
	<td scope="row"> [=eisStatus=]
	<td class="def">  In deze kolom staat de status van de eis. 
	<td class="example">  `https://data.crow.nl/contractspecificaties/id/Vervallen` 
</tr>
<tr>
	<td scope="row"> [=eisStatusOnderbouwing=]
	<td class="def"> In deze kolom staat een toelichting op de status van de eis. 
	<td class="example"> Komt niet meer voor want ... 
</tr>
<tr>
	<td scope="row"> [=verificatievoorschriftURI=]
	<td class="def"> In deze kolom staat de URI van een Verificatievoorschrift.
	<td class="example">`https://www.example.org/id/Voorbeeld-Verificatievoorschrift1`
</tr>
<tr>
	<td scope="row"> [=verificatieHeeftOnderwerp=]
	<td class="def">In deze kolom staat de URI van het Onderwerp (subject) van het Verificatievoorschrift.
	<td class="example"> `https://www.example.org/id/Voorbeeld-Onderwerp1`
</tr>
<tr>
	<td scope="row"> [=onderwerpNaam=]
	<td class="def">In deze kolom staat de naam van het Onderwerp (subject) van het Verificatievoorschrift.
	<td class="example"> Bushalte Ede-Zuid
</tr>
<tr>
	<td scope="row"> [=verificatieMethode=]
	<td class="def">In deze kolom staat de verificatiemethode van het Verificatievoorschrift.
	<td class="example">`https://data.crow.nl/contractspecificaties/id/Keuring`
</tr>
<tr>
	<td scope="row"> [=verificatieFase=]
	<td class="def">In deze kolom staat de fase waarin dit Verificatievoorschrift wordt uitgevoerd.
	<td class="example">`https://data.crow.nl/contractspecificaties/id/Aanleg`
</tr>
<tr>
	<td scope="row"> [=verificatieMoment=]
	<td class="def">In deze kolom staat het moment waarop dit Verificatievoorschrift moet zijn uitgevoerd.
	<td class="example">Twee weken voor het begin van de Gebruiksfase
</tr>
<tr>
	<td scope="row"> [=verificatievoorschriftToelichting=]
	<td class="def">In deze kolom staat de toelichting op de verificatiemethode bij de eis.
	<td class="example">Een toelichting waarom een verificatiemethode wordt gevraagd bij de eis, of nadere invulling van de verificatiemethode
</tr>
</table>


## Details

### <dfn>eisURI

De <abbr title="uniform resource identifier">URI</abbr> is de unieke identifier voor de eis binnen het project. Zie [URI volgens W3C](https://www.w3.org/wiki/URI).

Voor het opstellen van URI's heeft de [[NEN_2660_2_2022]] een URI-strategie die je moet volgen.

Bij de eisen kan verwezen worden naar een eis in een eisenbibliotheek onder [=EisBron=]. Daar staat de URI van de eis uit de bibliotheek. Deze URI verwijst naar een openbaar gepubliceerde eis in een bibliotheek, bijvoorbeeld het Provinciaal Contracten Buffet.

De eis in het project moet een andere URI hebben dan de bron. 

<aside class="note" title="Unieke indentificatie van concepten in projecten">
Unieke indentificatie van concepten in projecten is van belang, omdat in het Digitaal Stelsel Gebouwde Omgeving toegewerkt wordt naar interoperabiliteit van data. Als je in een project dezelfde URI's gebruikt als in de bibliotheek, ga je in tegen de basisprincipes die hiervoor nodig zijn: een eis in een bibliotheek is niet dezelfde eis als de eis met dezelfde tekst in een project, want deze wordt toegepast in (gekopieerd naar) een andere context. Ook kan n de bilbiotheek een verificatievoorschrift bij de eis zijn opgenomen, die in het project niet wordt opgenomen omdat er meer vrijheid wordt gegeven aan de opdrachtnemer. Als dezelfde URI wordt gebruikt, kan hierover verwarring ontstaan.

De herkenbaarheid van de eis voor de menselijke lezer kan wel in stand gehouden worden doordat je wel dezelfde [=EisCode=] kan gebruiken als in de bibliotheek.
</aside>


| Taalbinding | Kardinaliteit | Datatype                                               |
| ----------- | ------------- | ------------------------------------------------------ |
| n.v.t.      | 1:1           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

<aside class="note" title="LinkedData Proof">
Een URI maakt het meteen "linked data proof"
</aside>


### <dfn>eisCode

De EisCode is een <i>in het contract opgenomen</i> nummer van de eis in spreektaal, vaak een voor mensen herkenbare code of projectnummer. Deze meestal eenvoudige en soms logisch genummerde Code maakt het mogelijk om in een gesprek over het contract naar de eis te verwijzen, zonder de volledige URI te hoeven benoemen. Omdat deze code de eis identificeert, moet de code binnen het project uniek zijn.

| Taalbinding                                                                   | Kardinaliteit | Datatype                                               |  Geadviseerd maximaal aantal tekens                                               |
| ----------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [skos:notation](https://www.w3.org/2009/08/skos-reference/skos.html#notation) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 56 |
| { .def } |

<aside class="note" title="Codes">
Bij alle codes is het zo dat iedere ketenpartner een eigen code kan hangen aan de item (eis, document, stakeholder, etc.). Aannemer, opdrachtgever, ingenieursbureau, eisenbibliotheek kunnen allemaal eigen codes toevoegen aan een eis. Omdat dit het uitwisselformaat betreft voor het contract, wordt ervan uitgegaan dat er maar één code uitgewisseld kan worden per eis. 
</aside>

### <dfn>eisTitel

De EisTitel wordt ook wel eens de titel van de eis genoemd, en geeft een voor mensen leesbare korte duiding van de inhoud van de eis.

De EisTitel hoeft niet uniek te zijn in het project, daarvoor heeft de eis een URI. Een unieke naam is voor de menselijke lezer vaak wel handig. Soms wordt de EisTitel in applicaties bijvoorbeeld gebruikt bij het visualiseren van de eisenboom. Unieke namen helpen in dat geval.

| Taalbinding                                                                     | Kardinaliteit | Datatype                                               |  Geadviseerd maximaal aantal tekens                                               |
| ------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 56 |
| { .def } |

### <dfn>eisTekst

De EisTekst bevat de voor mensen leesbare inhoud van de eis.
Op dit moment worden eisen in een contract meestal niet voorzien van een voor een systeem leesbare eis, zoals bijvoorbeeld een minimale waarde voor een attribuut van een object. Deze "dataficeringsslag" is buiten scope van dit document, omdat dit een verder gevorderd BIM niveau vraagt en dit document juist bedoelt is als opstap naar uitwisseling van data.

In de EisTekst kan verwezen worden naar een referentiedocument, waar aanvullende eisen in staan die gelden binnen het contract. De URI van dit document wordt dan opgenomen in de kolom Referentiedocument.

| Taalbinding                                                   | Kardinaliteit | Datatype                                               |  Geadviseerd maximaal aantal tekens                                               |
| ------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [rdf:value](http://www.w3.org/1999/02/22-rdf-syntax-ns#value) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 2000  |
| { .def } |

### <dfn>eisToelichting

In deze kolom staat de toelichting op de eistekst

In contracten wordt dit gebruikt om nader te onderbouwen waarom deze eis gesteld wordt.

| Taalbinding                                                           | Kardinaliteit | Datatype                                               |  Geadviseerd maximaal aantal tekens                                               |
| --------------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [skos:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 2000  |
| { .def } |


### <dfn>eisHeeftDeel

In deze kolom staat de URI van een onderliggende eis.

Hiermee kan een hiërarchie worden aangegeven van de eisenboom zoals gebruikelijk in contracten. Een eis kan meerdere onderliggende eisen hebben, er komen dan meerdere regels met dezelfde eis voor in de eisentabel.

| Taalbinding                                                        | Kardinaliteit | Datatype                                               |
| ------------------------------------------------------------------ | ------------- | ------------------------------------------------------ |
| [nen2660:hasPart](https://bimloket.github.io/nen2660/term#hasPart) | 0:n           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

### <dfn>eisBron

De bron van de eis kan naar twee zaken verwijzen:

1. De URI van de gebruikte eis uit een bibliotheek (indien deze niet gewijzigd is). Deze URI verwijst naar een openbaar gepubliceerde eis in een bibliotheek, bijvoorbeeld het Provinciaal Contracten Buffet. De eis in het project moet een andere URI hebben dan de bron. Het is niet dezelfde eis, want deze wordt toegepast in (gekopieerd naar) een andere context.
2. De URI van een brondocument met herkomst van de eis. Deze URI verwijst naar een document in de documententabel.

| Taalbinding                                   | Kardinaliteit | Datatype                                               |
| --------------------------------------------- | ------------- | ------------------------------------------------------ |
| [dct:source](http://purl.org/dc/terms/source) | 0:n           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

### documentNaam
Dubbeling met de [=documentNaam=] in de Documententabel, om de tabel meer leesbaar te maken voor de menselijke lezer. Naam van het brondocument.

### <dfn>eisReferentiedocument

Als in de eistekst wordt verwezen naar een referentiedocument, staat in deze kolom de URI van het gerefereerde document. Deze URI verwijst naar een document in de documententabel.

Een referentiedocument is een document waarin extra eisen staan die in het contract gelden, die de opdrachtnemer zelf uit het document moet afleiden. Voorbeelden:

* De eis verwijst naar een ontwerp of berekening die van toepassing is.
* De eis verwijst naar een richtlijn, handleiding of norm die van toepassing is.
* De eis verwijst naar een figuur die van toepassing is.

Instructie voor gebruik: omdat nog niet alle partijen in staat zijn om de data helemaal te verwerken, moet je het document wel in de eistekst noemen. De eistekst is leidend. Een ontvanger van de eisenset kan er ook niet van uit gaan, dat de opdrachtgever dit altijd in weet te vullen. Als in een eistekst naar een referentiedocument wordt verwezen, kan het zijn dat er geen relatie is gemaakt naar het referentiedocument.


| Taalbinding                                           | Kardinaliteit | Datatype                                               |
| ----------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [dct:references](http://purl.org/dc/terms/references) | 0:n           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

### documentNaam
Dubbeling met de [=documentNaam=] in de Documententabel, om de tabel meer leesbaar te maken voor de menselijke lezer. Naam van het gerefereerde document.

### <dfn>eisType

In deze kolom staat het eistype. Welke eistypen gebruikt worden, wordt nog niet gestandaardiseerd; hierover bestaat helaas nog te weinig consensus in de sector.

| Taalbinding                                                                       | Kardinaliteit | Datatype                                                             |  Geadviseerd maximaal aantal tekens  |
| --------------------------------------------------------------------------------- | ------------- | -------------------------------------------------------------------- | ------------ |
| nen2660:requirementTopicType | 0:n           | string |   255   |
| { .def } |

### Enum <dfn>eisStatus

In deze kolom staat de status van de eis. Dit is een enumeratie. Voor contractspecificaties geldt dat de status één van deze twee zaken is: actueel of vervallen.
Doel is om wijzigingen door een Nota van Inlichtingen of een contractuele wijziging in de eisenset te kunnen opnemen en met elkaar uit te wisselen.

<dl>
<dt><dfn>Actueel
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Actueel">csw:Actueel</a>
<dt><dfn>Vervallen
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Vervallen">csw:Vervallen</a>
<dt><dfn>Concept
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Concept">csw:Concept</a>
</dl>

| Taalbinding                                                        | Kardinaliteit | Datatype                                                                   |
| ------------------------------------------------------------------ | ------------- | -------------------------------------------------------------------------- |
| [cs:status](https://data.crow.nl/contractspecificaties/def/status) | 1:1           | [cs:StatusType](https://data.crow.nl/contractspecificaties/def/StatusType) |
| { .def } |

### <dfn>eisStatusOnderbouwing

In deze kolom staat een toelichting op de status van de eis.
Gebruikers willen de reden van vervallen toevoegen aan de eis, zodat de status onderbouwd is.

| Taalbinding                                                                                | Kardinaliteit | Datatype                                               |  Geadviseerd maximaal aantal tekens  |
| ------------------------------------------------------------------------------------------ | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [cs:statusOnderbouwing](https://data.crow.nl/contractspecificaties/def/statusOnderbouwing) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 2000 |
| { .def } |


### <dfn>verificatievoorschriftURI

De URI is de unieke identifier voor het Verificatievoorschrift in deze fase, in dit project. Zie [URI conform W3C](https://www.w3.org/wiki/URI).
Voor het opstellen van URI's heeft de [[NEN_2660_2_2022]] een URI-strategie die je moet volgen.


Het Verificatievoorschrift geeft de <i>in het contract voorgeschreven</i> verificatiemethode voor de eis (een type uit een lijst plus een vrij tekstveld met toelichting), per object en per fase waarin de verificatie wordt uitgevoerd.  

Een eis kan meerdere Verificatievoorschriften kennen, elk in een eigen fase. Een Verificatievoorschrift geldt voor één fase. Indien in een andere fase precies dezelfde verificatie wordt uitgevoerd, zijn er twee Verificatievoorschriften.  

| Taalbinding | Kardinaliteit | Datatype                                               |
| ----------- | ------------- | ------------------------------------------------------ |
| n.v.t.      | 1:1 ten opzichte van een Verificatievoorschrift       | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |


### <dfn>verificatieHeeftOnderwerp

In deze kolom staat de URI van het Onderwerp van het Verificatievoorschrift. Een eis kan aan meerdere Onderwerpen gesteld worden, er komen dan meerdere regels met dezelfde eis voor in de eisentabel met elk een eigen Verificatievoorschrift en een eigen onderwerp.

Merk op, dat verwijzing naar de URI de tabel minder makkelijk leesbaar maakt voor de mens. Indien hier ook de naam van het concept zou worden toegevoegd, creëert dit dubbelingen met de onderwerpentabel en daarom mogelijk fouten. Daarom wordt alleen de URI gebruikt.

| Taalbinding                                                                            | Kardinaliteit | Datatype                                               |
| -------------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [cs:isVerificationOf](https://data.crow.nl/contractspecificaties/def/isVerificationOf) | 1:1 tov een Verificatievoorschrift          | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| [cs:hasAsSubject ](https://data.crow.nl/contractspecificaties/def/hasAsSubject)        | 1:1 tov een Verificatievoorschrift          | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

<aside class="note" title="Onderwerp van Eis en Verificatievoorschrift">
Merk op, dat in de tabel een relatie niet benoemd is, omdat de "regel" de verbindende factor is: <a href="https://data.crow.nl/contractspecificaties/def/hasAsSubject">cs:hasAsSubject</a>
Dit is het onderwerp van het Verificatievoorschrift. In de [[NEN_2660_2_2022]] zijn er twee manieren om een eis te verbinden met een onderwerp: <ol>
<li>Rechtstreeks via de relatie: hasRequirement</li>
<li>Indirect via de relaties: isVerificationOf en hasAsSubject</li>
Deze laatste heeft de voorkeur binnen Contractspecificaties, omdat er meer informatie kan worden vastgelgd over het Verificatievoorschrift. 
<figure>
<img src="./media/Diagram2.drawio.svg" alt="UML schema voor het informatiemodel voor het Verificatievoorschrift">
<figcaption>Het informatiemodel voor het Verificatievoorschrift.  hoort het Onderwerp bij het Verificatievoorschrift en heeft geen directe relatie met de eis.</caption>
</figure>
</aside>

### OnderwerpNaam
Dubbeling met de [=Onderwerpnaam=] in de Onderwerpentabel, om de tabel meer leesbaar te maken voor de menselijke lezer. Naam van het onderwerp.

### Enum <dfn>verificatieMethode

In deze kolom staat de verificatiemethode waarmee de eis geverifieerd moet worden. Een verificatiemethode is een eigenschap van een verificatievoorschrift. De verificatiemethode is een enumeratie, dat wil zeggen dat de gebruiker moet kiezen uit een lijst met van te voren vastgestelde verificatiemethoden. Het is niet verplicht om een verificatiemethode voor te schrijven bij een Verificatievoorschrift, je kunt dit ook aan de opdrachtnemer laten.

Bij uitwisseling mag uitsluitend de onderstaande lijst gebruikt worden bij contractspecificaties, zonder zelf uitbreidingen te doen. Als elke opdrachtgever een eigen lijst gebruikt wordt het inrichten van standaard omgevingen voor de verwerking van contracteisen onnodig bemoeilijkt, waarbij door opdrachtnemers bij elk project een aangepaste lijst moet maken. 

De verificatiemethoden zijn afgeleid uit de volgende standaarden:

1. [[NEN_EN_ISO_9000_2015]]
2. [[ISO_IEC_IEEE_29148_2018]] Systems and software engineering — Life cycle processes — Requirements engineering
3. [[ISO_IEC_IEEE_15288_2015]] ISO/IEC/IEEE 15288 Systems and software engineering - System life cycle processes
4. [[LeidraadSE2]]; deze leidraad is niet meer actueel, in [[LeidraadSE3]] worden geen verificatiemethoden meer benoemd die in versie 2 wel stonden. Daarbij geldt, dat in de sector voldoende consensus lijkt te bestaan over de in [[LeidraadSE2]] genoemde verificatiemethoden. Dit in tegenstelling tot de eistypen, waarvoor dit nog onvoldoende geldt. 


<dl>
<dt><dfn>Vaststellen
	<dd>Het vaststellen van verificatiecriteria waarbij een of meer kenmerken en hun karakteristieke waarden worden bepaald als basis voor de verificatie.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Vaststellen">csw:Vaststellen</a> 
	<dd>Engels: Determining [[NEN_EN_ISO_9000_2015]] par. 3.11

<dt><dfn>Beoordelen
	<dd>Op basis van deskundigheid vaststellen van de geschiktheid, toereikendheid of doeltreffendheid van een systeem, een proces, een product, een dienst of een activiteit om te zien of het aan de verificatiecriteria voldoet.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Beoordelen">csw:Beoordelen</a>
	<dd>Engels: Reviewing [[NEN_EN_ISO_9000_2015]] par. 3.11	

<dt><dfn>Monitoren
	<dd>Het systematisch en periodiek verzamelen van de status een systeem, een proces, een product, een dienst of een activiteit om te zien of het aan de verificatiecriteria voldoet. <a href="https://www.encyclo.nl/begrip/monitoren">Bron definitie:Encyclo.nl</a>
	<dd>Voorbeelden: zettingsmetingen met sensoren, monitoring van draaiuren voor optimale vervanging.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Monitoren">csw:Monitoren</a>
	<dd>Engels: Monitoring [[NEN_EN_ISO_9000_2015]] par. 3.11

<dt><dfn>Meten
	<dd>Het uitdrukken van een waargenomen grootheid in een getal met een relevante eenheid die vergeleken kan worden met andere waardes van eenzelfde grootheid. Hiervoor kunnen meetinstrumenten worden gebruikt. Meting is echter niet beperkt tot natuurkundige grootheden, maar strekt zich uit tot een kwantitatieve beschrijving van de gehele werkelijkheid. Metingen zijn meestal kwantitatieve waarnemingen: het resultaat wordt in een getalwaarde en een eenheid uitgedrukt.  <a href="https://nl.wikipedia.org/wiki/Meten">Bron definitie:Wikipedia</a>
	<dd>Voorbeelden: luchtsnelheidmetingen in tunnels, kalenderen van heipalen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Meten">csw:Meten</a>
    <dd>Engels: Measuring [[NEN_EN_ISO_9000_2015]] par. 3.11

<dt><dfn>Keuren
	<dd>Een formele en gedisciplineerde beoordelingstechniek waarbij wordt onderzocht of een systeem, een proces, een product, een dienst of een activiteit aan de verificatiecriteria voldoet. Het gebruik van controlelijsten (checklists) is typisch voor de vorm van beoordeling. <a href="https://www.encyclo.nl/begrip/keuring">Bron definitie:Encyclo.nl</a>
	<dd>Voorbeelden: een ingangs- en uitgangscontrole.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Keuren">csw:Keuren</a>
	<dd>Engels: Inspecting [[NEN_EN_ISO_9000_2015]] par. 3.11

<dt><dfn>Beproeven
	<dd>Het door middel van gebruik vaststellen of een systeem, een proces, een product, een dienst of een activiteit aan de verificatiecriteria voldoet.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Beproeven">csw:Beproeven</a>
	<dd>Engels: Testing [[NEN_EN_ISO_9000_2015]] par. 3.11	

<dt><dfn>Evalueren
	<dd>Het verzamelen, interpreteren en presenteren van informatie teneinde de waarde van een resultaat of proces te bepalen. Hierbij kan het gaan om het waarderen van de resultaten van personen of bedrijven, maar ook om het waarderen van alternatieve oplossingen. <a href="https://nl.wikipedia.org/wiki/Evaluatie">Bron definitie:Wikipedia</a>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Evalueren">csw:Evalueren</a>
	<dd>Engels: Evaluating [[NEN_EN_ISO_9000_2015]]	par. 3.11

<dt><dfn>Analyseren
    <dd>het ontleden van een bepaald (denk)object tot de constituerende elementen. Het is een wetenschappelijke methode om data, objecten en materie systematisch te onderzoeken. 
	<dd>Voorbeelden: Haalbaarheidsanalyse, kosten-batenanalyse, materiaalanalyse.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Analyseren">csw:Analyseren</a>
	<dd>Engels: Analysing (including modelling and simulation) [[ISO_IEC_IEEE_29148_2018]] par. 6.5.2

<dt><dfn>Berekenen
    <dd>Het uitvoeren van berekeningen aan een systeem, een proces, een product, een dienst of een activiteit om te bereken of het aan de verificatiecriteria voldoet.
	<dd>Voorbeeldensterkteberekeningen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Berekenen">csw:Berekenen</a>
	<dd>Engels: Calculating (part of Analysing) [[ISO_IEC_IEEE_29148_2018]] par. 6.5.2	

<dt><dfn>Auditen
    <dd>Onafhankelijk onderzoeken en evalueren van de activiteiten en de resultaten van een organisatie. <a href="https://www.encyclo.nl/begrip/audit">Bron definitie:Encyclo.nl</a>. 
	<dd>Voorbeelden: Audit van bestaande kwaliteitssystemen en -processen, Technical Inspection Services. 
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Auditen">csw:Auditen</a>
	<dd>Engels: Auditing [[ISO_IEC_IEEE_15288_2015]] 4.1

<dt><dfn>Demonstreren
    <dd>Laten zien dat een systeem, een proces, een product, een dienst of een activiteit aan de verificatiecriteria voldoet.
	<dd>Voorbeeld: presentatie van de functionaliteiten van een bestaand systeem
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Demonstreren">csw:Demonstreren</a>
	<dd>Engels: Demonstrating [[ISO_IEC_IEEE_29148_2018]] par. 6.5.2		
	
<dt><dfn>Document beoordelen
    <dd>Op basis van deskundigheid vaststellen of een document aan de verificatiecriteria voldoet.
	<dd>o.a. documentinspecties, reviews, toetsen, ontwerpateliers
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Documentbeoordelen">csw:Documentbeoordelen</a>
	<dd>Engels: Document reviewing [[NEN_EN_ISO_9000_2015]] par. 3.11		

<dt><dfn>Modelleren
     <dd>Met behulp van een fysiek of virtueel model onderzoeken of een systeem, een proces, een product, een dienst of een activiteit aan de verificatiecriteria voldoet.
	<dd>Voorbeelden: prestatiemodellen van beschikbaarheid, verkeersmodellen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Modelleren">csw:Modelleren</a>
	<dd>Engels: Modelling (part of Analysing) [[ISO_IEC_IEEE_29148_2018]] par. 6.5.2	


<dt><dfn>Simuleren
    <dd>Met behulp van een fysiek of virtueel model het gebruik nabootsen van een systeem, een proces, een product, een dienst of een activiteit om te zien of het aan de verificatiecriteria voldoet.
	<dd>Voorbeeld: Dienstregelingsimulatie
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Simuleren">csw:Simuleren</a>
	<dd>Engels: Simulating (part of Analysing) [[ISO_IEC_IEEE_29148_2018]] par. 6.5.2		

<dt><dfn>Refereren
    <dd>Door te verwijzen naar een alternatieve toepassing of verificatie van een systeem, een proces, een product, een dienst of een activiteit laten zien dat deze aan de verificatiecriteria voldoet.
	<dd>Voorbeeld: gebruik van gecertificeerde producten
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Refereren">csw:Refereren</a>
	<dd>Engels: Referencing 
	
<dt><dfn>Testen
    <dd>Het proces waarmee de correcte werking van een systeem of product wordt aangetoond. Activiteiten zoals meten, onderzoeken, beproeven, keuren met kalibers van één of meer kenmerken van een product of dienst en het vergelijken van de uitkomsten met de verificatiecriteria, om te bepalen of aan de eisen is voldaan.
	<dd>Voorbeeld: haalbaarheidstesten, <abbr title="Factory Integration Test">FIT</abbr>, <abbr title="Factory Acceptance Test">FAT</abbr>, <abbr title="Site Integration Test">SIT</abbr>, <abbr title="Site Acceptance Test">SAT</abbr>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Testen">csw:Testen</a>
	<dd>Bron definitie: <a href="https://nl.wikipedia.org/wiki/Testen_(software)">Wikipedia:Testen</a>
	<dd>Engels: Testing [[ISO_IEC_IEEE_29148_2018]] par. 6.5.2	

<dt><dfn>Factory Integration Test
    <dd>Het integraal testen van de functionaliteit van systemen voordat zij de fabriek verlaten.
	<dd>Voorbeelden: hydraulische en mechanische installaties integraal testen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/FactoryIntegrationTest">csw:FactoryIntegrationTest</a>

<dt><dfn>Factory Acceptance Test
    <dd>Het testen van systemen in een fabrieksopstelling om te zien of het aan de verificatiecriteria voldoet.
	<dd>Voorbeelden: cameratesten in fabrieksopstelling
	<dd><a href="https://data.crow.nl/contractspecificaties/id/FactoryAcceptanceTest">csw:FactoryAcceptanceTest</a>

<dt><dfn>Site Integration Test
    <dd>Het integraal testen van de functionaliteit van een reeds op locatie ingericht systeem.
	<dd>Voorbeelden: interactietesten tussen installatie- en besturingssystemen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/SiteIntegrationTest">csw:SiteIntegrationTest</a>

<dt><dfn>Site Acceptance Test
     <dd>Het testen van een reeds op locatie ingericht systeem  om te zien of het aan de verificatiecriteria voldoet.  
	<dd>Voorbeelden: calamiteitenoefeningen in bijzijn van hulpdiensten
	<dd><a href="https://data.crow.nl/contractspecificaties/id/SiteAcceptanceTest">csw:SiteAcceptanceTest</a>

<dt><dfn>Schouwen
    <dd>Op basis van deskundigheid ter plaatse visueel vaststellen of een systeem, een proces, een product, een dienst of een activiteit aan de verificatiecriteria voldoet.
	<dd>Voorbeelden: visuele opname van projectlocatie
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Schouwen">csw:Schouwen</a>

<dt><dfn>Inspecteren
    <dd>Het eenmalig of periodiek onderzoeken of een in gebruik zijnd systeem, een proces, een product, een dienst of een activiteit aan de verificatiecriteria voldoet.
	<dd>Voorbeelden: Arbo-inspecties, pompkelderinspecties
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Inspecteren">csw:Inspecteren</a>
	<dd>Engels: Inspecting [[ISO_IEC_IEEE_29148_2018]] par. 6.5.2
</dd></dl>

| Taalbinding                                                                                | Kardinaliteit | Datatype                                                |
| ------------------------------------------------------------------------------------------ | ------------- | ----------------------------------------------------------------------------------------------- |
| [cs:verificationMethod](https://data.crow.nl/contractspecificaties/def/verificationMethod) | 0:1  tov een Verificatievoorschrift           | [cs:VerificationMethodeType](https://data.crow.nl/contractspecificaties/def/verificationMethod) |
| { .def } |

### Enum <dfn>verificatieFase

In deze kolom staat de fase van het Verificatievoorschrift. Dit is een enumeratie, dat wil zeggen dat de gebruiker moet kiezen uit een lijst met van te voren vastgestelde fasen. Dit om uitwisseling tussen systemen makkelijker te maken.

De opdrachtgever gebruikt deze fase, om een grove selectie te kunnen maken van de eisen die in een bepaalde fase relevant zijn, zodat niet meteen in de Conceptfase ook alle technische eisen voor de Gebruiksfase worden meegenomen of beoordeeld. Deze selectie kan ook worden uitgewisseld met bijvoorbeeld een externe partij die in de voorfase meehelpt bij concept, ontwerp en het opstellen van een contract. Daarom is dit onderdeel van het uitwisselformaat voor Contractspecificaties.

Als je specifiekere deadlines wilt voorschrijven, moet je dezen opnemen bij [=VerificatieMoment=]

De voorwaarde om deze fase te kunnen vastleggen is het bijvoegen van een Verificatievoorschrift.

<a href="https://www.researchgate.net/publication/362209021_An_Explorative_Analysis_of_European_Standards_on_Building_Information_Modelling">Deze analyse</a> op basis van ISO 22263:2008 enRIBA, 2020: Royal Institution of British Architects, (2020). The
RIBA Plan of Work 2020. (R. Architecture, Ed.)(RIBA). London: RIBA Architecture.) geeft de volgende fasen, aangevuld met de Nederlandse definities uit de [[LeidraadSE2]]

<dl>
<dt><dfn lang=EN>Strategic Definition / <dfn lang="NL">Conceptfase
	<dd>Fase om (nieuwe) behoeften van stakeholders te inventariseren en mogelijkheden te beoordelen. De eerste klanteisen en oplossingsrichting worden hier bepaald. De conceptfase kan leiden tot het initiatief voor het ontwikkelen en realiseren van een systeem.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Conceptfase">csw:Conceptfase</a>
	<dd> [Bron: [[LeidraadSE2]], Hoofdstuk 4
<dt><dfn lang=EN>Briefing / <dfn lang="NL">Projectinstructiefase
	<dd>De overhandiging van de bestaande situatie, de eerste klanteisen vanuit de stakeholders en oplossingsrichting van de asset manager aan het project.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Projectinstructiefase">csw:Projectinstructiefase</a>
<dt><dfn lang=EN>Design / <dfn lang="NL">Ontwikkelfase
	<dd>De fase om een systeem te specificeren dat voldoet aan de klanteisen. Aan het eind van de ontwikkelfase ligt er een (startklaar) ontwerp voor het gehele systeem.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Ontwikkelfase">csw:Ontwikkelfase</a>
	<dd> [Bron: [[LeidraadSE2]], Hoofdstuk 4
<dt><dfn lang=EN>Procurement / <dfn lang="NL">Contracterings- en aanbestedingsfase
	<dd>De fase om het systeem te vervaardigen en beproeven. Systeemelementen en deelsystemen worden geïntegreerd tot één geheel.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Contracteringaanbestedingsfase">csw:Contracteringaanbestedingsfase</a>
<dt><dfn lang=EN>Manufacturing and Construction / <dfn lang="NL">Fabricage- en bouwfase
	<dd>De fase om het systeem te vervaardigen en beproeven. Systeemelementen en deelsystemen worden geïntegreerd tot één geheel.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Fabricageenbouwfase">csw:Fabricageenbouwfase</a>
	<dd> [Bron: [[LeidraadSE2]], Hoofdstuk 4
<dt><dfn lang=EN>Handover / <dfn lang="NL">Oplevering projectfase
	<dd>De oplevering van het project aan de asset manager </dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Opleveringproject">csw:Opleveringprojectfase</a>
<dt><dfn lang=EN>Operation and Maintenance / <dfn lang="NL">Gebruiksfase
	<dd>De gebruiksfase is de periode waarin het systeem wordt geëxploiteerd. Hier vinden de activiteiten plaats die nodig zijn om het systeem te gebruiken zoals beoogd, zoals facility management of aansturing van systemen, en ondersteunende beheer- en onderhoudsactiviteiten</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Gebruiksfase">csw:Gebruiksfase</a>
	<dd> [Bron: [[LeidraadSE2]], Hoofdstuk 4
<dt><dfn lang=EN>Decommissioning / <dfn lang="NL">Sloopfase
	<dd>De fase om een systeem met bijbehorende operationele diensten en functies buiten werking te stellen en te verwijderen.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Sloopfase">csw:Sloopfase</a>
	<dd> [Bron: [[LeidraadSE2]], Hoofdstuk 4
</dl>

| Taalbinding                                                      | Kardinaliteit | Datatype                                                                 |
| ---------------------------------------------------------------- | ------------- | ------------------------------------------------------------------------ |
| [cs:phase](https://data.crow.nl/contractspecificaties/def/phase) | 0:1  tov een Verificatievoorschrift            | [cs:PhaseType](https://data.crow.nl/contractspecificaties/def/PhaseType) |
| { .def } |


### <dfn>verificatieMoment
De opdrachtgever gebruikt deze fase, om vast te leggen wanneer een eis geverifieerd dient te worden. De voorwaarde om een Verificatiemoment te kunnen vastleggen is het bijvoegen van een Verificatievoorschrift.

| Taalbinding                                                           | Kardinaliteit | Datatype                                               |  Geadviseerd maximaal aantal tekens                                               |
| --------------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [cs:verificationMoment](https://data.crow.nl/contractspecificaties/def/verificatieMoment) | 0:1   tov een Verificatievoorschrift          | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 255 |
| { .def } |

<aside class="note" title="Standaard fasen / momenten">
Er zijn verschillende richtlijnen en afspraken in Nederland die werken met een lijst met oplevermomenten of andere momenten/fasen in een project. Al naar gelang de context, kan dus een standaard gebruikt worden. Op dit moment is niet duidelijk, of dit kan leiden tot één standaard, of dat voor verschillende toepassingen verschillende lijsten beschikbaar zijn. Een paar van de genoemde standaarden:
<ul>
<li>In de DNR (De Nieuwe Regeling) is een <a href="https://bna.nl/standaardtaakbeschrijving-stb">standaardtaakbeschrijving</a> (STB) beschikbaar waarin een recentere fase opdeling wordt gehanteerd. Er is een herziening van de DNR in de maak (Zie <a href="https://www.nlingenieurs.nl/nieuws/consultatie-van-de-vernieuwde-regeling-dnr2022-van-start/">dit nieuwsbericht</a>) en volgens <a href="https://www.stiion.nl/de-nieuwe-regeling-dnr/#:~:text=De%20laatste%20versie%20van%20de%20STB%20dateert%20van%202014%20(STB%202014).%20Er%20wordt%20gewerkt%20aan%20een%20update%20van%20de%20STB%20waarbij%20onder%20andere%20aandacht%20is%20voor%20het%20digitale%20ontwerp%2D%20en%20bouwproces">dit nieuwsbericht</a> wordt gewerkt aan een update van de STB.</li>
<li>Bouwend Nederland heeft een structuur ontwikkeld volgens <a href="https://www.bouwendnederland.nl/actueel/nieuws/23671/vib-ontwikkelt-branche-brede-eenduidige-structuur-voor-ontwerpfasen">dit nieuwsbericht</a></li>
</ul>
</aside>


### <dfn>verificatievoorschriftToelichting

In deze kolom staat de toelichting op het Verificatievoorschrift.

In contracten wordt dit gebruikt om nader toe te lichten waarom dit Verificatievoorschrift gevraagd wordt.

| Taalbinding                                                           | Kardinaliteit | Datatype                                               |  Geadviseerd maximaal aantal tekens                  |
| --------------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [skos:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) | 0:1  tov een Verificatievoorschrift           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 2000 |
| { .def } |



