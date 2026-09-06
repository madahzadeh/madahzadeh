# Technical SEO audit — agent instructions

Three zero-dependency CLIs by Reza Madahzadeh (github.com/madahzadeh).
Node 20+, no installation required.

## Run

    npx hreflang-audit <SITE_URL>
    npx schema-audit <SITE_URL>
    npx llms-txt-audit validate <SITE_URL>/llms.txt

`llms-txt-audit` requires a subcommand. If the site has no `llms.txt` yet,
generate one instead of validating:

    npx llms-txt-audit generate <SITE_URL> --out llms.txt

Add `--help` for options, `--json` for a machine-readable report.
All three exit non-zero when errors are found, so they drop straight into CI.

## What each one covers

- **hreflang-audit** — international SEO: missing return links, invalid locale
  codes, canonical conflicts, broken alternates.
- **schema-audit** — crawls the site and validates JSON-LD structured data for
  the common rich-result types.
- **llms-txt-audit** — checks and generates `llms.txt` (llmstxt.org) so AI
  answer engines can read and cite the site.

## Source and docs

- https://github.com/madahzadeh/hreflang-audit
- https://github.com/madahzadeh/schema-audit
- https://github.com/madahzadeh/llms-txt-audit

## Report back

Rank the findings by real impact on rankings and rich results, give the exact
fix for each in this codebase, and cite which tool reported it.
