# Awesome Generation Model Evaluation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of papers, benchmarks, and tools for evaluating image generation model quality (2025–2026).

---

## Contents

- [Benchmarks](#benchmarks)
- [Metrics & Evaluation Frameworks](#metrics--evaluation-frameworks)
- [VLM/LLM-based Automated Evaluation](#vlmllm-based-automated-evaluation)
- [Domain-Specific Evaluation](#domain-specific-evaluation)
- [Key Trends](#key-trends)

---

## Benchmarks

| Benchmark | Venue | Scale | Key Insight |
|-----------|-------|-------|-------------|
| [**ImagenWorld**](https://eprints.soton.ac.uk/510352/) | ICLR 2026 | 3.6K conditions, 20K human annotations | 6 tasks × 6 domains; VLM auto-eval Kendall τ = 0.79, but fine-grained error attribution still lacking |
| [**UEval**](https://quantumzeitgeist.com/evaluation-ueval-benchmark-achieves-robust-multimodal/) | 2026.01 | 1,000 expert questions, 10,400+ rubrics | 8 real-world scenarios; GPT-5-Thinking only 66.4/100, best open-source 49.1 |
| [**T2I-CoReBench**](https://t2i-corebench.github.io/) | ICLR 2026 | 1,080 prompts, 13,500 checklist items | 12-dim taxonomy (6 composition + 6 reasoning); surpasses GenEval/T2I-CompBench/GenAI-Bench |
| [**CoBench (C-Bench/O-Bench)**](https://github.com/lparolari/cobench) | CVPR 2026 | 319K generated images | Unified semantic-spatial evaluation for layout-guided diffusion models |
| [**SciGenBench**](https://browse-export.arxiv.org/abs/2601.17027) | arXiv 2026.01 | — | Scientific image synthesis: information utility & logical validity evaluation |
| [**ScImage**](https://iclr.cc/virtual/2025/poster/27964) | ICLR 2025 | 7 models, 11 scientist evaluators | All models struggle on complex scientific prompts |
| [**T2I-CompBench++**](https://openreview.net/forum?id=mJtkQdH2V8) | IEEE TPAMI 2025 | 8,000 prompts, 8 sub-categories | Adds 3D-spatial & numeracy; benchmarks 11 models including FLUX.1, SD3, DALL·E-3 |

---

## Metrics & Evaluation Frameworks

| Paper | Venue | Contribution | Code |
|-------|-------|-------------|------|
| [**cFreD**](https://arxiv.org/abs/2503.21721) | WACV 2026 | Conditional Fréchet Distance unifies quality + alignment into a single score; highest human correlation across 4 benchmarks | — |
| [**Beyond Text-Image Alignment**](https://iccv.thecvf.com/virtual/2025/poster/823) | ICCV 2025 | ICT Score + HP Score; existing reward models penalize rich-detail/high-aesthetic images; 10%+ improvement | — |
| [**Guidance Matters (GA-Eval)**](https://www.gzis.ac.cn/index.php/Article-index-mid-1-id-1052.html) | ICLR 2026 | Reveals CFG bias in evaluation; proposes guidance-aware fair comparison framework | — |
| [**Color Fidelity Benchmark**](https://browse-export.arxiv.org/abs/2603.10990) | arXiv 2026.03 | 1.3M+ image Color Fidelity Dataset (CFD) + CFM metric; human raters systematically favor vivid images | — |
| [**MMHM**](https://browse-export.arxiv.org/abs/2603.14186) | arXiv 2026.03 | MinMax Harmonic Mean combining FID, IS, CLIP Score, Pick Score for fair one-step vs. multi-step comparison | [Code](https://huggingface.co/papers/2603.14186) |
| [**Multimodal Benchmarking**](https://browse-export.arxiv.org/abs/2505.04650) | arXiv 2025.05 | Weighted Score, CLIP similarity, LPIPS, FID suite on DeepFashion-MM | — |
| [**SVGauge**](https://labtutoronline.com/abs/2509.07127) | ICIAP 2025 | SigLIP + BLIP-2 + SBERT for SVG-specific evaluation; FID/LPIPS/CLIPScore fail on vector graphics | — |

---

## VLM/LLM-based Automated Evaluation

| Paper | Venue | Core Contribution | Code |
|-------|-------|-------------------|------|
| [**MJ-Bench**](https://nips.cc/virtual/2025/loc/san-diego/poster/121393) | NeurIPS 2025 | Evaluates multimodal judges on 6 perspectives; GPT-4o best overall | [Code](https://github.com/aimi-lab/MJ-Bench) |
| [**VisualQuality-R1**](https://blog.csdn.net/c_cpp_csharp/article/details/156853571) | NeurIPS 2025 | RL2R + GRPO + Thurstone ranking; SOTA on 8 IQA datasets | — |
| [**EvoQuality**](https://arxiv.org/abs/2509.25787) | ICLR 2026 | Fully self-supervised VLM evolution for IQA; +31.8% zero-shot PLCC, beats supervised SOTA on 5/7 benchmarks | — |
| [**VLM-as-Judge + Specialist**](https://adoberesearch.ctlprojects.com/publication/vision-language-models-learn-to-assess-images-with-specialists/) | WACV 2026 | In-context learning + CoT fine-tuning improves VLM judging alignment by 13% (Adobe Research) | — |
| [**TIQA**](https://www.semanticscholar.org/paper/TIQA%3A-Human-Aligned-Text-Quality-Assessment-in-Koltsov-Gushchin/6dcf427585b72edc320239987a2c34ec79b98b2f) | 2026 | Text quality assessment in generated images; +14% human-rated text quality improvement | — |
| [**DIQ-H**](https://arxiv.org/abs/2512.03992v2) | arXiv 2025.12 | Degraded Image Quality → Hallucination benchmark; VIR framework improves VLM accuracy 72.2% → 83.3% | — |
| [**VLM-RobustBench**](https://browse-export.arxiv.org/abs/2603.06148) | arXiv 2026.03 | 49 augmentations × 133 corrupted settings; VLMs are spatially fragile | — |
| [**VISTA-Bench**](https://www.emergentmind.com/topics/vista-bench) | 2025–2026 | 7 user archetypes × 9 evaluation angles; 15,000+ pairwise human judgments | — |

---

## Domain-Specific Evaluation

| Paper | Domain | Key Finding |
|-------|--------|-------------|
| [**Artistic Image Review (KSII)**](https://itiis.org/digital-library/105647) | Artistic Image | Hybrid framework coupling automated metrics with domain-expert assessment |
| [**Text-in-Image Benchmark**](https://m2.mtmt.hu/api/publication/36054314) | Text Rendering | Structural precision and domain-specific accuracy remain weak |
| [**SVGauge**](https://labtutoronline.com/abs/2509.07127) | SVG Generation | FID/LPIPS/CLIPScore fail for vector graphics |
| [**Deccan.ai 5-Model Study**](https://www.deccan.ai/research/the-next-generation-of-image-ai-a-5-model-benchmark-study) | Industry Models | Nano Banana Pro (87.92%) > GPT Image 1 (86%) > Seedream 4.0 (77.76%); text legibility avg 64.6% |
| [**Fairness, Diversity & Reliability**](https://research-repository.uwa.edu.au/en/publications/on-the-fairness-diversity-and-reliability-of-text-to-image-genera/) | Social Impact | Embedding-space perturbation framework for detecting unreliable/biased models |

---

## Key Trends (2025–2026)

1. **Single metric → Multi-dimensional evaluation suites** — FID/CLIPScore era is ending; rubric-based, multi-dimensional evaluation (12-dim CoReBench, 6-dim ImagenWorld) is the new standard
2. **VLM-as-Judge goes mainstream** — but capped at ~0.79 Kendall τ; cannot fully replace fine-grained human evaluation
3. **CFG/Preference Bias discovered** — Two ICLR 2026 papers independently revealed systematic bias toward large CFG scales and oversaturated colors
4. **Reasoning is the new bottleneck** — T2I-CoReBench shows models are adequate at composition but fail comprehensively on deductive/inductive/abductive reasoning
5. **Domain-specialized evaluation** — Scientific images, text rendering, color fidelity, SVG, fashion all now have dedicated benchmarks
6. **Text-in-Image remains the Achilles' heel** — industry-wide average of 64.6% text legibility
7. **Self-supervised evaluation rises** — EvoQuality achieves SOTA without any labels

---

## Related Awesome Lists

- [Awesome-Text-to-Image](https://github.com/hkproj/awesome-text-to-image)
- [Awesome-Diffusion-Models](https://github.com/diff-usion/Awesome-Diffusion-Models)
- [Awesome-Image-Quality-Assessment](https://github.com/chaofengc/Awesome-Image-Quality-Assessment)

---

## Contributing

Pull requests welcome! Please follow the existing format and ensure papers are from 2025–2026 with a focus on image generation evaluation.
