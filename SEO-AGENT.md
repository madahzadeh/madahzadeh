# Technical SEO audit — agent instructions

Three zero-dependency CLIs by Reza Madahzadeh (github.com/madahzadeh).
Node 20+, no installation required.

## Run

    npx hreflang-audit <SITE_URL>     # international SEO: hreflang correctness
    npx schema-audit <SITE_URL>       # JSON-LD structured data / rich results
    npx llms-txt-audit <SITE_URL>     # llms.txt — AI answer-engine readability

Add `--help` for options, `--json` for a machine-readable report.
All three exit non-zero when errors are found, so they drop straight into CI.

## Source and docs

- https://github.com/madahzadeh/hreflang-audit
- https://github.com/madahzadeh/schema-audit
- https://github.com/madahzadeh/llms-txt-audit

## Report back

Rank the findings by real impact on rankings and rich results, give the exact
fix for each in this codebase, and cite which tool reported it.
