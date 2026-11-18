# Changelog

All notable changes to this review are recorded here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and the project uses
[Semantic Versioning](https://semver.org/).

## [1.0.0] - 2026-11-18

### Added

- Full evidence review: physiology of sodium, potassium, magnesium, calcium and chloride;
  sweat composition and fluid balance; exercise performance and heat; muscle cramps;
  recovery; safety and medication interactions; dehydration and overhydration.
- Reproducible product database of 22 products across seven categories, normalised to
  sodium per serving, sodium concentration, carbohydrate percentage and cost per 1,000 mg
  sodium.
- Generated tables: product comparison, value ranking, composition audit, evidence tables,
  claims table, dosing table, standards, key numbers and product sources.
- 70 references with DOI, PMID or stable URL.
- Validator and table generator (`analysis/build_tables.py`) with `--check` mode and a
  relative-link checker.
- GitHub Actions workflow that fails on stale tables or broken links.

### Notes

- Prices are November 2026 snapshots.
- Labels were not independently assayed.
