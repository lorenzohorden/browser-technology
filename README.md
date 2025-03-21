# browser-technology
This is a school project where we made a prototype for a government form, this is for educational purposes.

## week 1

### onderzoek

Ik begon de week met het bekijken van de NS huisstijl en het kopieren van kleurwaarden van achtergronden, teksten etc. Dat deed ik eerst op de NS website zelf en later vond ik een link op teams waar het heel makkelijk aangegeven stond, daar heb ik het grid systeem van.

Ik heb ook gekeken naar het formulier om te kijken wat ik wilde gaan uitwerken, voor nu begin ik met vraag 1 omdat ik nog geen input types heb verwerkt en het overslaan van 1b als je niet getrouwd bent lijkt me een leuke uitdaging.

### waarschuwing

De docenten zeiden dat we een waarschuwing moesten implementeren, omdat we een overheidsformulier maken en vorig jaar werden leerlingen benaderd door de overheid. Ik heb een kleine section gemaakt met een waarschuwing erin en een `input type="checkbox` met een kruis in het label, zodat je hem weg kunt klikken.

### formulier

Ik ben begonnen an het formulier door een form element te stylen alsof het een container is. Daarin heb ik een aantal input elementen gezet waarin de naam ingevuld kan worden in delen.

### feedback

De feedback was vrij simpel omdat er nog niet zo veel was om feedback op te geven: goed bezig ga zo door


## week 2

### fieldset

Ik kwam er deze week achter dat fieldset bestond en dat dat een goede manier was om secties aan te geven in een formulier. Ik heb al mijn section elementen vervangen door fieldsets en heb alle headers vervangen door legend elementen.

### conditionele styling

Ik ben ook begonnen met het maken van meldingen als velden niet correct zijn ingevuld. Alle input type text velden krijgen een rode rand eromheen als ze fout zijn een een groene rand als ze correct zijn ingevuld met `:invalid` en `:valid`. Ik heb ervoor gekozen om een `outline` te gebruiken, omdat een `border` de box-sizing veranderd, waardoor elementen iets verplaatsen.

### progressive disclosure

vraag 1B is niet nodig om in te vullen, wanneer de overledene niet getrouwd was. Het is dus ook niet nodig om al die vragen te laten zien als dat niet zo is. Ik heb om dit op te lossen `:has()` gebruikt, zodat je de extra vragen alleen kan invullen als die van toepassing zijn.

### feedback

Het belangrijkste punt van de feedback is dat ik bij vraag 1B geen progressive enhancement gebruik, als nu een gebruiker geen `:has` heeft worden de andere vragen niet weergeven. Dit wil ik oplossen door de onnodige vragen te verweideren met `:has` in plaats van andersom. Ik zou ook een `@support` kunnen gebruiken, maar deze manier is korter en ik vind het erg slim.

## week 3

### conditionele styling II

Deze week kwam ik erachter dat `user-invalid` en `user-valid` bestaan. Ik heb alle stijl veranderd, omdat ik de velden eerst zonder opmaak wil hebben als ze niet zijn ingevuld.

Ook heb ik het advies van `:has(:not)` gebruikt, omdat dit beter werkt met progressive enhancement.

### JavaScript :)

Ik heb JavaScript gebruikt om bij vraag 1B de inputvelden die niet altijd verplicht zijn dynamisch te veranderen naar `required` als ze required zijn. 

Ook heb ik ervoor gezorgd dat de inputvelden die niet hoger kunnen zijn dan de huidige datum een max krijgen aan de hand van de `Date` in JavaScript.

### foutmeldingen

Als een veld `:user-invalid` is krijgt een element nu een rode rand, maar ik denk dat het beter is voor de gebruiker als er ook een foutmelding bijkomt. Dit zorgt ervoor dat de gebruiker altijd weet dat een element invalid is, ok als die gebruiker bijvoorbeeld kleurenblind is. Ik heb gekozen om de meldingen alleen "De .. is incorrect", hoewel dit niet altijd het geval is als er bijvoorbeeld een leeg input veld is, is het wel duidelijk dat het veld niet correct is.

### feedback

De feedback was de feedback van Jeremy Keith, hij heeft niet echt feedback gegeven maar meer gepraat over progressive enhancement en het verschil tussen imperative en declerative talen.

## week 4 (laatste week)

### foutmeldingen II

Ik heb nog geen foutmeldingen gemaakt voor input type radio, omdat als ik een `::after` met tekst aan een input type radio plak, dan staat er twee keer een foutmelding. Mijn oplossing voor dit probleem is de `::after` op de `fieldset` zetten, hierdoor komt onderaan de fieldset een melding, waardoor het duidelijk is dat het over de hele fieldset gaat.

### gegevens ophalen via sessionstorage

Ik wilde dit eerst zelf doen, maar wegens tijd tekort heb ik chatGPT een aantal vragen gesteld waarna hij met de code kwam in `SessionStorage.js`. Ik snap waarom deze code werkt en kan hem uitleggen, maar ik wist eerst niet dat de FormData functie bestond. Ik snap nu wel hoe het werkt, dus volgende keer zou ik het wel zonder ChatGPT kunnen namaken.

### conclusie

Over het aantal vragen dat ik heb verwerkt ben ik niet trots. Ik had er achteraf meer willen doen, maar ik bleef een beetje hangen op mijn HTML en de indeling van de fieldsets. Hierdoor vind ik wel dat het allemaal erg overzichtelijk is en dit heeft de CSS ook vrij simpel gehouden. Dus ik heb kwaliteit over kwantiteit gekozen, wat op zich niet erg is, alleen ik had wel meer kwantiteit kunnen hebben vind ik zelf.
