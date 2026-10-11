# FlyPath — GO & KEGG enrichment explorer

A public Drosophila enrichment interface for GitHub Pages. This directory is ready to upload; no build command, package installation, custom domain, or paid hosting is required for this frontend.

## Publish with GitHub Pages

1. Create a new **public** repository named `flypath-explorer` in your GitHub account.
2. Upload `index.html` at the repository root. You can also upload `build-info.json` and this README. The supplied `.nojekyll` file disables Jekyll if it is included; the single HTML page has no underscore asset folders and does not depend on Jekyll.
3. Open **Settings → Pages**. Set **Source** to **Deploy from a branch**, select **main** and **/(root)**, then **Save**.
4. Wait for the Pages deployment to finish and use GitHub's **Visit site** link. Its form is `https://YOUR-USERNAME.github.io/flypath-explorer/`.
5. Select **Load glycolysis example**, then **Run enrichment**. Confirm BP, MF, CC, and KEGG results appear. Download a full JSON result if you want to retain it.

Do not upload your research CSVs to the repository. Visitors select files inside the web app; the chosen gene column is submitted for analysis, not committed to GitHub.

## Analysis hosting and privacy

GitHub Pages hosts the interface. The existing public FlyPath service at `https://drosophila-kegg-explorer.wavystork1.chatgpt.site/api/enrich` still runs the analyses. The browser's address bar remains on `github.io`, but the backend hostname is visible in application source and network tools. This is not an offline app and it is not a migration of the backend.

Gene lists and optional custom backgrounds are sent to that service. GO queries go to g:Profiler; KEGG uses live reference downloads and the existing validated FlyPath enrichment engine. Neither the app nor this repository saves submitted lists or results. Export results before closing the page.

The backend permits noncredentialed JSON requests from HTTPS GitHub Pages origins. It must remain available and public for the frontend to work. A blocked network request or provider outage will be shown as an analysis error. No credentials, tokens, or private datasets are included in this package.

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
