# Galoy Regulatory Content Pipeline

A structured prompt workflow that converts a single regulatory input into four publication-ready outputs — an internal intelligence log entry, a newsletter section, a LinkedIn post, and a targeted BD outreach email.

Built as an assessment submission for the Galoy Marketing & BD Internship (Summer 2026).

---

## How It Works

```
Regulatory Input (OCC bulletin, Fed guidance, state charter update)
        │
        ▼
┌─────────────────────┐
│  01 · Radar Entry   │  ← Internal intelligence log
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│  02 · Newsletter    │  ← The Bitcoin Banking Standard
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│  03 · LinkedIn Post │  ← C-suite banker audience
└─────────┬───────────┘
          │  (+ bank research)
          ▼
┌─────────────────────┐
│  04 · Outreach Email│  ← BD / sales enablement
└─────────────────────┘
```

Each prompt is self-contained but designed to chain. Output from Prompt 01 feeds Prompt 02, and so on. Prompt 04 draws from all three prior outputs plus a bank-specific research input.

**Total time from input to four outputs: under 20 minutes, with editing.**

---

## Repo Structure

```
galoy-prompt-workflow/
├── README.md                        # This file
├── system-prompt.md                 # Base context — set once per session
├── prompts/
│   ├── 01-regulatory-radar.md       # Internal intelligence log entry
│   ├── 02-newsletter-section.md     # The Bitcoin Banking Standard
│   ├── 03-linkedin-post.md          # LinkedIn, C-suite banker audience
│   └── 04-bank-outreach-email.md    # BD cold/warm outreach
├── knowledge-base/
│   ├── galoy-product-overview.md    # What Galoy builds and how
│   ├── bank-segment-profiles.md     # Target bank type profiles
│   └── banned-phrases.md           # Content quality filter
└── examples/
    └── sample-run.md               # Full walkthrough with sample outputs
```

---

## Setup

### Option A — Claude Projects (Recommended)

1. Create a new Claude Project
2. Upload all files from `knowledge-base/` as project documents
3. Paste `system-prompt.md` as the project's system prompt
4. Run prompts from `prompts/` sequentially in the conversation

The knowledge base files load automatically into context every session. No re-pasting required.

### Option B — Any LLM with System Prompt Support

1. Paste `system-prompt.md` as the system context
2. Manually include relevant `knowledge-base/` content in your first message
3. Run prompts in order, carrying outputs forward

---

## What Counts as a Qualifying Regulatory Input

Not every regulatory headline is worth running through the pipeline. Before starting:

**Run it if:**
- A federal banking regulator (OCC, FDIC, Federal Reserve, NCUA) issues a bulletin, final rule, interpretive letter, or statement
- A state banking department updates its money transmission or digital asset licensing framework
- Congress advances legislation with direct implications for bank-held digital assets
- A major bank announces a Bitcoin or stablecoin product (signals implicit regulatory green-lighting)

**Skip it if:**
- It's a think tank opinion with no enforcement weight
- It rehashes existing guidance without a new interpretive position
- It's crypto-native regulation (SEC, CFTC) with no direct bank nexus

---

## What This Workflow Doesn't Do

It doesn't replace judgment. Prompt 01's Relevance Score needs a human check — the model doesn't know Galoy's current sales pipeline or which bank verticals are being prioritized. Prompt 04 in particular needs someone to verify the bank profile notes before sending; a wrong assumption about asset size or charter type can sink a cold email.

The workflow handles volume and consistency. The human handles context and accuracy.

---

## Contributing / Iterating

Each prompt file includes a "Design Notes" section explaining why constraints are set the way they are. If you're refining a prompt, update that section to document what changed and why. This keeps the library useful for whoever runs it next.

---

*Submitted for the Galoy Marketing & BD Internship — Summer 2026*
