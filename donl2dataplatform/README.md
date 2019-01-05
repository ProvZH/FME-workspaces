Deze workspace kopieert de metadata van de provincie Zuid-Holland op [data.overheid.nl](http://data.overheid.nl) naar [Dataplatform.nl](http:/zuid-holland.dataplatform.nl). Hij is bedoeld om de NGR metadata initieel in te lezen in de database van Dataplatform.nl.

Data.overheid.nl en Dataplatform.nl zijn beide gebouwd op [CKAN](https://nl.wikipedia.org/wiki/CKAN). Voor het uitlezen en wegschrijven van de gegevens maak de workspace dan ook gebruik van de [CKAN API](https://docs.ckan.org/en/2.8/api/). 

Alleen de metadata die via het [Nationaal Georegister (NGR)](http://www.nationaalgeoregister.nl) gepubliceerd is, wordt meegenomen in de kopieerslag.

De mapping van het NGR datamodel op dat van CKAN is de reden om de metadata te kopiëren van data.overheid.nl, en níet rechtstreeks van het NGR. Het is lastig om deze mapping te maken. We streven er bovendien naar om de gegevens op Dataplatform.nl zo veel mogelijk aan te laten sluiten op de landelijke metadatastandaarden. Vandaar dat we er voor gekozen hebben om de mapping van data.overheid.nl over te nemen.

Via de published parameter `environment` kun je switchen tussen de acceptatie- en productieomgeving van Dataplatform.nl. Let op: je moet eerst wel de juiste API keys invullen in de private parameters `api_key_acc` en `api_key_prod`.

De published parameter `prefix` bevat de tekst die bij het kopiëren vooraan de naam van een dataset wordt geplakt. De parameter is standaard leeg. Het kan handig zijn om tijdens testen wél een prefix mee te geven. Je kunt een dataset of package namelijk wel verwijderen, maar hij is pas écht verdwenen na 'purgen' van de database. Om dit te kunnen doen, heb je echter beheerrechten nodig.