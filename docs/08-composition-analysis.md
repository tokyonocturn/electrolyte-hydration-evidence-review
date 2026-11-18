# Composition analysis: sodium, ratios, carbohydrate and additives

This chapter is the label-level analysis behind the product tables. Every figure is
generated from [`data/products.csv`](../data/products.csv); the full tables are in
[product comparison](generated/product-comparison.md) and
[composition audit](generated/composition-audit.md).

## Sodium concentration versus sweat

The single most useful comparison is sodium concentration (mg/L) against sweat
(roughly 230–2,070 mg/L, mean ~966 mg/L at 42 mmol/L).

| Product | Sodium mg/L | Equivalent mmol/L | Versus average sweat |
| --- | --- | --- | --- |
| Waterboy Weekend Recovery | 2,368 | 103 | 2.5× |
| LMNT (at 500 mL) | 2,000 | 87 | 2.1× |
| TRIORAL ORS | 1,725 | 75 | 1.8× |
| NormaLyte | 1,702 | 74 | 1.8× |
| Redmond Re-Lyte | 1,712 | 74 | 1.8× |
| BIOLYTE | 1,480 | 64 | 1.5× |
| DripDrop | 1,398 | 61 | 1.4× |
| Liquid I.V. | 1,121 | 49 | 1.2× |
| Precision PH 1000 | 1,000 | 43 | 1.04× |
| Skratch | 800 | 35 | 0.83× |
| Powerade | 677 | 29 | 0.70× |
| Nuun Sport | 600 | 26 | 0.62× |
| Gatorade | 457 | 20 | 0.47× |
| BODYARMOR | 63 | 3 | 0.07× |
| PRIME | 20 | 0.9 | 0.02× |
| CORE | 0 | 0 | 0 |

Two observations follow.

**Most "electrolyte" products are stronger than sweat.** That is not inherently wrong: a
concentrated stick is meant to be diluted, and a high-sodium drink can be sipped slowly.
But it means the label "electrolyte" tells you nothing about whether the product matches
sweat.

**Mainstream sports drinks are weaker than sweat.** They are designed for palatability
and for people who are also eating. Their sodium is enough to improve retention modestly,
not enough to replace a heavy sweat loss.

## Sodium-to-potassium ratio

Sweat is sodium-dominant: about 42 mmol/L sodium against 6 mmol/L potassium, a molar ratio
near 7:1. Products vary enormously:

- **Skratch** 13.6:1 and **LMNT** 8.5:1 are close to sweat.
- **Gatorade** 5.7:1 is moderately sodium-forward.
- **ORS** 3.8:1 reflects the clinical formula, which includes potassium for diarrhoea
  losses.
- **Liquid I.V.** 2.4:1 and **Pedialyte** 2.3:1 are potassium-heavy relative to sweat.
- **PRIME** and **BODYARMOR** are potassium-dominant, with almost no sodium.

For hydration, a high potassium-to-sodium ratio is the wrong direction: it replaces the
electrolyte you lost least. For general nutrition, potassium is beneficial, but a sports
drink is an expensive way to buy it. A banana has about 400 mg potassium for $0.30; a
PRIME bottle has 700 mg for $2.39.

## Carbohydrate content

Carbohydrate concentration determines whether a drink fuels, hydrates, or both.

| Product | Carb g/100 mL | Category |
| --- | --- | --- |
| Gatorade | 6.1% | Fuel + fluid |
| Powerade | 5.8% | Fuel + fluid |
| Skratch | 3.8% | Light fuel |
| Precision PH 1000 | 3.4% | Light fuel |
| Pedialyte powder | 3.2% | ORS |
| Liquid I.V. | 2.5% | Hydration |
| BIOLYTE | 2.5% | Hydration |
| LMNT | 0.2% | Hydration |
| Nuun Sport | 0.8% | Hydration |
| Re-Lyte | 0% | Hydration |
| SaltStick | 0% | Hydration |

The 6–8% band is the sweet spot for simultaneous fueling and emptying. Above ~8%, gastric
emptying slows ([PF-07](generated/evidence-tables.md)). Below ~3%, the drink is a
hydration product with a little sugar for taste.

For events over 2.5 hours, 90 g/h of carbohydrate cannot come from a 6% drink alone
without drinking 1.5 L/h. That is why long-course athletes combine drinks with gels,
chews and bars.

## Sugar-free products

Sugar-free electrolyte products are not automatically better. The decision depends on the
job:

| Goal | Sugar-free? | Why |
| --- | --- | --- |
| Daily hydration, office, heat | Yes | Fewer calories, no dental load |
| Gym session under 60 min | Yes | No fueling need |
| Endurance over 60–90 min | No | Carbohydrate is the performance ingredient |
| Ultra-endurance | No (or separate fuel) | 60–90 g/h needed |
| Diarrhoea | No | Glucose drives sodium absorption |
| Weight loss | Possibly | But water is cheaper |

The marketing claim that sugar "blocks hydration" is false at sports-drink
concentrations. Hypertonic solutions do slow emptying, but a 6% drink is not hypertonic.

## Non-nutritive sweeteners

Sweetener choice is the most emotionally charged label decision in the category. The
evidence does not support panic, and it does not support indifference.

**Stevia (steviol glycosides).** Plant-derived, generally well tolerated. No established
safety signal at food-additive doses. Some people detect a bitter aftertaste.

**Sucralose and acesulfame potassium.** The most common blend in mainstream sugar-free
drinks. Both are approved and have acceptable daily intakes far above typical exposure.
Sucralose may alter the gut microbiome in some studies; the clinical significance is
unclear. Acesulfame K has been associated with changes in glucose metabolism in
observational work, not established causation.

**Erythritol.** A sugar alcohol used in some "natural" products. A 2023 study associated
plasma erythritol with cardiovascular events and showed platelet effects in vitro
([SC-05](generated/evidence-tables.md)). EFSA reviewed the evidence and found no causal
relationship, noting that erythritol is also produced endogenously
([SC-05](generated/evidence-tables.md)). It is a hypothesis, not a proven harm. At high
doses it causes osmotic diarrhoea ([SC-08](generated/evidence-tables.md)).

**Aspartame.** IARC classified it as Group 2B ("possibly carcinogenic") in 2023 on limited
evidence; JECFA reaffirmed the acceptable daily intake of 40 mg/kg
([SC-06](generated/evidence-tables.md)). A 70 kg adult would need about 14 cans of diet
soda to reach the ADI. The classification is a hazard statement, not a risk estimate at
usual intake.

**WHO guidance.** WHO advises against using non-sugar sweeteners for weight control
([SC-07](generated/evidence-tables.md)). That is about long-term weight outcomes, not
about whether a sugar-free electrolyte drink is safer than a sugar-sweetened one.

Practical position: sugar-free products are fine for hydration. If you are uneasy about a
specific sweetener, choose a product that uses a different one or none. The electrolyte
content matters more than the sweetener.

## Other additives

| Additive | Why it is there | Concern |
| --- | --- | --- |
| Citric acid | Tartness, preservation | None at food doses; can erode enamel with heavy sipping |
| Sodium citrate / bicarbonate | Sodium source, buffering | Sodium without chloride; bicarbonate can cause GI gas |
| Maltodextrin | Carbohydrate, mouthfeel | High glycaemic index; not a problem in context |
| Colours (Yellow 5, Red 40, beta-carotene) | Appearance | Rare sensitivity; no general safety issue at food doses |
| Preservatives (EDTA, potassium sorbate) | Shelf life | None at approved doses |
| Caffeine | Stimulant | 3–6 mg/kg improves performance; can worsen anxiety and sleep |
| B vitamins | "Energy" marketing | Harmless; turns urine bright yellow |
| BCAAs | Marketing | No hydration or performance benefit at these doses |
| "Proprietary blends" | Concealment | Cannot be evaluated; avoid |

## Label transparency

Across the 22 products:

- **Sodium** is declared by 21 of 22 (95%).
- **Potassium** is declared by 21 of 22 (95%).
- **Magnesium** is declared by 13 of 22 (59%).
- **Calcium** is declared by 6 of 22 (27%).
- **Chloride** is declared by 8 of 22 (36%).

Chloride is the notable gap: it is the second most abundant ion in sweat, and most labels
omit it. Some of those products contain chloride (sodium chloride is the sodium source)
but do not quantify it; others use citrate or bicarbonate and contain little or none.

A product that lists "electrolytes" without amounts (CORE is the clearest example) is
not providing information a consumer can act on.

## Serving sizes and doses

The dose that matters is sodium per serving, and servings are not standard:

- A stick is one serving.
- A tablet is one serving, usually dissolved in 500 mL.
- A bottle may be 1–2.8 servings.
- A capsule serving may be one or two capsules.
- A tub serving is a scoop whose mass varies by flavour.

Normalising to sodium per 1,000 mg and cost per 1,000 mg removes the distortion. It also
reveals how small most "electrolyte" doses are: a 300 mg tablet replaces about 300 mL of
average sweat, which is 10–15 minutes of moderate exercise in heat.

## What a good formulation looks like

- 500–1,000 mg sodium per serving for exercise use.
- 100–200 mg potassium, not 700 mg.
- Little or no magnesium and calcium, unless the product is a multinutrient.
- 4–9% carbohydrate if it is meant to fuel; under 3% if it is not.
- Chloride declared if sodium chloride is the sodium source.
- No proprietary blends.
- A clear statement of the water volume the serving is designed for.
