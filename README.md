# Saudi e-invoicing reference data

Open data behind the CashHub e-invoicing reference (https://cashhubapp.com/en/e-invoicing-reference).

| File | What it holds |
|---|---|
| `data/codes.json` | 240 business rules from ZATCA's SDK 238-R3.3.8 and the XML implementation standard: official text, severity, family, where it appears in each, and for 40 of them the Arabic and English page links. |
| `data/glossary.json` | 37 e-invoicing terms with Arabic and English definitions and their place in ZATCA documents. |
| `data/zatca-waves.json` | Integration waves 1 to 25: revenue threshold, years counted, dates, and ZATCA's announcement links. |
| `data/penalties.json` | The 18 offences in ZATCA's violations classification guide (2nd edition, May 2024): the first-time action and the fine for each repeat, plus the older November 2021 figures for comparison. The penalty calculator (https://cashhubapp.com/en/zatca-penalty-calculator) reads the same file. |

Checked 2026-10-26. Every record carries its source. Rule text is ZATCA's own and stays in English as published.

## Licence

CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). Credit "CashHub e-invoicing reference" with a link. ZATCA's documents remain ZATCA's.

## Corrections

Open an issue with the code, what is wrong and a link to the ZATCA document, or use https://cashhubapp.com/en/correct-us.

## Updating

The site build writes these files (`tools/build_zatca_ref.py` in the site repo; `penalties.json` is `tools/data/zatca_ref_penalties.json`); copy them here after each reference change and add a line to CHANGELOG.md.
