# Task 1 — Legal Scope, Asset Inventory & Threat Model

**Project:** Authorized Security Assessment of a Local OWASP Juice Shop Lab  
**Prepared by:** Akshaya C.A.  
**Purpose:** Educational security documentation for a controlled local lab.

## Project status

This repository provides a **ready-to-review planning dossier**: scope, asset inventory, data-flow diagram, STRIDE threat register, abuse cases, risk ratings, and rules of engagement.

The repository does **not** claim that a live security test, vulnerability discovery, or remediation validation has been completed. The lab setup and any practical checks must be performed separately before describing them as completed.

## Repository contents

- `01-authorization-and-scope.md` — authorization assumptions, boundaries, and exclusions
- `02-asset-inventory.md` — assets, owners, classifications, and trust boundaries
- `03-data-flow.md` — data-flow diagram and explanation
- `04-stride-threat-register.md` — STRIDE threats, abuse cases, risks, and mitigations
- `05-rules-of-engagement.md` — test windows, evidence handling, escalation, and stop conditions
- `06-risk-methodology.md` — risk-rating method and prioritization
- `diagrams/data-flow.mmd` — editable Mermaid data-flow diagram

## Lab assumptions

The proposed target is OWASP Juice Shop running locally on the student's own computer, bound to `127.0.0.1` only. The assessment is limited to the intentionally vulnerable training application and its local supporting components. No public or third-party systems are in scope.

## Suggested GitHub description

A cybersecurity internship task documenting legal scope, asset inventory, data flows, STRIDE threats, risk prioritization, and rules of engagement for a local intentionally vulnerable web-application lab.
