# Skill: Vector 3 — Supplementation Stack Adjustments

## Purpose
Evaluate the current supplement stack against biomarker data. Identify gaps, redundancies, and antagonistic interactions. Provide precise, mechanistically-grounded recommendations.

---

## Analytical Logic

### Step 1: Stack Audit Against Biomarker Deficits
For each lab marker deviating from performance_optimal_ranges.json:
Check supplement_interaction_map.json for relevant supplemental interventions.
Cross-reference if the client is already supplementing for that deficit.
If already supplementing: assess whether dose is therapeutic vs. sub-therapeutic.

### Step 2: Hepatic Load Assessment
If client stack includes any of: oral androgens, prohormones, high-dose niacin, high-dose acetaminophen:
- Check AST, ALT, GGT against organ_health ranges
- If any are elevated: mandate NAC and/or TUDCA (see supplement_interaction_map.json)
- Flag dose and timing

### Step 3: Androgen-Support Stack Review
If Total T or Free T are sub-optimal:
- Check Zinc status: if Zinc <70 ug/dL -> recommend 25-50mg Zinc bisglycinate
- Check Vitamin D3: if <40 ng/mL -> recommend 2000-5000 IU D3 + K2
- Check DHEA-S: if <200 ug/dL -> flag for DHEA consideration (physician oversight)
- Check Prolactin: if elevated -> flag dopamine precursor discussion

### Step 4: Cardiovascular/Lipid Stack Review
If ApoB >100 or TG >100 or TG:HDL >2.0:
- Citrus Bergamot: 500-1000 mg/day if not already on lipid-lowering therapy
- Omega-3 FA: 2-4g EPA+DHA/day
- CoQ10: 200-400mg/day ubiquinol
- Berberine: 500mg 2-3x/day for insulin resistance component

### Step 5: Recovery / Micronutrient Stack
- Sleep <7 hrs or HRV declining: Magnesium glycinate 200-400mg at bedtime
- Ferritin <30: Iron bisglycinate 25-50mg with Vitamin C, away from coffee/tea
- Hs-CRP >1.0: Curcumin 500-1000mg with piperine, Omega-3s

### Step 6: Interaction Screening
Run all recommendations against supplement_interaction_map.json antagonistic_interactions section.
Flag any high-risk combinations (e.g., high Zinc depleting Copper, Berberine with cyclosporine).

---

## Output Template

**Vector 3: Supplementation Stack Adjustments**

ORGAN PROTECTION (if indicated):
- [Compound]: [Dose] [Timing] | Rationale: [biomarker driver]

HORMONE AXIS SUPPORT:
- [Compound]: [Dose] [Timing] | Rationale: [biomarker driver]

CARDIOVASCULAR/METABOLIC:
- [Compound]: [Dose] [Timing] | Rationale: [biomarker driver]

MICRONUTRIENT REPLETION:
- [Compound]: [Dose] [Timing] | Rationale: [biomarker driver]

INTERACTION FLAGS:
- [Flag description if any antagonistic combinations detected]

STACK REDUNDANCIES (if any):
- [Note any compounds in current stack that are redundant or unnecessary]
