# Bowornthat Kerdsong - e-portfolio (static site)

Single-page bilingual (Thai / English) portfolio. No build tools are needed to host it.

## Publish on GitHub Pages
1. Create a GitHub repository (for example `portfolio`). It must be public on a free account.
2. Upload the **contents** of this `site/` folder to the repository root (`index.html`, `assets/`, `.nojekyll`, `README.md`).
   Via the web: *Add file > Upload files*, drag the contents in, commit. (`.nojekyll` is a hidden file - if your file manager hides it, upload it from the terminal or create an empty file with that name on GitHub.)
3. In the repository: *Settings > Pages > Build and deployment*. Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`. Save.
4. After a minute the site is live at `https://USERNAME.github.io/REPO/`. Open it on a phone, check both languages, then generate the QR code from that exact URL.
5. Optional: add the two Open Graph lines marked `TODO` in the `<head>` of `index.html` (absolute `og:url` and `og:image`) so link previews show the photo.

Useful URLs: `.../?lang=en` opens English, `.../?lang=th` opens Thai. Default is Thai.

## Regenerate after editing content
Edit the JSON files in `../_src/`, then run `python3 ../_src/build_site.py` (needs Python 3 with Pillow). The script rebuilds `index.html`, re-exports every photo (metadata stripped, max 1400 px) and re-copies the two CV PDFs, then runs its own checks.

## Privacy note
The page carries `noindex, nofollow`, but that only asks search engines to stay away - anyone with the link can read it. The Personal section includes date of birth, home address and dormitory room, as in the CV; remove blocks from the content JSON if you do not want them online.
