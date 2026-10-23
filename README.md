# ToonClipz song games

Each folder is one finished, self-contained game. No build step.
The root `index.html` forwards straight to the current demo game, so the plain site link opens it.

## big-michael-michael/
Looze Cannon, "Big Michael Michael".

| File | What it is |
|---|---|
| `index.html` | The whole game (HTML, CSS and JavaScript in one file) |
| `big-michael-michael.mp3` | The song. Loaded by that exact name |
| `looze-closed.png` / `looze-open.png` | The singer, mouth closed and open. The game swaps them on every word |
| `cover.jpg` | End-screen cover and link-preview image |

Do not rename these files. `index.html` loads them by name from the same folder.

## Hosting
Any static host works. Two easy options:

- **Netlify:** connect this repo, leave the build command empty, set the publish directory to the repo root. The game is then at `https://<site>.netlify.app/big-michael-michael/`.
- **GitHub Pages:** Settings → Pages → deploy from the `main` branch, root folder. The game is then at `https://<user>.github.io/<repo>/big-michael-michael/`.

After it is live, change the `og:image` meta tag in `index.html` from `cover.jpg` to the full URL of the cover (for example `https://<site>.netlify.app/big-michael-michael/cover.jpg`), so links shared in DMs and bios show the cover.

## Adding the next artist
Copy the `big-michael-michael/` folder, rename it, and replace the song, art and the `PRESET` block near the top of the script in `index.html`. The `PRESET` block holds the title, artist, file names, chorus times and the note chart (built from the song's timed lyrics).
