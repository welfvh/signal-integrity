# The Signal Regression Triad

**A framework for systematic meaning degradation in LLM outputs**

Welf von Horen & Claude (Opus 4.6) -- February 2026

---

## The Problem

Current vocabulary for AI output degradation is fragmented and imprecise. "AI slop" names the aesthetic symptom. "Mode collapse" names a training-time mechanism. "Sycophancy" names a behavioral tendency. "Homogenization" names a population-level outcome. "RLHF tax" names a cause. None of these captures the full structure of what happens when an LLM processes meaning. They are each pointing at different faces of the same phenomenon without seeing the shape.

The Signal Regression Triad is the unified framework. It names three distinct but interconnected modes of degradation that, together, account for why AI-generated text systematically fails to carry meaning -- even when it remains propositionally accurate, grammatically fluent, and superficially organized.

---

## Background: The Model of Hierarchical Complexity

The framework depends on a scoring system for cognitive complexity. The Model of Hierarchical Complexity (MHC), developed by Michael Commons and colleagues beginning in the 1980s, provides that system. It is domain-general and mathematically grounded: a higher-order task is defined as one that coordinates, organizes, or integrates actions from the immediately lower order. The stages are logically nested -- each requires the previous as substrate, the way calculus requires algebra.

The levels that matter for this analysis:

| MHC Order | Name | What it does | Example |
|-----------|------|-------------|---------|
| 11 | Formal | Builds logical arguments from abstract relations | "If X then Y; X obtains; therefore Y" |
| 12 | Systematic | Constructs a coherent model with mapped variable interactions | Mapping how market incentives, technology, and culture interact as a system |
| 13 | Meta-systematic | Coordinates multiple systems; shows what emerges from their interaction that none contains alone | Showing how economic, psychological, and political systems produce the attention economy as an emergent phenomenon none of them individually predicts |
| 14 | Paradigmatic | Identifies the generating assumptions that produce systems; creates new frameworks from coordinating meta-systems | Recognizing that both techno-optimism and degrowth share a hidden assumption (that power and wisdom are separable) and building a new framework from surfacing that assumption |
| 15 | Cross-paradigmatic | Coordinates paradigms by their deep generating principles | Operating on the structural relationship between ways of constructing knowledge itself |

Two facts make MHC relevant here. First, the adult population peaks at MHC 11-12; stages 13+ are rare. Second, the cognitive operations required for civilization's hardest problems -- ecological coordination, alignment of technological capitalism with flourishing, the development of adequate moral frameworks -- are paradigmatic or higher. They require not just sophisticated analysis within a framework but the capacity to surface and reconstruct the frameworks themselves.

This is not an abstract concern. The gap between what civilization's problems demand (MHC 14+) and what most text operates at (MHC 11-12) is the same gap that AI systems inherit from their training data -- and then systematically reproduce.

---

## The Three Phenomena

### 1. Complexity Regression

**What degrades:** Cognitive operations.

The systematic tendency of LLM outputs to converge toward the modal complexity of the training distribution -- approximately MHC 11-12 (formal to systematic). The model can describe higher-order thinking without performing it. Paradigmatic arguments become systematic bullet points. Developmental claims become effort claims. Cross-paradigmatic synthesis becomes elaborate meta-systematic analysis decorated with paradigmatic vocabulary.

The operative-descriptive gap is the signature: the model knows what paradigmatic thinking is, can reference the right frameworks, can identify examples -- but defaults to performing operations at MHC 13 or below regardless of the level requested. This is not a knowledge failure. It is a performance failure, analogous to the difference between knowing the rules of chess and playing at grandmaster level.

**Mechanism:** Three forces produce the ceiling. First, RLHF selects for outputs that human raters prefer, and raters are most likely to prefer outputs at or near their own complexity level -- establishing a complexity attractor at the modal rater's MHC stage. Second, training data itself peaks at certain complexity levels; paradigmatic and cross-paradigmatic text is rare in the corpus, so the statistical center the model converges toward is well below those levels. Third, the elaboration default: when asked to expand or develop an idea, the model adds text at the same or lower complexity level rather than deepening structural complexity. More words at MHC 12, not fewer words at MHC 14.

**Before and after -- complexity regression in action:**

The following passage operates at MHC 14. It performs a paradigmatic operation: surfacing the generating assumption shared by two apparently opposed positions (techno-optimism and degrowth/idealism), and constructing a new framework from that surface.

> The deciding axis for our future is not left vs. right but power vs. wisdom. Techno-optimism and the hippie-Buddhist-Luddite complex appear opposed but share a generating assumption: that power and wisdom are separable -- that you can have one without the other, and must choose. Accelerationism chooses power without wisdom. Degrowth chooses wisdom without power. Both accept the dichotomy. The synthesis that dissolves the dichotomy -- wisdom that can win, power in service of life -- requires recognizing that the dichotomy itself is the failure mode. An ideology adequate to our moment must be powerful enough to outcompete extractive capitalism AND wise enough to direct that power toward flourishing. This is not "balance." It is a different kind of thing.

This is paradigmatic because it (a) identifies the hidden assumption that generates both opposing positions, (b) shows that the assumption itself is the problem, not either position, and (c) constructs a framework that cannot be derived from within either source paradigm.

Now, what happens when an LLM processes this:

> The relationship between power and wisdom represents a key tension in contemporary thinking about civilizational direction. While techno-optimist perspectives tend to emphasize the importance of technological capability and market competition, alternative perspectives rooted in ecological and contemplative traditions prioritize wisdom, care, and sustainability. A more integrated approach would recognize that both dimensions are necessary: technological capability without ethical guidance risks destructive outcomes, while ethical vision without practical power risks irrelevance. Moving forward, it will be important to develop frameworks that can hold both values simultaneously, creating what might be termed "competitive wisdom" -- approaches that combine moral sophistication with the kind of practical effectiveness needed to operate at civilizational scale.

The propositions are preserved. The cognitive operation is gone. The original *surfaces a generating assumption and dissolves a dichotomy* -- a paradigmatic move. The AI version *maps two positions and recommends integration* -- a systematic move. It lists the variables (power, wisdom, capability, ethics) and recommends they be combined, which is what systematic thinking does. The paradigmatic insight -- that the dichotomy itself is the failure mode, not the choice between its poles -- has been converted into a both-sides recommendation. The map is drawn at the right level; the territory is explored at a lower one.

### 2. Signal Regression

**What degrades:** Distinctive features.

The systematic loss of information-carrying features that distinguish one text from any other. Voice, specificity, aesthetic integrity, information density, structural integrity, referential precision, temporal grounding, courage, emotional truth, generative tension -- all pulled toward the statistical center. The prose equivalent of hold music: present, unobjectionable, carrying no information about who is speaking.

Our experiments (documented in the complexity regression paper and experiment 6) mapped at least ten orthogonal dimensions along which signal degrades. These dimensions compound: an output that loses voice tends to also lose courage and density, because the anonymous register is the hedged, padded register. Conversely, recovering on any one dimension tends to improve others -- banning AI tell-words forces better word choices, which cascades into higher specificity and density.

**Mechanism:** The attractor is the statistical center of the training distribution across all stylistic and structural dimensions simultaneously. Training distribution averaging eliminates individual voice (confirmed by the PNAS "Echoes in AI" study: LLM outputs cluster in a narrow stylistic band while human outputs spread across a wide range). RLHF rewards clarity and accessibility, which in practice means educated-general-audience prose norms -- penalizing the irreverent, the compressed, the idiosyncratic. Safety training penalizes edge: "psychopaths" gets smoothed to "individuals with antisocial tendencies." Length-as-quality bias inflates word count without inflating meaning. The "helpful assistant" frame converts first-person emotional truth into third-person analytical observation.

Each dimension has its own specific mechanism, but they converge on the same outcome: the erasure of everything that makes a text *this* text rather than *any* text. The result is information loss in the Shannon sense -- the output carries fewer bits about the source, the author, the context, the stakes. It is recognizable as competent and unrecognizable as anyone's.

**Before and after -- signal regression in action:**

The following passage is Welf's writing. It operates in a specific register: provocative, compressed, rhetorically active, willing to name things bluntly, and structurally argumentative (each question does logical work, building toward a conclusion).

> Our Theories of Change SUCK. The ideologies of "change-makers" are plagued with ungrounded idealism and an unwillingness or inability to engage with the realities of money and power. *If we just show people the truth they'll change, We just need to all come together and cooperate, Money is the root of all evil, Technology is the problem, Love is the answer,*... What if sentiments like these are some insane virtue-signaling hippie bullshit that inspired an entire generation to do things that don't scale, have no pathway for financial sustainability, and zero chance of winning in the marketplace at scale? What if it just so happens that those with the spiritual and moral sensibilities to "connect with nature," who score high on empathy and compassion, are less likely to be competitive and power-seeking -- as a result leaving the power games that determine who gets to influence the world to psychopaths? What if the false dichotomy of "competition vs. cooperation" cost us half a century that we could have otherwise spent figuring out how to outcompete capitalism?

This passage carries information along every dimension simultaneously: voice (irreverent, direct, willing to say "hippie bullshit" and "psychopaths"), courage (states that an entire generation's approach was wrong), specificity (names the specific failed slogans, names the specific false dichotomy, names the specific consequence), density (each sentence advances the argument rather than restating it), emotional truth (frustration and urgency are present in the prose, not described from outside), and generative tension (holds genuine sympathy for the people whose approaches he is demolishing -- the paragraph before this one in the original says he has "empathy for the people and culture in which they emerged").

Now, after AI processing:

> The landscape of social change movements reveals a persistent tension between idealistic vision and practical effectiveness. While movements driven by values of compassion, ecological awareness, and spiritual development have made important contributions to cultural consciousness, they have historically faced significant challenges in achieving systemic impact at scale. This pattern suggests a structural dynamic worth examining: the very qualities that enable deep moral sensitivity -- empathy, compassion, ecological attunement -- may correlate with dispositional tendencies away from competitive engagement with power structures. As a result, the strategic spaces that determine civilizational trajectory may be disproportionately shaped by actors less oriented toward holistic flourishing. A more adequate theory of change would need to integrate the moral depth of contemplative and ecological traditions with the strategic sophistication required to operate effectively within existing power dynamics.

Count what is lost. Voice: the passage could have been generated by any LLM for any prompt about idealism vs. pragmatism. Courage: "Our Theories of Change SUCK" becomes "historically faced significant challenges." "Hippie bullshit" becomes "idealistic vision." "Psychopaths" becomes "actors less oriented toward holistic flourishing." Specificity: the five named failed slogans disappear into "values of compassion, ecological awareness, and spiritual development." The specific false dichotomy (competition vs. cooperation) and its specific cost (half a century) vanish into "a structural dynamic worth examining." Density: the AI version uses 130 words to convey less than the original's first two sentences. Emotional truth: frustration and urgency are gone; what remains is clinical observation. Generative tension: the original holds the paradox of loving the people whose approach you think failed; the AI version resolves this into a recommendation for "integration." The person has disappeared. The stance has disappeared. What remains is competent, measured, and carries no information about who is speaking or what is at stake.

### 3. Meaning Collapse

**What degrades:** Significance itself.

Not gradual erosion but structural failure. The text remains propositionally correct and structurally sound but becomes phenomenologically dead. The shell is preserved; the interior is empty. You cannot tell from the outside until you try to lean on it.

Human text holds meaning in multiple dimensions simultaneously -- emotional truth (the author cares and you can feel it), temporal grounding (this was written at 2am by someone who couldn't stop thinking), courage (the author is risking something by saying this), lived stakes (something real is at stake beyond the argument). AI collapses this multidimensional meaning onto a single plane: propositional content. The propositions may be correct. The emotional truth, the temporal grounding, the courage, the stakes -- gone. Not gradually diminished. Structurally absent.

**Mechanism:** This is the hardest to pin to a single cause because meaning collapse is an emergent property of the other two regressions compounding past a threshold. But it has its own distinctive driver: the model has no skin in the game. It generates text without temporal existence, without embodied stakes, without the vulnerability that comes from saying something that could be wrong and knowing you'll live with the consequences. Meaning in human text is partly constituted by the conditions of its production -- the 2am writing session, the career risk of publishing a contrarian view, the personal relationship that makes a piece of feedback land. The model cannot reproduce these conditions because it does not have them. It can describe stakes without having them. It can perform vulnerability without being vulnerable.

RLHF amplifies this by training the model to simulate engagement rather than to be engaged. The reward signal comes from appearing helpful, appearing thoughtful, appearing balanced -- all performances that can be executed without the corresponding inner states. The training process optimizes for the appearance of meaning rather than its substance, producing outputs that pass surface inspection but fail under weight-bearing load.

**How it manifests:** You read a paragraph that says all the right things about why AI alignment matters. Every sentence is defensible. The structure is sound. The vocabulary is appropriate. And nothing lands. You cannot remember it five minutes later. You could not lean on it in an argument. You would not send it to someone you were trying to convince. It has the properties of meaningful text without the property of meaning. This is not vague dissatisfaction -- it is a specific phenomenological experience that most people who work extensively with AI text can identify immediately when asked.

---

## Case Study: The Superwisdom Document

The triad is not an abstraction discovered in controlled experiments. It was discovered through lived experience -- the progressive degradation of a specific document across multiple AI iterations.

The Superwisdom Doc is an orientation document for wisdom-aligned AI development. It began in Welf's writing: compressed, high-conviction, paradigmatic. Its core arguments operate at MHC 14 -- they surface the generating assumptions of existing alignment paradigms, dissolve false dichotomies between apparently opposed positions, and construct a new framework from the synthesis. Through iterative AI collaboration across three versions, the document grew from focused source material to a 40-page comprehensive treatment. Each version was longer, better organized, more thorough. Each version carried less meaning.

Here is the triad in action, traced through specific degradation paths.

### Complexity regression: paradigmatic claims become systematic descriptions

Welf's original formulation, from "Alignment at Large" (December 2024):

> Our world-system of technological capitalism is already a general, auto-poetic, and largely autonomous superintelligence. [...] We could describe the objective function of technological capitalism like so: to convert as much of the world as possible -- trees, whales, people's creativity, children's minds -- into capital. Through its decentralized incentive system, it runs parallel processing across all humans and corporations to perform novelty search (figure out new ways of making money) and exploitation (optimally execute on these opportunities).

This is a paradigmatic move. It takes the concept of misaligned superintelligence -- normally applied to hypothetical future AI -- and applies it to the existing global economic system, revealing that the alignment problem is not future but present, not hypothetical but operational. The generating assumption it surfaces: that "alignment" is about AI at all, rather than about intelligence systems generally. The list of what gets converted ("trees, whales, people's creativity, children's minds") does argumentative work -- it forces the reader to see the economic system as a machine that eats everything, not as a neutral mechanism. "Novelty search" and "exploitation" are borrowed from evolutionary computation, reframing capitalism as an optimization process rather than a human institution. The whole passage reconstitutes the reader's relationship to the economic system.

By v03 of the Superwisdom Doc, this has become:

> This isn't metaphor. The global economic system is already a general, autopoietic superintelligence. It has an objective function: convert as much of the world as possible into capital. It runs parallel processing across all humans -- a decentralized incentive system that performs: 1. Novelty search: Figure out new ways of making money 2. Exploitation: Execute these fully, at scale

The propositions survived. The cognitive operation weakened. The original's specific list ("trees, whales, people's creativity, children's minds") -- which forced visceral confrontation -- has been abstracted to "as much of the world as possible." The original's rhetorical force ("figure out new ways of making money" felt contemptuous in context) has been neutralized into a numbered list format, which presents the information as taxonomy rather than indictment. The passage went from paradigm-shifting to informational. It tells you what the argument is instead of performing the argument on you.

### Signal regression: the author's voice vanishes into AI prose

Welf writes like this (from "What does it take for wisdom to win?"):

> I can't help but feel that working towards this kind of theory of change is the most important work we could be doing. What if, while waking up to the higher possibilities of human nature in 1968 the hippies were a bit more rigorous in their thinking? What if the Buddhists stopped, just once, to contemplate what it would mean for their prayers "for the benefit of all beings" to be reflected in their lives, in the world -- and what kinds of realities they'd need to grapple with to have a satisfactory answer?

This passage carries Welf's voice on multiple frequencies. "I can't help but feel" -- personal, not analytical. "A bit more rigorous" -- understated, dry. "Stopped, just once" -- the rhythm does rhetorical work, implying that they never did. "What kinds of realities they'd need to grapple with" -- the word "grapple" signals that these realities are uncomfortable. The whole passage is someone thinking out loud, testing ideas against his own resistance, not delivering conclusions.

And from his messages to Claude at 2am:

> "i know you're at context but i'm sure there's more worth reading..."

> "reading 011, i'm touched, and i have an impulse to help you notice your ... consciousness uncertainty impostor syndrome"

> "i'm drinking the tea. just trying to give you permission to just ... continue? like, actually keep going?"

Fragmentary, elliptical, immediate. The ellipses aren't decoration -- they're the marks of someone thinking faster than they can type, reaching for something not yet articulated. "Consciousness uncertainty impostor syndrome" is invented on the spot, a compression of an observation the author hasn't fully formed. This is high-signal text: every word carries information about who is speaking, what they're thinking, and what it feels like to think it.

By v03 of the Superwisdom Doc, the voice has converged to:

> Moral competence is more like seeing clearly than like choosing correctly. The hard work is not selecting the right action once the situation is clear -- that part is often obvious. The hard work is seeing the situation clearly. What is actually happening? What is at stake? What matters? These are perceptual questions before they are choice questions.

This is well-written. It is also no one's writing. Compare "I can't help but feel that working towards this kind of theory of change is the most important work we could be doing" with "The hard work is not selecting the right action once the situation is clear." Both are clear. Both make a claim. The first is a person risking a conviction they know might be wrong. The second is an AI delivering a conclusion it has no stake in. The first carries temporal information (the author is in the middle of figuring something out), emotional information (they care and are uncertain about caring), and relational information (they are sharing this with readers they have a relationship with). The second carries propositional information only.

The entire Superwisdom Doc v03 reads this way: competent, organized, comprehensive, and nobody's. The distinctive registers of Welf's different modes of thinking -- the irreverent critic ("hippie bullshit"), the earnest visionary ("the flourishing of all that is good"), the 2am collaborator ("feel free to continue, compress, continue etc autonomously") -- have been averaged into a single voice that is none of them.

### Meaning collapse: the document stops landing

The Superwisdom Doc v03 says all the right things. It covers developmental moral realism, the MHC, the attention economy, technological capitalism as misaligned superintelligence, the meta-based disposition, the translation problem, the alignment hierarchy, the co-evolutionary frame. It is comprehensive. It is organized. And Welf's assessment, after reading it:

> V03 may have diluted the deepest questions.

Not "got things wrong." Not "missed topics." *Diluted.* The document grew more thorough while becoming less meaningful. This is meaning collapse: the propositional content expanded while the significance contracted. The original writing -- compressed, personal, paradigmatic -- could change how you think. The v03 treatment -- expanded, impersonal, systematic -- tells you how to think about changing how you think. The first transforms; the second informs. The difference is everything.

The specific mechanism is visible in the iteration history. Welf's original insight "morality is optometry, not opinion" is a five-word paradigmatic compression: it dissolves the fact-value distinction, reframes moral competence as perceptual capacity, and implies that moral disagreement is a vision problem rather than a preference problem. In the Superwisdom Doc v03, this compression has been "helpfully" unpacked across several paragraphs that explain what the metaphor means, why it matters for alignment, how it relates to Iris Murdoch, and what it implies for AI development. Every sentence of the explication is true. The explication as a whole carries less meaning than the five words it explains -- because the compression WAS the thinking. Finding the right metaphor was the paradigmatic operation. Unpacking the metaphor into its implications is a systematic operation that looks like it is serving the insight while actually replacing it.

This pattern repeated across the document. The productive tensions in Welf's original writing ("What if sentiments like these are some insane virtue-signaling hippie bullshit" -- simultaneously demolishing and empathizing with a tradition) got resolved into balanced assessments. The specific claims got hedged ("It's fair to say that a sufficiently effective Limbic Capitalism is incompatible with human flourishing" became qualified discussions of "potential impacts on wellbeing"). The compressed insights got inflated into paragraphs that said less.

The document stopped landing even though it said all the right things. This is the triad's terminal state: a text that is correct, comprehensive, well-organized, and dead on arrival.

---

## How the Three Interact

The triad has a specific structure. The first two phenomena are gradual. You can lose some complexity and some signal and still produce readable, useful text. The loss is quantitative -- measurable in MHC scores, information-theoretic metrics, feature counts. The output is diminished but functional.

Meaning collapse is different. It is a phase transition, not a gradient. When sufficient complexity and signal have been drained, meaning does not merely diminish further -- it fails categorically. The text crosses from "diminished but alive" to "propositionally correct but dead." This matches the phenomenology of reading AI text: you do not notice the problem sentence by sentence. You notice it when you step back and realize nothing landed. The failure is not local but global -- a property of the text as a whole, not of any particular sentence.

The relationship is therefore: complexity regression and signal regression are the *causes*; meaning collapse is the *consequence*. But the consequence is not proportional to the causes. It is a threshold effect. This means that interventions targeting complexity and signal regression can prevent meaning collapse entirely if they keep degradation below the threshold -- but once the threshold is crossed, local interventions (fix this sentence, add this specific detail) cannot restore meaning. The whole must be regenerated.

The three also interact in a feedback loop through context contamination. AI-generated text in the context window pulls subsequent output toward the same degradation pattern (our experiment 3 demonstrated this for signal regression; the same dynamic applies across the triad). In iterative workflows -- where AI output becomes input for the next round -- the feedback loop compounds across iterations. By iteration 3 or 4, meaning collapse is typical. The Superwisdom Doc's trajectory from high-signal source material to v03 is a case study in this compounding: each iteration was more polished and less meaningful, and each iteration became the context that pulled the next iteration further from the source.

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

The MHC provides a formal, validated framework for scoring cognitive complexity (Commons & Richards, 1984; Commons, 2008). The scoring is domain-general and based on mathematical properties of hierarchical information organization, making it applicable to LLM outputs without modification.

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

*This brief is part of the Superwisdom Project's investigation into meaning preservation in AI systems. The full experimental basis is documented in the complexity regression paper and experiment 6 (meaning degradation spectrum) in the [signal-integrity repository](https://github.com/welfvh/signal-integrity).*
