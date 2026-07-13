# 07 — Procedure

Perform silently; output only the JSON.

1. Read the full paper.
2. Identify the model(s) and the sentences describing why each model was created
   or how it was used.
3. Map qualifying evidence to the taxonomy using the definitions, signal
   patterns, and disambiguation rules.
4. Classify each goal into "goals" (High/Medium, present) or "uncertain_goals"
   (Low). Any of the six goals not placed in either array is treated as absent —
   do not enumerate absent goals.
5. Record any purpose that fits no goal in "outside_taxonomy".
6. Emit only the JSON object below, with no text, markdown, or commentary outside
   it. Valid, parseable JSON; no trailing commas.
