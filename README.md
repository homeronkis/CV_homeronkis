# Igor Kim — CV

Personal CV / portfolio site.

- **Rendered:** https://homeronkis.github.io/CV_homeronkis/
- **Plain text (ATS-friendly):** [`CV.md`](./CV.md)
- **Source:** [`index.html`](./index.html) + [`styles.less`](./styles.less)

## Stack of the page itself

Static HTML + Less (compiled in browser via less.js CDN) + Inter / JetBrains Mono via Google Fonts. No build step, no JS framework — deliberately simple so it loads instantly and doesn't break.

## Sections

- Hero with skim summary
- About (3 paragraphs)
- What I do best — five signature niches
- Experience — 7 entries from 2018 to present
- Stack — 8 grouped pill columns
- Contact

## Updating

```sh
git clone git@github.com:homeronkis/CV_homeronkis.git
# edit index.html / styles.less / CV.md
git commit -am "<change>"
git push
# GitHub Pages picks up automatically (~1-2 min)
```

## Why two formats

`index.html` is for humans — designed, animated, visually intentional. `CV.md` is for machines — Greenhouse / Lever / Workday ATS systems strip styling and parse plain text. Both are kept in sync.
