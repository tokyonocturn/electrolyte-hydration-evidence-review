# Contributing

Corrections with a source are the most useful contribution. Please open an issue or a pull
request with:

1. The file and line you are correcting.
2. The source (DOI, PMID, regulator document, or a photograph or URL of the product label).
3. Whether the change affects a generated table.

## Editing data

The CSVs in `data/` are the single source of truth.

- `products.csv` and `references.csv` are comma-separated with quoted text fields.
- `evidence.csv`, `claims.csv`, `dosing.csv` and `standards.csv` use `|` as the delimiter.

After any change:

```bash
python analysis/build_tables.py
python analysis/build_tables.py --check
```

Commit the regenerated files in `docs/generated/` and `docs/references.md` with the data
change. A pull request that edits a generated table by hand will fail CI.

## Adding a product

- Use a stable slug id.
- Record sodium, potassium, magnesium and calcium per **stated serving at the stated
  dilution**. Use 0 and `*_decl = N` when the label does not declare a value; never guess.
- Record chloride only when the label states a milligram amount.
- Attach both a label URL and a price URL.
- State the price channel and the snapshot date.
- Add a note for label variants, scoop-weight drift or discontinued sizes.

## Adding evidence

- One row per question, not per paper.
- Report the effect estimate and confidence interval when the source does.
- Grade status and certainty separately.
- Prefer the largest or most recent systematic review; cite the primary trial when the
  review is not specific enough.
- If the evidence is observational, say so in `design` and cap certainty at Low.

## Style

- Plain English, no hype, no brand voice.
- Numbers with units. Ranges with an en dash.
- Do not describe a mechanism as if it were an outcome.
- If a claim has no source, delete it rather than softening it.

## Not accepted

- Affiliate or referral links.
- Unpublished manufacturer claims presented as evidence.
- Anecdotes presented as data.
- Changes that remove a safety caveat to make a product look better.
