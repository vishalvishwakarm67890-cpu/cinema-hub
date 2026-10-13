# Cinema Hub

A clean, fast **movie discovery catalog** — built as a static site with plain HTML, CSS and JavaScript. No frameworks, no build step, no API keys.

Browse a hand-picked set of films from India and around the world. Search by title, actor or director, filter by genre, and tap any poster to open a detail view with the synopsis, cast, director, runtime and rating.

## Features

- **Search** across title, cast, director, genre and year
- **Genre filters** generated automatically from the catalog
- **Detail modal** with synopsis, cast chips and key facts
- **Generated poster art** — each poster is an inline SVG, so there are no external image dependencies
- **Responsive** layout that works on phones, tablets and desktop
- **Zero dependencies** — one self-contained `index.html`

## Tech

- HTML5 + CSS3 (custom properties, CSS grid, `aspect-ratio`)
- Vanilla JavaScript (no libraries)
- Fonts: system font stack, so nothing to download

## Run locally

Just open `index.html` in a browser. Or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Live site

Deployed with **GitHub Pages** from the `main` branch (root folder).

## Adding a film

Open `index.html`, find the `MOVIES` array in the `<script>` block, and add an object:

```js
{
  title: "Your Film", year: 2024,
  genres: ["Drama"], rating: 8.0, runtime: 120,
  director: "Director Name",
  cast: ["Actor One", "Actor Two"],
  synopsis: "A short description of the story.",
  colors: ["#4f46e5", "#1e1b4b"]   // poster gradient
}
```

The poster, filters and stats all update automatically.

---

*All film details are provided for information only.*
