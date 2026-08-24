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
- explicit continuous linear-scale alignment/comparison (`Slide Ruler`);
- explicit-only weighting;
- separation of measurement from interpretation/authority;
- versioned reproducible receipts whose derived numeric/claim fields are not caller-injectable.

Explicit V0.1 contracts:

```text
SCHEMA_VERSION=transparent-instruments/0.1
SCALE_MODEL=LINEAR_MIN_MAX
WEIGHTED_AGGREGATION_MODEL=COMPENSATORY_WEIGHTED_MEAN
STORAGE_CONTRACT=PUBLIC_API_APPEND_ONLY_NOT_TAMPER_PROOF
```

Unsupported scale models are rejected rather than silently treated as linear. A compensatory weighted mean is identified as mathematical aggregation only, not a safety/veto/authority mechanism.

### Current execution evidence

The contribution now has a read-only GitHub Actions matrix (`permissions: contents: read`) with no external Python-package installation. The tested source head completed successfully across:

```text
ubuntu-latest / Python 3.12   PASS
ubuntu-latest / Python 3.13   PASS
windows-latest / Python 3.12  PASS
windows-latest / Python 3.13  PASS
macos-latest / Python 3.12    PASS
macos-latest / Python 3.13    PASS
```

Per matrix job, the tested contract is:

```text
UNIT_TESTS=41
PASS=41
FAIL=0
ERROR=0

SEED=20260823
ROUNDTRIP_CHECKS=10000
EXTREME_SCALE_CHECKS=10000
NARROW_SCALE_CHECKS=10000
PROJECTION_CHECKS=5000
WEIGHTED_CHECKS=5000
ALIGNMENT_CHECKS=5000
TOTAL_RANDOMIZED_INVARIANT_CHECKS=45000
RESULT=PASS
```

This establishes the tested reference behavior on GitHub-hosted Ubuntu, Windows, and macOS under CPython 3.12/3.13. It does **not** establish the user's current iBUYPOWER host, every Python implementation, scientific validity, production readiness, or authority.

### Failure-seeking record

The draft preserves corrections rather than erasing earlier green results. Failure-seeking has found and corrected:

1. NaN/infinity contamination;
2. append-order language that could be mistaken for timestamp currentness;
3. extreme finite intermediate arithmetic and finite-weight sum overflow;
4. incomplete/forgeable derived receipt fields;
5. hidden linear-scale and compensatory-aggregation assumptions;
6. precision loss on narrow same-sign floating-point intervals;
7. overbroad append-only wording and insufficient weighted-result provenance.

The narrow-interval finding was independently reproduced against high-precision decimal arithmetic, then frozen with a concrete regression and 10,000 ULP-scale randomized checks.

### Independent review

Multiple manually requested GitHub Copilot review cycles were used as advisory review, not authority. Review findings included canonical numeric storage, repeated bead scans, duplicated derived receipt fields, stale validation metadata, repository-root execution ergonomics, and wording clarity around normalized weighted position. Concrete correctness/clarity findings were corrected or explicitly bounded.

Copilot reviews are `COMMENTED` advisory evidence; they do not merge, approve, or establish scientific validity.

### Important limits / holds

- no claim of scientific validity for arbitrary dimensions;
- no prediction or semantic-equivalence claim;
- no authority/permission behavior;
- no timestamp-currentness engine;
- no generic logarithmic/ordinal scale semantics;
- public-API append-only is not tamper-proof persistence;
- the iBUYPOWER host has not yet been tested;
- repository software license is not yet selected, so public visibility is not presented as a grant of open-source reuse rights;
- PR #2 remains draft and unmerged/canonical promotion has not occurred.

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
FINITE INPUT != SAFE INTERMEDIATE ARITHMETIC
SERIALIZED RECEIPT != TRUSTED CLAIM
LINEAR SCALE != GENERIC SCALE
COMPENSATORY AGGREGATE != DECISION AUTHORITY
PUBLIC API APPEND-ONLY != TAMPER-PROOF MEMORY
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

Keep PR #2 draft. Preserve the license and iBUYPOWER holds. Do not merge or broaden claims merely because cross-platform implementation tests are green; next useful evidence should come from explicit persistence/load testing, human-factor evaluation, or the intended local-host proof rather than feature expansion.
