# DealSlice

Turn a full deal data pull into a focused, task-ready export.

Drop in a CSV, CSV.GZ, TSV, JSON, XLSX or XLS deal pull, turn nested JSON into separate columns, pick the columns a task needs (or use a preset), filter by deal status and HQ, and download a clean CSV or Excel file.

**Your data stays in your browser.** Files are read and processed on your device and are never uploaded anywhere. Saved presets live in your own browser's local storage.

## Use it

Open the GitHub Pages link for this repository. No install or account needed.

## Run locally

It is a single static page. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Publish with GitHub Pages

Settings → Pages → Build and deployment → Source: **Deploy from a branch**, Branch: `main`, folder `/ (root)`. The site appears at `https://<owner>.github.io/<repo>/` within a minute or two.

## Notes

- React 18.3.1 and SheetJS (`xlsx`) 0.18.5 load from jsDelivr.
- SheetJS 0.18.5 has known advisories when reading untrusted spreadsheets (prototype pollution, ReDoS). Risk is low here because people open their own pulls, but upgrading to SheetJS 0.20.3+ from https://cdn.sheetjs.com is recommended (vendor `xlsx.full.min.js` into the repo and point the script tag at it).
