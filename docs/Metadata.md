# Metadata

Omdat CSV in principe platte tekst bestanden zijn, bestaat er geen geïntegreerde mogelijkheid om metadata aan te geven. Dit is wel handig bij gegevens overdracht. Bij CSV is hiervoor [CSVW](https://csvw.org/) voor bedacht. Binnen Contractspecifaties doen we dan ook de aanbeveling om dit te gebruiken. 

## Gegevens over de set

Om de gegevenset goed te kunnen onderscheiden en identificeren zijn minimaal de volgende gegevens nodig.

| Gegeven      | Toelichting                                      | Taalbinding                                            |
|--------------|--------------------------------------------------|--------------------------------------------------------|
| Titel        | Een naam/titel waarmee de eisenset herkenbaar is | [dc:title](http://purl.org/dc/terms/title)             |
| Beschrijving | Een eventuele toelichting op de set              | [dc:description](http://purl.org/dc/terms/description) |
| Uitgever     | De organisatie of persoon die de data verstrekt  | [dc:publisher](http://purl.org/dc/terms/publisher)     |
| Datum        | De datum waarop de set gemaakt is                | [dc:date](http://purl.org/dc/terms/date)               |
| { .def }     |

## Gegevens over de distributie

Om de CSV file (de distributie) goed te kunnen lezen/interpreteren zijn minimaal de volgende gegevens nodig. Deze zijn gebaseerd op: 
* [CSV Dialect](http://dataprotocols.org/csv-dialect/)
* [Model for Tabular Data and Metadata on the Web](https://www.w3.org/TR/tabular-data-model/#syntax)

In de kolom 'Best practice' staat de aanbeveling voor Contractspecificaties.

| Gegeven            | Toelichting                                                                                                                       | Taalbinding   | Best practice |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------|---------------|---------------|
| Encodering         | Specificeert hoe de CSV gecodeert is.                                                                                             | `encoding`    | `utf-8`       |
| Quote teken        | Specificeert een één-karakter tekenreeks om te gebruiken als aanhalingsteken.                                                     | `quoteChar`   | `"`           |
| Dubbel quote teken | Bepaalt de behandeling van aanhalingstekens in velden.                                                                            | `doubleQuote` | `true`        |
| Header             | Geeft aan of het bestand een header-rij bevat. Indien `true` is de eerste rij in het bestand een header-rij, geen gegevens.       | `header`      | `true`        |
| Scheidingsteken    | Specificeert een één-karakter tekenreeks om te gebruiken als veldscheidingsteken. Standaard is dit `,`, maar vanuit NL Excel `;`) | `delimiter`   | `;`           |
| { .def }     |

## JSON metadata file

Bovenstaande gegevens worden vastgelegd in een [JSON-LD](https://json-ld.org/) bestand. Dit bestand bevat daarnaast ook een beschrijving van de tabellen en de kolommen. Dit wordt gedaan om bij elke kolom aan te kunnen geven wat de taalbinding is naar de ontologie van Contractspecificaties. Deze verandert in principe niet. Hierdoor hoeft er in de JSON-LD Metadata file niet veel aangepast te worden als deze wordt opgeleverd tezamen met de CSV's. Een voorbeeld is te vinden op de [#TODO GitHub](...). 

De gegevens die aangepast moeten worden betreffen:
* De gegevens over de set;
* De gegevens over de distributie;
* Overal waar de naam van een CSV file wordt aangehaald moet de juiste worden ingevuld.

> EXAMPLE "Metadata gegevens in te vullen in JSON-LD file"
>   ```
>  "dc:title": "Voorbeeld bestand",
>  "dc:description": "Een voorbeeld bestand uitgelegd",
>  "dc:publisher": "Stichting CROW",
>  "dc:date": "2022-12-31",
>  "dialect": {
>    "encoding": "utf-8",
>    "quoteChar": "\"",
>    "doubleQuote": true,
>    "header": true,
>    "delimiter": ";"
>   }
> ...
>     "url": "Eisentabel voorbeeld.csv",
> ...
>       "valueUrl": "Documententabel voorbeeld.csv#{eisBron}"
>   ```