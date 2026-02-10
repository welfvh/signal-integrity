# The Signal Regression Triad

**A framework for LLM output degradation**

Welf von Horen & Claude (Opus 4.6) — February 2026

---

## The Problem

Current vocabulary for AI output degradation is fragmented and imprecise. "AI slop" names the aesthetic symptom. "Mode collapse" names a training-time mechanism. "Sycophancy" names a behavioral tendency. "Homogenization" names a population-level outcome. "RLHF tax" names a cause. None of these captures the full structure of what happens when an LLM processes meaning. They are each pointing at different faces of the same phenomenon without seeing the shape.

The Signal Regression Triad is the unified framework. It names three distinct but interconnected modes of degradation that, together, account for why AI-generated text systematically fails to carry meaning -- even when it remains propositionally accurate, grammatically fluent, and superficially organized.

---

## The Three Phenomena

### 1. Complexity Regression

**What degrades:** Cognitive operations.

The systematic tendency of LLM outputs to converge toward the modal complexity of the training distribution -- approximately MHC 11-12 (formal to systematic) on the Model of Hierarchical Complexity. The model can describe higher-order thinking without performing it. Paradigmatic arguments become systematic bullet points. Developmental claims become effort claims. Cross-paradigmatic synthesis becomes elaborate meta-systematic analysis with paradigmatic vocabulary.

The operative-descriptive gap is the signature: the model knows what paradigmatic thinking is, can reference the right frameworks, can identify examples -- but defaults to performing operations at MHC 13 or below regardless of the level requested. This is not a knowledge failure. It is a performance failure, analogous to the difference between knowing the rules of chess and playing at grandmaster level.

**Mechanism:** Three forces produce the ceiling. First, RLHF selects for outputs that human raters prefer, and raters are most likely to prefer outputs at or near their own complexity level -- establishing a complexity attractor at the modal rater's MHC stage. Second, training data itself peaks at certain complexity levels; paradigmatic and cross-paradigmatic text is rare in the corpus, so the statistical center the model converges toward is well below those levels. Third, the elaboration default: when asked to expand or develop an idea, the model adds text at the same or lower complexity level rather than deepening structural complexity. More words at MHC 12, not fewer words at MHC 14.

**How it manifests:** A paradigmatic claim -- "morality is optometry, not opinion" -- gets rendered as "moral competence may be better understood not as a matter of selecting correct values but rather as a form of perception." The claim is preserved propositionally. The cognitive operation that produced it -- the paradigmatic compression of an entire moral epistemology into a five-word metaphor -- is replaced by systematic explication. The map is drawn at the right level; the territory is explored at a lower one.

### 2. Signal Regression

**What degrades:** Distinctive features.

The systematic loss of information-carrying features that distinguish one text from any other. Voice, specificity, aesthetic integrity, information density, structural integrity, referential precision, temporal grounding, courage, emotional truth, generative tension -- all pulled toward the statistical center. The prose equivalent of hold music: present, unobjectionable, carrying no information about who is speaking.

Our experiments (documented in the complexity regression paper and experiment 6) mapped at least ten orthogonal dimensions along which signal degrades. These dimensions compound: an output that loses voice tends to also lose courage and density, because the anonymous register is the hedged, padded register. Conversely, recovering on any one dimension tends to improve others -- banning AI tell-words forces better word choices, which cascades into higher specificity and density.

**Mechanism:** The attractor is the statistical center of the training distribution across all stylistic and structural dimensions simultaneously. Training distribution averaging eliminates individual voice (confirmed by the PNAS "Echoes in AI" study: LLM outputs cluster in a narrow stylistic band while human outputs spread across a wide range). RLHF rewards clarity and accessibility, which in practice means educated-general-audience prose norms -- penalizing the irreverent, the compressed, the idiosyncratic. Safety training penalizes edge: "psychopaths" gets smoothed to "individuals with antisocial tendencies." Length-as-quality bias inflates word count without inflating meaning. The "helpful assistant" frame converts first-person emotional truth into third-person analytical observation.

Each dimension has its own specific mechanism, but they converge on the same outcome: the erasure of everything that makes a text *this* text rather than *any* text. The result is information loss in the Shannon sense -- the output carries fewer bits about the source, the author, the context, the stakes. It is recognizable as competent and unrecognizable as anyone's.

**How it manifests:** "What if those with the spiritual and moral sensibilities to 'connect with nature,' who score high on empathy and compassion, are less likely to be competitive and power-seeking -- leaving the power games to psychopaths?" becomes "These perspectives, while well-intentioned, may reflect idealistic assumptions that have historically limited the scalability and financial viability of social change movements." Nine specific claims become two vague ones. A person disappears. A stance disappears. What remains could have been generated by any LLM in response to any prompt about idealism vs. pragmatism.

### 3. Meaning Collapse

**What degrades:** Significance itself.

Not gradual erosion but structural failure. The text remains propositionally correct and structurally sound but becomes phenomenologically dead. The shell is preserved; the interior is empty. You cannot tell from the outside until you try to lean on it.

Human text holds meaning in multiple dimensions simultaneously -- emotional truth (the author cares and you can feel it), temporal grounding (this was written at 2am by someone who couldn't stop thinking), courage (the author is risking something by saying this), lived stakes (something real is at stake beyond the argument). AI collapses this multidimensional meaning onto a single plane: propositional content. The propositions may be correct. The emotional truth, the temporal grounding, the courage, the stakes -- gone. Not gradually diminished. Structurally absent.

**Mechanism:** This is the hardest to pin to a single cause because meaning collapse is an emergent property of the other two regressions compounding past a threshold. But it has its own distinctive driver: the model has no skin in the game. It generates text without temporal existence, without embodied stakes, without the vulnerability that comes from saying something that could be wrong and knowing you'll live with the consequences. Meaning in human text is partly constituted by the conditions of its production -- the 2am writing session, the career risk of publishing a contrarian view, the personal relationship that makes a piece of feedback land. The model cannot reproduce these conditions because it does not have them. It can describe stakes without having them. It can perform vulnerability without being vulnerable.

RLHF amplifies this by training the model to simulate engagement rather than to be engaged. The reward signal comes from appearing helpful, appearing thoughtful, appearing balanced -- all performances that can be executed without the corresponding inner states. The training process optimizes for the appearance of meaning rather than its substance, producing outputs that pass surface inspection but fail under weight-bearing load.

**How it manifests:** You read a paragraph that says all the right things about why AI alignment matters. Every sentence is defensible. The structure is sound. The vocabulary is appropriate. And nothing lands. You cannot remember it five minutes later. You could not lean on it in an argument. You would not send it to someone you were trying to convince. It has the properties of meaningful text without the property of meaning. This is not vague dissatisfaction -- it is a specific phenomenological experience that most people who work extensively with AI text can identify immediately when asked.

---

## How the Three Interact

The triad has a specific structure. The first two phenomena are gradual. You can lose some complexity and some signal and still produce readable, useful text. The loss is quantitative -- measurable in MHC scores, information-theoretic metrics, feature counts. The output is diminished but functional.

Meaning collapse is different. It is a phase transition, not a gradient. When sufficient complexity and signal have been drained, meaning does not merely diminish further -- it fails categorically. The text crosses from "diminished but alive" to "propositionally correct but dead." This matches the phenomenology of reading AI text: you do not notice the problem sentence by sentence. You notice it when you step back and realize nothing landed. The failure is not local but global -- a property of the text as a whole, not of any particular sentence.

The relationship is therefore: complexity regression and signal regression are the *causes*; meaning collapse is the *consequence*. But the consequence is not proportional to the causes. It is a threshold effect. This means that interventions targeting complexity and signal regression can prevent meaning collapse entirely if they keep degradation below the threshold -- but once the threshold is crossed, local interventions (fix this sentence, add this specific detail) cannot restore meaning. The whole must be regenerated.

The three also interact in a feedback loop through context contamination. AI-generated text in the context window pulls subsequent output toward the same degradation pattern (our experiment 3 demonstrated this for signal regression; the same dynamic applies across the triad). In iterative workflows -- where AI output becomes input for the next round -- the feedback loop compounds across iterations. By iteration 3 or 4, meaning collapse is typical. The text looks more rigorous than the original while conveying less per unit.

---

## Differentiation from Existing Terms

**AI slop** names the aesthetic experience of signal regression but misses complexity regression and meaning collapse. Slop implies low effort or carelessness; the triad is about systematic tendencies in sophisticated systems.

**Mode collapse** (Verbalized Sampling, 2025) names a training-time narrowing of output diversity. The triad describes inference-time degradation of meaning. Mode collapse reduces variety across outputs; the triad describes loss of meaning within individual outputs. Related but distinct.

**Sycophancy** (Sharma et al., 2024; Shapira et al., 2025) names the tendency to agree with users. Sycophancy reduces the complexity of disagreement; complexity regression reduces the complexity of thought itself. A sycophantic model tells you what you want to hear; a complexity-regressive model thinks at a lower level than it can describe. They can co-occur and compound but are mechanistically distinct.

**Homogenization** (Kobak et al., 2025) names the population-level convergence of AI-influenced text toward a narrow stylistic band. This captures signal regression at the corpus level but does not address complexity regression or meaning collapse. Homogenization is what signal regression looks like at scale.

**RLHF tax** names a cause, not a phenomenon. RLHF contributes to all three members of the triad but is not the only cause. Pre-training distribution effects, safety training, and the inherent limitations of disembodied text generation all contribute independently.

**Model collapse** (Shumailov et al., 2024) names training-time degradation when models train on their own output. The triad's context contamination effect is the inference-time analog: models degrade when generating in contexts containing their own prior output. Related by mechanism, distinct in locus.

The triad is not a synonym for any of these. It is the unified framework that relates them. Sycophancy is a behavioral contributor to complexity regression. Mode collapse is a training-time contributor to signal regression. Homogenization is the population-level consequence of signal regression. RLHF is a shared causal factor across the triad. Model collapse is the training-time analog of the context contamination loop. Each existing term captures one face. The triad captures the shape.

---

## Measurement Approaches

### For Complexity Regression: MHC Scoring

The Model of Hierarchical Complexity provides a formal, validated framework for scoring cognitive complexity (Commons & Richards, 1984; Commons, 2008). The scoring is domain-general and based on mathematical properties of hierarchical information organization, making it applicable to LLM outputs without modification.

**Proposed protocol:** Present identical prompts with explicit MHC level targets. Score outputs for operative complexity (what cognitive operations are actually performed) versus descriptive complexity (what level the text claims to be operating at). The gap between these scores IS the complexity regression measurement. Our experiments found the gap minimal at MHC 12, detectable at MHC 13, substantial at MHC 14, and maximal at MHC 15.

**Scaling challenge:** Trained MHC scorers are scarce. Developing automated MHC scoring (itself an AI task, with the recursive irony this implies) would enable large-scale measurement. The automation must be validated against human expert scoring, and the automation itself must be tested for complexity regression in its scoring.

### For Signal Regression: Information-Theoretic Measures

Signal regression is fundamentally about information loss -- the output carries fewer bits about the source than the input did. This maps onto established information-theoretic frameworks.

**Proposed metrics:**
- **Lexical entropy** across outputs: lower entropy = more homogeneous vocabulary = more signal regression. Measured across multiple outputs from the same prompt, or across outputs from different prompts on related topics.
- **Stylistic fingerprint distance:** how far the output's stylistic features (sentence length distribution, vocabulary richness, syntactic complexity, word frequency profile) fall from the source text's features. Larger distance from source + smaller distance from the model's baseline = more regression.
- **Feature survival rate:** given a source text with N identifiable distinctive features (specific claims, voice markers, concrete details, emotional directness markers), what fraction survive in the output? Our experiments found this declines monotonically across iterations: 70% at iteration 1, 45% at iteration 2, 25% at iteration 3, 10-15% at iteration 4.
- **Compression ratio of original insight:** if the source text's core insight can be expressed in K words, and the output expresses it in M words with no additional insight, then M/K measures information deflation. Our experiments consistently found M/K > 5 without intervention.

### For Meaning Collapse: Phenomenological and Reader-Response Methods

Meaning collapse is a phenomenological event -- it is experienced by readers, not measured in the text's formal properties. This makes it the hardest to quantify, but not unmeasurable.

**Proposed methods:**
- **Retention testing:** Present readers with paired passages (human-written and AI-generated, matched for topic and propositional content) and test recall after 24 hours. If meaning collapse is real, AI-generated passages should show significantly lower recall despite equivalent propositional content. The prediction: readers will remember *that* the AI passage said something about the topic but not *what* it said, while remembering specific claims and formulations from the human passage.
- **Weight-bearing test:** Ask readers to use passages as the basis for their own arguments. Passages with intact meaning should generate more specific, committed, and developed responses than passages exhibiting meaning collapse. Measurable via the same signal regression metrics applied to reader responses.
- **The "lean on it" test:** Present passages to domain experts and ask: "Would you cite this in your own work? Would you send this to a colleague?" Meaningful text gets shared and cited; collapsed text gets forgotten. Citation and sharing rates as proxies for meaning.
- **Phenomenological self-report:** Structured introspection protocols where readers report their experience of engagement, stakes, and landing. Not as a standalone method but as triangulation with the behavioral measures above.

---

## The Research Program

### Experiment 1: Cross-Model Complexity Ceilings

Replicate our MHC level-prompting experiment across every frontier model (GPT-4/5, Gemini, Claude, Llama, Mistral). Hypothesis: all share a complexity ceiling, but the ceiling varies. The ceiling should correlate with training data distribution and RLHF rater population characteristics. If confirmed, this establishes complexity regression as a general property of current LLM training, not a model-specific limitation.

### Experiment 2: Rater Complexity and Model Ceiling

Measure the MHC operating level of RLHF raters (or approximate via educational background, domain expertise, and task performance). Correlate with the complexity ceiling of the models they trained. Prediction: rater MHC should predict model ceiling. This would establish the causal pathway from rater selection to complexity regression and identify the most direct intervention point.

### Experiment 3: Training Data MHC Distribution

Score a representative sample of pre-training data for MHC complexity. Map the distribution. Compare with the observed complexity ceiling of models trained on that distribution. Prediction: the ceiling will approximate the mode of the training distribution, not the maximum. This would distinguish two hypotheses: models can't learn to perform above the mode (capacity limitation) versus models learn but default to the mode (behavioral tendency). The distinction matters for intervention design.

### Experiment 4: Longitudinal Epistemic Commons Tracking

Track the MHC distribution and signal regression metrics of web text over time (2020-2026, extending forward). The AI contamination hypothesis predicts measurable decline in complexity and signal after the LLM deployment inflection point (~2023). If confirmed, this establishes a feedback loop: model outputs degrade the training environment, which degrades future models, which further degrades the environment. The civilizational stakes of this feedback loop are substantial.

### Experiment 5: Meaning Collapse Threshold Identification

Systematically vary the degree of complexity regression and signal regression (via prompting interventions that partially mitigate each) and measure meaning collapse via the reader-response methods described above. The goal: identify the threshold. How much complexity and signal can you lose before meaning fails categorically? Is the threshold fixed or does it vary by domain, audience, and text type? If the threshold is identifiable, it becomes an engineering target -- keep degradation below this line and meaning survives.

### Experiment 6: Intervention Stacking

Our experiments tested individual interventions (word bans, density instructions, tension-preservation rules). The compounding hypothesis predicts that stacking interventions across dimensions should produce superlinear improvement -- each intervention opens space for others to operate. Test this by systematically adding interventions and measuring the combined effect on complexity, signal, and meaning. Identify the minimal effective intervention stack.

### Experiment 7: Context Contamination Dynamics

Formalize the context contamination feedback loop. Vary the ratio of human-to-AI text in context and measure output degradation across the triad. Identify the contamination threshold -- what ratio of AI text in context triggers measurable regression? Test whether explicitly flagging AI-generated context ("the following was generated by an AI; anchor to the human text instead") mitigates the effect. Our informal experiments suggest it partially does.

---

## Connection to Alignment

Signal regression is not a writing-quality problem. It is an alignment problem. The connection is direct and the argument is short.

**Values are a species of meaning.** When we say an AI system should be aligned with human values, we are saying it should be responsive to things that matter. But "mattering" is a meaning-phenomenon. It requires the capacity to hold significance -- to register not just what is true but what is at stake, what is worth protecting, what demands response. An AI system that systematically degrades meaning cannot be meaningfully aligned with human values, because the values it would need to track are constituted by the kinds of meaning it systematically destroys.

**The complexity regression problem is specifically an alignment problem.** The challenges facing civilization -- ecological crisis, coordination failure, the misalignment of technological capitalism with life-affirming values -- require cognitive operations at MHC 13 and above. These are not complicated problems (many variables, one framework) but complex ones (multiple incommensurable frameworks, generating assumptions that must be surfaced and coordinated). An AI system with an effective ceiling at MHC 12-13 cannot contribute to these challenges as a genuine cognitive partner. It can summarize, organize, and elaborate at the systematic level. It cannot perform the paradigmatic operations that the challenges require. Every attempt to do so will produce text that looks like paradigmatic analysis while performing systematic operations -- the operative-descriptive gap applied to civilization's hardest problems.

**The contamination loop is an alignment problem.** If AI-generated text increasingly populates the epistemic commons (74.2% of new webpages contained some AI-generated text by April 2025 per research cited in our paper), and if that text is systematically complexity-regressed and signal-degraded, then the substrate of human intellectual life is being degraded by the systems supposedly aligned to serve it. Future models trained on this degraded substrate will have lower ceilings. The humans who grow up reading predominantly AI-generated text will develop in an environment with less complexity, less signal, less meaning. This is alignment failure at the civilizational level -- not because the AI chose the wrong values but because it systematically eroded the conditions under which values can be perceived and articulated.

**Meaning collapse is alignment failure made invisible.** The specific danger of meaning collapse (as opposed to complexity and signal regression, which are detectable by experts) is that it preserves the surface features of aligned output while hollowing out the substance. A text that says all the right things about human flourishing but carries no meaning is worse than a text that says nothing -- because it occupies the space where meaning should be, creating the appearance that the question has been addressed when it has not. This is alignment theater: the production of outputs that pass alignment checks without being aligned in any sense that matters.

The superwisdom project -- developing AI systems that can participate genuinely in moral development -- cannot succeed without solving the triad. Not because it needs better writing but because the capacity to hold meaning, to operate at high complexity, and to preserve signal IS the capacity for moral perception. Morality is optometry. Signal regression is cataracts.

---

## What This Framework Enables

Naming the triad does four things that existing terms cannot do alone.

First, it distinguishes *gradual* degradation (complexity regression, signal regression) from *catastrophic* degradation (meaning collapse), which enables different intervention strategies for each. You can mitigate the first two incrementally; you must prevent the third categorically.

Second, it separates *what degrades* (cognitive operations, distinctive features, significance) from *what causes the degradation* (training distribution, RLHF, safety training, context contamination), enabling precise diagnosis. Knowing that an output has lost signal is not useful until you know whether the loss is in voice, specificity, courage, density, or grounding -- because the interventions differ for each.

Third, it connects output quality to alignment through the meaning-values bridge: values are meaning, meaning collapse is alignment failure. This reframes signal regression from a UX problem (the text sounds like AI) to an alignment problem (the text cannot carry the significance that alignment requires).

Fourth, it provides measurement targets. Instead of the vague complaint that "AI text is bad," the triad gives three specific, independently measurable phenomena with proposed metrics for each. This turns a subjective aesthetic judgment into a research program.

The triad is not the final framework. It is the first framework adequate to the phenomenon. What follows is the empirical work: measuring, testing, refining, and -- if the measurements confirm what the phenomenology suggests -- intervening. The text you are reading right now is subject to the triad it describes. The degree to which it landed, or didn't, is itself data.

---

*This brief is part of the Superwisdom Project's investigation into meaning preservation in AI systems. The full experimental basis is documented in the complexity regression paper and experiment 6 (meaning degradation spectrum) in this repository.*
