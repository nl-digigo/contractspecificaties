# Eisen

Het eisenformat wordt gebruikt om de eisen te kunnen uitwisselen als data. Bij elke kolom is aangegeven wat de vertaling/binding is naar linked data standaarden, hoe vaak deze waarde ingevuld mag worden per eis ("kardinaliteit") en een beschrijving.

Een eis is een [NEN2660:Requirement](https://bimloket.github.io/nen2660/def#Requirement) volgens NEN 2660.

## Eisenformat

Het format wordt rijen getoond in plaats van in kolommen, om de leesbaarheid te bevorderen.



<table class="data">
<thead>
	<th>Kolomnaam
	<th>Definitie
	<th>Voorbeeld
</thead>
<tr>
	<td scope="row"> [=EisURI=]
	<td class="def">In deze kolom staat de unieke identifier (URI) van de eis.
	<td class="example">`https://www.example.org/id/Voorbeeld-Eis1`
</tr>
<tr>
	<td scope="row"> [=EisCode=]
	<td class="def">In deze kolom staat de code of het nummer van de eis.
    <td class="example">EIS1099
</tr>
	<td scope="row"> [=EisTitel=]
	<td class="def">In deze kolom staat de de naam oftewel de titel van de eis.
	<td class="example">Voorbeeldeis
</tr>
	<td scope="row"> [=EisTekst=]
	<td class="def">In deze kolom staat de eistekst.
	<td class="example">Dit is de tekst van de voorbeeldeis
</tr>
<tr>	
	<td scope="row"> [=EisToelichting=]
	<td class="def">In deze kolom staat de toelichting op de eis.
	<td class="example">Dit is de toelichting van de voorbeeldeis, om achtergrond / doel en reden van de eis te kunnen verduidelijken
</tr>
<tr>
	<td scope="row"> [=EisheeftDeel=]
	<td class="def">In deze kolom staat de URI van een onderliggende eis. 
	<td class="example"> `https://www.example.org/id/Voorbeeld-Eis2`
</tr>
<tr>
	<td scope="row"> [=EisBron=]
	<td class="def"> In deze kolom staat de URI van een bron van de eis in een eisenbibliotheek of brondocument. 
	<td class="example"> `https://www.example.org/id/Voorbeeld-Document1`
</tr>
<tr>
	<td scope="row"> [=EisReferentiedocument=]
	<td class="def"> In deze kolom staat de URI van een gerefereerd document waarin aanvullende eisen staan 
	<td class="example"> `https://www.example.org/id/Voorbeeld-Document2`
</tr>
<tr>
	<td scope="row"> [=EisType=]
	<td class="def"> In deze kolom staat het eistype. 
	<td class="example"> `https://data.crow.nl/contractspecificaties/id/Proceseis` 
</tr>
<tr>
	<td scope="row"> [=EisStatus=]
	<td class="def">  In deze kolom staat de status van de eis. 
	<td class="example">  `https://data.crow.nl/contractspecificaties/id/Vervallen` 
</tr>
<tr>
	<td scope="row"> [=EisStatusOnderbouwing=]
	<td class="def"> In deze kolom staat een toelichting op de status van de eis. 
	<td class="example"> Komt niet meer voor want ... 
</tr>
<tr>
	<td scope="row"> [=EisverificatieplanURI=]
	<td class="def"> In deze kolom staat de URI van een verificatieplan bij de eis.
	<td class="example">`https://www.example.org/id/Voorbeeld-Verificatieplan1`
</tr>
<tr>
	<td scope="row"> [=EisheeftOnderwerp=]
	<td class="def">In deze kolom staat de URI van het Onderwerp (subject) van de eis.
	<td class="example"> `https://www.example.org/id/Voorbeeld-Onderwerp1`
</tr>
<tr>
	<td scope="row"> [=EisverificatieplanMethode=]
	<td class="def">In deze kolom staat de verificatiemethode van het verificatieplan.
	<td class="example">`https://data.crow.nl/contractspecificaties/id/Keuring`
</tr>
<tr>
	<td scope="row"> [=EisverificatieplanFase=]
	<td class="def">In deze kolom staat de fase waarin dit Eisverificatieplan wordt uitgevoerd.
	<td class="example">`https://data.crow.nl/contractspecificaties/id/Aanleg`
</tr>
<tr>
	<td scope="row"> [=EisverificatieplanToelichting=]
	<td class="def">In deze kolom staat de toelichting op de verificatiemethode bij de eis.
	<td class="example">Een toelichting waarom een verificatiemethode wordt gevraagd bij de eis, of nadere invulling van de verificatiemethode
</tr>
</table>


## Details

### <dfn>EisURI

De URI is de unieke identifier voor de eis binnen het project. Zie [URI volgens W3C](https://www.w3.org/wiki/URI).

Voor het opstellen van URI's heeft de [[NEN_2660_2_2022]] een URI-strategie die je moet volgen.

Bij de eisen kan verwezen worden naar een eis in een eisenbibliotheek onder [=EisBron=]. Daar staat de URI van de eis uit de bibliotheek. Deze URI verwijst naar een openbaar gepubliceerde eis in een bibliotheek, bijvoorbeeld het Provinciaal Contracten Buffet.

De eis in het project moet een andere URI hebben dan de bron. Het is niet dezelfde eis, want deze wordt toegepast in (gekopieerd naar) een andere context.


| Taalbinding | Kardinaliteit | Datatype                                               |
| ----------- | ------------- | ------------------------------------------------------ |
| n.v.t.      | 1:1           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

> NOTE
> Een URI maakt het meteen "linked data proof"

### <dfn>EisCode

De EisCode is een nummer van de eis in spreektaal, vaak een voor mensen herkenbare code of projectnummer. Deze meestal eenvoudige en soms logisch genummerde Code maakt het mogelijk om in een gesprek naar de eis te verwijzen, zonder de volledige URI te hoeven benoemen.

| Taalbinding                                                                   | Kardinaliteit | Datatype                                               |
| ----------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [skos:notation](https://www.w3.org/2009/08/skos-reference/skos.html#notation) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def } |

### <dfn>EisTitel

De EisTitel wordt ook wel eens de titel van de eis genoemd, en geeft een voor mensen leesbare korte duiding van de inhoud van de eis.

De EisTitel hoeft niet uniek te zijn in het project, daarvoor heeft de eis een URI. Een unieke naam is voor de menselijke lezer vaak wel handig. Soms wordt de EisTitel in applicaties bijvoorbeeld gebruikt bij het visualiseren van de eisenboom. Unieke namen helpen in dat geval.

| Taalbinding                                                                     | Kardinaliteit | Datatype                                               |
| ------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def } |

### <dfn>EisTekst

De EisTekst bevat de voor mensen leesbare inhoud van de eis.
Op dit moment worden eisen in een contract meestal niet voorzien van een voor een systeem leesbare eis, zoals bijvoorbeeld een minimale waarde voor een attribuut van een object. Deze "dataficeringsslag" is buiten scope van dit document, omdat dit een verder gevorderd BIM niveau vraagt en dit document juist bedoelt is als opstap naar uitwisseling van data.

In de EisTekst kan verwezen worden naar een referentiedocument, waar aanvullende eisen in staan die gelden binnen het contract. De URI van dit document wordt dan opgenomen in de kolom Referentiedocument.

| Taalbinding                                                   | Kardinaliteit | Datatype                                               |
| ------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [rdf:value](http://www.w3.org/1999/02/22-rdf-syntax-ns#value) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def } |

### <dfn>EisToelichting

In deze kolom staat de toelichting op de eistekst

In contracten wordt dit gebruikt om nader te onderbouwen waarom deze eis gesteld wordt.

| Taalbinding                                                           | Kardinaliteit | Datatype                                               |
| --------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [skos:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def } |


### <dfn>EisheeftDeel

In deze kolom staat de URI van een onderliggende eis.

Hiermee kan een hiërarchie worden aangegeven van de eisenboom zoals gebruikelijk in contracten. Een eis kan meerdere onderliggende eisen hebben, er komen dan meerdere regels met dezelfde eis voor in de eisentabel.

| Taalbinding                                                        | Kardinaliteit | Datatype                                               |
| ------------------------------------------------------------------ | ------------- | ------------------------------------------------------ |
| [nen2660:hasPart](https://bimloket.github.io/nen2660/term#hasPart) | 0:n           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

### <dfn>EisBron

De bron van de eis kan naar twee zaken verwijzen:

1. De URI van de gebruikte eis uit een bibliotheek (indien deze niet gewijzigd is). Deze URI verwijst naar een openbaar gepubliceerde eis in een bibliotheek, bijvoorbeeld het Provinciaal Contracten Buffet. De eis in het project moet een andere URI hebben dan de bron. Het is niet dezelfde eis, want deze wordt toegepast in (gekopieerd naar) een andere context.
2. De URI van een brondocument met herkomst van de eis. Deze URI verwijst naar een document in de documententabel.

| Taalbinding                                   | Kardinaliteit | Datatype                                               |
| --------------------------------------------- | ------------- | ------------------------------------------------------ |
| [dct:source](http://purl.org/dc/terms/source) | 0:n           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

### <dfn>EisReferentiedocument

Als in de eistekst wordt verwezen naar een referentiedocument, staat in deze kolom de URI van het gerefereerde document. Deze URI verwijst naar een document in de documententabel.

Een referentiedocument is een document waarin extra eisen staan die in het contract gelden, die de opdrachtnemer zelf uit het document moet afleiden. Voorbeelden:

* De eis verwijst naar een ontwerp of berekening die van toepassing is.
* De eis verwijst naar een richtlijn, handleiding of norm die van toepassing is.

Instructie voor gebruik: omdat nog niet alle partijen in staat zijn om de data helemaal te verwerken, moet je het document wel in de eistekst noemen. De eistekst is leidend. Een ontvanger van de eisenset kan er ook niet van uit gaan, dat de opdrachtgever dit altijd in weet te vullen. Als in een eistekst naar een referentiedocument wordt verwezen, kan het zijn dat er geen relatie is gemaakt naar het referentiedocument.


| Taalbinding                                           | Kardinaliteit | Datatype                                               |
| ----------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [dct:references](http://purl.org/dc/terms/references) | 0:n           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

### <dfn>EisType

In deze kolom staat het eistype. De aspecteisen zijn grotendeels overgenomen uit de [Leidraad SE v3](https://www.leidraadse.nl/assets/files/downloads/LeidraadSE/V3/Leidraad_V3_SE_web.pdf); de eistypen die aanduiden aan wat voor concept de eis is gesteld zijn aangepast aan de onderwerpen uit deze richtlijn. Dit is een enumeratie.

Bij uitwisseling mag je uitsluitend de onderstaande lijst gebruiken, zonder zelf uitbreidingen te doen. Als elke opdrachtgever een eigen lijst met eistypen en aspecten gebruikt wordt het inrichten van standaard omgevingen voor de verwerking van contracteisen onnodig bemoeilijkt, waarbij bij elk project een aangepaste lijst moet worden gemaakt.

Eistypen:

<div class="issue" data-number="48"></div>

<dl>
<dt><dfn>Informatie-eis
   <dd>Verzameling van eisen die betrekking hebben op de te leveren informatieproducten
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Informatie-eis">csw:Informatie-eis</a>
	   
<dt><dfn>Systeemeis
   <dd>De beschrijving van het geheel aan samenhangende of elkaar beïvloedende eisen dat bijdraagt aan het tot standkomen en gebruiken danwel toepassen van het geintegreerde systeem.
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Systeemeis">csw:Systeemeis</a>
   <dd>Bron: Leidraad SE v3 
	 
<dt><dfn>Proceseis
   <dd>De beschrijving van het gevraagde geheel van samenhangende of elkaar beïnvloedende activiteiten dat input omzet in output. 
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Proceseis">csw:Proceseis</a>
   <dd>Bron: Leidraad SE v3

<dt><dfn>Functie-eis
   <dd>De beschrijving van de gevraagde beoogde werking en/of verrichting van een systeem.
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Functie-eis">csw:Functie-eis</a>
 <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Betrouwbaarheid
   <dd>De waarschijnlijkheid dat de vereiste functie wordt uitgevoerd onder gegeven omstandigheden gedurende een bepaald tijdsinterval. 
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Betrouwbaarheid">csw:Aspecteis-Betrouwbaarheid</a>
 <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Beschikbaarheid
   <dd>De waarschijnlijkheid dat de vereiste functie op een willekeurig moment kan worden uitgevoerd onder gegeven omstandigheden.	
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Beschikbaarheid">csw:Aspecteis-Beschikbaarheid</a>
 <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Onderhoudbaarheid
   <dd>De waarschijnlijkheid dat de activiteiten voor onderhoud kunnen worden uitgevoerd binnen de hiervoor vastgestelde tijden, onder gegeven omstandigheden teneinde de vereiste functie te kunnen (blijven) uitvoeren.
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Onderhoudbaarheid">csw:Aspecteis-Onderhoudbaarheid</a>
 <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Veiligheid
   <dd>De waarschijnlijkheid dat de vereiste functie en de daarvoor benodigde activiteiten zonder optredend letsel aan personen kan worden vervuld dan wel uitgevoerd en de waarschijnlijkheid dat de integriteit van de functie  en de daaraan verbonden data en datastructuren gewaarborgd blijven van ongewenste beïnvloeding.	   
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Veiligheid">csw:Aspecteis-Veiligheid</a>
 <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Gezondheid
   <dd>De waarschijnlijkheid dat de vereiste functie en de daarvoor benodigde activiteiten zonder negatieve gezondheidsrisico's voor personen kan worden vervuld dan wel uitgevoerd.
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Gezondheid">csw:Aspecteis-Gezondheid</a>
   <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Omgeving
   <dd>De waarschijnlijkheid dat de vereiste functie en de daarvoor benodigde activiteiten zonder ongewenste risico's voor de omgeving kunnen wordenvervuld en/of gerealiseerd.	
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Omgeving">csw:Aspecteis-Omgeving</a>    
   <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Duurzaamheid
   <dd>De waarschijnlijkheid dat de vereiste functie en de daarvoor benodigde activiteiten binnen de hieraan gestelde eisen en PPP (People/Planet/Profit)-doelstellingen kunnen worden gerealiseerd.  
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Duurzaamheid">csw:Aspecteis-Duurzaamheid</a>
   <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Vormgeving
   <dd>De beschrijving van de gevraagde prestatie ten aanzien van het beeld en het materiaalgebruik met inachtneming van de omgevings- en de gezondheidseisen van het systeem en haar onderdelen.
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Vormgeving">csw:Aspecteis-Vormgeving</a>
   <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Toekomstvastheid
   <dd>De beschrijving van de gevraagde prestatie van een systeem ten aanzien van de vereiste levensduur van het systeem (als functie en als object) en haar onderdelen.	    
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Toekomstvastheid">csw:Aspecteis-Toekomstvastheid</a>
   <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Sloopbaarheid
   <dd>De waarschijnlijkheid dat de vereiste functie aan het einde van de levensduur op beheerste wijze kan worden teruggebracht tot minimaal secundaire grondstoffen en met inachtneming van de overige aspecten.  
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Sloopbaarheid">csw:Aspecteis-Sloopbaarheid</a>
   <dd>Bron: Leidraad SE v3 
</dd></dl>

| Taalbinding                                                                       | Kardinaliteit | Datatype                                                             |
| --------------------------------------------------------------------------------- | ------------- | -------------------------------------------------------------------- |
| [nen2660:requirementTopicType](https://w3id.org/nen2660/def#requirementTopicType) | 0:n           | [cs:EisType](https://data.crow.nl/contractspecificaties/def/EisType) |
| { .def } |

### <dfn>EisStatus

In deze kolom staat de status van de eis. Dit is een enumeratie. Voor contractspecificaties geldt dat de status één van deze twee zaken is: actueel of vervallen.
Doel is om wijzigingen door een Nota van Inlichtingen of een contractuele wijziging in de eisenset te kunnen opnemen en met elkaar uit te wisselen.

<dl>
<dt><dfn>Actueel
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Actueel">csw:Actueel</a>
<dt><dfn>Vervallen
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Vervallen">csw:Vervallen</a>
</dl>

| Taalbinding                                                        | Kardinaliteit | Datatype                                                                   |
| ------------------------------------------------------------------ | ------------- | -------------------------------------------------------------------------- |
| [cs:status](https://data.crow.nl/contractspecificaties/def/status) | 1:1           | [cs:StatusType](https://data.crow.nl/contractspecificaties/def/StatusType) |
| { .def } |

### <dfn>EisStatusOnderbouwing

In deze kolom staat een toelichting op de status van de eis.
Gebruikers willen de reden van vervallen toevoegen aan de eis, zodat de status onderbouwd is.

| Taalbinding                                                                                | Kardinaliteit | Datatype                                               |
| ------------------------------------------------------------------------------------------ | ------------- | ------------------------------------------------------ |
| [cs:statusOnderbouwing](https://data.crow.nl/contractspecificaties/def/statusOnderbouwing) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def } |

<p class="note">
De "eigenaar" van een eis is vaak een interne rolhouder. In het contract gelden hiervoor de projectafspraken en kan de eigenaar vertegenwoordigd zijn door een andere rolhouder. Een eigenaar van een eis kan intern bijvoorbeeld de objectbeheerder zijn, maar in het contract is de technisch manager eerste aanspreekpunt voor de eis. Meestal wordt de eigenaar niet benoemd in de vraagspecificaties. Daarom is "eigenaarschap" niet opgenomen in de eisentabel.
</p>


### <dfn>EisverificatieplanURI

De URI is de unieke identifier voor het Eisverificatieplan in deze fase, in dit project. Zie [URI conform W3C](https://www.w3.org/wiki/URI).
Voor het opstellen van URI's heeft de [[NEN_2660_2_2022]] een URI-strategie die je moet volgen.


Het Eisverificatieplan geeft de verificatiemethode voor de eis (een type uit een lijst plus een vrij tekstveld met toelichting), per object en per fase waarin de verificatie wordt uitgevoerd.  

Een eis kan meerdere verificatieplannen kennen, elk in een eigen fase. Een Eisverificatieplan geldt voor één fase. Indien in een andere fase precies dezelfde verificatie wordt uitgevoerd, zijn er twee Eisverificatieplannen.  



Kardinaliteit: 1:1 ten opzichte van een verificatieplan
Datatype:

| Taalbinding | Kardinaliteit | Datatype                                               |
| ----------- | ------------- | ------------------------------------------------------ |
| n.v.t.      | 1:1           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

<figure>
<img src="./media/Diagram2.drawio.svg" alt="UML schema voor het informatiemodel voor het verificatieplan">
<figcaption>Het informatiemodel voor het verificatieplan. In de [[NEN_2660_2_2022]] hoort het Onderwerp bij het Eisverificatieplan en heeft geen directe relatie met de eis.</caption>
</figure>

### <dfn>EisheeftOnderwerp

In deze kolom staat de URI van het Onderwerp van het Eisverificatieplan. Een eis kan aan meerdere Onderwerpen gesteld worden, er komen dan meerdere regels met dezelfde eis voor in de eisentabel met elk een eigen Eisverificatieplan en een eigen onderwerp.

Merk op, dat verwijzing naar de URI de tabel minder makkelijk leesbaar maakt voor de mens. Indien hier ook de naam van het concept zou worden toegevoegd, creëert dit dubbelingen met de onderwerpentabel en daarom mogelijk fouten. Daarom wordt alleen de URI gebruikt.

| Taalbinding                                                                            | Kardinaliteit | Datatype                                               |
| -------------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [cs:isVerificationOf](https://data.crow.nl/contractspecificaties/def/isVerificationOf) | 1:1 tov het Eisverificatieplan          | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| [cs:hasAsSubject ](https://data.crow.nl/contractspecificaties/def/hasAsSubject)        | 1:1 tov het Eisverificatieplan          | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

> Merk op, dat in de tabel een relatie niet benoemd is, omdat de "regel" de verbindende factor is: <a href="https://data.crow.nl/contractspecificaties/def/hasAsSubject">cs:hasAsSubject</a>


### <dfn>EisverificatieplanMethode

In deze kolom staat de methode waarmee de eis geverifieerd moet worden. Dit is een enumeratie. Een eisverificatiemethode is een eigenschap van een eisverificatieplan. De eigenschap heeft een enumeratie van de verschillende mogelijke methoden, dat wil zeggen dat de gebruiker een lijst kan opstellen met verificatiemethoden en een waarde uit deze lijst kan gebruiken.

Bij uitwisseling mag uitsluitend de onderstaande lijst gebruikt worden bij contractspecificaties, zonder zelf uitbreidingen te doen. Als elke opdrachtgever een eigen lijst met eistypen en aspecten gebruikt wordt het inrichten van standaard omgevingen voor de verwerking van contracteisen onnodig bemoeilijkt, waarbij bij elk project een aangepaste lijst moet worden gemaakt.

Classificatie volgens:

1. [[NEN_EN_ISO_9000_2015]]
2. [[ISO_IEC_IEEE_29148_2018]] Systems and software engineering — Life cycle processes — Requirements engineering
4. [[LeidraadSE2]]; deze leidraad is niet meer actueel, in [[LeidraadSE3]] worden geen verificatiemethoden meer benoemd die in versie 2 wel stonden.

<dl>
<dt><dfn>Vaststellen
	<dd>Activiteit om een of meer kenmerken en hun karakteristieke waarden te achterhalen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Vaststellen">csw:Vaststellen</a> 
	<dd>Bron: [[NEN_EN_ISO_9000_2015]]

<dt><dfn>Beoordelen
	<dd>Vaststelling van de geschiktheid, toereikendheid of doeltreffendheid van een object voor het bereiken van vastgestelde doelstellingen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Beoordelen">csw:Beoordelen</a>
	<dd>Bron: [[NEN_EN_ISO_9000_2015]]

<dt><dfn>Monitoren
	<dd>Vaststellen van de status van een systeem, een proces, een product, een dienst of een activiteit. Bijvoorbeeld zettingen, monitoring van draaiuren t.b.v. optimale vervanging
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Monitoren">csw:Monitoren</a>
	<dd>Bron: [[NEN_EN_ISO_9000_2015]]

<dt><dfn>Meten
	<dd>Proces om een waarde vast te stellen. o.a. luchtsnelheidmetingen in tunnels, kalenderen van heipalen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Meten">csw:Meten</a>
	<dd>Bron: [[NEN_EN_ISO_9000_2015]] en [[LeidraadSE2]]

<dt><dfn>Keuren
	<dd>Vaststelling van conformiteit met gespecificeerde eisen. Bijvoorbeeld keuring, ingangs- en uitgangscontrole
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Keuren">csw:Keuren</a>
	<dd>Bron: [[NEN_EN_ISO_9000_2015]]

<dt><dfn>Beproeven
	<dd>Vaststellen volgens eisen voor een specifiek beoogd€ gebruik of toepassing
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Beproeven">csw:Beproeven</a>
	<dd>Bron: [[NEN_EN_ISO_9000_2015]]

<dt><dfn>Evalueren
	<dd>Beoordelen van de voortgang die behaald is met betrekking tot het bereiken van de doelen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Evalueren">csw:Evalueren</a>
	<dd>Bron: [[NEN_EN_ISO_9000_2015]]

<dt><dfn>Analyse
	<dd>o.a. haalbaarheidsanalyse, kosten-batenanalyse
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Analyse">csw:Analyse</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Berekening
	<dd>o.a. sterkteberekeningen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Berekening">csw:Berekening</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Auditen
	<dd>Audit van bestaande kwaliteitssystemen en -processen (o.a. Technical Inspection Services
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Auditen">csw:Auditen</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Demonstratie
	<dd>o.a. presentatie van de functionaliteiten van een bestaand systeem
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Demonstratie">csw:Demonstratie</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Documentbeoordeling
	<dd>o.a. documentinspecties, reviews, toetsen, ontwerpateliers
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Documentbeoordeling">csw:Documentbeoordeling</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Modellering
	<dd>o.a. prestatiemodellen van beschikbaarheid, verkeersmodellen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Modellering">csw:Modellering</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Simulaties
	<dd>o.a. dienstregelingsimulatie
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Simulaties">csw:Simulaties</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Referentie
	<dd>o.a. gebruik van gecertificeerde producten
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Referentie">csw:Referentie</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Testen
	<dd>haalbaarheidstesten, FIT, FAT, SIT, SAT
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Testen">csw:Testen</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Factory Integration Test
	<dd>o.a. hydraulische en mechanische installaties integraal testen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/FactoryIntegrationTest">csw:FactoryIntegrationTest</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Factory Acceptance Test
	<dd>o.a. cameratesten in fabrieksopstelling
	<dd><a href="https://data.crow.nl/contractspecificaties/id/FactoryAcceptanceTest">csw:FactoryAcceptanceTest</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Site Integration Test
	<dd>o.a. interactietesten tussen installatie- en besturingssystemen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/SiteIntegrationTest">csw:SiteIntegrationTest</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Site Acceptance Test
	<dd>o.a. calamiteitenoefeningen in bijzijn van hulpdiensten
	<dd><a href="https://data.crow.nl/contractspecificaties/id/SiteAcceptanceTest">csw:SiteAcceptanceTest</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Schouw
	<dd>o.a. visuele opname van projectlocatie
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Schouw">csw:Schouw</a>
	<dd>Bron: [[LeidraadSE2]]

<dt><dfn>Inspectie (cs)
	<dd>o.a. Arbo-inspecties, pompkelderinspecties
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Inspectie">csw:Inspectie</a>
	<dd>Bron: [[LeidraadSE2]]
</dd></dl>

| Taalbinding                                                                                | Kardinaliteit | Datatype                                                                                        |
| ------------------------------------------------------------------------------------------ | ------------- | ----------------------------------------------------------------------------------------------- |
| [cs:verificationMethod](https://data.crow.nl/contractspecificaties/def/verificationMethod) | 0:1           | [cs:VerificationMethodeType](https://data.crow.nl/contractspecificaties/def/verificationMethod) |
| { .def } |

### <dfn>EisverificatieplanFase

In deze kolom staat de fase van het eisverificatieplan. Dit is een enumeratie. Hierbij worden de volgende fasen onderscheiden:

<dl>
<dt><dfn>Conceptfase
	<dd>Fase om (nieuwe) behoeften van stakeholders te inventariseren en mogelijkheden te beoordelen. De eerste klanteisen en oplossingsrichting worden hier bepaald. De conceptfase kan leiden tot het initiatief voor het ontwikkelen en realiseren van een systeem.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Conceptfase">csw:Conceptfase</a>
<dt><dfn>Ontwikkelfase
	<dd>De fase om een systeem te specificeren dat voldoet aan de klanteisen. Aan het eind van de ontwikkelfase ligt er een (startklaar) ontwerp voor het gehele systeem.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Ontwikkelfase">csw:Ontwikkelfase</a>
<dt><dfn>Realisatiefase
	<dd>De fase om het systeem te vervaardigen en beproeven. Systeemelementen en deelsystemen worden geïntegreerd tot één geheel.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Realisatiefase">csw:Realisatiefase</a>
<dt><dfn>Gebruiksfase
	<dd>De gebruiksfase is de periode waarin het systeem wordt geëxploiteerd. Hier vinden de  activiteiten plaats die nodig zijn om het systeem te gebruiken zoals beoogd.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Gebruiksfase">csw:Gebruiksfase</a>
<dt><dfn>Beheer- en onderhoudsfase
	<dd>De periode waarin de ondersteunende activiteiten worden uitgevoerd, die noodzakelijk zijn om het systeem in werking te houden.</dd>
<dt><dfn>Sloopfase
	<dd>De fase om een systeem met bijbehorende operationele diensten en functies buiten werking te stellen en te verwijderen.</dd>
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Sloopfase">csw:Sloopfase</a>
</dl>

[Bron: Leidraad SE versie 2, Hoofdstuk 4](https://www.leidraadse.nl/assets/files/downloads/LeidraadSE/V2/LeidraadSE_def_lowres.pdf)

<div class="issue" data-number="53"></div>

| Taalbinding                                                      | Kardinaliteit | Datatype                                                                 |
| ---------------------------------------------------------------- | ------------- | ------------------------------------------------------------------------ |
| [cs:phase](https://data.crow.nl/contractspecificaties/def/phase) | 0:1           | [cs:PhaseType](https://data.crow.nl/contractspecificaties/def/PhaseType) |
| { .def } |

### <dfn>EisverificatieplanToelichting

In deze kolom staat de toelichting op de eisverificatiemethode.

In contracten wordt dit gebruikt om nader toe te lichten waarom deze eisverificatiemethode gevraagd wordt.

| Taalbinding                                                           | Kardinaliteit | Datatype                                               |
| --------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [skos:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def } |


<div class="issue" data-number="37"></div>