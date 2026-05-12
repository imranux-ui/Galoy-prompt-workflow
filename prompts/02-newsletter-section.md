# Prompt 02 — Newsletter Section

**Purpose:** Turn a Radar entry into a publication-ready section for *The Bitcoin Banking Standard*, Galoy's newsletter for bank executives, compliance officers, and fintech operators.

**Input source:** The `One-Line Summary` and `Key Implication` fields from Prompt 01.

**Output feeds:** Prompt 03 (LinkedIn post).

---

## Prompt

```
TASK: Write a newsletter section for "The Bitcoin Banking Standard," Galoy's newsletter
for bank executives, compliance officers, and fintech operators.

INPUT:
- Radar summary: {{paste One-Line Summary from Prompt 01}}
- Key implication: {{paste Key Implication from Prompt 01}}
- Audience: Senior bank executives and compliance teams evaluating Bitcoin and
  stablecoin infrastructure
- Tone: Informed, direct, slightly editorial — analysis, not a press release

CONSTRAINTS:
- Length: 150-200 words
- Do not open with "In a significant development" or any variant of that phrase
- Do not use: "landscape," "ecosystem," "robust," "seamless," or "game-changer"
- Include the issuing body and document type in the first or second sentence
- End with a sentence that connects this development to a concrete decision a
  banker might face in the next 90 days
- No section headers, no bullet points — flowing prose only

OUTPUT: The newsletter section only. No title, no preamble, no sign-off.
```

---

## Design Notes

**Why the 90-day closing hook:** Newsletter readers are busy executives. The section earns its place by being actionable, not just informative. The 90-day constraint forces a specific connection between the regulatory development and an actual decision — a board presentation, a vendor RFP, a compliance review — rather than a vague "this is worth watching."

**Why banned phrases:** "Landscape," "ecosystem," and "robust" are the most statistically common AI-generated filler in financial content. Readers in compliance and risk roles notice this. The explicit ban forces more precise language.

**Why no headers or bullets:** This is a newsletter section, not a slide. It needs to read like something a person wrote for another person. Headers in a 175-word section signal a template, not an analyst.

**Tone calibration:** The audience is not Bitcoin-native. Many readers are skeptical of digital assets and primarily motivated by regulatory compliance and competitive pressure from peer banks. The section should inform them, not sell them. If the regulatory development is genuinely favorable to Bitcoin adoption, that case makes itself — don't editorialize beyond what the facts support.
