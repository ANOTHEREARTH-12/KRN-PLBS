# KRN P&L / Balance Sheet Portal

A single-file web app (`index.html`) for KRN Tax Consultancy to prepare Trading, Profit & Loss and Balance Sheet statements for clients.

## Features

- Password screen with an animated character; the portal opens only after the correct password (only a salted hash is stored in the code)
- Client master (name, PAN, address, entity type, signatory) with every financial year stored under the client
- Trading account is optional; switch it off for service businesses
- Proprietorship, Partnership / LLP (interest, remuneration, profit sharing) and Company layouts
- Fixed-asset block with WDV depreciation feeding both P&L and Balance Sheet
- Create next FY: closing balances carry forward automatically
- Password lock on opening (set on first use; change it under Settings → Security)
- Export to PDF (horizontal T-format with schedules and signature block)
- Import clients and year figures from Excel / CSV; backup and restore as JSON

## Run locally

Open `index.html` in Chrome. No build step.

## Host on GitHub Pages

1. Repo **Settings → Pages**
2. Source: **Deploy from a branch**, Branch: `main`, Folder: `/ (root)`
3. Open `https://<your-username>.github.io/<repo-name>/`

## Data and privacy

- The password screen is a deterrent, not server-side security: anyone who can read the page source could bypass or attack it. Do not rely on it to protect sensitive data on a shared computer; use a strong password and keep the repo public only if that is acceptable.
- The password is a simple lock (stored as a salted hash in the browser). It does not encrypt the data.
- All client data is stored in the **browser's local storage** on the device being used. Nothing is uploaded to GitHub or any server.
- Use **Backup** regularly and keep the JSON files outside this repo (they are git-ignored).
- PDF export and Excel import load jsPDF, jsPDF-AutoTable and SheetJS from cdnjs, so they need internet access.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole application |
| `README.md` | This file |
| `.gitignore` | Keeps backups and OS files out of the repo |
