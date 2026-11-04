# Bowornthat Kerdsong - e-portfolio (static site, v8)

Single-page bilingual (Thai / English) portfolio mirroring the printed Portfolio book (sections 01-10), with a vital-signs strip and a 2015-2027 timeline before the book sections.
Fonts: Google Fonts (IBM Plex Sans Thai, Noto Sans Thai, IBM Plex Mono) with system fallbacks; no external scripts.
No build tools are needed to host it.

## Publish on GitHub Pages
1. Create a GitHub repository (public on a free account).
2. Upload the **contents** of this `site/` folder to the repository root (`index.html`, `assets/`, `.nojekyll`, `README.md`).
   Each PDF is under 25 MB, the web-upload limit per file. `.nojekyll` is a hidden file - upload it from the terminal or create an empty file with that name on GitHub.
3. *Settings > Pages > Build and deployment*: Deploy from a branch, `main`, `/ (root)`. Save.
4. After a minute the site is live at `https://USERNAME.github.io/REPO/`. Check both languages on a phone, then generate the QR code from that exact URL.

Useful URLs: `.../?lang=en` opens English, `.../?lang=th` opens Thai. Default is Thai.

## Regenerate after editing
`python3 ../_src/build_site.py` (needs Python 3 with Pillow and beautifulsoup4). The script refreshes its mirror of the book build (`_src/bookref/`), re-exports every photo (metadata stripped, never cropped) and copies the newest CV and Portfolio (web) PDFs.

## Privacy note
The page carries `noindex, nofollow`, but anyone with the link can read it. The Personal block includes date of birth, home address and dormitory room, as in the CV and the book.
