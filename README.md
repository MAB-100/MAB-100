# Muhammad Abbas Bukhari

AI Engineer at [CureMD](https://www.curemd.com). I build production LLM systems (RAG, evaluation harnesses and multi-agent workflows) and run the data infrastructure underneath them.

[LinkedIn](https://linkedin.com/in/muhammad-abbas-bukhari) · [shahabbas661@gmail.com](mailto:shahabbas661@gmail.com)

## Highlights

- Shipped two company-wide RAG products with 475k+ emails indexed, serving 12 teams
- Gate every deploy with an LLM evaluation harness (YAML benchmark suites, LLM-as-judge grading) and a 1,400+ test pytest suite
- Run full-pipeline observability with Langfuse: per-stage traces, token and cost accounting, and sampled quality scores on production traffic
- Build multi-agent automation with LangGraph
- Operate a 9-node Kerberized Hadoop HA cluster, the AI department's data backbone

## Production work at CureMD

Built at CureMD. The code is proprietary and not public.

**Client Communications Intelligence platform.** RAG over 214k+ client emails from 871 healthcare practices. The pipeline: Outlook (Microsoft Graph) → MongoDB + Milvus (HNSW), then an LLM query planner routing across 4 retrieval modes, reranking, LLM relevance filtering and citation-grounded answers. It's served as an OpenAI-compatible streaming API (FastAPI, SSE). An adaptive retry orchestrator recovers failed retrievals across 7 pipeline stages.

**Personal Email Assistant.** A self-service RAG assistant that employees connect to their own mailbox (260k+ emails ingested). Onboarding happens entirely in the chat: MSAL device-flow sign-in, an auto-triggered first ingestion and token refresh. Ingestion is fault-tolerant, with checkpoint/resume, MongoDB–Milvus consistency audits and incremental syncs every 10 minutes.

**Multi-agent data-pipeline automation.** Takes a data pipeline from requirements to a one-click Docker deployment, cutting days to minutes. Three LangGraph agents do the work: a rule-based pipeline recommender with 36 templates, a configuration generator and validator, and a Docker deployment engine. The deployment engine merges compose files, resolves port conflicts, consolidates volumes and monitors health.

**Hadoop HA automation.** Provisions Kerberized Hadoop high-availability clusters from bare Linux machines with no manual configuration. A full 9-node bring-up takes about 30 minutes instead of days.

## Public projects

| Project | What it is | Stack |
|---|---|---|
| [Audio-to-Image Generation](https://github.com/MAB-100/Audio-to-image-Generation-Model) | Turns audio into images: classifies sounds with YAMNet, then generates images with SDXL-based Playground v2.5 | MediaPipe, Diffusers, PyTorch |
| [Python Mini Projects](https://github.com/MAB-100/python-mini-projects) | 18 small projects: recommender systems, NLP, OpenCV, Flask/Django/Streamlit apps, PyQt desktop apps | Python, scikit-learn, Django, Flask |

## Tech stack

| Area | Tools |
|---|---|
| AI and LLM | Python, OpenAI API, Ollama, LangGraph, LangChain, Langfuse, RAG, LLM evaluation |
| Data | Milvus, MongoDB, PostgreSQL, MySQL, Redis |
| Backend and infrastructure | FastAPI, Flask, Docker, Hadoop (HDFS HA), ZooKeeper, Kerberos, Linux |

## Background

BS Computer and Information Sciences, PIEAS (CGPA 3.71/4.00). Before moving into AI engineering I did security research: one-class intrusion detection, Vision Transformer malware classifiers and data-exfiltration detection.
