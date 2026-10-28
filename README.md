# N5 Kanji

An installable study app for the 105 kanji commonly taught for JLPT N5. Each kanji has:

- its meaning and stroke count
- its Japanese reading (訓 kun'yomi) and Chinese reading (音 on'yomi), in hiragana and romaji
- an animated, numbered stroke-order diagram and a stroke-by-stroke strip
- at least three example words for each reading where they exist; tap a word to see each of its kanji drawn stroke by stroke

It is a single static page with no build step. Once loaded, it works offline.

## Publish with GitHub Pages

1. Upload all seven files to a GitHub repository, at the top level (on github.com: **Add file › Upload files**, select them all, **Commit changes**).
2. In the repository, open **Settings › Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, then **Save**.
4. After a minute the site is live at `https://<your-username>.github.io/<repository-name>/`.

## Install on iPhone or iPad

1. Open the site's URL in **Safari**.
2. Tap **Share › Add to Home Screen**, then **Add**.
3. Launch **N5 Kanji** from the home screen. It opens full screen.
4. Open it once while online. After that it works without a connection.

On Android or desktop Chrome, use the install icon in the address bar, or **⋮ › Install app** / **Add to Home screen**.

## Updating

After changing `index.html`, also change `VERSION` in `sw.js` (for example `n5-kanji-v2`). Installed copies pick up the new version the next time they are opened online.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: page, styles, script, kanji data and stroke data |
| `manifest.webmanifest` | App name, colours and icons for installing |
| `sw.js` | Service worker that caches the app for offline use |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | Home-screen and browser icons |

## Credits

Stroke-order data from [KanjiVG](https://kanjivg.tagaini.net) by Ulrich Apel, licensed [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). Fonts: Shippori Mincho and Zen Kaku Gothic New from Google Fonts.
