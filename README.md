# The Capital Files

Canada's early-stage capital, rebuilt from the filings themselves.

An Open Nshipyard project. Charts: https://open.nshipyard.com/charts

## The problem, in three numbers

- **$75M of $1.75B.** Ottawa's Venture and Growth Capital Plan (announced October 22, 2026) gives pre-seed and seed $75M, 4.3% of the plan and its smallest stream. The fund-of-funds stream gets $700M. Fund-of-funds applications close January 21, 2027.
- **4 managers, 3 rounds.** HarbourVest, Kensington, Northleaf and Teralys won the federal fund-of-funds stream in 2013 ($340M), 2017 ($279M) and 2021 ($350M). Round four is the 2026 Growth VCCI stream.
- **15 days vs 322 days.** A US private raise becomes public data 15 days after first sale: Form D is structured XML with a free API, a nightly bulk download and a permanent company ID (CIK). The Canadian equivalent, Form 45-106F1, is filed within 10 days on SEDAR+ but published one PDF at a time: no bulk file, no API, no company ID. Ontario's exempt market dashboard, the best public extract in the country, took 322 days to publish 2024 raises (updated November 18, 2025).

## The build

Turn Form 45-106F1 exempt-distribution filings into the structured, bulk, queryable file the US gets from Form D:

1. Extract the public fields of Form 45-106F1 from SEDAR+ (issuer, head office, industry, security type, exemptions and dollars by jurisdiction, directors and officers). Schedule 1 purchaser identities are confidential and are never collected or published.
2. Validate totals against the Ontario Securities Commission's open exempt-market file and CVCA quarterly aggregates.
3. Join issuers to the federal Grants and Contributions file (2.3 GB open CSV) so a company's public support and private raises sit in one record.
4. Publish versioned data releases, an OpenAPI spec and a REST API under /api/v1, following the Open Nshipyard pattern.

## What exists today

- Three verified charts (EN and FR) in the Open Nshipyard gallery: the $1.75B split, the repeat fund-of-funds winners, and the 15-day vs 322-day publication lag.
- A live watch on round four: expressions of interest for the $700M fund-of-funds stream close January 21, 2027; winners are expected in spring 2027 based on prior rounds.

## Sources

- ISED, Venture and Growth Capital Plan news release and backgrounder, October 22, 2026
- ISED, VCAP and VCCI recipient lists, 2013 to 2021
- Auditor General of Canada, Spring 2016 Report 1 (VCAP)
- SEC EDGAR, Form D rules and data APIs
- CSA and BCSC guidance, Form 45-106F1 (SEDAR+, since June 9, 2023)
- Ontario Securities Commission, Exempt Market Dashboard and open file
- NACO and Startup Genome, March 2026 (seed gap); Leaders Fund, 2025 (headquarters cohorts)

Research notes and the verification log live with the charts. Every number in this repo traces to a published source named next to it.
