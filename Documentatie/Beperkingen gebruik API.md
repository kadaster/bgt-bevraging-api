# Beperkingen gebruik BGT Bevraging API
Het gebruik van de BGT Bevraging API is kosteloos. Bij het gebruik van deze service gelden voorwaarden om overmatig of onwenselijk gebruik van de API te voorkomen. Kadaster wil de BGT Bevraging API voor alle bronhouders en dataleveranciers snel en bruikbaar houden. Om dit te kunnen waarborgen zijn limieten ingesteld.

Bij kosteloos gebruik geldt een maximum van <TO BE DEFINED> berichten per dag (quota limit). Daarnaast is een beperking gesteld aan de hoeveelheid berichten per seconde (rate limit). Hierbij wordt gemonitord hoeveel requests een gebruiker per tijdsperiode indient en wordt gecontroleerd of de gebruiker het maximaal aantal requests per tijdsperiode niet overschrijdt. Wanneer overschrijding wordt geconstateerd, wordt een `429 Too Many Requests` foutmelding gestuurd.
  
# Headers
## Quotum  

Quotum response headers
  
| Header | Beschrijving |
|:--- |:--- |
| Kadaster-RateLimit-DayLimit | Aantal requests per dag |
| Kadaster-RateLimit-DayLimit-Remaining | Aantal resterende client requests in de huidige tijdsperiode | 
  
### Rate limiting 

Rate limiting response headers, comform NL API Strategie:

| Header | Beschrijving |
|:--- |:--- |
| X-Rate-Limit-Limit | Aantal requests per seconde (n) |
| X-Rate-Limit-Remaining | Aantal resterende client requests in de huidige tijdsperiode: waarbij x het aantal ingediende requests is. |
| X-Rate-Limit-Reset | Aantal seconden in de tijdsperiode. In dit geval is dit altijd 1 seconde. |

Komt u hier structureel boven? [Neem dan contact met ons op](https://formulieren.kadaster.nl/contact_bgt).
