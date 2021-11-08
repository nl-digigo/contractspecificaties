# Doelentabel

De doelentabel wordt gebruikt voor de doelen van het project. Op de eerste regel staan de kolomnamen. Op de tweede regel staat een korte toelichting; op de derde regel de vertaling / binding naar de NEN 2660. Op de vierde regel staat aangegeven, hoeveel relaties er kunnen voorkomen in dit veld (cardinaliteit). Als er meer dan één relatie voorkomt, komen er regels bij in de uitwisseling. 


Bij het functioneel specificeren begin je met het vaststellen van de doelstellingen van het systeem. Vanuit die doelstellingen bedenk je welke functies het systeem nodig heeft.

De vertaling / binding van doelen naar NEN 2660 is nog niet bekend. 

De vertaling / binding van de relatie tussen doelen en functies naar NEN 2660 is nog niet bekend.

[issue 14](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/14)

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
<th> Specificeert
</th></tr>
<tr>
<td> In deze kolom staat de unieke naam (URI) van het doel. </td>
<td> In deze kolom staat de code of het nummer van het doel. </td>
<td> In deze kolom staat de de naam oftewel de titel van het doel. </td>
<td> In deze kolom staat het doel beschreven. </td>
<td> In deze kolom staat de URI van een onderliggend doel. </td>
<td> In deze kolom staat de URI van het Onderwerp van het doel. </td>
</tr>
<tr>
<td> [URI](https://www.w3.org/wiki/URI) </td>
<td> skos:Notation </td>
<td> skos:prefLabel </td>
<td> nen2660:heeftVoorwaardeSpecificatie </td>
<td> nen2660:heeftDeel </td>
<td> ONBEKEND </td>
</tr>
<tr>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 0:n </td>
<td> 1:n </td>
</tr>
</table>

## Voorbheeld doelentabel

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
<th> Specificeert
</th></tr>
<tr>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeelddoel0001 </td>
<td> DOEL-0001 </td>
<td> Veilig verkeer </td>
<td> De nieuwe inrichting van de openbare ruimte dient te zorgen voor veilig verkeer, zodat de kans op ernstige verkeersongevallen halveert </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeelddoel0002 </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeeldfunctie0001 </td>
</tr>
<tr>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeelddoel0001  </td>
<td>  </td>
<td>  </td>
<td>  </td>
<td> https://bimloket.github.io/COINS-3.0-Contract-als-data/#voorbeelddoel0003 </td>
<td>  </td>
</tr>
</table>



