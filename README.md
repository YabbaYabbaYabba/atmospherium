# 🔮 The Atmospherium

A small apparatus for brewing atmospheric image prompts, and it works with any generator.

Type a subject, pick a vibe, choose where the prompt is going, and reroll ingredients until the mood is right. The same brew is reshaped for each image model's preferred prompt style.

**Live app:** https://yabbayabbayabba.github.io/atmospherium/

## Supported targets

| Target | Prompt style | Negatives | Notes |
|---|---|---|---|
| Universal | Descriptive sentences | Inline "Avoid …" | Paste anywhere |
| Midjourney | Comma keywords + params | `--no` | `--ar`, `--stylize`, `--chaos`, `--weird`, `--raw`, `--v 8.2 / 8.1 / 7` |
| Stable Diffusion / SDXL | Weighted tags | Separate field | Subject weighting, quality tags, suggested SDXL resolution |
| Flux | Descriptive sentences | None (Flux ignores them) | |
| ChatGPT / GPT Image | Request in sentences | Inline | Aspect ratio stated in words |
| Gemini / Imagen | Request in sentences | Inline | Aspect ratio stated in words |
| Ideogram | Descriptive sentences | Separate field | Set the ratio in the toolbar |
| Adobe Firefly | Descriptive sentences | Inline | Set the ratio in the panel |
| Leonardo | Comma keywords | Separate field | Set dimensions in the sidebar |

## Features

- **9 vibes plus Chaos Brew:** Whimsical Wonder, Eerie Liminal, Gothic Romance, Solarpunk Bloom, Neon Feral, Rain-Soaked Noir, Cosmic Reverie, Analogue Summer, Nordic Calm
- **8 ingredient rows:** mood, light, palette, texture, motif, lens, finish and one odd detail
- Reroll one row or all of them, **lock** the rows you like, **edit** any phrase inline, or **leave a row out**
- Prompt length: short, standard or rich
- Random subject generator
- Copy the prompt and the negative prompt separately
- **Share links:** the whole brew is encoded in the URL
- **Recent brews:** the last 15 copied prompts, kept in your browser; tap one to restore it
- Light, dark or auto theme
- Keyboard shortcuts: `R` reroll · `C` copy · `S` random subject
- Works on phones. On iPhone, open it in Safari and choose Share → Add to Home Screen.

## Running it

It is a single self-contained `index.html` with no build step and no dependencies. Open it in a browser, or serve it with GitHub Pages.

## Adding your own vibes

Add an entry to the `VIBES` object in `index.html` with the same six keys (`mood`, `lighting`, `palette`, `texture`, `motif`, `quirky`). The new vibe is picked up automatically, Chaos Brew included.

## Licence

MIT
