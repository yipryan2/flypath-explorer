# FlyPath — GO & KEGG enrichment explorer

A public Drosophila enrichment interface for GitHub Pages. This directory is ready to upload; no build command, package installation, custom domain, or paid hosting is required for this frontend.

## Publish with GitHub Pages

1. Create a new **public** repository named `flypath-explorer` in your GitHub account.
2. Upload `index.html` at the repository root. You can also upload `build-info.json` and this README. The supplied `.nojekyll` file disables Jekyll if it is included; the single HTML page has no underscore asset folders and does not depend on Jekyll.
3. Open **Settings → Pages**. Set **Source** to **Deploy from a branch**, select **main** and **/(root)**, then **Save**.
4. Wait for the Pages deployment to finish and use GitHub's **Visit site** link. Its form is `https://YOUR-USERNAME.github.io/flypath-explorer/`.
5. Select **Load glycolysis example**, then **Run enrichment**. Confirm BP, MF, CC, and KEGG results appear. Download a full JSON result if you want to retain it.

Do not upload your research CSVs to the repository. Visitors select files inside the web app; the chosen gene column is submitted for analysis, not committed to GitHub.

## Features

- Paste genes or upload CSV/TSV with a selectable identifier column.
- GO Biological Process, Molecular Function, Cellular Component, and KEGG.
- Source-specific query/background counts and FDR methods.
- Multiple-parent GO graph, nested badges, ancestor/descendant highlighting.
- Sort/search/significance filtering, enrichment chart, CSV and JSON exports.
- Provider versions, annotation dates and analysis/retrieval timestamps.

## Verification

The original enrichment engine, mapping, GO normalization and new CORS suite passed 35 automated tests. The standalone bundle passed syntax, integrity and dependency checks. All React, React DOM, Lucide and CSS resources are bundled into `index.html` (about 282 KB), with no CDN runtime imports. Browser visual testing and a live GitHub Pages deployment require verification after upload.

Official setup guide: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
