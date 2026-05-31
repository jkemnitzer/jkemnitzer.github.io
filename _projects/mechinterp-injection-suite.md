---
layout: page
title: mechinterp-injection-suite
description: A mechanistic interpretability pipeline for identifying attention-head circuits causally responsible for prompt injection in instruction-tuned LLMs. Supports 9+ model architectures including Llama, Gemma, Mistral, Qwen, and Phi.
img:
importance: 1
category: work
github: https://github.com/jkemnitzer/mechinterp-injection-suite
---

A research-grade interpretability toolkit for understanding how prompt injection attacks operate at the neural circuit level in instruction-tuned large language models.

The pipeline performs a 14-step analysis — from initial calibration through circuit identification — to pinpoint which attention heads enable a model to override its system instructions when presented with conflicting user directives.

**Core capabilities:**
- Full head ablation sweeps across all attention layers
- Causal sufficiency testing via activation patching
- Direct logit attribution for per-head contribution analysis
- Circuit classification into HUB_SPOKE, ENSEMBLE, and PLATEAU topologies
- Cross-model compatibility (Llama, Gemma, Mistral, Qwen, Phi, and more)

**Stack:** TransformerLens · PyTorch · Hugging Face · Pydantic · CUDA

Outputs include ablation statistics, attention heatmaps, and structured JSON results for downstream analysis.
