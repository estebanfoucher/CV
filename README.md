## CV MkDocs site

This repository hosts a minimalist CV website built with **MkDocs** (Material theme).

The source pages live in the `content/` directory and are rendered to a static site.

### Structure

- `mkdocs.yml` – MkDocs configuration (site name, theme, navigation, CSS).  
- `content/index.md` – Home page (photo, short intro, contact, LinkedIn, direct CV PDF link).  
- `content/cv.md` – Detailed CV in HTML/Markdown with embedded project videos and per‑internship report links.  
- `content/assets/` – Static assets (photo, videos, PDFs, CSS).

Existing files in `docs/` are kept as a separate data/archive area; the MkDocs site does **not** use `docs/` as its `docs_dir`.

### Assets

Assets used by the site are stored outside `docs/`:

- Photo: `content/assets/photo.jpg`  
- Videos: `content/assets/videos/3D-reconstruction_demo_clip.mp4` and  
  `content/assets/videos/tell_tales_demo_clip.mp4`  
- Reports: `content/assets/reports/report_2021.pdf`, `report_2022.pdf`, `report_2023.pdf`

To provide the main CV PDF download, place a file at:

- `content/assets/reports/CV.pdf`

or adjust the link in `content/index.md` to match your preferred filename.

If you add new media under `docs/`, copy them into `content/assets/…` before building:

```bash
cp docs/your_file.ext content/assets/your_file.ext
```

### Local preview

1. Install MkDocs and the Material theme (for example, via pip):

```bash
pip install mkdocs mkdocs-material
```

2. Serve the site locally:

```bash
mkdocs serve
```

Then open `http://127.0.0.1:8000/` in your browser.

### Build

To build the static site into the `site/` directory:

```bash
mkdocs build
```

The generated `site/` folder can be deployed to any static hosting provider.

### GitHub Pages deployment (optional)

One option is to use the built-in MkDocs deployment helper (it creates/updates a `gh-pages` branch):

```bash
mkdocs gh-deploy
```

This publishes the contents of `site/` to GitHub Pages without changing the existing `docs/` directory.


