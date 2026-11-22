# StockCommand

A free, browser-based inventory and warehouse management dashboard.  
Track SKUs, adjust stock, monitor low-stock alerts, and export CSV — no server, no account, no cost.

**Live URL after deploy:** `https://<your-github-username>.github.io/<repo-name>/`

---

## Three commands to go live

```bash
# 1. Create a new repo on GitHub (do this once at github.com/new, name it e.g. stockcommand)
#    Then run these commands from INSIDE this stockcommand/ folder:

git init
git add .
git commit -m "Launch StockCommand"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/<YOUR_REPO>.git
git push -u origin main

# 2. Enable GitHub Pages in the repo settings — one click:
#    Settings > Pages > Source: "GitHub Actions"
#    (GitHub will find the workflow automatically)

# 3. Wait ~60 seconds for the first Action to run, then visit:
#    https://<YOUR_USERNAME>.github.io/<YOUR_REPO>/
```

> **Every future push to `main` re-deploys automatically.** No extra steps.

---

## What's inside

| File | Purpose |
|------|---------|
| `index.html` | The full StockCommand app — all CSS and JS inline, zero dependencies |
| `.github/workflows/deploy.yml` | GitHub Actions workflow that publishes to Pages on every push to `main` |
| `README.md` | This file |

---

## Features

- **Dashboard** — KPI cards (SKU count, units on-hand, inventory value, low-stock / out-of-stock alerts) plus a recent movements table
- **Inventory** — Full product table with search, category / warehouse / status filters, pagination, inline edit and delete
- **Warehouses** — Capacity utilisation cards with colour-coded fill bars; add new warehouses
- **Low Stock** — Dedicated alert view listing every product below its reorder point with shortfall numbers
- **Stock Adjustment** — Add, remove, or set exact quantity with optional reason note; every change is logged
- **CSV Export** — One-click download of the full inventory as a spreadsheet-ready CSV
- **Persistent data** — All data lives in `localStorage`; nothing leaves the browser

---

## Enabling GitHub Pages (one-time, ~30 seconds)

1. Push this folder to a GitHub repo (see the three commands above).
2. In the repo on GitHub: **Settings → Pages → Build and deployment → Source → GitHub Actions**.
3. The workflow at `.github/workflows/deploy.yml` runs automatically on the next push (or trigger it manually: **Actions → Deploy StockCommand to GitHub Pages → Run workflow**).
4. GitHub shows the live URL at the top of the Pages settings panel once the first deploy completes.

---

## Customising

- **Rename the app** — change the `<title>` tag and `.logo` text in `index.html`.
- **Seed different products** — edit the `products` and `warehouses` arrays in the `seedData()` function near the top of the `<script>` block.
- **Clear seed data in the browser** — open DevTools → Application → Local Storage → delete the `sc_*` keys, then reload.

---

*Built by StockCommand — shift November 16 2026.*
