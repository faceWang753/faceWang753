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
- 115 tests, 93% coverage, typed Python, JSON Schemas, and CI on Python 3.10-3.12;
- [zero-key demo](https://facewang753.github.io/finmirror/) and
  [Hugging Face dataset](https://huggingface.co/datasets/mingyang233/FinMirror).

The included evidence-blind control reaches 71.4% case accuracy and 0% strict pair
reliability. That validates a narrow diagnostic protocol on synthetic data; it is not a
claim that FinMirror measures real-world production safety. The next milestone is a
licence-audited, expert-reviewed Canadian real-source pilot.

## Open-source work

- [FinSight-AI PR #14](https://github.com/juanjuandog/FinSight-AI/pull/14) - adds an
  ordered evidence-snapshot fingerprint to RAG traces; updated after maintainer review
  with null-safe encoding, regression tests, and a documented hash boundary.
- [TradingAgents PR #1179](https://github.com/TauricResearch/TradingAgents/pull/1179) -
  proposes exact public-data run receipts for reproducible agent research.

Both are submitted upstream contributions. I list them as work under review, not merged
features or endorsements.

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
