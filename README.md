# §754 Asset Allocation Tool

Single-file, browser-based tool for tracking per-partner ownership of §754 basis-adjustment
asset groups through buy-ins and buy-outs, and computing time-weighted annual allocation
percentages to apply against workpaper depreciation.

This repository publishes a previously built tool — v1.0, built April 24, 2026 (per file metadata).

## Use it

- **Hosted:** https://terminat0r4815.github.io/754-allocator/
- **Local:** download [`754-allocator.html`](754-allocator.html) and open it in any modern browser.

No install, no server, no dependencies. All data stays in your browser (localStorage).

## What it does

- **Partners** — partner roster with initial/current shares; paste lists straight from Excel
- **Transactions** — purchases (each creates a pooled §754 asset group), gifts (ownership
  transfer without a §754 asset), and share splits; Excel import supported
- **Allocation** — time-weighted annual allocation percentages per partner for each §754
  asset group, plus a cross-group summary for the selected year
- **Data** — JSON export/import, CSV export of allocations, print-friendly layout, and a
  built-in example dataset

## Notes

- Data is stored only in the browser's localStorage — use **Export JSON** for backups or to
  move data between machines.
- A purchase transaction pools all sellers into one §754 asset group; each buyer's units in
  the group equal the shares they bought.
