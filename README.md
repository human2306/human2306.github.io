# Subhadeep — GitHub Pages Personal Archive

This version is designed for **GitHub Pages** and is driven by CSV files.

## Folder structure

```text
/
├── index.html
├── styles.css
├── app.js
├── .nojekyll
├── data/
│   ├── achievements.csv
│   ├── dj_sets.csv
│   └── movies.csv
└── images/
    └── home/
```

## 1. Home photos

Put homepage images in `images/home/` using:

```text
home_01.jpg
home_02.jpg
...
home_13.jpg
```

`.jpg`, `.jpeg`, `.png`, and `.webp` are supported. Missing files remain blank photo squares. Change `homeImageCount` near the top of `app.js` if you want more or fewer slots.

## 2. Achievements

Achievements need **no images**. The site automatically generates an original journal-cover-inspired design from the category and publication/venue name.

Edit `data/achievements.csv`. Columns:

```text
order,year,title,place,category,description,link
```

Example:

```csv
1,2026,My Paper,Nature Communications,Publication,"One-line description.",https://example.com
```

Useful categories: `Publication`, `Research`, `Talk`, `Fellowship`, `Scholarship`, `Award`.

## 3. The Decks

Edit `data/dj_sets.csv`. Columns:

```text
order,title,url,genre,duration,location,date
```

Paste a YouTube or SoundCloud URL and the page embeds it automatically.

## 4. Movies

Movies are intentionally **text-only**: title + year. No poster files are needed.

Edit `data/movies.csv`. Columns:

```text
order,title,year
```

Example:

```csv
1,Persona,1966
2,Perfect Days,2023
```

Add a row, commit to GitHub, and the list updates automatically.

## 5. Test locally

Because CSV files are loaded with JavaScript, use a local server rather than double-clicking `index.html`:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## 6. GitHub Pages

For a user site, use a repository named exactly:

```text
SubhadeepDuari.github.io
```

Publish from `main` / `/ (root)` in **Settings → Pages**.

## Normal update workflow

- Home: add/replace files in `images/home/`
- Achievements: edit `data/achievements.csv`
- The Decks: edit `data/dj_sets.csv`
- Movies: edit `data/movies.csv`

No routine HTML edits are needed.


## Achievement covers
Publication and milestone cards can use local image files placed in `images/achievements/`.
The current package includes built-in journal-cover-style images and achievement cover files already referenced from `data/achievements.csv`.


## Current home-photo filenames (13 slots)

This package is configured for 13 homepage photographs. Convert HEIC files to JPG before upload, because HEIC is not reliably supported across browsers. Then rename them to:

```text
home_01.jpg
home_02.jpg
home_03.jpg
home_04.jpg
home_05.jpg
home_06.jpg
home_07.jpg
home_08.jpg
home_09.jpg
home_10.jpg
home_11.jpg
home_12.jpg
home_13.jpg
```

A source-to-target mapping is included at `images/home/RENAME_MAP.txt`.

## Current achievement edits

Removed: DST-INSPIRE, EMBO Marseille, and Gold Medal.
`Scalable Computational Phenomics` is now labeled as a **bioRxiv preprint**.
