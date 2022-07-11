# Documenten
Het documentenformat wordt gebruikt voor de definitie van de documenten. De volgende documenten worden opgenomen in de documententabel:

* Brondocumenten voor eisen: dit kan een beleidsstuk zijn, of een norm of wet of ander document waarin eisen beschreven staan. Dit document wordt toegevoegd om een relatie te behouden met het bronddocument en om de context van de eis te kunnen opzoeken. De eisen in de eisentabel zijn de eisen die contractueel gelden, een opdrachtnemer hoeft het brondocument niet zelf te scannen op eisen.
* Van toepassing zijnde documenten, waarnaar verwezen wordt in een eistekst. Dit kan een beleidsstuk zijn, of een norm of wet of ander document waarin eisen beschreven staan. Een opdrachtnemer wordt door deze verwijzing verplicht om zelf de eisen in dit document te scannen en mee te nemen in de verificatie en validatie.
* Overige contractuele documenten, zodat ook teksten in paragraven kunnen worden toegevoegd als data. Dit betreft een document, waarvan hele paragraven niet zijn vertaald naar eisen, maar een context bieden voor de eisen, bijvoorbeeld inleidende hoofdstukken van de Vraagspecificatie Eisen, Proces en informatieleveringsspecificatie. Dank zij de documententabel kan een opdrachtnemer wel de teksten per paragraaf inlezen en deze als context oproepen in eigen projectbeheersingssystemen.

De vertaling / binding van documenten naar NEN2660-2 is nen2660:InformatieObject. Merk op: ook een eis wordt gezien als InformatieObject; maar deze wordt opgenomen in de Eisentabel. In de onderwerpentabel zijn te leveren documenten/datasets (informatieleveringen) óók InformatieObject. De informatieleveringen die gevráágd worden in het contract, staan niet in de Documententabel.


## Documentenformat

Het format wordt in 2 delen getoond in verband met de leesbaarheid van dit document. De laatste rij bevat een voorbeeld uitwerking.

<table class="wikitable" style="text-align:left; valign:top">
<tr>
<th> [=documentURI=]
</th>
<th> [=DocumentCode=]
</th>
<th> [=DocumentNaam=]
</th>
<th> [=DocumentVersie=]
</th>
<th> [=DocumentVersieDatum=]
</th>
</tr>
<tr>
<td> In deze kolom staat de unieke naam (URI) van het document. </td>
<td> In deze kolom staat de code ofwel het nummer van het document. </td>
<td> In deze kolom staat de naam van het document. </td>
<td> In deze kolom staat de versie van het document. </td>
<td> In deze kolom staat de versiedatum van het document. </td>
</tr>
</table>
<br><br>
<table class="wikitable" style="text-align:left; valign:top">
<tr>
<th> [=DocumentAuteur=]
</th>
<th> [=DocumentType=]
</th>
<th> [=DocumentHoofdstuk=]
</th>
<th> [=DocumentHoofdstukTitel=]
</th>
<th> [=DocumentParagraaf=]
</th>
<th> [=DocumentParagraafTitel=]
</th>
<th> [=DocumentParagraafTekst=]
</th></tr>
<tr>
<td> In deze kolom staat de auteur van het document. </td>
<td> In deze kolom staat het documenttype. </td>
<td> In deze kolom staat het hoofdstuknummer. </td>
<td> In deze kolom staat de hoofdstuktitel. </td>
<td> In deze kolom staat het paragraafnummer. </td>
<td> In deze kolom staat de paragraaftitel. </td>
<td> In deze kolom staat de paragraaftekst. </td>
</td></tr>
</table>



## Details documententabel


### <dfn>DocumentURI
De URI is de unieke identifier voor het document binnen het project.

[URI](https://www.w3.org/wiki/URI)

Cardinaliteit: 1:1

> Een URI maakt het meteen "linked data proof"


### <dfn>DocumentCode
De DocumentCode is een nummer van het onderwerp in spreektaal, vaak een voor mensen herkenbare code of projectnummer. Deze meestal eenvoudige en soms logisch genummerde Code maakt het mogelijk om in een gesprek naar hetdocument te verwijzen, zonder de volledige URI te hoeven benoemen.

[skos:notation](https://www.w3.org/2009/08/skos-reference/skos.html#notation)

Cardinaliteit: 1:1

### <dfn>DocumentNaam
De DocumentNaam is de voor mensen leesbare naam van het document. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.

[skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel)

Cardinaliteit: 1:1

### <dfn>DocumentVersie
In deze kolom staat de versie van het document.

Cardinaliteit: 0:1


### <dfn>DocumentVersieDatum
In deze kolom staat de versiedatum van het document.

Cardinaliteit: 0:1

### <dfn>DocumentAuteur
In deze kolom staat de auteur van het document.

Cardinaliteit: 0:n

### <dfn>DocumentType
In deze kolom staat het documenttype. Voor documenttypen is nog geen nationale afspraak gemaakt. 

Cardinaliteit: 0:1

### <dfn>DocumentHoofdstuk
In deze kolom staat het hoofdstuknummer.

Cardinaliteit: 0:n

### <dfn>DocumentHoofdstukTitel
In deze kolom staat de hoofdstuktitel.

Cardinaliteit: 0:1 ten opzichte van [=DocumentHoofdstuk=]

### <dfn>DocumentParagraaf
In deze kolom staat het paragraafnummer. 

Cardinaliteit: 0:n ten opzichte van [=DocumentHoofdstuk=]


### <dfn>DocumentParagraafTitel
In deze kolom staat de paragraaftitel.

Cardinaliteit: 0:1 ten opzichte van [=DocumentParagraaf=]


### <dfn>DocumentParagraafTekst
In deze kolom staat de paragraaftekst.

Cardinaliteit: 0:1 ten opzichte van [=DocumentParagraaf=]




