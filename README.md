# PP-SPEC-040: Proof of Efficacy Mapping to NIST AI 100-2

**Status:** DRAFT v0.1  
**Author:** Craig Ellrod / Nebulonium, Inc. / HACKERverse®  
**License:** CC BY 4.0

**Normative specification:** [`PP-SPEC-040-NIST-AI-100-2-Adversarial-ML-Mapping.md`](./PP-SPEC-040-NIST-AI-100-2-Adversarial-ML-Mapping.md)

## Purpose

This repository defines a Proof Protocol mapping between NIST AI 100-2, *Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations*, and Proof Protocol evidence, efficacy, and proof semantics.

NIST AI 100-2 is treated as a pluggable source of adversarial machine-learning taxonomy, attack, and mitigation context. Proof Protocol remains framework-agnostic and independently establishes whether a selected control performed as claimed.

## Repository contents

- `PP-SPEC-040-NIST-AI-100-2-Adversarial-ML-Mapping.md` — normative mapping specification
- `README.md` — repository overview
- `LICENSE` — license for original Proof Protocol material
- `CONTRIBUTING.md` — contribution guidance
- `CITATION.cff` — citation metadata

## Architectural principle

> **Threat frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks identify what may be tested. Proof Protocol independently establishes whether a control worked and what evidence proves the result.

## Ownership and external-framework notice

This Proof Protocol mapping is independently authored. NIST AI 100-2 and associated NIST materials remain subject to their applicable ownership and publication terms. Mapping establishes interoperability, not dependency, endorsement, or transfer of ownership.
