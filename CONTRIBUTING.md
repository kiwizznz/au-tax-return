# Contributing to AU Tax Return

Thanks for your interest in contributing! This is a Claude Code plugin that helps Australians organise their tax-related documentation.

## How to Contribute

### Reporting Issues

- Use [GitHub Issues](https://github.com/kiwizznz/au-tax-return/issues) to report bugs or suggest features.
- Include steps to reproduce any bugs.
- For tax-related suggestions, specify the relevant ATO form, schedule, or occupation guide.

### Submitting Changes

1. Fork the repository.
2. Create a feature branch from `main`.
3. Make your changes.
4. Submit a pull request against `main`.

## Adding a New Industry Guide

The most impactful contribution you can make is adding support for a new industry. Each industry guide lives in `skills/au-tax-return/references/industries/` and contains:

1. Common deductions for that industry
2. Industry-specific email search patterns (vendor domains, subject line patterns)
3. Links to the relevant ATO occupation guide
4. Common mistakes for that industry
5. Salary benchmarks (for Medicare Levy Surcharge context)

### Steps

1. Copy `skills/au-tax-return/references/industries/_template.md` to `{industry-name}.md`
2. Fill in all sections using the [ATO occupation guides](https://www.ato.gov.au/individuals-and-families/income-deductions-offsets-and-records/guides-for-occupations-and-industries) as a starting point
3. Add Gmail search patterns for vendors common in that industry
4. Test your email patterns against real Gmail syntax
5. Submit a pull request

### Industries We'd Love to See

- Healthcare / Nursing
- Trades (electricians, plumbers, builders)
- Education / Teachers
- Legal
- Finance / Banking
- Real estate
- Hospitality
- Transport / Logistics
- Creative / Media
- Government / Public sector

### Guidelines for Industry Guides

- **Reference the ATO.** All deduction guidance should be traceable to a published ATO resource.
- **Be specific with email patterns.** Include actual vendor domains and subject line patterns, not just generic searches.
- **Include common mistakes.** What does the ATO flag as audit targets for this industry?
- **Don't provide personalised advice.** Use language like "expenses in this category may be deductible" rather than "you can claim this."
- **Keep it current.** Note which financial year your rates and thresholds apply to.

## Other Contributions

- Improvements to the scanning strategy (better email patterns, fewer false positives)
- Better handling of specific tax scenarios (capital gains, crypto, HECS/HELP, private health insurance)
- Clarity and usability improvements to the skill workflow
- Bug fixes
- Documentation improvements

## Important Notes

- **This tool organises information, it does not provide tax advice.** See the README for the full legal disclaimer.
- **Accuracy matters.** If you're contributing tax-related guidance, reference the relevant ATO documentation.
- **Keep it current.** Australian tax rules change each financial year. Note which FY your contribution targets.
- **Language matters.** Avoid "you can claim" or "this is deductible" — use "may be deductible" or "consult your tax agent."

## Code of Conduct

Be respectful and constructive. We're all here to make tax time a bit less painful.
