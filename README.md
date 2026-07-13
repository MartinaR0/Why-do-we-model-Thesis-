# Why-do-we-model-Thesis-

This repository contains everything needed to reproduce the classification study.
The prompt sent to the LLM is provided as one complete file


## Prompt layout

`prompt/prompt_full.txt` is the exact, assembled prompt as sent to the model.
`prompt/components/` contains the same text split into logical blocks:

1. `01_role.md` — who the model is told to be
2. `02_reading_and_unit.md` — which sections to read; what counts as one unit
3. `03_taxonomy.md` — the six functional goals (points to `codebook/` for detail)
4. `04_signal_patterns.md` — positive/negative anchors per goal
5. `05_disambiguation_rules.md` — how to resolve competing goals
6. `06_evidence_and_confidence.md` — quoting rules + confidence levels
7. `07_procedure.md` — the ordered steps the model performs
8. `08_output_format.json` — the required JSON output schema

## Codebook

`codebook/` re-organizes the goal information by goal, so a reader who wants to understand one goal (e.g. "For Documenting") finds its definition, signal patterns, and disambiguation rules in a single file: `codebook/for_documenting.md`.

The content in `codebook/` is the same as in `prompt/components/`, only grouped per goal instead of per prompt-block.
