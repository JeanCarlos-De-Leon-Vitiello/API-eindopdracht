# Astro Starter Kit: Minimal

```sh
npm create astro@latest -- --template minimal
```

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
├── src/
│   └── pages/
│       └── index.astro
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).


## Week 1/1
idee:
Voor de API opdracht wil ik een movie website maken die aan de hand van je mood op dat moment een aantal films aanraad aan de gebruiker. Ik wil dit gaan doen met emoji's en spraak zodat de gebruiker zijn gevoel kan omschrijven inplaats van de emoji aan te klikken. Vervolgens wil ik een soort bookmark page hebben waar de gebruiker zijn film kan opslaan en later dan weer kan bekijken.

**content api's:**
TMDB api

**web api's:**
local storage api 
view transition

**voorang:**
web annimation api 
view transition api

**extra:**
web ai api
web to speech api 
notification api

**Wat heb ik gedaan**
Vandaag ben ik bezig geweest met het bedenken van mijn eind opdracht en een start maken. Ik heb een start gemaakt door een fetch te doen naar de TMDB content API zodat ik de genre van de films kan ophalen en die koppelen aan een mood. Ik heb een aantal buttons toegevoegd er daar de attribute data-mood="" gekoppeld zodat ik dan de mood met de genre waarde kan koppelen.

**Wat heb ik geleerd:**
- data-""= attributte 
- hoe je de attributte kan ophalen met .getAttribute
- hoe ik een fetch kan doen naar de tmdb api

**Wat ga ik morgen doen:**
morgen wil ik aan de hand van de genre films kunnen ophalen zodat ik een set films kan tonen aan de gebruiker. Ik wil dat gaan doen met localstorage zodat ik de waarde in de results page kan ophalen.

## week 1/2
Vandaag ben ik bezig geweest met het doorgeven van de mood van de mood.astro naar de results.astro. Ik ben er achter gekomen dat als ik local storage wil gebruiken dat ik dat moet gaan doen via de browser. 

Maar dat is in mijn geval geen goed idee omdat er een kans is dat ik de api key in de url mee geef wanneer ik een fetch wil gaan uitvoeren in de browser. devine: vars was dus geen oplossing voor mij. 

Daarom heb ik ervoor gekozen om de mood via de URL door te geven. Op die manier kan ik in movie-results.astro de mood uitlezen met Astro.url.searchParams.get("mood"), die koppelen aan een genre-id, en daarna serverside een fetch doen naar de TMDB API. Dat is in mijn geval beter omdat mijn API key serverside blijft.

**Wat heb ik geleerd:**
- export const prerender = false; (astro prerenderd pages waardoor de url de mood niet mee krijgt. met dit heb ik het uitgezet)
- hoe je local storage kan gebruiken om een value op te slaan.
- hoe je een search param uit een url kan halen en hergebruiken.
- astro prerenderd de html pages die je hebt. Ik heb geleerd hoe je dat uit kan zetten.

**Wat ga ik volgende week doen:**
volgende week wil ik beginnen met het invullen van de resultaten pagina zodat je een film krijg als je op een mood heb geklikt. als dat is gelukt wil ik een bookmark functie maken met local storage.


## weekly nerd:
Hacker Filosofie
**Wat is hacker filosofie?**
Hacker filosofie draait om het zelf maken, begrijpen en beheren van technologie, zodat je controle houdt over je digitale omgeving. Een hacker is niet alleen iemand die systemen kraakt, maar vooral iemand die zelf dingen bouwt, technologie doorgrondt en bijvoorbeeld een eigen server host. De kern is: hoe meer je zelf doet, hoe meer controle en onafhankelijkheid je hebt.

**Waarom is dit belangrijk?**
Tegenwoordig worden apparaten steeds moeilijker te repareren door embedded systemen en geplande veroudering. Dit zorgt voor een groeiende afhankelijkheid van externe partijen, vooral grote Amerikaanse techbedrijven.
Door je eigen infrastructuur te beheren, zoals een eigen server of statische website, kun je:
- meer controle krijgen over je data en systemen
- minder afhankelijk zijn van big tech
- duurzamer omgaan met technologie

**Static sites en duurzame webhosting**
Static site generators maken lichte, snelle websites zonder zware afhankelijkheden. Dit verlaagt energieverbruik en maakt hosting eenvoudiger.
Belangrijke principes:
- gebruik system fonts in plaats van externe webfonts
- comprimeer afbeeldingen
- gebruik lazy loading voor media

- Toegankelijkheid (Accessibility)
Gebruik CSS media queries zoals prefers-reduced-motion om animaties uit te schakelen voor gebruikers die gevoelig zijn voor beweging. Dit voorkomt usability-problemen en maakt je site inclusiever.
Eigen server draaien
Het opzetten van een eigen server geeft maximale controle over je content en infrastructuur. Dit kan al eenvoudig met tools zoals Python of Node.js die een lokale server starten vanuit een map met HTML-bestanden.
Best practices

- Do’s
Bouw en beheer zoveel mogelijk zelf
Host je eigen server
Gebruik static site generators
Kies voor system fonts
Comprimeer afbeeldingen
Denk aan toegankelijkheid
Gebruik lazy loading
Hergebruik oude hardware

- Don’ts
Vermijd volledige afhankelijkheid van big tech
Gebruik geen animaties zonder fallback
Accepteer geen apparaten die niet te repareren zijn
Zet niet al je content op gesloten platformen
Actiepunten
Zet een eigen server op (bijvoorbeeld met een oude computer)
Installeer serversoftware zoals Nginx of een simpele static server
Maak en host je eigen website
Bekijk alternatieven zoals http://prikbord.page
Experimenteer met static site generators
Implementeer prefers-reduced-motion in je CSS
Start of sluit je aan bij een studiecirkel over self-hosting

**feedback sessie**
tijdens de feedback sessie heb ik mijn opdracht besproken in de groep en wat ik uiteindelijk wil gaan maken. Ik verteld welke api's ik van plan ben te gebruiken om de eindresultaat te realiseren. Ik kreeg van Jad te horen dat als ik de web speech api wil gaan gebruiken dat ik ook gebruik moet gaan maken van de Web AI api zodat die de speech kan translate naar een mood. Ik heb besloten om dat te gaan doen als extra voor als ik extra tijd over heb.

### Weeksamenvating 1
Deze week heb ik mijn idee voor de API-opdracht uitgewerkt en een begin gemaakt door te kijken naar welke api's ik kan gaan gebruiken en welke api's er zijn. Ik wil een movie website maken waarbij gebruikers op basis van hun mood een passende film kunnen vinden. Daarvoor heb ik gekozen om de TMDB API te gebruiken als content API. Ik heb een eerste fetch gedaan naar de TMDB API en ben begonnen met het koppelen van moods aan filmgenres. Ook heb ik buttons gemaakt met een data-mood attribuut, zodat ik kan uitlezen welke mood de gebruiker kiest wanneer de gebruiker er op heeft geklikt.

Ik heb onderzocht hoe ik de gekozen mood kan doorgeven naar een andere pagina. Eerst wilde ik hiervoor localStorage gebruiken, maar ik kwam erachter dat dit client-side werkt en minder geschikt was voor mijn situatie, omdat ik de fetch server side doe. Daarom heb ik ervoor gekozen om de mood via de URL als param mee te geven en deze in Astro uit te lezen met Astro.url.searchParams.get("mood"). Ook heb ik geleerd dat Astro pagina’s standaard prerendered, en dat ik met export const prerender = false; kan zorgen dat de pagina dynamisch werkt met URL-parameters. Anders doet de fetch niks met wat de gebruiker heeft gekozen.

Deze week heb ik vooral geleerd hoe ik data-attributen kan gebruiken, hoe ik waarden uit buttons kan ophalen met .getAttribute(), hoe ik een fetch naar de TMDB API uitvoer, hoe URL search parameters werken en waarom server-side fetches belangrijk zijn om mijn API key veilig te houden.

## week 2/1
**Wat heb ik gedaan**
- fetch gedaan naar de tmdb movie api om de films op te halen.
- math random/floor gebruikt om een random film te tonen op basis van de genre.
- fetch informatie in de html gezet 

**Wat heb ik geleerd:**
- hoe ik layouts kan maken en importeren op verschillende pages. 
- hoe ik met const  = Astro.props; verschillende attribute kan mee geven aan een layout of components.
- de & is de begin van een query in de url en is om verschillende parrams te kunnen meegeven in een url.
- en de ? is om het begin van de extra parameters aan te geven.

**Wat ga ik morgen doen:**
Morgen wil ik een fetch doen naar de cast van de film die wordt opgehaald en kijken hoe ik components en layouts kan gebruiken.

## weekly nerd:
**Johan van stichting Accessibility**
Hij liet zien hoe iemand de screenreader gebruikt. Het was heel snel waardoor ik niet wist wat er gezegt werd of wat voor website het was. je hoorde veel click en links door de links die op de pagina zijn. het was de bol.com website.

Hij besefte dat hij niks toegankelijk kon maken zonder de mensen die daarmee gaan werken.

**4 basis principes van de wcag**
perceivable
operable
understandeble
robust 

je kan heel makkelijk de wcag verkeert te intepeteren. De wcag is een goede basis maar het is niet optimaal.

als de afbeelding decoratief is dan hoef je geen alt in te vullen omdat iemand met een screenreader er niks aan heeft.

een schermlezer heeft al heelveel functies. je hoeft niet onnodige functies toe te voegen anders gaat de screenreader dit ook op lezen.

je komt erachter door zelf een screenreader te gebruiken en ermee te oefenenen. met h kan je door alle headings gaan. hiervan hebben ze nog een aantal functies.

**vragen als je voor zo iemand ontwerpt**
wat maakt het voor haar of hem moeilijk 
wat heeft hij/zij nodig 
heb je een project van je zelf waar hij/zij zou afhaken

**voorbeeld 1: martijn**
martijn gebruikt websites helemaal ingezoomed. wat hij vervelend vind is:
- navigatie of andere elementen die schuiven wanneer je scrolled door de website.
- sticky headers
- captha die letters met een streep erdoor heen zijn lastig te lezen voor hem

een oplossing zou kunnen zijn om de annimatie weg te halen door een knop te klikken.

**wat martijn nodig heeft**
- schaalbaarheid
- contrast
- gerelateerde info bij elkaar 
- visuele indicatoren zoals een focusrant 

**voorbeeld 2: naduah**
ze heeft heel veel pijn en is vaak moe.

**wat voor problemen heeft ze tijdens het web gebruiken**
- velle kleuren
- website met veel informatie
- als ze lang moet zoeken naar wat ze nodig heeft.


**Voorbeeld 3: guido**
heeft asperger. 

loopt tegen:
- visuele prikkels
- audio prikkels

alles komt extra hard bij hem binnen. advertenties die te luid zijn of visueel te veel willen doen. De website wordt dan onbruikbaar voor hem. wil met drie kliks iets kunnen vinden. anders wordt het te veel voor hem.

**wat werkt voor hem**
- voorspelbaarheid
- rustige layout en vormgeving
- duidelijke instucties en meldingen 

## week 2/2
**Wat heb ik gedaan**
- component gemaakt voor de buttons.
- layout gemaakt van de head van de html om het op verschillende pagina's te gebruiken.
- fetch gedaan naar de cast van de films die ik ophaal met de randomindex.
- poster van de film opgehaald en de backdrop

**Wat heb ik geleerd:**
Ik heb ontdekt dat als ik gebruik maak van mathrandom ik niet nog - 1 hoeft te doen om de laatste film op te kunnen halen. Math.random houdt hier al rekening mee. IK had eerst -1 gebruikt maar het bleek steeds dat ik errors kreeg bij bepaalde indexen. door die -1 weg te halen was dat opgelost.

**Wat ga ik volgende week doen:**
Volgende week wil ik een begin maken aan de functie om een film op te kunnen slaan met localstorage api.

**feedback sessie**
Tijdens de feedback sessie ben ik erachter gekomen dat localstorage api te klein is om te tellen voor mijn cijfer. Ook is het belangrijk dat ik een creatief deel creeer. Ik ben van plan iets met carousel te doen en of viewtransitions. Voor de rest was mijn idee goed en de code ook wel.

### Weeksamenvating 2
Deze week heb ik de resultatenpagina verder opgebouwd. Ik heb een fetch gedaan naar de TMDB Movie API om films op te halen op basis van de gekozen mood en het gekoppelde genre. Daarna heb ik met Math.random() en Math.floor() een willekeurige film uit de resultaten gekozen. Van deze film heb ik informatie zoals de titel, beschrijving, poster en backdrop opgehaald en in de HTML getoond.

Ook ben ik verder gegaan met het opdelen van mijn project in herbruikbare onderdelen. Ik heb gewerkt met layouts en components, zodat ik dezelfde structuur op meerdere pagina’s kan gebruiken. Daarbij heb ik geleerd hoe ik met Astro.props waardes kan meegeven aan een component of layout. Daarnaast heb ik een fetch gedaan naar de cast van de gekozen film, zodat ik castinformatie kan tonen die hoort bij de random film.

Deze week heb ik vooral geleerd hoe URL-query’s werken, zoals het verschil tussen ? en & in een URL. Ook heb ik beter leren werken met Math.random() en Math.floor(). Ik kwam erachter dat ik geen -1 hoef te doen bij het berekenen van een random index, omdat Math.random() nooit precies 1 wordt. Door die fout weg te halen kreeg ik geen errors meer bij bepaalde indexen. Tijdens de feedbacksessie heb ik geleerd dat localStorage waarschijnlijk te klein is als hoofd-Web API voor mijn beoordeling, waardoor ik ben gaan nadenken over andere toepassingen zoals een carousel en View Transitions.

## week 3/1
**Wat heb ik gedaan**
- Een aparte Cast.astro component gemaakt om castleden herbruikbaar te tonen.
- De castleden uit de TMDB API op de resultatenpagina gezet.
- Per castlid de naam, afbeelding en rol in de film getoond.
- Een link toegevoegd zodat je vanaf een castlid naar een detailpagina kunt gaan.
- De id en castname van een castlid meegegeven via de URL zodat je op de resultaten pagina de details kan tonen van die cast lid.

**Wat heb ik geleerd:**
Ik heb geleerd hoe ik componenten kan gebruiken om mijn HTML overzichtelijker en herbruikbaarder te maken. In plaats van dezelfde structuur steeds opnieuw te schrijven, kan ik één component maken en daar verschillende data aan meegeven met Astro.props. Dit heb ik toegepast bij de castkaarten, waarbij ik de data uit de TMDB API doorgeef aan mijn Cast.astro component.

Ook heb ik geleerd hoe ik met .map() meerdere castleden kan renderen op basis van de API-data. Voor elk castlid wordt automatisch dezelfde component gebruikt, maar met andere informatie zoals de naam, afbeelding en rol. Daarnaast heb ik geleerd hoe ik informatie via de URL kan meegeven, bijvoorbeeld de id en castname van een castlid. Daardoor kan ik op een detailpagina de juiste data ophalen op basis van de waarde uit de URL. Hierdoor begrijp ik beter waarom componenten handig zijn wanneer dezelfde soort content meerdere keren terugkomt, zoals bij castkaarten.

**Wat ga ik volgende keer doen:**
Volgende keer wil ik een aparte detailpagina maken voor een acteur. Op die pagina wil ik de id en naam uit de URL halen met Astro.url.searchParams.get(). Daarna wil ik met de actor id een fetch doen naar de TMDB person API, zodat ik extra informatie kan tonen zoals de profielfoto, geboortedatum, geboorteplaats, afdeling en biografie. Ook wil ik onderzoeken hoe ik Astro View Transitions kan gebruiken om de overgang tussen de castkaart en de detailpagina mooier te maken.

## week 3/2
**Wat heb ik gedaan**
- Een aparte castDetailsPage.astro gemaakt voor de detailpagina van een acteur.
- Met Astro.url.searchParams.get() de actor id en naam uit de URL gehaald.
- Een fetch gedaan naar de TMDB person API om extra informatie over een acteur op te halen.
- De profielfoto, geboortedatum, geboorteplaats, afdeling en biografie van de acteur getoond.
- Astro View Transitions toegevoegd tussen de castkaart en de detailpagina.

**Wat heb ik geleerd:**
Ik heb geleerd hoe ik een aparte detailpagina kan maken voor een castlid en hoe ik data via de URL kan hergebruiken op die pagina. Met Astro.url.searchParams.get() kan ik de id en naam van een acteur uit de URL halen en die gebruiken om een nieuwe fetch te doen naar de TMDB person API. Daardoor kan ik per acteur specifieke informatie tonen, zoals de profielfoto, geboortedatum, geboorteplaats, afdeling en biografie.

Ook heb ik geleerd hoe Astro View Transitions werken tussen twee pagina’s. Door dezelfde transition:name te gebruiken op de castafbeelding en de detailafbeelding kan Astro een overgang maken tussen de castkaart en de detailpagina. De animatie wordt gekoppeld doordat elke castafbeelding een unieke transition name krijgt op basis van de actor id, bijvoorbeeld "cast" + castMember.id. Op de detailpagina gebruik ik dezelfde naam opnieuw met "cast" + actorId. Daardoor begrijpt Astro dat deze twee afbeeldingen bij elkaar horen en kan de afbeelding van de castkaart overgaan naar de afbeelding op de detailpagina. Met transition:animate bepaal ik vervolgens hoe die overgang beweegt. Hierdoor voelt de navigatie minder plotseling en wordt de relatie tussen de kaart en de detailpagina duidelijker.

**Wat ga ik volgende week doen:**
Volgende week wil ik verder werken aan de creatieve interactie van mijn project. Uit de feedback kwam naar voren dat de View Transition goed werkt, maar dat ik ook nog iets moet doen met de Web Animations API. Daarom wil ik een carousel maken of verbeteren waarbij de castkaarten animeren tijdens het scrollen. Mijn doel is dat de kaart in het midden meer naar voren komt en dat kaarten verder van het midden kleiner of meer naar achter worden geplaatst.

**feedback sessie**
Bij de feedback sessie hebben we het vooral gehad over het afronden van de eindopdracht. De toepassing van de viewtransition was goed alleen moet ik nog iets gaan doen met de annimations api. Dat gaat mijn focus zijn voor volgende week.

### Weeksamenvating 3
Deze week heb ik gewerkt aan het tonen van castleden en het maken van een detailpagina voor acteurs. Ik heb een aparte Cast.astro component gemaakt, zodat ik castkaarten herbruikbaar kan tonen op de resultatenpagina. De castdata haal ik op uit de TMDB API en geef ik per castlid door aan de component met Astro.props. Met .map() render ik automatisch meerdere castkaarten, waarbij elke kaart eigen data krijgt zoals naam, afbeelding en rol.

Daarnaast heb ik ervoor gezorgd dat je vanaf een castkaart naar een detailpagina kunt gaan. Hiervoor geef ik de id en castname van een castlid mee via de URL. Op de detailpagina lees ik deze waarden weer uit met Astro.url.searchParams.get(). Daarna doe ik met de actor id een nieuwe fetch naar de TMDB person API, zodat ik extra informatie over de acteur kan tonen, zoals de profielfoto, geboortedatum, geboorteplaats, afdeling en biografie.

Ook heb ik Astro View Transitions toegevoegd tussen de castkaart en de detailpagina. Door dezelfde transition:name te gebruiken op de castafbeelding en de detailafbeelding begrijpt Astro dat deze twee afbeeldingen bij elkaar horen. Met transition:animate bepaal ik hoe de overgang beweegt. Hierdoor voelt de overgang tussen de resultatenpagina en de detailpagina vloeiender en duidelijker.

Tijdens de feedbacksessie kreeg ik terug dat de View Transition goed werkt, maar dat ik ook nog iets moet doen met de Web Animations API. Daarom wil ik volgende week verder werken aan een creatieve interactie, zoals een carousel waarbij de middelste castkaart meer naar voren komt en kaarten aan de zijkant kleiner of verder naar achter worden geplaatst.

## week 4/1
**Wat heb ik gedaan**
- Een carousel gemaakt voor de castlijst op de resultatenpagina.
- De castlijst een cast-carousel class gegeven en elke castkaart een cast-card class.
- CSS scroll snap toegevoegd zodat de kaarten netjes naar het midden scrollen.
- Perspective en transform-origin toegevoegd om een 3D effect mogelijk te maken.
- Onderzocht hoe scrollLeft, offsetWidth en offsetLeft werken om het midden van de carousel te berekenen.

**Wat heb ik geleerd:**
Ik heb geleerd hoe ik een horizontale carousel kan opbouwen met CSS en hoe ik de castkaarten daarin goed kan positioneren. Door de castlijst een cast-carousel class te geven en elke kaart een cast-card class, kan ik de carousel en de individuele kaarten apart stylen en selecteren met JavaScript. Ook heb ik geleerd hoe CSS Scroll Snap werkt om kaarten naar het midden te laten snappen.

Daarnaast heb ik onderzocht hoe ik met JavaScript het midden van de carousel kan berekenen. Hierbij heb ik geleerd wat scrollLeft, offsetWidth en offsetLeft betekenen. scrollLeft geeft aan hoeveel pixels er horizontaal is gescrold, offsetWidth geeft de zichtbare breedte van een element en offsetLeft geeft de positie van een kaart vanaf de linkerkant. Door deze waardes kan ik berekenen welke kaart het dichtst bij het midden van de carousel staat. Ook heb ik geleerd dat perspective en transform-origin nodig zijn om later een 3D-effect te kunnen maken met transforms zoals translateZ() en scale().

**Wat ga ik volgende keer doen:**
Volgende keer wil ik de carousel verder uitbreiden met de Web Animations API. Ik wil berekenen hoe ver elke castkaart van het midden staat en die afstand gebruiken om de kaarten te animeren. Het doel is dat de middelste kaart groter en meer naar voren komt, terwijl de kaarten verder van het midden kleiner worden en meer naar achter lijken te staan.

## week 4/2
**Wat heb ik gedaan**
- De Web Animations API gebruikt om de castkaarten te animeren tijdens het scrollen.
- Berekend welke kaart het dichtst bij het midden van de carousel staat.
- Met Math.abs() en Math.min() een progress waarde gemaakt tussen 0 en 1.
- De kaarten groter of kleiner gemaakt op basis van hun afstand tot het midden.
- Met translateZ() de middelste kaart meer naar voren gezet en kaarten verder van het midden naar achteren geplaatst.
- fallback img ingesteld
- :global() gebruik je als een html element bijvoorbeeld in een layout zit maar je wilt stylen op de normale pagina

**Wat heb ik geleerd:**
Ik heb geleerd hoe ik de Web Animations API kan gebruiken om elementen te animeren met JavaScript. In mijn carousel bereken ik eerst waar het midden van de carousel is en daarna waar het midden van elke castkaart staat. Met Math.abs() bereken ik de afstand tussen de kaart en het midden, zonder dat de uitkomst negatief wordt. Daarna gebruik ik Math.min() om van die afstand een progress waarde te maken die maximaal 1 kan zijn.

Ook heb ik geleerd hoe ik die progress kan gebruiken om de animatie te bepalen. Als een kaart dicht bij het midden staat, blijft de scale groter en staat de kaart meer naar voren. Als een kaart verder van het midden staat, wordt de kaart kleiner en gaat hij met translateZ() meer naar achter.

**Wat ga ik volgende week doen:**
Volgende week wil ik mijn project verder afronden en verbeteren. Ik wil de styling van de pagina’s af maken, zodat de homepage, resultatenpagina en cast detailpagina beter bij elkaar passen. Ook wil ik de carousel nog testen en finetunen, zodat de animatie stabiel blijft tijdens het scrollen en goed werkt met fallback-afbeeldingen. Daarnaast wil ik mijn README verder af maken.

**feedback sessie**
Bij de feedback sessie hebben we het vooral gehad over het afronden van de eindopdracht. De toepassing van de viewtransition was goed alleen moet ik nog iets gaan doen met de annimations api. Dat gaat mijn focus zijn voor volgende week.

### Weeksamenvating 4
Deze week heb ik gewerkt aan de cast carousel op de resultatenpagina. Ik heb de castlijst omgezet naar een carousel en de lijst een cast-carousel class gegeven. Elke castkaart heeft een cast-card class gekregen, zodat ik de carousel en de losse kaarten apart kan stylen en selecteren met JavaScript. Ook heb ik CSS Scroll Snap getest om de kaarten netjes naar het midden te laten snappen.

Daarna heb ik onderzocht hoe ik met JavaScript kan berekenen welke kaart het dichtst bij het midden van de carousel staat. Hiervoor heb ik gewerkt met scrollLeft, offsetWidth en offsetLeft. Met deze waardes kan ik het midden van de carousel en het midden van elke kaart berekenen. Vervolgens heb ik de Web Animations API gebruikt om de castkaarten tijdens het scrollen te animeren.

Met Math.abs() bereken ik de afstand tussen een kaart en het midden zonder negatieve waardes te krijgen. Met Math.min() maak ik daar een progress waarde van tussen 0 en 1. Die progress gebruik ik om de grootte en diepte van de kaarten te bepalen. Kaarten dicht bij het midden blijven groter en staan meer naar voren, terwijl kaarten verder van het midden kleiner worden en met translateZ() naar achter lijken te gaan.

Ook heb ik een fallback image ingesteld voor castleden zonder afbeelding en geleerd waarom vaste image-formaten belangrijk zijn voor een stabiele carousel. Daarnaast heb ik geleerd wanneer je :global() in Astro gebruikt, bijvoorbeeld wanneer je een HTML-element wilt stylen dat eigenlijk in een layout staat.

## week 5
**wat heb ik gedaan**
- de styling van de pagina's afgemaakt
- readme afgemaakt

# Eind reflectie
Tijdens de api opdracht heb ik een movie website gemaakt waarbij gebruikers op basis van hun mood een film kunnen vinden. Ik ben begonnen met het onderzoeken van verschillende API’s en heb uiteindelijk gekozen voor de TMDB API als content API. Hiermee haal ik films, castinformatie en acteurdetails op. Door de gekozen mood via de URL mee te geven, kan ik deze server-side uitlezen in Astro en daarna een fetch doen naar de TMDB API.

Ik heb veel geleerd over het werken met Astro. Zo heb ik geleerd hoe ik pagina’s dynamisch kan maken met export const prerender = false, hoe ik query parameters kan uitlezen met Astro.url.searchParams.get() en hoe ik data kan doorgeven aan components met Astro.props. Door een aparte Cast.astro component te maken, werd mijn code overzichtelijker en kon ik castkaarten herbruikbaar tonen met .map().

Ook heb ik gewerkt met meerdere web API’s. Ik heb Astro View Transitions gebruikt om de overgang tussen een castkaart en de detailpagina vloeiender te maken. Daarnaast heb ik de Web Animations API gebruikt voor de cast carousel. Hierbij bereken ik met scrollLeft, offsetWidth en offsetLeft welke kaart het dichtst bij het midden staat. Met Math.abs() en Math.min() maak ik daar een progress waarde van, waarmee ik de kaarten groter, kleiner, naar voren of naar achter kan animeren met scale() en translateZ().

Een belangrijk leerpunt was dat kleine technische keuzes veel invloed kunnen hebben op hoe stabiel een interface voelt. Bij de carousel merkte ik bijvoorbeeld dat afbeeldingen zonder vaste afmetingen of ontbrekende afbeeldingen de berekening konden breken waardoor scroll snap raar deed. Daarom heb ik gewerkt met vaste formaten en een fallback image. Ook heb ik geleerd dat toegankelijkheid belangrijk blijft bij animaties, bijvoorbeeld door rekening te houden met prefers-reduced-motion.

Als ik verder zou werken aan dit project, zou ik de interacties nog meer verfijnen. Ik zou bijvoorbeeld de carousel stabieler maken op verschillende schermgroottes, de biografie op de detailpagina inklapbaar maken met een “Lees meer”-knop en misschien alsnog experimenteren met spraakinput of AI om een mood automatisch te herkennen. Over het algemeen ben ik tevreden met wat ik heb gebouwd, omdat ik meerdere API’s heb gecombineerd en beter ben gaan begrijpen hoe client-side interactie, server-side data en animatie samenkomen in één project.

## bronnen: 
**window.location.href**
https://stackoverflow.com/questions/7077770/window-location-href-and-window-open-methods-in-javascript

**TMDB api**
https://developer.themoviedb.org/docs/getting-started

**devine:vars:** Variabel van ss (server side) naar cs (client side) doorgeven.
https://docs.astro.build/en/reference/directives-reference/#definevars

**prerender weghalen:**
https://docs.astro.build/en/guides/upgrade-to/v5/#removed-support-for-dynamic-prerender-values-in-routes

**image oproepen**
https://developer.themoviedb.org/docs/image-basics

**math.random**
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random

**math.floor**
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor

**View-transitions**
https://docs.astro.build/en/guides/view-transitions/

**web annimation api**
https://developer.mozilla.org/en-US/docs/Web/API/Web_Animations_API/Using_the_Web_Animations_API

**scrollLeft**
https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollLeft

**offsetWidth**
https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/offsetWidth

**offsetLeft**
https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/offsetLeft

**math.abs**
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/abs

**math.min**
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/min

## AI bronnen
**Prompt gebruikt voor uitleg over waarom -1 hier niet werkt:**
"Ik gebruik in JavaScript `Math.floor(Math.random() * data.results.length - 1)` om een random film uit een array te kiezen, maar soms krijg ik de error `Cannot read properties of undefined`. Kun je uitleggen waarom de `- 1` hier fout gaat, waarom daardoor soms index `-1` ontstaat, en waarom `Math.floor(Math.random() * data.results.length)` wel goed werkt?"

**Prompt gebruikt voor uitleg over het berekenen van het midden van de carousel:**
"Ik maak een horizontale carousel in JavaScript en wil weten welke kaart het dichtst bij het midden staat. Wat heb ik nodig om het midden van de carousel te berekenen? Kun je uitleggen wat `scrollLeft`, `offsetWidth` en `offsetLeft` doen, hoe ik daarmee `carouselCenter` en `cardCenter` bereken, en hoe ik daarna met `Math.abs(carouselCenter - cardCenter)` de afstand tussen een kaart en het midden kan bepalen?"


