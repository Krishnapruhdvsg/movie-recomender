# Reel Good — Movie Night Picker

A lightweight movie recommendation project. Open `index.html` in a browser, choose a region, language, mood, and optional genre/runtime filters, then browse a four-film shortlist. The built-in catalog includes 100 Kannada titles. The app also queries the public Wikidata SPARQL endpoint without an API key, requesting up to 100 films per selected language. Wikidata has gaps in its movie metadata, so ratings, runtimes, genres, and descriptions may be unavailable.

## Run it

Open `index.html` in any modern browser. Live results need an internet connection. The browser calls `https://query.wikidata.org/sparql` directly; there is no API key or account setup. Google Fonts are an optional visual enhancement.

## Customize

Edit the `movies` array in `index.html` to add curated titles. Those entries are combined with live Wikidata results and deduplicated by title, so they remain available when public metadata is sparse. The live catalog is built from Wikidata's `film` type and original-language property, with publication date, runtime, and genre where available. The app filters returned records locally.
