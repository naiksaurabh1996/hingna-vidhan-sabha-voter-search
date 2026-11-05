# Hingna Vidhan Sabha — Voter Search (Demo)

A bilingual (English/Marathi) voter-roll search interface with filters, summary statistics, and CSV export. The project also includes a Google Colab notebook for OCR-based PDF-to-CSV/Excel processing.

## Contents

- `index.html` — standalone voter-search interface (public-safe demo with an **empty dataset**)
- `Roll_to_Search.ipynb` — Colab notebook for processing voter-roll PDFs into structured outputs

## Demo

Open `index.html` in a modern browser (Chrome, Edge, Firefox, or Safari). The interface loads without a server, but the public demo intentionally contains no voter records.

## Use the OCR notebook

1. Open `Roll_to_Search.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Create a Google Drive folder named `rolls_pdf` and place the authorized PDF files there.
3. Run the notebook cells from top to bottom.
4. Generated CSV/Excel/HTML files are written to `rolls_out`.

The notebook expects filenames containing `MAR` or `ENG` and a part number (for example, `MAR-82.pdf` or `ENG-82.pdf`).

## Add your own dataset locally

The included `index.html` has an empty embedded payload so no voter data is published in this repository. To build a populated search page, use the notebook's output/build step locally with data you are authorized to process.

**Do not commit electoral-roll data or populated HTML files to a public repository.** Electoral rolls can contain personal information such as names, ages, addresses, and EPIC identifiers. Keep real datasets and populated exports private, and share them only with authorized users in accordance with applicable rules.

## GitHub Pages

This repository can be published as a static demo:

1. Push the files to a GitHub repository.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and `/ (root)`, then save.
5. GitHub will show the published site URL after deployment.

The published page will be the empty-data demo unless you deliberately replace it with a dataset. Do not publish populated electoral-roll data.

## Notes

- The HTML is standalone and uses browser features including `DecompressionStream`; use a recent browser.
- OCR results may need manual review against the source PDFs.
