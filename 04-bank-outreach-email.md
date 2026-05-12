# Prompt 04 — Bank Outreach Email

**Purpose:** A targeted cold or warm outreach email to a specific bank, using the regulatory development as the opening context and hook.

**Input source:** Prompt 01's `One-Line Summary`, plus manual research on the target bank. Reference `knowledge-base/bank-segment-profiles.md` to match the bank type before running.

**Output feeds:** Nothing downstream — terminal output for BD use. Human review required before sending.

---

## Prompt

```
TASK: Write a short outreach email from Galoy to a specific bank contact, using a
recent regulatory development as the opening context.

INPUT:
- Regulatory context: {{paste One-Line Summary from Prompt 01}}
- Bank name: {{full legal name of the target bank}}
- Contact role: {{CEO / Chief Digital Officer / CRO / Head of Strategy / other}}
- Bank profile notes: {{paste any known details: asset size, charter type (national /
  state / credit union), current fintech posture, relevant recent news, digital asset
  activity — or write "minimal research available"}}
- Galoy product most relevant to this bank: {{Bitcoin-backed lending / stablecoin
  payments / Bitcoin brokerage / general infrastructure inquiry}}
- Sender name and title: {{your name and role at Galoy}}

CONSTRAINTS:
- Subject line: specific and informational — state the regulatory topic plainly,
  optionally reference the bank by name
- Body: 110-130 words maximum
- Do not open with "I hope this email finds you well" or any variant
- Do not open with a compliment about the bank
- Reference the regulatory development in the first two sentences
- One product concept maximum — do not list features
- The ask is a 20-minute call only — nothing more
- Tone: peer-to-peer; write as someone who tracks this space, not as a vendor pitching
- If bank profile notes are minimal, keep claims about the bank general — do not
  fabricate specifics

OUTPUT: Subject line on its own line, then a blank line, then the email body.
```

---

## Pre-Run Checklist

Before running this prompt, confirm the following:

- [ ] You have the correct contact name and role (check LinkedIn; don't address a generic title if you have a name)
- [ ] Bank profile notes include at minimum: asset size tier (community <$1B / mid-size $1-10B / regional $10B+) and charter type
- [ ] The Galoy product you've selected actually maps to this bank's profile — see `bank-segment-profiles.md` for guidance
- [ ] You've verified the regulatory development is relevant to this bank's charter type (e.g., OCC guidance applies to national charter banks, not state-chartered institutions under FDIC primary supervision)

---

## Post-Run Review

Before sending any output from this prompt:

- [ ] Verify all bank-specific claims in the email against your research notes — the model can hallucinate details if profile notes were thin
- [ ] Confirm subject line doesn't read as spam-filter bait (avoid all-caps, excessive punctuation, words like "opportunity" or "solution")
- [ ] Check word count — if it ran over 130 words, cut the least specific sentence first
- [ ] Read aloud: if it sounds like a marketing email, rewrite the opening

---

## Design Notes

**Why 110-130 words:** Cold emails from vendors rarely get read past the first three sentences by senior bank executives. The word count constraint forces a genuine editorial decision: what is the single most important thing this person needs to know? If you can't answer that in 130 words, the pitch isn't ready.

**Why peer-to-peer tone:** Bank executives receive dozens of vendor pitches monthly. The ones that get responses typically read like they came from someone who genuinely follows the space — not from a sales process. The regulatory hook serves this: it frames Galoy as a team tracking the same developments the banker tracks, not a company cold-calling a prospect list.

**Why one product concept maximum:** A feature list in a cold email signals that the sender doesn't know enough about the recipient to know what's relevant. One specific, well-chosen product reference shows you did the research. If you genuinely don't know which product fits, use "general infrastructure inquiry" and keep the email focused entirely on the regulatory context.
