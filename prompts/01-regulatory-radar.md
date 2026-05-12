# Prompt 01 — Regulatory Radar Entry

**Purpose:** Capture and classify a regulatory development as a structured internal intelligence log entry.

**When to run:** Immediately after identifying a qualifying regulatory development (see README for the filter criteria).

**Output feeds:** Prompts 02, 03, and 04 all draw from this entry. Run this first, every time.

---

## Prompt

```
TASK: Create a Regulatory Radar entry for Galoy's internal intelligence database.

INPUT:
- Regulatory development: {{paste headline or brief summary of the development}}
- Source document: {{official document name, issuing body, and date if known}}
- URL or reference: {{direct link, or write "not available"}}

OUTPUT FORMAT — use this structure exactly, including bold labels:

**Date Logged:** [today's date]
**Issuing Body:** [OCC / FDIC / Federal Reserve / NCUA / State: ___]
**Document Type:** [Final Rule / Bulletin / Interpretive Letter / Statement / Proposed Rule / Other]
**Title:** [official document title, or best available description]
**One-Line Summary:** [what it says, plain English, 20 words maximum]
**Galoy Relevance Score:** [High / Medium / Low] — [one sentence explaining the relevance]
**Key Implication:** [what this means for banks considering Bitcoin or stablecoin infrastructure, 2-3 sentences]
**Action Flag:** [Content / BD Outreach / Monitor / No Action]
**Tags:** [select all that apply: lending | payments | custody | stablecoin | licensing | AML | capital-requirements | state-charter | federal-charter]
```

---

## Field Reference

| Field | Notes |
|-------|-------|
| **One-Line Summary** | This is the field Prompts 02 and 04 pull from directly. Keep it factual, not editorialized. |
| **Galoy Relevance Score** | High = directly affects bank ability to offer Bitcoin products. Medium = indirectly relevant or state-level. Low = monitor only. |
| **Key Implication** | This feeds Prompt 02. Write it from the perspective of a bank compliance officer, not a Bitcoin advocate. |
| **Action Flag** | Content = queue for newsletter + LinkedIn. BD Outreach = trigger Prompt 04 for target banks. Monitor = log only. No Action = archive. |
| **Tags** | Used to filter the radar log by Galoy product line. Tag generously — an entry can have multiple tags. |

---

## Design Notes

The fixed output format makes every entry machine-readable and consistent regardless of who runs the prompt. Tags enable filtering the `regulatory_radar_log.md` by product line without reading every entry.

The Relevance Score + Action Flag pairing is intentional: Score tells you *what it is*, Flag tells you *what to do next*. A quick scan of the log gives the team a full triage picture without opening individual entries.

One thing this prompt won't do well: judge political likelihood for proposed rules. If the input is a Proposed Rule, the Key Implication should note that it's in comment period and reflect uncertainty accordingly. Don't let the model state a proposed rule as settled policy.
