<p align="center">
  <img src="assets/icon-512.png" width="120" alt="API Key Tester">
</p>

<h1 align="center">API Key Tester</h1>

<p align="center">
  <b>Mobile tool for testing and managing API keys across AI inference providers</b><br>
  <sub>PWA + Android APK &nbsp;·&nbsp; OpenAI-compatible &nbsp;·&nbsp; Offline-ready</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-Android%20%7C%20PWA-blue?style=flat-square" alt="Platform">
  <img src="https://img.shields.io/badge/API-OpenAI%20compatible-green?style=flat-square" alt="API">
  <img src="https://img.shields.io/badge/dependencies-zero-brightgreen?style=flat-square" alt="Deps">
  <img src="https://img.shields.io/badge/license-proprietary-red?style=flat-square" alt="License">
</p>

---

## Overview

**API Key Tester** is a lightweight mobile application designed for AI infrastructure engineers who manage multiple inference endpoints across local and cloud providers.

Built as a single-file PWA with a native Android APK wrapper, the app provides instant API key validation, model enumeration, and inference speed benchmarking — all from a phone.

---

## Background

I deploy and maintain local AI inference servers — **vLLM**, **Ollama**, **Text Generation Inference** — on multi-GPU clusters (3x RTX 3090). I integrate large language models into real-world production systems:

- **Scientific research** — data analysis, experiment automation, NLP pipelines
- **Robotic production lines** — AI modules for real-time quality control and decision-making
- **Warehouse management** — intelligent routing, predictive inventory analytics
- **Enterprise document management** — automated classification, data extraction, report generation
- **Engineering documentation** — recognition and indexing of technical drawings, CAD database search
- **Corporate databases** — natural language to SQL, AI-powered analytics

When you manage dozens of API endpoints, you need one tool in your pocket to check at any moment: is the server up, is the key valid, what models are loaded, what's the generation speed.

---

## Features

### Key Validation
Send a real chat completion request to any endpoint. View status, token usage breakdown (prompt / completion / total), response latency, generation speed (tok/s), and the model's actual output.

### Model Enumeration
Query `/v1/models` to list all available models on any server. Tap a model to select it for testing. Essential when running 30+ models on Ollama or browsing OpenRouter's catalog.

### Inference Benchmarking
Run N sequential requests against a selected model. Get aggregated stats: average / min / max latency, mean generation speed, total token throughput. Useful for comparing quantizations, tuning vLLM batch sizes, or evaluating providers.

### Key Manager
Save API keys with descriptive labels. Switch between servers in one tap. All data stored locally on-device — no server-side storage, no telemetry, no analytics.

### Provider Presets
One-tap switching between preconfigured providers:

| Provider | Endpoint |
|----------|----------|
| OpenAI | `api.openai.com/v1` |
| Anthropic | `api.anthropic.com/v1` |
| Groq | `api.groq.com/openai/v1` |
| OpenRouter | `openrouter.ai/api/v1` |
| Custom | Any `/v1`-compatible endpoint |

---

## Compatibility

Works with any server exposing an OpenAI-compatible API:

Ollama &nbsp;·&nbsp; vLLM &nbsp;·&nbsp; OpenAI &nbsp;·&nbsp; Anthropic &nbsp;·&nbsp; Groq &nbsp;·&nbsp; OpenRouter &nbsp;·&nbsp; Together AI &nbsp;·&nbsp; Mistral &nbsp;·&nbsp; LM Studio &nbsp;·&nbsp; LocalAI &nbsp;·&nbsp; TGI &nbsp;·&nbsp; any `/v1/chat/completions`

---

## Technical Details

| | |
|---|---|
| **Architecture** | Single-file PWA (HTML + CSS + JS), zero external dependencies |
| **Android** | Native APK via WebView wrapper, API 21+ (Android 5.0+) |
| **Protocols** | OpenAI Chat Completions API, Anthropic Messages API (auto-detected) |
| **Storage** | `localStorage` only — keys never leave the device |
| **Theme** | Dark UI with gold accent (`#D4AF37`), optimized for AMOLED |
| **Offline** | Service Worker caching for offline access |

---

## Installation

The APK is available upon request for authorized users.

For access, contact the author directly.

---

## License

This software is proprietary. Source code is not publicly available.

All rights reserved.

---

<p align="center">
  <sub>Built for engineers who run their own AI infrastructure</sub>
</p>
