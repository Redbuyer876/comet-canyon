# Comet Canyon

A browser speed platformer. Zuzu the comet fell out of the night sky; run her home through three levels and three storm bosses before the sun comes up.

The whole game is one file, `index.html`. There is nothing to build or install.

## Play it locally

Open `index.html` in a browser.

## Updating the live site

The site is served by GitHub Pages from the `main` branch.

1. Change `index.html`.
2. Commit and push to `main`.
3. The live site picks up the change in about a minute. Phones may hold the old copy for up to ten minutes; a refresh fixes that.

### First-time hosting setup

In the repository on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main`, folder `/ (root)` → Save.**

The site address appears on that same page a minute later. Free GitHub accounts can only host Pages from a public repository.

## Chip in (tips)

The game is free to play. The **Chip in** button on the title and results screens opens a panel where a player picks an amount (it starts at $1) and pays with Cash App or Venmo.

The settings are near the top of the script in `index.html`, in the `TIP` block:

| Setting | What it is |
| --- | --- |
| `live` | `false` = demo mode. The pay buttons open nothing and the panel is marked DEMO. Set to `true` once the real handles are in. |
| `cashtag` | Cash App $cashtag, with the `$` |
| `venmo` | Venmo username, without the `@` |
| `amounts` | The dollar choices offered |
| `amount` | The choice selected when the panel opens |
| `note` | The note filled in on Venmo |
| `blurb` | The sentence shown at the top of the panel |

The handles in the file right now are placeholders, and `live` is `false`, so no money can be sent anywhere yet.

Link formats used:

- Cash App: `https://cash.app/$cashtag/AMOUNT`
- Venmo: `https://venmo.com/USERNAME?txn=pay&amount=AMOUNT&note=NOTE`

## What is saved, and where

Best times, the leaderboard, the player's three-letter tag and the music setting are saved in the player's own browser. They are not shared between devices, and there is no server.

## Sound

All music and sound effects are generated in the page with the Web Audio API. There are no audio files.
