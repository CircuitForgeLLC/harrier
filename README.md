# Harrier — Insurance Navigation

> *Part of the Circuit Forge LLC "AI for the tasks you hate most" suite.*

**Status:** Backlog — not yet started. Peregrine must prove the model first.

## What it does

Harrier handles the full insurance fight: prior authorization tracking, claim dispute drafting, EOB (Explanation of Benefits) reconciliation, internal and external appeal letters, and state insurance commissioner complaints.

The harrier is low, fast, and persistent — exactly what fighting a denied claim requires.

## Why it's hard

Insurance disputes are engineered to be abandoned:
- Prior auth processes have no standard timeline or format across insurers
- EOBs are intentionally opaque — reconciling them against bills requires expertise
- Appeal deadlines are short (30–60 days internal, 4 months external)
- The regulatory landscape is complex: state insurance codes, ACA requirements, ERISA for employer plans

## Core pipeline

```
Log claim / denial / prior auth request
→ AI analyzes EOB + denial reason → Drafts appeal with clinical rationale
→ Human review + attach supporting docs → Submit appeal
→ Track deadline + escalation windows → External appeal / commissioner complaint if needed
```

## Key differentiators vs. Peregrine

- Medical + insurance jargon parsing (CPT codes, ICD codes, denial reason codes)
- Regulatory citation engine: state insurance code, ACA provisions, ERISA
- External appeal automation: state IDRE (Independent Dispute Resolution Entity) filing
- EOB reconciliation: match line items against Explanation of Benefits

## Product code (license key)

`CFG-HRRR-XXXX-XXXX-XXXX`

## Tech notes

- Shared `circuitforge-core` scaffold
- PDF parsing (pdfplumber) for EOBs and denial letters
- CPT/ICD code lookup: CMS public datasets
- State insurance department contact directory (structured YAML)
- Vision module: scan paper EOBs and denial letters via moondream2 / Claude vision
