# Edge Cases — Interpretation Guide

> **Purpose:** Documents known physiological edge cases that require adjusted interpretation logic within this coaching engine. Each case defines when a standard biomarker reading can be misleading, the corrective interpretation framework, and the decision tree for coaching response vs. clinical escalation.

---

## Edge Case 1: High Lean-Mass Creatinine False Flag

### The Problem
Standard creatinine reference ranges (0.6–1.2 mg/dL) are calibrated for sedentary-normal body composition. Athletes with >80 kg lean mass produce significantly more creatinine as a byproduct of muscle catabolism, routinely generating values of 1.2–1.5 mg/dL that fall outside standard ranges but are physiologically benign.

### Misinterpretation Risk
Flagging creatinine >1.2 mg/dL as renal dysfunction in a high-LM athlete leads to unnecessary clinical escalation and protocol disruption.

### Correct Interpretation Framework
1. **Always pair creatinine with eGFR and BUN.** Creatinine alone is insufficient.
2. **eGFR adjusts for body surface area** — values >60 mL/min/1.73m² are acceptable in athletes even with elevated creatinine.
3. **BUN:Creatinine ratio** should remain <20:1. If BUN is disproportionately elevated (>25 mg/dL), suspect dehydration or catabolic stress — not renal failure.
4. **Cystatin-C** is the superior renal biomarker for athletes (independent of muscle mass) — recommend requesting if available.

### Decision Tree
- Creatinine 1.2–1.5 mg/dL + eGFR >70 + BUN <25: ✅ NORMAL for high-LM athlete, no escalation
- Creatinine >1.5 mg/dL + eGFR <60: ⚠️ Monitor, repeat panel in 4 weeks with hydration optimization
- Creatinine >1.8 mg/dL or eGFR <45: 🚨 ESCALATE — nephrology referral per emergency_flags.md

---

## Edge Case 2: Elevated Hematocrit on TRT — Distinguishing Physiological from Pathological

### The Problem
Exogenous testosterone (TRT or supraphysiological doses) stimulates erythropoiesis, elevating hematocrit. Values of 50–54% are common in male athletes on TRT protocols and do not represent the same pathological risk as primary polycythemia vera.

### Misinterpretation Risk
Halting all protocols at hematocrit >50% for an athlete on TRT is overly conservative. However, failing to act on hematocrit >54% creates real thrombotic risk.

### Correct Interpretation Framework
1. **Assess RBC, hemoglobin, and MCV together.** TRT-driven erythrocytosis produces microcytic/normocytic RBCs. Macrocytic elevation suggests B12/folate deficiency compounding.
2. **Distinguish from polycythemia vera:** PV shows elevated WBC, platelets, and JAK2 V617F mutation — not typically present in TRT context.
3. **Hydration confounds hematocrit** — a single dehydrated blood draw can falsely elevate by 2–4%. Always confirm on a well-hydrated, fasted morning draw.
4. **Therapeutic phlebotomy** is a legitimate management tool for TRT-driven erythrocytosis above 52% in consultation with prescribing physician.

### Decision Tree
- Hematocrit 48–52% (TRT context) + confirmed hydration: ⚠️ Monitor monthly, optimize hydration, ensure EPA/DHA ≥3g/d
- Hematocrit 52–54% (TRT context): ⚠️ Flag prescribing physician, consider phlebotomy discussion, coaching protocol continues at reduced intensity
- Hematocrit >54% (any context): 🚨 HALT per emergency_flags.md — clinical escalation mandatory

---

## Edge Case 3: Hypothyroid Pattern Mimicking Overtraining Fatigue

### The Problem
Classic overtraining syndrome (OTS) and subclinical hypothyroidism share overlapping symptoms: chronic fatigue, reduced HRV, impaired recovery, low motivation, weight gain resistance, cold intolerance, and elevated resting heart rate. These are routinely attributed to training load without checking thyroid function.

### Misinterpretation Risk
Reducing training volume when the root cause is thyroid suppression does not resolve the symptom set and leads to prolonged underperformance.

### Correct Interpretation Framework
1. **Always check Free T3, Free T4, and TSH together** — TSH alone misses the most actionable pattern.
2. **Low Free T3 + normal TSH + normal Free T4:** Classic peripheral conversion suppression (deiodinase inhibition). Most common in caloric restriction, high cortisol states, and endurance overreaching. TSH appears normal because pituitary sees adequate T4.
3. **Elevated TSH + low Free T4:** True primary hypothyroidism — clinical referral required.
4. **All thyroid markers normal + OTS symptoms:** Training load is the primary variable. Execute deload protocol.
5. **Reverse T3** (if testable): Elevated rT3 in the context of low Free T3 confirms peripheral conversion suppression, not primary thyroid pathology.

### Decision Tree
- Free T3 <3.0 pg/mL + TSH <2.5 + normal FT4: ⚠️ Suspect caloric/cortisol suppression. Increase calories ≥200 kcal/d, reduce cardio volume, recheck in 6 weeks
- Free T3 <2.5 pg/mL any context: ⚠️ Flag to physician, consider rT3 panel
- TSH >4.0 + low FT4: 🚨 Primary hypothyroid — endocrinology referral, halt recommendations pending clinical management

---

## Edge Case 4: Skeletal Muscle Damage Elevating AST — Distinguishing from Hepatic ALT Elevation

### The Problem
AST (aspartate aminotransferase) is present in both liver and skeletal muscle. Heavy resistance training routinely elevates AST by 2–4x above standard reference range for 48–72 hours post-session. Interpreting elevated AST as hepatic injury in a training athlete is a systematic error.

### Misinterpretation Risk
Halting supplementation stacks or flagging hepatotoxicity based on post-training AST without assessing ALT and GGT leads to false clinical escalation.

### Correct Interpretation Framework
1. **The critical differentiator is ALT.** ALT is liver-specific. If AST is elevated but ALT is normal (or only mildly elevated), the AST source is skeletal muscle.
2. **AST:ALT ratio** >2:1 suggests alcoholic hepatitis in clinical settings, but in athletes, this ratio commonly reflects muscle-predominant AST release. Context is everything.
3. **GGT elevation** is the most specific marker of hepatocellular stress and is not elevated by exercise. Elevated GGT + elevated ALT = hepatic concern.
4. **Timing matters:** Blood draws should be >48 hours post-last-training-session for accurate hepatic assessment.
5. **CPK (creatine phosphokinase):** If available, elevated CPK (>1000 U/L) in the context of elevated AST with normal ALT/GGT confirms muscle source.

### Decision Tree
- AST elevated + ALT normal + GGT normal + heavy training within 48h: ✅ Exercise-induced, no intervention required
- AST elevated + ALT 40–80 U/L + GGT normal: ⚠️ Monitor — confirm draw timing, recheck in 2 weeks off-cycle
- AST elevated + ALT >80 U/L + GGT elevated: ⚠️ Hepatic signal — reduce or cycle off hepatotoxic compounds, recheck in 4 weeks
- AST or ALT >120 U/L: 🚨 HALT per emergency_flags.md — hepatotoxicity referral required

---

## Edge Case 5: HPTA Suppression Interpretation with Exogenous Androgens

### The Problem
Athletes using exogenous androgens (testosterone, SARMs, prohormones, anabolic steroids) will show suppressed LH and FSH as an expected pharmacological outcome of negative feedback on the hypothalamic-pituitary axis. Flagging LH + FSH both <1.0 mIU/mL as a pathological emergency in a client on exogenous androgens is clinically inappropriate — it is the expected result.

### Misinterpretation Risk
1. Triggering emergency escalation for pharmacologically expected suppression wastes clinical resources.
2. Alternatively, missing genuine HPTA dysfunction in a client claiming to be off-cycle creates a different risk.

### Correct Interpretation Framework
1. **Context is mandatory.** The compound_stack_notes field in client_profile_schema.json must document exogenous androgen use before any LH/FSH interpretation.
2. **On exogenous androgens:** LH + FSH suppression is expected and not an emergency. Monitor total testosterone (should be elevated by exogenous source), assess HPTA recovery timeline during post-cycle transition.
3. **Off-cycle / PCT context:** LH + FSH should recover within 8–16 weeks of cessation (individual variation). Persistent suppression at >16 weeks post-cessation warrants endocrinology referral.
4. **HPTA recovery markers:** LH + FSH trending upward + total testosterone recovering toward endogenous range (400–700 ng/dL) indicates successful HPTA reactivation.

### Decision Tree
- LH + FSH <1.0 mIU/mL (on-cycle, documented): ✅ Expected pharmacological suppression — no emergency escalation
- LH + FSH <1.0 mIU/mL (off-cycle >16 weeks): 🚨 HALT — endocrinology referral per emergency_flags.md
- LH + FSH suppressed + low total testosterone (not on exogenous): 🚨 Hypogonadism — immediate endocrinology referral

---

## Edge Case 6: Low Free T3 with Normal TSH — Euthyroid Sick / Caloric Suppression

### The Problem
This is the most commonly overlooked thyroid pattern in performance athletes. Standard thyroid panels report TSH and often only T4. Free T3 — the biologically active thyroid hormone — is the primary regulator of metabolic rate, protein synthesis, cardiac output, and recovery. TSH can be entirely normal while Free T3 is critically suppressed, producing a hypothyroid-like metabolic state.

### Mechanisms
1. **Caloric deficit / low-carbohydrate intake:** Carbohydrate restriction impairs deiodinase (D1/D2) enzyme activity — the enzyme converting T4 → T3 peripherally. This is the most common mechanism in physique athletes.
2. **Elevated cortisol:** Cortisol directly inhibits D1 deiodinase, reducing T4→T3 conversion. High-stress states suppress Free T3 even with adequate caloric intake.
3. **Overtraining:** Excessive volume without recovery drives cortisol chronically elevated, secondary to adrenal activation — producing the same deiodinase suppression.
4. **Low selenium:** Selenium is a required cofactor for deiodinase enzymes. Selenium deficiency impairs T3 synthesis.

### Non-Thyroidal Illness Syndrome (Euthyroid Sick)
In clinical medicine, this pattern is called "Euthyroid Sick Syndrome" — normal TSH, low Free T3, sometimes low Free T4 — observed in systemic illness, surgery, starvation. Athletes can exhibit a subclinical variant without overt illness due to the above mechanisms.

### Correct Interpretation Framework
1. **Free T3 <3.2 pg/mL = suboptimal**, regardless of TSH value.
2. **First-line intervention is nutritional:** Increase caloric intake (emphasize carbohydrate restoration), normalize the deficit, reduce cardio volume.
3. **Second-line:** Address cortisol (deload protocol, sleep optimization, stress management).
4. **Supplement support:** Selenium 200 mcg/d, zinc (if deficient), iodine (if deficient — check via dietary analysis).
5. **Do NOT recommend exogenous T3 (cytomel/liothyronine)** without endocrinology direction — this suppresses endogenous TSH and creates thyroid dependency.

### Decision Tree
- Free T3 3.0–3.2 pg/mL + caloric deficit confirmed: ⚠️ Nutritional intervention first, recheck in 6 weeks
- Free T3 <3.0 pg/mL + TSH normal + FT4 normal: ⚠️ Caloric/cortisol suppression — aggressive nutritional rebound + deload, physician notification
- Free T3 <2.5 pg/mL any context: 🚨 Clinical referral, endocrinology assessment, pause all aggressive cutting protocols
- Free T3 low + TSH elevated + FT4 low: 🚨 Primary hypothyroidism — endocrinology mandatory

---

## Quick-Reference Edge Case Matrix

| Pattern | Most Likely Cause | Coaching Action | Clinical Action |
|---------|------------------|-----------------|-----------------|
| Creatinine 1.2–1.5 + eGFR >70 | High lean mass | None | None |
| Hematocrit 50–54% on TRT | Erythropoiesis | Hydration, omega-3 | Physician notification |
| AST elevated + ALT normal post-training | Muscle damage | Delay redraw 48h | None |
| LH/FSH <1 (on-cycle) | HPTA suppression | Document, monitor | None |
| LH/FSH <1 (off-cycle >16 wk) | HPTA failure | HALT protocols | Endocrinology |
| Free T3 <3.2 + normal TSH | Caloric/cortisol suppression | Increase calories, deload | Physician notification |
| Free T3 <2.5 any context | Severe suppression or hypothyroid | HALT aggressive protocols | Endocrinology referral |
| Hematocrit >54% | Thrombotic risk | HALT per emergency_flags | Clinical escalation mandatory |
| ALT >120 U/L | Hepatotoxicity | HALT | Hepatology referral |
| eGFR <45 | Renal compromise | HALT | Nephrology referral |
