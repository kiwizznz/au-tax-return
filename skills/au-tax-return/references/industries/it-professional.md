# Industry Guide: IT / Tech Professional

**Covers:** Software engineers, developers, data scientists, DevOps/SRE, IT managers, tech leads, system administrators, cybersecurity professionals, AI/ML engineers, product managers (tech), UX designers (tech), IT consultants, enterprise architects, and similar tech roles.

**ATO occupation guide:** [IT professionals — income and work-related deductions](https://www.ato.gov.au/individuals-and-families/income-deductions-offsets-and-records/guides-for-occupations-and-industries/e-k/it-professionals-income-and-work-related-deductions)

> **Citation date:** May 2026. Applies to FY2024-25 and FY2025-26. Verify current rules at the ATO occupation guide link above.

---

## IT-Specific Deductions

### Technology & Equipment (D5)

Common purchases for IT workers:
- Laptops, desktops, monitors (often high-value — check depreciation rules in ato-general.md)
- Keyboards, mice, trackpads, USB hubs, docking stations
- Headsets, webcams, microphones (for meetings/calls)
- External storage drives, NAS devices
- Networking equipment (router, mesh WiFi — if for WFH)
- Cables, adapters, peripherals

**ATO effective lives for IT equipment:**

| Asset | Effective Life |
|-------|:-:|
| Laptop/notebook | 2 years |
| Desktop computer | 4 years |
| Computer monitor | 4 years |
| Printer | 5 years |
| Mobile phone | 3 years |
| Headset | 4 years |
| Router/networking | 4 years |

### Software & Subscriptions (D5)

Commonly claimed by IT professionals:
- **IDEs:** JetBrains (IntelliJ, WebStorm, PyCharm, DataGrip), Visual Studio
- **Dev tools:** GitHub Pro/Teams/Copilot, Docker, Postman, Figma, Linear, Notion
- **Cloud platforms:** AWS, Azure, GCP (for work/learning — not personal projects)
- **AI tools:** ChatGPT Plus, Claude Pro, GitHub Copilot, Cursor
- **Creative tools:** Adobe Creative Cloud (if used for work)
- **Security:** 1Password, antivirus/security software
- **Productivity:** Microsoft 365, Google Workspace (work portion)
- **Hosting:** Domain registrations, web hosting, DNS services
- **Communication:** Zoom, Slack (if personal subscriptions for work)

### Self-Education (D4)

IT-specific education that typically qualifies:
- **Cloud certifications:** AWS (SAA, SAP, DevOps, Security), Azure (AZ-900, AZ-104, AZ-305), GCP (ACE, PCA, PDE)
- **Security certifications:** CISSP, CEH, CompTIA Security+, OSCP
- **Agile/management:** Scrum Master, SAFe, PMP, PRINCE2
- **AI/ML:** Coursera/Udacity ML specializations, fast.ai
- **Platform-specific:** Kubernetes (CKA/CKAD), Terraform, Docker
- **University subjects:** Computer science, data science, cybersecurity (must relate to current role)
- **Conferences:** NDC Sydney, YOW!, DDD, Web Directions, PyCon AU, RubyConf AU, Agile Australia, AWS Summit, Microsoft Ignite, Google Cloud Next

**Does NOT qualify:**
- Bootcamps to switch from IT to a completely different career
- MBA (usually too general unless closely tied to current role)
- General interest courses unrelated to current tech work

### Professional Memberships (D3/D5)

- Australian Computer Society (ACS)
- IEEE
- ACM
- Professionals Australia
- ISACA (for governance/audit professionals)
- ISC2 (for CISSP holders)
- Agile Alliance
- Cloud-specific user groups (annual membership fees)

### Common Mistakes for IT Workers

1. **Double-dipping WFH:** Claiming phone/internet separately while using the 70c/hr fixed rate
2. **Not apportioning dual-use items:** Claiming 100% on a laptop also used for gaming/personal
3. **Claiming employer-provided gear:** Can't claim what your employer provides or reimburses
4. **Self-education for a new career:** Studying law or medicine while working as a developer
5. **Gaming/streaming subscriptions:** Not work-related even if on the same device
6. **Personal cloud projects:** AWS/Azure costs for personal projects aren't deductible
7. **Claiming commute:** Working from home some days doesn't make the commute deductible on office days

---

## IT-Specific Email Search Patterns

These supplement the common patterns in `email-search-common.md`. Replace `YYYY` with the financial year start.

### Hardware Vendors

**Major brands:**
```
from:(apple.com OR email.apple.com OR dell.com OR dell.com.au OR lenovo.com OR e.lenovo.com OR microsoft.com OR microsoftstore.com OR samsung.com OR samsung.com.au) subject:(receipt OR invoice OR "order confirmation" OR "tax invoice") after:YYYY/07/01 before:YYYY+1/06/30
```

**IT specialist retailers (AU):**
```
from:(centrecom.com.au OR mwave.com.au OR scorptec.com.au OR pccasegear.com OR ple.com.au OR msy.com.au OR umart.com.au) subject:(receipt OR invoice OR "order confirmation" OR "tax invoice") after:YYYY/07/01 before:YYYY+1/06/30
```

### Software & Dev Tools

```
from:(jetbrains.com OR github.com OR atlassian.com OR atlassian.net OR adobe.com OR 1password.com OR notion.so OR figma.com OR slack.com OR dropbox.com OR zoom.us OR openai.com OR anthropic.com OR cursor.com OR docker.com) subject:(receipt OR invoice OR payment OR subscription OR renewal) after:YYYY/07/01 before:YYYY+1/06/30
```

### Cloud Services

```
from:(amazonaws.com OR aws.amazon.com OR amazon.com OR azure.com OR azurecomm.net OR googlecloud.com OR digitalocean.com OR vercel.com OR netlify.com OR cloudflare.com OR namecheap.com OR godaddy.com OR render.com OR railway.app OR heroku.com OR linode.com OR hover.com) subject:(invoice OR receipt OR billing OR payment OR renewal) after:YYYY/07/01 before:YYYY+1/06/30
```

### IT Education & Certifications

**Online learning:**
```
from:(udemy.com OR coursera.org OR pluralsight.com OR acloudguru.com OR egghead.io OR frontendmasters.com OR educative.io OR codecademy.com OR oreilly.com OR packtpub.com OR manning.com OR pragprog.com OR leanpub.com) subject:(receipt OR payment OR invoice OR subscription OR enrollment OR purchase) after:YYYY/07/01 before:YYYY+1/06/30
```

**Exam providers:**
```
from:(pearsonvue.com OR credly.com OR kryterion.com OR webassessor.com OR youracclaim.com OR aws.training OR comptia.org OR certiport.com) subject:(exam OR certification OR registration OR receipt OR payment OR voucher) after:YYYY/07/01 before:YYYY+1/06/30
```

### IT Professional Memberships

```
from:(acs.org.au OR ieee.org OR acm.org OR professionalsaustralia.org.au OR isc2.org OR isaca.org OR agile-alliance.org) subject:(membership OR renewal OR invoice OR receipt OR payment OR "tax invoice") after:YYYY/07/01 before:YYYY+1/06/30
```

### Tech-Related Donations

```
from:(linuxaustralia.org.au OR wikimedia.org OR eff.org OR apache.org OR mozilla.org OR python.org OR fsf.org OR opensourcefoundation.org.au) subject:(donation OR receipt OR "thank you" OR "tax deductible") after:YYYY/07/01 before:YYYY+1/06/30
```

### Microsoft 365 / Google Workspace

```
from:(microsoft.com OR microsoftonline.com OR google.com OR payments-noreply@google.com) subject:(invoice OR receipt OR payment OR subscription OR "Microsoft 365" OR "Office 365" OR "Google Workspace" OR "Google One") after:YYYY/07/01 before:YYYY+1/06/30
```

---

## Salary Benchmarks (for context)

Typical salary ranges for IT professionals in Australia (2024-25):
- Junior developer: $60,000–$85,000
- Mid-level developer: $90,000–$130,000
- Senior developer/engineer: $130,000–$180,000
- Tech lead/principal: $160,000–$220,000
- Engineering manager: $170,000–$250,000
- IT consultant: $120,000–$200,000+

Most senior IT professionals earn above the MLS threshold ($97k/2024-25, $101k/2025-26) — flag private health insurance if they don't have hospital cover.
