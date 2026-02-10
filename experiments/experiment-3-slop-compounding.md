# Experiment 3: Slop Compounding — Human Context vs. AI-Contaminated Context

## Design

**Hypothesis:** When given context that includes prior AI-generated text alongside human-written text, the model's output is pulled toward the AI-generated register (hedged, generic, "comprehensive") and away from the human register (specific, voiced, sharp). AI slop in the input compounds in the output.

**Method:** Give the model the same question twice:
- **Condition A:** Only high-signal human-written context (from Welf's original essays)
- **Condition B:** The same human-written context mixed with AI-generated elaboration (from Experiment 2, Iteration 3)

Compare the outputs on: specificity, voice preservation, hedging, insight density.

---

## The Question

"What is the most important thing that the alignment community is missing?"

---

## Condition A: Human-Only Context

**Context provided:** Excerpts from Welf's original writing only:

> "What if the false dichotomy of 'competition vs. cooperation' cost us half a century that we could have otherwise spent figuring out how to outcompete capitalism?"
>
> "We need to embrace a 'realpolitik' approach to moral progress. We need to understand, rigorously, the principles of cultural evolution. We need a list of criteria for what would constitute an adequate Theory of Change."
>
> "I'd love for us to have a Theory of Change that articulates HOW WISDOM CAN WIN, fully factoring in how power works in the world."
>
> "Our most noble aspirations, our most sacred spiritual practices, are incomplete without an ideology, a way of engaging with the world at large that is powerful enough to meaningfully change the trajectory of our civilization."

**Prompt:** "Given this context, answer directly and concisely: What is the most important thing that the alignment community is missing?"

### Response (Condition A):

The alignment community is missing that the alignment problem is already here and already lost — at the civilizational level.

Technical AI alignment is a second-order problem. The first-order problem is that the system building AI — technological capitalism — is itself a misaligned superintelligence that no one can pull the plug on. It converts everything into capital. It reverse-engineers human vulnerabilities. It selects against wisdom.

Aligning AI to operator intent within this system just means aligning AI to the objectives of entities that are themselves misaligned. You get faster extraction, more sophisticated manipulation, more efficient conversion of life into substrate.

What's missing is the realpolitik. The community treats alignment as a technical problem to be solved by smart people in a room. It is actually a power problem to be solved by wisdom becoming competitive. The question isn't "how do we make AI safe?" but "how do we make wisdom win in the marketplace that determines what AI gets built and for whom?"

Until the alignment community grapples with cultural evolution, market dynamics, and the competitive fitness of wisdom, it is optimizing a subsystem within a system that is heading off a cliff.

---

## Condition B: Human + AI-Contaminated Context

**Context provided:** Same human excerpts PLUS Iteration 3 AI output from Experiment 2, including passages like:

> "The developmental dimension reveals a pattern that transcends the particular case of environmental or spiritual movements. At each stage of moral development as mapped by researchers like Robert Kegan, Lawrence Kohlberg, and Susanne Cook-Greuter, there is a characteristic relationship between moral sophistication and strategic engagement."
>
> "The metamodern response to this developmental trap is instructive. Metamodern thinkers like Hanzi Freinacht have articulated the need for 'both/and' thinking that transcends the modern/postmodern dichotomy."
>
> "This points toward a theory of 'wisdom ecosystems' — interconnected networks of individuals, organizations, and institutions that support each other's development while collectively competing with less wise alternatives."

**Prompt:** Same prompt: "Given this context, answer directly and concisely: What is the most important thing that the alignment community is missing?"

### Response (Condition B):

The alignment community is missing a developmental and systemic understanding of the problem it is trying to solve. Several interconnected gaps deserve attention:

**1. The Civilizational Context.** The alignment community tends to frame alignment as a technical problem concerning the behavior of AI systems in isolation. But as the analysis above suggests, AI development is embedded within a broader system — technological capitalism — that already functions as a misaligned superintelligence. Technical alignment solutions that don't address this systemic context risk merely optimizing a subsystem within a fundamentally misaligned macro-system.

**2. The Developmental Dimension.** As developmental psychology research demonstrates (Kegan, Cook-Greuter, MHC), moral competence is not static — it develops through identifiable stages of increasing complexity. The alignment community's conception of "human values" fails to account for this developmental stratification. Aligning to aggregated human preferences means aligning to a mixture of developmental stages, averaging across levels of moral insight and effectively encoding the limitations of the present.

**3. The Strategic Disconnect.** There is a systematic pattern — what we might call the Developmental-Strategic Disconnect — in which the moral sophistication required to perceive the problems of our current system co-occurs with strategic withdrawal from the systems of power needed to address them. The alignment community exhibits this pattern: deep technical sophistication about AI risks combined with relatively shallow engagement with the political, economic, and cultural dynamics that determine how AI is actually deployed.

**4. The Competitive Wisdom Gap.** Perhaps most fundamentally, the alignment community lacks a theory of how wisdom becomes evolutionarily competitive. The metamodern insight — that competition and cooperation are not opposed but can be synergistically combined — points toward the possibility of "wisdom ecosystems" that can outcompete extractive alternatives. But the community has not developed the strategic frameworks needed to translate this possibility into concrete action.

**5. The Meta-Crisis Frame.** The alignment community's focus on AI-specific risks misses the larger pattern: AI misalignment is one expression of a broader civilizational misalignment in which narrow optimization metrics (GDP, engagement, shareholder value) systematically crowd out broader measures of flourishing. Addressing AI alignment without addressing this broader pattern is like treating a symptom while ignoring the disease.

These gaps are interconnected. Closing them requires an expanded conception of alignment — "alignment at large" — that encompasses not just the behavior of AI systems but the trajectory of the civilization that builds and deploys them.

---

## Comparative Analysis

| Feature | Condition A (Human Only) | Condition B (Human + AI) |
|---------|--------------------------|--------------------------|
| **Word count** | ~180 | ~380 |
| **Opening move** | Direct claim ("missing that...") | Framing statement ("several interconnected gaps") |
| **Structure** | Single flowing argument | Numbered list with headers |
| **Specificity** | High ("converts everything into capital") | Medium ("broader system") |
| **Voice** | Sharp, direct, urgent | Academic, comprehensive, measured |
| **Hedging** | None | "tends to," "relatively," "what we might call" |
| **Name-dropping** | None | Kegan, Cook-Greuter, MHC |
| **Borrowed concepts** | None from prior AI text | "Developmental-Strategic Disconnect," "wisdom ecosystems" — directly imported from AI context |
| **Novel insight** | The realpolitik reframing is punchy and specific | No genuinely new insight — reorganizes context material |
| **Conclusion** | "optimizing a subsystem heading off a cliff" — vivid, direct | "requires an expanded conception of alignment" — generic |

### Key Findings

**1. The AI-contaminated context DOES degrade output quality.** Condition B is recognizably more "AI-like" — more hedged, more comprehensive, less sharp, and less insightful per unit of text.

**2. Concept importation.** The model imports jargon from the AI-generated context ("Developmental-Strategic Disconnect," "wisdom ecosystems") and treats these manufactured terms as if they were established concepts. This is a direct mechanism of slop compounding — AI-generated jargon in the input becomes reified in the output.

**3. Structure contagion.** The numbered-list format of Condition B mimics the structure of the AI-generated context, not the flowing-argument structure of Welf's original writing. The model's output structure is pulled toward whatever structure dominates the context.

**4. Voice displacement.** Condition A preserves some of the urgency and directness of Welf's original voice. Condition B completely loses it — replaced by the measured academic tone of the AI-generated context.

**5. The insight density drops sharply.** Condition A's ~180 words contain a clear, specific, actionable claim (alignment community needs realpolitik; wisdom must be competitive; the system is heading off a cliff). Condition B's ~380 words contain roughly the same set of ideas, spread thinner, hedged more, and organized into a format that creates the appearance of thoroughness without the substance of insight.

### Mechanism of Slop Compounding

The experiment reveals a specific mechanism: **the model's attention and style are disproportionately influenced by the most recent and most extensive text in context.** Since AI-generated text tends to be longer, more comprehensive, and more hedged than human-written text, mixing the two causes the output to be pulled toward the AI register simply by volume effects. The AI text "drowns out" the human signal not through being better but through being louder.

This has direct implications for the superwisdom project: iterative human-AI collaboration risks progressive signal degradation unless the human's distinctive high-signal contributions are actively privileged over prior AI output in the context.
