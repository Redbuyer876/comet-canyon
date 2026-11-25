# Comet Canyon

A browser speed platformer. Zuzu the comet fell out of the night sky; run her home through three levels and three storm bosses before the sun comes up.

The whole game is one file, `public/index.html`. There is nothing to build or install.

## Play it locally

Open `public/index.html` in a browser.

## Updating the live site

The site is hosted on Cloudflare Workers as static files. Only the `public/` folder is published; nothing else in this repo is served. The settings are in `wrangler.jsonc`.

1. Change `public/index.html`.
2. Commit and push to `main`.
3. Cloudflare builds and deploys the push on its own, usually within a minute. A refresh shows the change.

The repo is connected to the `comet-canyon` Worker in the Cloudflare dashboard (Workers & Pages → comet-canyon → Settings → Builds). Build history and logs are under the Worker's Deployments tab.

To deploy by hand instead, run `npx wrangler deploy` from this folder. The first time on a new computer, run `npx wrangler login` and approve it in the browser.

## Chip in (tips)

The game is free to play. The **Chip in** buttons on the title screen (top right and under Start run) and on the results screen open a panel where a player picks an amount (it starts at $1) and pays with Cash App or Venmo.

The settings are near the top of the script in `public/index.html`, in the `TIP` block:

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
