Wegdeel
=======

Dit hoofdstuk beschrijft de wijzigingen voor het object Wegdeel in BRT.Next ten
opzichte van de [vorige versie van het
wijzigingsvoorstel](https://docs.geostandaarden.nl/brtnext/cv-im-brtnext-20221104/#wegdeel).

Overzicht
---------

Hieronder volgt een overzicht van de attributen en attribuutwaarden van het
object Wegdeel, na doorvoeren van de wijzigingen t.o.v. vorige versie
wijzigingsvoorstel.

*Overzicht attributen en waarden/type van object Wegdeel in BRT.Next*

| Attribuutnaam            | Waarde of «type»            | Geometrietype | Kardinaliteit |
|--------------------------|-----------------------------|---------------|---------------|
| geometrie                | «vlak»                      |               | 1 -1          |
|                          | «lijn»                      |               |               |
| typeWegdeel              | autosnelweg                 | vlak          | 1..n          |
|                          | autoweg                     | vlak          |               |
|                          | hoofdweg                    | vlak          |               |
|                          | regionale weg               | vlak          |               |
|                          | lokale weg                  | vlak          |               |
|                          | straat                      | vlak          |               |
|                          | overig                      | vlak          |               |
|                          | parkeerplaats               | vlak          |               |
|                          | OV-baan                     | vlak          |               |
|                          | fietspad                    | vlak, lijn    |               |
|                          | voetpad                     | vlak, lijn    |               |
|                          | voetgangersgebied           | vlak          |               |
|                          | startbaan, landingsbaan     | vlak          |               |
|                          | rolbaan, platform           | vlak          |               |
|                          | veerverbinding              | lijn          |               |
|                          | fietsveer                   | lijn          |               |
|                          | voetveer                    | lijn          |               |
| ligging                  | op vast deel van brug       |               | 0..n          |
|                          | op beweegbaar deel van brug |               |               |
|                          | op rotonde                  |               |               |
|                          | op oprit / afrit            |               |               |
|                          | op knooppuntverbinding      |               |               |
|                          | op overweg                  |               |               |
|                          | in tunnel                   |               |               |
| verhardingsbreedteklasse | \> 7 meter                  |               |               |
|                          | 4 – 7 meter                 |               |               |
|                          | 2 – 4 meter                 |               |               |
|                          | \< 2 meter                  |               |               |
| verhardingstype          | verhard                     |               | 1-1           |
|                          | half verhard                |               |               |
|                          | onverhard                   |               |               |
|                          | onbekend                    |               |               |
| relatieveHoogteligging   | «geheel getal [-9;9]»       |               | 1-1           |
| status                   | bestaand                    |               | 1-1           |
| naam                     | «tekst»                     |               | 0..n          |
| naam: herkomst           | «tekst»                     |               | 0..n          |
| A-wegnummer              | «tekst»                     |               | 0..n          |
| N-wegnummer              | «tekst»                     |               | 0..n          |
| E-wegnummer              | «tekst»                     |               | 0..n          |
| S-wegnummer              | «tekst»                     |               | 0..n          |
| afritnummer              | «tekst»                     |               | 0..1          |
| afritnaam                | «tekst»                     |               | 0..1          |
| knooppuntnaam            | «tekst»                     |               | 0..1          |
| brugnaam                 | «tekst»                     |               | 0..1          |
| tunnelnaam               | «tekst»                     |               | 0..1          |

Wijzigingen t.o.v. vorige versie
--------------------------------

De volgende wijzigingen zijn doorgevoerd in het object Wegdeel ten opzichte van
vorige versie wijzigingsvoorstel.

### Attributen

*Hernoemen*

| Attribuutnaam | wordt hernoemd naar |
|---------------|---------------------|
| type          | type**Wegdeel**     |

### Attribuutwaarden

*Hernoemen*

| Attribuutwaarde               | wordt hernoemd naar |
|-------------------------------|---------------------|
| ~~rijbaan~~ autosnelweg   | autosnelweg         |
| ~~rijbaan~~ autoweg       | autoweg             |
| ~~rijbaan~~ hoofdweg      | hoofdweg            |
| ~~rijbaan~~ regionale weg | regionale weg       |
| ~~rijbaan~~ lokale weg    | lokale weg          |
| ~~rijbaan~~ straat        | straat              |
| ~~rijbaan~~ overig        | overig              |
| parkeer~~vlak~~           | parkeer**plaats**   |
| veer~~dienst, pontveer~~  | veer**verbinding**  |

*Definities*

| Voor attribuutwaarde | wordt definitie                                                                                                                   | aangepast naar                                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| straat               | Wegdeel dat onderdeel is van een weg van zeer plaatselijk belang, gelegen binnen ~~bebouwd~~ gebied.                          | Wegdeel dat onderdeel is van een weg van zeer plaatselijk belang, gelegen binnen gebied **met bebouwing**.                               |
| parkeerplaats        | ~~Wegdeel bestemd~~ voor het parkeren van ~~motor~~voertuigen.                                                            | **Parkeergelegenheid** voor het parkeren van **meerdere** voertuigen **in de openlucht met een aparte toegang vanaf de doorgaande weg**. |
| rolbaan, platform    | Wegdeel uitsluitend bedoeld voor vliegverkeer ten behoeve van het taxiën ~~van vliegtuigen~~ of het parkeren van vliegtuigen. | Wegdeel uitsluitend bedoeld voor vliegverkeer ten behoeve van het taxiën of het parkeren van vliegtuigen.                                |