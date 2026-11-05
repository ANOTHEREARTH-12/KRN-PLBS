# KRN P&L / Balance Sheet Portal

A single-file web app (`index.html`) for KRN Tax Consultancy to prepare Trading, Profit & Loss and Balance Sheet statements for clients.

## Features

- Client master (name, PAN, address, entity type, signatory) with every financial year stored under the client
- Trading account is optional; switch it off for service businesses
- Proprietorship, Partnership / LLP (interest, remuneration, profit sharing) and Company layouts
- Fixed-asset block with WDV depreciation feeding both P&L and Balance Sheet
- Create next FY: closing balances carry forward automatically
- Export to PDF (horizontal T-format with schedules and signature block)
- Import clients and year figures from Excel / CSV; backup and restore as JSON

## Run locally

Open `index.html` in Chrome. No build step.

## Host on GitHub Pages

1. Repo **Settings → Pages**
2. Source: **Deploy from a branch**, Branch: `main`, Folder: `/ (root)`
3. Open `https://<your-username>.github.io/<repo-name>/`

## Data and privacy

- All client data is stored in the **browser's local storage** on the device being used. Nothing is uploaded to GitHub or any server.
- Use **Backup** regularly and keep the JSON files outside this repo (they are git-ignored).
- PDF export and Excel import load jsPDF, jsPDF-AutoTable and SheetJS from cdnjs, so they need internet access.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole application |
| `README.md` | This file |
| `.gitignore` | Keeps backups and OS files out of the repo |
