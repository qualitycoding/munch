# Munch

A hungry little blob is loose in the pantry at midnight. Eat every crumb, grab
the sour drops, and don't let the Rinds catch up to you.

Munch is a one-page maze-chase game — no build step, no dependencies, a
single `index.html` you can open directly or host anywhere that serves
static files.

**Play it live:** if GitHub Pages is enabled for this repository, it is served at
`https://qualitycoding.github.io/munch/`.

## Controls

- **Move:** arrow keys, WASD, or swipe the maze on a touch screen
- **Pause:** `P` or `Esc`
- **Mute:** the speaker icon under the maze

Your best score and your mute setting are saved in the browser's `localStorage`. The page loads its two
fonts from Google Fonts; offline it falls back to system fonts.

## How it plays

- Clear every crumb (`·`) to finish the level. The pace picks up each level.
- The four sour drops in the corners turn the tables for a few seconds —
  while they're active, the Rinds turn pale and you can eat them for points
  instead of losing a life.
- Watch for the occasional bonus cookie once a level is about half-eaten.
- Each of the four Rinds behaves a little differently:

  | Rind | Personality | Behavior |
  |------|-------------|----------|
  | Pip  | Reckless    | Charges straight at you |
  | Zest | Cunning     | Cuts you off ahead of where you're headed |
  | Fig  | Sneaky      | Splits the difference between you and Pip |
  | Peel | Shy         | Chases from a distance, backs off up close |

## Running locally

No build tools needed — just open the file:

```
open index.html
```

Or serve it (useful for testing on a phone on the same network):

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Publishing on GitHub Pages

1. Push this repo's contents to the `main` branch.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch",
   branch `main`, folder `/ (root)`.
4. Save. GitHub will publish the page at
   `https://<your-username>.github.io/<repo-name>/` within a minute or two.

The included `.nojekyll` file tells GitHub Pages to serve the files as-is,
without running them through Jekyll first.

## Credits

Built for the fun of it. Munch, Pip, Zest, Fig, and Peel are original
characters — no relation to anyone else's arcade cabinet.

## License

Apache License 2.0 — see `LICENSE`.
