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
- separation of measurement from interpretation/authority;
- versioned reproducible receipts whose derived numeric/claim fields are not caller-injectable.

Explicit V0.1 models:

```text
SCALE_MODEL=LINEAR_MIN_MAX
WEIGHTED_AGGREGATION_MODEL=COMPENSATORY_WEIGHTED_MEAN
```

Unsupported scale models are rejected rather than silently treated as linear. A compensatory weighted mean is identified as a mathematical aggregation only, not a safety/veto/authority mechanism.

Current local reference-candidate validation:

```text
PYTHON=3.13.5
OS=Linux x86_64
EXTERNAL_DEPENDENCIES=NONE
UNIT_TESTS=38
UNIT_PASS=38
UNIT_FAIL_ERROR=0
RANDOMIZED_INVARIANT_CHECKS=35000
RANDOMIZED_SEED=20260823
RANDOMIZED_RESULT=PASS
```

The current newest GitHub PR head does not have an exact-head GitHub Actions execution. The 38/38 + 35,000 PASS is therefore classified as local reference-candidate evidence, not remote CI evidence.

Failure-seeking has found and corrected:

1. NaN/infinity contamination;
2. append-order language that could be mistaken for timestamp currentness;
3. extreme finite intermediate arithmetic and finite-weight sum overflow;
4. incomplete/forgeable derived receipt fields;
5. hidden linear-scale and compensatory-aggregation assumptions.

A manually requested GitHub Copilot review on an earlier head reviewed all seven files, recommended approval, and produced two concrete improvement comments: canonicalize validated Scale endpoints and avoid repeated bead rescans in weighted lookup. Both were addressed, replied to, and resolved. Copilot is advisory only and is not merge authority. A fresh current-head review is still required before treating that review as current.

Important limits:
- no claim of scientific validity for arbitrary dimensions;
- no prediction or semantic-equivalence claim;
- no authority/permission behavior;
- no timestamp-currentness engine;
- no generic logarithmic/ordinal scale semantics;
- no Windows/macOS validation yet;
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
APPEND ORDER != OBSERVED-TIME CURRENTNESS
SERIALIZED RECEIPT != TRUSTED CLAIM
LINEAR SCALE != GENERIC SCALE
COMPENSATORY AGGREGATE != DECISION AUTHORITY
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

Keep PR #2 draft. Request a fresh Copilot review only after the PR head is stable; do not merge merely because local tests are green. License selection and Windows validation remain separate owner/local proof gates.
