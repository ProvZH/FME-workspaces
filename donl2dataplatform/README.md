Deze workspace kopieert de metadata van de provincie Zuid-Holland op [data.overheid.nl](http://data.overheid.nl) naar [Dataplatform.nl](http:/zuid-holland.dataplatform.nl). Het is bedoelt om de NGR metadata initieel in te lezen in de database van Dataplatform.nl.

data.overheid.nl en Dataplatform.nl maken beide gebruik van [CKAN](https://nl.wikipedia.org/wiki/CKAN). Voor het uitlezen en wegschrijven van de gegevens wordt dan ook gebruik gemaakt van de [CKAN API](https://docs.ckan.org/en/2.8/api/). 

Alleen de metadata die via het [Nationaal Georegister (NGR)](http://www.nationaalgeoregister.nl) gepubliceerd is, wordt meegenomen in de kopieerslag.

De mapping van het NGR datamodel op dat van CKAN is de reden om de metadata te kopiëren van data.overheid.nl, en níet rechtstreeks van het NGR. Het is lastig om deze mapping te maken en we streven er naar om op Dataplatform.nl zo veel mogelijk aan te sluiten bij de landelijke portalen. Vandaar dat we er voor gekozen hebben om de mapping van data.overheid.nl over te nemen.

Via de published parameter `environment` kun je switchen tussen de acceptatie- en productieomgeving van Dataplatform.nl. Let op: het is wel nodig om de juiste API keys in te vullen in de private parameters `api_key_acc` en `api_key_prod`.

De published parameter `prefix` bevat de tekst die bij het kopiëren vooraan de naam van een dataset wordt geplakt. De parameter is standaard leeg. Het kan handig zijn om tijdens testen wél een prefix mee te geven. Je kunt een dataset of package namelijk wel verwijderen, maar hij is pas écht verdwenen na 'purgen' van de database. Hier heb je beheerrechten voor nodig.

