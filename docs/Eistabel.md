# Eisentabel


Voorstel is om de volgende tabel te gebruiken voor de eisen. Op de tweede regel staat de vertaling / binding naar de NEN 2660.


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
<th> heeftDeel
</th>
<th> Ernst
</th>
<th> Bron
</th>
<th> Specificeert
</th></tr>
<tr>
<td> [URI](https://www.w3.org/wiki/URI) </td>
<td> skos:Notation </td>
<td> skos:prefLabel </td>
<td> nen2660:heeftVoorwaardeSpecificatie </td>
<td> ONBEKEND </td>
<td> nen2660:heeftDeel </td>
<td> nen2660:voorwaardeErnstType </td>
<td> nen2660:voorwaardeBronType </td>
<td> ONBEKEND </td>
</td></tr>
</table>

Over unieke naam van de eis: gebruikers geven de voorkeur aan een unieke identifier over projecten heen, zodat een eis uit een bron (eisenbibliotheek) herkend kan worden

## Eisen
Een eis heeft een vertaling / binding naar de NEN 2660 als InformationObject


## Verificatiemethode
Een verificatiemethode is ook een eis; het onderwerp van de verificatiemethode is een andere eis. In de eisentabel is het verschil niet meteen duidelijk, voor leesbaarheid kan de verificatiemethode direct onder de eis worden gezet in de Eisentabel.

Een verificatiemethode heeft een vertaling / binding naar de NEN 2660 als InformationObject

## Verificatiemethoden
Gebruikelijk is in contracten het aangeven van een of meer verificatiemethodes, eventueel met een of meer verificatiemomenten. 

De taalbinding van een verificatiemethode- en moment naar NEN 2660 is nog niet bekend. 

[issue 15](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/15)


## Toelichting op de kolommen in de Eistabel

### URI
Met URI wordt bedoeld: de unieke naam van de eis. Zie [URI conform W3C](https://www.w3.org/wiki/URI). 

De URI is unieke naam voor de eis binnen het project.
Bij de eisen kan verwezen worden naar een eis in een eisenbibliotheek onder "Bron".

Bij de eisen kan de URI ook de verwijzing zijn naar de eis in een bibliotheek; dan mogen de overige kolommen niet zijn aangepast en ook geen


### Code
In de code kan een in het project gebruikte code staan, die heeft mogelijk maakt in een gesprek naar de eis of het concept te verwijzen, zonder de volledige URI te hoeven benoemen. 



### Naam
De naam is de voor mensen leesbare naam van de eis. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.



### Type
Bij "Type" staat welk concept bedoeld wordt:
1. FysiekObject  
2. Functie  
3. Activiteit   
4. Informatieproducten
5. Eis 


### Tekst
Bij "Tekst" staat de eistekst


### Toelichting op de eistekst
Een contractuele eis kan onderbouwd worden met een toelichting.

De taalbinding van toelichting naar NEN 2660 is nog niet bekend. 

[Issue 17]https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/17



### HeeftDeel
Bij HeeftDeel kan een hiërarchie worden aangegeven van de eisenboom zoals gebruikelijk in contracten. Een eis kan meerdere onderliggende eisen hebben, er komen dan meerdere regels met dezelfde eis voor in de eisentabel. 



### Ernst


### Bron


### Specificeert
Hier staat de URI van het concept waar de eis aan gesteld wordt. Een eis kan aan meerdere concepten gesteld worden, er komen dan meerdere regels met dezelfde eis voor in de eisentabel. 


De taalbinding van specificeert naar NEN 2660 is nog niet bekend. 

[Issue 18](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/18)








