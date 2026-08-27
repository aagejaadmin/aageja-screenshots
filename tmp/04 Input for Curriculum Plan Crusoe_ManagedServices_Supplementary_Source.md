# Crusoe Cloud — Managed-Services Source Content (Supplementary, Verified)

Curated for the Managed-Services Operator curriculum. Content recovered
verbatim from Crusoe's own live product pages (crusoe.ai/cloud/* and
docs.crusoecloud.com), verified August 2026. Scope is the console /
managed / low-code layer. Kubernetes/Slurm/Terraform/bare-metal
("infrastructure layer") content is deliberately EXCLUDED — see the
out-of-scope note at the end.

---

## 1. Serverless Fine-Tuning (GA — July 7, 2026)

Managed, LoRA-based fine-tuning of open LLMs. Crusoe's own description:
"We run the LoRA (Low-Rank Adaptation) workflow for fast, precise, and
cost-effective fine-tuning."

**Workflow (four stages, console/UI-driven):**
1. **Model selection** — choose from a curated library of open LLMs.
2. **Data upload** — "Upload your training data to your isolated environment in standard JSONL or Parquet format."
3. **Configuration** — adjust hyperparameters via UI, SDK, or API, with pre-configured defaults.
4. **Deploy / download** — "Deploy in one click to Self-Serve Deployments for inference, or download raw weights in .safetensors format."

**Observability:** "View detailed granular training metrics. Audit trails are included on every job." "If a hardware blip occurs, the system automatically recovers and restarts, so downtime stays minimal."

**Not supported — bring-your-own base model.** Per Crusoe's FAQ: "this is a managed service, not a custom training platform. Users select from available models rather than bringing their own base models." (Teach model selection from the catalog, NOT a BYOM/base-model-upload workflow.)

---

## 2. Managed Inference

Serving open-source models with "ultra-low latency and high throughput,"
built on Crusoe's MemoryAlloy™ memory fabric.

**Three deployment options:**
- **Serverless Inference** — usage-based, fully managed API, accessed through Crusoe Intelligence Foundry. Best for early-stage, low-volume, and experimentation.
- **Self-Serve Deployments** (generally available) — two optimization profiles: **throughput** (optimized for cost/resource efficiency) and **responsiveness** (optimized for low latency). Supports **fine-tuned models deployed in one click** from Serverless Fine-Tuning. Best for production-scale, predictable-cost workloads.
- **Tailored Deployments** — team-assisted optimization for proprietary models; dedicated, benchmarked, SLA-backed endpoint. (Team-assisted, not a self-serve console workflow — this is the only path involving a customer's own/proprietary model, and it is not the operator's independent task.)

**Model catalog:** 20+ open models — DeepSeek V3/V4, Gemma 4, GLM 5.1/5.2, Llama 3.3/3.1, Qwen variants, Kimi K2.6, NVIDIA Nemotron models, Yutori n1.5.

**Performance (Crusoe claim):** up to 9.9x faster time-to-first-token and 5x higher throughput vs. vLLM (Llama-3.3-70B, 4-node).

**Pricing:** usage-based (pay-as-you-go) for serverless; provisioned throughput priced in **AI Model Units (AMUs)** for predictable cost on self-serve/production.

---

## 3. Command Center (managed-services-relevant features only)

Unified operations platform to "monitor, diagnose, and optimize AI
workloads through integrated observability."

**In-scope for the console operator:**
- **Real-time health monitoring** — "Track individual GPU health, storage, and network performance in real-time."
- **Cost & utilization tracking** — monitor "on-demand and spot costs to ensure your infrastructure is always running at peak efficiency"; track utilization so every GPU is "visible and accountable."
- **Notification Center** — "streams critical alerts to Slack or webhooks." (This is the real alerting capability — configure alerts on health/cost/performance events, delivered to Slack or webhooks.)
- **Telemetry Conduit** — streams pre-defined metrics into an existing observability stack.
- **Real-time logs** — accelerate troubleshooting "without the hunt for hidden errors."

**Out of scope for THIS persona (require Kubernetes / infra layer — do NOT build into managed-services modules):**
- **AutoClusters** — automated node remediation; requires a running CMK (Kubernetes) cluster + add-on.
- **CMK / Kubernetes logging** ("journald and Kubernetes logs"), topology-aware cluster provisioning.

---

## 4. Capacity & Cost Model

**GPU options:** NVIDIA GB200, B200, H200, H100; AMD MI300X, MI355X.

**Capacity types (teach the tradeoff):**
- **On-demand** — billed per minute, no commitment; highest cost, immediate availability.
- **Spot** — up to 90% discount; suitable for fault-tolerant workloads; may be reclaimed on short notice.
- **Reserved** — committed capacity; deepest discounts in exchange for a usage commitment.

**Cost modeling inputs:** per-minute compute (on-demand), per-token inference pricing (serverless), and provisioned-throughput AMUs (self-serve/production). Match capacity type to workload: production vs. experimental, latency-sensitive vs. batch.

---

## Out-of-scope boundary (for the curriculum agent)

This program is for operators who consume Crusoe through its **console and
managed services**. Exclude, throughout: Kubernetes (CMK), Slurm,
Terraform, bare-metal GPU provisioning, RDMA/topology tuning, and
AutoClusters. Where a feature spans both layers (e.g., Command Center),
teach only the console/managed-services capabilities listed above.
