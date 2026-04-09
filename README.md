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
canvas api 

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


weekly nerd:


feedback sessie
tijdens de feedback sessie heb ik mijn opdracht besproken in de groep en wat ik uiteindelijk wil gaan maken. Ik verteld welke api's ik van plan ben te gebruiken om de eindresultaat te realiseren. Ik kreeg van Jad te horen dat als ik de web speech api wil gaan gebruiken dat ik ook gebruik moet gaan maken van de Web AI api zodat die de speech kan translate naar een mood. Ik heb besloten om dat te gaan doen als extra voor als ik extra tijd over heb.

bronnen: 
**devine:vars:** Variabel van ss (server side) naar cs (client side) doorgeven.
https://docs.astro.build/en/reference/directives-reference/#definevars

**prerender weghalen:**
https://docs.astro.build/en/guides/upgrade-to/v5/#removed-support-for-dynamic-prerender-values-in-routes