# Elite Performance & Bio-Optimization Coaching Engine

Advanced AI coaching system for elite sports performance professionals. Designed for use with Claude via MCP File System or Google Sheets servers.

## Output Vectors
- Vector 1: Biomarker & Laboratory Analysis
- Vector 2: Nutritional Course Correction
- Vector 3: Supplementation Stack Adjustments
- Vector 4: Training Strain Management

## Repository Structure
- /system-prompts/ — coach_engine_v1.md, check_in_template.md, emergency_flags.md
- /reference-ranges/ — performance_optimal_ranges.json, hormone_axis_matrix.md, supplement_interaction_map.json
- /skills/ — biomarker_analysis.md, nutritional_correction.md, supplementation_stack.md, training_strain_management.md
- /data-schemas/ — client_profile_schema.json, check_in_log_template.csv
- /examples/ — sample_check_in_anonymized.md, edge_cases.md

## How to Use
1. Feed coach_engine_v1.md into your Claude instance as the system prompt.
2. Mount /reference-ranges/ and /data-schemas/ via your MCP File System server.
3. Submit a completed check_in_template.md as the user message.
4. Receive a structured four-vector analysis output.
5. Log all check-in data to check_in_log_template.csv for longitudinal tracking.

## No-Hallucination Contract
All biomarker evaluations are anchored to performance_optimal_ranges.json.
Every recommendation must cite a specific client data field.
Ranges from general training data are never used.

## Versioning
System prompt versions tracked in /system-prompts/ with _v[N] suffixes.
Increment version on any change to analytical logic or output structure.
