---
description: Sort downloaded receipt attachments into the correct tax return folders
argument-hint: [tax-return-folder e.g. tax-return-FY2024-25]
---

The user has downloaded receipt attachments from their email and dropped them into the `receipts-to-sort/` folder inside their tax return folder. Your job is to read each file, match it to the correct deduction category, rename it clearly, and move it to the right place.

## Find the tax return folder

If an argument was provided, use: $ARGUMENTS

If no argument was provided, look for the most recent `tax-return-FY*` folder in the current working directory.

If no tax return folder exists, tell the user to run `/tax` first.

## Process

1. **Read `deductions.csv`** from the tax return folder to understand what items have been identified and which ATO categories they belong to.

2. **List all files** in `receipts-to-sort/`.

3. **For each file**, read/examine it to determine:
   - What vendor it's from
   - What item or service it's for
   - The dollar amount
   - The date

4. **Match it to an item in `deductions.csv`** by comparing vendor, amount, and date. If there's a clear match, move the file to the correct `receipts/D{X}-{category}/` subfolder with a clear name: `{vendor}-{brief-description}-{YYYYMMDD}.{ext}`

5. **If the receipt contradicts the CSV** (e.g., the CSV says "laptop" but the PDF is actually a router, or the amount is different), flag it to the user: "The CSV has this listed as 'Umart laptop — $649' but the receipt says 'Ubiquiti UDM Dream Machine (router) — $649'. Should I update the CSV to match the receipt?" Always trust the actual receipt over the CSV entry.

6. **If no clear match**, ask the user:
   - "I found `receipt-12345.pdf` — it's a $649 invoice from Umart dated 22/10/2024. Which deduction does this belong to?" and offer the ATO categories as options.
   - If the item isn't in the CSV at all, ask if it should be added.

6. **After sorting all files**, update `deductions.csv` to add the receipt file path in the Receipt File column for each matched item.

7. **Report what was done:**
   - Files sorted and where they went
   - Files that couldn't be matched (still in `receipts-to-sort/`)
   - Any new items added to the CSV

## Naming convention

Rename files to: `{vendor}-{brief-description}-{YYYYMMDD}.{ext}`

Examples:
- `apple-macbook-pro-20240915.pdf`
- `jbhifi-dell-monitor-20240803.pdf`
- `umart-udm-dream-machine-20241022.pdf`
- `jetbrains-intellij-subscription-20240701.pdf`
