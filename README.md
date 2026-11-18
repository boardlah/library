# The Game Shelf — GitHub Pages board game library

A responsive board game collection site with 41 starter entries, search, five filters, game detail pop-ups, WhatsApp link and a browser-based admin editor.

## Files to upload

Upload these **six files** directly into the root of your GitHub repository:

- `index.html` — public board game catalogue
- `admin.html` — game and brand editor
- `styles.css` — responsive styling and brand colours
- `app.js` — catalogue, search, filters and game details
- `admin.js` — local admin editor, image uploads, JSON import/export
- `games.json` — **all games, image links, and brand settings**

`README.md` is optional and can also be uploaded.

## Publish to GitHub Pages

1. On GitHub, create a new repository, e.g. `boardgame-library`.
2. Select **Add file → Upload files**, and upload all six files **from inside this folder** (not a nested directory). Commit them to the `main` branch.
3. Go to **Settings → Pages → Build and deployment**. Choose **Deploy from a branch**, `main`, and `/ (root)`; save.
4. Your website will appear at `https://YOUR-USERNAME.github.io/boardgame-library/` after deployment. The admin editor is at `/admin.html`.

## Add, edit or remove games

1. Open `https://YOUR-USERNAME.github.io/boardgame-library/admin.html`.
2. Add or edit games, upload images, or update your brand name and logo. Your changes are saved as a **draft only in the browser you're using**.
3. Click **Export games.json** to download your complete updated collection.
4. On GitHub, open the repository's `games.json`, use **Add file → Upload files** and upload the downloaded file, replacing the existing `games.json`; commit the change. Alternatively open `games.json` in GitHub's editor and paste the new JSON contents.
5. Wait for GitHub Pages to rebuild, then refresh your public site. All visitors will see the changes.

**Important security limitation:** GitHub Pages is static. This admin interface does not have a password or a server-side database. Anyone can view the admin page and make **local drafts in their own browser**, but only someone with write access to your GitHub repository can publish changes. Do **not** put a GitHub personal access token into the site's code or browser local storage. If you want secure multi-device, one-click publishing, you will need authentication and a backend or managed CMS.

## Best cover image dimensions

**Recommended: 800 × 800 px (1:1 ratio), transparent PNG or WebP.** Keep the full game box/cover within the image with approximately 8–12% transparent padding. A transparent PNG makes game boxes stand out on the soft blue card background. Portrait or landscape images also work: the website uses `object-fit: contain`, so images are never cropped and all game cards stay aligned.

Uploaded images are automatically fitted on a transparent **800 × 800 canvas** and compressed as WebP with transparency, where browser support allows. This means no cropping. Upload files smaller than 15 MB. For faster websites, use files around 100–300 KB after optimisation.

**Note:** Uploaded images are embedded inside `games.json` as data URLs to make the workflow work with GitHub Pages alone. With many large images, `games.json` can become large and slow the website. For a large collection, it is better to upload optimised images into an `images/` folder in your repository and paste their URL/path, e.g. `images/beer-bread.webp`, into the admin image URL field. A plain relative path works too.

## Collection details

The 41 starting entries are supplied with preliminary approximate player counts, duration ranges, difficulty categories and audience tags. Some titles have multiple editions, regional editions or are recently published, so these values **must be reviewed against your actual rulebooks and boxes**, especially *Nak Makan Apa, Hikadyat Al-Kisah, Collect!, Excalibur, JinxO, Flip 7: With a Vengeance, Uno Flip Attack!* and *Flamecraft Duals*. Expansions are marked and may require their base game. Audience categories and difficulty levels are editorial classifications, not official publisher ratings.

For checking game information, the catalogue can be cross-checked with [BoardGameGeek](https://boardgamegeek.com/) and the publisher's official game page.

## Edit brand colours

Your primary brand colour `#2d658b` is set in `styles.css` as `--blue`. Secondary colours are defined alongside it at the start of the stylesheet.

## Local preview

Open the folder in VS Code and run a local web server (e.g. the Live Server extension). Opening `index.html` as a `file://` path can prevent the browser from loading `games.json` because of browser security restrictions.
