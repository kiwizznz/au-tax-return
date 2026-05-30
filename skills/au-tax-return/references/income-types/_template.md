# Income Type: [Name]

**Covers:** [The income/asset situations this module applies to. The orchestrator reads this line to decide when to load the module — be specific, e.g. "Sole traders and contractors operating under an ABN, including gig-economy and freelance income."]

**ATO reference:** [URL to the main ATO page for this income type]

> **Citation date:** [Month Year]. Applies to FY[XXXX-XX] and FY[XXXX-XX]. Verify current rules at the ATO link above.

**Output additions:** [What this module contributes to the return folder, e.g. a `{name}/` subfolder with `{name}-summary.md` and `{name}-schedule.csv`. Leave blank if it only adds rows to the main deduction summary.]

**Note:** Occupation/work-related deductions are handled by `../industries/`. Keep this module focused on the income type itself — don't duplicate D1–D15 work-deduction content here.

---

## Intake — Details to Gather

[The questions to ask the user up front when this income type applies. These drive email search, apportionment, and any CGT treatment. Use a bullet list, one item per detail, with a short note on why each matters.]

- **[Detail]** — [why it matters]
- **[Detail]** — [why it matters]

## Income (Assessable)

[How to identify and record income from this source. What must be declared, and any timing rules.]

| Income Type | Example |
|---|---|
| [Type] | [Example] |

## Deductible Expenses (Immediate)

[Expenses deductible in full in the year incurred, with any conditions.]

| Expense | Notes |
|---|---|
| [Expense] | [Notes] |

## Capital / Depreciation Treatment (if applicable)

[Depreciating assets, capital works, or other items spread over time rather than deducted immediately. Remove this section if not relevant to the income type.]

## CGT Implications (if applicable)

[Whether disposing of the asset triggers a CGT event, the cost base elements, discounts, and what records are needed. Remove if not relevant.]

## Email Search Patterns

_Supplement the common patterns in `../email-search-common.md` with searches specific to this income type._

### [Category Name]

```
from:([vendor1.com] OR [vendor2.com]) subject:(receipt OR invoice OR statement) after:YYYY/07/01 before:YYYY+1/06/30
```

## Common Mistakes / ATO Audit Targets

1. [Common mistake]
2. [Common mistake]

## Record-Keeping

[What records to keep and for how long. Note ATO retention periods.]
