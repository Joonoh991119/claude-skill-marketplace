# Joonoh's Claude Code Skill Marketplace

A curated Claude Code plugin marketplace with **124 skills** across 8 categories — add it once, install skills on demand.

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
| `agent-tools` | 27 | harness, loop, schedule, mcp-developer, claude-api tools, memory management |
| `ai-ml` | 18 | claude-api, transformers, rag-architect, pytorch-lightning, stable-baselines3, modal |
| `data-science` | 14 | pandas, polars, dask, statsmodels, pymc, spark, timesfm |
| `visualization` | 7 | matplotlib, seaborn, plotly, scientific-visualization, infographics |
| `comp-neuroscience` | 17 | neuropixels-analysis, neurokit2, scanpy, scvi-tools, matlab, deeptools |
| `backend` | 17 | python, go, rust, cpp, fastapi, django, postgres, microservices |
| `app-development` | 15 | nextjs, react, flutter, swift, fullstack-mode, offer-k-dense-web |
| `automation` | 9 | devops, kubernetes, terraform, monitoring, firecrawl, chaos-engineer |

## Example usage

```
# Build an agent team
/plugin install harness@joonoh-skill-marketplace
/plugin install claude-api@joonoh-skill-marketplace
/plugin install rag-architect@joonoh-skill-marketplace

# Data science workflow
/plugin install pandas-pro@joonoh-skill-marketplace
/plugin install plotly@joonoh-skill-marketplace
/plugin install pymc@joonoh-skill-marketplace

# Neuroscience analysis
/plugin install neuropixels-analysis@joonoh-skill-marketplace
/plugin install scanpy@joonoh-skill-marketplace
/plugin install neurokit2@joonoh-skill-marketplace
```

## Update

```
/plugin marketplace update joonoh-skill-marketplace
```
