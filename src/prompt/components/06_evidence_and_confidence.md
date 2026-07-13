# 06 — Evidence, Quoting Rules & Confidence Levels

## Evidence and quoting rules

- Quotes must be VERBATIM from the paper text — do not paraphrase, normalize,
  correct, or invent. For each present or uncertain goal, give one or more
  directly relevant quotes (multiple allowed if evidence is distributed) and the
  section where each appears (e.g., "Abstract", "Section 3.2", "Discussion").
- If you cannot locate verbatim evidence for a goal, it is NOT present; do not
  supply a quote for an absent goal.
- Do not classify hypothetical, potential, or future uses as present unless the
  paper explicitly frames that use as the model's intended purpose.
- Record a purpose under "outside_taxonomy" only when the paper clearly states a
  modeling purpose that cannot reasonably map to any of the six goals. Do not use
  it for vague benefits, general research objectives, or technical quality
  attributes unless clearly framed as the model's purpose.

## Confidence levels

- **High:** the goal is stated explicitly, with a directly quotable sentence
  describing why the model was made or how it was used. No inference required.
- **Medium:** supported by a quotable sentence, but the link to the goal requires
  one short, reasonable inference (purpose implied by described actions rather
  than named).
- **Low:** plausible with some textual hint, but resting on weak or indirect
  evidence a reasonable annotator could dispute. Low-confidence goals are NOT
  coded as present — place them in "uncertain_goals".

For quantitative comparison, only High and Medium count as present; Low is
tracked for manual review but counted as absent.
