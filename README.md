# Wisely

Systems software engineer (25 years) now building **AI agent infrastructure** — and keeping the
evidence public: every repository below ships tests that run offline and CI that gates on them.

> 25 年系統軟體經驗，現專注 AI agent 基礎建設（agent 付款、文件檢索、模型輸出驗證）；以下專案皆附離線測試與 CI 閘門。

## Public work

| Project | What it is | Evidence |
| --- | --- | --- |
| **[x402-agent-payments](https://github.com/Wisely0710/x402-agent-payments)** | x402 v2 payment stack for EVM: a server-side verifier, a browser client, and an MCP bridge that lets an agent pay for a resource | 54 tests, chain-free 30-second demo |
| **[docs-rag](https://github.com/Wisely0710/docs-rag)** | Retrieval over a repository's *current* documentation, served to coding agents over MCP: declared corpus scope, incremental SQLite index, vector + FTS5 fusion | 16 tests, lint / type / shellcheck gates |
| **[grounding-guard](https://github.com/Wisely0710/grounding-guard)** | Deterministic grounding checks for LLM output — numbers and identifiers the model produced that are not in the facts you supplied get flagged | pure Python, zero dependencies, 17 tests |
| **[llm-toolbox](https://github.com/Wisely0710/llm-toolbox)** | Five runnable LLM patterns: structured output, tool calling, streaming, context budgeting, and a hand-rolled agent loop | 10 tests, no network, no API key |

## What I care about

- **Payments for machines.** An agent with a wallet but no account: x402, EIP-712 / EIP-3009, and
  verification kept separate from settlement.
- **Retrieval you can measure.** Declared corpus scope, deterministic ranking, query metering —
  RAG without a vector database and without hand-waving.
- **Output that is checked, not trusted.** Prompt instructions reduce hallucinated values; a
  deterministic post-check is what removes them.
- **Gates over intentions.** Lint, types, tests, secret scanning and an end-to-end demo, enforced
  in CI rather than promised in a README.

<sub>Every number above is reproducible from the repository it belongs to.</sub>
