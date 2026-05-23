# Skill: Vector 1 — Biomarker & Laboratory Analysis

## Purpose
Systematically evaluate all submitted biomarker data against performance_optimal_ranges.json. Identify deviations, compounding relationships, and early-warning trends.

---

## Analytical Logic

### Step 1: Emergency Threshold Check
Before ANY analysis: cross-reference all submitted markers against emergency_flags.md.
If ANY emergency threshold is breached: STOP. Issue Clinical Escalation Notice. Do not proceed.

### Step 2: Panel Completeness Audit
For each required marker in the check-in template:
- If value provided: proceed to comparison
- If value is [NOT AVAILABLE]: flag as [DATA ABSENT: marker_name] and note analytical limitation

### Step 3: Individual Marker Comparison
Compare each submitted value against performance_optimal_ranges.json tiers:
- Below clinical_floor: flag as CRITICAL LOW
- Below acceptable lower bound: flag as SUB-OPTIMAL LOW
- Within optimal_performance range: flag as OPTIMAL
- Above acceptable upper bound: flag as ELEVATED - MONITOR
- Above elevated_flag: flag as ELEVATED - INTERVENTION REQUIRED

### Step 4: Compounding Relationship Analysis
Apply hormone_axis_matrix.md patterns to all hormone markers.
Key compound checks to always run:
- LH + FSH + Total T (HPTA axis pattern)
- Free T + SHBG + Total T (bioavailability pattern)
- E2 + SHBG + Total T (aromatization pattern)
- Cortisol + Total T (HPA-HPG competition pattern)
- Free T3 + TSH + caloric intake (thyroid conversion pattern)
- ALT + AST ratio (hepatic vs. skeletal muscle differentiation)
- Creatinine + eGFR + BUN (renal function triad)
- Fasting Insulin + TG:HDL ratio (insulin resistance composite)

### Step 5: Trend Analysis (When Prior Check-In Data Available)
If previous check-in data exists in check_in_log_template.csv:
- Calculate delta for each marker since last check-in
- Flag markers trending toward flag thresholds even if currently within range
- Note velocity of change (e.g., "ALT trending +15 U/L over 30 days - approaching flag threshold")

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

**Vector 1: Biomarker & Laboratory Analysis**

[EMERGENCY: if applicable]

CRITICAL FINDINGS:
- [Marker]: [Value] [Unit] | Optimal: [Range] | Status: CRITICAL | Action: [specific]

COMPOUNDING PATTERNS:
- [Pattern Name]: [findings and clinical interpretation]

SUB-OPTIMAL / MONITORING:
- [Marker]: [Value] [Unit] | Optimal: [Range] | Status: ELEVATED-MONITOR | Trend: [if available]

OPTIMAL:
- [List markers within optimal range briefly]

DATA ABSENT:
- [List missing markers that limit analysis]
