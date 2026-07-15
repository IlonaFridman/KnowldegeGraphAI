# AI Health-Chatbot Bibliometric Explorer

Single-file, offline-capable web app for the AI health-chatbot bibliometric dataset
(2,420 articles). **No install, no upload** — the dataset is embedded in `index.html`.

## Deploy on GitHub Pages (shareable link, nothing to install)
1. Create a repo and add: `index.html`, `data.json`, `.nojekyll`, `README.md`, `LICENSE`,
   **and the Step-3 output `citation_edges_doi.csv`** (copy it from your Analysis folder).
2. **Settings → Pages → Deploy from a branch → `main` / `/ (root)` → Save**.
3. Open `https://<username>.github.io/<repo>/`. Share that link — anyone uses the full
   app in a browser, no install and no upload.

## Automatic loading (when hosted)
Served over http/https, the app auto-loads from its own folder (or the parent folder):
- **`citation_edges_doi.csv`** → the **Network / cluster map** draws the true A→B
  citation network automatically (no upload).
- **`data.json`** → if present, overrides the embedded dataset (drop in a newer one
  without rebuilding `index.html`).

So for the citation network to work on GitHub, commit `citation_edges_doi.csv` alongside
`index.html`. Everything else works from the embedded data with nothing added.

## Run locally on Windows
Use the separate **`BiblioExplorer_Local.zip`** bundle (index.html + a one-click
`Start BiblioExplorer.bat` that runs a tiny built-in server so the citation network
auto-loads locally too).

## Features
Overview dashboard; most-cited table; clusters by study design / medical field /
research question; top authors and journals; interactive network / cluster-map builder
(group by field/question/design, or the true citation network; restrict to one field,
e.g. Oncology); global filters; CSV export with column selection; Save-as-PDF.

MIT-licensed.
