<div align="center">

# Generative AI Cookbooks

**Notebook-based learning tracks for federated learning and language-model pre-training.**

[![Jupyter notebooks](https://img.shields.io/badge/Jupyter-11%20notebooks-F37626?logo=jupyter&logoColor=white)](#notebook-catalog)

[Catalog](#notebook-catalog) · [Getting started](#getting-started) · [Reproducibility](#reproducibility-status)

</div>

## What is it?

This repository is a learning collection rather than a packaged Python library. It contains 11 Jupyter notebooks split across two progressive tracks: federated learning with Flower and the data, model, training, and evaluation stages of LLM pre-training.

The notebooks are best used for guided reading and experimentation. There is no root environment file, command-line entry point, or automated test suite.

## Notebook catalog

### Federated learning

| Notebook | Topic |
| --- | --- |
| [`L1_Why_Federated_Learning.ipynb`](federated-learning/L1_Why_Federated_Learning.ipynb) | Motivation and core concepts |
| [`L2_Federated_Training_Process.ipynb`](federated-learning/L2_Federated_Training_Process.ipynb) | Client/server training flow with Flower |
| [`L3_Tuning.ipynb`](federated-learning/L3_Tuning.ipynb) | Strategy and training configuration |
| [`L4_Data_Privacy.ipynb`](federated-learning/L4_Data_Privacy.ipynb) | Client-side privacy mechanisms |
| [`L5_Bandwidth.ipynb`](federated-learning/L5_Bandwidth.ipynb) | Communication and bandwidth controls |

### LLM pre-training

| Notebook | Topic |
| --- | --- |
| [`Lesson_1.ipynb`](pre-training-llm/Lesson_1.ipynb) | Why pre-train a model |
| [`Lesson_2.ipynb`](pre-training-llm/Lesson_2.ipynb) | Data preparation |
| [`Lesson_3.ipynb`](pre-training-llm/Lesson_3.ipynb) | Dataset packaging |
| [`Lesson_4.ipynb`](pre-training-llm/Lesson_4.ipynb) | Model preparation |
| [`Lesson_5.ipynb`](pre-training-llm/Lesson_5.ipynb) | Training |
| [`Lesson_6.ipynb`](pre-training-llm/Lesson_6.ipynb) | Evaluation |

## Getting started

Create an isolated environment and launch Jupyter from the repository root:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install jupyterlab
jupyter lab
```

On Windows PowerShell, activate with `.\.venv\Scripts\Activate.ps1`.

Install the imports required by the specific notebook you intend to run. The collection does not currently provide a tested shared requirements file, so a single blanket install command would be misleading.

## Reproducibility status

| Area | Status |
| --- | --- |
| Notebook source | **Implemented** — all 11 notebooks are committed. |
| Shared environment | **Unavailable** — dependency versions are not pinned at the root. |
| Federated-learning helpers | **Unavailable in this repository** — notebooks import local modules such as `utils1`, `utils2`, and `utils3`. |
| External data/model access | **Required by some notebooks** — review cells before execution, especially downloads and training workloads. |
| Automated verification | **Unavailable** — no CI or notebook execution tests are committed. |

The pre-training track acknowledges DeepLearning.AI resources in its [track README](pre-training-llm/README.md).

## Repository layout

```text
generative-ai-cookbooks/
├── federated-learning/   # five Flower-focused notebooks
└── pre-training-llm/     # six LLM pre-training notebooks
```
