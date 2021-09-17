# Eisentabel


Voorstel is om de volgende tabel te gebruiken voor de eisen en verificatiemethoden. Op de tweede regel staat de vertaling / binding naar de NEN 2660.


Een verificatiemethode is ook een eis; het onderwerp van de verificatiemethode is een andere eis. In de eisentabel is het verschil niet meteen duidelijk, voor leesbaarheid kan de verificatiemethode direct onder de eis worden gezet in de Eisentabel.


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
</th></tr>
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
</td></tr>
</table>

Over unieke naam van de eis: gebruikers geven de voorkeur aan een unieke identifier over projecten heen, zodat een eis uit een bron (eisenbibliotheek) herkend kan worden


## Eisen en Verificatiemethoden

Een eis/verificatiemethode heeft een vertaling / binding naar de NEN 2660 als InformationObject


## Verificatiemethoden
Gebruikelijk is in contracten het aangeven van een of meer verificatiemethodes, eventueel met een of meer verificatiemomenten. 

De vertaling / binding van een verificatiemethode- en moment naar NEN 2660 is nog niet bekend. 

[issue 15](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/15)


## Details Eisentabel

### URI
Met URI wordt bedoeld: de unieke naam van de eis. Zie [URI conform W3C](https://www.w3.org/wiki/URI). 

De URI is unieke naam voor de eis binnen het project.
Bij de eisen kan verwezen worden naar een eis in een eisenbibliotheek onder "Bron".

Bij de eisen kan de URI ook de verwijzing zijn naar de eis in een bibliotheek; dan mogen de overige kolommen niet zijn aangepast en ook geen


### Code
In de code kan een in het project gebruikte code staan, die heeft mogelijk maakt in een gesprek naar de eis te verwijzen, zonder de volledige URI te hoeven benoemen. 



### Naam
De naam is de voor mensen leesbare naam van de eis. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.



### Tekst
Bij "Tekst" staat de eistekst



### HeeftDeel
Bij HeeftDeel kan een hiërarchie worden aangegeven van de eisenboom zoals gebruikelijk in contracten. Een eis kan meerdere onderliggende eisen hebben, er komen dan meerdere regels met dezelfde eis voor in de eisentabel. 



### Ernst
De ernst van een eis (nen2660:voorwaardeErnstType) kan conform NEN 2660 de volgende lijst zijn:
* Wens
* Eis

Wordt door partijen het onderscheid maken tussen klanteis en systeemeis gewenst?

### Bron
De bron van een eis (nen2660:voorwaardeBronType) kan conform NEN 2660 de volgende lijst zijn:
* PerDefinitie
* DoorKlant
* DoorWetOfRegelgeving
* DoorSector

Gebruikers geven aan, hier liever een verwijzing te plaatsen naar één van deze zaken:
1. De URI van de gebruikte eis uit een bibliotheek (indien deze niet gewijzigd is)
2. De URI van een brondocument met herkomst van de eis - reden dat ook een documententabel gewenst wordt door gebruikers.
3. De URI van een van toepassing zijnd document - Strikt genomen niet de bron; moet dit in een andere kolom worden opgenomen?


[Issue 20](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/20)


### Specificeert
Hier staat de URI van het concept waar de eis aan gesteld wordt. Een eis kan aan meerdere concepten gesteld worden, er komen dan meerdere regels met dezelfde eis voor in de eisentabel. 


De vertaling / binding van specificeert naar NEN 2660 is nog niet bekend. 

[Issue 18](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/18)

Merk op, dat verwijzing naar de URI de tabel minder makkelijk leesbaar maakt voor de mens. Indien hier ook de naam van het concept zou worden toegevoegd, creeert dit dubbelingen met de onderwerpentabel en daarom mogelijk fouten. Daarom wordt alleen de URI gebruikt.


### Toelichting op de eistekst
Een contractuele eis kan onderbouwd worden met een toelichting.

De vertaling / binding van toelichting naar NEN 2660 is nog niet bekend. 

[Issue 17]https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/17


### Type

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

Bij verificatiemethoden: voorstel om toe te passen de lijst uit NEN-EN-ISO 9001:2015
* <a>Vaststellen</a>
* <a>Beoordelen</a>
* <a>Monitoren</a>
* <a>Meten</a>
* <a>Keuren</a>
* <a>Beproeven</a>
* <a>Evalueren</a>














