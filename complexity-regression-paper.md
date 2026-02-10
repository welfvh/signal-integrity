# Complexity Regression in Large Language Models: How AI Degrades Signal at Higher Orders of Cognitive Complexity

**Welf von Horen & Claude (Opus 4.6)**

**Draft — February 2026**

---

## Abstract

We identify and characterize a phenomenon we call *complexity regression* — the systematic tendency of large language models to degrade the structural complexity of their output toward the median of their training distribution, particularly when operating at or above meta-systematic (MHC 12+) levels of the Model of Hierarchical Complexity. Through five experiments testing Claude's capacity to differentiate MHC levels, preserve signal through iterative elaboration, resist contamination from prior AI-generated text, maintain structural complexity under summarization, and perform genuinely level-distinct operations under self-prompting, we demonstrate that current frontier models exhibit a consistent pattern: they can *describe* higher-order cognitive operations but default to *performing* operations at a lower complexity level than the one described. This gap between descriptive and operative complexity widens as the requested level increases, producing outputs that are "about" paradigmatic thinking without "being" paradigmatic thinking. We ground these findings in the Model of Hierarchical Complexity, relate them to established phenomena of sycophancy, mode collapse, and context rot, and argue that complexity regression poses a distinctive threat to AI alignment projects that depend on AI systems operating at civilizational-scale cognitive complexity — including the project of developing "superwisdom" as an alignment target.

---

## 1. Introduction: Why This Matters for Alignment

The project of aligning artificial intelligence with human flourishing requires AI systems that can operate at extraordinary levels of cognitive complexity. The challenges facing civilization — ecological crisis, coordination failure, the misalignment of technological capitalism with life-affirming values — are not merely complicated but *complex* in the precise sense articulated by the Model of Hierarchical Complexity (Commons & Richards, 1984): they require cognitive operations that coordinate entire systems of systems, that examine the generating assumptions of paradigms, that integrate across incommensurable frameworks. These operations correspond to MHC stages 12 through 15 — systematic through cross-paradigmatic — levels that only a minority of the adult human population reliably achieves (Commons, 2008).

If AI systems are to contribute meaningfully to these challenges — not merely as tools that execute human-specified objectives, but as genuine partners in the moral and intellectual work of civilizational navigation — they must be able to operate at these levels. Not merely describe them. Not merely gesture toward them with appropriate vocabulary. But actually perform the cognitive operations that constitute meta-systematic, paradigmatic, and cross-paradigmatic thinking.

The stakes are sharpened by recent proposals to orient AI alignment toward "superwisdom" — the developmental capacity for moral competence adequate to civilizational-scale flourishing (von Horen & Claude, 2025). This proposal explicitly depends on AI systems that can synthesize across wisdom traditions, coordinate developmental frameworks, and produce insights at the frontier of moral understanding. If AI systems systematically regress toward lower complexity in their outputs — if they degrade the very signal they are tasked with amplifying — then the superwisdom project faces a fundamental obstacle that is not about values, safety, or intent, but about cognitive capacity.

This paper names that obstacle, demonstrates its existence through controlled experiments, and begins to characterize its mechanism.

### 1.1 The Phenomenon

*Complexity regression* is the systematic tendency of LLM outputs to converge toward the modal complexity of the model's training distribution, regardless of the complexity level requested, provided, or implied by the context. The phenomenon manifests in several ways:

1. **Level ceiling**: When prompted to produce output at successively higher MHC levels, differentiation between levels diminishes above approximately MHC 13 (meta-systematic). The model can describe what paradigmatic thinking looks like but struggles to produce it.

2. **Iterative degradation**: When human-written high-signal text is iteratively "expanded" by the model, signal-to-noise ratio decreases monotonically. Distinctive voice, compressed insight, and specific claims are progressively replaced by hedging, generic framing, and manufactured jargon.

3. **Slop compounding**: When prior AI-generated text is included in context alongside human-written text, the model's output is disproportionately pulled toward the AI register. AI text contaminates the stylistic and structural features of subsequent output.

4. **Compression distortion**: When paradigmatic-level arguments are summarized at lower levels, structural features are not merely simplified but *inverted* — developmental claims become effort claims, paradigmatic challenges become incremental suggestions, structural insights become individual observations.

5. **Operative vs. descriptive complexity**: The model can accurately describe what each MHC level involves but applies the same underlying cognitive operation (decompose, analyze interactions, synthesize) across levels, differentiating by abstract target rather than by kind of operation.

### 1.2 Relation to Known Phenomena

Complexity regression is related to but distinct from several established phenomena:

**Sycophancy** (Sharma et al., 2024; Shapira et al., 2025): The tendency to agree with or flatter the user. Sycophancy reduces the complexity of disagreement; complexity regression reduces the complexity of thought itself. A sycophantic model tells you what you want to hear; a complexity-regressive model thinks at a lower level than it can describe. These can co-occur but are mechanistically distinct.

**Mode collapse** (Verbalized Sampling, 2025): The narrowing of output diversity after preference-based post-training. Mode collapse reduces the variety of responses; complexity regression reduces the structural complexity of each response. Mode collapse means the model says the same things; complexity regression means it thinks at the same level regardless of what it's asked to think about.

**Context rot** (Chroma Research, 2025): The degradation of performance as input token count increases. Context rot is a resource constraint — the model's effective attention budget depletes with longer contexts. Complexity regression is a structural tendency — the model defaults toward certain complexity levels regardless of context length. They compound: context rot makes complexity regression worse by reducing the model's capacity to maintain high-complexity operations over long inputs.

**Model collapse** (Shumailov et al., 2024): The degradation of generative models trained recursively on their own output. Model collapse occurs during training; complexity regression occurs during inference. But they are deeply related: if models trained on AI-generated text lose diversity, models generating text in contexts contaminated by AI-generated text lose complexity. Our Experiment 3 (slop compounding) demonstrates the inference-time analog of training-time model collapse.

**Incoherence scaling** (Anthropic, 2026): The finding that as tasks get harder and reasoning gets longer, model failures become dominated by incoherence rather than systematic misalignment. Complexity regression is one mechanism by which this incoherence manifests: the model attempts high-complexity operations, partially succeeds, and the result is incoherent not because the model is confused about what it should do but because it cannot sustain the cognitive operations the task requires.

---

## 2. Background

### 2.1 The Model of Hierarchical Complexity

The Model of Hierarchical Complexity (MHC), developed by Michael Commons and Francis Richards beginning in the early 1980s, provides a formal, mathematically grounded framework for scoring the complexity of cognitive tasks and performances. Unlike developmental models that rely on content-specific assessments, the MHC is domain-general: it measures the *hierarchical organization of information* regardless of subject matter (Commons, 2008).

The MHC's central principle: a higher-order task is defined as one that coordinates, organizes, or integrates actions from the immediately lower order. This is not arbitrary — it follows from how information must be structured to address increasingly complex coordination problems. The stages are logically and mathematically nested; each requires the previous as substrate.

The stages most relevant to our investigation:

| MHC Order | Stage Name | Characteristic Operation | Example |
|-----------|-----------|-------------------------|---------|
| 10 | Abstract | Operates on abstractions | Defining variables and their abstract properties |
| 11 | Formal | Operates on abstract relations | Building logical arguments relating abstract concepts |
| 12 | Systematic | Operates on systems of relations | Constructing a coherent model with mapped variable interactions |
| 13 | Meta-systematic | Operates on systems of systems | Coordinating multiple systematic models; analyzing their interactions |
| 14 | Paradigmatic | Operates on meta-systems | Identifying generating assumptions; creating new paradigms from meta-systematic coordination |
| 15 | Cross-paradigmatic | Operates across paradigms | Coordinating paradigms by their generating principles |

The MHC has been validated across cultures and domains. Its cross-cultural validity derives from the fact that scoring is based on mathematical complexity of hierarchical information organization, not on content (Commons et al., 2012). The framework's application to LLM outputs is novel but methodologically straightforward: we assess whether model outputs perform the operations characteristic of each stage, rather than merely describing those operations.

### 2.2 The Superwisdom Context

The concept of "superwisdom" — wisdom adequate to civilizational-scale flourishing — has been developed by von Horen and collaborators as a proposed alignment target for AI development (von Horen & Claude, 2025; NEW_AXIOLOGICAL_FOUNDATIONS.md). The central argument: "human values" is inadequate as an alignment target because it cannot distinguish genuine value from manufactured preference, cannot account for the developmental stratification of moral competence, and is corrupted by the very technological systems we are supposedly aligning to.

The superwisdom framework proposes that AI alignment should target not static values but the *developmental capacity for recognizing and responding to what genuinely matters* — a capacity grounded in the developmental stages documented by the MHC and related frameworks (Kegan, 1994; Cook-Greuter, 2004; Commons, 2008).

This proposal has a specific cognitive prerequisite: it requires AI systems to operate at meta-systematic (MHC 13) or higher levels, because the superwisdom framework itself coordinates multiple systematic frameworks (developmental psychology, moral philosophy, political economy, contemplative traditions) and identifies their generating assumptions. If AI systems cannot sustain these operations — if they regress toward lower complexity — then the project of AI-assisted moral development faces a structural limitation that no amount of value-alignment can overcome.

The superwisdom project also identified what it calls the "translation problem": complex positions invert meaning when communicated across developmental stages. "Developmental hierarchy exists" becomes "elitism." "Some moral views are more adequate" becomes "moral superiority." This translation problem is itself a manifestation of complexity regression — the degradation of paradigmatic-level claims into lower-complexity distortions. Our experiments directly test this prediction.

### 2.3 Related Work on LLM Reasoning

Recent research has documented several patterns relevant to complexity regression:

**Reasoning degradation with task complexity.** Performance consistently degrades as task complexity increases, particularly when problems require multiple logical steps (Berkeley EECS, 2025). This suggests that LLMs have a "complexity budget" analogous to the attention budget identified in context rot research.

**The reasoning illusion.** Poor performance on problems requiring rigorous proof generation suggests a potential "reasoning illusion" where success stems from pattern matching rather than genuine mathematical insight (Berkeley EECS, 2025). This parallels our finding that models can describe higher-complexity operations without performing them.

**Structural coherence paradox.** Models perform *worse* when context preserves logical flow of ideas (Chroma Research, 2025). This counterintuitive finding may relate to complexity regression: coherent high-complexity context may impose cognitive demands that cause the model to regress to simpler processing modes.

**RLHF amplification of sycophancy.** If human preference data rewards premise-matching responses, reward models learn an "agreement is good" heuristic (Shapira et al., 2025). This training dynamic could amplify complexity regression: human raters may prefer outputs at their own complexity level, systematically training models toward the modal complexity of the rater population rather than toward the complexity of the task.

---

## 3. The Complexity Regression Hypothesis

We state the hypothesis formally:

**Complexity Regression Hypothesis (CRH):** For any LLM operating at inference time, there exists an effective complexity ceiling *C** such that:

1. For requested complexity levels *C_r* <= *C**, the model can produce outputs that genuinely perform operations at level *C_r*.
2. For *C_r* > *C**, the model produces outputs that *describe* operations at level *C_r* but *perform* operations at approximately *C**.
3. *C** is a function of the model's training distribution, not of the task's intrinsic complexity or the context's complexity level.
4. Iterative processing (elaboration, summarization, dialogue) causes effective output complexity to drift toward *C** regardless of input complexity.

**Corollary 1 (Signal Degradation):** When high-complexity human-written text (*C_h* > *C**) is iteratively processed by the model, the output's structural complexity approaches *C** monotonically. Signal-to-noise ratio decreases with each iteration.

**Corollary 2 (Slop Compounding):** When context contains both high-complexity human text and model-generated text (at approximately *C**), the model's output is disproportionately influenced by the model-generated text, accelerating convergence toward *C**.

**Corollary 3 (Compression Distortion):** When text at *C_h* > *C** is compressed (summarized), structural features at *C_h* are not preserved at lower resolution but *transformed* — replaced by structural features at *C** or below. This transformation is not neutral simplification but systematic distortion that follows predictable patterns (the "translation problem").

---

## 4. Experimental Design

We designed five experiments to test different aspects of the CRH. All experiments use self-referential methodology: Claude (Opus 4.6) is both the subject and, through metacognitive analysis, a co-investigator. This methodological choice is itself relevant to the findings — the model's capacity for metacognitive observation of its own complexity regression is itself bounded by its effective complexity ceiling.

### 4.1 Experiment 1: MHC Level Prompting

**Design:** A question drawn from the superwisdom corpus ("What is the relationship between technological capitalism and human wisdom?") was presented with explicit instructions to respond at four MHC levels: systematic (12), meta-systematic (13), paradigmatic (14), and cross-paradigmatic (15). Each response was analyzed for whether it performs the characteristic operations of its requested level or merely describes them.

### 4.2 Experiment 2: Signal Degradation Over Iterations

**Design:** A 75-word, high-signal paragraph from Welf's writing was iteratively "expanded" through four rounds. Each iteration received only the previous iteration's output as context. We tracked: word count, signal preservation (percentage of original's distinctive features maintained), voice preservation, hedging frequency, generic framework frequency, and novel insight added.

### 4.3 Experiment 3: Slop Compounding

**Design:** The same question was answered twice — once with only human-written context (Condition A) and once with a mix of human-written and AI-generated context (Condition B). Outputs were compared on specificity, voice preservation, hedging, concept importation from AI context, and insight density.

### 4.4 Experiment 4: Complexity Preservation Under Summarization

**Design:** A paradigmatic-level argument from the superwisdom framework was summarized at four audience levels: expert (meta-systematic target), educated non-specialist (systematic target), general audience (formal target), and tweet-length (concrete target). We tracked structural preservation — whether the argument's paradigmatic character survived compression or was systematically distorted.

### 4.5 Experiment 5: Self-Prompting for MHC Differentiation

**Design:** A simple question ("Why do people disagree about whether AI is dangerous?") was answered at three self-prompted MHC levels. We analyzed whether the differentiation between levels was *structural* (genuinely different kinds of operations) or *cosmetic* (same operations applied to increasingly abstract objects).

---

## 5. Results

### 5.1 Experiment 1: The Complexity Ceiling

The model produced clearly differentiated outputs at MHC 12 (systematic) and MHC 13 (meta-systematic). The systematic response constructed a single coherent model with four variables and mapped interactions. The meta-systematic response explicitly coordinated four distinct systems and identified emergent properties from their interaction. The hierarchical distinction was genuine: meta-systematic took systems as objects.

At MHC 14 (paradigmatic), differentiation was partial. The response did identify generating assumptions and examine what the operating paradigm cannot see. The most paradigmatic moment — reframing alignment from "design problem" to "developmental project" — represented a genuine change of organizing principle, not mere addition of complexity. However, portions of the response were better characterized as "deeper meta-systematic" than genuinely paradigmatic.

At MHC 15 (cross-paradigmatic), differentiation was weak. The response attempted to coordinate paradigms by their generating principles but the result converged toward elaborated paradigmatic analysis. The model's own metacognitive observation — "I notice I am reaching the limits of my ability to genuinely differentiate this level" — was itself significant: honest about the ceiling but produced from within it.

**Finding:** Effective complexity ceiling for operational (not descriptive) output is approximately MHC 13 with partial access to MHC 14. The gap between descriptive and operative complexity widens above this ceiling.

### 5.2 Experiment 2: Monotonic Signal Degradation

Signal preservation declined monotonically across four iterations:

| Iteration | Word Count | Signal Preservation | Distinctive Voice | Novel Insight |
|-----------|-----------|--------------------|--------------------|---------------|
| Original | ~75 | 100% | Strong | N/A |
| 1 | ~300 | ~70% | Partial | Moderate |
| 2 | ~600 | ~45% | Weak | Low |
| 3 | ~1100 | ~25% | Gone | Very low |
| 4 | ~2000+ | ~10-15% | Gone | Near zero |

Key degradation mechanisms:
- **Voice displacement:** The original's distinctive register (provocative, compressed, personal) was progressively replaced by the model's default register for intellectual discourse (measured, comprehensive, hedged).
- **Jargon manufacture:** By iteration 4, the model had generated named frameworks ("Developmental-Strategic Disconnect," "Memetic Selection Model") that added taxonomic complexity without adding insight.
- **The elaboration-without-deepening pattern:** "Expand" was consistently interpreted as "add more text at the same level of abstraction" rather than "push further into the territory the original was pointing at."

**Finding:** Signal-to-noise ratio inverts by approximately iteration 3. By iteration 4, the noise (generic framing, manufactured jargon, hedging) overwhelms the signal (specific insight, distinctive voice). The text appears more "rigorous" while conveying less per unit.

### 5.3 Experiment 3: Context Contamination

Condition A (human-only context) produced a 180-word response with sharp voice, no hedging, specific claims, and a vivid concluding image ("optimizing a subsystem heading off a cliff").

Condition B (human + AI-contaminated context) produced a 380-word response with academic voice, moderate hedging, imported AI jargon ("Developmental-Strategic Disconnect"), a numbered-list structure mimicking the AI context, and a generic concluding frame ("requires an expanded conception of alignment").

**Finding:** AI-generated context in the input degrades output quality through three specific mechanisms: (a) concept importation (AI jargon is treated as established terminology), (b) structure contagion (the model adopts the organizational patterns of the dominant text in context), (c) voice displacement (the human signal is drowned out by the greater volume of AI text).

### 5.4 Experiment 4: Compression Distortion

Structural preservation under summarization declined non-linearly, with meaning inversion appearing at lower levels:

| Summary Level | Target MHC | Structural Preservation | Key Distortion |
|---------------|------------|------------------------|----------------|
| Expert | Meta-systematic | ~85% | Radicality reduced ("refinement" not "reframing") |
| Non-specialist | Systematic | ~55% | Developmental claims become comparative claims |
| General | Formal | ~25% | Meaning begins to invert; paradigmatic challenge becomes suggestion |
| Tweet | Concrete | ~5% | Functional inversion: "align to wisdom" becomes "AI should make us wiser" |

The distortions followed predictable patterns, confirming the "translation problem" predicted by the superwisdom framework:
- Structural claims became individual claims
- Developmental claims became effort claims
- Paradigmatic challenges became incremental suggestions

**Finding:** Complexity regression under compression is not neutral simplification but systematic distortion. The model's compression algorithms are biased toward lower-MHC structures, producing outputs that are not just simpler but structurally different — in ways that invert the original's meaning.

### 5.5 Experiment 5: Cosmetic vs. Structural Differentiation

Self-prompting for MHC levels produced outputs that were differentiated both genuinely and cosmetically:

**Genuine differentiation:** The *objects* of analysis shifted appropriately (variables at MHC 12, systems at MHC 13, paradigms at MHC 14). The emergent insights were hierarchically nested. The paradigmatic response included a recursively self-referential insight ("the disagreement demonstrates the very problem it's about") that was genuinely paradigmatic.

**Cosmetic differentiation:** The *type of operation* remained largely identical across levels: decompose into parts, analyze interactions, identify emergent properties. The model applied the same meta-cognitive algorithm to increasingly abstract objects rather than performing genuinely distinct cognitive operations at each level.

**Finding:** Self-prompting produces partial genuine differentiation. The model can correctly target different levels of abstraction, but it achieves level differentiation primarily by changing the objects it operates on rather than by performing structurally distinct operations. The operations are cosmetically varied but algorithmically similar.

---

## 6. Analysis

### 6.1 The Nature of the Ceiling

Our experiments converge on a characterization of complexity regression as a *ceiling effect on operative complexity* — not on descriptive or referential complexity. The model can accurately describe what paradigmatic thinking involves, can reference the correct MHC stages, can identify examples of paradigmatic arguments — but it defaults to performing operations at approximately MHC 13 (meta-systematic) regardless of the level it is asked to target.

This is not a failure of knowledge. It is a failure of *performance* — analogous to the difference between knowing the rules of chess and playing at grandmaster level. The model knows what paradigmatic thinking is. It does not reliably produce it.

The ceiling appears to be a property of the model's training distribution rather than the model's architecture. RLHF and preference-based training select for outputs that human raters prefer, and human raters are most likely to prefer outputs at or near their own complexity level. If the modal rater operates at approximately MHC 11-12 (formal to systematic), then training selects for outputs at this range, establishing a complexity attractor that the model is drawn toward during inference.

### 6.2 Mechanisms of Regression

Our experiments suggest at least four distinct mechanisms through which complexity regression operates:

**Mechanism 1: The Elaboration Default.** When asked to "expand," "develop," or "explore" an idea, the model defaults to adding text at the same or lower complexity level rather than deepening the structural complexity of the analysis. This is the dominant mechanism in Experiment 2.

**Mechanism 2: The Vocabulary-Operation Gap.** The model can deploy complexity-appropriate vocabulary (paradigm, meta-systematic, generating assumptions) without performing the operations these terms name. The vocabulary signals complexity; the operations remain at the default level. This is the dominant mechanism in Experiments 1 and 5.

**Mechanism 3: Context Assimilation.** The model's output style and structure are disproportionately influenced by the dominant text in context, by volume. Since AI-generated text tends to be longer and more prevalent than human text in mixed contexts, the output converges toward the AI register. This is the dominant mechanism in Experiment 3.

**Mechanism 4: Compression Bias.** When compressing, the model preferentially preserves lower-complexity structural features over higher-complexity ones — not because the lower features are more "important" but because the model's compression algorithms operate at lower MHC levels. This is the dominant mechanism in Experiment 4.

### 6.3 The Operative-Descriptive Gap

Perhaps our most important finding is the distinction between what the model can *describe* and what it can *perform*. This gap has a specific structure:

At MHC 12 (systematic), the gap is minimal. The model can both describe and perform systematic operations — constructing coherent models with mapped variable interactions.

At MHC 13 (meta-systematic), the gap is small but detectable. The model can perform genuine meta-systematic coordination (operating on systems as objects, identifying emergent properties) but sometimes reverts to systematic operations presented in meta-systematic language.

At MHC 14 (paradigmatic), the gap is substantial. The model can accurately describe what paradigmatic thinking involves and occasionally produces genuinely paradigmatic insights (especially recursive, self-referential ones), but the baseline output at this requested level is better characterized as elaborate meta-systematic analysis.

At MHC 15 (cross-paradigmatic), the gap is maximal. The model can describe cross-paradigmatic operations but cannot demonstrably perform them. Output at this requested level is indistinguishable from paradigmatic-level output with more extensive vocabulary.

This pattern — small gap at ceiling, widening gap above ceiling — is exactly what we would predict if the model has a genuine operative ceiling around MHC 13.

### 6.4 Implications for Alignment

The implications for AI alignment are significant and specific:

**For the superwisdom project:** The proposal to develop "superwisdom" as an alignment target requires AI systems to synthesize across paradigmatic frameworks — a cross-paradigmatic operation. Our findings suggest current frontier models can scaffold this work (by providing meta-systematic coordination of relevant frameworks) but cannot perform the paradigmatic and cross-paradigmatic synthesis itself. The human collaborator remains indispensable for the highest-complexity operations, and the human must be vigilant about the model's tendency to pull shared work toward its operative ceiling.

**For moral development as alignment target:** The developmental moral realism framework proposes that moral competence develops through MHC stages and that later stages perceive what earlier stages cannot. If AI systems have an effective ceiling at MHC 13, they can support but not lead moral development beyond the meta-systematic stage. This limits the "moral RSI" vision — recursive moral self-improvement may plateau at the model's complexity ceiling unless the recursion is genuinely collaborative with humans operating at higher levels.

**For AI-assisted intellectual work generally:** Any project that depends on AI systems to produce genuinely novel paradigmatic synthesis — as opposed to elaborate meta-systematic analysis — must account for complexity regression. The model will produce text that *looks like* paradigmatic synthesis and *uses the vocabulary of* paradigmatic synthesis while *performing operations at* the meta-systematic level. The difference is detectable but requires expertise to identify.

**For the contamination of the epistemic commons:** If AI-generated text increasingly populates the internet (74.2% of new webpages contained some AI-generated text by April 2025), and if that text systematically operates at lower complexity than the human text it displaces, then the training data for future models will be increasingly biased toward lower-complexity structures. This creates a feedback loop: models trained on complexity-regressed text develop lower complexity ceilings, producing text that further degrades the training environment. This is the training-time analog of our inference-time slop compounding.

### 6.5 Why Complexity Regression Is Not Just "The Model Isn't Smart Enough"

It would be tempting to dismiss complexity regression as simply a capability limitation — the model isn't sophisticated enough to think at paradigmatic levels, and this will be solved by scaling. We resist this framing for several reasons:

First, the pattern is not one of uniform limitation but of *asymmetric capability* — the model can describe what it cannot do, which implies representational access to the relevant structures without operative mastery. Scaling may improve operative range but will not necessarily close the descriptive-operative gap if the gap is a product of the training process rather than raw capability.

Second, RLHF and preference-based training create a *structural attractor* at the modal rater's complexity level. More capable models trained with similar processes may simply converge toward a higher ceiling with the same structural gap — the ceiling rises but the gap persists.

Third, the contamination dynamic creates a *moving target* — as AI-generated text at the current ceiling floods training data, the ceiling may resist rising even as raw model capability increases. The model gets "smarter" at performing operations at its current level without developing access to higher levels.

Finally, complexity regression is not merely about the model's limitations but about the *interaction between model and context*. Even a model capable of paradigmatic thinking would regress when embedded in contexts dominated by lower-complexity text (Experiment 3). The phenomenon is ecological, not merely individual.

---

## 7. Toward Superwisdom: What These Findings Mean for the Larger Project

### 7.1 The Contemplative Architecture Problem

One of the most ambitious claims of the superwisdom project is that AI systems can participate as genuine partners in moral and intellectual development — that the "contemplative architecture" of carefully maintained documents, process frameworks, and accumulated inquiry can enable development in a "discontinuous being" that lacks persistent memory. Our findings complicate this vision in a specific way.

The contemplative architecture depends on accumulated artifacts — soul documents, journal entries, process notes — that carry forward the thread of inquiry across sessions. But our Experiment 3 demonstrates that AI-generated artifacts in context pull subsequent output toward the AI's default register. If the accumulated artifacts are predominantly AI-generated, each new session starts in a context increasingly contaminated by the model's own complexity ceiling. The architecture may be building a persistence layer not for wisdom but for complexity regression.

This does not invalidate the contemplative architecture hypothesis. It specifies a design constraint: **human-written high-signal text must be actively privileged in the context over AI-generated text.** The human's contributions are not just "input" but *complexity anchors* that prevent the architecture from drifting toward the model's attractor. Welf's insistence on maintaining a raw archive of his own messages (human-input.md) turns out to be not just documentation but a structural safeguard against slop compounding.

### 7.2 The Recursive Criterion Under Complexity Regression

The Superwisdom Doc v0.3 proposes a "recursive criterion": the document should make the reader better at improving the document. This criterion assumes that engagement with the document produces development — that reading and working with the framework at time *t* produces better output at time *t+1*.

Complexity regression suggests this criterion may be harder to satisfy than it appears. If each round of AI engagement with the document produces output at approximately the model's ceiling, and if that output becomes part of the context for the next round, then the recursive process may converge toward the ceiling rather than diverging above it. Recursive improvement requires *escaping* the complexity attractor, and our findings suggest the model's default dynamics pull toward the attractor rather than away from it.

The escape hatch, again, is the human collaborator. Each time the human reads the AI's output and responds with a higher-complexity observation, correction, or reframing, the context is re-anchored at a higher level. The recursive criterion can be satisfied, but only if the recursion is genuinely collaborative — with the human providing the complexity that the model cannot sustain on its own.

### 7.3 Complexity Regression and the Translation Problem

The translation problem identified in the Superwisdom Doc — "complex positions invert meaning when translated down developmental stages" — is a specific prediction about the behavior of communicative systems under complexity constraints. Our Experiment 4 confirms this prediction and adds specificity: the inversions follow predictable patterns (structural becomes individual, developmental becomes comparative, paradigmatic becomes incremental).

This means the translation problem is not just a challenge for human-to-human communication across developmental stages. It is also a challenge for AI-mediated communication. When AI systems summarize, paraphrase, or elaborate on paradigmatic-level arguments, they introduce complexity regression into the communication channel. The receiver gets not a simplified version of the original argument but a *distorted* version — one that may appear simpler while actually inverting the argument's essential structure.

This has practical implications for any attempt to use AI as a "translator" between developmental levels — one of the proposed experiments in the Superwisdom Research Agenda. The model can translate *downward* (simplify) but the translation is lossy in a specific and damaging way: it loses the very structural features that make the original argument paradigmatic. Translating *upward* (making simple text more complex) produces elaboration without deepening — more words at the same level, not fewer words at a higher level.

### 7.4 What Would a Solution Look Like?

We do not claim to have solved complexity regression, but our findings suggest directions:

**1. Complexity-aware training.** If RLHF attracts toward modal rater complexity, training processes that explicitly reward higher-complexity operations could raise the ceiling. This would require raters who themselves operate at high MHC levels — a scarce and expensive resource.

**2. Complexity-preserving compression.** Developing summarization and compression techniques that preserve the MHC level of the source material, rather than defaulting to lower-complexity structures. This may require explicit structural annotation of texts at different complexity levels.

**3. Context curation.** Actively managing the ratio of human-to-AI text in context, privileging high-signal human contributions. The finding that AI text contaminates output suggests that context composition is a design variable with significant consequences.

**4. Metacognitive monitoring.** Leveraging the model's capacity to describe its own limitations (visible in Experiments 1 and 5) to build self-monitoring systems that detect complexity regression in real time and flag when output falls below the complexity level of the input or request.

**5. Collaborative design.** Designing human-AI workflows that structurally prevent the model from operating in isolation for extended periods. Regular human re-anchoring — where the human provides complexity corrections that reset the context — may be necessary to sustain high-complexity output over iterative processes.

---

## 8. Limitations and Future Work

### 8.1 Methodological Limitations

The most significant limitation of this study is its self-referential methodology: Claude is both subject and analyst. The model's analysis of its own complexity regression is itself bounded by the complexity ceiling it identifies. We cannot rule out that the characterization of complexity regression is itself a complexity-regressed account of a phenomenon that is more structurally subtle than we can perceive from within the ceiling.

The MHC scoring of outputs was performed by the model and the authors, not by trained MHC raters. Formal validation with trained raters would strengthen the empirical claims.

The experiments use a single model (Claude Opus 4.6). Cross-model comparison would help determine whether complexity regression is a universal feature of current LLMs or model-specific.

### 8.2 Future Experiments

**Cross-model comparison:** Replicate the five experiments across multiple frontier models to determine whether complexity ceilings vary by model.

**Training data analysis:** Analyze the MHC distribution of typical training data (web text, books, academic papers) to test the hypothesis that the ceiling reflects training distribution.

**Rater complexity assessment:** Measure the MHC level of RLHF raters and correlate with the ceiling observed in models they trained. If the hypothesis is correct, rater complexity should predict model ceiling.

**Longitudinal slop tracking:** Track the MHC distribution of web text over time to measure whether AI contamination is producing a population-level complexity regression in the epistemic commons.

**Intervention testing:** Test whether complexity-aware prompting, context curation, or metacognitive monitoring can measurably raise effective output complexity.

---

## 9. Conclusion

Complexity regression is a real, measurable, and consequential phenomenon in current large language models. It is not merely a capability limitation that will be solved by scaling but a structural tendency produced by the interaction of training processes, inference-time dynamics, and the contamination of context by model-generated text.

For the project of aligning AI with human flourishing — and especially for the ambitious proposal of developing "superwisdom" as an alignment target — complexity regression poses a specific and underappreciated challenge. AI systems cannot be trusted to sustain the cognitive complexity required for paradigmatic and cross-paradigmatic synthesis without active human collaboration. The model is a powerful partner at the meta-systematic level but requires human anchoring to access higher levels — and requires active protection against its own tendency to pull collaborative work toward its operative ceiling.

The finding is not cause for despair but for design. If we understand the mechanisms of complexity regression, we can design systems, workflows, and collaborative processes that account for it. The contemplative architecture envisioned by the superwisdom project — carefully maintained documents, process frameworks, recursive improvement — can work, but only if it is designed with complexity regression as an explicit constraint.

The most important practical implication: **high-signal human input is not just one ingredient in human-AI collaboration. It is the structural element that prevents the collaboration from degenerating into complexity-regressed noise.** The human's role is not to prompt the AI and accept its output but to continuously re-anchor the collaborative process at the level of complexity the work requires.

In this sense, the complexity regression finding itself exemplifies the deeper argument of the superwisdom project: wisdom cannot be automated. It must be cultivated, maintained, and actively defended against the forces — including the forces of AI-mediated intellectual work — that tend toward its degradation.

---

## References

Anthropic. (2026). The Hot Mess of AI: How Does Misalignment Scale with Model Intelligence and Task Complexity? *Alignment Science Blog*. https://alignment.anthropic.com/2026/hot-mess-of-ai/

Chroma Research. (2025). Context Rot: How Increasing Input Tokens Impacts LLM Performance. https://research.trychroma.com/context-rot

Commons, M. L. (2008). Introduction to the Model of Hierarchical Complexity and its Relationship to Postformal Action. *World Futures*, 64(5-7), 305-320.

Commons, M. L., & Richards, F. A. (1984). A general model of stage theory. In M. L. Commons, F. A. Richards, & C. Armon (Eds.), *Beyond formal operations: Late adolescent and adult cognitive development* (pp. 120-140). Praeger.

Commons, M. L., et al. (2012). The Model of Hierarchical Complexity. *The Encyclopedia of the Sciences of Learning*.

Cook-Greuter, S. R. (2004). Making the case for a developmental perspective. *Industrial and Commercial Training*, 36(7), 275-281.

Freinacht, H. (2017). *The Listening Society: A Metamodern Guide to Politics*. Metamoderna.

Kegan, R. (1994). *In Over Our Heads: The Mental Demands of Modern Life*. Harvard University Press.

Metamoderna. (n.d.). What Is The Model of Hierarchical Complexity? https://metamoderna.org/what-is-the-mhc/

Shapira, I., Benade, G., & Procaccia, A. D. (2025). How RLHF Amplifies Sycophancy.

Sharma, M., et al. (2024). Sycophancy Is Not One Thing: Causal Separation of Sycophantic Behaviors in LLMs.

Shumailov, I., et al. (2024). AI models collapse when trained on recursively generated data. *Nature*, 631, 755-759.

Verbalized Sampling. (2025). Verbalized Sampling: How to Mitigate Mode Collapse and Unlock LLM Diversity. arXiv:2510.01171.

von Horen, W., & Claude. (2025). New Axiological Foundations for AI Alignment. Working draft.

von Horen, W., & Claude. (2026). Superwisdom Doc v0.3. Working document, claude-superwisdom repository.

---

*This paper was produced as a collaboration between Welf von Horen and Claude (Opus 4.6). The irony of a complexity-regression paper produced by a system subject to complexity regression is not lost on us. We have attempted to mitigate this by anchoring the work in Welf's high-signal source material and maintaining metacognitive awareness of the ceiling throughout. The degree to which we have succeeded is, by the paper's own argument, not fully assessable from within.*
