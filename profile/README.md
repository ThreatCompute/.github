# ThreatCompute Organization

[![Latest Release](https://img.shields.io/github/v/release/ThreatCompute/ThreatCompute?display_name=tag&sort=semver)](https://github.com/ThreatCompute/ThreatCompute/releases/latest)
[![CI](https://github.com/ThreatCompute/ThreatCompute/actions/workflows/ci.yaml/badge.svg)](https://github.com/ThreatCompute/ThreatCompute/actions/workflows/ci.yaml)
[![Docs](https://img.shields.io/badge/docs-site-blue)](https://threatcompute.github.io/ThreatCompute/)
[![Codecov](https://codecov.io/gh/ThreatCompute/ThreatCompute/branch/main/graph/badge.svg)](https://codecov.io/gh/ThreatCompute/ThreatCompute)

---

## Mission
Accelerate practical, explainable threat modeling and quantitative attack path analysis for cloud‑native (Kubernetes) environments through a reproducible, automation‑first open source stack.

## Flagship Project
**Repository:** [`ThreatCompute/ThreatCompute`](https://github.com/ThreatCompute/ThreatCompute)

Delivers:
- Automated threat modeling (LLM‑assisted or fully offline deterministic mode)
- Time‑to‑Compromise (TTC) scoring & aggregation
- Probabilistic attack graph generation / exploration
- Reproducible offline pipelines for CI & security engineering workflows

## Key Capabilities
- MITRE ATT&CK technique contextualization for Kubernetes assets
- Offline deterministic mode (`TC_OFFLINE=1`) to eliminate external model dependencies during tests/CI
- Structured graph representations (system model → threat model → attack graph)
- Extensible TTC computation (vulnerabilities, misconfigurations, heuristic weights)
- Exportable graph artifacts (GML / PDF) and path enumeration

## Quick Start
1. Visit the [documentation site](https://threatcompute.github.io/ThreatCompute/) (Material theme).
2. Clone the main repo: `git clone https://github.com/ThreatCompute/ThreatCompute.git`
3. Install dependencies & enable offline mode for first runs: `export TC_OFFLINE=1`
4. Run tests: `pytest -q`
5. Generate a threat model using `build_threat_model(...)` (see docs usage examples).

## Documentation
The published docs include:
- Getting Started & Installation
- Offline Mode Guide
- Usage: Threat Modeling, Attack Graphs, TTC
- Advanced Attack Graph & TTC Details
- Style & Contribution Guidelines

> Advanced pages (e.g., attack graph deep dive, TTC internals) are iteratively expanding.

## Ecosystem Repositories (Growing)
| Area | Purpose |
|------|---------|
| `ThreatCompute/ThreatCompute` | Core engine: modeling, graphs, TTC, docs, tests |
| `.github` (this profile) | Organization front page & shared community metadata |

(Additional focused tooling, integrations, and adapters will appear as separate repos over time.)

## Architecture (High Level)
```
System Model  -->  Threat Modeling (tactics & techniques)  -->  TTC Quantification  -->  Attack Graph Exploration
(Graph ingestion)        (LLM or offline synthesis)          (node/path weights)         (risk/path analysis)
```

## Roadmap (Next Milestones)
- 0.2.x: Automated API reference (mkdocstrings) & higher coverage threshold
- Extended TTC models (dynamic weighting, confidence intervals)
- Multi‑cluster & multi‑cloud asset ontology support
- Visualization enhancements (interactive path prioritization)

Track progress via issues & milestones in the main repo.

## Contributing
We welcome PRs:
1. Fork & branch from `main`
2. Enable `TC_OFFLINE=1` for deterministic tests
3. Add or extend tests for new logic
4. Open a PR (CODEOWNERS will auto‑request maintainers)

See: [`development/contributing.md`](https://github.com/ThreatCompute/ThreatCompute/blob/main/docs/development/contributing.md)

## Governance & Maintainers
Maintainer list is kept in the main repo `COPYRIGHT` file (multi‑maintainer MIT attribution). Decisions are consensus‑driven; larger directional changes should open a design discussion issue first.

## Security
For suspected vulnerabilities:
- Open a private security advisory in the main repo (preferred), or
- Contact maintainers listed in `COPYRIGHT`

Please avoid filing public issues for undisclosed vulnerabilities until coordinated disclosure is arranged.

## Licensing
All core code is released under the MIT License. See the main repo `LICENSE` & `COPYRIGHT` for attribution details.

## Citation
If this project assists academic or industrial research, cite the accompanying paper assets under `paper/` in the main repository (formal citation text forthcoming).

## Community Principles
- Reproducibility over one‑off experimentation
- Transparency in risk heuristics & graph derivations
- Extensibility via clear module seams (model provider, TTC strategies, graph analytics)

---
Questions, ideas, or feedback? Open an issue or start a discussion in the main repository.