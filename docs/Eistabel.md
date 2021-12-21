# Eisentabel

De eisentabel wordt gebruikt voor de eisen. Bij elke kolom is aangegeven wat de vertaling/binding is naar linked data standaarden, hoe vaak deze waarde ingevuld mag worden per eis ("kardinaliteit") en een beschrijving.

Een eis is een [InformationObject](https://bimloket.github.io/nen2660/def#InformationObject) volgens NEN 2660.

<table class="wikitable" style="text-align:left; valign:top">
<tr>
<th> URI
</th>
<th> Code
</th>
<th> Naam
</th>
<th> Tekst
</th>
<th> Toelichting
</th>
<th> Verificatiemethode
</th>
<th> ToelichtingVerificatie
</th>
<th> heeftDeel
</th>
<th> Bron
</th>
<th> Referentiedocument
</th>
<th> Locatie in document
</th>
<th> specificeert
</th>
<th> Eistype
</th>
<th> Eigenaar
</th>
<th> Fase
</th>
<th> Status
</th>
<th> Onderbouwing status
</th>
</tr>
<tr>
<td> In deze kolom staat de unieke naam (URI) van de eis. </td>
<td> In deze kolom staat de code of het nummer van de eis. </td>
<td> In deze kolom staat de de naam oftewel de titel van de eis. </td>
<td> In deze kolom staat de eistekst. </td>
<td> In deze kolom staat de toelichting op de eis. </td>
<td> In deze kolom staat de verificatiemethode bij de eis </td>
<td> In deze kolom staat de toelichting op de verificatiemethode bij de eis. </td>
<td> In deze kolom staat de URI van een onderliggende eis. </td>
<td> In deze kolom wordt aangegeven wat de bron van de eis is. </td>
<td> In deze kolom wordt aangegeven in welk gerefereerd document meer eisen staan. </td>
<td> In deze kolom wordt aangegeven op welke locatie in een document de eis voorkomt. </td>
<td> In deze kolom staat de URI van het Onderwerp van de eis. </td>
<td> In deze kolom staat het eistype. </td>
<td> In deze kolom staat de eigenaar. </td>
<td> In deze kolom staat de fase van de eis. </td>
<td> In deze kolom staat de status van de eis. </td>
<td> In deze kolom staat een toelichting op de status van de eis. </td>
</tr>
<tr>
<td> [URI](https://www.w3.org/wiki/URI) </td>
<td> [skos:notation](https://www.w3.org/2009/08/skos-reference/skos.html#notation) </td>
<td> [skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel) </td>
<td> [rdf:value](https://www.w3.org/TR/rdf-schema/#ch_value) </td>
<td> [skos:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) </td>
<td> [nen2660:verificationMethodType](https://bimloket.github.io/nen2660/def#verificationMethodType) </td>
<td> [skos:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) </td>
<td> [nen2660:hasPart](https://bimloket.github.io/nen2660/term#hasPart) </td>
<td> [rdfs:seeAlso](https://www.w3.org/TR/rdf-schema/#ch_seealso) </td>
<td> [rdfs:seeAlso](https://www.w3.org/TR/rdf-schema/#ch_seealso) </td>
<td> [rdfs:comment](https://www.w3.org/TR/rdf-schema/#ch_comment) </td>
<td> [nen2660:hasRequirement](https://bimloket.github.io/nen2660/def#hasRequirement) </td>
<td> onbekend </td>
<td> [dcmi-terms:rightsHolder](https://dublincore.org/specifications/dublin-core/dcmi-terms/#rightsHolder) </td>
<td> ONBEKEND </td>
<td> [nen2660:hasState](https://bimloket.github.io/nen2660/term#hasState) </td>
<td> [SKOS:note](https://www.w3.org/2009/08/skos-reference/skos.html#note) </td>
</tr>
<tr>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 0:n </td>
<td> 0:n </td>
<td> 0:n </td>
<td> 0:n </td>
<td> 0:n </td>
<td> 0:n </td>
<td> 0:n </td>
<td> 0:n </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
</tr>
</table>


## Voorbeeld eisentabel
<table class="wikitable" style="text-align:left; valign:top">
<tr>
<th> URI
</th>
<th> Code
</th>
<th> Naam
</th>
<th> Tekst
</th>
<th> Toelichting
</th>
<th> Verificatiemethode
</th>
<th> ToelichtingVerificatie
</th>
<th> heeftDeel
</th>
<th> Bron
</th>
<th> Referentiedocument
</th>
<th> Locatie in document
</th>
<th> specificeert
</th>
<th> Eistype
</th>
<th> Eigenaar
</th>
<th> Fase
</th>
<th> Status
</th>
<th> Onderbouwing status
</th></tr>
<tr>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldeisentabel </td>
<td> EIS1099 </td>
<td> Voorbeeldeis </td>
<td> Dit is de tekst van de voorbeeldeis </td>
<td> Dit is de toelichting van de voorbeeldeis, om achtergrond / doel en reden van de eis te kunnen verduidelijken </td>
<td> Documentinspectie </td>
<td> Dit is de toelichting bij de verificatiemethode, om deze verder te kunnen verduidelijken </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldeisentabel </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldbrondocument </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldgerefereerddocument </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldlocatieindocument </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldtabel </td>
<td> Veiligheid </td>
<td> BIM loket </td>
<td> Ontwerp </td>
<td> Vervallen </td>\
<td> Reden van vervallen van eis </td>
</td></tr>
</table>


## Details Eisentabel

### URI

In deze kolom staat de unieke naam (URI) van de eis. Zie [URI conform W3C](https://www.w3.org/wiki/URI). 

De URI is de unieke naam voor de eis binnen het project. Bij de eisen kan verwezen worden naar een eis in een eisenbibliotheek onder "Bron". Daar staat de URI van de eis uit de bibliotheek. Deze URI verwijst naar een openbaar gepubliceerde eis in een bibliotheek, bijvoorbeeld het Provinciaal Contracten Buffet. 

De eis in het project moet een andere URI hebben dan de bron. Het is niet dezelfde eis, want deze wordt toegepast in (gekopieerd naar) een andere context. 

### Code

In deze kolom staat de de naam (spreektaal/projectnummer) van de eis.
Deze meestal eenvoudige en soms logisch genummerde Code maakt het mogelijk om in een gesprek naar de eis te verwijzen, zonder de volledige URI te hoeven benoemen. 



### Naam

In deze kolom staat de de naam oftewel de titel van de eis
De naam is de voor mensen leesbare naam van de eis. Deze naam hoeft niet uniek te zijn in het project, daarvoor heeft de eis een URI, maar een unieke naam is voor de menselijke lezer vaak wel handig.

### Tekst

In deze kolom staat de eistekst. In deze tekst kan verwezen worden naar een referentiedocument, waar aanvullende eisen in staan die gelden binnen het contract. De URI van dit document wordt dan opgenomen in de kolom Referentiedocument.

### Toelichting

In deze kolom staat de toelichting op de eistekst 
In contracten wordt dit gebruikt om nader te onderbouwen waarom deze eis gesteld wordt. 

#### Enum <dfn>`Verificatiemethode`
In deze kolom staat de methode waarmee de eis geverifieerd moet worden. Een verificatiemethode is een eigenschap ('property') van een eis in de NEN2660-2. De eigenschap heeft een enumeratie van de verschillende mogelijke methoden, dat wil zeggen dat de gebruiker een lijst kan opstellen met verificatiemethoden en een waarde uit deze lijst kan gebruiken. 

Bij uitwisseling mag je uitsluitend de onderstaande lijst gebruiken, zonder zelf uitbreidingen te doen. Als elke opdrachtgever een eigen lijst met eistypen en aspecten gebruikt wordt het inrichten van standaard omgevingen voor de verwerking van contracteisen onnodig bemoeilijkt, waarbij bij elk project een aangepaste lijst moet worden gemaakt.

Classificatie volgens: 
1. NEN-EN-ISO 9000:2015 Kwaliteitsmanagementsystemen - Grondbeginselen en verklarende woordenlijst
2. ISO/IEC/IEEE 29148:2018 Systems and software engineering — Life cycle processes — Requirements engineering
3. [Leidraad SE (V2 en 3)](https://www.leidraadse.nl/assets/files/downloads/LeidraadSE/V2/LeidraadSE_def_lowres.pdf)

| Verificatiemethode    | Omschrijving                                                                | Bron | 
| --------------------- | --------------------------------------------------------------------------- | ---- |
| Vaststellen           | Activiteit om een of meer kenmerken en hun karakteristieke waarden te achterhalen. | NEN-EN-ISO 9001:2015 | 
| Beoordelen            | Vaststelling van de geschiktheid, toereikendheid of doeltreffendheid van een object voor het bereiken van vastgestelde doelstellingen. | NEN-EN-ISO 9001:2015 | 
| Monitoren             | Vaststellen van de status van een systeem, een proces, een product, een dienst of een activiteit. Bijvoorbeeld zettingen, monitoring van draaiuren t.b.v. optimale vervanging | NEN-EN-ISO 9001:2015 | 
| Meten                 | Proces om een waarde vast te stellen. | NEN-EN-ISO 9001:2015 | 
| Keuren                | Vaststelling van conformiteit met gespecificeerde eisen. Bijvoorbeeld keuring, ingangs- en uitgangscontrole| NEN-EN-ISO 9001:2015 |
| Beproeven             | Vaststellen volgens eisen voor een specifiek beoogd€ gebruik of toepassing. | NEN-EN-ISO 9001:2015 |
| Evalueren             | Beoordelen van de voortgang die behaald is met betrekking tot het bereiken van de doelen. | NEN-EN-ISO 9001:2015 | {.data} |
| Analyse               | o.a. haalbaarheidsanalyse, kosten-batenanalyse | Leidraad SE v2 | 
| Berekening            | o.a. sterkteberekeningen | Leidraad SE v2 | 
| Auditen               | Audit van bestaande kwaliteitssystemen en -processen (o.a. Technical Inspection
Services) | Leidraad SE v2 | 
| Demonstratie          | o.a. presentatie van de functionaliteiten van een bestaand systeem | Leidraad SE v2 | 
| Documentbeoordelingen | o.a. documentinspecties, reviews, toetsen, ontwerpateliers | Leidraad SE v2 |
| Modellering             | o.a. prestatiemodellen van beschikbaarheid, verkeersmodellen | Leidraad SE v2 |
| Simulaties             | o.a. dienstregelingsimulatie | Leidraad SE v2 |  

| Referentie            | o.a. gebruik van gecertificeerde producten | Leidraad SE v2 | 
| Testen            | haalbaarheidstesten, FIT, FAT, SIT, SAT | Leidraad SE v2 | 
| Factory Integration Test | o.a. hydraulische en mechanische installaties integraal
	 testen | Leidraad SE v2 | 
| Factory Acceptance Test | o.a. cameratesten in fabrieksopstelling | Leidraad SE v2 | 
| Site Integration Test | o.a. interactietesten tussen installatie- en besturingssystemen | Leidraad SE v2 |
| Site Acceptance Test  | o.a. calamiteitenoefeningen in bijzijn van hulpdiensten) | Leidraad SE v2 |
| Meten             | o.a. luchtsnelheidmetingen in tunnels, kalenderen van heipalen | Leidraad SE v2 | 
| Schouw | o.a. visuele opname van projectlocatie | Leidraad SE v2 |
| Inspecties| o.a. Arbo-inspecties, pompkelderinspecties | Leidraad SE v2 | 
| {.data def}  
 
  

### ToelichtingVerificatie

In deze kolom staat de toelichting op de verificatiemethode.
In contracten wordt dit gebruikt om nader toe te lichten waarom deze verificatiemethode gevraagd wordt. 

### heeftDeel

In deze kolom staat de URI van een onderliggende eis. 
Hiermee kan een hiërarchie worden aangegeven van de eisenboom zoals gebruikelijk in contracten. Een eis kan meerdere onderliggende eisen hebben, er komen dan meerdere regels met dezelfde eis voor in de eisentabel. 

### Bron

De bron van de eis kan naart twee zaken verwijzen: 
1. De URI van de gebruikte eis uit een bibliotheek (indien deze niet gewijzigd is). Deze URI verwijst naar een openbaar gepubliceerde eis in een bibliotheek, bijvoorbeeld het Provinciaal Contracten Buffet. De eis in het project moet een andere URI hebben dan de bron. Het is niet dezelfde eis, want deze wordt toegepast in (gekopieerd naar) een andere context. 
2. De URI van een brondocument met herkomst van de eis. Deze uri verwijst naar een document in de documententabel.

### Referentiedocument

Als in de eistekst wordt verwezen naar een referentiedocument, staat in deze kolom de URI van het gerefereerde document. Deze uri verwijst naar een document in de documententabel.

### Locatie in document

Als zowel een pdf (voor mensen leesbare versie) als een dataset met eisen worden meegenomen, dan staat in deze kolom de URI die verwijst naar een paragraaf in een document in de documententabel.

### Specificeert

In deze kolom staat de URI van het Onderwerp van de eis. Een eis kan aan meerdere Onderwerpen gesteld worden, er komen dan meerdere regels met dezelfde eis voor in de eisentabel. 

Merk op, dat verwijzing naar de URI de tabel minder makkelijk leesbaar maakt voor de mens. Indien hier ook de naam van het concept zou worden toegevoegd, creeert dit dubbelingen met de onderwerpentabel en daarom mogelijk fouten. Daarom wordt alleen de URI gebruikt.

### Type
In deze kolom staat het eistype.

Bij uitwisseling mag je uitsluitend de onderstaande lijst gebruiken, zonder zelf uitbreidingen te doen. Als elke opdrachtgever een eigen lijst met eistypen en aspecten gebruikt wordt het inrichten van standaard omgevingen voor de verwerking van contracteisen onnodig bemoeilijkt, waarbij bij elk project een aangepaste lijst moet worden gemaakt. 

Eistypen:
* <a>Functie-eis</a> 
* <a>Proceseis</a>
* <a>Systeemeis</a>
* <a>Informatie-eis</a>
* <a>Aspecteis: Betrouwbaarheid</a>
* <a>Aspecteis: Beschikbaarheid</a>
* <a>Aspecteis: Onderhoudbaarheid</a>
* <a>Aspecteis: Veiligheid</a>
* <a>Aspecteis: Gezondheid</a>
* <a>Aspecteis: Omgeving</a>
* <a>Aspecteis: Duurzaamheid</a>
* <a>Aspecteis: Vormgeving</a>
* <a>Aspecteis: Toekomstvastheid</a>
* <a>Aspecteis: Sloopbaarheid</a>

### Eigenaar

In deze kolom staat een eigenaar van de eis (naam natuurlijk persoon en/of organisatie).

### Fase

In deze kolom staat de fase van de eis of verificatiemethode. Hierbij worden de volgende fasen onderscheiden:
* Ontwerpfase
* Bouwfase
* Beheerfase
* Sloopfase

### Status

In deze kolom staat de status van de eis. Voor contractspecificaties geldt dat de status één van deze twee zaken is: actueel of vervallen. 
Doel is om wijzigingen door een Nota van Inlichtingen of een contractuele wijziging in de eisenset te kunnen opnemen en met elkaar uit te wisselen.

### Onderbouwing status

In deze kolom staat een toelichting op de status van de eis.
Gebruikers willen de reden van vervallen toevoegen aan de eis, zodat de status onderbouwd is.
