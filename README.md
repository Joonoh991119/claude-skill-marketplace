# Joonoh's Claude Code Skill Marketplace — CSNL-on-AI Edition

**v2.0.0** · A focused marketplace curated for the **CSNL AI Knowledge System** project at Seoul National University BCS / 이상훈 인지시스템신경과학연구실 (Cognitive Systems Neuroscience Lab).

> Previous v1.0 was a 162-skill general-purpose catalog. v2.0 cuts to **118 lab-essential skills** organized for actual CSNL workflows: paper-scout RAG, csnl-ops operational DB, Bayesian observer modeling, multi-LLM orchestration via OpenRouter + Ollama, lab automation, and scientific writing.

## Add this marketplace

```
/plugin marketplace add Joonoh991119/claude-skill-marketplace
```

Install any skill:

```
/plugin install <skill-name>@joonoh-skill-marketplace
```

## What "CSNL-on-AI" means

The CSNL AI Knowledge System integrates **lab operations** (calendars, NAS, slides), **paper-scout** (5-phase RAG-driven recommendation), **paper-blitz** (paper → academic PPT generation), and the **_lab_ai_harness** Slack-DM interview loop on shared infrastructure (Supabase + Vercel + GH Actions cron + Ollama local LLMs). This marketplace is the toolbelt for working inside that system.

**Active CSNL repos** (operational context, not skill plugins):
- [CSNL-vnilab/Exp_Platform_by_Joonoh](https://github.com/CSNL-vnilab/Exp_Platform_by_Joonoh) — 연구실 공용 실험 스케쥴링 플랫폼 (Next.js 16 + Supabase)
- `csnl-ops` (private/local) — CSNL operational DB on `csnl_ops` Supabase schema, GH Actions cron, NAS slide reconciliation
- `_lab_ai_harness` — Slack-DM interview cycle (Python, JOP-owned)

## Categories (curated for CSNL workflows)

| Category | Count | Anchored to |
|---|---:|---|
| `agent-core` | 17 | Multi-session orchestration, harness, /cf boot, verification gates |
| `lab-ai-orchestration` | 14 | Ollama routing, RAG, MCP servers (zotero-mcp, slack-mcp, notion-mcp) |
| `literature-research` | 16 | arXiv/bioRxiv/PubMed/OpenAlex, Zotero, citation, peer review |
| `scientific-docs` | 18 | PPTX/PDF/DOCX/XLSX, posters, LaTeX, schematics, markitdown |
| `comp-cognitive-neuroscience` | 9 | MATLAB Psychtoolbox, Bayesian observer (Time2Dist), PyMC, NeuroKit2 |
| `data-stats-bayes` | 10 | Pandas, statsmodels, networkx (PI-network), aeon, scikit-learn |
| `visualization` | 6 | Matplotlib, Plotly, drawio, Nano-Banana infographics |
| `lab-infra-web` | 15 | Next.js 16 + React + TypeScript + Supabase + Playwright + WCAG-AA design |
| `lab-automation` | 6 | GH Actions cron, Firecrawl, monitoring, API design |
| `ml-deep-learning` | 3 | PyTorch Lightning, GPU optimization, Modal cloud |
| `csnl-custom` | 4 | CSNL-built skill plugins |

**`csnl-essential` tag** marks the 28 skills used daily across CSNL projects.

## Custom CSNL plugins

| Plugin | Source | Purpose |
|---|---|---|
| `ai-science-reading-tutor` | [Joonoh991119/ai-science-reading-tutor](https://github.com/Joonoh991119/ai-science-reading-tutor) | 14 skills: corpus-manager, rag-pipeline (hybrid dense+BM25), paper-processor, equation-parser, ontology-rag, sci-viz, eval-runner, workflow-orchestrator, tutor-content-gen — csnl-ai-knowledge-system Phase 2–4 prototype |
| `boec-simulator` | [Joonoh991119/boec_simulator](https://github.com/Joonoh991119/boec_simulator) | BOEC MATLAB simulator agent team: math-reviewer, numerical-auditor, livescript-builder, qa-validator |
| `lab-chore` | [Joonoh991119/lab_chore](https://github.com/Joonoh991119/lab_chore) | NRF 중견연구 연차보고서 예산 편성 5-sheet spreadsheet automation |
| `csnl-lab-knowledge-system` | [CSNL-vnilab/lab-knowledge-system](https://github.com/CSNL-vnilab/lab-knowledge-system) | `csnl-meeting-notes` skill — AI Knowledge Orchestrator integrating Slack, Zotero, Google Calendar, Notion |

## Meta-review: what was removed from v1.0 and why

v2.0 removed **44 skills** from v1.0. Removal rubric:

**Out of scope: not cognitive systems neuroscience**
- Single-cell genomics (scanpy, scvi-tools, scvelo, anndata, cellxgene-census, pydeseq2, lamindb, geniml, pysam, tiledbvcf, arboreto, deeptools, flowio) — CSNL studies time perception / magnitude estimation in humans, not RNA-seq
- Survival analysis kept (`scikit-survival`) — useful for participant retention modeling

**Out of scope: not in lab's stack**
- Vue, Angular, Flutter, React Native, Swift, Kotlin specialist, Rails, Laravel, Django, NestJS, Spring Boot, ASP.NET, PHP, C#, Go, Rust, C++, Java architect — lab uses Next.js + React + TypeScript + Python only
- Game-developer, embedded-systems, WordPress, Shopify, Salesforce — not relevant
- Atlassian MCP — lab uses Slack + Notion, not Jira

**Out of scope: overkill for lab scale**
- Kubernetes, Terraform, Cloud-architect, SRE-engineer, Chaos-engineer — Vercel Hobby + Supabase + GH Actions is sufficient
- Spark-engineer, dask, vaex — lab data is small (trial-level behavioral)
- ML-pipeline, fine-tuning-expert — lab uses APIs (OpenRouter) and pretrained embeddings, no training pipeline
- Stable-baselines3, pufferlib (RL), torch-geometric — not in research scope

**Replaced with better alternatives**
- `markdown-mermaid-writing` (kept once in `scientific-docs`, removed duplicate from `visualization`)
- `frontend-design` kept; added `design-accessibility-review`, `design-handoff`, `design-ux-copy` (matches `feedback_design` rules)

**Added in v2.0**
- `interview` — multi-turn structured interviews, used by `_lab_ai_harness` for PI campaigns
- `deep-research` — format-controlled evidence-tracked reports (matches `feedback_deep_research_rules`)
- `semantic-scholar` — concurrent multi-keyword + batch DOI lookup for paper-scout
- `drawio` — diagram tool for `csnl-ai-knowledge-system` architecture docs
- `scikit-survival` — participant retention modeling
- `scilingo-pedagogy` — pedagogical evidence base for the Korean-scientist English tutor
- `design-accessibility-review`, `design-handoff`, `design-ux-copy` — pre-ship UX gates
- `code-documenter` — keep csnl-ops endpoints documented

## Example usage by workflow

### Setting up a new CSNL session

```
/plugin install harness@joonoh-skill-marketplace
/plugin install init@joonoh-skill-marketplace
/plugin install productivity-memory-management@joonoh-skill-marketplace
/plugin install local-llm@joonoh-skill-marketplace
```

### Working on paper-scout / paper-blitz / ai-science-reading-tutor

```
/plugin install ai-science-reading-tutor@joonoh-skill-marketplace
/plugin install rag-architect@joonoh-skill-marketplace
/plugin install openalex-database@joonoh-skill-marketplace
/plugin install pyzotero@joonoh-skill-marketplace
/plugin install playwright-expert@joonoh-skill-marketplace
/plugin install interview@joonoh-skill-marketplace
```

### Working on csnl-ops / lab-reservation / Exp_Platform_by_Joonoh

```
/plugin install nextjs-developer@joonoh-skill-marketplace
/plugin install typescript-pro@joonoh-skill-marketplace
/plugin install postgres-pro@joonoh-skill-marketplace
/plugin install design-accessibility-review@joonoh-skill-marketplace
/plugin install devops-engineer@joonoh-skill-marketplace
/plugin install test-master@joonoh-skill-marketplace
```

### Working on Time2Dist / Bayesian observer modeling

```
/plugin install matlab@joonoh-skill-marketplace
/plugin install bayesian-observer-modeling@joonoh-skill-marketplace
/plugin install pymc@joonoh-skill-marketplace
/plugin install statistical-analysis@joonoh-skill-marketplace
/plugin install boec-simulator@joonoh-skill-marketplace
```

### Lab-meeting / GRM / Paper Blitz / Brainday output

```
/plugin install csnl-lab-knowledge-system@joonoh-skill-marketplace
/plugin install pptx@joonoh-skill-marketplace
/plugin install latex-posters@joonoh-skill-marketplace
/plugin install scientific-slides@joonoh-skill-marketplace
/plugin install scientific-schematics@joonoh-skill-marketplace
/plugin install venue-templates@joonoh-skill-marketplace
```

### NRF grant cycle (Q1 annual + 중견 reports)

```
/plugin install lab-chore@joonoh-skill-marketplace
/plugin install research-grants@joonoh-skill-marketplace
/plugin install scientific-writing@joonoh-skill-marketplace
/plugin install xlsx@joonoh-skill-marketplace
```

## Anchored to user memory

This curation honors persistent feedback recorded in `~/.claude/projects/-Users-joonoh/memory/`:

- `feedback_no_anthropic_api` — J's apps (Axon, SciLingo) use OpenRouter + Ollama. `claude-api` kept as reference only, never used as `ANTHROPIC_API_KEY` in production code.
- `feedback_opus_orchestrator` — Opus 4.7 dispatches; harness skill is foundational.
- `feedback_paper_scout` — PI-network crawl > keyword; Playwright > WebFetch; bot token > MCP. Anchors `playwright-expert`, `openalex-database`, `networkx`, `interview`.
- `feedback_slides_master` — PPTX rules anchored to `pptx`, `scientific-slides`, `latex-posters`.
- `feedback_design` — No AI purple; macOS system colors; WCAG-AA; mandatory UX review. Anchors `design-accessibility-review`, `frontend-design`, `design-ux-copy`.
- `feedback_deep_research_rules` — Academic cites; 70/30 exploit/explore; uncertainty qualifier per claim. Anchors `deep-research`, `scientific-critical-thinking`.
- `feedback_unverified_merge_pattern` — Vitest green ≠ runtime verified. Anchors `test-master`, `playwright-expert`, `review`, `code-reviewer`.
- `feedback_axon_orchestration` — Parallel worktree agents. Anchors `harness`, `loop`, `schedule`.
- `reference_bayesian_observer_skill` — Anchors `bayesian-observer-modeling`, `pymc`.
- `project_csnl_paperblitz_harness` — Anchors `interview`, `local-llm` (gemma3:12b audit).

## Update

```
/plugin marketplace update joonoh-skill-marketplace
```

## Versioning

| Version | Plugins | Focus |
|---|---:|---|
| v1.0.0 | 162 | Generic catalog across 11 categories |
| **v2.0.0** | **118** | **CSNL-on-AI focused; v1.0 inventory minus 44 out-of-scope skills + 6 newly-added lab-essential skills** |

---

Curated by Joonoh (JOP, 박준오) · SNU Brain & Cognitive Sciences · Cognitive Systems Neuroscience Lab
