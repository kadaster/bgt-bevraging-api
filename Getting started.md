# Getting Started 
  
Om aan te sluiten kunt u de volgende stappen doorlopen:
1.	[Aanmelden om toegang te krijgen tot de productieomgeving](#aanmelden)
2.	[Bekijk de functionaliteit en specificaties](#functionaliteiten-en-specificaties)
3.	[Implementeer de API Client](#implementeer-de-api-client)
4.	[Probeer en test de API](#probeer-en-test-de-api)
  
## Aanmelden  
  
[Vraag een API key voor de productieomgeving aan.](https://formulieren.kadaster.nl/aanvraag_bgt_bevraging_api_productie)  
  
## Functionaliteiten en specificaties  
 
U kunt de Open API Specificaties (OAS3) van de API bekijken in [Swagger-formaat](https://kadaster.github.io/bgt-bevraging-api/Technische%20specificatie/) of [Redoc.](https://kadaster.github.io/bgt-bevraging-api/Technische%20specificatie/Redoc/)
De (resolved) OAS3 is hier te downloaden: 

* [openapi.json](https://api.bgt.kadaster.nl/bevraging/v1/openapi.json).
* [openapi.yaml](https://api.bgt.kadaster.nl/bevraging/v1/openapi.yaml).
  
### Beschikbare endpoints  
  
De API kent de volgende endpoints:  

•	*objecten*
Hiermee zijn BGT objecten op te vragen. De endpoint levert afhankelijk van de gebruikte parameter combinatie één of meer voorkomens van één of meer objecten met links naar gerelateerde resources en evt. detail gegevens daarvan.

•	*bevragingen*
Hiermee kan de status van de verwerking van een bevraging gevolgd worden of het resultaat worden gedownload.
  
### Zoekingangen van de verschillende endpoints  
  
Elk endpoint beschikt over een eigen set aan gegevens en elk endpoint is door middel van verschillende zoekingangen te bevragen.  
In de tabel [Wat zit in welk endpoint](https://github.com/kadaster/bgt-bevraging-api/blob/concept-OAS/Documentatie/Wat%20zit%20in%20welk%20endpoint_.pdf) is af te lezen welke zoekingangen mogelijk zijn bij de verschillende endpoints en welke informatie dit oplevert.
  
###   Algemene functionaliteit  
  
Er zijn een aantal algemene functies die gelden voor bovenstaande aanvragen:  
  
•	De expand functionaliteit is te gebruiken om binnen een response extra informatie te ontvangen over een van de gerelateerde objecttypen. Zo kan bijvoorbeeld bij een buurt de gegevens van de gerelateerde wijk worden opgevraagd door expand=wijk mee te nemen in de bevraging. Voor de werking, zie feature [expand.](https://github.com/kadaster/bgt-bevraging-api/blob/concept-OAS/Documentatie/Features/expand.feature)

•	Bij sommige endpoints wordt paginering gebruikt om het aantal zoekresultaten per zoekvraag te beperken. Met de page parameter kan een volgende pagina worden gevraagd. Met de pageSize parameter kan gekozen worden voor meer of minder zoekresultaten per pagina (standaard is 20, maximum is 100). Voor de werking, zie feature [paginering.](https://github.com/kadaster/bgt-bevraging-api/blob/concept-OAS/Documentatie/Features/paginering.feature) 

•	Sommige resources bevatten geometrie. De API ondersteunt op dit moment alleen het RD coördinatenstelsel (epsg:28992). Bij een aanvraag die geometrie teruglevert, moet de request header Accept-Crs worden meegestuurd.

Voor alle feature beschrijvingen zie: (https://github.com/kadaster/bgt-bevraging-api/blob/concept-OAS/Documentatie/Features/).
  
### Uitwerking Use cases  
  
#### Opvragen van actuele voorkomens met een lijst van object identificaties
  
#### opvragen van voorkomens met een lijst van object identificaties en een regisatie van en/of registratie tot datume en tijd
  
#### Zoeken van actuele voorkomens binnen een bounding box

#### Zoeken van actuele voorkomens binnen een polygon

#### Zoeken van actuele voorkomens binnen een multipolygon

#### Zoeken van actuele voorkomens met een lijst van bronhoudercodes

#### Zoeken van voorkomens binnen een bounding box, met registratie van en/of tot datum+tijd en evt. een lijst met object types

#### Zoeken van voorkomens binnen een polygon, met registratie van en/of tot datum+tijd en evt.een lijst met object types

#### Zoeken van voorkomens binnen een multipolygon, met registratie van en/of tot datum+tijd en evt. een lijst met object types

#### Zoeken van voorkomens met een lijst van bronhouder codes, registratie van en/of tot datum+tijd en evt. lijst met object types

#### Opvragen van een actueel voorkomen van een specfiek object

#### Opvragen van voorkomens van een specifiek object met registratie van en/of tot datum+tijd

#### Opvragen van een specifiek voorkomen van een specifiek object

#### Opvragen van de status van de verwerking van een bevraging

#### Opvragen van het resultaat (bestand) van een bevraging
  
### Beperking gebruik BGT Bevraging API
  
Het gebruik van de BGT Bevraging API is kosteloos. Bij het gebruik van deze service gelden voorwaarden om overmatig of onwenselijk gebruik van de API te voorkomen. Kadaster wil de BGT Bevraging API voor alle bronhouders en dataleveranciers snel en bruikbaar houden. Om dit te kunnen waarborgen zijn limieten ingesteld. Meer informatie over de beperkingen van de BGT Bevraging API vindt u [hier.](https://github.com/kadaster/bgt-bevraging-api/blob/concept-OAS/Documentatie/Beperkingen%20gebruik%20API.md)     
  
## Implementeer de API client  
  
Client code kan worden gegenereerd met de “[genereervariant](https://api.bgt.kadaster.nl/bevraging/v1/openapi.yaml)” van de API-specificaties en een code generator. Een overzicht met codegeneratoren is te vinden op [OpenAPI.Tools.](https://openapi.tools/#sdk)  
  
## Probeer en test de API  
  
De werking van de API is het gemakkelijkst te testen met behulp van [Postman](https://www.getpostman.com/). De [openapi.yaml](https://api.bgt.kadaster.nl/bevraging/v1/openapi.yaml) kan als geïmporteerd als project, waarna de verschillende requests worden ingeladen die deze API ondersteunt.
  
### API Key  
  
Om de API te kunnen bevragen, is een API key nodig. Deze kunt u bij het request opnemen in request header “X-Api-Key”. [Vraag een API key voor de BGT Bevraging API aan.](https://formulieren.kadaster.nl/aanvraag_bgt_bevraging_api_productie)  
  
### Testgevallen  
  
  
### URL  
  
De API is te benaderen via de volgende url:

Productieomgeving:  
https://api.bgt.kadaster.nl/bevraging/v1/  
  


    
