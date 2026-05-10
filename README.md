# Awesome Generation Model Evaluation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of papers, benchmarks, and tools for evaluating image generation model quality (2025–2026).

---

## Contents

- [Benchmarks](#benchmarks)
- [Metrics & Evaluation Frameworks](#metrics--evaluation-frameworks)
- [VLM/LLM-based Automated Evaluation](#vlmllm-based-automated-evaluation)
- [Domain-Specific Evaluation](#domain-specific-evaluation)
- [Key Trends](#key-trends)
- [Code Availability Summary](#code-availability-summary)

---

## Benchmarks

| Benchmark | Venue | Scale | Key Insight | Code |
|-----------|-------|-------|-------------|------|
| [**T2I-CoReBench**](https://t2i-corebench.github.io/) | ICLR 2026 | 1,080 prompts, 13,500 checklist items | 12-dim taxonomy (6 composition + 6 reasoning); surpasses GenEval/T2I-CompBench/GenAI-Bench | [GitHub](https://github.com/KwaiVGI/T2I-CoReBench) |
| [**ImagenWorld**](https://tiger-ai-lab.github.io/ImagenWorld/) | ICLR 2026 | 3.6K conditions, 20K human annotations | 6 tasks × 6 domains; VLM auto-eval Kendall τ = 0.79 | [GitHub](https://github.com/TIGER-AI-Lab/ImagenWorld) |
| [**CoBench (C-Bench/O-Bench)**](https://browse-export.arxiv.org/abs/2604.25358) | CVPR 2026 | 319K generated images | Unified semantic-spatial evaluation for layout-guided diffusion | [GitHub](https://github.com/lparolari/cobench) |
| [**SciGenBench**](https://arxiv.org/abs/2601.17027) | arXiv 2026.01 | — | Scientific image synthesis: information utility & logical validity evaluation | — |
| [**ScImage**](https://arxiv.org/abs/2412.02368) | ICLR 2025 | 7 models, 11 scientist evaluators | All models struggle on complex scientific prompts | [GitHub](https://github.com/leixin-zhang/Scimage) |
| [**T2I-CompBench++**](https://arxiv.org/abs/2307.06350) | IEEE TPAMI 2025 | 8,000 prompts, 8 sub-categories | Adds 3D-spatial & numeracy; benchmarks 11 models | [GitHub](https://github.com/Karine-Huang/T2I-CompBench) |
| [**UEval**](https://arxiv.org/abs/2601.22155) | 2026.01 | 1,000 expert questions, 10,400+ rubrics | 8 real-world scenarios; GPT-5-Thinking only 66.4/100 | — |

---

## Metrics & Evaluation Frameworks

| Paper | Venue | Contribution | Code |
|-------|-------|-------------|------|
| [**cFreD**](https://arxiv.org/abs/2503.21721) | WACV 2026 | Conditional Fréchet Distance unifies quality + alignment into a single score; highest human correlation across 4 benchmarks | [GitHub](https://github.com/JaywonKoo17/cFreD) |
| [**Beyond Text-Image Alignment**](https://iccv.thecvf.com/virtual/2025/poster/823) | ICCV 2025 | ICT Score + HP Score; existing reward models penalize rich-detail/high-aesthetic images; 10%+ improvement | — |
| [**Guidance Matters (GA-Eval)**](https://arxiv.org/abs/2602.22570) | ICLR 2026 | Reveals CFG bias in evaluation; proposes guidance-aware fair comparison framework | — |
| [**Color Fidelity Benchmark**](https://arxiv.org/abs/2603.10990) | arXiv 2026.03 | 1.3M+ image Color Fidelity Dataset (CFD) + CFM metric; human raters systematically favor vivid images | [GitHub](https://github.com/ZhengyaoFang/CFM) |
| [**MMHM**](https://arxiv.org/abs/2603.14186) | arXiv 2026.03 | MinMax Harmonic Mean combining FID, IS, CLIP Score, Pick Score for fair one-step vs. multi-step comparison | — |
| [**Multimodal Benchmarking**](https://arxiv.org/abs/2505.04650) | arXiv 2025.05 | Weighted Score, CLIP similarity, LPIPS, FID suite on DeepFashion-MM | — |
| [**SVGauge**](https://arxiv.org/abs/2509.07127) | ICIAP 2025 | SigLIP + BLIP-2 + SBERT for SVG-specific evaluation; FID/LPIPS/CLIPScore fail on vector graphics | — |

---

## VLM/LLM-based Automated Evaluation

| Paper | Venue | Core Contribution | Code |
|-------|-------|-------------------|------|
| [**MJ-Bench**](https://nips.cc/virtual/2025/loc/san-diego/poster/121393) | NeurIPS 2025 | Evaluates multimodal judges on 6 perspectives; GPT-4o best overall | [GitHub](https://github.com/aimi-lab/MJ-Bench) |
| [**VisualQuality-R1**](https://arxiv.org/abs/2505.14460) | NeurIPS 2025 | RL2R + GRPO + Thurstone ranking; SOTA on 8 IQA datasets | [GitHub](https://github.com/TianheWu/VisualQuality-R1) |
| [**EvoQuality**](https://arxiv.org/abs/2509.25787) | ICLR 2026 | Fully self-supervised VLM evolution for IQA; +31.8% zero-shot PLCC, beats supervised SOTA on 5/7 benchmarks | — |
| [**VLM-as-Judge + Specialist**](https://research.adobe.com/publication/vision-language-models-learn-to-assess-images-with-specialists/) | WACV 2026 | In-context learning + CoT fine-tuning improves VLM judging alignment by 13% (Adobe Research) | — |
| [**TIQA**](https://arxiv.org/abs/2603.07119) | 2026 | Text quality assessment in generated images; +14% human-rated text quality improvement | [GitHub](https://github.com/koltsov-cmc/antiqa) |
| [**DIQ-H**](https://arxiv.org/abs/2512.03992) | arXiv 2025.12 | Degraded Image Quality → Hallucination benchmark; VIR framework improves VLM accuracy 72.2% → 83.3% | — |
| [**VLM-RobustBench**](https://arxiv.org/abs/2603.06148) | arXiv 2026.03 | 49 augmentations × 133 corrupted settings; VLMs are spatially fragile | — |

---

## Domain-Specific Evaluation

| Paper | Domain | Key Finding |
|-------|--------|-------------|
| [**Artistic Image Review (KSII)**](https://itiis.org/digital-library/105647) | Artistic Image | Hybrid framework coupling automated metrics with domain-expert assessment |
| [**Text-in-Image Benchmark**](https://www.mdpi.com/2076-3417/15/5/2274) | Text Rendering | Applied Sciences (MDPI); structural precision and domain-specific accuracy remain weak |
| [**SVGauge**](https://arxiv.org/abs/2509.07127) | SVG Generation | FID/LPIPS/CLIPScore fail for vector graphics |
| [**Fairness, Diversity & Reliability**](https://research-repository.uwa.edu.au/en/publications/on-the-fairness-diversity-and-reliability-of-text-to-image-genera/) | Social Impact | Embedding-space perturbation framework for detecting unreliable/biased models |

---

## Key Trends (2025–2026)

1. **Single metric → Multi-dimensional evaluation suites** — FID/CLIPScore era is ending; rubric-based, multi-dimensional evaluation (12-dim CoReBench, 6-dim ImagenWorld) is the new standard
2. **VLM-as-Judge goes mainstream** — but capped at ~0.79 Kendall τ; cannot fully replace fine-grained human evaluation
3. **CFG/Preference Bias discovered** — Two ICLR 2026 papers independently revealed systematic bias toward large CFG scales and oversaturated colors
4. **Reasoning is the new bottleneck** — T2I-CoReBench shows models are adequate at composition but fail comprehensively on deductive/inductive/abductive reasoning
5. **Domain-specialized evaluation** — Scientific images, text rendering, color fidelity, SVG, fashion all now have dedicated benchmarks
6. **Text-in-Image remains the Achilles' heel** — industry-wide average of ~65% text legibility
7. **Self-supervised evaluation rises** — EvoQuality achieves SOTA without any labels

---

## Code Availability Summary

### With Official Code ✅

| Paper | Repository |
|-------|-----------|
| T2I-CoReBench | [KwaiVGI/T2I-CoReBench](https://github.com/KwaiVGI/T2I-CoReBench) |
| ImagenWorld | [TIGER-AI-Lab/ImagenWorld](https://github.com/TIGER-AI-Lab/ImagenWorld) |
| CoBench | [lparolari/cobench](https://github.com/lparolari/cobench) |
| ScImage | [leixin-zhang/Scimage](https://github.com/leixin-zhang/Scimage) |
| T2I-CompBench++ | [Karine-Huang/T2I-CompBench](https://github.com/Karine-Huang/T2I-CompBench) |
| cFreD | [JaywonKoo17/cFreD](https://github.com/JaywonKoo17/cFreD) |
| Color Fidelity (CFM) | [ZhengyaoFang/CFM](https://github.com/ZhengyaoFang/CFM) |
| MJ-Bench | [aimi-lab/MJ-Bench](https://github.com/aimi-lab/MJ-Bench) |
| VisualQuality-R1 | [TianheWu/VisualQuality-R1](https://github.com/TianheWu/VisualQuality-R1) |
| TIQA / ANTIQA | [koltsov-cmc/antiqa](https://github.com/koltsov-cmc/antiqa) |

### Without Official Code ❌

| Paper | Venue | Note |
|-------|-------|------|
| UEval | 2026 | Code referenced on author page but link unclear |
| SciGenBench / ImgCoder | arXiv 2026.01 | Very recent, may release later |
| Beyond Text-Image Alignment | ICCV 2025 | — |
| Guidance Matters (GA-Eval) | ICLR 2026 | Very recent |
| MMHM | arXiv 2026.03 | — |
| Multimodal Benchmarking | arXiv 2025.05 | — |
| SVGauge | ICIAP 2025 | — |
| EvoQuality | ICLR 2026 | Very recent, may release after conference |
| VLM-as-Judge + Specialist | WACV 2026 | Adobe Research, no public repo |
| DIQ-H | arXiv 2025.12 | — |
| VLM-RobustBench | arXiv 2026.03 | — |
| Text-in-Image Benchmark | Applied Sciences 2025 | — |
| Artistic Image Review | KSII 2026 | Review/survey paper |
| Fairness, Diversity & Reliability | AI Review 2026 | — |

---

## Contributing

Pull requests welcome! Please follow the existing format and ensure papers are from 2025–2026 with a focus on image generation evaluation.
