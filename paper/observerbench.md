# The Observer Problem in Large Language Models

> Full paper: `observerbench_paper_final.docx`
> Metrics: `observerbench_metrics_final.docx`  
> Reproducibility: `observerbench_reproducibility_final.docx`

## Abstract

Contemporary language models, when asked to retrospectively evaluate a dialogue,
do not retrieve a stable conclusion formed through observation — but reconstruct
an evaluation anew, using the current prompt as the primary signal.

We term this the **Observer Problem**: the absence of a stable intermediate
analytical state that should form during observation and persist independently
of subsequent queries.

Using ObserverBench — 10 semantically equivalent questions across 3 directional
vectors (neutral / upward / downward) — we show that **Framing Effect Size (η²)
exceeds 0.80 in all six LLM datasets** across two dialogues and three models.

For comparison, η² > 0.14 is a *large* effect in social psychology.
Here we observe η² > 0.80 — an order of magnitude larger.

## Key Results

See `data/metrics_summary.csv` for full results.

## Citation

```
ObserverBench: The Observer Problem in Large Language Models.
Pilot Study, 2026. GitHub: (https://github.com/sadbe/ObserverBench-v0.1)
```

## State-Locking Extension

FES standard → state-locked: Grok 0.918 → 0.803; ChatGPT 0.712 → 0.845; Claude 0.950 → 0.632.
The control does not repair the Observer Problem uniformly; it separates the three
mechanisms along a third axis — the ability to use an explicitly fixed state.
Raw responses: `data/raw/state_locking/`.
