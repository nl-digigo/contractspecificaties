# Documenten

Het documentenformat wordt gebruikt voor de definitie van de documenten. De volgende documenten worden opgenomen in de documententabel:

- Brondocumenten voor eisen: dit kan een beleidsstuk zijn, of een norm of wet of ander document waarin eisen beschreven staan. Dit document wordt toegevoegd om een relatie te behouden met het brondocument en om de context van de eis te kunnen opzoeken. De eisen in de eisentabel zijn de eisen die contractueel gelden, een opdrachtnemer hoeft het brondocument niet zelf te scannen op eisen.
- Van toepassing zijnde documenten, waarnaar verwezen wordt in een eistekst. Dit kan een beleidsstuk zijn, of een norm of wet of ander document waarin eisen beschreven staan. Een opdrachtnemer wordt door deze verwijzing verplicht om zelf de eisen in dit document te scannen en mee te nemen in de verificatie en validatie.
- Overige contractuele documenten, zodat ook teksten in paragraven kunnen worden toegevoegd als data. Dit betreft een document, waarvan hele paragraven niet zijn vertaald naar eisen, maar een context bieden voor de eisen, bijvoorbeeld inleidende hoofdstukken van de Vraagspecificatie Eisen, Proces en informatieleveringsspecificatie. Dank zij de documententabel kan een opdrachtnemer wel de teksten per paragraaf inlezen en deze als context oproepen in eigen projectbeheersingssystemen.

De vertaling / binding van documenten is naar [cs:Document](https://data.crow.nl/contractspecificaties/def/Document) als specialisatie van nen2660:InformatieObject. Merk op: ook een eis wordt gezien als InformatieObject; maar deze wordt opgenomen in de Eisentabel. In de onderwerpentabel zijn te leveren documenten/datasets (informatieleveringen) óók InformatieObject. De informatieleveringen die gevráágd worden in het contract, staan niet in de Documententabel.

## Documentenformat

Het format wordt in 2 delen getoond in verband met de leesbaarheid van dit document. De laatste rij bevat een voorbeeld uitwerking.

<table class="data">
<thead>
  <th> [=documentURI=]
  <th> [=DocumentCode=]
  <th> [=DocumentNaam=]
  <th> [=DocumentVersie=]
  <th> [=DocumentVersieDatum=]
</thead>
<tr class="def">
  <td> In deze kolom staat de unieke naam (URI) van het document.
  <td> In deze kolom staat de code ofwel het nummer van het document.
  <td> In deze kolom staat de naam van het document.
  <td> In deze kolom staat de versie van het document.
  <td> In deze kolom staat de versiedatum van het document.
</tr>
</table>

<table class="data">
<thead>
  <th> [=DocumentAuteur=]
  <th> [=DocumentType=]
  <th> [=DocumentSectie=]
  <th> [=DocumentSectieNaam=]
  <th> [=DocumentSectieTekst=]
</thead>
<tr class="def">
  <td> In deze kolom staat de auteur van het document.
  <td> In deze kolom staat het documenttype.
  <td> In deze kolom staat de sectie URI
  <td> In deze kolom staat de sectie naam.
  <td> In deze kolom staat de sectie tekst.
</tr>
</table>

## Details documententabel

### <dfn>DocumentURI

De URI is de unieke identifier voor het document binnen het project.

[URI](https://www.w3.org/wiki/URI); Voor het opstellen van URI's heeft de NEN 2660-2 een URI-strategie die je moet volgen.

| Taalbinding | Kardinaliteit | Datatype                                               |
| ----------- | ------------- | ------------------------------------------------------ |
| n.v.t.      | 1:1           | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def }

> Een URI maakt het meteen "linked data proof"

### <dfn>DocumentCode

De DocumentCode is een nummer van het onderwerp in spreektaal, vaak een voor mensen herkenbare code of projectnummer. Deze meestal eenvoudige en soms logisch genummerde Code maakt het mogelijk om in een gesprek naar hetdocument te verwijzen, zonder de volledige URI te hoeven benoemen.

| Taalbinding                                                                   | Kardinaliteit | Datatype                                               |
| ----------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [skos:notation](https://www.w3.org/2009/08/skos-reference/skos.html#notation) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def }

### <dfn>DocumentNaam

De DocumentNaam is de voor mensen leesbare naam van het document. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.

| Taalbinding                                                                     | Kardinaliteit | Datatype                                               |
| ------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------ |
| [skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel) | 1:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def }

### <dfn>DocumentVersie

In deze kolom staat de versie van het document.

| Taalbinding                                                        | Kardinaliteit | Datatype                                               |
| ------------------------------------------------------------------ | ------------- | ------------------------------------------------------ |
| [cs:versie](https://data.crow.nl/contractspecificaties/def/versie) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def }

### <dfn>DocumentVersieDatum

In deze kolom staat de versiedatum van het document.

| Taalbinding                                                                  | Kardinaliteit | Datatype                                           |
| ---------------------------------------------------------------------------- | ------------- | -------------------------------------------------- |
| [cs:versieDatum](https://data.crow.nl/contractspecificaties/def/versieDatum) | 0:1           | [xsd:date](https://www.w3.org/2001/XMLSchema#date) |
| { .def }

### <dfn>DocumentAuteur

In deze kolom staat de auteur van het document.

| Taalbinding                                     | Kardinaliteit | Datatype                                               |
| ----------------------------------------------- | ------------- | ------------------------------------------------------ |
| [dct:creator](http://purl.org/dc/terms/creator) | 0:n           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def }

### <dfn>DocumentType

In deze kolom staat het documenttype. Voor documenttypen is nog geen nationale afspraak gemaakt.

| Taalbinding                                                                    | Kardinaliteit | Datatype                                               |
| ------------------------------------------------------------------------------ | ------------- | ------------------------------------------------------ |
| [cs:documentType](https://data.crow.nl/contractspecificaties/def/documentType) | 0:1           | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def }


<p class="note" title="Teksten opnemen als data">
De bovenstaande eigenschappen van het document zijn voldoende om bij een eis het brondocument te kunnen meegeven. 
Naast eisen kunnen ook teksten in de contractdocumenten worden meegegeven als data. Hiervan kan de opdrachtnemer gebruik maken om het gehele contract te kunnen verwerken in een projectmanagementsysteem, om bijvoorbeeld eisen af te leiden uit de tekst, of risico's, of andere zaken. 
Ook kan deze optie gebruikt worden in een contract voor ingenieursdiensten, waarbij ook het samenstellen van een contract wordt gevraagd aan een opdrachtnemer.
</p>

### <dfn>DocumentSectie

In deze kolom staat de documentsectie. Deze kan gebruikt worden om een document verder op te delen. Middels de 'heeft deel' relatie kunnen net zoveel secties aan een document toegevoegd worden als er nodig zijn.

| Taalbinding                                                        | Kardinaliteit         | Datatype                                               |
| ------------------------------------------------------------------ | --------------------- | ------------------------------------------------------ |
| [nen2660:hasPart](https://bimloket.github.io/nen2660/term#hasPart) | 0:n (t.o.v. Document) | [xsd:anyURI](https://www.w3.org/2001/XMLSchema#anyURI) |
| { .def }

### <dfn>DocumentSectieNaam

De DocumentSectieNaam is de voor mensen leesbare naam van het onderwerp. Deze naam hoeft niet uniek te zijn in het project, maar dat is natuurlijk wel handig.

| Taalbinding                                                                     | Kardinaliteit               | Datatype                                               |
| ------------------------------------------------------------------------------- | --------------------------- | ------------------------------------------------------ |
| [skos:prefLabel](https://www.w3.org/2009/08/skos-reference/skos.html#prefLabel) | 1:1 (t.o.v. DocumentSectie) | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def }

### <dfn>DocumentSectieTekst

In deze kolom staat de paragraaftekst.

| Taalbinding                                                   | Kardinaliteit               | Datatype                                               |
| ------------------------------------------------------------- | --------------------------- | ------------------------------------------------------ |
| [rdf:value](http://www.w3.org/1999/02/22-rdf-syntax-ns#value) | 0:1 (t.o.v. DocumentSectie) | [xsd:string](https://www.w3.org/2001/XMLSchema#string) |
| { .def }
