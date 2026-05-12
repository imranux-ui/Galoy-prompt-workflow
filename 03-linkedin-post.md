# Prompt 03 — LinkedIn Post

**Purpose:** A post for Galoy's company LinkedIn, distilling the newsletter section for a C-suite banker audience scrolling between meetings.

**Input source:** The newsletter section output from Prompt 02.

**Output feeds:** Nothing downstream — this is a terminal output. Can be published directly after a human review pass.

---

## Prompt

```
TASK: Write a LinkedIn post for Galoy's company LinkedIn account based on this
newsletter section.

INPUT:
- Newsletter section: {{paste full output from Prompt 02}}

AUDIENCE: CEOs, CROs, and Chief Digital Officers at US commercial banks and credit unions.
They are not Bitcoin natives. They are risk managers first. Most are on LinkedIn to monitor
industry developments, not to engage with content.

TONE: Confident, not evangelical. State the regulatory fact. Draw one clear inference.
Let the reader decide what to do with it.

CONSTRAINTS:
- 80-120 words maximum
- Do not open with a question
- One hashtag maximum (optional — omit if it feels forced)
- One emoji maximum (optional — omit if it adds nothing)
- Do not use: "game-changer," "exciting," "thrilled," "proud to share," "I'm honored"
- Last line must be a declarative statement — not a CTA phrase like "Let's connect!"
  or "Drop a comment below" or "What do you think?"
- Do not mention Galoy's products unless the regulatory development makes the
  product mention genuinely relevant and non-promotional

OUTPUT: The post text only. No label, no preamble.
```

---

## Design Notes

**Why no opening question:** "Is your bank ready for X?" is the single most overused pattern in B2B LinkedIn content. It signals a marketing template, not a point of view. Senior executives get pitched constantly. A confident statement differentiates.

**Why the no-CTA constraint on the last line:** Explicit engagement prompts ("What do you think?") perform well with general audiences and poorly with senior financial executives. That cohort reads, decides, and occasionally reaches out privately. Prompting them to "drop a comment" reads as amateur.

**Why 80-120 words:** LinkedIn's algorithm doesn't favor brevity the way Twitter/X does, but the audience does. A 400-word post asking a compliance officer to scroll signals low editorial judgment. Keep it tight enough that the whole thing is visible before the "see more" fold on mobile.

**On mentioning Galoy products:** The post should primarily be useful to the reader, not promotional for Galoy. If the regulatory development directly enables a Galoy product (e.g., OCC greenlights Bitcoin custody), a single natural mention is fine. If the connection is indirect, omit the product reference entirely. Credibility compounds; a hard sell on every post erodes it.
