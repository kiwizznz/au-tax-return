# Income-Type Modules

Each file here covers an **additional income or asset type** a taxpayer might have beyond their salary/wages — rental property, sole-trader/ABN income, capital gains on shares or crypto, foreign income, and so on. The orchestrator (`SKILL.md` Step 1) asks which of these apply, then loads every module that matches.

## How this axis differs from `../industries/`

These are two separate extensibility axes — a return can use several modules from **both** at once:

| Axis | Folder | What it changes |
|---|---|---|
| **Occupation** | `../industries/` | Tweaks *work-related* deductions (D1–D15) for a job — vendors, certifications, memberships |
| **Income type** | `income-types/` (here) | Adds a *new income source and its schedule* — extra income, deductible expenses, depreciation, CGT |

A salaried developer with a rental and some sold shares would load `industries/it-professional.md` **and** `income-types/rental-property.md` **and** (one day) `income-types/shares-cgt.md`.

## Available income types

- **rental-property.md** — Residential investment/rental property (Div 40/43, borrowing costs, CGT, apportionment)

## Adding a new income type

1. Copy `_template.md` to `{income-type}.md` (e.g. `sole-trader.md`).
2. Fill in every section, citing the relevant ATO resource for each rule.
3. Write a clear **`Covers:`** header — the orchestrator matches modules to the user by reading it. List the situations the module applies to.
4. List the module's **`Output additions:`** so the orchestrator knows what extra files/sections to create.
5. Submit a pull request.

> Adding a module needs **no change to `SKILL.md` or the skill description** — the orchestrator discovers modules by listing this folder.

### Ideas we'd love to see

- Sole trader / ABN / business income (Schedule of business income & expenses)
- Capital gains — shares, ETFs, managed funds (CGT events, 50% discount, carry-forward losses)
- Crypto assets (disposals, staking income, record-keeping)
- Foreign income (foreign employment, foreign rental, foreign pensions, FITO)
- Managed investment trust / distribution income
