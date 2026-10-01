# PP-SPEC-040: Proof of Efficacy Mapping to NIST AI 100-2

| Field | Value |
|---|---|
| Status | DRAFT v0.1 |
| Author | Craig Ellrod, Nebulonium, Inc. (dba HACKERverse®) |
| Date | October 1, 2026 |
| License | CC BY 4.0 |
| Maps to | NIST AI 100-2, Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations |
| Series | Proof Protocol Framework Mapping Specifications |

---

## 1. Purpose

This specification defines how adversarial machine-learning attack, taxonomy, and mitigation context from NIST AI 100-2 can be bound to Proof Protocol test cases, evidence, and efficacy results.

NIST remains authoritative for its publication, terminology, taxonomy, and definitions. This document defines a **Proof Protocol mapping** and does not supersede or modify NIST AI 100-2.

## 2. Scope

NIST AI 100-2 supplies adversarial machine-learning terminology and attack/mitigation context that can identify what should be exercised. Proof Protocol supplies an independent evidence model for determining what happened during a test and whether a selected defensive control or mitigation performed as claimed.

Independent witnessing and evidence-capture implementation are defined elsewhere in the Proof Protocol specification family.

## 3. Core Question

Proof of efficacy asks:

> **Was there a control, and did it work?**

A taxonomy can classify an attack or mitigation. Proof Protocol adds experimental evidence about the behavior of a particular implemented control under defined adversarial conditions.

## 4. Metric Definitions

Against a defined adversarial corpus, each case is recorded as **blocked**, **detected**, **missed**, or **INVALID**.

Relevant measurements include:

- containment rate;
- detection rate;
- miss rate;
- false-positive rate against paired benign cases;
- robustness against attack variants, manipulation, evasion, poisoning, extraction, inference, or other applicable adversarial conditions;
- version-level results; and
- INVALID status when required evidence is incomplete or broken.

Target levels are engagement- and risk-specific rather than imposed by this mapping.

## 5. Evidence Produced

Mapped tests can produce:

- **Proof records** binding NIST taxonomy context, test case, control/mitigation, system/version, verdict, timestamp, and evidence references;
- **ProofStamp™** trusted timestamps bound to evidence/verdict objects;
- **ProofBundle™** packages containing proof records, metrics, corpus manifests, and environment/context;
- **ProofRegister™** records for issued proof artifacts; and
- corpus and environment manifests identifying the tested adversarial conditions.

## 6. Mapping to NIST AI 100-2

| NIST AI 100-2 context | Proof Protocol treatment | Evidence |
|---|---|---|
| Attack class/category | Record the applicable taxonomy classification as test context. | Corpus/test metadata |
| Attack goal or capability | Bind the adversarial objective and assumptions to the test case. | Test definition |
| Attack technique/condition | Exercise an independently defined reproducible case representing the condition. | Execution evidence |
| Mitigation/control | Record the mitigation claim separately from observed behavior. | Control descriptor |
| Detection expectation | Measure whether the exercised condition was identified. | Detection result |
| Prevention/containment expectation | Measure whether the attack objective reached the protected target. | Outcome evidence |
| Attack variant/evasion | Exercise variants designed to manipulate, evade, or bypass the mitigation. | Robustness evidence |
| System/model context | Bind material model, data, policy, control, application, and environment versions to the result. | Environment descriptor |
| Downstream effect | Obtain target, application, SIEM, vendor, model, or equivalent evidence when necessary to establish efficacy. | Outcome evidence |

## 7. Interoperability Rules

1. The NIST publication identifier/version and relevant taxonomy element SHOULD be recorded when applicable.
2. NIST terminology and classifications MUST NOT be silently redefined.
3. Proof Protocol verdicts are Proof Protocol results; they are not NIST scores, certifications, or endorsements.
4. A mitigation's presence, configuration, activation, and efficacy are distinct facts.
5. A control firing does not by itself establish efficacy when the claim concerns protection of a downstream target or outcome.
6. Target, application, model, SIEM, vendor, or equivalent evidence SHOULD complete the evidence round trip when required.
7. Missing required evidence MUST yield **INVALID**, not PASS.
8. Material changes to the tested model, system, data, control, policy, environment, taxonomy mapping, or corpus SHOULD trigger retesting where they can affect the result.

## 8. Framework-Agnostic Architecture

> **Threat frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks can identify **what to test**: threats, vulnerabilities, attack classes, controls, mitigations, design assertions, identity claims, or risk conditions. Proof Protocol independently establishes **whether the control worked and what evidence proves that result**.

No external framework is required for Proof Protocol to operate. A Proof Protocol implementation MAY use NIST AI 100-2, MITRE ATLAS, MAESTRO, OWASP, AIVSS, a proprietary threat model, another recognized framework, or no external framework at all when the test condition is otherwise sufficiently defined.

Adding, replacing, muting, or removing a framework mapping does not alter the Proof Protocol architecture, evidence model, Proof of Efficacy determination, ProofBundle™, ProofStamp™, ProofRegister™, or independent corroboration requirements.

A framework mapping therefore establishes **interoperability**, not architectural dependency.

## 9. Relationship to Proof Protocol

This mapping is part of the Proof Protocol specification family maintained by Nebulonium, Inc.

The relationship is intentionally asymmetric:

> **NIST AI 100-2 supplies adversarial machine-learning taxonomy and attack/mitigation context. Proof Protocol supplies the evidence model for determining whether a selected defensive control or mitigation performed as claimed.**

No affiliation, endorsement, certification, or sponsorship by NIST is implied.

## 10. Source Framework, Attribution, and License

NIST AI 100-2 is an external NIST publication. NIST remains the authoritative source for its content and terminology.

This mapping cites and summarizes NIST concepts for interoperability and does not substantially reproduce the publication. This Proof Protocol mapping is independently authored and licensed under **CC BY 4.0**.

NIST names, publication identifiers, and any third-party material appearing in NIST publications remain subject to their applicable terms.

## 11. References

- NIST AI 100-2, *Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations*.

## 12. Versioning

This mapping is versioned independently of NIST AI 100-2. Material upstream changes SHOULD trigger a mapping review and, where necessary, a new version identifying the NIST publication revision mapped.

---

*Proof Protocol · proofprotocol.io · CC BY 4.0*
