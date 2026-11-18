# Electrolytes and Hydration: An Independent Evidence Review and Product Database

A source-linked review of sodium, potassium, magnesium, calcium and chloride: what they do,
when electrolyte products help, when water and food are enough, where the real risks sit,
and what 22 real products cost per **1,000 mg of sodium**.

Built as a reproducible repository: every table is generated from the CSV datasets in
[`data/`](data/), and every quantitative claim traces to a reference.

**No brand funding, sponsorship or affiliate links.** Prices were collected in November
2026 and will change.

---

## Bottom line

**Electrolytes are real, useful in specific situations, and oversold for everything else.**
Sodium is the only one that matters acutely. Most people doing ordinary exercise do not
need a supplement. The people who do (long events, heat, heavy sweaters, diarrhoea) can
get sodium for a fraction of what the premium brands charge.

| Question | Answer | Confidence |
| --- | --- | --- |
| Does everyone need electrolytes? | **No.** Water and food cover exercise under about an hour. | High |
| When are they useful? | Prolonged exercise, heat, high sweat losses, diarrhoea, post-exercise rehydration. | Moderate–High |
| Which electrolyte matters? | **Sodium.** It drives fluid retention and thirst. | High |
| Does sodium boost performance? | Only by improving fluid intake or retention, not independently. | Moderate |
| Do electrolytes prevent cramps? | **No.** Cramps are a neuromuscular fatigue problem. | Moderate |
| Does magnesium help cramps? | **No** clinically meaningful effect. | Moderate |
| Are sports drinks better than water? | For exercise over an hour, often yes, because of carbohydrate and fluid, not electrolytes. | Moderate |
| Is ORS better than a sports drink? | For diarrhoea, decisively. For exercise it is a cheap high-sodium option. | High |
| What is the real danger? | **Overdrinking** (hyponatraemia) and **potassium excess** in at-risk people. | High |
| What does sodium cost? | **$0.23–$8.81 per 1,000 mg**: a **38×** spread for the same ion. | Price snapshot |

The detailed argument is in the [full report](report/electrolyte-hydration-scientific-report.md).

---

## What is in this repository

| Path | Contents |
| --- | --- |
| [`report/electrolyte-hydration-scientific-report.md`](report/electrolyte-hydration-scientific-report.md) | Comprehensive report: physiology, sweat, performance, cramps, recovery, products, safety, dosing, verdict. |
| [`docs/01-methodology.md`](docs/01-methodology.md) | Search strategy, inclusion rules, grading, price method, limitations, AI disclosure. |
| [`docs/02-electrolyte-physiology.md`](docs/02-electrolyte-physiology.md) | What sodium, potassium, magnesium, calcium and chloride do. |
| [`docs/03-sweat-and-fluid-balance.md`](docs/03-sweat-and-fluid-balance.md) | Sweat composition, sodium loss, sweat testing, acclimation, fluid balance. |
| [`docs/04-exercise-performance-and-heat.md`](docs/04-exercise-performance-and-heat.md) | Dehydration, carbohydrate, sodium, heat acclimation, hyperhydration. |
| [`docs/05-muscle-cramps.md`](docs/05-muscle-cramps.md) | Why the electrolyte theory of cramps fails, and what actually helps. |
| [`docs/06-recovery.md`](docs/06-recovery.md) | Rehydration, glycogen, protein, and what recovery products oversell. |
| [`docs/07-product-categories.md`](docs/07-product-categories.md) | Powders, tablets, RTDs, ORS, sports drinks, capsules, enhanced water. |
| [`docs/08-composition-analysis.md`](docs/08-composition-analysis.md) | Sodium concentration, Na:K ratios, carbohydrate, sweeteners, additives, labels. |
| [`docs/09-safety-and-interactions.md`](docs/09-safety-and-interactions.md) | Sodium and potassium excess, kidney and cardiovascular risk, medication interactions. |
| [`docs/10-dehydration-and-overhydration.md`](docs/10-dehydration-and-overhydration.md) | Dehydration, EAH, hypernatraemia, water intoxication, heat illness. |
| [`docs/11-brands-testing-cost.md`](docs/11-brands-testing-cost.md) | Transparency, certification, brand notes, pricing and value tiers. |
| [`docs/12-dosage-guidance.md`](docs/12-dosage-guidance.md) | Decision tree, sweat-rate protocol, sodium and carbohydrate targets, product equivalents. |
| [`docs/13-verdict.md`](docs/13-verdict.md) | Bottom line, who benefits, product picks, evidence gaps. |
| [`docs/generated/`](docs/generated/) | Generated product comparison, value ranking, composition audit, evidence tables, claims, dosing, standards, key numbers, product sources. |
| [`docs/references.md`](docs/references.md) | 70 references with DOI, PMID or stable URL. |
| [`data/products.csv`](data/products.csv) | 22-product database: sodium, potassium, magnesium, calcium, chloride, carbohydrate, sweeteners, price, certification. |
| [`data/evidence.csv`](data/evidence.csv) | 63 graded evidence rows across 10 domains. |
| [`data/claims.csv`](data/claims.csv) | 26 common claims adjudicated. |
| [`data/dosing.csv`](data/dosing.csv) | Scenario-based sodium, fluid and carbohydrate targets. |
| [`data/standards.csv`](data/standards.csv) | Reference intakes, upper limits, sweat composition, ORS specification. |
| [`data/references.csv`](data/references.csv) | Reference metadata. |
| [`data/data-dictionary.md`](data/data-dictionary.md) | Column definitions and grading scheme. |
| [`analysis/build_tables.py`](analysis/build_tables.py) | Validates the datasets, computes cost and concentration, regenerates all tables. |

---

## Reproduce it

Requires Python 3.10+ and no third-party packages.

```bash
python analysis/build_tables.py           # validate + regenerate tables
python analysis/build_tables.py --check   # fail if outputs are stale or a link is broken
```

The `validate` GitHub Actions workflow runs `--check` on every push.

---

## What the data shows

**Sodium is the dose that matters.** Products range from 0 mg (CORE) to 1,725 mg (TRIORAL)
per serving. A 300 mg tablet replaces about 300 mL of average sweat; a 1,000 mg stick
replaces about a litre.

**Concentration varies more than the category suggests.** At the label's dilution, sodium
ranges from 0 mg/L to 2,368 mg/L. Average sweat is about 966 mg/L. Sports drinks sit below
sweat; premium sticks sit above it.

**Potassium is usually the wrong direction.** Sweat is sodium-dominant (about 7:1 molar).
Several popular drinks are potassium-dominant, replacing the electrolyte lost least.

**Chloride is the transparency gap.** Only 8 of 22 products declare it, despite it being
the second most abundant ion in sweat.

**Cost is unrelated to sodium.** The cheapest product per milligram is a WHO ORS sachet at
$0.23 per 1,000 mg; the most expensive is a bottle of Gatorade at $8.81. The electrolyte
itself costs a fraction of a cent.

---

## Scope and caveats

- This is a review of published evidence and label data, **not medical advice**. Kidney
  disease, heart failure, hypertension, pregnancy and medication use change the answer.
- Labels were **not independently assayed**. Where a product lacks certification or a
  published certificate of analysis, the label is the best available evidence.
- Prices are **November 2026 snapshots** from named channels and exclude shipping.
- The 22-product sample is **purposive**, chosen to span the market's claims, not a census.
- Evidence certainty is graded per row; where it is low, the text says so.

---

## Licence

Text and data are released under the MIT Licence. See [LICENSE](LICENSE) and
[NOTICE](NOTICE). Cite via [CITATION.cff](CITATION.cff).

Corrections are welcome, open an issue with a source.
