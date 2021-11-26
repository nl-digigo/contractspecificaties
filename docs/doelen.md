# Doelentabel

De doelentabel wordt gebruikt voor de doelen van het project. Op de eerste regel staan de kolomnamen. Op de tweede regel staat een korte toelichting; op de derde regel de vertaling / binding naar de NEN2660-2. Op de vierde regel staat aangegeven, hoeveel relaties er kunnen voorkomen in dit veld (multipliciteit). Als er meer dan één relatie voorkomt, komen er regels bij in de uitwisseling. 


Bij het functioneel specificeren begin je met het vaststellen van de doelstellingen van het systeem. Vanuit die doelstellingen bedenk je welke functies het systeem nodig heeft.

<p class="note">
Een doel is net als een eis een [InformationObject](https://bimloket.github.io/nen2660/def#InformationObject) volgens NEN 2660
</p>


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
<th> specificeert
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
<td> skos:notation </td>
<td> skos:prefLabel </td>
<td> rdf:value </td>
<td> nen2660:heeftDeel </td>
<td> nen2660:heeftVoorwaarde </td>
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

## Voorbeeld doelentabel

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
<th> specificeert
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



