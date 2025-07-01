# llm-api-playground
--
Repo for setup fo LLM API Playground

## Overview

This repository contains AI pipelines and workflows used to evaulate effectiveness of various Large Language Models (LLMs) for pedogical use cases and develop early-stage custom application protoypes (and potentially production-ready components) for use in the academic setting.

 These workflows may integrate services such as Retrieval-Augmented Generation (RAG), Optical Character Recognition (OCR), LLM inference, prompt management, and evaluation, based on the intended use case.

These workflows support projects like **Digital Latin**, as well as future applications at the intersection of AI and teaching and learning.

---

## Directory Structure

### `api_integration_summaries/`

Notebooks should embed all metadata, setup details, usage context, and example outputs.  

- Notebook-driven documentation for each provider
- Contains credential origin (e.g. AWS SSM path)
- Serves as both credential validator and onboarding guide  
- Includes test output, supported models, and external doc references  
- Screenshots or example responses may also be stored here

---

### `benchmarking/`

- Structured experiments that run multiple models across the same tasks  
- Includes performance metrics: latency, output quality, cost, retries  
- May be organized by project (`/digital-latin`) or test method  
- Ideal for evaluating provider readiness or informing tool design

---

### `playground_environments/`

Workspaces and environments that enable team-based experimentation, examples include GitLab runners, Colab notebooks, and Binder environments.

- Contains temporary or test-ready environments for experimentation  
- Examples might include:
  - Multi-user Colab notebooks
  - GitLab CI/Pipelines
  - Binder-based explorables  
- Useful for team demos, parallel exploration, or debugging

---

### `prototype_ai_workflows/`

Early-stage exploration of logic and systems.  
Works may include notebooks, CLI scripts, or hybrid environments that reflect current thinking for RAG pipelines, OCR-first flows, and more.

- Experimental and incomplete LLM workflows  
- Often include:
  - Notebooks or scripts
  - OCR + LLM combinations
  - RAG pipelines
  - Partial integration attempts  
- Intended primarily for internal iteration, testing, and review

---

### `production_ai_workflow/` (TBD)

More modular and hardened components possible to deploy in backend workers or integrated systems. These may form the basis of `ai_worker` components in downstream tools.

- More stable and modularized workflows or pipelines  
- May support:
  - Backend LLM services (FastAPI workers, wrappers)
  - Deployable inference/classification/ranking pipelines
  - Frontend interfaces or APIs calling AI logic  
- Intended to support downstream tools and apps

---

### `shared_components/`(TBD)

- Shared Python functions or classes reusable across workflows
- Examples:
  - Prompthandlers
  - Model routers
  - Retry logic
  - Input validators  
- Helps keep duplicated logic out of both prototype and production flows

---

## Notes

- All work is intended to move from `prototype_ai_workflow/` → `production_ai_workflow/`, or another production repository, when ready.

- This repo is not intended to be a monolithic tool — it's a collaborative space for pipeline R&D and tooling integration.


---

## Scope of This Repository

This project provides:

- Executable integration summaries for major LLM APIs (OpenAI, Anthropic, Cohere, etc.)
- Prototypes of multi-component AI workflows involving LLMs and supporting services (e.g. OCR, retrieval)
- Experiment-friendly environments for testing models, endpoints, and interfaces
- Comparative benchmarking across models, including latency, token usage, and response quality
- Clear handoff paths from prototype to production-ready tooling

---

## Local Setup

Requirements vary by subdirectory. In general:

```bash
git clone https://github.com/your-org/llm-api-playground.git
cd llm-api-playground
