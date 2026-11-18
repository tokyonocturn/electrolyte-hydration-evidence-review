# Methodology

## What this review is

An independent, source-linked synthesis of the evidence on electrolyte supplements and
hydration products, combined with a product database that normalises 22 products to
**sodium per serving, sodium concentration, carbohydrate concentration and cost per
1,000 mg of sodium**.

It answers five questions:

1. What do sodium, potassium, magnesium, calcium and chloride actually do?
2. When does electrolyte supplementation improve health or performance, and when is
   water and food sufficient?
3. What is in these products, and do the labels support the marketing?
4. Where is the harm: sodium excess, potassium excess, overhydration, interactions?
5. Which products are honest, well formulated and good value per useful dose?

## Scope and inclusion rules

**Evidence.** Peer-reviewed randomised trials, systematic reviews, meta-analyses,
prospective cohorts, consensus statements, national guidelines and regulatory documents.
Priority went to Cochrane reviews, the largest outcome trials, and syntheses that report
confidence intervals and certainty. Observational evidence is included but labelled,
because it cannot establish causation.

**Products.** Twenty-two products selected purposively across seven categories:

| Category | Products | Why it is included |
| --- | --- | --- |
| Electrolyte powder | 7 | The dominant direct-to-consumer format |
| Electrolyte tablet | 2 | Cheapest per serving, weakest dose |
| Sports drink (RTD) | 4 | The mass-market baseline |
| Electrolyte drink (RTD) | 1 | Premium bottled electrolyte drink |
| Oral rehydration solution | 4 | The clinical benchmark |
| Electrolyte capsule | 2 | Dose without fluid |
| Enhanced water | 2 | "Electrolyte" claims with little or no sodium |

The sample is not a census. It was chosen to test the claims the market makes: that
high sodium is better, that potassium matters, that sugar-free is superior, that
"electrolytes" means something on a bottle of flavoured water, and that a premium stick
is worth 6× a sachet of ORS.

A product was eligible if its label declared sodium per serving and a price could be
attached to a specific pack size. Products that market "electrolytes" without declaring
any amounts are included in the database but flagged as unscorable; they are a
transparency finding, not a silent omission.

**Excluded:** animal and in-vitro studies (used only for mechanism), unpublished
manufacturer claims, marketplace listings without a verifiable label, products whose
price could not be tied to a pack size, and electrolyte products marketed solely for
children or pets.

## Search strategy

PubMed, the Cochrane Library, journal sites and regulator sites (FDA, EFSA, WHO,
Health Canada, KDIGO) were searched using combinations of:

`electrolyte`, `sodium`, `potassium`, `magnesium`, `calcium`, `chloride`,
`sports drink`, `oral rehydration solution`, `ORS`, `hydration`, `sweat`,
`sweat sodium`, `heat acclimation`, `exercise-associated hyponatremia`,
`exercise-associated muscle cramps`, `dehydration`, `hypernatremia`,
`hyponatremia`, `salt substitute`, `sodium intake`, `blood pressure`,
`salt tablet`, `carbohydrate-electrolyte`, `osmolality`, `gastric emptying`,
`artificial sweetener`, `erythritol`, `aspartame`.

Each candidate was screened at title and abstract level; the abstract or full text was
read for every number used. Where a review and its included trials disagreed, both are
reported. Where a widely repeated claim had no primary source, it is marked unsupported
rather than repeated.

## Grading scheme

Two independent axes, deliberately separated:

**Status**: what the estimate shows:

| Status | Meaning |
| --- | --- |
| Established | Physiology or fact not seriously disputed |
| Benefit | Intervention improves a relevant outcome |
| No benefit | No difference, or a difference too small to matter |
| Harm | Intervention worsens a relevant outcome |
| Mixed | Direction depends on population, dose or context |
| Insufficient | Data do not answer the question |

**Certainty**: how much to trust it:

| Certainty | Meaning |
| --- | --- |
| High | Consistent RCTs or meta-analyses, or unambiguous physiology |
| Moderate | Some inconsistency, indirectness or risk of bias |
| Low | Small studies, surrogate outcomes, or observational data only |
| Very low | Expert opinion, mechanism, or case reports |

These are not GRADE in the strict sense. They are a transparent summary of the same
considerations, applied consistently across the evidence table.

## Product and price method

- **Serving** is the label's stated serving at the label's stated dilution, not a
  bottle, not a scoop the manufacturer happens to sell in a tub.
- **Sodium concentration** (mg/L and mmol/L) is computed at the smallest volume the brand
  recommends. Drinking the same stick in more water lowers concentration, not dose.
- **Cost per serving** = pack price ÷ servings per pack.
- **Cost per 1,000 mg sodium** = cost per serving ÷ sodium per serving × 1,000. This is
  the only price metric that compares a 1,725 mg ORS sachet, a 1,000 mg stick and a
  270 mg bottle on equal terms.
- **Prices** are one-time list prices collected in November 2026 from the brand store or a
  named retailer, excluding shipping and subscription discounts. They will change.
- **Salt equivalent** = sodium × 2.542, because 1 g of sodium chloride contains 393 mg
  sodium.

No brand paid for inclusion, supplied product, or reviewed a draft. There are no
affiliate links.

## Transparency scoring

For each product we recorded whether the label declares an amount for each of the five
electrolytes. "Not declared" is not zero: a product can contain potassium from a flavour
system and never disclose it. The audit therefore counts declarations, not ingredients.

## Limitations

1. **Label values are not assays.** We did not independently test any product. A label
   can be wrong; without a certificate of analysis, the label is the best available
   evidence and should be treated as such.
2. **Prices are a snapshot.** Retail prices move weekly; cost rankings are stable in
   order of magnitude but not to the cent.
3. **Sweat testing is imprecise.** The physiological ranges are population data, and an
   individual's sweat sodium can vary two-fold between sessions.
4. **Outcome evidence is uneven.** Hydration and performance have decent trial evidence.
   Cramps, "recovery" and hangover claims do not.
5. **The product sample is purposive.** It spans the market's claims, not its sales.
6. **No individual medical advice.** Kidney disease, heart failure, hypertension and
   medication use change everything in this document. Those decisions belong to a
   clinician who knows the person.

## Reproducibility and AI disclosure

Every number in the prose that comes from the datasets is generated by
[`analysis/build_tables.py`](../analysis/build_tables.py), and the CI workflow fails if a
committed table is stale. The literature synthesis, product selection and interpretation
were drafted with AI assistance and checked against the cited sources; errors are the
responsibility of the maintainer, not the sources. Corrections are welcome via the issue
template.
