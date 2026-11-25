# Comet Canyon

A browser speed platformer served as a static site by GitHub Pages from the `main` branch.

If `HANDOFF.md` exists in this folder, read it before doing anything else. It is a private, uncommitted file with the full project history, current state and the list of what needs doing.

## How the project works

- The whole game is `index.html`: styles, markup and script in one file. No build step, no packages. Open the file in a browser to run it.
- Keep it one file unless the owner asks otherwise.
- Sections of the script are marked with `/* ---------- name ---------- */` comments. Search for those instead of relying on line numbers.
- All music and sound effects are generated in the page with the Web Audio API. There are no audio files.
- Scores, the leaderboard, the player's tag and the music setting are saved in the player's own browser. There is no server.

## Rules

- **Pushing to `main` changes the live site.** Ask before pushing.
- **The repo is public.** Never commit secrets, private notes or personal details. `HANDOFF.md` is in `.gitignore` for that reason and must stay out of git.
- **Tips.** The `TIP` block near the top of the script controls the Chip in panel. Never set `live: true` unless the owner has given the real Cash App and Venmo handles in this session. Never invent or guess a handle. The game stays free to play and the wording stays "Chip in" or "Tip", not "Buy".
- **Originality.** Characters, art and music are original. Do not copy another game's characters, art or music.
- **Look.** Flat poster shapes, the six colors defined in `:root`, Bowlby One for display text, Chivo Mono for everything else.
- **Storage.** Every localStorage read and write stays inside try/catch, and the page must work with storage unavailable.

## Before calling a change done

Load the page at phone size (about 393×749) and in landscape, then:

1. Start a run and reach a results screen.
2. Check the leaderboard panel and the tag picker.
3. Open the Chip in sheet from the title and from the results screen.
4. Toggle music and sound.
5. Confirm the browser console shows no errors.

Say plainly what was checked by running it and what was not.
