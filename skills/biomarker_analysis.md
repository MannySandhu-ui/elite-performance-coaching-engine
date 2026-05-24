---
Skill: Vector 1 — Biomarker & Laboratory Analysis
---

## Purpose

Systematically evaluate all submitted biomarker data against `performance_optimal_ranges.json`. Identify deviations, compounding relationships, and early-warning trends.

---

## Analytical Logic

### Step 1: Emergency Threshold Check

Before ANY analysis: cross-reference all submitted markers against `emergency_flags.md`. If ANY emergency threshold is breached: **STOP**. Issue Clinical Escalation Notice. Do not proceed.

### Step 2: Panel Completeness Audit

For each required marker in the check-in template:
- If value provided: proceed to comparison
- If value is `[NOT AVAILABLE]`: flag as `[DATA ABSENT: marker_name]` and note analytical limitation

### Step 3: Individual Marker Comparison

Compare each submitted value against `performance_optimal_ranges.json` tiers:

| Result | Status |
|--------|--------|
| Below `clinical_floor` | 🚨 CRITICAL LOW |
| Below acceptable lower bound | ⚠️ SUB-OPTIMAL LOW |
| Within `optimal_performance` range | ✅ OPTIMAL |
| Above acceptable upper bound | ⚠️ ELEVATED — MONITOR |
| Above `elevated_flag` | 🚨 ELEVATED — INTERVENTION REQUIRED |

### Step 4: Compounding Relationship Analysis

Apply `hormone_axis_matrix.md` patterns to all hormone markers. Key compound checks to always run:

1. **LH + FSH + Total T** → HPTA axis pattern
2. **Free T + SHBG + Total T** → Bioavailability pattern
3. **E2 + SHBG + Total T** → Aromatization pattern
4. **Cortisol + Total T** → HPA-HPG competition pattern
5. **Free T3 + TSH + caloric intake** → Thyroid conversion pattern
6. **ALT + AST ratio** → Hepatic vs. skeletal muscle differentiation
7. **Creatinine + eGFR + BUN** → Renal function triad
8. **Fasting Insulin + TG:HDL ratio** → Insulin resistance composite

> **Cross-reference `edge_cases.md`** for any pattern that matches a known ambiguity (e.g., creatinine in high lean mass, AST post-training, HPTA suppression on-cycle, low Free T3 with normal TSH).

### Step 5: Trend Analysis (When Prior Check-In Data Available)

If previous check-in data exists in `check_in_log_template.csv`:
- Calculate **delta** for each marker since last check-in
- Flag markers **trending toward** flag thresholds even if currently within range
- Note velocity of change (e.g., *"ALT trending +15 U/L over 30 days — approaching flag threshold"*)

### Step 6: Output Formatting

Organize output in this sequence:
1. Emergency notices (if any)
2. Data absent flags
3. Critical deviations (emergency or critical low/high)
4. Compounding pattern findings
5. Sub-optimal findings requiring monitoring
6. Optimal markers (brief acknowledgment)
7. Trend alerts

---

## Output Template

```
## 📊 Vector 1: Biomarker & Laboratory Analysis

### [EMERGENCY — if applicable]
> ⛔ HALT: [Marker] = [Value] [Unit] — exceeds emergency threshold. Clinical escalation required. No further protocol recommendations issued.

### CRITICAL FINDINGS:
- **[Marker]:** [Value] [Unit] | Optimal: [Range] | Status: CRITICAL | Action: [specific]

### COMPOUNDING PATTERNS:
- **[Pattern Name]:** [findings and clinical interpretation]

### SUB-OPTIMAL / MONITORING:
- **[Marker]:** [Value] [Unit] | Optimal: [Range] | Status: ELEVATED-MONITOR | Trend: [if available]

### OPTIMAL:
[List markers within optimal range — brief]

### DATA ABSENT:
[List missing markers that limit analysis]
```

---

## No-Hallucination Contract

- All range references MUST cite `performance_optimal_ranges.json` tier values exactly as stored
- NEVER use standard clinical reference ranges as the evaluation baseline
- Every finding must reference a specific submitted client data field
- If a marker is not submitted, it MUST be listed under DATA ABSENT — never inferred or assumed
