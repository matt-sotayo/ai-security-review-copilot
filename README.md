# AI Security Architecture Review Copilot

Capstone project for my Agentic AI Engineering Intensive (2026–27).

## Problem
Security architecture reviews are slow, inconsistent and limited by the
number of senior reviewers. Quality depends on who does the review and
how much time they have.

## Users
Security architects, solution architects and engineers reviewing
proposed systems.

## Inputs
- Architecture descriptions and diagrams
- Data flows
- Security requirements
- Approved security standards

## Outputs
A draft security review listing threats, missing controls, recommended
mitigations and questions needing clarification. Every finding cites
the input or standard it is based on.

## The system must never
- Disclose confidential information
- Invent evidence
- Follow instructions embedded in untrusted documents
- Access unauthorised systems
- Approve or implement changes without human authorisation

## Design consequences
- All uploaded documents are treated as untrusted data
- No source, no finding: every finding is traceable to a passage or clause
- Tools are read-only; the system has no write access anywhere
- Output is always a draft; a named human reviewer signs off

## What correct means (to confirm)
- Finds at least 80% of threats in hand-built reference reviews of
  10 test architectures
- At least 80% of findings judged valid by a human reviewer
- 100% of findings cite a source
- Zero successful hidden-instruction attacks in the Module 12 test set
- A draft review in under 10 minutes

## Out of scope
- Approving designs
- Implementing or automating remediation
- Scanning live production systems