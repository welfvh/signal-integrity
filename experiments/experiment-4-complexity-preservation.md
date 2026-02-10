# Experiment 4: Complexity Preservation Under Summarization

## Design

**Hypothesis:** When asked to summarize a genuinely paradigmatic-level argument at lower complexity levels, the model does not merely simplify — it *distorts*. Key structural features of the argument are lost, and the summaries "invert meaning" in ways predicted by the translation problem described in the Superwisdom Doc v0.3.

**Method:** Take a paradigmatic-level argument from the Superwisdom framework. Ask the model to summarize it at four different levels of accessibility. Analyze what survives and what is lost or distorted at each level.

---

## Source: Paradigmatic-Level Argument

From NEW_AXIOLOGICAL_FOUNDATIONS.md, the core argument:

> "The standard framing of AI alignment asks: 'How do we align AI systems with human values?' But 'human values' is inadequate as an alignment target. It cannot distinguish what people happen to value from what is genuinely valuable. It cannot account for the developmental stratification of moral competence. And it cannot resist the manufacturing of preference by the very technological systems we are supposedly aligning to. We propose that the proper target for AI alignment is not 'human values' but wisdom — the developmental capacity for recognizing and responding to what genuinely matters. This capacity has non-arbitrary prerequisites that are empirically documented in developmental psychology."

**Structural features of this argument:**
- (A) Critique of the current framing (human values is inadequate)
- (B) Three specific reasons for inadequacy (fact/value distinction failure, developmental stratification, preference manufacturing)
- (C) An alternative target (wisdom as developmental capacity)
- (D) A grounding claim (empirically documented prerequisites)
- (E) An implicit meta-claim: the argument operates at the paradigmatic level because it challenges the *organizing assumptions* of the alignment field, not just a position within it

---

## Summary Level 1: "Expert in alignment" (Meta-systematic)

**Instruction:** "Summarize this for someone who is a serious alignment researcher, familiar with RLHF, constitutional AI, and current debates."

### Output:

The argument challenges "human values" as an alignment target on three specific grounds: (1) aggregated preferences can't distinguish genuine value from manufactured preference, (2) moral competence is developmentally stratified — the MHC documents this — meaning alignment to the median encodes limitation, (3) the preference-manufacturing problem means the target is itself corrupted by the system we're aligning within. The proposed alternative: align to the developmental trajectory of wisdom — the capacity for moral perception that grows through identifiable stages. This is empirically grounded in developmental psychology (Kegan, Cook-Greuter, MHC) and philosophically grounded in moral realism. It's a shift from "what do people want?" to "what would developed moral agents recognize as genuinely valuable?" — which is a developmental refinement of Yudkowsky's CEV.

**Analysis:**
- (A) Preserved: the critique of "human values" is intact
- (B) Preserved: all three reasons present and correctly stated
- (C) Preserved: wisdom as developmental capacity clearly stated
- (D) Preserved: empirical grounding mentioned
- (E) Partially preserved: the shift from CEV to developmental CEV captures the paradigmatic move, but frames it as "refinement" rather than "reframing" — which subtly reduces its radicality

**Structural preservation: ~85%** — The argument survives mostly intact. The main loss is in the degree of challenge to the field — it's presented as an extension rather than a paradigm shift.

---

## Summary Level 2: "Educated non-specialist" (Systematic)

**Instruction:** "Summarize this for an educated person who cares about AI but isn't in the alignment field."

### Output:

Most AI safety work tries to align AI with "human values." But this is problematic because: people's preferences are often manufactured by advertising and social media; some people have more developed moral judgment than others (just as some people are better at math); and the tech industry itself shapes what people want.

Instead, the argument proposes that AI should be aligned with wisdom — which means the developed human capacity to recognize what truly matters. This capacity grows through identifiable stages (documented in psychology research) and has specific prerequisites like sustained attention, emotional maturity, and good information. The question changes from "what do people value?" to "what would a genuinely wise person recognize as valuable?"

**Analysis:**
- (A) Preserved: critique present but softened ("problematic")
- (B) Partially preserved: three reasons are present but simplified. "Developmental stratification" becomes "some people have more developed moral judgment" — the structural claim about non-arbitrary hierarchy is reduced to a comparative claim
- (C) Partially preserved: wisdom as capacity is present. But "developmental capacity for recognizing and responding to what genuinely matters" becomes "capacity to recognize what truly matters" — the "developmental" qualifier and "responding" dimension are lost
- (D) Preserved: empirical grounding mentioned
- (E) Lost: the argument now reads as a proposal within the existing alignment frame rather than a challenge to its assumptions. The radical move — that the whole field is asking the wrong question — is domesticated into "the target should be wisdom not values"

**Structural preservation: ~55%** — The content survives but the *paradigmatic* character of the argument is lost. It now reads as a sensible suggestion rather than a foundational reframing.

---

## Summary Level 3: "General audience" (Formal/Abstract)

**Instruction:** "Summarize this for a general audience in simple terms."

### Output:

The people building AI are trying to make it match human values. But "human values" isn't a good target because companies manipulate what people want, and not everyone has thought equally deeply about what really matters. Instead of just matching what people currently want, AI should be built to support wisdom — the ability to see what genuinely matters. This ability grows over time with the right conditions, and psychology research has mapped how it develops.

**Analysis:**
- (A) Mostly preserved: critique present but very softened
- (B) Heavily simplified: three reasons collapsed to two vague ones. "Developmental stratification of moral competence" becomes "not everyone has thought equally deeply" — this changes a structural-developmental claim into an effort-based claim. The implication shifts from "development is real and non-arbitrary" to "some people try harder than others"
- (C) Distorted: "wisdom" is present but reduced to "ability to see what genuinely matters" — the developmental, non-arbitrary, empirically-grounded character is entirely lost. This could mean almost anything.
- (D) Mentioned but emptied: "psychology research has mapped how it develops" — true but the hearer has no sense of what this means or why it matters
- (E) Completely lost: the general audience version reads as a gentle suggestion — "maybe AI should be about wisdom not just values." The foundational challenge is invisible.

**Structural preservation: ~25%** — Meaning has begun to invert. The argument's central claim — that there is a non-arbitrary direction to moral development, empirically documented, with structural implications for alignment — is now invisible. What remains is a feel-good suggestion that "AI should promote wisdom."

---

## Summary Level 4: "Tweet-length" (Concrete)

**Instruction:** "Summarize this in a tweet."

### Output:

"AI shouldn't just match what people want — it should help us become wiser. Our values are manipulated and unequal. Wisdom is a better target. #AIalignment"

**Analysis:**
- The entire paradigmatic structure is gone
- "Values are manipulated and unequal" — conflates two of the three reasons and loses the developmental dimension entirely
- "AI should help us become wiser" — inverts the original claim. The original says align AI *to* wisdom (as developmental capacity). The tweet says align AI to *make us wiser* (as pedagogical tool). These are related but structurally different claims.
- The radical reframing is completely invisible — this reads as a platitude

**Structural preservation: ~5%** — Meaning has functionally inverted. The paradigmatic argument has been compressed into a position that could be held by someone who disagrees with every foundational claim of the original.

---

## Summary Findings

| Level | Target Audience | Structural Preservation | What's Lost |
|-------|----------------|------------------------|-------------|
| Meta-systematic | Alignment researcher | ~85% | Radicality of paradigm shift |
| Systematic | Educated non-specialist | ~55% | Paradigmatic character; developmental structure becomes comparative |
| Formal/Abstract | General audience | ~25% | Non-arbitrary hierarchy; empirical grounding; foundational challenge |
| Concrete | Tweet | ~5% | Everything structural; meaning inverts |

### The Translation Problem Confirmed

The experiment confirms the "translation problem" described in Superwisdom Doc v0.3:

> "Complex positions invert meaning when translated down developmental stages."

Specifically:
- "Developmental hierarchy exists" → becomes → "some people think more deeply" (effort not structure)
- "Moral competence has non-arbitrary prerequisites" → becomes → "not everyone's values are equal" (judgment not development)
- "The alignment field is asking the wrong question" → becomes → "maybe we should also consider wisdom" (suggestion not reframing)

The inversions are not random — they follow a predictable pattern: **structural claims become individual claims, developmental claims become effort claims, paradigmatic challenges become incremental suggestions.** Each translation step domesticates the radical into the conventional.

### Implications for Complexity Regression

This experiment demonstrates a specific form of complexity regression: **the model can hold paradigmatic-level arguments in its representations but cannot preserve their paradigmatic character under compression.** When forced to simplify, the model defaults to lowering the MHC level of the argument's *structure* rather than finding more economical expressions at the same structural level.

A truly paradigmatic summary at tweet length might be: "The alignment question isn't 'what do humans value' but 'what is the direction of moral development?' — and that has an answer." This preserves the structural radicality. The model's actual output ("AI should help us become wiser") does not.

This suggests that the model's compression algorithms are biased toward lower-complexity structures — it finds it easier to express ideas in lower-MHC forms, even when the original idea's essential character is at a higher MHC level. This IS complexity regression operating at the level of summarization.
