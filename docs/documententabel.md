# Documenten
De documententabel wordt gebruikt voor de definitie van de documenten. Op de eerste regel staan de kolomnamen. Op de tweede regel staat een korte toelichting; op de derde regel de vertaling / binding naar de NEN2660-2. Op de vierde regel staat aangegeven, hoeveel relaties er kunnen voorkomen in dit veld (multipliciteit). Als er meer dan één relatie voorkomt, komen er regels bij in de uitwisseling.

De volgende documenten worden opgenomen in de documententabel

* Brondocumenten voor eisen: dit kan een beleidsstuk zijn, of een norm of wet of ander document waarin eisen beschreven staan. Dit document wordt toegevoegd om een relatie te behouden met het bronddocument en om de context van de eis te kunnen opzoeken. De eisen in de eisentabel zijn de eisen die contractueel gelden, een opdrachtnemer hoeft het brondocument niet zelf te scannen op eisen.
* Van toepassing zijnde documenten, waarnaar verwezen wordt in een eistekst. Dit kan een beleidsstuk zijn, of een norm of wet of ander document waarin eisen beschreven staan. Een opdrachtnemer wordt door deze verwijzing verplicht om zelf de eisen in dit document te scannen en mee te nemen in de verificatie en validatie.
* Overige contractuele documenten, zodat ook teksten in paragraven kunnen worden toegevoegd als data. Dit betreft een document, waarvan hele paragraven niet zijn vertaald naar eisen, maar een context bieden voor de eisen, bijvoorbeeld inleidende hoofdstukken van de Vraagspecificatie Eisen, Proces en informatieleveringsspecificatie. Dank zij de documententabel kan een opdrachtnemer wel de teksten per paragraaf inlezen en deze als context oproepen in eigen projectbeheersingssystemen.

De vertaling / binding van documenten naar NEN2660-2 is nen2660:InformatieObject. Merk op: ook een eis wordt gezien als InformatieObject; maar deze wordt opgenomen in de Eisentabel. In de onderwerpentabel zijn te leveren documenten/datasets (informatieleveringen) óók InformatieObject. De informatieleveringen die gevráágd worden in het contract, staan niet in de Documententabel.

In de tabel staat op de tweede regel een korte toelichting op de inhoud; op de derde regel de vertaling / binding naar NEN2660-2 (of andere standaard?)
[Issue 25](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/25)

## Documententabel

<table class="wikitable" style="text-align:left; valign:top">
<tr>
<th> URI
</th>
<th> Code
</th>
<th> Naam
</th>
<th> Versie
</th>
<th> VersieDatum
</th>
<th> Auteur
</th>
<th> Type document
</th>
<th> Hoofdstuknummer
</th>
<th> Hoofdstuktitel
</th>
<th> Paragraafnummer
</th>
<th> Paragraaftitel
</th>
<th> Paragraaf tekst
</th></tr>
<tr>
<td> In deze kolom staat de unieke naam (URI) van het document. </td>
<td> In deze kolom staat de code ofwel het nummer van het document. </td>
<td> In deze kolom staat de naam van het document. </td>
<td> In deze kolom staat de versie van het document. </td>
<td> In deze kolom staat de versiedatum van het document. </td>
<td> In deze kolom staat de auteur van het document. </td>
<td> In deze kolom staat het documenttype. </td>
<td> In deze kolom staat het hoofdstuknummer. </td>
<td> In deze kolom staat de hoofdstuktitel. </td>
<td> In deze kolom staat het paragraafnummer. </td>
<td> In deze kolom staat de paragraaftitel. </td>
<td> In deze kolom staat de paragraaftekst. </td>
</td></tr>
<tr>
<td> [URI](https://www.w3.org/wiki/URI) </td>
<td> skos:notation </td>
<td> skos:prefLabel </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
<td> rdfs:Class </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
<td> ONBEKEND </td>
</td></tr>
<tr>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:n </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
<td> 1:1 </td>
</td></tr>
</table>


<div class="issue" data-number="32"></div>


## Informatiemodel

Onbekend is of de informatie in de tabel een vertaling / binding naar NEN2660-2 moet hebben of een ander informatiemodel?

[Issue19](https://github.com/bimloket/COINS-3.0-Contract-als-data/issues/19)

## Details documententabel


### URI
In deze kolom staat de unieke naam (URI) van het document.


### Code
In deze kolom staat de code ofwel het nummer van het document.


### Naam
In deze kolom staat de naam van het document. 


### Versie
In deze kolom staat de versie van het document.


### VersieDatum
In deze kolom staat de versiedatum van het document.


### Auteur
In deze kolom staat de auteur van het document.


### Documenttype
In deze kolom staat het documenttype. Voor documenttypen is nog geen nationale afspraak gemaakt.


### Hoofdstuknummer
In deze kolom staat het hoofdstuknummer.


### Hoofdstuktitel
In deze kolom staat de hoofdstuktitel.


### Paragraafnummer
In deze kolom staat het paragraafnummer. 



### Paragraaftitel
In deze kolom staat de paragraaftitel.



### Paragraaftekst
In deze kolom staat de paragraaftekst.





