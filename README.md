<!--
  GitHub profile README — save this as README.md in a repo named exactly
  after your GitHub username (e.g. github.com/yourusername/yourusername).
  Replace every YOURUSERNAME below.
-->

<h1 align="center">Raza Ali</h1>

<p align="center">
  <b>AI Engineer</b> — I build LLM systems and measure them.<br>
  RAG pipelines, agent orchestration, fine-tuning, and the eval harnesses that prove any of it works.
</p>

<p align="center">
  <a href="https://linkedin.com/in/YOURUSERNAME"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://huggingface.co/razaali1607"><img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face"></a>
  <a href="mailto:you@example.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Lahore,%20PK-open%20to%20remote-2ea44f?style=flat-square" alt="Location">
</p>

---

### About

BS Data Science graduate (2026). I work on the part of AI engineering that isn't the demo: retrieval
quality, evaluation harnesses, cost and latency budgets, and knowing when a feature you built should
ship turned **off**.

Two of the features in the repos below are disabled by default because the numbers said so. Every
benchmark in every README maps to a committed artifact — one project fails its own build if the
write-up quotes a number the data doesn't contain.

```
retrieval quality  ·  eval harness design  ·  agent orchestration
fine-tuning        ·  cost & latency        ·  guardrails
```

---

### Projects

<table>
<tr>
<td width="50%" valign="top">

#### Structured JSON Extraction
**LoRA fine-tune vs. hosted LLM**

A 1.7B open model fine-tuned to extract a strict 16-field schema, benchmarked against the
`gpt-4o-mini` teacher that labelled its training data.

`0.884 macro-F1` vs teacher's `0.925` — at **29% of the cost**.

Also the finding I like most: constrained decoding buys validity, **not** accuracy.

<sub>PyTorch · PEFT/LoRA · Qwen3-1.7B · Batch API</sub>

[Code](https://github.com/YOURUSERNAME/schema-extract-lab) ·
[Model](https://huggingface.co/razaali1607/qwen3-1.7b-jobpost-lora)

</td>
<td width="50%" valign="top">

#### MCP Guardrail Gateway
**Tool-poisoning detection & PII redaction**

A security proxy for the Model Context Protocol. Catches instructions hidden in tool descriptions
(OWASP MCP03:2025) before the model ever sees them.

`17/17 recall` on a frozen test split — and the false-positive cost is published next to it, because
a detection rate without its cost is marketing.

<sub>Python · FastMCP · Presidio · SQLite</sub>

[Code](https://github.com/YOURUSERNAME/mcpgw) ·
[Demo](https://www.loom.com/share/89a4733055464269b578d16b834a3b07)

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### Hybrid-Search RAG Assistant
**Citation-first, with RAGAS evaluation**

Answers university regulations with per-claim section and page citations, and refuses when retrieval
confidence is low.

Every retrieval feature gated on a committed delta report. Reranking lifted `hit@5 0.921 → 0.968`.
Query rewrite regressed, so it ships off.

<sub>FastAPI · LangChain · Pinecone · Redis · React</sub>

[Code](https://github.com/YOURUSERNAME/campus-rag)

</td>
<td width="50%" valign="top">

#### Multi-Agent Research Agent
**Durable human-in-the-loop**

Plans a report, pauses for your approval, researches sections in parallel, grades and revises its own
drafts.

The pause is persisted, not in-memory — kill the process mid-approval and the run resumes to a
finished report. Fixing the grading rubric cut revision loops `39 → 15`.

<sub>LangGraph · FastAPI · PostgreSQL · React 19</sub>

[Code](https://github.com/YOURUSERNAME/atlas)

</td>
</tr>
</table>

<details>
<summary><b>Multi-Agent Startup Evaluation Platform</b> — six agents, five external APIs, deterministic scoring</summary>

<br>

Give it a startup idea, get a scored viability report, market research and an MVP plan. The
interesting constraint: **no LLM touches the scoring path.** Models infer attributes; the 0–100
verdict comes from transparent weighted formulas, so a founder can audit why they got the number
they got. A failing data provider degrades the report's confidence rating instead of failing the
request.

<sub>FastAPI · Next.js 16 · PostgreSQL · ChromaDB · asyncio · Docker</sub>

[Code](https://github.com/YOURUSERNAME/startbot) ·
[Demo](https://www.loom.com/share/3cee6c72811247ff971438fe96effe16)

</details>

---

### Stack

| | |
|---|---|
| **Languages** | Python (async) · TypeScript · SQL · Bash |
| **LLM & agents** | OpenAI API (structured outputs, tool calling, Batch) · LangChain · LangGraph · Model Context Protocol |
| **RAG** | Hybrid search (BM25 + RRF) · cross-encoder reranking · chunking strategies · semantic caching · Pinecone · ChromaDB |
| **Evals & observability** | RAGAS · hit@k / MRR / macro-F1 harnesses · ablation-gated releases · Langfuse · structured logging · cost & latency profiling |
| **Fine-tuning** | PyTorch · Transformers · PEFT/LoRA · Hugging Face · constrained decoding |
| **Backend** | FastAPI · PostgreSQL · SQLAlchemy · Alembic · Redis · SSE streaming · JWT/OAuth2 |
| **Infra** | Docker · GitHub Actions · pytest · Locust · uv |

---

### Currently

Deepening cloud deployment (AWS), and looking for **AI / LLM engineering roles — remote or
relocation**. If you're hiring and want to poke holes in any number above, the artifacts are all
committed. That's the point of them.

<p align="center">
  <sub>
    <a href="https://linkedin.com/in/YOURUSERNAME">LinkedIn</a> ·
    <a href="https://huggingface.co/razaali1607">Hugging Face</a> ·
    <a href="mailto:you@example.com">Email</a>
  </sub>
</p>
