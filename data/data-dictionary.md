# Data dictionary

The CSV files are the source of truth. `analysis/build_tables.py` validates them and
generates every Markdown table. `evidence.csv`, `claims.csv`, `dosing.csv` and
`standards.csv` use `|` as the delimiter so that prose can contain commas; `products.csv`
and `references.csv` are conventional comma-separated files with quoted text fields.

## products.csv

| Column | Type | Meaning |
| --- | --- | --- |
| `id` | slug | Stable identifier |
| `brand` | text | Brand name |
| `product` | text | Product name as sold |
| `category` | enum | Sports drink (RTD), Electrolyte drink (RTD), Electrolyte powder, Electrolyte tablet, Oral rehydration solution, Electrolyte capsule, Enhanced water |
| `format` | enum | Stick, Tub, Tablet, Capsule, Bottle, Sachet, Can |
| `serving_desc` | text | Serving and dilution as stated on the label |
| `water_ml` | number | Water used for concentration maths; the smallest recommended dilution |
| `na_mg` | number | Sodium per serving, mg |
| `k_mg` | number | Potassium per serving, mg (0 if not declared) |
| `mg_mg` | number | Magnesium per serving, mg |
| `ca_mg` | number | Calcium per serving, mg |
| `cl_mg` | number or blank | Chloride per serving, mg; blank when not declared |
| `carb_g` | number | Total carbohydrate per serving, g |
| `sugar_g` | number | Sugars per serving, g |
| `sweetener_class` | enum | None, Sugar, Stevia, Sucralose, Sucralose + ace-K, Erythritol, Monk fruit + stevia, Stevia + sugar |
| `sweeteners` | text | Sweeteners as named on the label |
| `additives` | text | Notable other ingredients |
| `servings` | number | Servings per package |
| `price_usd` | number | Package price, USD |
| `price_date` | date | Price snapshot date (YYYY-MM-DD) |
| `price_channel` | text | Where the price came from |
| `price_url` | URL | Price source |
| `label_url` | URL | Label source |
| `certification` | text | Third-party certification, or "None found" |
| `na_decl` … `cl_decl` | Y/N | Whether the label declares a quantitative amount |
| `notes` | text | Caveats, label variants, concentration notes |

Computed fields (not stored): sodium mg/L, sodium mmol/L, salt equivalent, cost per
serving, cost per 1,000 mg sodium, carbohydrate % w/v, Na:K mass and molar ratios,
electrolytes declared.

## evidence.csv

| Column | Meaning |
| --- | --- |
| `id` | Domain prefix + number (`PH-01`, `HY-01`, …) |
| `domain` | Physiology, Hydration, Performance, Heat, Cramps, Recovery, Safety: sodium, Safety: potassium, Safety: other, Clinical ORS |
| `question` | The question the row answers |
| `population` | Who was studied |
| `design` | Study design |
| `n` | Participants, or NA |
| `intervention` / `comparator` | What was compared |
| `metric` | Unit or outcome measure |
| `estimate` | Point estimate or qualitative result |
| `ci_low` / `ci_high` | Confidence limits where reported |
| `status` | Benefit, No benefit, Harm, Mixed, Insufficient, Established |
| `certainty` | High, Moderate, Low, Very low, Not graded |
| `reference_id` | Foreign key to references.csv |
| `notes` | Caveats |

## claims.csv

`id`, `claim`, `verdict` (Supported, Partially supported, Unsupported, False, Misleading,
Insufficient), `explanation`, `evidence_ids` (space-separated), `reference_ids`
(space-separated).

## dosing.csv

`scenario`, `population`, `sodium_mg_per_h`, `fluid_ml_per_h`, `carb_g_per_h`, `notes`,
`reference_ids`. Numeric fields may contain a range (e.g. `300-600`) or a qualitative value
(e.g. `Thirst-guided`).

## standards.csv

`id`, `parameter`, `value`, `unit`, `applies_to`, `source_id`, `notes`. Reference intakes,
upper limits, sweat composition ranges and the WHO ORS specification.

## references.csv

`id` (`R01`…), `citation`, `type`, `doi`, `pmid`, `url`. At least one identifier is present
for every row.

## Grading

**Status** describes what the evidence shows; **certainty** describes how much to trust it.
They are independent: a low-certainty harm signal and a high-certainty physiological fact
can both be true. See [the methodology](../docs/01-methodology.md).
