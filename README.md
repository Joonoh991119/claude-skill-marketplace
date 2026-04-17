# Joonoh's Claude Code Skill Marketplace

A curated Claude Code plugin marketplace with **162 skills** across 11 categories — add it once, install skills on demand.

## Add this marketplace

```
/plugin marketplace add Joonoh991119/claude-skill-marketplace
```

Then install any skill:

```
/plugin install <skill-name>@joonoh-skill-marketplace
```

## Categories

| Category | Count | What's included |
|---|---|---|
| `agent-tools` | 27 | harness, loop, schedule, mcp-developer, rag-architect, anthropic-skills-* |
| `ai-ml` | 18 | claude-api, transformers, pytorch-lightning, stable-baselines3, modal, shap |
| `data-science` | 14 | pandas, polars, dask, statsmodels, pymc, spark, timesfm, aeon |
| `visualization` | 7 | matplotlib, seaborn, plotly, scientific-visualization, infographics |
| `comp-neuroscience` | 18 | neuropixels-analysis, neurokit2, scanpy, scvi-tools, matlab, boec-simulator |
| `backend` | 17 | python, go, rust, cpp, fastapi, django, postgres, microservices |
| `app-development` | 15 | nextjs, react, flutter, swift, fullstack-mode, offer-k-dense-web |
| `automation` | 11 | devops, kubernetes, terraform, firecrawl, chaos-engineer, lab-chore, csnl-lab-knowledge-system |
| `literature-research` | 18 | arxiv, pubmed, biorxiv, openalex, literature-review, paper-processor, pyzotero |
| `documents-presentation` | 16 | pdf, xlsx, docx, pptx, latex-posters, scientific-slides, venue-templates |
| `research-tools` | 1 | ai-science-reading-tutor (14 skills: corpus-manager, rag-pipeline, equation-parser…) |

## Custom CSNL plugins

These plugins are sourced directly from CSNL lab repositories:

| Plugin | Source | Description |
|---|---|---|
| `ai-science-reading-tutor` | [Joonoh991119/ai-science-reading-tutor](https://github.com/Joonoh991119/ai-science-reading-tutor) | 14 skills: corpus-manager, rag-pipeline (hybrid dense+BM25), paper-processor, equation-parser, ontology-rag, sci-viz, eval-runner, workflow-orchestrator |
| `boec-simulator` | [Joonoh991119/boec_simulator](https://github.com/Joonoh991119/boec_simulator) | BOEC neural circuit simulator agents: math-reviewer, numerical-auditor, livescript-builder, qa-validator |
| `lab-chore` | [Joonoh991119/lab_chore](https://github.com/Joonoh991119/lab_chore) | NRF 중견연구 연차보고서 예산 편성 5-시트 스프레드시트 자동 생성 |
| `csnl-lab-knowledge-system` | [CSNL-vnilab/lab-knowledge-system](https://github.com/CSNL-vnilab/lab-knowledge-system) | CSNL 회의록 작성 — Slack, Zotero, Google Calendar, Notion 통합 |

## Example usage

```
# Agent team setup
/plugin install harness@joonoh-skill-marketplace
/plugin install claude-api@joonoh-skill-marketplace
/plugin install mcp-developer@joonoh-skill-marketplace

# Computational neuroscience
/plugin install neuropixels-analysis@joonoh-skill-marketplace
/plugin install boec-simulator@joonoh-skill-marketplace
/plugin install neurokit2@joonoh-skill-marketplace

# Research workflow
/plugin install ai-science-reading-tutor@joonoh-skill-marketplace
/plugin install literature-review@joonoh-skill-marketplace
/plugin install scientific-writing@joonoh-skill-marketplace
/plugin install pptx@joonoh-skill-marketplace

# Lab management
/plugin install lab-chore@joonoh-skill-marketplace
/plugin install csnl-lab-knowledge-system@joonoh-skill-marketplace
```

## Update

```
/plugin marketplace update joonoh-skill-marketplace
```
