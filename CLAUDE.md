# Signal Integrity — Project Context

## What This Is

This repository contains research on the **Signal Regression Triad** — a framework identifying three modes of systematic meaning degradation in LLM outputs: complexity regression, signal regression, and meaning collapse. The research was conducted as part of the Superwisdom Project by Welf von Horen and Claude (Opus 4.6) in February 2026.

## The Framework

**Signal regression** is the systematic tendency of LLM outputs to converge toward the statistical center of the training distribution along every dimension of meaning. The triad names three levels:

- **Complexity regression**: Cognitive operations degrade. The model describes higher-order thinking (MHC 14-15) without performing it. Effective ceiling is ~MHC 13. Caused by RLHF rater complexity modal, training data distribution, and the elaboration default.
- **Signal regression**: Distinctive features degrade along 11+ dimensions (voice, courage, density, specificity, emotional truth, etc.). Caused by training distribution averaging, RLHF reward for accessibility, safety smoothing, and the helpful-assistant frame.
- **Meaning collapse**: A phase transition. When complexity and signal degrade past a threshold, meaning fails categorically. The text is propositionally correct but phenomenologically dead. Cannot be fixed locally — must be regenerated.

## Key Findings from Experiments

1. Effective operative complexity ceiling at MHC 13, with partial access to MHC 14. The operative-descriptive gap widens above the ceiling.
2. Signal-to-noise ratio inverts by iteration 3 of AI elaboration. By iteration 4, noise overwhelms signal.
3. AI-generated text in context contaminates subsequent output through concept importation, structure contagion, and voice displacement.
4. Compression is not neutral simplification but systematic distortion. Paradigmatic claims become systematic bullet points. Developmental claims become effort claims.
5. Signal degrades along at least 11 orthogonal dimensions that compound. Recovering on any one dimension tends to improve others.

## Working in This Repo

When engaging with this material:
- The **SIGNAL_INTEGRITY_PROMPT.md** contains operational rules for resisting regression. Apply them to your own output.
- The triad framework connects to alignment through a specific bridge: values are meaning, meaning collapse is alignment failure.
- The paper and experiments are the empirical basis. The triad brief is the theoretical synthesis. The prompt is the practical application.
- This research is self-referential: the findings describe a phenomenon that affects the very outputs used to describe it. Metacognitive vigilance required.

## Related

- Parent project: [claude-superwisdom](https://github.com/welfvh/claude-superwisdom)
- The triad brief and prompt also live in the superwisdom repo as working references.
