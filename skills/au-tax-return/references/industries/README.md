# Industry Guides

Each file in this directory is an industry-specific guide containing:
1. Common deductions for that industry
2. Industry-specific email search patterns
3. Links to the relevant ATO occupation guide
4. Common mistakes for that industry

## Available Industries

- **it-professional.md** — Software engineers, developers, IT managers, data scientists, cybersecurity, DevOps, and similar tech roles

## Adding a New Industry

1. Copy `_template.md` to `{industry-name}.md`
2. Fill in all sections — use the ATO's occupation-specific guides as a starting point: https://www.ato.gov.au/individuals-and-families/income-deductions-offsets-and-records/guides-for-occupations-and-industries
3. Add email search patterns for vendors common in that industry
4. Submit a pull request

### Guidelines
- Use the ATO's own occupation categories where possible
- Include specific vendor email patterns (not just generic "receipt" searches)
- Add the ATO occupation guide URL if one exists
- Include common mistakes specific to that industry
- Add salary benchmarks for MLS threshold context
- Test your email patterns against real Gmail syntax
