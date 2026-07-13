# Understanding Why We Model: An LLM-Based Analysis of Conceptual Modeling Literature

This repository contains everything needed to reproduce the classification study.
The prompt sent to the LLM is provided as one complete file

This repository contains everything needed to reproduce the classification study from the thesis Understanding Why We Model: An LLM-Based Analysis of Conceptual Modeling Literature

The study tests whether the six functional goals of modeling identified by Sousa et al. describe the modeling purposes reported in the OntoUML/UFO conceptual modeling literature, and evaluates which large language model is most suitable for extracting and classifying those purposes from academic papers.

# Repository structure 
.
├── Dataset/             # The Excel workbooks produced by the analysis
├── MD/                  # All papers from the revised catalog, converted to Markdown
├── llm_classification/  # Raw LLM output (pure JSON), per subset
│   └── scale_up/        # Claude's full classification of the 104 scale-up papers
├── prompt/              # The exact prompt sent to the model, plus per-block components and codebook
└── main.py              # Classification runner


Dataset/

The Excel workbooks the analysis was built on:


the comparison workbook — the LLM-vs-human evaluation on the 40-paper reference set (per-model KPIs, per-goal accuracy, per-paper agreement, disagreements, and a combined per-model view against the gold reference);
the scale-up workbook — the goal-frequency counts from Claude's classification of the full corpus;

MD/

Every paper in the revised OntoUML/UFO catalog, converted from PDF to Markdown with Docling. Image content is removed, since classification is based on text rather than diagrams.

llm_classification/

The pure, unedited JSON output from the models, organized per subset. Each file is one model's classification of one paper, following the schema in prompt/components/08_output_format.json.

The scale_up/ subfolder holds the full Claude classification of the 104 papers that were not part of the 40-paper reference set

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
