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
<th> heeftDeel
</th>
<th> Ernst
</th>
<th> Bron
</th></tr>
<tr>
<td>  </td>
<td> skos:Notation </td>
<td> skos:prefLabel </td>
<td> nen2660:heeftVoorwaardeSpecificatie </td>
<td> nen2660:heeftDeel </td>
<td> nen2660:voorwaardeErnstType </td>
<td> nen2660:voorwaardeBronType </td>
<td>  </td>
</td></tr>
</table>

Over unieke naam van de eis: gebruikers geven de voorkeur aan een unieke identifier over projecten heen, zodat een eis uit een bron (eisenbibliotheek) herkend kan worden

## Eisen
Een eis heeft een vertaling / binding naar de NEN 2660 als InformationObject




## Verificatiemethoden
Gebruikelijk is in contracten het aangeven van een of meer verificatiemethodes, eventueel met een of meer verificatiemomenten. 

De taalbinding van een verificatiemethode- en moment naar NEN 2660 is nog niet bekend. 

[issue 15](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/15)


## Toelichting op de kolommen in de Tabellen

### URI
Met URI wordt bedoeld: de unieke naam van het onderwerp of de eis. Zie [URI conform W3C](https://www.w3.org/wiki/URI). 

De URI is unieke naam voor het onderwerp of de eis binnen het project; bij de definitie kan worden verwezen naar het type uit een ontologie ofwel objecttypenbiblkiotheek.
Bij de eisen kan verwezen worden naar een eis in een eisenbibliotheek onder "Bron".

Bij de eisen kan de URI ook de verwijzing zijn naar de eis in een bibliotheek; dan mogen de overige kolommen niet zijn aangepast en ook geen


### Code
In de code kan een in het project gebruikte code staan, die heeft mogelijk maakt in een gesprek naar de eis of het concept te verwijzen, zonder de volledige URI te hoeven benoemen. 



### Naam
De naam is de voor mensen leesbare naam van het concept. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.



### Type
Bij "Type" staat welk concept bedoeld wordt:
1. FysiekObject  
2. Functie  
3. Activiteit   
4. Informatieproducten



### Definitie
Bij "definitie" staat ofwel een tekst die het concept definieert, ofwel een URI die verwijst naar de definitie in een ontologie (objecttypenbibliotheek).



### HeeftDeel
Bij HeeftDeel kan een hiërarchie worden aangegeven zoals een objectenboom of functieboom zoals gebruikelijk in contracten. Een concept kan uit meerdere delen bestaan, er komen dan meerdere regels voor in de eisentabel. 



### Eigenaar
Vooral bij objecten is het voor de opdrachtgever handig, te weten wie de eigenaar is. De eigenaar is de persoon of rol bij de opdrachtgever die verantwoordelijk is voor beheer van dit objecttype, en die geconsulteerd moet worden bij afwijking van de eisen.



De taalbinding van eigenaar naar NEN 2660 is nog niet bekend. 

[Issue 16](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/16)



