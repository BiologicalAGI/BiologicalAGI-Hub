# BiologicalAGI Public Contribution Index

Status: **DRAFT / ORIENTATION / NON-RUNTIME**  
Date: 2026-08-23

## Purpose

Provide a small evidence-based map of public BiologicalAGI work without treating repository visibility as proof of maturity.

Classification vocabulary:

- `TESTED_REFERENCE` — executable artifact with a bounded validation record.
- `RESEARCH_DRAFT` — documented research/design, not production truth.
- `ORIENTATION` — documentation/navigation only.
- `PLACEHOLDER_OR_EARLY` — public artifact exists but is not being promoted as mature.
- `PRIVATE_NOT_LINKED` — intentionally excluded from the public map.

## Current public contribution

### Transparent Instruments — Abacus + Slide Ruler V0.1

Repository: `BiologicalAGI/Stella-Prime`  
Draft PR: `#2`  
Branch: `contrib/transparent-instruments-v0-1`  
Classification: `TESTED_REFERENCE / PUBLIC_DRAFT`

Purpose:
- provenance-carrying multidimensional observations (`Abacus`);
- explicit continuous scale alignment/comparison (`Slide Ruler`);
- explicit-only weighting;
- separation of measurement from interpretation/authority.

Current recorded validation:

```text
PYTHON=3.13.5
OS=Linux x86_64
EXTERNAL_DEPENDENCIES=NONE
UNIT_TESTS=18
UNIT_PASS=18
UNIT_FAIL_ERROR=0
RANDOMIZED_INVARIANT_CHECKS=25000
RANDOMIZED_SEED=20260823
RANDOMIZED_RESULT=PASS
```

Evidence history matters: the first 12-test pass was followed by an adversarial review that found a real non-finite-number defect (`NaN`/infinity could contaminate normalization/weighting). The code was hardened, the expanded 18-test suite became the current unit baseline, and a committed fixed-seed driver then passed 25,000 additional implementation-invariant checks. The earlier pass remains documented rather than erased.

Important limits:
- no claim of scientific validity for arbitrary dimensions;
- no prediction or semantic-equivalence claim;
- no authority/permission behavior;
- no Windows validation yet;
- repository license is not yet selected, so public visibility is not presented as a grant of open-source reuse rights.

## Public research

### Stella Luanti V0.2 research

Repository: `BiologicalAGI/Stella-Prime`  
Branch: `research/luanti-v0.2-build-contract-2026-08-23`  
Classification: `RESEARCH_DRAFT`

Purpose:
- renderer-independent world/event semantics;
- explicit observation/report/knowledge distinctions;
- bounded companion proposal/policy separation;
- accessibility/recovery proof planning;
- open-source reciprocity and Luanti evidence-capture planning.

Important limit: GitHub research does not establish current local-machine state or authorize local/canonical mutation.

## Public orientation surfaces

### BiologicalAGI-Hub

Classification: `ORIENTATION`

This repository is the public documentation/navigation surface. It is not a runtime, deployment, automation, or active-agent system.

### travis-project-hub

Classification: `ORIENTATION / LOCAL-WORKFLOW MAP`

This repository currently documents relationships among local development projects. References to private projects do not make those private projects public or validated.

## Public early/placeholder projects

The following repositories are intentionally **not promoted as mature** by this index:

- `BiologicalAGI/DGE` — `PLACEHOLDER_OR_EARLY`
- `BiologicalAGI/Holographic-adaptation-` — `PLACEHOLDER_OR_EARLY`
- `BiologicalAGI/UEIF-system-integration` — `PLACEHOLDER_OR_EARLY`

Public existence is evidence only that an artifact/repository exists, not that its claims are implemented or validated.

## Private operational/research systems

Private repositories are intentionally not expanded into this public index. Their existence does not imply public availability, production readiness, or permission to redistribute their contents.

Examples include private TCV/ABACUS and SCOS workspaces.

## Contribution discipline

```text
VISIBLE != VALIDATED
TESTED != PRODUCTION
RESEARCH != CURRENT MACHINE STATE
CAPABILITY != AUTHORITY
PUBLIC BRANCH != CANONICAL MAIN
AI-ASSISTED ANALYSIS != HUMAN UNDERSTANDING
```

When a public artifact is promoted, record:

1. what was actually executed/observed;
2. environment/version where relevant;
3. what failed or remains untested;
4. whether licensing permits reuse;
5. whether the artifact is merged/canonical or only a branch/draft;
6. provenance and significant AI assistance where relevant to upstream policy.

## Current next public step

Review Transparent Instruments draft PR #2, choose an explicit software license if reusable open-source distribution is intended, then continue failure-seeking and add cross-platform validation before expanding features.
