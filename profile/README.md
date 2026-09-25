<a href="https://nodegrove.io"><img src="https://raw.githubusercontent.com/nodegrove/.github/main/profile/banner.png" alt="Nodegrove: your private AI server. No hardware to buy." width="100%"></a>

**Nodegrove is a private AI server in the cloud.** One workspace that stays as you left it: your files, models, installed tools and settings persist between sessions, and a GPU attaches when you start working and detaches when you stop. Create images and video, run open models privately, fine-tune.

The service is not open yet. Today there is [nodegrove.io](https://nodegrove.io), its free calculators, the open data below and a waitlist; next is a small invite-only pilot. [Request early access](https://nodegrove.io/#early-access).

### Open data

**[llm-vram-dataset](https://github.com/nodegrove/llm-vram-dataset)**: how much GPU memory 29 open-weight models need at six quantisations and every common context length, and which of 13 GPUs run each one. Architecture values from each model's config.json, GPU specs from the manufacturers, one formula written out. CSV and JSON under CC BY 4.0: use it anywhere, with a link back.

- **Newer models pay far less for context.** At 32k tokens, Qwen3 32B (2025, standard attention) spends 8.6 GB on its KV cache; its successor Qwen3.8 27B (2026, hybrid attention) spends 2.3 GB.
- **Active parameters set the speed, not the memory.** Qwen3-Coder-Next 80B-A3B reads 3B parameters per token but keeps all 79.7B in memory: 48.9 GB at Q4_K_M with 8k context, against 22.4 GB for the dense Qwen3 32B.
- **24 of 29 models fit a 24 GB card at Q4_K_M with 8k context.** The largest is Qwen3.6 35B-A3B at 22.4 GB, under the 22.8 GB line (95% of the card).

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22966137.svg)](https://doi.org/10.5281/zenodo.22966137) [Latest release](https://github.com/nodegrove/llm-vram-dataset/releases/latest) · [Method and columns](https://nodegrove.io/data) · Data version 2026-09-25

### Free tools

- **[Can I run it?](https://nodegrove.io/tools/can-i-run-it)** Your GPU and any model: fits or not, how fast, and what to change when it does not.
- **[LLM VRAM calculator](https://nodegrove.io/tools/llm-vram-calculator)** Weights, KV cache and overhead for any model, with the formula shown.
- **[Tokens-per-second estimator](https://nodegrove.io/tools/llm-speed-estimator)** How fast a model can run on a given GPU, from bandwidth and weight size.
- **[Build vs rent calculator](https://nodegrove.io/tools/build-vs-rent-calculator)** Your hours, your electricity, your plan. Finds the break-even month.

Plus a page for [every model](https://nodegrove.io/models) and [every GPU](https://nodegrove.io/gpus) in the dataset, and [guides](https://nodegrove.io/guides) to running open models.

### How we work

- Every number is a published specification, a formula written out on the page, or a number you typed in. Nothing is a benchmark.
- Every source is linked, so every figure can be checked, and corrections are made in public.
- We say [where your data lives](https://nodegrove.io/data-and-privacy), layer by layer, instead of calling it safe.

<sub>[nodegrove.io](https://nodegrove.io) · [About](https://nodegrove.io/about) · [info@nodegrove.io](mailto:info@nodegrove.io)</sub>
