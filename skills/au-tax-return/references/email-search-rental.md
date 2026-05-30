# Email Search Patterns — Rental Property

Gmail search patterns for identifying rental-property-related transactions. Use these during the scanning phase when the user has investment/rental properties.

## Property Manager Communications

### Mega query — property manager statements and notices
```
subject:("owner statement" OR "landlord statement" OR "rental statement" OR "rent disbursement" OR "rent payment" OR "inspection report" OR "lease renewal" OR "tenancy agreement") after:YYYY/07/01 before:YYYY+1/06/30
```

### Common property management companies
```
from:(raywhite.com OR ljhooker.com.au OR harcourts.com.au OR mcgrath.com.au OR barryplant.com.au OR jelliscraig.com.au OR raineandhorne.com.au OR belleproperty.com.au OR bigginscott.com.au OR nelsonalexander.com.au OR professionals.com.au OR firstnational.com.au OR century21.com.au OR prd.com.au OR eldersrealestate.com.au) after:YYYY/07/01 before:YYYY+1/06/30
```

### Property management software platforms
```
from:(propertyme.com.au OR console.com.au OR managedapp.com.au OR ourtradie.com.au) after:YYYY/07/01 before:YYYY+1/06/30
```

### End-of-year / tax summaries
EOFY summaries are typically issued in July/August — extend the search past 30 June:
```
subject:("end of year" OR "EOFY" OR "annual summary" OR "tax summary" OR "financial year summary") from:(raywhite OR ljhooker OR harcourts OR mcgrath OR barryplant OR jelliscraig) after:YYYY+1/06/01 before:YYYY+1/09/30
```

---

## Landlord Insurance

### Mega query
```
subject:("landlord insurance" OR "landlord protection" OR "landlord preferred" OR "building insurance" OR "landlord policy") after:YYYY/07/01 before:YYYY+1/06/30
```

### Specialist landlord insurers
```
from:(terrischeer.com.au OR ebm.com.au OR rentcover.com.au) after:YYYY/07/01 before:YYYY+1/06/30
```

### General insurers with landlord products
```
from:(allianz.com.au OR qbe.com.au OR aami.com.au OR gio.com.au OR cgu.com.au OR nrma.com.au OR racv.com.au OR suncorp.com.au) subject:(landlord OR building OR property OR renewal) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Body Corporate / Strata

### Mega query
```
subject:("body corporate" OR "owners corporation" OR "strata levy" OR "levy notice" OR "levy assessment" OR "admin fund" OR "sinking fund" OR "capital works fund" OR "special levy") after:YYYY/07/01 before:YYYY+1/06/30
```

### Strata management companies
```
from:(picagroup.com.au OR whittles.com.au OR mbcm.com.au OR stratacare.com.au OR bcms.com.au OR ourbodycorp.com.au OR strataconnect.com.au) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Rates and Taxes

### Council rates
```
subject:("rate notice" OR "rates notice" OR "council rates") after:YYYY/07/01 before:YYYY+1/06/30
```

### Water rates
```
from:(sydneywater.com.au OR citywestwater.com.au OR southeastwater.com.au OR yvw.com.au OR unitywater.com.au OR sawater.com.au) after:YYYY/07/01 before:YYYY+1/06/30
```

### Land tax
```
from:(revenue.nsw.gov.au OR sro.vic.gov.au OR osr.qld.gov.au OR revenuesa.sa.gov.au) subject:(land tax) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Loan / Finance

### Annual interest statements (critical for deductions)
```
subject:("interest statement" OR "annual tax statement" OR "annual interest" OR "loan statement" OR "mortgage statement") after:YYYY/07/01 before:YYYY+1/06/30
```

### Bank loan communications
```
from:(commbank.com.au OR anz.com OR nab.com.au OR westpac.com.au OR macquarie.com OR ing.com.au OR bankwest.com.au OR suncorp.com.au OR athena.com.au OR ubank.com.au OR loans.com.au) subject:(loan OR mortgage OR interest OR statement) after:YYYY/07/01 before:YYYY+1/06/30
```

### Settlement / purchase (for cost base records)
```
subject:(settlement OR "settlement statement" OR conveyancing OR "trust account") after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Tradesperson / Maintenance

### Mega query — invoices from trades
```
subject:(invoice OR "tax invoice" OR quote) (plumber OR electrician OR painter OR locksmith OR gardener OR cleaner OR "pest control" OR handyman OR "air conditioning" OR "hot water") after:YYYY/07/01 before:YYYY+1/06/30
```

### Marketplace platforms
```
from:(hipages.com.au OR airtasker.com OR serviceseeking.com.au) after:YYYY/07/01 before:YYYY+1/06/30
```

### Franchise services
```
from:(jimscleaning.com.au OR jimsgroup.com.au OR flick.com.au OR terminix.com.au) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Furniture / Appliance / Fit-out Purchases

### Mega query — large purchases likely for rental fit-out
```
from:(ikea.com OR thegoodguys.com.au OR harveynorman.com.au OR appliancesonline.com.au OR templeandwebster.com.au OR fantasticfurniture.com.au OR freedom.com.au OR amartfurniture.com.au OR snooze.com.au OR sleepingduck.com.au OR beaconlighting.com.au OR bunnings.com.au) subject:(order OR receipt OR invoice OR confirmation OR delivery) after:YYYY/07/01 before:YYYY+1/06/30
```

### Made-to-measure / custom items (curtains, blinds)
```
subject:(curtain OR blind OR "made to measure" OR shutter) subject:(order OR invoice OR receipt OR confirmation) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Quantity Surveyor / Depreciation

```
from:(bmtqs.com.au OR washingtonbrown.com.au OR duotax.com.au OR mcgqs.com.au OR depreciator.com.au) after:YYYY/07/01 before:YYYY+1/06/30
```

```
subject:("depreciation schedule" OR "tax depreciation" OR "quantity surveyor") after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Solar / Energy Installations

```
subject:(solar OR "solar installation" OR "solar invoice" OR "feed-in tariff") after:YYYY/07/01 before:YYYY+1/06/30
```

### Energy companies (for rental property utility bills if landlord pays)
```
from:(originenergy.com.au OR agl.com.au OR energyaustralia.com.au OR redenergy.com.au OR alintaenergy.com.au) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Property Accountant / Tax Services

```
from:(thepropertyaccountant.com.au OR propertytaxspecialists.com.au) after:YYYY/07/01 before:YYYY+1/06/30
```

```
subject:("property tax" OR "rental schedule" OR "depreciation" OR "investment property") from:(accountant OR tax) after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Gmail Syntax Reference

Same syntax as `email-search-common.md` — see that file for full Gmail search operator reference.

Key operators for rental property scanning:
- `from:domain.com.au` — sender domain
- `subject:(word1 OR word2)` — subject line search
- `after:YYYY/MM/DD before:YYYY/MM/DD` — date range
- `has:attachment` — emails with attachments
- `filename:pdf` — specific attachment types
- `"exact phrase"` — exact match
- Combine with AND (space) and OR
- Use parentheses for grouping
