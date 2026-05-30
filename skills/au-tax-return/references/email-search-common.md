# Gmail Search Patterns — Common (All Industries)

These patterns find receipts and invoices that are relevant to workers across all industries. Industry-specific vendor patterns are in the relevant `industries/` file.

## Date Range Filters

Append to every query:
- **FY 2025-26:** `after:2025/07/01 before:2026/06/30`
- **FY 2024-25:** `after:2024/07/01 before:2025/06/30`
- **FY 2023-24:** `after:2023/07/01 before:2024/06/30`

---

## Mega Queries (Broad Sweeps)

Start with these to gauge receipt volume before drilling into categories.

**All receipts/invoices:**
```
subject:(receipt OR invoice OR "tax invoice" OR "payment confirmation" OR "order confirmation" OR "payment receipt" OR "billing statement") after:YYYY/07/01 before:YYYY+1/06/30
```

**All subscriptions/renewals:**
```
subject:(subscription OR renewal OR "recurring payment" OR "auto-renewal" OR "plan renewal") (receipt OR invoice OR payment OR confirmation) after:YYYY/07/01 before:YYYY+1/06/30
```

**PDF invoices specifically:**
```
subject:(invoice OR receipt OR "tax invoice") has:attachment filename:pdf after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Australian Retailers (General)

```
from:(officeworks.com.au OR jbhifi.com.au OR harveynorman.com.au OR amazon.com.au OR kogan.com OR ebay.com.au OR ikea.com.au) subject:(receipt OR invoice OR "order confirmation" OR "tax invoice") after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Internet & Phone (All Workers)

```
from:(telstra.com OR telstra.com.au OR optus.com.au OR myoptus.com.au OR tpg.com.au OR aussiebroadband.com.au OR iinet.net.au OR internode.on.net OR vodafone.com.au OR amaysim.com.au OR belong.com.au OR superloop.com OR spintel.com.au) subject:(bill OR invoice OR receipt OR payment OR statement) after:YYYY/07/01 before:YYYY+1/06/30
```

Note: Only the work-related percentage is deductible. If using WFH fixed rate, these are already covered.

---

## Energy (For WFH Actual Cost Method)

```
from:(originenergy.com.au OR agl.com.au OR energyaustralia.com.au OR alintaenergy.com.au OR redenergy.com.au OR powershop.com.au OR momentum.com.au OR simply.com.au) subject:(bill OR invoice OR statement OR receipt) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Income Protection Insurance

**By keyword:**
```
subject:("income protection" OR "salary continuance" OR "income insurance") (invoice OR receipt OR premium OR renewal OR payment OR statement) after:YYYY/07/01 before:YYYY+1/06/30
```

**By insurer:**
```
from:(tal.com.au OR aia.com.au OR metlife.com.au OR zurich.com.au OR mlc.com.au OR onepath.com.au OR clearview.com.au OR nobleoak.com.au) subject:(premium OR invoice OR renewal OR receipt OR payment OR statement) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Donations (DGR Receipts)

```
subject:(donation OR "tax deductible" OR "tax-deductible" OR "DGR" OR "deductible gift" OR "gift receipt") (receipt OR "thank you") after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Payment Processors

Catches subscriptions and purchases routed through payment processors.

**PayPal:**
```
from:(paypal.com OR paypal.com.au) subject:(receipt OR payment OR "you sent" OR transaction OR "automatic payment") after:YYYY/07/01 before:YYYY+1/06/30
```

**Stripe:**
```
from:(stripe.com OR receipt@stripe.com) subject:(receipt OR payment OR invoice) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Conferences & Events (All Industries)

```
subject:("registration confirmation" OR "ticket confirmation" OR "event confirmation" OR "your ticket" OR "conference" OR "summit") from:(eventbrite.com OR humanitix.com OR ti.to OR tito.io OR meetup.com OR bizzabo.com OR swoogo.com OR hopin.com) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Education Platforms (General)

```
from:(udemy.com OR coursera.org OR pluralsight.com OR linkedin.com OR skillshare.com OR khanacademy.org) subject:(receipt OR payment OR invoice OR subscription OR enrollment OR purchase) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Books (General)

```
from:(amazon.com.au OR amazon.com OR booktopia.com.au OR bookdepository.com) subject:(receipt OR "order confirmation" OR invoice OR dispatch) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Office Furniture/Equipment (WFH)

```
from:(officeworks.com.au OR ikea.com.au OR amazon.com.au OR jbhifi.com.au OR harveynorman.com.au OR kogan.com) subject:(receipt OR invoice OR "order confirmation" OR "tax invoice") (desk OR chair OR monitor OR keyboard OR mouse OR headset OR webcam OR "standing desk" OR ergonomic) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Gmail Syntax Reference

| Syntax | Meaning |
|--------|---------|
| `from:(domain.com)` | Emails from a sender domain |
| `from:(a.com OR b.com)` | Emails from either domain |
| `subject:(word1 OR word2)` | Subject contains either word |
| `subject:("exact phrase")` | Subject contains exact phrase |
| `after:YYYY/MM/DD` | Emails after date |
| `before:YYYY/MM/DD` | Emails before date |
| `has:attachment` | Has attachments |
| `filename:pdf` | Has PDF attachments |
| `-from:(domain.com)` | Exclude sender |
