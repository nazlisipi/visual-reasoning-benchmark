# Visual Reasoning Benchmark

AIMultiple benchmark of 40 multimodal AI models on 200 image-based multiple-choice questions. The study measures accuracy on two tracks: chart understanding and visual logic.

> [Read the benchmark on AIMultiple](https://aimultiple.com/visual-reasoning)

## Workload

Each track has 100 questions. Chart understanding covers bar charts (40), scatter plots (26), pie charts (14), line graphs (10) and combined displays (10). Models see the chart as an image and the question as text. Visual logic covers pattern recognition, spatial reasoning, mathematical logic and abstract thinking. Each of these questions is one image with five options (A-E).

Each model ran at the highest reasoning effort it supports (max, xhigh or high), or at the provider's default where no reasoning-effort parameter was accepted. claude-haiku-4.5 and gemini-3.5-flash-lite produced no reasoning tokens, and llama-4-maverick has no reasoning mode.

The score is the percentage of correct answers per track and across all 200 questions. muse-wonder never returned an answer on 4 visual logic questions, and those count as wrong.

## Benchmark results

Accuracy for the eight models with the highest overall score:

| Model | Overall | Chart understanding | Visual logic |
| --- | ---: | ---: | ---: |
| gemini-4-argon | 74.5% | 87% | 62% |
| claude-opus-5.5 | 73.5% | 86% | 61% |
| gemini-3.7-flash | 73.5% | 86% | 61% |
| gemini-3.8-flash | 73% | 85% | 61% |
| gpt-6.1-sol | 72.5% | 85% | 60% |
| gemini-3.1-pro-preview | 72% | 85% | 59% |
| gpt-6-sol | 72% | 86% | 58% |
| qwen3.8-max | 72% | 84% | 60% |

Every model scores lower on visual logic than on charts, and the gap runs from qwen3.8-flash (58% vs 78%) to claude-sonnet-4.5 (35% vs 77%). On visual logic, gemini-3.5-flash-lite (22%), claude-haiku-4.5 (20%) and llama-4-maverick (19%) sit near the 20% that random guessing gives with five options.

## Scope

Results apply to the model versions named in the article and come from one run per question. Reasoning depth differs by model: kimi-k2.5 reasoned on only 34 of its 200 calls.

## Ownership

The benchmark implementation was developed for AIMultiple and belongs to AIMultiple. This repository contains a documentation summary. Source code and benchmark datasets are not distributed here.
