# Mingyang (Ethan) Wang

Data and AI engineer in Toronto. I build tools that give AI agents governed access to
data, and tests that show where models and agent tools fail. Before that: three and a half
years of banking software and data pipelines at ICBC, and an M.Eng. in AI/ML at McMaster
(2025). I also evaluate finance-focused LLM responses on contract for Cohere.

## What I am building

### [txn-dq-checks](https://github.com/faceWang753/txn-dq-checks)

A PostgreSQL "trap" database of 641 bank transactions with 26 planted errors, 12 text-to-SQL
tasks, and a grader that runs the model's SQL as a read-only role and compares result sets.
The repo publishes the failing SQL from two models with root causes.

It also holds [north_mcp](https://github.com/faceWang753/txn-dq-checks/tree/main/north_mcp),
an MCP server that maps the calling user to a least-privilege PostgreSQL role and lets
row-level security decide what they see. The same query returns 641 rows for one user and
505 for another, with no SQL parsing in the server.

### [FinMirror](https://github.com/faceWang753/finmirror)

A finance-agent benchmark of 126 cases. It changes one fact in a controlled evidence set and
checks whether the agent's answer, citations and calculation change with it. The checks are
deterministic; no LLM judge is needed. The data is synthetic, so a score says how a system
behaves under this protocol, not how safe it is in production.
[Demo](https://facewang753.github.io/finmirror/) |
[Dataset](https://huggingface.co/datasets/mingyang233/FinMirror)

### [EvalContract](https://github.com/faceWang753/evalcontract)

Turns written release criteria for an AI agent into a CI gate over recorded outputs: a small
JSON contract, no model calls or API keys. [Demo](https://facewang753.github.io/evalcontract/)

## Open-source work

Open, waiting on maintainers:

- **Inspect AI** [PR #4801](https://github.com/UKGovernmentBEIS/inspect_ai/pull/4801):
  `inspect score --from-scan` adds the results of a completed Inspect Scout scan to an eval
  log as scores. It addresses an issue a maintainer accepted.
- **postgres-mcp** [#243](https://github.com/crystaldba/postgres-mcp/issues/243),
  [#244](https://github.com/crystaldba/postgres-mcp/issues/244) and
  [PR #245](https://github.com/crystaldba/postgres-mcp/pull/245): restricted mode has no row
  cap, and failed queries are not flagged as tool errors. The PR fixes the second.
- **Cohere North MCP SDK** [#60](https://github.com/cohere-ai/north-mcp-python-sdk/issues/60):
  the auth example says endpoints require authentication, but the default server accepts
  calls with no identity.

Resolved:

- **PydanticAI** [#7108](https://github.com/pydantic/pydantic-ai/issues/7108): I raised a
  regression concern about a trace-privacy fix. The fix's author found part of it wrong and
  part of it "a real bug we would have shipped", and fixed that part before
  [PR #7131](https://github.com/pydantic/pydantic-ai/pull/7131) merged.

Reproductions and review:

- **PydanticAI** [#7041](https://github.com/pydantic/pydantic-ai/issues/7041): reproduced a
  silently dropped approval response and checked the third-party fix in
  [PR #7079](https://github.com/pydantic/pydantic-ai/pull/7079), which is still open.

I use AI coding tools and say so in each pull request.

## What I am looking for

Forward-deployed, solutions and applied AI engineering roles: work where I take a model or
an agent into a customer's data and make it reliable there. I am authorized to work in
Canada.

## Contact

[LinkedIn](https://www.linkedin.com/in/ethan-wang-8867aa2a9/) | [Email](mailto:mingyangwang233@gmail.com)
