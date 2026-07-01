# UBone3D — Project Page

Project page for **UBone3D: Physics-Rectified Conditional Flow Matching for Anatomical 3D Shape Completion from Ultrasound**.

Text-only page (no figures yet), modeled after the [Nerfies](https://github.com/nerfies/nerfies.github.io) template.

## Structure

```
UBone3D-page/
├── index.html            # the page (title, authors, abstract, method, results, BibTeX)
├── .nojekyll             # serve static/ as-is on GitHub Pages
└── static/css/
    ├── bulma.min.css     # bundled, no CDN needed
    └── index.css         # page-specific styles
```

## Before publishing

- Fill in the real links in `index.html` (search for `href="#"`): Paper PDF, arXiv, Data.
- Add figures later if desired: drop images into `static/images/` and add `<img>` tags to `index.html`.
- Update the `booktitle` in the BibTeX block once the venue is confirmed.

## Preview locally

```bash
cd UBone3D-page
python3 -m http.server 8000   # open http://localhost:8000
```

## Deploy

Push to the `UBone3D-page` repo, then **Settings → Pages → Source: `main` / root**.
The site will be served at `https://answerrtx.github.io/UBone3D-page`.
