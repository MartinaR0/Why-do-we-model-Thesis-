# 03 — Taxonomy of Functional Goals

Full per-goal detail (definition + signal patterns + disambiguation) is in
`../../codebook/`. The definitions below are the ones embedded in the prompt.

1. **For Intervening** — A goal of using a model as an instrument through which
   one changes something in the world. The model directly guides or enables the
   creation of a system, artifact, or implementation. The model is actively used
   to build something, not merely proposed. Actual implementation is strong
   evidence, but an explicitly stated intended use for implementation,
   integration, transformation, artifact generation, or system development may
   also count when the paper frames this as the model's purpose.

2. **For Understanding** — A goal of creating a model to support domain
   understanding and meaning negotiation. The model helps people develop
   knowledge about a domain, clarify concepts, or negotiate shared meaning.

3. **For Problem-solving** — A goal of using a model to guide problem-solving
   and decision making. The model helps stakeholders identify what needs to
   change or make a decision, but the model itself is NOT the implementation
   instrument.

4. **For Communicating** — A goal of using a model to support communication
   between people about a domain of interest (meetings, explanations, live
   discussion bridging different groups). If the paper explicitly states that the
   model supports communication between stakeholders but does not specify whether
   it is synchronous or asynchronous, code Communicating only when the context
   suggests interaction, explanation, alignment, or discussion between distinct
   people or groups.

5. **For Documenting** — A goal of using a model to support asynchronous
   communication between people about a domain of interest: documentation,
   knowledge base, or reference for people not part of the original modeling
   process.

6. **For Learning** — A goal of creating or using a model to learn modeling,
   modeling methods, and modeling tools. The goal is to gain MODELING knowledge,
   not domain knowledge.
