# Lau was here.

Laurence "Lau" Asencio's portfolio: a static website in plain HTML, CSS and JavaScript, with no build step.

## Open it on your computer

Double-click `index.html`. Everything works offline except the fonts, which load from Google Fonts.

## Put it online with GitHub Pages

1. On GitHub, create a new **public** repository. GitHub Pages is free for public repositories.
   - Name it `lauttey.github.io` to get the address <https://lauttey.github.io>.
   - Or give it any other name, like `portfolio`, to get `https://lauttey.github.io/portfolio/`.
2. Put the contents of this folder at the top level of the repository. `index.html` must sit next to the `assets` folder, not inside another folder. In PowerShell or Terminal, from this folder:

   ```
   git init
   git add .
   git commit -m "Portfolio"
   git branch -M main
   git remote add origin https://github.com/lauttey/REPOSITORY-NAME.git
   git push -u origin main
   ```

   You can also use **Add file → Upload files** on the repository page and drag in everything from this folder.
3. In the repository, open **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the **main** branch and the **/ (root)** folder, then click **Save**.
4. After a minute or two, the site is live at the address from step 1. Every new push updates it.

## What's where

| Path | What it holds |
|---|---|
| `index.html` | The whole page: layout, styles, scripts, and the text for the projects, gallery events and certificates |
| `assets/profile/` | The profile photos that rotate in the circle at the top |
| `assets/logos/` | Logos and tool icons (work experience, education, toolkit and the logos on the cards) |
| `assets/projects/<project>/` | Each project's card picture (`thumb`), popup cover (`cover`), whole cover for the full-screen viewer (`full`) and documentation photos (`photo-01`, `photo-02`, …) |
| `assets/gallery/<event>/` | Each gallery event's card picture, cover, whole cover photo and "More photos" |
| `assets/certificates/` | Certificate images; `thumbs/` holds the small ones on the shelf |
| `assets/files/` | Attachments, like the Monsoon AI submission PDF |
| `.nojekyll` | Tells GitHub Pages to serve the files exactly as they are |

## Changing pictures

- To swap a picture, replace its file with a new one that has the same name and format.
- Gallery and documentation photos also have their size listed in `index.html` (`w:` and `h:`, near the bottom). Update those if the new picture has a different shape.
- To add a profile photo, put it in `assets/profile/` and add its path to `PFP_PHOTOS` in `index.html`.
