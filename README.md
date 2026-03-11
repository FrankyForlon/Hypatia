![Uploading image.png…]()
# Hypatia

**A Research Library and Intellectual Foundation for AI-Based Psychological Assessment**

Hypatia is a research program investigating a foundational question: *What does an AI system actually measure when it infers personality from natural language?*

This repository contains the primary source library, critical essays, white papers, and supplementary research data that constitute the intellectual foundation of the Hypatia project. It is maintained by [Peter Golub](mailto:p.golub@utah.edu) and Chad Keith.

---

## The Thesis

Large language models can infer Big Five personality traits from brief open-ended text with correlations approaching *r* = .85-.88 against self-report instruments (Wright et al., 2026; Park, 2025). The science is validated at the highest levels of peer review. But the science alone does not answer the question that matters for any applied system: *what is the ontological status of the output?*

Hypatia's answer: the output is a **cognitive model** --- a digital twin of what we call the *Inner Self* --- with predictive power within specifiable boundary conditions. It is not a measurement of a fixed trait. It is not a prediction of future behavior. It is a structured representation of how a person thinks, values, and narrates --- bounded by a fidelity ceiling that the system reports honestly rather than conceals.

The research collected here develops this thesis through six critical book reviews, a synthesis of twelve peer-reviewed articles, and a white paper that integrates the philosophical, empirical, and architectural arguments into a single framework.

---

## Repository Structure

```
Hypatia/
+-- Hypatia Library/
|   +-- Hypatia Books and Book Reviews/
|   |   +-- [6 source texts (PDF)]
|   |   +-- [6 critical review essays (DOCX)]
|   |   +-- [1 presentation (PPTX)]
|   +-- Hypatia Articles/
|   |   +-- [12 peer-reviewed research articles (PDF)]
|   |   +-- [Abridged article summaries]
|   |   +-- Chad Keith/         # Founder's papers
|   |   +-- Peter Golub/        # Consultant's papers and white papers
|   +-- Hypatia_Bibliography.docx
|   +-- Hypatia_Library_cleaned_articles.docx
+-- personality_llm_zero_shot-main/
|   +-- [Wright et al. replication data and Jupyter notebooks]
+-- README.md
```

---

## The Hypatia Library

### Books and Critical Reviews

Six books were selected for the Library because each addresses a distinct failure mode that any AI personality assessment system must confront. The critical reviews connect each book's core argument to specific architectural and epistemological recommendations for Hypatia.

| Book | Author | Review Focus |
|------|--------|-------------|
| *Artificial Superintelligence* | Roman Yampolskiy | Unconstrained optimizers and systems that do not know their own limits. The case for building boundary conditions into the architecture rather than discovering them in production. |
| *How Emotions Are Made* | Lisa Feldman Barrett | Construction vs. detection. If psychological categories are constructed rather than found, then the instrument shapes the output --- and the system must report its own constructive role. |
| *Psychology of Intelligence Analysis* | Richards Heuer (CIA) | Cognitive bias as compression artifact. The case for Analysis of Competing Hypotheses (ACH): output a matrix of competing personality models, not a single authoritative profile. |
| *The Cult of Personality* | Annie Murphy Paul | A century of personality tests that survived by institutional embedding rather than scientific validity. The warning against building another instrument that persists because it is useful rather than because it is true. |
| *Generative Agent Simulations of Human Behavior* | Joon Sung Park | The fidelity ceiling (85% attitudes / 80% personality / 66% novel behavior), memory architecture, and the Galaxy problem --- why the jump from 78% to 85% comes from richer memory, not smarter models. |
| *The (Honest) Truth About Dishonesty* | Dan Ariely | The fudge factor and universal micro-dishonesty. Organic conversational data is not unfiltered truth --- it is self-report the speaker does not recognize as self-report. |

### Research Articles

Twelve peer-reviewed articles spanning LLM-based personality inference, psychometric validation, and collective intelligence, including:

- **Wright et al. (2026)** --- *Assessing Personality Using Zero-Shot Generative AI Scoring of Brief Open-Ended Text.* Published in *Nature Human Behaviour*. Demonstrates *r* = .88 for zero-shot Big Five scoring from brief open-ended narratives. The foundational empirical validation for the field.
- **Park (2025)** --- *Generative Agent Simulations of Human Behavior.* Stanford dissertation documenting the fidelity ceiling and demonstrating that longitudinal episodic memory is the key architectural variable.
- **Serapio-Garcia et al. (2025)** --- Construct validity of LLM personality assessment across multiple psychometric frameworks.
- **Burton (2024)** --- How LLMs reshape collective intelligence.
- **Hussain (2025)** --- Personality prediction from life stories using LLMs.
- **Zhu (2025)** --- Evaluating LLM alignment on personality inference from real-world interviews.

The complete set of articles, with abridged summaries optimized for both human and AI readers, is available in `Hypatia_Library_cleaned_articles.docx`.

### Bibliography

`Hypatia_Bibliography.docx` provides a complete annotated bibliography of all materials in the Library.

---

## White Papers

**"What Are We Measuring? On Digital Twinning, Behavioral Prediction, and the Epistemology of AI Psychological Assessment"**
*Peter Golub, March 2026*

The central white paper synthesizes the entire Library into a single argument. Key claims:

1. **The cognitive twin framework.** AI personality assessments produce cognitive models --- digital twins of the Inner Self --- not measurements of fixed traits. The paper locates this output on a spectrum between the biological twin (deterministic, no psychological content) and the behavioral twin (e.g., Park's Oracle, psychologically empty despite perfect prediction).

2. **The fidelity ceiling is structural, not improvable.** Text predicts text, not action. The 19-point gap between attitudinal prediction (85%) and behavioral prediction (66%) reflects the fundamental limit of any system that infers from language alone.

3. **B = f(P, E).** Behavior is a function of person and environment (Lewin, 1936). The system should output context-sensitive models rather than context-free scores, representing how traits manifest differently across situations.

4. **The fudge factor.** Organic conversation is pre-edited by the speaker's self-enhancing narrative machinery (Ariely, 2012). The system must model this bias structurally --- through asymmetric confidence intervals rather than naive accuracy claims.

5. **Honest boundary reporting.** A system that reports what it cannot know is more trustworthy, and ultimately more useful, than one that claims omniscience.

---

## Supplementary Data

### Wright et al. Replication (`personality_llm_zero_shot-main/`)

Reproducible pipeline and supplementary data from Wright et al. (2026), including:

- **Jupyter notebooks** for zero-shot LLM personality scoring, AAPECS reasoning analysis, and paper figure collation
- **Multi-model outputs** from Claude Sonnet, GPT-4.1, GPT-4.1 Mini, Gemini Flash, Grok 3 Beta, Llama Maverick, and Qwen 3 235B
- **Self-reported data** (two samples) for validation against LLM-scored traits
- **Seed run data** for reproducibility verification

See `personality_llm_zero_shot-main/README.md` for details.

---

## Key Concepts

| Concept | Definition |
|---------|-----------|
| **Fidelity Ceiling** | The structural accuracy limits of text-based inference: ~85% on attitudes, ~80% on personality traits, ~66% on novel behavior (Park, 2025). |
| **Cognitive Twin** | A digital model of the Inner Self --- bounded, honest, and useful precisely because it specifies what it can and cannot predict. |
| **B = f(P, E)** | Lewin's field equation. Personality is not context-free; assessment outputs should model person-environment interactions. |
| **Fudge Factor** | Ariely's term for universal small-scale self-deception. Organic conversation carries systematic upward bias in prosocial and competence-related self-description. |
| **Galaxy Problem** | The challenge of detecting synthetic personas in conversational data (Park, 2025). AI-generated text is indistinguishable from human at ~59% accuracy. |
| **ACH** | Analysis of Competing Hypotheses (Heuer). Output a matrix of competing personality models weighted by evidence, not a single profile. |
| **Hermeneutical Lacuna** | The interpretive gap in text-only assessment where non-verbal, physiological, and contextual cues are absent. |

---

## Future Directions

The research program outlined in these materials points toward several development priorities:

1. **Original empirical validation** --- Structured replication comparing Hypatia's pipeline against raw LLM scoring and self-report instruments (N >= 50).
2. **Context-sensitive prototyping** --- Demonstrating B = f(P, E) by modeling the same person across divergent conversational contexts.
3. **MCP/Agent integration** --- Specification for Hypatia as a Model Context Protocol server, enabling any AI agent to model its interlocutor's psychology in real time.
4. **Privacy and consent architecture** --- Formalizing data sovereignty, consent models, and multi-party conversation handling for clinical and enterprise deployment.
5. **Academic publication** --- Submission of the white paper with original data to peer-reviewed journals.

---

## Authors

**Peter Golub** --- Strategic consultant, research synthesis, critical essays, white papers, and repository architecture.
Contact: [p.golub@utah.edu](mailto:p.golub@utah.edu)

**Chad Keith** --- Founder, ConversaTrait (Hypatia). Platform architecture, original research, and product development.

---

## License

Materials in this repository are provided for research and educational purposes. Individual works retain their respective copyrights. See specific files for licensing details.

---

## Citation

If referencing this research program or its materials:

> Golub, P. & Keith, C. (2026). *Hypatia: A Research Library and Intellectual Foundation for AI-Based Psychological Assessment.* GitHub repository. https://github.com/FrankyForlon/Hypatia
