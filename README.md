# DRAGON.MOVIE

> _Cinema, summoned with a single ID._

A cinematic streaming **front-end** for movies and TV. Search by title or paste an
IMDb ID, and Dragon.Movie will fan it out across three premium third-party players,
remember your watchlist, and pick up exactly where you stopped — all from a single
static `index.html` with **zero build step**.

[![Open Live Site](https://img.shields.io/badge/Open-Live%20Site-e0454a?style=for-the-badge)](https://dark-z-666.github.io/DRAGON-MOVIE/)
[![License: MIT](https://img.shields.io/badge/License-MIT-ffd166?style=for-the-badge)](./LICENSE)
[![Made with HTML, CSS, JS](https://img.shields.io/badge/Stack-HTML%20%2B%20CSS%20%2B%20JS-6f7bff?style=for-the-badge)](#tech)

---

## Why Dragon.Movie

Most "watch any movie" sites are loud, ad-soaked and ugly. Dragon.Movie is the
opposite — a **calm, premium UI** that respects your time:

- A **cinematic dark theme** (obsidian + ember + gold) and a **parchment light
  theme** that mirror it perfectly.
- Real **inline SVG iconography** — no emoji-as-icon kitsch.
- **Three player servers** with one-tap hot-swap, so a dead embed is one click
  away from a live one.
- **Zero tracking, zero cookies, zero accounts.** Watchlist + Continue Watching
  live in your browser's `localStorage` only.
- **Keyboard-first navigation.** Power users will feel at home.

---

## Features

| Area | What you get |
|------|--------------|
| **Hero search** | Type a title (e.g. _Inception_) or paste an IMDb ID (`tt1375666`) — Dragon.Movie auto-resolves the closest match via OMDb. |
| **Trending rail** | Curated 16-title rail, hydrated live from OMDb (real posters, ratings, genres, runtimes). |
| **Top TV rail** | 14 era-defining series, ditto. |
| **Continue Watching** | Auto-tracks every title you play (incl. exact season + episode for TV). Stored locally. |
| **Watchlist** | Heart any card or use the player's "Save" button. Persists across reloads. |
| **Command-palette search** | Press `/` anywhere — live OMDb search with poster thumbs, keyboard nav, copy-IMDb-ID, and one-click play. |
| **Premium player shell** | Glass UI · Movie/TV mode · Server pills · Native `<select>`s for Season/Episode (with title labels) plus +/− steppers · Fullscreen · Refresh · Share-link copier. |
| **Genre filter** | 12 genre chips that filter the Trending and Top TV rails in place. |
| **Theme toggle** | Cinematic dark ↔ parchment light, persisted. |
| **Mobile drawer nav** | Full-height slide-in menu with search and theme shortcuts. |
| **Toast system** | ARIA-live notifications for every state change (saved, copied, error, etc). |
| **Deep links** | `?id=tt1375666&type=movie` or `?id=tt0903747&type=tv&s=1&e=2` autoplay on load. |
| **SEO + Share** | OpenGraph + Twitter card meta, JSON-LD structured data, inline SVG favicon. |

### Keyboard shortcuts

| Key | Action |
|-----|--------|
| `/` | Open search palette |
| `F` | Fullscreen the player |
| `R` | Refresh / reload the embed |
| `T` | Toggle theme |
| `W` | Toggle the current title in your watchlist |
| `[` / `]` | Previous / next episode (TV only) |
| `Esc` | Close any modal / drawer |

---

## Tech

- **One file**, no bundler. Pure HTML + CSS + a single jQuery 3.6 script tag.
- **OMDb** for metadata (title, year, poster, rating, genre, runtime, season info).
- **Three embed providers**, used identically for movies and TV:
  - [`vidsrc.to`](https://vidsrc.to)
  - [`2embed.to`](https://www.2embed.to)
  - [`autoembed.co`](https://autoembed.co)
- **Fonts:** Playfair Display (display), Space Grotesk (UI), JetBrains Mono (IDs).
- **Storage:** `localStorage` for theme, watchlist, continue-watching.

The whole thing is a single `index.html` you can drop on GitHub Pages, Netlify,
Vercel, Cloudflare Pages, or any S3 bucket — no Node build, no toolchain.

---

## Local preview

```sh
git clone https://github.com/dark-z-666/DRAGON-MOVIE.git
cd DRAGON-MOVIE
python3 -m http.server 8080
# open http://localhost:8080
```

Or just open `index.html` directly in your browser — there's no API key to
configure (Dragon.Movie ships with a public OMDb demo key).

---

## Disclaimer

Dragon.Movie is a **UI front-end only**. It does **not host, upload, or store any
video files**. All playback is provided by independent third-party embed services
(vidsrc.to, 2embed.to, autoembed.co). Trademarks, posters and metadata belong to
their respective owners; metadata is fetched live from the [OMDb API](https://www.omdbapi.com/).

If you are a rights-holder and an embedded service hosts material that infringes
your rights, please contact the embed provider directly — Dragon.Movie has no
control over their content.

---

## License

[MIT](./LICENSE) — © Dark Z.
