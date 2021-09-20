# Eisentabel

Voorstel is om de volgende tabel te gebruiken voor de eisen en verificatiemethoden. Op de tweede regel staat een korte toelichting; op de derde regel de vertaling / binding naar de NEN 2660.


Een verificatiemethode is ook een eis; het onderwerp van de verificatiemethode is een andere eis. In de eisentabel is het verschil niet meteen duidelijk, voor leesbaarheid kan de verificatiemethode direct onder de eis worden gezet in de Eisentabel.

Een eis/verificatiemethode heeft een vertaling / binding naar de NEN 2660 als InformationObject


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
<th> heeftDeel
</th>
<th> Ernst
</th>
<th> Bron
</th>
<th> Specificeert
</th>
<th> Toelichting
</th>
<th> Eistype
</th>
<th> Initiator
</th>
<th> Fase
</th>
<th> Status
</th>
<th> Onderbouwing status
</th></tr>
<tr>
<td> In deze kolom staat de unieke naam (URI) van de eis of verificatiemethode. </td>
<td> In deze kolom staat de code of het nummer van de eis of verificatiemethode. </td>
<td> In deze kolom staat de de naam oftewel de titel van de eis of verificatiemethode. </td>
<td> In deze kolom staat de eistekst of een nadere detaillering van de verificatiemethode. </td>
<td> In deze kolom staat de URI van een onderliggende eis. </td>
<td> In deze kolom wordt aangegeven, of het een 'wens' of een 'eis' betreft. </td>
<td> In deze kolom wordt aangegeven wat de bron van de eis of verificatiemethode is. </td>
<td> In deze kolom staat de URI van het Onderwerp van de eis of de verificatiemethode. </td>
<td> In deze kolom staat de toelichting op de eis of de verificatiemethode. </td>
<td> In deze kolom staat het eistype of het type verificatiemethode. </td>
<td> In deze kolom staat de initiator van de eis of de verificatiemethode. </td>
<td> In deze kolom staat de fase van de eis of verificatiemethode. </td>
<td> In deze kolom staat de status van de eis of de verificatiemethode. </td>
<td> In deze kolom staat een toelichting op de status van de eis of de verificatiemethode. 
</td></tr>
<tr>
<td> [URI](https://www.w3.org/wiki/URI) </td>
<td> skos:Notation </td>
<td> skos:prefLabel </td>
<td> nen2660:heeftVoorwaardeSpecificatie </td>
<td> nen2660:heeftDeel </td>
<td> nen2660:voorwaardeErnstType </td>
<td> nen2660:voorwaardeBronType </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
</td></tr>
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
<th> heeftDeel
</th>
<th> Ernst
</th>
<th> Bron
</th>
<th> Specificeert
</th>
<th> Toelichting
</th>
<th> Eistype
</th>
<th> Initiator
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
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldeisentabel </td>
<td> wens </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldeisentabel </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldtabel </td>
<td> Dit is de toelichting van de voorbeeldeis, om achtergrond / doel en reden van de eis te kunnen verduidelijken </td>
<td> Veiligheid </td>
<td> BIM loket </td>
<td> Ontwerp </td>
<td> Vervallen </td>\
<td> Reden van vervallen van eis </td>
</td></tr>
<tr>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldeisentabel </td>
<td> VER1099 </td>
<td> Voorbeeld verificatiemethode </td>
<td> Dit is het verificatievoorschrift </td>
<td>  </td>
<td>  </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldeisentabel </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldeisentabel </td>
<td> </td>
<td> </td>
<td> Ontwerp </td>
<td> BIM loket </td>
<td> </td>
<td> </td>
</td></tr>
</table>


## Details Eisentabel

### URI
In deze kolom staat de unieke naam (URI) van de eis. Zie [URI conform W3C](https://www.w3.org/wiki/URI). 

De URI is unieke naam voor de eis binnen het project. 
Bij de eisen kan verwezen worden naar een eis in een eisenbibliotheek onder "Bron". 

Bij de eisen kan de URI ook de verwijzing zijn naar de eis in een bibliotheek; dan mogen de overige kolommen niet zijn aangepast en er ook geen extra informatie zijn toegevoegd. 

[Issue 23](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/23)


### Code
In deze kolom staat de de naam (spreektaal/projectnummer) van de eis.
Deze meestal eenvoudige en soms logisch genummerde Code maakt het mogelijk om in een gesprek naar de eis te verwijzen, zonder de volledige URI te hoeven benoemen. 



### Naam
In deze kolom staat de de naam oftewel de titel van de eis
De naam is de voor mensen leesbare naam van de eis. Deze naam hoeft niet uniek te zijn in het project, daarvoor heeft de eis een URI, maar een unieke naam is voor de menselijke lezer vaak wel handig.



### Tekst
In deze kolom staat de eistekst.
De eistekst kan een link of URI bevatten van een van toepassing zijnd document. Dit document wordt dan opgenomen in de Documententabel.



### HeeftDeel
In deze kolom staat de URI van een onderliggende eis. 
Hiermee kan een hiërarchie worden aangegeven van de eisenboom zoals gebruikelijk in contracten. Een eis kan meerdere onderliggende eisen hebben, er komen dan meerdere regels met dezelfde eis voor in de eisentabel. 



### Ernst
In deze kolom wordt aangegeven, of het een 'wens' of een 'eis' betreft.
De ernst van een eis (nen2660:voorwaardeErnstType) kan conform NEN 2660 de volgende lijst zijn:
* Wens
* Eis

Wordt door partijen het onderscheid maken tussen klanteis en systeemeis gewenst?

[Issue 26](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/26)

### Bron
In deze kolom wordt aangegeven wat de bron van de eis is. Volgens de NEN 2660 kan dit uitsluitend de volgende lijst zijn:
* PerDefinitie
* DoorKlant
* DoorWetOfRegelgeving
* DoorSector

Gebruikers geven aan, hier liever een verwijzing te plaatsen naar één van deze zaken:
1. De URI van de gebruikte eis uit een bibliotheek (indien deze niet gewijzigd is)
2. De URI van een brondocument met herkomst van de eis - reden dat ook een documententabel gewenst wordt door gebruikers.


Deze plek is niet de locatie voor de URI van een van toepassing zijnd document. Daar wordt naar verwezen in de eistekst zelf.


[Issue 20](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/20)


### Specificeert
In deze kolom staat de URI van het Onderwerp van de eis. Een eis kan aan meerdere Onderwerpen gesteld worden, er komen dan meerdere regels met dezelfde eis voor in de eisentabel. 


De vertaling / binding van specificeert naar NEN 2660 is nog niet bekend. 

[Issue 18](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/18)

Merk op, dat verwijzing naar de URI de tabel minder makkelijk leesbaar maakt voor de mens. Indien hier ook de naam van het concept zou worden toegevoegd, creeert dit dubbelingen met de onderwerpentabel en daarom mogelijk fouten. Daarom wordt alleen de URI gebruikt.


### Toelichting op de eistekst
In deze kolom staat de toelichting op de eis. 
In contracten wordt dit gebruikt om nader te onderbouwen waarom deze eis gesteld wordt. 

De vertaling / binding van toelichting naar NEN 2660 is nog niet bekend. 

[Issue 17](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/17)


### Type
In deze kolom staat het eistype of het type verificatiemethode.
Bij eisen: voorstel om toe te passen de lijst uit de [Leidraad Systems Engineering versie 3](https://www.leidraadse.nl/assets/files/downloads/LeidraadSE/V3/Leidraad_V3_SE_web.pdf):

* <a>Topeis</a> (systeemeis?)
* <a>Proceseis</a>
* <a>Functieeis</a>
* <a>Aspecteis</a>
* <a>Betrouwbaarheid</a>
* <a>Beschikbaarheid</a>
* <a>Onderhoudbaarheid</a>
* <a>Veiligheid</a>
* <a>Gezondheid</a>
* <a>Omgeving</a>
* <a>Duurzaamheid</a>
* <a>Vormgeving</a>
* <a>Toekomstvastheid</a>
* <a>Sloopbaarheid</a>

Bij verificatiemethoden: voorstel om toe te passen de lijst uit NEN-EN-ISO 9000:2015 Kwaliteitsmanagementsystemen - Grondbeginselen en verklarende woordenlijst
* <a>Vaststellen</a>
* <a>Beoordelen</a>
* <a>Monitoren</a>
* <a>Meten</a>
* <a>Keuren</a>
* <a>Beproeven</a>
* <a>Evalueren</a>

[Issue 24](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/24)

### Initiator
In deze kolom staat de initiator van de eis (naam natuurlijk persoon en/of organisatie).

De vertaling / binding van initiator naar NEN 2660 is nog niet bekend. 

[Issue 21](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/21)


### Fase
In deze kolom staat de fase van de eis of verificatiemethode.

De vertaling / binding van fase naar NEN 2660 is nog niet bekend. 

[issue 15](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/15)


### Status
In deze kolom staat de status van de eis.
Gebruikers willen de status toevoegen aan de eis, zoals "actueel" of vervallen", bijvoorbeeld om wijzigingen door een Nota van Inlichtingen of een contractuele wijziging in de eisenset te kunnen opnemen en met elkaar uit te wisselen.

De vertaling / binding van status naar NEN 2660 is nog niet bekend. 


### Onderbouwing status
In deze kolom staat een toelichting op de status van de eis.
Gebruikers willen de reden van vervallen toevoegen aan de eis, zodat de status onderbouwd is.

De vertaling / binding van de onderbouwing van de status naar NEN 2660 is nog niet bekend. 

[Issue 22](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/22)














