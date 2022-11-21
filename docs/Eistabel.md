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
	<td scope="row"> [=VerificatievoorschriftURI=]
	<td class="def"> In deze kolom staat de URI van een Verificatievoorschrift.
	<td class="example">`https://www.example.org/id/Voorbeeld-Verificatievoorschrift1`
</tr>
<tr>
	<td scope="row"> [=VerificatieheeftOnderwerp=]
	<td class="def">In deze kolom staat de URI van het Onderwerp (subject) van het Verificatievoorschrift.
	<td class="example"> `https://www.example.org/id/Voorbeeld-Onderwerp1`
</tr>
<tr>
	<td scope="row"> [=VerificatieMethode=]
	<td class="def">In deze kolom staat de verificatiemethode van het Verificatievoorschrift.
	<td class="example">`https://data.crow.nl/contractspecificaties/id/Keuring`
</tr>
<tr>
	<td scope="row"> [=VerificatieFase=]
	<td class="def">In deze kolom staat de fase waarin dit Verificatievoorschrift wordt uitgevoerd.
	<td class="example">`https://data.crow.nl/contractspecificaties/id/Aanleg`
</tr>
<tr>
	<td scope="row"> [=VerificatieMoment=]
	<td class="def">In deze kolom staat het moment waarop dit Verificatievoorschrift moet zijn uitgevoerd.
	<td class="example">Twee weken voor het begin van de Gebruiksfase
</tr>
<tr>
	<td scope="row"> [=VerificatieToelichting=]
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

<aside class="note" title="LinkedData Proof">
Een URI maakt het meteen "linked data proof"
</aside>


### <dfn>EisCode

De EisCode is een <i>in het contract opgenomen</i> nummer van de eis in spreektaal, vaak een voor mensen herkenbare code of projectnummer. Deze meestal eenvoudige en soms logisch genummerde Code maakt het mogelijk om in een gesprek over het contract naar de eis te verwijzen, zonder de volledige URI te hoeven benoemen. Omdat deze code de eis identificeert, moet de code binnen het project uniek zijn.

| Taalbinding                                                                   | Kardinaliteit | Datatype                                               |  Maximaal aantal tekens                                               |
| ----------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [skos:notation](https://www.w3.org/2009/08/skos-reference/skos.html#notation) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 56 |
| { .def } |

<aside class="note" title="Codes">
Bij alle codes is het zo dat iedere ketenpartner een eigen code kan hangen aan de item (eis, document, stakeholder, etc.). Aannemer, opdrachtgever, ingenieursbureau, eisenbibliotheek kunnen allemaal eigen codes toevoegen aan een eis. Omdat dit het uitwisselformaat betreft voor het contract, wordt ervan uitgegaan dat er maar één code uitgewisseld kan worden per eis. 
</aside>

### <dfn>EisTitel

De EisTitel wordt ook wel eens de titel van de eis genoemd, en geeft een voor mensen leesbare korte duiding van de inhoud van de eis.

De EisTitel hoeft niet uniek te zijn in het project, daarvoor heeft de eis een URI. Een unieke naam is voor de menselijke lezer vaak wel handig. Soms wordt de EisTitel in applicaties bijvoorbeeld gebruikt bij het visualiseren van de eisenboom. Unieke namen helpen in dat geval.

| Taalbinding                                                                     | Kardinaliteit | Datatype                                               |  Maximaal aantal tekens                                               |
| ------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 56 |
| { .def } |

### <dfn>EisTekst

De EisTekst bevat de voor mensen leesbare inhoud van de eis.
Op dit moment worden eisen in een contract meestal niet voorzien van een voor een systeem leesbare eis, zoals bijvoorbeeld een minimale waarde voor een attribuut van een object. Deze "dataficeringsslag" is buiten scope van dit document, omdat dit een verder gevorderd BIM niveau vraagt en dit document juist bedoelt is als opstap naar uitwisseling van data.

In de EisTekst kan verwezen worden naar een referentiedocument, waar aanvullende eisen in staan die gelden binnen het contract. De URI van dit document wordt dan opgenomen in de kolom Referentiedocument.

| Taalbinding                                                   | Kardinaliteit | Datatype                                               |  Maximaal aantal tekens                                               |
| ------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [rdf:value](http://www.w3.org/1999/02/22-rdf-syntax-ns#value) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 2000  |
| { .def } |

### <dfn>EisToelichting

In deze kolom staat de toelichting op de eistekst

In contracten wordt dit gebruikt om nader te onderbouwen waarom deze eis gesteld wordt.

| Taalbinding                                                           | Kardinaliteit | Datatype                                               |  Maximaal aantal tekens                                               |
| --------------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [skos:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 2000  |
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
* De eis verwijst naar een figuur die van toepassing is.

Instructie voor gebruik: omdat nog niet alle partijen in staat zijn om de data helemaal te verwerken, moet je het document wel in de eistekst noemen. De eistekst is leidend. Een ontvanger van de eisenset kan er ook niet van uit gaan, dat de opdrachtgever dit altijd in weet te vullen. Als in een eistekst naar een referentiedocument wordt verwezen, kan het zijn dat er geen relatie is gemaakt naar het referentiedocument.


| Taalbinding                                           | Kardinaliteit | Datatype                                               |
| ----------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [dct:references](http://purl.org/dc/terms/references) | 0:n           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |

### Enum <dfn>EisType

In deze kolom staat het eistype. De aspecteisen zijn grotendeels overgenomen uit de [[LeidraadSE3]]; de eistypen die aanduiden aan wat voor concept de eis is gesteld zijn aangepast aan de onderwerpen uit deze richtlijn. Dit is een enumeratie.

Bij uitwisseling mag je uitsluitend de onderstaande lijst gebruiken, zonder zelf uitbreidingen te doen. Als elke opdrachtgever een eigen lijst met eistypen en aspecten gebruikt wordt het inrichten van standaard omgevingen voor de verwerking van contracteisen onnodig bemoeilijkt, waarbij bij elk project een aangepaste lijst moet worden gemaakt.

Eistypen:

<div class="issue" data-number="48"></div>

<dl>
<dt><dfn>Informatie-eis
   <dd>Eis gesteld aan een te leveren [=Informatieproduct=]
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Informatie-eis">csw:Informatie-eis</a>
	   
<dt><dfn>Systeemeis
   <dd>Eis gesteld aan een [=FysiekObject=]
   <dd>Een eis die het tot stand komen en gebruiken dan wel toepassen van het geïntegreerde systeem specificeert. Bron: [[LeidraadSE3]]
   <dd>Andere in de sector gebruikte namen van eisen die allemaal tot de Systeemeisen behoren: Functionele eis; Prestatie-eis; Technische eis; Ontwerprandvoorwaarde
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Systeemeis">csw:Systeemeis</a>
	 
<dt><dfn>Proceseis
   <dd>Eis gesteld aan een [=Werkzaamheid=]
   <dd>De beschrijving van het gevraagde geheel van samenhangende of elkaar beïnvloedende activiteiten dat input omzet in output. Bron: [[LeidraadSE3]] 
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Proceseis">csw:Proceseis</a>

<dt><dfn>Functie-eis
   <dd>Eis gesteld aan een [=Functie=]
   <dd>De beschrijving van de gevraagde beoogde werking en/of verrichting van een systeem. Bron: [[LeidraadSE3]]
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Functie-eis">csw:Functie-eis</a>

<dt><dfn>Aspecteis: Betrouwbaarheid
   <dd>De waarschijnlijkheid dat de vereiste functie wordt uitgevoerd onder gegeven omstandigheden gedurende een bepaald tijdsinterval. 
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Betrouwbaarheid">csw:Aspecteis-Betrouwbaarheid</a>
 <dd>Bron: [[LeidraadSE3]]

<dt><dfn>Aspecteis: Beschikbaarheid
   <dd>De waarschijnlijkheid dat de vereiste functie op een willekeurig moment kan worden uitgevoerd onder gegeven omstandigheden.	
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Beschikbaarheid">csw:Aspecteis-Beschikbaarheid</a>
 <dd>Bron: [[LeidraadSE3]]

<dt><dfn>Aspecteis: Onderhoudbaarheid
   <dd>De waarschijnlijkheid dat de activiteiten voor onderhoud kunnen worden uitgevoerd binnen de hiervoor vastgestelde tijden, onder gegeven omstandigheden teneinde de vereiste functie te kunnen (blijven) uitvoeren.
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Onderhoudbaarheid">csw:Aspecteis-Onderhoudbaarheid</a>
 <dd>Bron: [[LeidraadSE3]]

<dt><dfn>Aspecteis: Veiligheid
   <dd>De waarschijnlijkheid dat de vereiste functie en de daarvoor benodigde activiteiten zonder optredend letsel aan personen kan worden vervuld dan wel uitgevoerd en de waarschijnlijkheid dat de integriteit van de functie  en de daaraan verbonden data en datastructuren gewaarborgd blijven van ongewenste beïnvloeding.	   
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Veiligheid">csw:Aspecteis-Veiligheid</a>
 <dd>Bron: [[LeidraadSE3]]

<dt><dfn>Aspecteis: Gezondheid
   <dd>De waarschijnlijkheid dat de vereiste functie en de daarvoor benodigde activiteiten zonder negatieve gezondheidsrisico's voor personen kan worden vervuld dan wel uitgevoerd.
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Gezondheid">csw:Aspecteis-Gezondheid</a>
   <dd>Bron: [[LeidraadSE3]]

<dt><dfn>Aspecteis: Omgeving
   <dd>De waarschijnlijkheid dat de vereiste functie en de daarvoor benodigde activiteiten zonder ongewenste risico's voor de omgeving kunnen wordenvervuld en/of gerealiseerd.	
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Omgeving">csw:Aspecteis-Omgeving</a>    
   <dd>Bron: [[LeidraadSE3]]

<dt><dfn>Aspecteis: Duurzaamheid
   <dd>De waarschijnlijkheid dat de vereiste functie en de daarvoor benodigde activiteiten binnen de hieraan gestelde eisen en PPP (People/Planet/Profit)-doelstellingen kunnen worden gerealiseerd.  
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Duurzaamheid">csw:Aspecteis-Duurzaamheid</a>
   <dd>Bron: [[LeidraadSE3]]

<dt><dfn>Aspecteis: Vormgeving
   <dd>De beschrijving van de gevraagde prestatie ten aanzien van het beeld en het materiaalgebruik met inachtneming van de omgevings- en de gezondheidseisen van het systeem en haar onderdelen.
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Vormgeving">csw:Aspecteis-Vormgeving</a>
   <dd>Bron: Leidraad SE v3

<dt><dfn>Aspecteis: Toekomstvastheid
   <dd>De beschrijving van de gevraagde prestatie van een systeem ten aanzien van de vereiste levensduur van het systeem (als functie en als object) en haar onderdelen.	    
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Toekomstvastheid">csw:Aspecteis-Toekomstvastheid</a>
   <dd>Bron: [[LeidraadSE3]]

<dt><dfn>Aspecteis: Sloopbaarheid
   <dd>De waarschijnlijkheid dat de vereiste functie aan het einde van de levensduur op beheerste wijze kan worden teruggebracht tot minimaal secundaire grondstoffen en met inachtneming van de overige aspecten.  
   <dd><a href="https://data.crow.nl/contractspecificaties/id/Aspecteis-Sloopbaarheid">csw:Aspecteis-Sloopbaarheid</a>
   <dd>Bron: [[LeidraadSE3]]
</dd></dl>

| Taalbinding                                                                       | Kardinaliteit | Datatype                                                             |
| --------------------------------------------------------------------------------- | ------------- | -------------------------------------------------------------------- |
| [nen2660:requirementTopicType](https://w3id.org/nen2660/def#requirementTopicType) | 0:n           | [cs:EisType](https://data.crow.nl/contractspecificaties/def/EisType) |
| { .def } |

### Enum <dfn>EisStatus

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

### <dfn>EisStatusOnderbouwing

In deze kolom staat een toelichting op de status van de eis.
Gebruikers willen de reden van vervallen toevoegen aan de eis, zodat de status onderbouwd is.

| Taalbinding                                                                                | Kardinaliteit | Datatype                                               |  Maximaal aantal tekens  |
| ------------------------------------------------------------------------------------------ | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [cs:statusOnderbouwing](https://data.crow.nl/contractspecificaties/def/statusOnderbouwing) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 2000 |
| { .def } |


### <dfn>VerificatievoorschriftURI

De URI is de unieke identifier voor het Verificatievoorschrift in deze fase, in dit project. Zie [URI conform W3C](https://www.w3.org/wiki/URI).
Voor het opstellen van URI's heeft de [[NEN_2660_2_2022]] een URI-strategie die je moet volgen.


Het Verificatievoorschrift geeft de <i>in het contract voorgeschreven</i> verificatiemethode voor de eis (een type uit een lijst plus een vrij tekstveld met toelichting), per object en per fase waarin de verificatie wordt uitgevoerd.  

Een eis kan meerdere Verificatievoorschriften kennen, elk in een eigen fase. Een Verificatievoorschrift geldt voor één fase. Indien in een andere fase precies dezelfde verificatie wordt uitgevoerd, zijn er twee Verificatievoorschriften.  

| Taalbinding | Kardinaliteit | Datatype                                               |
| ----------- | ------------- | ------------------------------------------------------ |
| n.v.t.      | 1:1 ten opzichte van een Verificatievoorschrift       | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def } |


### <dfn>VerificatieheeftOnderwerp

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


### Enum <dfn>VerificatieMethode

In deze kolom staat de methode waarmee de eis geverifieerd moet worden. Een eisverificatiemethode is een eigenschap van een Verificatievoorschrift. De eisverificatiemethode is een enumeratie, dat wil zeggen dat de gebruiker moet kiezen uit een lijst met van tye voren vastgestelde verificatiemethoden. Het is niet verplicht om een verificatiemethode voor te schrijven bij een Verificatievoorschrift, je kunt dit ook aan de opdrachtnemer laten.

Bij uitwisseling mag uitsluitend de onderstaande lijst gebruikt worden bij contractspecificaties, zonder zelf uitbreidingen te doen. Als elke opdrachtgever een eigen lijst met eistypen en aspecten gebruikt wordt het inrichten van standaard omgevingen voor de verwerking van contracteisen onnodig bemoeilijkt, waarbij bij elk project een aangepaste lijst moet worden gemaakt.

Classificatie volgens:

1. [[NEN_EN_ISO_9000_2015]]
2. [[ISO_IEC_IEEE_29148_2018]] Systems and software engineering — Life cycle processes — Requirements engineering
4. [[LeidraadSE2]]; deze leidraad is niet meer actueel, in [[LeidraadSE3]] worden geen verificatiemethoden meer benoemd die in versie 2 wel stonden.

<div class="issue" data-number="63"></div>

<dl>
<dt><dfn>Vaststellen
	<dd>Het vaststellen van verificatiecriteria waarbij een of meer kenmerken en hun karakteristieke waarden worden bepaald als basis voor de verificatie.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Vaststellen">csw:Vaststellen</a> 

<dt><dfn>Beoordelen
	<dd>Op basis van deskundigheid vaststellen van de geschiktheid, toereikendheid of doeltreffendheid van een object voor het bereiken van de gewenste functionaliteit en kwaliteit.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Beoordelen">csw:Beoordelen</a>

<dt><dfn>Monitoren
	<dd>Het systematisch en periodiek verzamelen van de functionaliteits- of kwaliteitsstatus van een systeem, een proces, een product, een dienst of een activiteit. 
	<dd>Voorbeelden: zettingsmetingen met sensoren, monitoring van draaiuren voor optimale vervanging.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Monitoren">csw:Monitoren</a>
	<dd>Bron definitie: <a href="https://www.encyclo.nl/begrip/monitoren">Encyclo.nl:Monitoren</a>

<dt><dfn>Meten
	<dd>Het uitdrukken van een waargenomen grootheid in een getal met een relevante eenheid die vergeleken kan worden met andere waardes van eenzelfde grootheid. Hiervoor kunnen meetinstrumenten worden gebruikt. Meting is echter niet beperkt tot natuurkundige grootheden, maar strekt zich uit tot een kwantitatieve beschrijving van de gehele werkelijkheid. Metingen zijn meestal kwantitatieve waarnemingen: het resultaat wordt in een getalwaarde en een eenheid uitgedrukt. 
	<dd>Voorbeelden: luchtsnelheidmetingen in tunnels, kalenderen van heipalen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Meten">csw:Meten</a>
	<dd>Bron definitie: <a href="https://nl.wikipedia.org/wiki/Meten">Wikipedia:Meten</a>

<dt><dfn>Keuren
	<dd>Een formele en gedisciplineerde beoordelingstechniek waarbij een product of dienst wordt onderzocht op kwaliteit en functionaliteit. Het gebruik van controlelijsten (checklists) is typisch voor de vorm van beoordeling. 
	<dd>Voorbeelden: een ingangs- en uitgangscontrole.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Keuren">csw:Keuren</a>
	<dd>Bron definitie: <a href="https://www.encyclo.nl/begrip/keuring">Encyclo.nl:Keuren</a>

<dt><dfn>Beproeven
	<dd>Het door middel van gebruik vaststellen dat de gewenste functionaliteit en kwaliteit worden gehaald.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Beproeven">csw:Beproeven</a>

<dt><dfn>Evalueren
	<dd>Het verzamelen, interpreteren en presenteren van informatie teneinde de waarde van een resultaat of proces te bepalen. Hierbij kan het gaan om het waarderen van de resultaten van personen of bedrijven, maar ook om het waarderen van alternatieve oplossingen. 
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Evalueren">csw:Evalueren</a>
	<dd>Bron definitie: <a href="https://nl.wikipedia.org/wiki/Evaluatie">Wikipedia:Evalueren</a>

<dt><dfn>Analyseren
    <dd>het ontleden van een bepaald (denk)object tot de constituerende elementen. Het is een wetenschappelijke methode om data, objecten en materie systematisch te onderzoeken. 
	<dd>Voorbeelden: Haalbaarheidsanalyse, kosten-batenanalyse, materiaalanalyse.
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Analyse">csw:Analyse</a>

<dt><dfn>Berekenen
    <dd>Het uitvoeren 
	<dd>Voorbeeldensterkteberekeningen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Berekening">csw:Berekening</a>

<dt><dfn>Auditen
	<dd>Audit van bestaande kwaliteitssystemen en -processen (o.a. Technical Inspection Services
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Auditen">csw:Auditen</a>

<dt><dfn>Demonstreren
	<dd>o.a. presentatie van de functionaliteiten van een bestaand systeem
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Demonstratie">csw:Demonstratie</a>

<dt><dfn>Document beoordelen
	<dd>o.a. documentinspecties, reviews, toetsen, ontwerpateliers
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Documentbeoordeling">csw:Documentbeoordeling</a>

<dt><dfn>Modellering
	<dd>o.a. prestatiemodellen van beschikbaarheid, verkeersmodellen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Modellering">csw:Modellering</a>

<dt><dfn>Simulaties
	<dd>o.a. dienstregelingsimulatie
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Simulaties">csw:Simulaties</a>

<dt><dfn>Referentie
	<dd>o.a. gebruik van gecertificeerde producten
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Referentie">csw:Referentie</a>

<dt><dfn>Testen
	<dd>haalbaarheidstesten, FIT, FAT, SIT, SAT
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Testen">csw:Testen</a>

<dt><dfn>Factory Integration Test
	<dd>o.a. hydraulische en mechanische installaties integraal testen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/FactoryIntegrationTest">csw:FactoryIntegrationTest</a>

<dt><dfn>Factory Acceptance Test
	<dd>o.a. cameratesten in fabrieksopstelling
	<dd><a href="https://data.crow.nl/contractspecificaties/id/FactoryAcceptanceTest">csw:FactoryAcceptanceTest</a>

<dt><dfn>Site Integration Test
	<dd>o.a. interactietesten tussen installatie- en besturingssystemen
	<dd><a href="https://data.crow.nl/contractspecificaties/id/SiteIntegrationTest">csw:SiteIntegrationTest</a>

<dt><dfn>Site Acceptance Test
	<dd>o.a. calamiteitenoefeningen in bijzijn van hulpdiensten
	<dd><a href="https://data.crow.nl/contractspecificaties/id/SiteAcceptanceTest">csw:SiteAcceptanceTest</a>

<dt><dfn>Schouw
	<dd>o.a. visuele opname van projectlocatie
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Schouw">csw:Schouw</a>

<dt><dfn>Inspectie (cs)
	<dd>o.a. Arbo-inspecties, pompkelderinspecties
	<dd><a href="https://data.crow.nl/contractspecificaties/id/Inspectie">csw:Inspectie</a>
</dd></dl>

| Taalbinding                                                                                | Kardinaliteit | Datatype                                                                                        |
| ------------------------------------------------------------------------------------------ | ------------- | ----------------------------------------------------------------------------------------------- |
| [cs:verificationMethod](https://data.crow.nl/contractspecificaties/def/verificationMethod) | 0:1  tov een Verificatievoorschrift           | [cs:VerificationMethodeType](https://data.crow.nl/contractspecificaties/def/verificationMethod) |
| { .def } |

### Enum <dfn>VerificatieFase

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


### <dfn>VerificatieMoment
De opdrachtgever gebruikt deze fase, om vast te leggen wanneer een eis geverifieerd dient te worden. De voorwaarde om een Verificatiemoment te kunnen vastleggen is het bijvoegen van een Verificatievoorschrift.

| Taalbinding                                                           | Kardinaliteit | Datatype                                               |  Maximaal aantal tekens                                               |
| --------------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [skos:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) | 0:1   tov een Verificatievoorschrift          | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 255 |
| { .def } |

<aside class="note" title="Standaard fasen / momenten">
Er zijn verschillende richtlijnen en afspraken in Nederland die werken met een lijst met oplevermomenten of andere momenten/fasen in een project. Al naar gelang de context, kan dus een standaard gebruikt worden. Op dit moment is niet duidelijk, of dit kan leiden tot één standaard, of dat voor verschillende toepassingen verschillende lijsten beschikbaar zijn. Een paar van de genoemde standaarden:
<ul>
<li>In de DNR (De Nieuwe Regelening) is een <a href="https://bna.nl/standaardtaakbeschrijving-stb">standaardtaakbeschrijving</a> (STB) beschikbaar waarin een recentere fase opdeling wordt gehanteerd. Er is een herziening van de DNR in de maak (Zie <a href="https://www.nlingenieurs.nl/nieuws/consultatie-van-de-vernieuwde-regeling-dnr2022-van-start/">dit nieuwsbericht</a>) en volgens <a href="https://www.stiion.nl/de-nieuwe-regeling-dnr/#:~:text=De%20laatste%20versie%20van%20de%20STB%20dateert%20van%202014%20(STB%202014).%20Er%20wordt%20gewerkt%20aan%20een%20update%20van%20de%20STB%20waarbij%20onder%20andere%20aandacht%20is%20voor%20het%20digitale%20ontwerp%2D%20en%20bouwproces">dit nieuwsbericht</a> wordt gewerkt aan een update van de STB.</li>
<li>Bouwend Nederland heeft een structuur ontwikkeld volgens <a href="https://www.bouwendnederland.nl/actueel/nieuws/23671/vib-ontwikkelt-branche-brede-eenduidige-structuur-voor-ontwerpfasen">dit nieuwsbericht</a></li>
</ul>
</aside>


### <dfn>VerificatieToelichting

In deze kolom staat de toelichting op het Verificatievoorschrift.

In contracten wordt dit gebruikt om nader toe te lichten waarom dit Verificatievoorschrift gevraagd wordt.

| Taalbinding                                                           | Kardinaliteit | Datatype                                               |  Maximaal aantal tekens                                               |
| --------------------------------------------------------------------- | ------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [skos:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) | 0:1  tov een Verificatievoorschrift           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) | 2000 |
| { .def } |


<div class="issue" data-number="37"></div>
