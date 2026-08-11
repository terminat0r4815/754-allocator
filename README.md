# §754 Asset Allocation Tool

Single-file, browser-based tool for tracking per-partner ownership of §754 basis-adjustment
asset groups through buy-ins and buy-outs, and computing time-weighted annual allocation
percentages to apply against workpaper depreciation.

This repository publishes a previously built tool — v1.0, built April 24, 2026.

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
- **JSON export/import** — the entire dataset travels as a single JSON file (see below)
- CSV export of allocations, print-friendly layout, and a built-in example dataset

## JSON export / import

Everything the tool knows — partners, transactions, and settings — exports to one dated JSON
file (`section754-state-YYYY-MM-DD.json`) via **Export JSON** in the footer, and
**Import JSON** restores that file exactly. Use it to:

- **Back up your work** — localStorage is per-browser and can be cleared, so export after
  meaningful changes
- **Move between machines or browsers** — export on one, import on the other
- **Share a scenario** — send the file to a colleague; importing reproduces your exact state
- **Keep per-engagement snapshots** — e.g., archive a year-end file for each partnership

## Notes

- A purchase transaction pools all sellers into one §754 asset group; each buyer's units in
  the group equal the shares they bought.
