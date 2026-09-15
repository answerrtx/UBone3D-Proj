# UBone3D — Project Page

Project page for **UBone3D: Physics-Rectified Conditional Flow Matching for Anatomical 3D Shape Completion from Ultrasound**, accepted by ECCV 2026.

Modeled after the [Nerfies](https://github.com/nerfies/nerfies.github.io) template.

## Structure

```
UBone3D-page/
├── index.html            # the page (title, video, abstract, method, results)
├── .nojekyll             # serve static/ as-is on GitHub Pages
└── static/
    ├── css/
    │   ├── bulma.min.css     # bundled, no CDN needed
    │   └── index.css         # page-specific styles
    ├── images/
    │   ├── ubone3d_arc.png   # architecture overview (Method)
    │   ├── visa.png          # simulated-data comparison (Results)
    │   └── resb.png          # in-vivo comparison (Results)
    └── pdfs/
        ├── visa.pdf          # vector originals, linked from the figures
        └── resb.pdf
```

The figures under `static/images/` are rendered from the source PDFs; each one
links back to its vector original. To regenerate after editing a PDF:

```bash
pdftocairo -png -r 200 -singlefile static/pdfs/visa.pdf static/images/visa
```

The overview video is embedded straight from YouTube. Note that the embed will
report `Error 153` when `index.html` is opened over `file://` — that is a
null-origin restriction, not a page bug. Preview over HTTP (below) instead.

## Still to do

- Remove the "under construction" notice under the title, and the
  `(Page under construction)` suffix in the `og:title` meta tag.
- Restore a BibTeX section once the official DOI is available.

## Preview locally

```bash
cd UBone3D-page
python3 -m http.server 8000   # open http://localhost:8000
```

## Deploy

Pages source is **`main` / root** (`UBone3D-Proj` repo → Settings → Pages).
Every push to `main` redeploys automatically; the site is served at
`https://answerrtx.github.io/UBone3D-Proj`.

The `Jekyll site CI` workflow only runs a build check on push and pull request
— it does not deploy, and `.nojekyll` means Pages serves the files as-is.
