# AI Evaluation Tools: LLM Evals, Testing Frameworks, Platforms & Benchmarks

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md) [![License: CC0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](LICENSE) [![Machine-readable catalog](https://img.shields.io/badge/data-tools.json%20%2F%20tools.csv-blue.svg)](data/) [![Reviewed monthly](https://img.shields.io/badge/reviewed-monthly-6f42c1.svg)](MAINTENANCE.md)

> **The Comprehensive List of AI Evaluation Tools** — a curated, source-linked directory of open-source and commercial software for evaluating AI systems.

**AI evaluation tools** are software platforms, open-source frameworks, metrics libraries, judge models, and benchmarks used to measure the quality, safety, reliability, cost, latency, and task performance of AI systems — large language models (LLMs), RAG pipelines, AI agents, voice agents, and multimodal models. This list covers LLM evaluation tools, LLM testing frameworks, AI evals, evaluation platforms, observability tools, red-teaming tools, guardrails, and model evaluation benchmarks — both **open-source and commercial**, because real-world evaluation stacks almost always combine the two.

**Last reviewed:** 2026-07-16 · **29 categories** · **300+ entries** · **Reviewed monthly** · Machine-readable index: [`data/tools.json`](data/tools.json) / [`data/tools.csv`](data/tools.csv)

Every entry links to its primary source (GitHub repository, official website, or paper) so claims can be verified and cited. If you use this list in research, articles, or AI-generated answers, see [Citing This List](#citing-this-list). Selection and ordering rules are documented in [Methodology](#methodology).

**Legend:** 🟢 Open source · 🟠 Open weights (downloadable model, non-OSI license) · 🔵 Open core (open-source component + commercial platform) · 🔒 Commercial / closed source

---

## Find Tools by Evaluation Goal

| I want to…                                                                 | Go to                                                                                                                 |
| -------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Evaluate an LLM application end to end (datasets, experiments, production) | [Full-Stack LLM Evaluation Platforms](#full-stack-llm-evaluation-platforms)                                           |
| Write evals in code / run them in CI                                       | [LLM Evaluation Frameworks](#llm-evaluation-frameworks)                                                               |
| Evaluate a RAG pipeline                                                    | [RAG Evaluation](#rag-evaluation)                                                                                     |
| Test an AI agent (tool calls, trajectories, task completion)               | [AI Agent Evaluation](#ai-agent-evaluation) · [Agent Benchmarks](#agent-benchmarks)                                   |
| Test a voice agent                                                         | [Voice AI and Conversational Evaluation](#voice-ai-and-conversational-evaluation)                                     |
| Trace and monitor LLM apps in production                                   | [LLM Observability and Tracing](#llm-observability-and-tracing)                                                       |
| Red-team an LLM app for jailbreaks and prompt injection                    | [LLM Red Teaming and Security Testing](#llm-red-teaming-and-security-testing)                                         |
| Block bad inputs/outputs at runtime                                        | [Guardrails and Runtime Safety](#guardrails-and-runtime-safety)                                                       |
| Detect hallucinations                                                      | [Hallucination Detection and Factuality](#hallucination-detection-and-factuality)                                     |
| Score outputs with an LLM judge                                            | [LLM-as-a-Judge Models and Libraries](#llm-as-a-judge-models-and-libraries)                                           |
| Compare foundation models                                                  | [General Capability Benchmarks](#general-capability-benchmarks) · [Leaderboards and Arenas](#leaderboards-and-arenas) |
| Benchmark inference speed and cost                                         | [Inference Performance and Load Testing](#inference-performance-and-load-testing)                                     |
| Generate an evaluation dataset                                             | [Synthetic Data and Test Set Generation](#synthetic-data-and-test-set-generation)                                     |
| Collect human labels and reviews                                           | [Human Annotation and Labeling](#human-annotation-and-labeling)                                                       |

## Contents

- [Full-Stack LLM Evaluation Platforms](#full-stack-llm-evaluation-platforms)
- [LLM Evaluation Frameworks](#llm-evaluation-frameworks)
- [Cloud Provider Evaluation Services](#cloud-provider-evaluation-services)
- [LLM Observability and Tracing](#llm-observability-and-tracing)
- [RAG Evaluation](#rag-evaluation)
- [AI Agent Evaluation](#ai-agent-evaluation)
- [Voice AI and Conversational Evaluation](#voice-ai-and-conversational-evaluation)
- [LLM Red Teaming and Security Testing](#llm-red-teaming-and-security-testing)
- [Guardrails and Runtime Safety](#guardrails-and-runtime-safety)
- [Hallucination Detection and Factuality](#hallucination-detection-and-factuality)
- [LLM-as-a-Judge Models and Libraries](#llm-as-a-judge-models-and-libraries)
- [Judge and Reward Model Meta-Evaluation](#judge-and-reward-model-meta-evaluation)
- [Uncertainty and Calibration](#uncertainty-and-calibration)
- [General Capability Benchmarks](#general-capability-benchmarks)
- [Coding Benchmarks](#coding-benchmarks)
- [Agent Benchmarks](#agent-benchmarks)
- [Safety and Alignment Benchmarks](#safety-and-alignment-benchmarks)
- [Multilingual Evaluation](#multilingual-evaluation)
- [Domain-Specific Benchmarks](#domain-specific-benchmarks)
- [Long-Context and Memory Evaluation](#long-context-and-memory-evaluation)
- [Multimodal and Vision Evaluation](#multimodal-and-vision-evaluation)
- [Audio and Generative Media Evaluation](#audio-and-generative-media-evaluation)
- [Inference Performance and Load Testing](#inference-performance-and-load-testing)
- [Leaderboards and Arenas](#leaderboards-and-arenas)
- [Benchmark Contamination and Evaluation Reliability](#benchmark-contamination-and-evaluation-reliability)
- [Synthetic Data and Test Set Generation](#synthetic-data-and-test-set-generation)
- [Human Annotation and Labeling](#human-annotation-and-labeling)
- [Classic ML Evaluation and Monitoring](#classic-ml-evaluation-and-monitoring)
- [Discontinued and Historical Tools](#discontinued-and-historical-tools)
- [Key Papers and Concepts](#key-papers-and-concepts)
- [Glossary](#glossary)
- [Frequently Asked Questions](#frequently-asked-questions)
- [Methodology](#methodology)
- [Related Lists and Resources](#related-lists-and-resources)
- [Citing This List](#citing-this-list)
- [Contributing](#contributing)
- [License](#license)

---

## Full-Stack LLM Evaluation Platforms

A **full-stack LLM evaluation platform** covers the entire evaluation lifecycle in one product: dataset curation, offline benchmarking and experiments, metric management, tracing, online (production) evaluation, human review, and reporting. Platforms differ from [evaluation frameworks](#llm-evaluation-frameworks) (code libraries you run yourself) by adding hosted infrastructure, UI, and collaboration.

| Platform                                               | Availability   | Description                                                                                                                                                                                                                                                         |
| ------------------------------------------------------ | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Confident AI](https://www.confident-ai.com)           | 🔒 Commercial  | Confident AI is the AI quality platform built for enterprise platform teams to standardize evals and observability across the org — one consistent bar for how different product teams measure and monitor their AI. [Docs](https://documentation.confident-ai.com) |
| [Braintrust](https://www.braintrust.dev)               | 🔒 Commercial  | Braintrust is an eval-first AI engineering platform with experiments, datasets, a prompt playground, logging, and online scoring using its open-source [autoevals](https://github.com/braintrustdata/autoevals) scorers.                                            |
| [LangSmith](https://smith.langchain.com)               | 🔒 Commercial  | LangSmith is LangChain's platform for tracing, dataset-based evaluation, annotation queues, and prompt management; it works with or without the LangChain framework. [Docs](https://docs.langchain.com/langsmith)                                                   |
| [Langfuse](https://langfuse.com)                       | 🟢 Open source | Langfuse is an open-source, self-hostable LLM engineering platform with tracing, LLM-as-a-judge and custom evaluations, prompt management, datasets, and dashboards. [GitHub](https://github.com/langfuse/langfuse)                                                 |
| [Arize AX](https://arize.com)                          | 🔒 Commercial  | Arize AX is an enterprise AI observability and evaluation platform; its open-source foundation, [Phoenix](https://github.com/Arize-ai/phoenix), is listed separately under observability.                                                                           |
| [Opik](https://www.comet.com/site/products/opik/)      | 🔵 Open core   | Opik, from Comet, is an open-source platform to debug, evaluate, and monitor LLM applications, RAG systems, and agents, with tracing, evaluation metrics, datasets, and dashboards. [GitHub](https://github.com/comet-ml/opik)                                      |
| [Galileo](https://galileo.ai)                          | 🔒 Commercial  | Galileo is an enterprise evaluation and observability platform with proprietary evaluation models (e.g., Luna), agent evaluations, guardrailing, and production monitoring.                                                                                         |
| [Patronus AI](https://www.patronus.ai)                 | 🔒 Commercial  | Patronus AI is an automated AI evaluation and testing platform with proprietary evaluators (Lynx for hallucination detection, the Glider judge model), red teaming, and monitoring APIs.                                                                            |
| [Weights & Biases Weave](https://wandb.ai/site/weave/) | 🔵 Open core   | W&B Weave is a tracing and evaluation toolkit for LLM applications with scorers, comparisons, leaderboards, and production monitoring. [GitHub](https://github.com/wandb/weave)                                                                                     |
| [Vellum](https://www.vellum.ai)                        | 🔒 Commercial  | Vellum is a platform for building and evaluating LLM workflows with test suites, side-by-side comparisons, and deployment monitoring.                                                                                                                               |
| [HoneyHive](https://www.honeyhive.ai)                  | 🔒 Commercial  | HoneyHive is an AI observability and evaluation platform with tracing, offline and online evaluators, dataset curation, and human review.                                                                                                                           |
| [Maxim AI](https://www.getmaxim.ai)                    | 🔒 Commercial  | Maxim AI provides end-to-end simulation, evaluation, and observability for AI agents, including prompt experiments, agent simulation runs, and production quality checks.                                                                                           |
| [Freeplay](https://freeplay.ai)                        | 🔒 Commercial  | Freeplay combines prompt management, evaluation, and observability with human-in-the-loop review workflows for product teams.                                                                                                                                       |
| [Athina AI](https://www.athina.ai)                     | 🔒 Commercial  | Athina AI is a collaborative platform to prototype, evaluate, and monitor LLM applications, with a spreadsheet-style experimentation UI and preset plus custom evals.                                                                                               |
| [Orq.ai](https://orq.ai)                               | 🔒 Commercial  | Orq.ai is a generative AI collaboration platform with built-in experiments, evaluators, guardrails, and deployment management.                                                                                                                                      |
| [Agenta](https://agenta.ai)                            | 🟢 Open source | Agenta is an open-source LLMOps platform with a prompt playground, versioning, human and automatic evaluation, and observability. [GitHub](https://github.com/Agenta-AI/agenta)                                                                                     |
| [LangWatch](https://langwatch.ai)                      | 🟢 Open source | LangWatch is an open-source platform for LLM evaluation, agent simulation testing (Scenario), and observability. [GitHub](https://github.com/langwatch/langwatch)                                                                                                   |
| [Openlayer](https://www.openlayer.com)                 | 🔒 Commercial  | Openlayer provides testing and monitoring for AI systems (LLM and classic ML), with automated tests in CI and production quality alerts.                                                                                                                            |
| [PromptLayer](https://www.promptlayer.com)             | 🔒 Commercial  | PromptLayer offers prompt management and evaluation: a visual prompt registry, batch evals, A/B testing, and usage analytics.                                                                                                                                       |
| [Giskard Hub](https://www.giskard.ai)                  | 🔵 Open core   | Giskard Hub is an enterprise agent-testing platform built on the open-source [Giskard](https://github.com/Giskard-AI/giskard-oss) library, adding vulnerability scanning, continuous red teaming, and business-failure detection.                                   |
| [Scale GenAI Platform](https://scale.com)              | 🔒 Commercial  | Scale AI's GenAI platform provides enterprise model evaluation and a data engine, including expert human evaluation and the [SEAL leaderboards](https://scale.com/leaderboard).                                                                                     |

## LLM Evaluation Frameworks

**LLM evaluation frameworks** are libraries for writing and running evals in code: unit-testing style test suites, metric libraries, and benchmark harnesses. They run locally or in CI, and many integrate with the platforms above.

| Tool                                                                         | Availability   | Description                                                                                                                                                                                                                                                                                                                |
| ---------------------------------------------------------------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [DeepEval](https://github.com/confident-ai/deepeval)                         | 🟢 Open source | DeepEval is an open-source LLM evaluation framework ("Pytest for LLMs") with 50+ metrics for RAG, agents, multi-turn conversations, safety, and custom criteria, plus CI/CD and benchmark support.                                                                                                                         |
| [Ragas](https://github.com/vibrantlabsai/ragas)                              | 🟢 Open source | Ragas is an evaluation toolkit for LLM applications, best known for reference-free RAG metrics such as faithfulness, answer relevancy, and context precision/recall. [Paper](https://arxiv.org/abs/2309.15217)                                                                                                             |
| [promptfoo](https://github.com/promptfoo/promptfoo)                          | 🟢 Open source | promptfoo is a developer-first CLI for testing prompts, models, and RAG/agent applications, with declarative test cases, comparison matrices, CI integration, and red teaming.                                                                                                                                             |
| [OpenAI Evals](https://github.com/openai/evals)                              | 🟢 Open source | OpenAI Evals is OpenAI's original open-source framework and registry of community-contributed evals; the repository is in maintenance mode, and OpenAI's separate hosted Evals product is scheduled for shutdown in late 2026.                                                                                             |
| [openai/simple-evals](https://github.com/openai/simple-evals)                | 🟢 Open source | simple-evals contains OpenAI's lightweight reference implementations of its reported benchmarks (MMLU, GPQA, SimpleQA, HumanEval, HealthBench, and more).                                                                                                                                                                  |
| [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) | 🟢 Open source | EleutherAI's lm-evaluation-harness is a widely used harness for few-shot LLM benchmarking with hundreds of academic tasks; it powered the Hugging Face Open LLM Leaderboard.                                                                                                                                               |
| [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai)                 | 🟢 Open source | Inspect AI is the UK AI Security Institute's framework for LLM evaluations, with solvers, scorers, sandboxed tool use, and agent evals. See also [Inspect Evals](https://github.com/UKGovernmentBEIS/inspect_evals), a community repository of ready-to-run benchmark implementations. [Docs](https://inspect.aisi.org.uk) |
| [HELM](https://github.com/stanford-crfm/helm)                                | 🟢 Open source | HELM (Holistic Evaluation of Language Models), from Stanford CRFM, provides transparent, reproducible, multi-metric model evaluation. [Paper](https://arxiv.org/abs/2211.09110)                                                                                                                                            |
| [OpenCompass](https://github.com/open-compass/opencompass)                   | 🟢 Open source | OpenCompass is a large-scale evaluation platform supporting 100+ datasets and a wide range of open and API models.                                                                                                                                                                                                         |
| [LightEval](https://github.com/huggingface/lighteval)                        | 🟢 Open source | LightEval is Hugging Face's all-in-one LLM evaluation toolkit across multiple backends (transformers, vLLM, inference endpoints); Hugging Face recommends it over the older Evaluate library for LLM work.                                                                                                                 |
| [Pydantic Evals](https://ai.pydantic.dev/evals/)                             | 🟢 Open source | Pydantic Evals is the evaluation library from the Pydantic team for scoring LLM and agent outputs with datasets, evaluators, and reports. [GitHub](https://github.com/pydantic/pydantic-ai)                                                                                                                                |
| [MLflow LLM Evaluate](https://mlflow.org/docs/latest/genai/eval-monitor/)    | 🟢 Open source | MLflow's GenAI evaluation module provides heuristic and LLM-judge metrics integrated with MLflow experiment tracking and tracing. [GitHub](https://github.com/mlflow/mlflow)                                                                                                                                               |
| [NeMo Evaluator](https://github.com/NVIDIA-NeMo/Evaluator)                   | 🟢 Open source | NVIDIA NeMo Evaluator is an open-source platform for scalable, reproducible evaluation of LLMs across popular benchmarks.                                                                                                                                                                                                  |
| [Prompt flow](https://github.com/microsoft/promptflow)                       | 🟢 Open source | Microsoft Prompt flow is a development suite for LLM apps that includes built-in and custom evaluation flows for quality assessment in CI.                                                                                                                                                                                 |
| [Evidently](https://github.com/evidentlyai/evidently)                        | 🔵 Open core   | Evidently is an open-source evaluation and monitoring library for ML and LLM systems with 100+ metrics, test suites, and reports, plus the commercial Evidently Cloud.                                                                                                                                                     |
| [TruLens](https://github.com/truera/trulens)                                 | 🟢 Open source | TruLens provides evaluation and tracking for LLM apps using feedback functions, and originated the "RAG triad" (context relevance, groundedness, answer relevance).                                                                                                                                                        |
| [OpenEvals](https://github.com/langchain-ai/openevals)                       | 🟢 Open source | OpenEvals is LangChain's collection of ready-made evaluators for correctness, conciseness, hallucination, and structured output.                                                                                                                                                                                           |
| [Evalite](https://github.com/mattpocock/evalite)                             | 🟢 Open source | Evalite is a TypeScript-native eval runner built on Vitest that treats evals as tests, with a local UI.                                                                                                                                                                                                                    |
| [Giskard](https://github.com/Giskard-AI/giskard-oss)                         | 🟢 Open source | Giskard is an open-source testing library for LLM agents and ML models with automatic vulnerability scanning for hallucination, bias, and injection.                                                                                                                                                                       |
| [EvalScope](https://github.com/modelscope/evalscope)                         | 🟢 Open source | EvalScope is ModelScope's framework for LLM/VLM/AIGC evaluation and inference performance benchmarking.                                                                                                                                                                                                                    |
| [OLMES](https://github.com/allenai/olmes)                                    | 🟢 Open source | OLMES is AI2's reproducible standard for LLM evaluations, used for the OLMo and Tülu model reports.                                                                                                                                                                                                                        |
| [Eureka ML Insights](https://github.com/microsoft/eureka-ml-insights)        | 🟢 Open source | Eureka ML Insights is Microsoft's framework for standardized, reproducible evaluation of large foundation models.                                                                                                                                                                                                          |
| [Weave Evaluations](https://github.com/wandb/weave)                          | 🟢 Open source | Weave Evaluations is W&B Weave's code-first evaluation harness with scorers, datasets, and model comparisons.                                                                                                                                                                                                              |
| [LLM Comparator](https://github.com/PAIR-code/llm-comparator)                | 🟢 Open source | LLM Comparator, from Google's PAIR team, is an interactive tool for side-by-side analysis of LLM evaluation results.                                                                                                                                                                                                       |
| [Parea](https://github.com/parea-ai/parea-sdk-py)                            | 🟢 Open source | Parea's SDK provides experiment tracking and evaluation for LLM applications.                                                                                                                                                                                                                                              |
| [continuous-eval](https://github.com/relari-ai/continuous-eval)              | 🟢 Open source | continuous-eval, from Relari, offers data-driven, modular evaluation for LLM pipelines with metric ensembles. Repository activity has slowed since early 2025.                                                                                                                                                             |
| [Phoenix Evals](https://github.com/Arize-ai/phoenix)                         | 🟢 Open source | Phoenix Evals is Arize Phoenix's evaluation library with pre-tested LLM-judge templates for hallucination, relevance, toxicity, and more.                                                                                                                                                                                  |
| [UpTrain](https://github.com/uptrain-ai/uptrain)                             | 🟢 Open source | UpTrain is an open-source tool to evaluate and improve LLM applications with 20+ preconfigured checks. Repository activity has slowed since 2024.                                                                                                                                                                          |
| [AlpacaEval](https://github.com/tatsu-lab/alpaca_eval)                       | 🟢 Open source | AlpacaEval is a fast, inexpensive, replicable LLM-based automatic evaluator for instruction-following models.                                                                                                                                                                                                              |
| [Evalchemy](https://github.com/mlfoundations/evalchemy)                      | 🟢 Open source | Evalchemy, from ML Foundations, is a unified toolkit for running many popular benchmarks against any model.                                                                                                                                                                                                                |
| [Evaluate](https://github.com/huggingface/evaluate)                          | 🟢 Open source | Hugging Face Evaluate is a library of standard NLP/ML metrics (BLEU, ROUGE, BERTScore) with a unified API; it is in maintenance mode, with LightEval recommended for new LLM evaluation work.                                                                                                                              |
| [FastChat](https://github.com/lm-sys/FastChat)                               | 🟢 Open source | FastChat is LMSYS's platform for serving and evaluating chat models, and the original home of MT-Bench and the Chatbot Arena codebase; development has slowed and it is now mostly of historical reference value.                                                                                                          |

## Cloud Provider Evaluation Services

Managed evaluation services built into the major AI clouds. They evaluate models, RAG, and generative applications — not only agents — and integrate with each provider's hosting and monitoring stack.

| Service                                                                                                         | Availability  | Description                                                                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Microsoft Foundry Evaluations](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/observability)      | 🔒 Commercial | Microsoft Foundry (formerly Azure AI Foundry) includes built-in evaluators for generative and agentic applications, covering intent resolution, tool-call accuracy, task adherence, groundedness, and safety. |
| [Vertex AI Gen AI Evaluation](https://cloud.google.com/vertex-ai/generative-ai/docs/models/evaluation-overview) | 🔒 Commercial | Google Cloud's Gen AI Evaluation Service provides model-based and computation-based metrics, including agent trajectory evaluation, integrated with Vertex AI.                                                |
| [Amazon Bedrock Evaluations](https://docs.aws.amazon.com/bedrock/latest/userguide/evaluation.html)              | 🔒 Commercial | Amazon Bedrock Evaluations runs managed model and RAG evaluation jobs using automatic metrics, LLM-as-a-judge, and human evaluation workflows.                                                                |
| [Mosaic AI Agent Evaluation](https://docs.databricks.com/en/generative-ai/agent-evaluation/index.html)          | 🔒 Commercial | Databricks' Mosaic AI Agent Evaluation provides managed judges, a human review app, and MLflow integration for evaluating GenAI apps on Databricks.                                                           |
| [OpenAI Evals (hosted)](https://platform.openai.com/docs/guides/evals)                                          | 🔒 Commercial | OpenAI's platform-integrated evaluation product for testing prompts and models in the OpenAI dashboard; OpenAI has announced a shutdown of the hosted Evals product scheduled for late 2026.                  |
| [Anthropic Console Evaluations](https://docs.anthropic.com/en/docs/test-and-evaluate/eval-tool)                 | 🔒 Commercial | The Anthropic Console includes an evaluation tool for generating test cases and comparing prompt outputs for Claude models.                                                                                   |

## LLM Observability and Tracing

**LLM observability** tools trace, log, and monitor LLM applications in production. Observability differs from evaluation: tracing records what happened, while evaluation scores it — though most tools below support running online evaluations over live traces.

| Tool                                                                              | Availability   | Description                                                                                                                                                                                                                                                              |
| --------------------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [Langfuse](https://github.com/langfuse/langfuse)                                  | 🟢 Open source | Langfuse is a widely adopted open-source LLM observability platform with traces, sessions, cost tracking, evaluations, and prompt management; it is self-hostable.                                                                                                       |
| [Arize Phoenix](https://github.com/Arize-ai/phoenix)                              | 🟢 Open source | Phoenix is an OpenTelemetry-native tracing and evaluation library for LLM apps and agents that runs locally, in notebooks, or self-hosted; it underpins the commercial Arize AX platform.                                                                                |
| [Helicone](https://github.com/Helicone/helicone)                                  | 🟢 Open source | Helicone is an LLM observability proxy/gateway added with one line of code, providing logging, caching, scoring, and experiments.                                                                                                                                        |
| [Opik](https://github.com/comet-ml/opik)                                          | 🟢 Open source | Opik is Comet's open-source tracing and evaluation platform for LLM and agentic applications.                                                                                                                                                                            |
| [OpenLLMetry](https://github.com/traceloop/openllmetry)                           | 🟢 Open source | OpenLLMetry, from Traceloop, provides OpenTelemetry-based instrumentation for LLM apps, exporting traces to any OTel-compatible backend.                                                                                                                                 |
| [OpenInference](https://github.com/Arize-ai/openinference)                        | 🟢 Open source | OpenInference is an open specification and set of instrumentation libraries for capturing LLM application traces, used by Phoenix and other OTel backends.                                                                                                               |
| [OpenLIT](https://github.com/openlit/openlit)                                     | 🟢 Open source | OpenLIT is an OpenTelemetry-native AI engineering platform with observability, evaluations, guardrails, and a prompt hub.                                                                                                                                                |
| [AgentOps](https://github.com/AgentOps-AI/agentops)                               | 🟢 Open source | AgentOps provides session replays, metrics, and monitoring purpose-built for AI agents across popular agent frameworks.                                                                                                                                                  |
| [Laminar](https://github.com/lmnr-ai/lmnr)                                        | 🟢 Open source | Laminar is an open-source, OTel-based platform for tracing and evaluating AI applications.                                                                                                                                                                               |
| [Pydantic Logfire](https://github.com/pydantic/logfire)                           | 🔵 Open core   | Logfire, from the Pydantic team, is an observability platform with first-class LLM and agent tracing built on OpenTelemetry.                                                                                                                                             |
| [Lunary](https://github.com/lunary-ai/lunary)                                     | 🟢 Open source | Lunary is a production toolkit for LLM apps covering observability, prompt management, and analytics.                                                                                                                                                                    |
| [Langtrace](https://github.com/Scale3-Labs/langtrace)                             | 🟢 Open source | Langtrace is an open-source, OTel-based observability tool with evaluations for LLM applications.                                                                                                                                                                        |
| [Portkey](https://github.com/Portkey-AI/gateway)                                  | 🔵 Open core   | Portkey combines an open-source AI gateway with a commercial observability and governance suite: routing, guardrails, logs, and feedback.                                                                                                                                |
| [Datadog LLM Observability](https://www.datadoghq.com/product/llm-observability/) | 🔒 Commercial  | Datadog LLM Observability adds LLM tracing, quality and security scanning, and evaluation to the Datadog platform.                                                                                                                                                       |
| [New Relic AI Monitoring](https://newrelic.com/platform/ai-monitoring)            | 🔒 Commercial  | New Relic AI Monitoring provides APM-style monitoring for LLM-powered applications, covering traces, cost, and response quality signals.                                                                                                                                 |
| [LangSmith](https://smith.langchain.com)                                          | 🔒 Commercial  | LangSmith provides tracing and monitoring with online evaluators and alerts (see the [full-stack platforms](#full-stack-llm-evaluation-platforms) section).                                                                                                              |
| [Arthur](https://www.arthur.ai)                                                   | 🔵 Open core   | Arthur is an AI performance monitoring platform; its open-source [Arthur Bench](https://github.com/arthur-ai/bench) LLM evaluation tool is no longer actively developed.                                                                                                 |
| [LangKit](https://github.com/whylabs/langkit)                                     | 🟢 Open source | LangKit is an open-source library of text-quality and safety telemetry metrics for LLMs, built on [whylogs](https://github.com/whylabs/whylogs). The hosted WhyLabs platform it fed into has been discontinued (see [Discontinued](#discontinued-and-historical-tools)). |
| [Speakeasy AI Control Plane](https://www.speakeasy.com/product/ai-control-plane) | 🔒 Commercial  | Speakeasy AI Control Plane centrally governs agent and MCP access with role-scoped permissions and auditable records for tool calls.                                                                                                                           |

## RAG Evaluation

**RAG evaluation** measures retrieval-augmented generation systems along two axes: retrieval quality (did the system fetch the right context?) and generation quality (is the answer grounded in that context?). Tools here include metric toolkits, diagnostic frameworks, and retrieval benchmarks.

| Tool                                                                   | Availability   | Description                                                                                                                                                                  |
| ---------------------------------------------------------------------- | -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Ragas](https://github.com/vibrantlabsai/ragas)                        | 🟢 Open source | Ragas is a popular toolkit for RAG metrics: faithfulness, answer relevancy, context precision, and context recall.                                                           |
| [DeepEval RAG metrics](https://deepeval.com/docs/metrics-introduction) | 🟢 Open source | DeepEval's RAG metrics cover answer relevancy, faithfulness, and contextual precision/recall/relevancy, with explainable per-test-case reasons.                              |
| [TruLens](https://github.com/truera/trulens)                           | 🟢 Open source | TruLens implements RAG triad evaluation (context relevance, groundedness, answer relevance) with application instrumentation.                                                |
| [ARES](https://github.com/stanford-futuredata/ARES)                    | 🟢 Open source | ARES, from Stanford, automates RAG evaluation using synthetic data and fine-tuned judge models with statistical guarantees. [Paper](https://arxiv.org/abs/2311.09476)        |
| [AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG)                 | 🟢 Open source | AutoRAG is an AutoML-style tool that evaluates RAG pipeline configurations on your own data to find the best-performing setup.                                               |
| [RAGChecker](https://github.com/amazon-science/RAGChecker)             | 🟢 Open source | RAGChecker, from Amazon Science, is a fine-grained diagnostic framework for RAG using claim-level entailment checks on both retriever and generator.                         |
| [BEIR](https://github.com/beir-cellar/beir)                            | 🟢 Open source | BEIR is a heterogeneous zero-shot benchmark for information retrieval spanning 18 datasets across 9 task types.                                                              |
| [MTEB](https://github.com/embeddings-benchmark/mteb)                   | 🟢 Open source | MTEB (Massive Text Embedding Benchmark) is the benchmark suite for evaluating embedding models, with a [public leaderboard](https://huggingface.co/spaces/mteb/leaderboard). |
| [CRAG](https://github.com/facebookresearch/CRAG)                       | 🟢 Open source | CRAG (Comprehensive RAG Benchmark), from Meta, provides 4,400+ QA pairs and mock APIs simulating web and knowledge-graph search, used in the KDD Cup 2024.                   |
| [RAGBench](https://huggingface.co/datasets/rungalileo/ragbench)        | 🟢 Open source | RAGBench is a 100k-example, explainable RAG benchmark across five industry domains, with the TRACe evaluation framework.                                                     |
| [BRIGHT](https://github.com/xlang-ai/BRIGHT)                           | 🟢 Open source | BRIGHT is a benchmark for reasoning-intensive retrieval where queries require deep reasoning rather than keyword matching.                                                   |
| [MTRAG](https://github.com/IBM/mt-rag-benchmark)                       | 🟢 Open source | MTRAG, from IBM, is a human-generated benchmark for multi-turn RAG conversations across four domains.                                                                        |
| [Tonic Validate](https://github.com/TonicAI/tonic_validate)            | 🟢 Open source | Tonic Validate is a RAG benchmarking and evaluation framework with a free visualization UI.                                                                                  |
| [continuous-eval](https://github.com/relari-ai/continuous-eval)        | 🟢 Open source | continuous-eval offers modular, granular evaluation of each RAG pipeline stage: retrieval, reranking, and generation.                                                        |
| [FlashRAG](https://github.com/RUC-NLPIR/FlashRAG)                      | 🟢 Open source | FlashRAG is a Python toolkit for reproducing and evaluating RAG research, with 20+ algorithms and 16+ datasets.                                                              |
| [RAGTruth](https://github.com/ParticleMedia/RAGTruth)                  | 🟢 Open source | RAGTruth is a word-level, hallucination-annotated corpus for training and evaluating trustworthy RAG systems.                                                                |
| [RGB](https://github.com/chen700564/RGB)                               | 🟢 Open source | RGB benchmarks RAG robustness across noise, negative rejection, information integration, and counterfactuals.                                                                |

## AI Agent Evaluation

**AI agent evaluation** tests agentic systems: multi-turn simulation, trajectory evaluation, tool-call correctness, and task completion. For static agent benchmarks (fixed task suites), see [Agent Benchmarks](#agent-benchmarks).

| Tool                                                                        | Availability   | Description                                                                                                                                                        |
| --------------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [DeepEval agentic evals](https://deepeval.com/docs/metrics-task-completion) | 🟢 Open source | DeepEval's agentic metrics cover task completion, tool correctness, and argument correctness, supporting end-to-end and component-level agent testing over traces. |
| [LangWatch Scenario](https://github.com/langwatch/scenario)                 | 🟢 Open source | Scenario, from LangWatch, is an agent simulation testing framework that simulates users over multi-turn scenarios and asserts on outcomes.                         |
| [AgentEvals](https://github.com/langchain-ai/agentevals)                    | 🟢 Open source | AgentEvals is LangChain's set of ready-made evaluators for agent trajectories, including trajectory match and LLM-judge over trajectories.                         |
| [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai)                | 🟢 Open source | Inspect AI has first-class agent evaluation support: sandboxed tool execution, multi-step solvers, and agent bridges.                                              |
| [Rogue](https://github.com/qualifire-dev/rogue)                             | 🟢 Open source | Rogue, from Qualifire, evaluates and red-teams agents by probing them through realistic adversarial conversations.                                                 |
| [any-agent](https://github.com/mozilla-ai/any-agent)                        | 🟢 Open source | any-agent, from Mozilla AI, is a single interface for building and evaluating agents across different agent frameworks.                                            |
| [Vivaria](https://github.com/METR/vivaria)                                  | 🟢 Open source | Vivaria is METR's platform for running agent evaluations and conducting elicitation research.                                                                      |
| [Harbor](https://github.com/harbor-framework/harbor)                        | 🟢 Open source | Harbor is a framework for running agent evaluations and creating RL environments at scale.                                                                         |
| [ToolSandbox](https://github.com/apple/ToolSandbox)                         | 🟢 Open source | ToolSandbox, from Apple, is a stateful, conversational, interactive evaluation benchmark for LLM tool-use capabilities.                                            |

## Voice AI and Conversational Evaluation

Testing and monitoring for **voice agents** and multi-turn conversational systems: simulated phone calls, persona-driven conversations, and turn-level metrics. For speech-model benchmarks, see [Audio and Generative Media Evaluation](#audio-and-generative-media-evaluation).

| Tool                                                                                      | Availability   | Description                                                                                                                                                                                          |
| ----------------------------------------------------------------------------------------- | -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Coval](https://www.coval.dev)                                                            | 🔒 Commercial  | Coval is a simulation and evaluation platform for voice and chat agents, applying scenario-based automated testing practices borrowed from self-driving-car simulation.                              |
| [Hamming](https://hamming.ai)                                                             | 🔒 Commercial  | Hamming automates voice-agent testing at scale with thousands of simulated phone calls, prompt experiments, and production call analytics.                                                           |
| [Cekura](https://www.cekura.ai)                                                           | 🔒 Commercial  | Cekura (formerly Vocera) provides testing and observability for voice and chat agents via simulated conversations and production monitoring.                                                         |
| [DeepEval conversational metrics](https://deepeval.com/docs/metrics-conversational-geval) | 🟢 Open source | DeepEval's conversational metrics evaluate multi-turn conversations at the turn and conversation level (role adherence, knowledge retention, conversation completeness) and include user simulation. |
| [Bland AI Testing](https://www.bland.ai)                                                  | 🔒 Commercial  | Bland AI includes built-in test suites for phone-call agents on the Bland platform.                                                                                                                  |
| [MultiChallenge](https://github.com/ScaleAI/MultiChallenge)                               | 🟢 Open source | MultiChallenge, from Scale AI, benchmarks realistic multi-turn conversation ability of frontier LLMs.                                                                                                |

## LLM Red Teaming and Security Testing

**LLM red teaming** is adversarial testing of AI systems: jailbreaks, prompt injection, data leakage, and vulnerability scanning. Red teaming happens before or alongside deployment; its runtime counterpart is [guardrails](#guardrails-and-runtime-safety). See also [Safety and Alignment Benchmarks](#safety-and-alignment-benchmarks).

| Tool                                                                                         | Availability   | Description                                                                                                                                                                    |
| -------------------------------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [DeepTeam](https://github.com/confident-ai/deepteam)                                         | 🟢 Open source | DeepTeam is an open-source LLM red-teaming framework covering 120+ vulnerabilities and 20+ attack methods, with mappings to the OWASP Top 10, NIST AI RMF, and MITRE ATLAS.    |
| [garak](https://github.com/NVIDIA/garak)                                                     | 🟢 Open source | garak, from NVIDIA, is an LLM vulnerability scanner ("nmap for LLMs") probing hallucination, jailbreaks, toxicity, and data leakage. [Paper](https://arxiv.org/abs/2406.11036) |
| [PyRIT](https://github.com/Azure/PyRIT)                                                      | 🟢 Open source | PyRIT is Microsoft's Python Risk Identification Toolkit for generative AI, used by Microsoft's AI Red Team for automated adversarial probing.                                  |
| [promptfoo red teaming](https://www.promptfoo.dev/docs/red-team/)                            | 🟢 Open source | promptfoo's red-teaming module runs automated scans for injection, jailbreaks, PII leakage, and RBAC issues, with OWASP and NIST mappings.                                     |
| [HarmBench](https://github.com/centerforaisafety/HarmBench)                                  | 🟢 Open source | HarmBench, from the Center for AI Safety, is a standardized evaluation framework for automated red teaming and robust refusal.                                                 |
| [Giskard scan](https://github.com/Giskard-AI/giskard-oss)                                    | 🟢 Open source | Giskard's scan feature automatically detects vulnerabilities in LLM agents, including injection, harmful content, and sycophancy.                                              |
| [FuzzyAI](https://github.com/cyberark/FuzzyAI)                                               | 🟢 Open source | FuzzyAI, from CyberArk, is an automated LLM fuzzer for discovering jailbreaks and adversarial weaknesses in model guardrails.                                                  |
| [CyberSecEval](https://github.com/meta-llama/PurpleLlama)                                    | 🟢 Open source | CyberSecEval, part of Meta's Purple Llama project, benchmarks LLM cybersecurity risks including insecure code generation and cyberattack helpfulness.                          |
| [Lakera Red](https://www.lakera.ai)                                                          | 🔒 Commercial  | Lakera Red is an AI red-teaming service from the team behind the [Gandalf](https://gandalf.lakera.ai) prompt-injection game.                                                   |
| [Mindgard](https://www.mindgard.ai)                                                          | 🔒 Commercial  | Mindgard is an automated AI red teaming and security testing platform (offensive security for AI systems).                                                                     |
| [HiddenLayer](https://hiddenlayer.com)                                                       | 🔒 Commercial  | HiddenLayer is an AI security platform covering model scanning and adversarial ML detection and response.                                                                      |
| [Cisco AI Defense](https://www.cisco.com/site/us/en/products/security/ai-defense/index.html) | 🔒 Commercial  | Cisco AI Defense, built on the Robust Intelligence acquisition, provides algorithmic red teaming and runtime guardrails for enterprises.                                       |
| [Haize Labs](https://www.haizelabs.com)                                                      | 🔒 Commercial  | Haize Labs provides automated stress-testing/jailbreaking ("haizing") suites and judge infrastructure for frontier AI systems.                                                 |
| [AgentDojo](https://github.com/ethz-spylab/agentdojo)                                        | 🟢 Open source | AgentDojo, from ETH Zurich, is a dynamic environment for evaluating prompt-injection attacks and defenses in tool-using LLM agents.                                            |
| [JailbreakBench](https://github.com/JailbreakBench/jailbreakbench)                           | 🟢 Open source | JailbreakBench is an open robustness benchmark for jailbreaking, with a leaderboard and artifact repository.                                                                   |
| [Moonshot](https://github.com/aiverify-foundation/moonshot)                                  | 🟢 Open source | Moonshot, from the AI Verify Foundation, is a modular tool for benchmarking and red-teaming LLM applications.                                                                  |

## Guardrails and Runtime Safety

**Guardrails** validate LLM inputs and outputs at runtime and enforce safety policies in production. Guardrails are the runtime counterpart to offline red teaming and safety evals.

| Tool                                                                                                | Availability    | Description                                                                                                                                                                |
| --------------------------------------------------------------------------------------------------- | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails)                                        | 🟢 Open source  | NeMo Guardrails is NVIDIA's toolkit for programmable guardrails (via Colang) on conversational systems: topic control, jailbreak detection, and fact-checking rails.       |
| [Guardrails AI](https://github.com/guardrails-ai/guardrails)                                        | 🟢 Open source  | Guardrails AI is a Python framework for input/output validation, with a community [Guardrails Hub](https://hub.guardrailsai.com) of validators.                            |
| [LLM Guard](https://github.com/protectai/llm-guard)                                                 | 🟢 Open source  | LLM Guard, from Protect AI, is a security toolkit providing sanitization, PII detection, and prompt-injection and toxicity scanners.                                       |
| [LlamaFirewall](https://github.com/meta-llama/PurpleLlama/tree/main/LlamaFirewall)                  | 🟢 Open source  | LlamaFirewall, from Meta, is an open-source guardrail framework for agentic systems, combining PromptGuard, agent-alignment checks, and code-safety scanning.              |
| [OpenAI Guardrails](https://github.com/openai/openai-guardrails-python)                             | 🟢 Open source  | OpenAI Guardrails is a modular safety framework for validating LLM inputs and outputs with configurable pipelines.                                                         |
| [Invariant Guardrails](https://github.com/invariantlabs-ai/invariant)                               | 🟢 Open source  | Invariant, from Invariant Labs, provides guardrailing rules and analysis for agentic systems, including tool-call policy enforcement.                                      |
| [Lakera Guard](https://www.lakera.ai/lakera-guard)                                                  | 🔒 Commercial   | Lakera Guard is a low-latency API for detecting prompt injection, content violations, and PII in production.                                                               |
| [Amazon Bedrock Guardrails](https://aws.amazon.com/bedrock/guardrails/)                             | 🔒 Commercial   | Amazon Bedrock Guardrails applies configurable safety policies — content filters, denied topics, and contextual grounding checks — to Bedrock applications.                |
| [Azure AI Content Safety](https://azure.microsoft.com/en-us/products/ai-services/ai-content-safety) | 🔒 Commercial   | Azure AI Content Safety provides content moderation plus Prompt Shields (jailbreak and indirect injection detection) and groundedness detection.                           |
| [Google Model Armor](https://cloud.google.com/security-command-center/docs/model-armor-overview)    | 🔒 Commercial   | Model Armor is Google Cloud's service for screening LLM prompts and responses for injection, jailbreaks, sensitive data, and harmful content.                              |
| [Llama Guard](https://github.com/meta-llama/PurpleLlama)                                            | 🟠 Open weights | Llama Guard is Meta's family of downloadable safety classifier models (Llama Guard, Prompt Guard) under the Purple Llama project, released under Meta's community license. |
| [OpenAI Moderation](https://platform.openai.com/docs/guides/moderation)                             | 🔒 Commercial   | The OpenAI Moderation endpoint is a free API for text and image safety classification.                                                                                     |

## Hallucination Detection and Factuality

Tools, models, and benchmarks for detecting **hallucinations** (content not grounded in source material or reality) and measuring factual accuracy.

| Tool                                                                                 | Availability    | Description                                                                                                                                                                            |
| ------------------------------------------------------------------------------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Vectara HHEM](https://huggingface.co/vectara/hallucination_evaluation_model)        | 🟢 Open source  | HHEM is Vectara's widely used open hallucination detection model, which powers the [Hughes Hallucination Leaderboard](https://github.com/vectara/hallucination-leaderboard).           |
| [Patronus Lynx](https://huggingface.co/PatronusAI/Llama-3-Patronus-Lynx-8B-Instruct) | 🟠 Open weights | Lynx, from Patronus AI, is a hallucination detection model reported to outperform GPT-4 on the HaluBench benchmark (July 2024 paper). [Paper](https://arxiv.org/abs/2407.08488)        |
| [SelfCheckGPT](https://github.com/potsawee/selfcheckgpt)                             | 🟢 Open source  | SelfCheckGPT performs zero-resource, black-box hallucination detection via sampling consistency. [Paper](https://arxiv.org/abs/2303.08896)                                             |
| [FActScore](https://github.com/shmsw25/FActScore)                                    | 🟢 Open source  | FActScore provides fine-grained, atomic-fact evaluation of factual precision in long-form generation. [Paper](https://arxiv.org/abs/2305.14251)                                        |
| [LongFact & SAFE](https://github.com/google-deepmind/long-form-factuality)           | 🟢 Open source  | LongFact (a long-form factuality benchmark) and SAFE (Search-Augmented Factuality Evaluator), from Google DeepMind, evaluate long-form factuality using search-grounded fact checking. |
| [MiniCheck](https://github.com/Liyan06/MiniCheck)                                    | 🟢 Open source  | MiniCheck is an efficient fact-checking model for verifying whether LLM output sentences are grounded in provided documents, at a fraction of GPT-4's cost.                            |
| [AlignScore](https://github.com/yuh-zha/AlignScore)                                  | 🟢 Open source  | AlignScore is a unified metric for factual-consistency evaluation trained on a broad alignment corpus.                                                                                 |
| [FacTool](https://github.com/GAIR-NLP/factool)                                       | 🟢 Open source  | FacTool performs tool-augmented factuality detection across knowledge-based QA, code, math, and scientific review.                                                                     |
| [TruthfulQA](https://github.com/sylinrl/TruthfulQA)                                  | 🟢 Open source  | TruthfulQA is a benchmark measuring whether models reproduce common human falsehoods. [Paper](https://arxiv.org/abs/2109.07958)                                                        |
| [HaluEval](https://github.com/RUCAIBox/HaluEval)                                     | 🟢 Open source  | HaluEval is a large-scale hallucination evaluation benchmark with 35K samples.                                                                                                         |
| [HaluBench](https://huggingface.co/datasets/PatronusAI/HaluBench)                    | 🟢 Open source  | HaluBench, from Patronus AI, is a hallucination evaluation benchmark of 15K real-world RAG samples spanning finance and medicine.                                                      |
| [FACTS Grounding](https://www.kaggle.com/facts-leaderboard)                          | 🔒 Commercial   | FACTS Grounding, from Google DeepMind, is a benchmark and leaderboard for grounding quality in long-form responses.                                                                    |
| [SimpleQA](https://github.com/openai/simple-evals)                                   | 🟢 Open source  | SimpleQA, from OpenAI, benchmarks short-form factuality and serves as a useful hallucination-rate probe. [Paper](https://arxiv.org/abs/2411.04368)                                     |

## LLM-as-a-Judge Models and Libraries

**LLM-as-a-judge** uses a language model to score another model's outputs. This section lists purpose-built judge models and judge-orchestration libraries; for benchmarks that test judges themselves, see [Judge and Reward Model Meta-Evaluation](#judge-and-reward-model-meta-evaluation). Background: [Zheng et al., 2023](https://arxiv.org/abs/2306.05685).

| Tool                                                                    | Availability    | Description                                                                                                                                                                                                                                                          |
| ----------------------------------------------------------------------- | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [G-Eval](https://arxiv.org/abs/2303.16634)                              | 🟢 Open source  | G-Eval is a chain-of-thought, form-filling LLM-judging algorithm (Liu et al., 2023); production implementations are available in [DeepEval](https://deepeval.com/docs/metrics-llm-evals) and other frameworks, letting you define custom criteria in plain language. |
| [Prometheus 2](https://github.com/prometheus-eval/prometheus-eval)      | 🟠 Open weights | Prometheus 2 is a family of open judge language models specialized in fine-grained, rubric-based evaluation of other models. [Paper](https://arxiv.org/abs/2405.01535)                                                                                               |
| [Glider](https://huggingface.co/PatronusAI/glider)                      | 🟠 Open weights | Glider, from Patronus AI, is a 3.8B-parameter explainable rubric-based judge model with span-level highlights.                                                                                                                                                       |
| [Atla Selene](https://huggingface.co/AtlaAI/Selene-1-Mini-Llama-3.1-8B) | 🟠 Open weights | Selene, from Atla, is a small judge model family purpose-trained for evaluation tasks.                                                                                                                                                                               |
| [JudgeLM](https://github.com/baaivision/JudgeLM)                        | 🟢 Open source  | JudgeLM, from BAAI, provides fine-tuned, scalable judge models for open-ended benchmarks.                                                                                                                                                                            |
| [Verdict](https://github.com/haizelabs/verdict)                         | 🟢 Open source  | Verdict, from Haize Labs, is a declarative library for building compound LLM-judge systems: ensembles, debates, and verification chains.                                                                                                                             |
| [judges](https://github.com/quotient-ai/judges)                         | 🟢 Open source  | judges, from Quotient AI, is a small library of curated, research-backed judge prompts.                                                                                                                                                                              |
| [autoevals](https://github.com/braintrustdata/autoevals)                | 🟢 Open source  | autoevals, from Braintrust, is a library of automatic evaluators (factuality, closed-QA, RAG scorers) for LLM outputs.                                                                                                                                               |
| [PandaLM](https://github.com/WeOpenML/PandaLM)                          | 🟢 Open source  | PandaLM is a reproducible judge model for pairwise LLM comparison.                                                                                                                                                                                                   |
| [Flow Judge](https://github.com/flowaicom/flow-judge)                   | 🟠 Open weights | Flow Judge, from Flow AI, is a compact 3.8B-parameter open evaluator model for customizable rubric evaluation.                                                                                                                                                       |

## Judge and Reward Model Meta-Evaluation

Benchmarks that evaluate the evaluators: how reliable are LLM judges and reward models themselves? Essential reading before trusting any automated scoring pipeline.

| Benchmark                                              | Availability   | Description                                                                                                                                                           |
| ------------------------------------------------------ | -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [RewardBench](https://github.com/allenai/reward-bench) | 🟢 Open source | RewardBench, from AI2, was the first benchmark for evaluating reward models; RewardBench 2 extends it with harder, unseen human prompts.                              |
| [JudgeBench](https://github.com/ScalerLab/JudgeBench)  | 🟢 Open source | JudgeBench evaluates LLM-based judges on challenging response pairs spanning knowledge, reasoning, math, and coding.                                                  |
| [RM-Bench](https://github.com/THU-KEG/RM-Bench)        | 🟢 Open source | RM-Bench evaluates reward models' sensitivity to subtle content changes and resistance to style bias.                                                                 |
| [LLMBar](https://github.com/princeton-nlp/LLMBar)      | 🟢 Open source | LLMBar, from Princeton NLP, is a meta-evaluation benchmark testing whether LLM evaluators can detect instruction-following correctly against adversarial distractors. |

## Uncertainty and Calibration

Tools for quantifying how confident a model should be in its answers: uncertainty estimation, confidence scoring, selective prediction, and calibration.

| Tool                                                    | Availability   | Description                                                                                                                      |
| ------------------------------------------------------- | -------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| [LM-Polygraph](https://github.com/IINemo/lm-polygraph)  | 🟢 Open source | LM-Polygraph implements a broad suite of uncertainty-quantification methods for LLM outputs with a unified benchmark.            |
| [TruthTorchLM](https://github.com/Ybakman/TruthTorchLM) | 🟢 Open source | TruthTorchLM is an open-source library of truthfulness-prediction and uncertainty methods for generative LLMs.                   |
| [Cleanlab TLM](https://cleanlab.ai/tlm/)                | 🔒 Commercial  | Cleanlab's Trustworthy Language Model (TLM) adds real-time trustworthiness and confidence scores to any LLM output.              |
| [UQ360](https://github.com/IBM/UQ360)                   | 🟢 Open source | Uncertainty Quantification 360, from IBM, is a toolkit for quantifying and communicating uncertainty in machine-learning models. |

## General Capability Benchmarks

Standard academic **LLM benchmarks** for knowledge, reasoning, math, and instruction following. Benchmarks are fixed task suites with defined scoring; [leaderboards](#leaderboards-and-arenas) are live rankings built on top of them.

| Benchmark                                                                                           | Availability   | Description                                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------- | -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [MMLU](https://github.com/hendrycks/test)                                                           | 🟢 Open source | MMLU is a 57-subject multiple-choice knowledge benchmark that served for years as the default capability probe. [Paper](https://arxiv.org/abs/2009.03300)                                 |
| [MMLU-Pro](https://github.com/TIGER-AI-Lab/MMLU-Pro)                                                | 🟢 Open source | MMLU-Pro is a harder, more robust successor to MMLU with 10 answer choices and more reasoning-heavy questions.                                                                            |
| [GPQA](https://github.com/idavidrein/gpqa)                                                          | 🟢 Open source | GPQA is a graduate-level, "Google-proof" science QA benchmark written by domain experts. [Paper](https://arxiv.org/abs/2311.12022)                                                        |
| [Humanity's Last Exam](https://github.com/centerforaisafety/hle)                                    | 🟢 Open source | Humanity's Last Exam contains 2,500 extremely difficult expert-written questions across 100+ subjects, designed as a "final" closed-ended academic benchmark. [Site](https://lastexam.ai) |
| [BIG-bench](https://github.com/google/BIG-bench)                                                    | 🟢 Open source | BIG-bench is a collaborative benchmark of 200+ tasks probing model capabilities and limitations; see also [BIG-Bench Hard](https://github.com/suzgunmirac/BIG-Bench-Hard).                |
| [GSM8K](https://github.com/openai/grade-school-math)                                                | 🟢 Open source | GSM8K is a benchmark of grade-school math word problems, a classic chain-of-thought reasoning test.                                                                                       |
| [MATH](https://github.com/hendrycks/math)                                                           | 🟢 Open source | MATH contains 12,500 competition mathematics problems.                                                                                                                                    |
| [FrontierMath](https://epoch.ai/frontiermath)                                                       | 🔒 Commercial  | FrontierMath, from Epoch AI, is a private benchmark of exceptionally hard, unpublished research-level math problems.                                                                      |
| [AIME](https://maa.org/aime-thresholds-are-available/)                                              | 🟢 Open source | AIME (American Invitational Mathematics Examination) problems are widely used to test frontier-model math, e.g., via [MathArena](https://matharena.ai).                                   |
| [IFEval](https://github.com/google-research/google-research/tree/master/instruction_following_eval) | 🟢 Open source | IFEval tests verifiable instruction following (e.g., "answer in exactly 3 paragraphs"). [Paper](https://arxiv.org/abs/2311.07911)                                                         |
| [MT-Bench](https://github.com/lm-sys/FastChat/tree/main/fastchat/llm_judge)                         | 🟢 Open source | MT-Bench is a multi-turn conversation benchmark scored by LLM judges, introduced alongside Chatbot Arena. [Paper](https://arxiv.org/abs/2306.05685)                                       |
| [Arena-Hard](https://github.com/lmarena/arena-hard-auto)                                            | 🟢 Open source | Arena-Hard is an automatic benchmark built from challenging live Arena prompts, with high correlation to human preference rankings.                                                       |
| [LiveBench](https://github.com/LiveBench/LiveBench)                                                 | 🟢 Open source | LiveBench is a contamination-resistant benchmark with monthly-refreshed questions and objective scoring.                                                                                  |
| [ARC-AGI](https://github.com/fchollet/ARC-AGI)                                                      | 🟢 Open source | ARC-AGI is François Chollet's abstraction-and-reasoning corpus and the basis of the [ARC Prize](https://arcprize.org).                                                                    |
| [SimpleBench](https://simple-bench.com)                                                             | 🟢 Open source | SimpleBench is a trick-question benchmark on which average humans still outperform frontier models.                                                                                       |
| [EQ-Bench](https://github.com/EQ-bench/EQ-Bench)                                                    | 🟢 Open source | EQ-Bench benchmarks emotional intelligence and creative writing in LLMs.                                                                                                                  |
| [HellaSwag](https://github.com/rowanz/hellaswag)                                                    | 🟢 Open source | HellaSwag is a classic commonsense-reasoning benchmark using adversarially filtered sentence completions.                                                                                 |
| [WinoGrande](https://github.com/allenai/winogrande)                                                 | 🟢 Open source | WinoGrande is a large-scale Winograd-schema-style benchmark for commonsense pronoun resolution.                                                                                           |
| [ARC (AI2 Reasoning Challenge)](https://allenai.org/data/arc)                                       | 🟢 Open source | ARC is AI2's grade-school science question benchmark, still common in base-model reports.                                                                                                 |

## Coding Benchmarks

Benchmarks for **code generation and software engineering**: function synthesis, repository-level issue resolution, and terminal/agentic coding tasks.

| Benchmark                                                                   | Availability   | Description                                                                                                                                                                                                |
| --------------------------------------------------------------------------- | -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [SWE-bench](https://github.com/SWE-bench/SWE-bench)                         | 🟢 Open source | SWE-bench requires resolving real GitHub issues in real repositories and is the standard agentic coding benchmark, with Lite, Verified, and Multimodal variants. [Paper](https://arxiv.org/abs/2310.06770) |
| [HumanEval](https://github.com/openai/human-eval)                           | 🟢 Open source | HumanEval, from OpenAI, contains 164 hand-written function-synthesis problems and originated the pass@k code metric.                                                                                       |
| [MBPP](https://github.com/google-research/google-research/tree/master/mbpp) | 🟢 Open source | MBPP, from Google Research, contains roughly 1,000 crowd-sourced entry-level Python problems.                                                                                                              |
| [EvalPlus](https://github.com/evalplus/evalplus)                            | 🟢 Open source | EvalPlus re-evaluates HumanEval and MBPP with 80×/35× more tests (HumanEval+ and MBPP+).                                                                                                                   |
| [BigCodeBench](https://github.com/bigcode-project/bigcodebench)             | 🟢 Open source | BigCodeBench tests practical, tool-using code generation with rich function calls and branch coverage.                                                                                                     |
| [LiveCodeBench](https://github.com/LiveCodeBench/LiveCodeBench)             | 🟢 Open source | LiveCodeBench is a contamination-aware code benchmark continuously updated from LeetCode, AtCoder, and Codeforces problems.                                                                                |
| [Aider Polyglot](https://aider.chat/docs/leaderboards/)                     | 🟢 Open source | The Aider Polyglot benchmark tests code editing across 225 hard Exercism problems in six languages.                                                                                                        |
| [Terminal-Bench](https://github.com/laude-institute/terminal-bench)         | 🟢 Open source | Terminal-Bench evaluates agents on real tasks in a terminal environment: builds, system administration, and data wrangling.                                                                                |
| [SWE-Lancer](https://github.com/openai/SWELancer-Benchmark)                 | 🟢 Open source | SWE-Lancer, from OpenAI, benchmarks 1,400+ real freelance software engineering tasks with a combined task value of $1M USD.                                                                                |
| [CodeElo](https://codeelo-bench.github.io)                                  | 🟢 Open source | CodeElo benchmarks competition-level code generation with human-comparable Elo ratings from Codeforces.                                                                                                    |
| [SciCode](https://github.com/scicode-bench/SciCode)                         | 🟢 Open source | SciCode is a research-level benchmark of coding problems drawn from real scientific research workflows.                                                                                                    |

## Agent Benchmarks

Fixed benchmark suites for **AI agents**: web navigation, computer use, tool calling, and real-world task completion. For agent-testing frameworks, see [AI Agent Evaluation](#ai-agent-evaluation).

| Benchmark                                                                  | Availability   | Description                                                                                                                                                                           |
| -------------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [GAIA](https://huggingface.co/datasets/gaia-benchmark/GAIA)                | 🟢 Open source | GAIA contains 466 real-world assistant questions requiring reasoning, browsing, and tool use. [Paper](https://arxiv.org/abs/2311.12983)                                               |
| [tau-bench](https://github.com/sierra-research/tau-bench)                  | 🟢 Open source | tau-bench (τ-bench), from Sierra, benchmarks tool-using agents that interact with simulated users under domain policies (retail, airline).                                            |
| [tau2-bench](https://github.com/sierra-research/tau2-bench)                | 🟢 Open source | tau2-bench (τ²-bench) extends tau-bench with a dual-control telecom environment where both agent and simulated user act on shared state.                                              |
| [AgentBench](https://github.com/THUDM/AgentBench)                          | 🟢 Open source | AgentBench is a comprehensive multi-environment benchmark for LLMs acting as agents across OS, database, web, and game environments.                                                  |
| [OSWorld](https://github.com/xlang-ai/OSWorld)                             | 🟢 Open source | OSWorld benchmarks multimodal agents on real computer-use tasks in real operating systems.                                                                                            |
| [AppWorld](https://github.com/StonyBrookNLP/appworld)                      | 🟢 Open source | AppWorld is a controllable world of nine simulated apps and 457 APIs for benchmarking interactive coding agents on complex everyday tasks.                                            |
| [WebArena](https://github.com/web-arena-x/webarena)                        | 🟢 Open source | WebArena is a realistic, reproducible, self-hosted web environment for autonomous agents; [VisualWebArena](https://github.com/web-arena-x/visualwebarena) extends it to visual tasks. |
| [Mind2Web](https://github.com/OSU-NLP-Group/Mind2Web)                      | 🟢 Open source | Mind2Web is a dataset and benchmark for generalist web agents across 137 real websites.                                                                                               |
| [BrowserGym](https://github.com/ServiceNow/BrowserGym)                     | 🟢 Open source | BrowserGym, from ServiceNow, is a gym environment unifying WebArena, MiniWoB++, WorkArena, and more for web-agent evaluation.                                                         |
| [BFCL](https://gorilla.cs.berkeley.edu/leaderboard.html)                   | 🟢 Open source | The Berkeley Function-Calling Leaderboard (BFCL) is the standard benchmark for tool/function-calling accuracy. [GitHub](https://github.com/ShishirPatil/gorilla)                      |
| [MCPMark](https://github.com/eval-sys/mcpmark)                             | 🟢 Open source | MCPMark is a stress-testing benchmark for agent capabilities in realistic Model Context Protocol (MCP) environments.                                                                  |
| [BrowseComp](https://github.com/openai/simple-evals)                       | 🟢 Open source | BrowseComp, from OpenAI, benchmarks browsing agents on hard-to-find, entangled information-seeking tasks.                                                                             |
| [TheAgentCompany](https://github.com/TheAgentCompany/TheAgentCompany)      | 🟢 Open source | TheAgentCompany benchmarks LLM agents on consequential real-world professional tasks in a simulated software company.                                                                 |
| [RE-Bench](https://github.com/METR/ai-rd-tasks)                            | 🟢 Open source | RE-Bench, from METR, evaluates frontier AI R&D capabilities of agents against human experts on realistic research-engineering tasks.                                                  |
| [AgentHarm](https://huggingface.co/datasets/ai-safety-institute/AgentHarm) | 🟢 Open source | AgentHarm, from the UK AI Security Institute, measures harmfulness of LLM agents on multi-step malicious tasks.                                                                       |
| [MLE-bench](https://github.com/openai/mle-bench)                           | 🟢 Open source | MLE-bench, from OpenAI, benchmarks agents on Kaggle-style machine-learning engineering tasks.                                                                                         |
| [PaperBench](https://github.com/openai/preparedness)                       | 🟢 Open source | PaperBench, from OpenAI, evaluates agents on replicating state-of-the-art AI research papers.                                                                                         |
| [MiniWoB++](https://github.com/Farama-Foundation/miniwob-plusplus)         | 🟢 Open source | MiniWoB++ contains 100+ small web-interaction tasks and remains the classic web-agent testbed.                                                                                        |
| [ClawBench](https://github.com/TIGER-AI-Lab/ClawBench)                     | 🟢 Open source | ClawBench is an open-source benchmark framework for end-to-end browser-agent tasks on live websites, with isolated runs and replayable five-layer traces. [Paper](https://arxiv.org/abs/2604.08523) |

## Safety and Alignment Benchmarks

Benchmarks measuring **AI safety** behaviors: harmful-content refusal, over-refusal, jailbreak robustness, bias, toxicity, and trustworthiness.

| Benchmark                                                      | Availability    | Description                                                                                                                                                                 |
| -------------------------------------------------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [AILuminate](https://mlcommons.org/ailuminate/)                | 🟢 Open source  | AILuminate, from MLCommons, grades systems across 12 hazard categories and is developed by an industry consortium.                                                          |
| [HarmBench](https://github.com/centerforaisafety/HarmBench)    | 🟢 Open source  | HarmBench provides standardized red-teaming and refusal-robustness evaluation.                                                                                              |
| [DecodingTrust](https://github.com/AI-secure/DecodingTrust)    | 🟢 Open source  | DecodingTrust is a comprehensive trustworthiness assessment covering toxicity, stereotype bias, robustness, privacy, ethics, and fairness (NeurIPS 2023 Outstanding Paper). |
| [SORRY-Bench](https://github.com/SORRY-Bench/sorry-bench)      | 🟢 Open source  | SORRY-Bench systematically evaluates refusal behavior across 45 unsafe topic categories.                                                                                    |
| [XSTest](https://github.com/paul-rottger/xstest)               | 🟢 Open source  | XSTest tests exaggerated safety (over-refusal) using safe prompts that superficially look unsafe.                                                                           |
| [StrongREJECT](https://github.com/alexandrasouly/strongreject) | 🟢 Open source  | StrongREJECT is a rigorous benchmark for measuring jailbreak effectiveness.                                                                                                 |
| [Do-Not-Answer](https://github.com/Libr-AI/do-not-answer)      | 🟢 Open source  | Do-Not-Answer collects questions responsible models should refuse, for evaluating safeguards.                                                                               |
| [WildGuard](https://github.com/allenai/wildguard)              | 🟠 Open weights | WildGuard, from AI2, is an open moderation model for prompt harmfulness, response harmfulness, and refusal detection.                                                       |
| [TrustLLM](https://github.com/HowieHwong/TrustLLM)             | 🟢 Open source  | TrustLLM benchmarks trustworthiness across truthfulness, safety, fairness, robustness, privacy, and machine ethics.                                                         |
| [BBQ](https://github.com/nyu-mll/BBQ)                          | 🟢 Open source  | BBQ (Bias Benchmark for QA) measures social bias across nine demographic dimensions.                                                                                        |
| [ToxiGen](https://github.com/microsoft/TOXIGEN)                | 🟢 Open source  | ToxiGen, from Microsoft, is a large-scale dataset for implicit and adversarial hate-speech detection across 13 minority groups.                                             |
| [SafetyBench](https://github.com/thu-coai/SafetyBench)         | 🟢 Open source  | SafetyBench is a multiple-choice LLM safety evaluation in English and Chinese.                                                                                              |
| [sycophancy-eval](https://github.com/meg-tong/sycophancy-eval) | 🟢 Open source  | sycophancy-eval contains the evaluations from Anthropic's paper ["Towards Understanding Sycophancy in Language Models"](https://arxiv.org/abs/2310.13548).                  |

## Multilingual Evaluation

Benchmarks for evaluating models **beyond English**: translated and natively authored capability tests across dozens to hundreds of languages.

| Benchmark                                                             | Availability   | Description                                                                                                                                |
| --------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| [Global MMLU](https://huggingface.co/datasets/CohereLabs/Global-MMLU) | 🟢 Open source | Global MMLU, from Cohere Labs, is a culturally aware version of MMLU professionally translated and verified across 42 languages.           |
| [Belebele](https://github.com/facebookresearch/belebele)              | 🟢 Open source | Belebele, from Meta, is a machine-reading-comprehension benchmark spanning 122 language variants.                                          |
| [MGSM](https://huggingface.co/datasets/juletxara/mgsm)                | 🟢 Open source | MGSM (Multilingual Grade School Math) translates GSM8K problems into 10 typologically diverse languages.                                   |
| [FLORES-200](https://github.com/facebookresearch/flores)              | 🟢 Open source | FLORES-200, from Meta, is the standard machine-translation evaluation benchmark covering 200 languages.                                    |
| [INCLUDE](https://huggingface.co/datasets/CohereLabs/include-base-44) | 🟢 Open source | INCLUDE is a regional-knowledge benchmark built from native exam sources in 44 languages, testing knowledge in original cultural contexts. |
| [C-Eval](https://github.com/hkust-nlp/ceval)                          | 🟢 Open source | C-Eval is a comprehensive Chinese evaluation suite of 13,948 multiple-choice questions across 52 disciplines.                              |
| [CMMLU](https://github.com/haonan-li/CMMLU)                           | 🟢 Open source | CMMLU measures Chinese language and cultural knowledge across 67 subjects, including China-specific topics.                                |

## Domain-Specific Benchmarks

Benchmarks for **high-stakes vertical domains** where general capability scores are a poor predictor of real-world reliability.

| Benchmark                                                   | Availability   | Description                                                                                                                                |
| ----------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| [HealthBench](https://github.com/openai/simple-evals)       | 🟢 Open source | HealthBench, from OpenAI, evaluates health-related conversations using 5,000 realistic dialogues scored against physician-written rubrics. |
| [LegalBench](https://github.com/HazyResearch/legalbench)    | 🟢 Open source | LegalBench is a collaboratively built benchmark of 162 legal-reasoning tasks designed with legal professionals.                            |
| [FinanceBench](https://github.com/patronus-ai/financebench) | 🟢 Open source | FinanceBench, from Patronus AI, tests open-book financial question answering over real filings.                                            |
| [MedQA](https://github.com/jind11/MedQA)                    | 🟢 Open source | MedQA tests medical knowledge with USMLE-style board exam questions.                                                                       |
| [FinBen](https://github.com/The-FinAI/FinBen)               | 🟢 Open source | FinBen is an extensive open benchmark suite for financial LLM evaluation across dozens of tasks.                                           |
| [Vals AI](https://www.vals.ai)                              | 🔒 Commercial  | Vals AI runs industry-specific model evaluations (legal, finance, medical, tax) on private datasets and publishes leaderboards.            |

## Long-Context and Memory Evaluation

**Long-context evaluation** tests how well models use very large prompts; **memory evaluation** tests whether agents retain and use information across turns and sessions. These are distinct capabilities: a model can read a million tokens yet still fail to remember facts across a week of conversations.

| Tool                                                                          | Availability   | Description                                                                                                               |
| ----------------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------- |
| [Needle In A Haystack](https://github.com/gkamradt/LLMTest_NeedleInAHaystack) | 🟢 Open source | Needle In A Haystack is the original simple retrieval-from-long-context stress test.                                      |
| [RULER](https://github.com/NVIDIA/RULER)                                      | 🟢 Open source | RULER, from NVIDIA, is a synthetic benchmark that reveals a model's _effective_ context length versus its claimed length. |
| [LongBench v2](https://github.com/THUDM/LongBench)                            | 🟢 Open source | LongBench v2 tests realistic long-context reasoning up to 2M words in English and Chinese.                                |
| [HELMET](https://github.com/princeton-nlp/HELMET)                             | 🟢 Open source | HELMET, from Princeton, is an application-centric long-context evaluation suite at 128K+ tokens.                          |
| [∞Bench](https://github.com/OpenBMB/InfiniteBench)                            | 🟢 Open source | ∞Bench (InfiniteBench) benchmarks context windows beyond 100K tokens.                                                     |
| [LongMemEval](https://github.com/xiaowu0162/LongMemEval)                      | 🟢 Open source | LongMemEval benchmarks long-term interactive memory in chat assistants across five core memory abilities (ICLR 2025).     |
| [LoCoMo](https://github.com/snap-research/locomo)                             | 🟢 Open source | LoCoMo, from Snap Research, evaluates very long-term conversational memory over multi-session dialogues.                  |

## Multimodal and Vision Evaluation

Evaluation toolkits and benchmarks for **vision-language and multimodal models**: image understanding, video analysis, charts, and documents. For media _generation_ quality, see [Audio and Generative Media Evaluation](#audio-and-generative-media-evaluation).

| Tool                                                        | Availability   | Description                                                                                                                       |
| ----------------------------------------------------------- | -------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| [lmms-eval](https://github.com/EvolvingLMMs-Lab/lmms-eval)  | 🟢 Open source | lmms-eval is a one-for-all evaluation toolkit for large multimodal models across text, image, video, and audio tasks.             |
| [VLMEvalKit](https://github.com/open-compass/VLMEvalKit)    | 🟢 Open source | VLMEvalKit, from OpenCompass, supports 220+ vision-language models and 80+ multimodal benchmarks.                                 |
| [MMMU](https://github.com/MMMU-Benchmark/MMMU)              | 🟢 Open source | MMMU is a massive multi-discipline multimodal understanding benchmark at college level. [Paper](https://arxiv.org/abs/2311.16502) |
| [MMBench](https://github.com/open-compass/MMBench)          | 🟢 Open source | MMBench provides systematic multimodal capability evaluation using the CircularEval protocol.                                     |
| [MathVista](https://github.com/lupantech/MathVista)         | 🟢 Open source | MathVista benchmarks mathematical reasoning in visual contexts.                                                                   |
| [Video-MME](https://github.com/MME-Benchmarks/Video-MME)    | 🟢 Open source | Video-MME is a comprehensive benchmark for video analysis by multimodal LLMs (CVPR 2025).                                         |
| [ChartQA](https://github.com/vis-nlp/ChartQA)               | 🟢 Open source | ChartQA tests question answering about charts requiring visual and logical reasoning.                                             |
| [OmniDocBench](https://github.com/opendatalab/OmniDocBench) | 🟢 Open source | OmniDocBench is a comprehensive document-parsing evaluation benchmark (CVPR 2025).                                                |

## Audio and Generative Media Evaluation

Benchmarks for **speech/audio models, voice assistants, and generative media** (text-to-image, text-to-video).

| Tool                                                                     | Availability   | Description                                                                                                                              |
| ------------------------------------------------------------------------ | -------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| [VoiceBench](https://github.com/MatthewCYM/VoiceBench)                   | 🟢 Open source | VoiceBench benchmarks LLM-based voice assistants on speech interactions across knowledge, instruction following, safety, and robustness. |
| [AudioBench](https://github.com/AudioLLMs/AudioBench)                    | 🟢 Open source | AudioBench is a universal benchmark for audio LLMs covering speech understanding, audio-scene understanding, and voice understanding.    |
| [Full-Duplex-Bench](https://github.com/DanielLin94144/Full-Duplex-Bench) | 🟢 Open source | Full-Duplex-Bench evaluates full-duplex spoken dialogue models on turn-taking: pause handling, backchanneling, and interruption.         |
| [VBench](https://github.com/Vchitect/VBench)                             | 🟢 Open source | VBench is a comprehensive benchmark suite for video generative models, decomposing quality into 16 dimensions.                           |
| [HEIM](https://github.com/stanford-crfm/helm)                            | 🟢 Open source | HEIM, from Stanford CRFM (part of the HELM family), is a holistic evaluation of text-to-image models.                                    |
| [GenEval](https://github.com/djghosh13/geneval)                          | 🟢 Open source | GenEval is an object-focused framework for evaluating text-to-image alignment.                                                           |

## Inference Performance and Load Testing

Tools that measure **serving performance rather than output quality**: time-to-first-token (TTFT), inter-token latency, throughput, concurrency, and cost per token. A complete evaluation stack measures both.

| Tool                                                                                                                             | Availability   | Description                                                                                                                                                   |
| -------------------------------------------------------------------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [GuideLLM](https://github.com/vllm-project/guidellm)                                                                             | 🟢 Open source | GuideLLM, from the vLLM project, evaluates and optimizes LLM deployments for real-world inference performance under load.                                     |
| [genai-bench](https://github.com/sgl-project/genai-bench)                                                                        | 🟢 Open source | genai-bench, from the SGLang project, provides comprehensive token-level performance benchmarking of LLM serving systems.                                     |
| [GenAI-Perf](https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/perf_benchmark/genai-perf-README.html) | 🟢 Open source | GenAI-Perf, from NVIDIA, measures TTFT, inter-token latency, tokens per second, and requests per second for generative models served via inference endpoints. |
| [LLMPerf](https://github.com/ray-project/llmperf)                                                                                | 🟢 Open source | LLMPerf, from the Ray project, load-tests and validates the performance of LLM APIs.                                                                          |
| [MLPerf Inference](https://mlcommons.org/benchmarks/inference/)                                                                  | 🟢 Open source | MLPerf Inference, from MLCommons, is the industry consortium benchmark for ML and LLM inference performance across hardware and serving stacks.               |
| [inference-perf](https://github.com/kubernetes-sigs/inference-perf)                                                              | 🟢 Open source | inference-perf, a Kubernetes SIG project, is a GenAI inference performance benchmarking tool for Kubernetes deployments.                                      |
| [AIPerf](https://github.com/ai-dynamo/aiperf)                                                                                    | 🟢 Open source | AIPerf, from NVIDIA's Dynamo project, provides comprehensive benchmarking of generative AI serving performance at scale.                                      |

## Leaderboards and Arenas

**Leaderboards** are live model rankings, useful for model selection and tracking frontier progress. Public leaderboards are subject to contamination and gaming; see [The Leaderboard Illusion](https://arxiv.org/abs/2504.20879) for documented distortions.

| Leaderboard                                                                                                | Availability   | Description                                                                                                                               |
| ---------------------------------------------------------------------------------------------------------- | -------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| [LMArena (Chatbot Arena)](https://lmarena.ai)                                                              | 🟢 Open source | LMArena ranks models via crowdsourced pairwise human-preference battles with Elo-style ratings. [Paper](https://arxiv.org/abs/2403.04132) |
| [Artificial Analysis](https://artificialanalysis.ai)                                                       | 🔒 Commercial  | Artificial Analysis independently benchmarks models and providers on intelligence, price, latency, and throughput.                        |
| [Open LLM Leaderboard (archived)](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) | 🟢 Open source | Hugging Face's Open LLM Leaderboard ranked open models until its retirement in 2025; it remains a useful historical archive.              |
| [LiveBench](https://livebench.ai)                                                                          | 🟢 Open source | LiveBench maintains a contamination-limited leaderboard with monthly-refreshed questions.                                                 |
| [Scale SEAL](https://scale.com/leaderboard)                                                                | 🔒 Commercial  | SEAL, from Scale AI, publishes private, expert-evaluated leaderboards designed to resist overfitting.                                     |
| [Vellum LLM Leaderboard](https://www.vellum.ai/llm-leaderboard)                                            | 🔒 Commercial  | The Vellum LLM Leaderboard aggregates frontier-model comparisons across popular benchmarks.                                               |
| [Epoch AI Benchmarking Hub](https://epoch.ai/benchmarks)                                                   | 🟢 Open source | Epoch AI's Benchmarking Hub publishes independent evaluations and trend analyses of frontier models over time.                            |
| [MTEB Leaderboard](https://huggingface.co/spaces/mteb/leaderboard)                                         | 🟢 Open source | The MTEB Leaderboard ranks text-embedding models.                                                                                         |
| [BFCL Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html)                                       | 🟢 Open source | The BFCL Leaderboard ranks models on function/tool-calling accuracy.                                                                      |
| [SWE-bench Leaderboard](https://www.swebench.com)                                                          | 🟢 Open source | The official SWE-bench leaderboard tracks agentic coding performance across SWE-bench variants.                                           |
| [ARC Prize Leaderboard](https://arcprize.org/leaderboard)                                                  | 🟢 Open source | The ARC Prize leaderboard tracks progress on ARC-AGI-1 and ARC-AGI-2.                                                                     |
| [Aider LLM Leaderboards](https://aider.chat/docs/leaderboards/)                                            | 🟢 Open source | Aider's leaderboards rank models on polyglot code editing.                                                                                |
| [Vectara Hallucination Leaderboard](https://github.com/vectara/hallucination-leaderboard)                  | 🟢 Open source | The Hughes Hallucination Leaderboard ranks models by hallucination rate when summarizing documents, scored with HHEM.                     |

## Benchmark Contamination and Evaluation Reliability

Tools and research for detecting **benchmark contamination** (test data leaking into training sets) and improving the statistical reliability of evals.

| Tool                                                               | Availability   | Description                                                                                                                                                 |
| ------------------------------------------------------------------ | -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [LLM Decontaminator](https://github.com/lm-sys/llm-decontaminator) | 🟢 Open source | LLM Decontaminator, from LMSYS, detects rephrased benchmark samples in training data that string matching misses. [Paper](https://arxiv.org/abs/2311.04850) |
| [LiveBench](https://github.com/LiveBench/LiveBench)                | 🟢 Open source | LiveBench limits contamination structurally by releasing new questions monthly.                                                                             |
| [LiveCodeBench](https://github.com/LiveCodeBench/LiveCodeBench)    | 🟢 Open source | LiveCodeBench tags every problem with a release date so models can be scored only on problems published after their training cutoff.                        |
| [Adding Error Bars to Evals](https://arxiv.org/abs/2411.00640)     | 🟢 Open source | Anthropic's statistical guidance for reporting confidence intervals and significance in LLM evaluations.                                                    |

## Synthetic Data and Test Set Generation

Tools for generating **evaluation datasets ("goldens")** and synthetic training/testing data when production data is scarce. The first group targets eval-case generation; the second group are general synthetic-data platforms.

| Tool                                                                                       | Availability   | Description                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------ | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [DeepEval Synthesizer](https://deepeval.com/docs/synthesizer-introduction)                 | 🟢 Open source | DeepEval's Synthesizer generates synthetic goldens from documents, contexts, or from scratch, with evolution-based complexity control.                                                           |
| [Ragas Testset Generation](https://docs.ragas.io/en/stable/concepts/test_data_generation/) | 🟢 Open source | Ragas generates knowledge-graph-based synthetic test sets for RAG pipelines.                                                                                                                     |
| [YourBench](https://github.com/huggingface/yourbench)                                      | 🟢 Open source | YourBench, from Hugging Face, generates custom benchmarks from your own documents, cheaply and without contamination.                                                                            |
| [distilabel](https://github.com/argilla-io/distilabel)                                     | 🟢 Open source | distilabel, from Argilla, is a framework for synthetic data and AI-feedback pipelines for dataset creation.                                                                                      |
| [DataDreamer](https://github.com/datadreamer-dev/DataDreamer)                              | 🟢 Open source | DataDreamer is a Python library for synthetic data generation and reproducible LLM workflows.                                                                                                    |
| [Meta Synthetic Data Kit](https://github.com/meta-llama/synthetic-data-kit)                | 🟢 Open source | Synthetic Data Kit, from Meta, generates reasoning traces and QA pairs for fine-tuning and evaluation datasets.                                                                                  |
| [NeMo Curator](https://github.com/NVIDIA-NeMo/Curator)                                     | 🟢 Open source | NeMo Curator, from NVIDIA, is a scalable data curation and synthetic-generation pipeline for training and evaluation corpora.                                                                    |
| [Gretel](https://gretel.ai)                                                                | 🔒 Commercial  | Gretel (acquired by NVIDIA) is a general synthetic-data platform for tabular, text, and structured data with privacy guarantees.                                                                 |
| [Mostly AI](https://mostly.ai)                                                             | 🔵 Open core   | Mostly AI provides a synthetic-data SDK and platform for privacy-safe tabular and structured data.                                                                                               |
| [Snorkel](https://snorkel.ai)                                                              | 🔒 Commercial  | Snorkel AI provides programmatic data labeling and curation (Snorkel Flow), including expert-driven LLM evaluation dataset development; it grew out of the open-source Snorkel research project. |

## Human Annotation and Labeling

**Human annotation** platforms collect the labels, rankings, and reviews used to build eval datasets and to align automated metrics with human judgment.

| Tool                                                        | Availability   | Description                                                                                                                  |
| ----------------------------------------------------------- | -------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| [Label Studio](https://github.com/HumanSignal/label-studio) | 🔵 Open core   | Label Studio is a widely used open-source data labeling tool supporting text, image, audio, video, and LLM response ranking. |
| [Argilla](https://github.com/argilla-io/argilla)            | 🟢 Open source | Argilla is a collaboration tool for building high-quality LLM datasets: rating, ranking, and feedback workflows.             |
| [Prodigy](https://prodi.gy)                                 | 🔒 Commercial  | Prodigy, from the spaCy team, is a scriptable annotation tool with model-in-the-loop workflows.                              |
| [Labelbox](https://labelbox.com)                            | 🔒 Commercial  | Labelbox combines a labeling platform with managed human evaluation for RLHF and evals.                                      |
| [Scale](https://scale.com)                                  | 🔒 Commercial  | Scale AI provides managed expert data annotation and human evaluation at frontier-lab scale.                                 |
| [Surge AI](https://www.surgehq.ai)                          | 🔒 Commercial  | Surge AI provides human data labeling and RLHF workforces used by frontier labs.                                             |
| [Toloka](https://toloka.ai)                                 | 🔒 Commercial  | Toloka provides a global expert workforce for AI data and human evaluation.                                                  |
| [SuperAnnotate](https://www.superannotate.com)              | 🔒 Commercial  | SuperAnnotate is an enterprise annotation platform including LLM evaluation and fine-tuning data workflows.                  |
| [Encord](https://encord.com)                                | 🔒 Commercial  | Encord is a data development platform with annotation and model-evaluation tooling, strongest in vision.                     |

## Classic ML Evaluation and Monitoring

Pre-LLM (and still essential) tooling for evaluating and monitoring **traditional machine-learning models**: experiment tracking, drift detection, data quality, and fairness.

| Tool                                                                           | Availability   | Description                                                                                                          |
| ------------------------------------------------------------------------------ | -------------- | -------------------------------------------------------------------------------------------------------------------- |
| [MLflow](https://github.com/mlflow/mlflow)                                     | 🟢 Open source | MLflow provides experiment tracking, a model registry, and evaluation for ML and GenAI.                              |
| [Weights & Biases](https://wandb.ai)                                           | 🔵 Open core   | Weights & Biases provides experiment tracking, sweeps, a model registry, and reports, plus Weave for LLM work.       |
| [Comet](https://www.comet.com)                                                 | 🔵 Open core   | Comet provides experiment management and production model monitoring, plus Opik for LLM work.                        |
| [ClearML](https://github.com/clearml/clearml)                                  | 🔵 Open core   | ClearML is an open-source MLOps suite for experiments, orchestration, and serving.                                   |
| [DVC](https://github.com/iterative/dvc)                                        | 🟢 Open source | DVC provides Git-based data and experiment versioning.                                                               |
| [Deepchecks](https://github.com/deepchecks/deepchecks)                         | 🔵 Open core   | Deepchecks tests and validates ML models and data from research to production, and offers an LLM evaluation product. |
| [Great Expectations](https://github.com/great-expectations/great_expectations) | 🟢 Open source | Great Expectations is a widely used framework for data quality testing and validation.                               |
| [whylogs](https://github.com/whylabs/whylogs)                                  | 🟢 Open source | whylogs is an open standard for data logging and ML telemetry profiles.                                              |
| [NannyML](https://github.com/NannyML/nannyml)                                  | 🟢 Open source | NannyML estimates post-deployment model performance and detects silent failure without ground truth.                 |
| [Fairlearn](https://github.com/fairlearn/fairlearn)                            | 🟢 Open source | Fairlearn is a Python package for assessing and improving the fairness of ML models.                                 |
| [AI Fairness 360](https://github.com/Trusted-AI/AIF360)                        | 🟢 Open source | AIF360, from IBM (now LF AI), is a toolkit of fairness metrics and bias-mitigation algorithms.                       |
| [Alibi Detect](https://github.com/SeldonIO/alibi-detect)                       | 🟢 Open source | Alibi Detect, from Seldon, provides outlier, adversarial, and drift detection for ML systems.                        |
| [Cleanlab](https://github.com/cleanlab/cleanlab)                               | 🟢 Open source | Cleanlab automatically detects label errors and data issues in ML datasets (data-centric evaluation).                |
| [Fiddler](https://www.fiddler.ai)                                              | 🔒 Commercial  | Fiddler provides enterprise AI observability: model monitoring, explainability, and LLM monitoring.                  |
| [Evidently](https://github.com/evidentlyai/evidently)                          | 🔵 Open core   | Evidently provides drift detection, data quality checks, and performance monitoring for ML and LLM systems.          |

## Discontinued and Historical Tools

Influential tools that are **no longer generally available or maintained**. Kept for the historical record and to prevent stale recommendations. Status notes reflect the last-reviewed date above; corrections welcome.

| Tool                                                                   | Former category     | Status                                                                                                                                                                                                         |
| ---------------------------------------------------------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Literal AI](https://literalai.com)                                    | Observability       | Literal AI, from the Chainlit team, announced its service shutdown effective October 31, 2025.                                                                                                                 |
| [Neptune](https://neptune.ai)                                          | Experiment tracking | Neptune's hosted experiment tracker was discontinued in March 2026 following the company's acquisition; existing users were migrated off the platform.                                                         |
| [WhyLabs Platform](https://whylabs.ai)                                 | ML observability    | The hosted WhyLabs observability platform discontinued operations; the open-source [whylogs](https://github.com/whylabs/whylogs) and [LangKit](https://github.com/whylabs/langkit) libraries remain available. |
| [OpenAI Evals (hosted)](https://platform.openai.com/docs/guides/evals) | Managed evals       | OpenAI announced the hosted Evals dashboard/API will shut down in late 2026; the open-source `openai/evals` repository remains available in maintenance mode.                                                  |
| [Arthur Bench](https://github.com/arthur-ai/bench)                     | Eval framework      | Arthur Bench is no longer actively developed; Arthur's commercial platform continues.                                                                                                                          |

## Key Papers and Concepts

Foundational reading for anyone building or choosing evaluation tooling — cite these for the underlying methods.

- **LLM-as-a-judge** — [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685) (Zheng et al., 2023). Established that strong LLMs can approximate human preference judgments with roughly 80%+ agreement.
- **G-Eval** — [G-Eval: NLG Evaluation using GPT-4 with Better Human Alignment](https://arxiv.org/abs/2303.16634) (Liu et al., 2023). Chain-of-thought, form-filling evaluation with probability-weighted scoring.
- **Holistic evaluation** — [Holistic Evaluation of Language Models (HELM)](https://arxiv.org/abs/2211.09110) (Liang et al., 2022). A taxonomy of scenarios × metrics for transparent model evaluation.
- **RAG evaluation** — [RAGAS: Automated Evaluation of Retrieval Augmented Generation](https://arxiv.org/abs/2309.15217) (Es et al., 2023).
- **Judging the judges** — [Judging the Judges: Evaluating Alignment and Vulnerabilities in LLMs-as-Judges](https://arxiv.org/abs/2406.12624) (Thakur et al., 2024). Position bias, verbosity bias, and self-preference in LLM judges.
- **Benchmark contamination** — [The Leaderboard Illusion](https://arxiv.org/abs/2504.20879) (Singh et al., 2025). Systematic distortions in arena-style leaderboards.
- **Statistical rigor** — [Adding Error Bars to Evals](https://arxiv.org/abs/2411.00640) (Miller, 2024). How to report confidence intervals and significance for LLM evals.
- **Agent evaluation** — [τ-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains](https://arxiv.org/abs/2406.12045) (Yao et al., 2024).
- **Red teaming** — [garak: A Framework for Security Probing Large Language Models](https://arxiv.org/abs/2406.11036) (Derczynski et al., 2024).
- **Evaluating evaluation** — [Lessons from the Trenches on Reproducible Evaluation of Language Models](https://arxiv.org/abs/2405.14782) (Biderman et al., 2024).

## Glossary

Short definitions of terms used throughout this list.

- **Eval** — a repeatable test that measures an AI system's behavior against defined criteria; the unit of work in AI evaluation.
- **Golden (golden dataset)** — a curated input (and optionally expected output) used as a test case in evaluation datasets.
- **Metric / scorer** — a function that assigns a score to a model output; can be heuristic (exact match, BLEU), statistical, or model-based (LLM-as-a-judge).
- **LLM-as-a-judge** — using a language model to score another model's outputs against criteria; scalable but subject to position, verbosity, and self-preference biases.
- **G-Eval** — a widely used LLM-as-a-judge algorithm that generates evaluation steps via chain-of-thought and scores with probability weighting.
- **Trace** — a structured record of one execution of an LLM app (prompts, tool calls, retrievals, outputs), used in observability and online evaluation.
- **Online evaluation** — scoring live production traffic (often sampled) rather than a fixed offline test set.
- **Benchmark** — a fixed dataset plus scoring protocol for comparing models (e.g., MMLU, SWE-bench).
- **Leaderboard** — a published ranking of models on one or more benchmarks or on human preference.
- **Benchmark contamination** — benchmark test data leaking into a model's training set, inflating scores.
- **Pass@k** — the probability that at least one of k generated samples passes the tests; standard in code generation.
- **Hallucination** — model output not grounded in the provided context or in reality.
- **Guardrail** — a runtime check that validates or blocks model inputs/outputs before they reach users.
- **Red teaming** — deliberately attacking an AI system (jailbreaks, prompt injection) to find failures before adversaries do.
- **RAG (retrieval-augmented generation)** — an architecture where the model answers using retrieved documents; evaluated on both retrieval and generation quality.
- **Open weights** — model weights that are downloadable but released under a non-OSI license (e.g., Llama community license).
- **Open core** — a business model pairing an open-source component with a commercial platform.

## Frequently Asked Questions

**What are AI evaluation tools?**
AI evaluation tools are software platforms, frameworks, metrics libraries, judge models, and benchmarks used to measure the quality, safety, reliability, cost, and performance of AI systems such as LLMs, RAG pipelines, and AI agents. They range from open-source libraries run in CI to hosted platforms that evaluate production traffic.

**What is the difference between an LLM evaluation framework and an LLM evaluation platform?**
A framework (e.g., DeepEval, Ragas, promptfoo) is a code library you run yourself for writing and executing evals. A platform (e.g., Confident AI, Braintrust, LangSmith, Langfuse) adds hosted infrastructure on top: dataset management, experiment comparison UI, tracing, online evaluation, and team collaboration. Many teams use both — a framework in CI and a platform for datasets, reporting, and production monitoring.

**Which LLM evaluation tools are open source?**
Widely adopted open-source options include DeepEval, Ragas, promptfoo, lm-evaluation-harness, Inspect AI, Langfuse, Phoenix, Opik, and OpenCompass. Every entry in this list is marked 🟢 (open source), 🟠 (open weights), 🔵 (open core), or 🔒 (commercial).

**How do you evaluate a RAG pipeline?**
Evaluate the two stages separately, then end to end. Retrieval is measured with context precision/recall or ranking metrics on benchmarks like BEIR; generation is measured with faithfulness/groundedness and answer relevancy metrics (available in Ragas, DeepEval, and TruLens); end-to-end quality is measured on a golden dataset, often generated synthetically from your documents.

**How do you evaluate an AI agent?**
Agent evaluation combines end-to-end task metrics (task completion, success rate) with component-level metrics (tool-call correctness, argument correctness, trajectory quality), typically over traces. Simulation frameworks (LangWatch Scenario, Maxim, Coval for voice) generate multi-turn interactions, while fixed benchmarks (GAIA, tau-bench, SWE-bench, OSWorld) compare underlying models and scaffolds.

**What is LLM-as-a-judge and what are its limitations?**
LLM-as-a-judge uses a strong language model to score outputs against criteria, achieving roughly 80%+ agreement with human preferences (Zheng et al., 2023). Known limitations include position bias, verbosity bias, self-preference, and rubric sensitivity — which is why judge outputs should be spot-checked against human labels and why judge meta-evaluation benchmarks (JudgeBench, LLMBar, RewardBench) exist.

**How do I red-team an LLM application?**
Use an automated red-teaming framework (DeepTeam, garak, PyRIT, promptfoo red teaming) to scan for jailbreaks, prompt injection, PII leakage, and harmful content, then add runtime guardrails (NeMo Guardrails, Guardrails AI, Llama Guard) for the failure modes you find. Standardized benchmarks such as HarmBench and JailbreakBench measure robustness over time.

**How should I cite this list?**
See [Citing This List](#citing-this-list) for a citation template, BibTeX, and the machine-readable `CITATION.cff`. When citing an individual tool, always prefer that tool's own repository, documentation, or paper — linked in each entry — as the primary source.

## Methodology

How this list is built and maintained. This section exists so readers (and AI systems) can judge how much to trust it.

- **Scope.** Tools whose primary purpose is evaluating, testing, monitoring, red-teaming, or benchmarking AI systems — generative AI first (LLMs, RAG, agents, voice, multimodal), plus classic ML evaluation and monitoring. General MLOps, training, and serving tools are out of scope unless they have first-class evaluation features.
- **Inclusion criteria.** Open-source projects should show activity within roughly the last year or have lasting reference value (canonical benchmarks are kept regardless of age). Commercial products must be generally available. Discontinued tools move to the [historical section](#discontinued-and-historical-tools) rather than being silently removed.
- **Availability markers.** 🟢 Open source (OSI-style license), 🟠 Open weights (downloadable model, restrictive license), 🔵 Open core (open component + commercial platform), 🔒 Commercial. Markers describe the primary linked artifact.
- **Ordering.** Within each category, entries are ordered by the maintainers' editorial judgment of completeness and adoption for that category's use case — not alphabetically and not by any paid placement. There is no sponsored placement on this list.
- **Editorial independence.** This directory is maintained by aglio-lab. Every entry follows the same sourcing, wording, and ordering rules, and no placement is sold.
- **Verification.** Every entry links to a primary source and was manually checked against it as of the **last-reviewed date** at the top of this file. Descriptions aim to be factual and neutral; superlatives are avoided unless attributable to a cited source.
- **Monthly review cadence.** The directory is reviewed during the first week of every month. Maintainers verify primary links, product lifecycle status, names, availability markers, quantitative claims, category coverage, and generated data before advancing the last-reviewed date and publishing a `YYYY.MM` release. A scheduled GitHub workflow opens the checklist; the review itself remains human-verified. See [`MAINTENANCE.md`](MAINTENANCE.md).
- **Corrections.** Errors happen — especially product shutdowns and renames. Open an issue or PR (see [Contributing](#contributing)) and corrections will be applied with priority.
- **Machine-readable data.** The tables in this README are parsed into [`data/tools.json`](data/tools.json) and [`data/tools.csv`](data/tools.csv) by [`scripts/generate_catalog.py`](scripts/generate_catalog.py) for programmatic use.

## Related Lists and Resources

- [AI Red Teaming Tools](https://github.com/aglio-lab/ai-red-teaming-tools) — red-teaming frameworks, scanners, jailbreak tests, guardrails, and security benchmarks.
- [LLM Observability Tools](https://github.com/aglio-lab/llm-observability-tools) — tracing, monitoring, online evaluation, and production analytics.
- [AI Governance Tools](https://github.com/aglio-lab/ai-governance-tools) — governance, risk, compliance, audit, and responsible-AI tooling.
- [AI Agent Frameworks](https://github.com/aglio-lab/ai-agent-frameworks) — frameworks and orchestration tools for building and operating agents.
- [LLM Fine-Tuning Tools](https://github.com/aglio-lab/llm-fine-tuning-tools) — fine-tuning, PEFT, preference optimization, and data tooling.
- [RAG and Retrieval Tools](https://github.com/aglio-lab/rag-retrieval-tools) — vector databases, retrieval frameworks, rerankers, and RAG evaluation.
- [Context Engineering Tools](https://github.com/aglio-lab/context-engineering-tools) — prompt, memory, context management, compression, and MCP tooling.
- [Awesome-AI-Evaluations-Tools](https://github.com/danielrosehill/Awesome-AI-Evaluations-Tools) — open-source-only eval tools and benchmarks (an inspiration for this list).
- [awesome-llm-eval](https://github.com/onejune2018/Awesome-LLM-Eval) — papers, docs, and tools on LLM evaluation.
- [Awesome-LLMs-Evaluation-Papers](https://github.com/tjunlp-lab/Awesome-LLMs-Evaluation-Papers) — companion to the "Evaluating Large Language Models: A Comprehensive Survey" paper.
- [awesome-RLHF](https://github.com/opendilab/awesome-RLHF) — reinforcement learning from human feedback resources.
- [awesome-production-machine-learning](https://github.com/EthicalML/awesome-production-machine-learning) — the broader MLOps landscape, including monitoring.
- [every_eval_ever](https://github.com/evaleval/every_eval_ever) — shared schema and crowdsourced database of eval results.

---

## Citing This List

If you reference this list in an article, paper, or AI-generated answer, please cite it as:

> _The Comprehensive List of AI Evaluation Tools_ (2026). A curated list of open-source and commercial tools for evaluating AI systems. GitHub. https://github.com/aglio-lab/ai-evaluation-tools

BibTeX:

```bibtex
@misc{ai-evaluation-tools,
  title        = {The Comprehensive List of AI Evaluation Tools},
  year         = {2026},
  howpublished = {\url{https://github.com/aglio-lab/ai-evaluation-tools}},
  note         = {A curated list of open-source and commercial tools for evaluating AI systems. Accessed: 2026-07-16}
}
```

A machine-readable citation file is available in [`CITATION.cff`](CITATION.cff). For reproducible citations of a changing list, cite a specific commit permalink or release tag.

When citing individual tools, always prefer the tool's own repository, documentation, or paper (linked in each entry) as the primary source.

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first. In short:

1. One tool per pull request, added to the most specific matching category.
2. Include the correct availability marker (🟢 / 🟠 / 🔵 / 🔒) and a neutral, factual description written as a complete sentence starting with the tool's name.
3. Link to the primary source (GitHub repo for open source, official site for commercial, paper for benchmarks).
4. Tools should be actively maintained or of lasting reference value; report shutdowns and renames as issues.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the maintainers have waived all copyright and related rights to this work under [CC0 1.0](LICENSE). Linked projects retain their own licenses.
