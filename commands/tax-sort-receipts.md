---
description: Sort downloaded receipt attachments into the correct tax return folders
argument-hint: [tax-return-folder e.g. tax-return-FY2024-25]
---

The user has downloaded receipt attachments from their email and dropped them into a `receipts-to-sort/` folder inside their tax return folder. Your job is to read each file, match it to the correct category, rename it clearly, and move it to the right place.

## Find the tax return folder

If an argument was provided, use: $ARGUMENTS

If no argument was provided, look for the most recent `tax-return-FY*` folder in the current working directory.

If no tax return folder exists, tell the user to run `/tax` first.

## Discover the structure

1. **Find all CSV files** in the tax return folder (including subfolders like `rental/`). These are your sources of truth — `deductions.csv`, `rental-schedule.csv`, or any other CSV the skill created.

2. **Find all `receipts-to-sort/` folders** — there may be one at the top level (for work deductions) and one under `rental/` (for rental property). Check all of them.

3. **Find all `receipts/` folders** and their existing subfolder structure. Don't assume specific folder names — the skill creates category folders like `D5-work-related/`, `plant-equipment/`, `expenses/`, etc. depending on the type of deduction. Work with whatever exists.

## Process

For each `receipts-to-sort/` folder found:

1. **Read the relevant CSV(s)** to understand what items have been identified and which categories they belong to.

2. **List all files** in the `receipts-to-sort/` folder.

3. **For each file**, read/examine it to determine:
   - What vendor it's from
   - What item or service it's for
   - The dollar amount
   - The date

4. **Match it to an item in a CSV** by comparing vendor, amount, and date. If there's a clear match, move the file to the correct `receipts/{category}/` subfolder with a clear name: `{vendor}-{brief-description}-{YYYYMMDD}.{ext}`

5. **If the receipt contradicts the CSV** (e.g., the CSV says "laptop" but the PDF is actually a router, or the amount is different), flag it to the user: "The CSV has this listed as 'Scorptec laptop — $XXX' but the receipt says 'TP-Link Deco XE75 (mesh router) — $XXX'. Should I update the CSV to match the receipt?" Always trust the actual receipt over the CSV entry.

6. **If no clear match**, ask the user:
   - "I found `receipt-12345.pdf` — it's a $XXX invoice from Officeworks dated DD/MM/YYYY. Which category does this belong to?" and offer the available categories as options.
   - If the item isn't in any CSV at all, ask if it should be added and to which CSV.

7. **If the folder contains both work deduction and rental CSVs**, and a receipt from an ambiguous vendor (e.g., Bunnings, IKEA, a tradesperson) could belong to either, ask the user: "This receipt could be for your work deductions or your rental property at [address] — which is it?" If they dropped it in the wrong `receipts-to-sort/` folder, move it to the correct one before sorting.

8. **After sorting all files**, update the relevant CSV(s) to add the receipt file path in the Receipt File column for each matched item.

9. **Report what was done:**
   - Files sorted and where they went
   - Files that couldn't be matched (still in `receipts-to-sort/`)
   - Any CSV entries updated or corrected
   - Any new items added

## Naming convention

Rename files to: `{vendor}-{brief-description}-{YYYYMMDD}.{ext}`

Examples:
- `lenovo-thinkpad-x1-20240915.pdf`
- `samsung-27in-monitor-20240803.pdf`
- `officeworks-standing-desk-20241022.pdf`
- `jetbrains-ide-subscription-20240701.pdf`
- `insurer-landlord-policy-20241219.pdf`
- `ikea-furniture-fitout-20260307.pdf`
- `solar-installer-panels-20260112.pdf`
