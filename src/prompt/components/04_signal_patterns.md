# 04 — Signal Patterns

Anchors for attention, NOT hard rules. A keyword alone is not sufficient
evidence; the surrounding sentence must show why the model was created, how it
was used, or what function it served.

```json
{
  "For Intervening":   {"positive": ["implemented", "deployed", "built", "used to create", "used to enable interoperability", "generated artifact"], "negative": ["would be implemented", "future work", "proposed only"]},
  "For Understanding": {"positive": ["understand", "clarify", "define", "conceptualize", "meaning negotiation", "shared understanding"], "negative": ["explains to external stakeholders"]},
  "For Problem-solving":{"positive": ["decision", "analyze options", "evaluate", "identify shortcomings", "what should change"], "negative": ["directly implemented after", "used to build"]},
  "For Communicating": {"positive": ["communicate", "meeting", "align stakeholders", "bridge between", "explain to", "discussion"], "negative": ["stored for future", "documentation system"]},
  "For Documenting":   {"positive": ["documentation", "knowledge base", "reference", "for future use", "knowledge management", "stored", "archived", "repository"], "negative": ["real-time", "meeting", "live discussion"]},
  "For Learning":      {"positive": ["learn modeling", "trial model", "learn OntoUML", "modeling method"], "negative": ["learn about the domain", "understand the data"]}
}
```
