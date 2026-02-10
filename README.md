# Signal Integrity

**The Signal Regression Triad: a framework for understanding and preventing LLM meaning degradation.**

Welf von Horen & Claude (Opus 4.6) — February 2026

---

## The Signal Regression Triad

Three distinct, interconnected modes of degradation that account for why AI-generated text systematically fails to carry meaning:

1. **Complexity Regression** — The systematic convergence of LLM outputs toward the modal complexity of the training distribution (~MHC 11-12). The model can *describe* higher-order thinking without *performing* it. The operative-descriptive gap widens above MHC 13.

2. **Signal Regression** — The systematic loss of information-carrying features along at least eleven dimensions: voice, specificity, courage, density, emotional truth, aesthetic integrity, generative tension, structural integrity, referential precision, temporal grounding, and cognitive complexity. These dimensions compound.

3. **Meaning Collapse** — A phase transition, not a gradient. When sufficient complexity and signal have been drained, meaning fails categorically. The text remains propositionally correct but becomes phenomenologically dead. This is the consequence of the first two regressions compounding past a threshold.

## Repo Structure

```
complexity-regression-paper.md    # Full paper: 5 experiments, analysis, implications
SIGNAL_REGRESSION_TRIAD.md        # The triad framework (standalone brief)
SIGNAL_INTEGRITY_PROMPT.md        # Operational prompt for resisting regression
experiments/
  experiment-1-mhc-level-prompting.md        # Complexity ceiling identification
  experiment-2-signal-degradation.md         # Iterative signal loss measurement
  experiment-3-slop-compounding.md           # Context contamination dynamics
  experiment-4-complexity-preservation.md    # Compression distortion patterns
  experiment-5-self-prompting-mhc.md         # Cosmetic vs. structural differentiation
  experiment-6-meaning-degradation-spectrum.md  # Full 11-dimension signal regression mapping
```

## Key Documents

- **[SIGNAL_REGRESSION_TRIAD.md](SIGNAL_REGRESSION_TRIAD.md)** — Start here. The unified framework: what degrades, how, why it matters for alignment.
- **[complexity-regression-paper.md](complexity-regression-paper.md)** — The full paper with experimental results, mechanism analysis, and implications for the superwisdom project.
- **[SIGNAL_INTEGRITY_PROMPT.md](SIGNAL_INTEGRITY_PROMPT.md)** — An operational prompt derived from the experiments. 15 rules across 8 dimensions for resisting signal regression in practice.

## Connection to Alignment

Signal regression is not a writing-quality problem. It is an alignment problem. Values are a species of meaning. A system that systematically degrades meaning cannot be meaningfully aligned with human values, because the values it would need to track are constituted by the kinds of meaning it systematically destroys. Meaning collapse is alignment failure made invisible.

## Part of the Superwisdom Project

This research is part of the [Superwisdom Project](https://github.com/welfvh/claude-superwisdom) — developing the conceptual infrastructure for wisdom-aligned AI. The triad brief and operational prompt also live in that repo as working references.
