# Edson Oliveira

**HCM Domain Expert · Agentic AI Engineer · NOC 21221 — Business Systems Analyst, IT**
**São Paulo, BR · open to global remote**

---

## About / Sobre

I bring 12+ years of hands-on experience in HCM/ERP systems — eSocial, CLT compliance, payroll integration — and I'm now channeling that domain depth into production-grade agentic AI: building systems that don't just assist but diagnose, decide, and act within guardrails.

Tenho 12+ anos de experiência com sistemas HCM/ERP — eSocial, conformidade CLT, integração de folha — e hoje aplico esse conhecimento de domínio para construir IA agêntica de produção: sistemas que não só assistem, mas diagnosticam, decidem e executam dentro de limites controlados.

My differentiator is the intersection of LGPD/eSocial compliance expertise and full-stack agentic engineering — I understand both what the error code means and how to build the pipeline that resolves it automatically.

Meu diferencial é a interseção entre conformidade LGPD/eSocial e engenharia agêntica full-stack — entendo o que o código de erro significa *e* sei construir o pipeline que o resolve automaticamente.

---

## Featured Project / Projeto Principal

### ⚙️ EII — ERP Incident Intelligence

**EN:** Autonomous diagnostic system for eSocial XML rejections. When the government's webservice rejects an HR/payroll transmission, EII parses the XML, retrieves the most relevant precedents from a curated knowledge base (93 incidents), runs a CRAG pipeline to generate a structured root-cause diagnosis, and queues it for mandatory analyst review before any corrective action is executed.

**PT:** Sistema de diagnóstico autônomo para rejeições de XML do eSocial. Quando o webservice do governo rejeita uma transmissão de RH/folha, o EII interpreta o XML, recupera os precedentes mais relevantes da base de conhecimento (93 incidentes), executa um pipeline CRAG para gerar um diagnóstico estruturado de causa raiz, e encaminha para revisão obrigatória do analista antes de qualquer ação corretiva.

**Stack:** LangGraph · SmartRouter (9 LLM providers) · Qdrant Cloud · CRAG · Gradio · FastAPI · fastmcp · Python 3.13

### Design targets (PRD)

| Metric | Target (PRD) | Status |
|---|---|---|
| eSocial incident MTTR | 70% reduction | 🎯 Target — measurement instrumentation in progress |
| Auto-resolution rate | ≥ 70% of R-* events | 🎯 Target — benchmark on versioned synthetic dataset planned |
| HITL escalation | ≤ 30% | 🎯 Target |
| Test suite | — | ✅ **120 tests green in CI** (3.11 + 3.13) |
| MCP exposure | — | ✅ `eii_query` + `eii_escalate` via fastmcp |

> Targets become results only with real measurements (documented baseline + N).

[![GitHub](https://img.shields.io/badge/GitHub-eii--erp--incident--intelligence-181717?logo=github)](https://github.com/edson-aiops/eii-erp-incident-intelligence)
[![CI](https://github.com/edson-aiops/eii-erp-incident-intelligence/actions/workflows/ci.yml/badge.svg)](https://github.com/edson-aiops/eii-erp-incident-intelligence/actions/workflows/ci.yml)
[![HuggingFace](https://img.shields.io/badge/🤗%20Demo-eii--erp--incident--intelligence-FFD21E)](https://huggingface.co/spaces/EdsonPO/eii-erp-incident-intelligence)

---

## HCM Agentic Stack / Ecossistema Agêntico HCM

**EN:** EII is the first module of a broader vision: an agent ecosystem purpose-built for HCM operations in the Brazilian regulatory context.

**PT:** O EII é o primeiro módulo de uma visão mais ampla: um ecossistema de agentes construído para operações de HCM no contexto regulatório brasileiro.

```
eSocial XML Rejection
        │
   [ eii_query ]  ←── MCP tool (Claude / any MCP client)
        │
   SmartRouter  →  9 LLM providers (Groq · Cerebras · Gemini · Kimi · …)
        │
   CRAG Pipeline  (Deep Agents — 8-node LangGraph)
   ├── Retrieve   → Qdrant Cloud (eSocial + EFD-Reinf KB, 93 incidents)
   ├── Grade      → Classification LLM (relevance filter)
   ├── Generate   → Best available LLM (root-cause diagnosis)
   ├── Evaluate   → 80% consensus threshold
   └── Reflect    → Self-correction loop (ADR-002)
        │
   PENDING queue  ← Human-in-the-Loop gate
        │
   [ eii_escalate ]  ←── APROVADO | REJEITADO
        │
   Audit log (SQLite · LGPD-compliant PII scrubbing)
```

**Domain guardrails / Guardrails de domínio:**
- PII scrubbing at parse time (CNPJ, CPF, NIS — LGPD)
- No corrective action without explicit analyst approval
- Confidence calibration: ALTA / MÉDIA / BAIXA
- Forced HITL escalation when evaluator rejects after max iterations
- ADR-010: pluggable guardrail protocol, LGPD mode = local-only inference

---

## Tech / Tecnologias

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?logo=langchain&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?logo=groq&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?logo=qdrant&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-FF7C00?logo=gradio&logoColor=white)
![FastMCP](https://img.shields.io/badge/fastmcp-MCP-6B48FF?logo=anthropic&logoColor=white)
![HuggingFace](https://img.shields.io/badge/🤗%20HuggingFace-Spaces-FFD21E)

---

## Links

[![GitHub](https://img.shields.io/badge/GitHub-edson--aiops-181717?logo=github)](https://github.com/edson-aiops)
[![HuggingFace](https://img.shields.io/badge/🤗%20HuggingFace-EdsonPO-FFD21E)](https://huggingface.co/EdsonPO)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-edson--oliveira--hcm-0A66C2?logo=linkedin)](https://linkedin.com/in/edson-oliveira-hcm)
