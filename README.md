# AU Tax Return

A Claude Code plugin that helps Australian workers organise their tax-related receipts and expenses for review by a registered tax agent.

## What It Does

- Scans your Gmail for receipts, invoices, and subscription confirmations from the financial year
- Categorises expenses by ATO deduction category (D1–D15)
- Adds general ATO guidance notes so your accountant has context
- Saves everything to a local folder — summary, CSV, receipt attachments, email references
- Prepares a draft email to your accountant with all documentation attached

The goal: you type `/tax`, answer a few questions, and walk away with a folder ready to send to your accountant.

## Industry Guides

The plugin includes industry-specific guidance for common deductions and email search patterns. Currently available:

- **IT / Tech Professionals** — software engineers, developers, IT managers, data scientists, DevOps, cybersecurity, AI/ML engineers

More industries can be added by the community — see [Contributing](#contributing).

## Installation

### Claude Desktop / Cowork App

```bash
git clone https://github.com/kiwizznz/au-tax-return.git
cd au-tax-return
zip -r ../au-tax-return.zip . -x '.git/*' '.DS_Store'
```

Then in the app: **Customize > Personal plugins > + > Upload plugin** and select the `au-tax-return.zip` file.

### Claude Code (CLI)

```bash
git clone https://github.com/kiwizznz/au-tax-return.git
claude --plugin-dir ./au-tax-return
```

## Usage

```
/tax                    # Prepares documentation for the most recent completed FY
/tax 2024-25            # Prepares documentation for a specific financial year
/tax-sort-receipts      # Sorts downloaded receipt attachments into the correct folders
```

### Workflow

1. Run `/tax` — it asks about your job and work arrangement, connects to Gmail, and scans your emails for receipts and invoices
2. It creates a `tax-return-FY{YEAR}/` folder with a summary, CSV, and `email-references.md` containing clickable Gmail links for each receipt
3. Click the links to download your receipt attachments and save them to `tax-return-FY{YEAR}/receipts-to-sort/`
4. Run `/tax-sort-receipts` — it reads each file, matches it to your deductions, corrects any misidentified items, and moves everything to the right `receipts/D{X}/` folder

### Requirements

- Claude Code or Claude Cowork with the Gmail MCP connector available
- A Gmail account with your purchase receipts

### Without Gmail

If Gmail isn't available, the plugin works in manual mode — it walks you through each deduction category and you provide the details. It still creates the full output folder.

## Output

The plugin creates a folder in your working directory:

```
tax-return-FY2024-25/
├── README.md                    # Overview for your accountant
├── deduction-summary.md         # Detailed breakdown of all items found
├── deductions.csv               # Structured data for import/review
├── accountant-email-draft.md    # Ready-to-send email text
├── email-references.md          # Links to original receipt emails
├── ato-guidance-notes.md        # Relevant ATO rules for items found
└── receipts/                    # Attachments organised by ATO category
    ├── D4-self-education/
    ├── D5-work-related/
    └── ...
```

## Contributing

We welcome contributions, especially new industry guides. To add support for a new industry:

1. Copy `skills/au-tax-return/references/industries/_template.md`
2. Fill in the industry-specific deductions, email search patterns, and common mistakes
3. Reference the relevant [ATO occupation guide](https://www.ato.gov.au/individuals-and-families/income-deductions-offsets-and-records/guides-for-occupations-and-industries)
4. Submit a pull request

See [CONTRIBUTING.md](CONTRIBUTING.md) for full guidelines.

## Disclaimer

**This is not a tax agent, and this is not tax advice.**

This is a free, open-source community tool that helps you **organise receipts and categorise expenses** — it's a documentation aid, not a tax return preparation service. It is not a registered tax agent or BAS agent under the [Tax Agent Services Act 2009](https://www.legislation.gov.au/Details/C2022C00170). It is not endorsed by or affiliated with the ATO or the Tax Practitioners Board.

Any ATO guidance included is general information sourced from publicly available ATO publications. It does not account for your individual circumstances. Expense categorisations are indicative only and may be inaccurate — AI makes mistakes.

**Always review outputs with a registered tax agent before lodging your return.** You can verify a practitioner's registration at the [TPB Public Register](https://www.tpb.gov.au/public-register).

This software is provided "as is" under the MIT license with no warranty of any kind. The authors and contributors accept no liability for any loss arising from use of this tool.

## License

MIT — see [LICENSE](LICENSE).
