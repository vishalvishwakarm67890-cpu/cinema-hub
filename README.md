# Cinema Hub

A **dark, cinematic streaming-style catalog** — built as a static site with plain HTML, CSS and JavaScript. No frameworks, no build step, no API keys.

Browse a hand-picked set of films from India and around the world in a Netflix-style layout: a featured hero banner, horizontally scrolling rows, poster thumbnails and a rich detail sheet. Then watch the trailer or find where to stream it **legally**.

## Features

- **Rotating hero banner** featuring trending films
- **Horizontal rows** — Trending Now, Top Rated, Made in India, Sci-Fi & Fantasy, Thrills & Crime, Family & Animation
- **Live search** across title, cast, director, genre, year and language
- **Detail sheet** with synopsis, director, cast, genres, runtime and rating
- **My List** — save titles to a personal watchlist (stored in your browser)
- **Trailer links** to YouTube
- **"Where to Watch"** links to legal platforms (JustWatch, Netflix, Prime Video, JioHotstar)
- **Generated poster & backdrop art** — every image is an inline SVG, so there are no external image dependencies
- **Responsive** — works on phones, tablets and desktop
- **Zero dependencies** — one self-contained `index.html`

## A note on content

Cinema Hub is a **catalog and discovery** site. It does **not** host, stream or link to any pirated movies. Every "watch" link points to an official, legal platform.

## Tech

- HTML5 + CSS3 (custom properties, CSS grid, `aspect-ratio`, backdrop blur)
- Vanilla JavaScript — no libraries
- System font stack, so nothing to download

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
  director: "Director Name", region: "India", language: "Hindi",
  cast: ["Actor One", "Actor Two"], trend: false,
  synopsis: "A short description of the story.",
  colors: ["#4f46e5", "#1e1b4b"]   // poster gradient
}
```

The hero, rows, search and stats all update automatically. Rows are defined in the `ROWS` array by a simple `pick` function.

---

*All film details are provided for information only. Cinema Hub links only to official platforms.*
