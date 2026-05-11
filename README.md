# Harrier — Government Forms & Benefits Navigation

> *Part of the Circuit Forge LLC "AI for the tasks you hate most" suite.*

**Status:** Backlog — not yet started. Peregrine must prove the model first.

## What it does

Harrier guides you through government forms and benefit applications — translating bureaucratic requirements into plain language, pre-filling what it can, and tracking deadlines so nothing lapses. Covers benefits, FAFSA, immigration paperwork, and permit processes.

The harrier is low, fast, and persistent — exactly what navigating government systems requires.

## Why it's hard

Government forms are designed for compliance, not usability:
- Applications are long, interdependent, and punish small errors with delays or denials
- Eligibility rules vary by state, household composition, income, and program
- Deadlines are strict and consequences of missing them are severe
- Immigration forms carry legal risk if misunderstood or incorrectly filed

## Core pipeline

```
Identify the form or benefit needed
→ AI explains eligibility requirements in plain language → Gather required documents
→ Pre-fill draft with AI assistance → Human review + submit
→ Track status + follow-up deadlines → Draft appeals if denied
```

## Coverage areas

- **Benefits:** SSI, SNAP, Medicaid, housing assistance, TANF
- **Education:** FAFSA, state grants, dependency edge cases
- **Immigration:** I-130, I-485, N-400, DACA renewal, travel documents
- **Permits & licenses:** by jurisdiction (building, business, professional)

## Product code (license key)

`CFG-HRRR-XXXX-XXXX-XXXX`

## Tech notes

- Shared `circuitforge-core` scaffold
- PDF parsing (pdfplumber) for government form templates
- Eligibility rule engine: structured YAML by program + jurisdiction
- State agency contact directory
- Vision module: scan mailed notices via moondream2 / Claude vision
