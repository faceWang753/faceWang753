# Mingyang (Ethan) Wang

AI evaluation and software engineer in Toronto. I completed an M.Eng. focused on AI/ML
at McMaster University in 2025, currently evaluate finance-focused LLM outputs, and
previously built banking software and ML/data systems at ICBC.

I care about a specific engineering question: **does an AI system reach the answer for
the right, reproducible reason?**

## What I am building

[![FinMirror - paired-world reliability tests for financial RAG and agents](https://raw.githubusercontent.com/faceWang753/finmirror/main/assets/finmirror-social-card.png)](https://github.com/faceWang753/finmirror)

### [FinMirror](https://github.com/faceWang753/finmirror)

FinMirror changes one fact in a controlled evidence world and checks whether a financial
RAG system or agent updates the complete verifiable output: answer, citations,
calculation operands, confidence, and abstention.

- 126 cases, 108 paired interventions, 18 groups, and 6 finance workflows;
- English, French, and Chinese controlled variants;
- deterministic core evaluator - no LLM judge required;
- 182 tests, 94% coverage, typed Python, JSON Schemas, and CI on Python 3.10-3.12;
- a hash-pinned Statistics Canada GDP calibration group with a reviewed open-licence
  receipt, deterministic source extraction, six disclosed interventions, and a separate
  expert-validation gate that currently fails closed;
- a [drop-in GitHub Actions gate](https://github.com/faceWang753/finmirror/blob/main/docs/GITHUB_ACTION.md)
  that blocks failed paired-world checks and publishes a reviewable reliability summary;
- [zero-key demo](https://facewang753.github.io/finmirror/) and
  [Hugging Face dataset](https://huggingface.co/datasets/mingyang233/FinMirror).

The included evidence-blind control reaches 71.4% case accuracy and 0% strict pair
reliability. That validates a narrow diagnostic protocol on synthetic data; it is not a
claim that FinMirror measures real-world production safety. The first Canadian
real-source lineage is now reproducible and licence-audited; its gold remains
provisional until two independent finance reviewers and a blinded adjudicator complete
the public review gate.

Finance or economics practitioners can review the bounded seven-case packet through the
[public expert-review path](https://github.com/faceWang753/finmirror/blob/main/docs/EXPERT_REVIEW_PACKET.md);
uncertainty and disagreement are recorded rather than hidden.

## Open-source work

- **Merged:** [FinSight-AI PR #14](https://github.com/juanjuandog/FinSight-AI/pull/14)
  adds an ordered evidence-snapshot fingerprint to RAG traces. I revised it after
  maintainer review with null-safe encoding, regression tests, and a documented hash
  boundary.
- **Independent reproduction and review:** on [PydanticAI issue #7041](https://github.com/pydantic/pydantic-ai/issues/7041#issuecomment-5160501465)
  I reproduced a silently dropped Vercel AI approval response and proposed a narrow,
  compatibility-preserving type boundary. A third-party [fix PR #7079](https://github.com/pydantic/pydantic-ai/pull/7079)
  now implements that responded-part boundary; I independently verified its current
  head with 223 passing tests plus clean Ruff and Pyright checks.
- **Awaiting maintainer alignment:** for [PydanticAI #7108](https://github.com/pydantic/pydantic-ai/issues/7108#issuecomment-5181209227)
  I built and tested a trace-privacy fix that removes inline binary payloads across
  instrumentation sinks without changing existing serialization fallbacks; for
  [#7115](https://github.com/pydantic/pydantic-ai/issues/7115#issuecomment-5181276821)
  I added deterministic `aclose()` propagation from UI encoding to the native agent
  stream. Both public branches include regression tests and are waiting for assignment
  before I open upstream PRs.
- **Public fallback implementation:** [EdgarTools issue #922](https://github.com/dgunning/edgartools/issues/922)
  adds fail-closed Schedule 14D-9 recommendation extraction, tested across 340 cases and
  a real SEC cassette replay
  ([public branch](https://github.com/faceWang753/edgartools/tree/feat/schedule-14d9-data-object)).
- **Under review:** [TradingAgents PR #1179](https://github.com/TauricResearch/TradingAgents/pull/1179)
  proposes machine-readable run manifests and honest replay boundaries for agent
  research.
- **Revision pushed:** [Dynamo security PR #1](https://github.com/handshake-project-dynamo/dynamo-2d8b317-security/pull/1)
  fixes a verifier-import hijack identified by automated review. The patch moves the
  verifier to a read-only directory and uses Python isolated mode; a local adversarial
  probe confirmed that an agent-written `pytest.py` no longer executes.

I distinguish merged work, work under review, and fallback branches so every claim is
independently verifiable.

## What I am looking for

I am authorized to work in Canada and open to full-time or remote roles in:

- AI/LLM evaluation and research engineering;
- applied ML and financial AI;
- RAG/agent reliability, data quality, and evaluation infrastructure;
- backend or ML-platform engineering with strong testing and observability.

If you maintain an open-source RAG or agent project, I am also interested in small,
reproducible contributions with a clearly defined integration seam.

## Contact

- [LinkedIn](https://www.linkedin.com/in/mingyang-wang-8867aa2a9)
- [Email](mailto:mingyangwang233@gmail.com)
