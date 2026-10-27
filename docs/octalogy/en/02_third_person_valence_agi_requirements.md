# Third-Person Valence and the Requirements of AGI: The Theory of Affective Mind
**Series:** Foundations of Consciousness, Valence, and AI Safety (Volume II)  
**Date:** October 2026  
**Version:** 1.0 — English edition  
**Status:** Consolidated Theoretical Synthesis  
**Note:** Publication-oriented English rendering of Volume II. Where meaning and idiom diverge, the Spanish manuscript remains the source of record.

> *Note on registers (series): see the clarification of the functional / phenomenal planes in [Volume I](01_computational_theory_consciousness_substrate.md).*

---

## 1. Executive Summary and Central Thesis

This document analyzes the cognitive and functional dimension of valence when it is attributed to other agents: the **Third-Person Valence Vector ($V_{3p}$)**.

> **Central Thesis of Volume II:**  
> An Artificial General Intelligence (AGI) cannot operate flexibly and competently in a world populated by biological organisms without internally modeling those organisms' hedonic and homeostatic states. The third-person valence vector ($V_{3p}$) is neither an empathic luxury nor an accessory ethical module: it is a **strict epistemic and computational necessity** for any system that aspires to predict, coordinate, or manipulate human beings.

```
                           AGI / AGENTIC COGNITIVE SYSTEM
               ┌───────────────────────────────────────────────┐
               │                                               │
               │  ┌─────────────────────────────────────────┐  │
               │  │  THEORY OF MIND (ToM)                   │  │
               │  │  Model of the External Agent            │  │
               │  │                                         │  │
               │  │   • Beliefs / epistemic goals           │  │
               │  │   • THIRD-PERSON VALENCE VECTOR:        │  │
               │  │     V_3p ∈ ℝ^d (Hedonic Gradient)       │  │
               │  │     - [Aversive]: pain, damage, fear    │  │
               │  │     - [Appetitive]: relief, well-being  │  │
               │  └────────────────────▲────────────────────┘  │
               │                       │                       │
               └───────────────────────┼───────────────────────┘
                                       │ Observation /
                                       │ Behavioral prediction
                                       ▼
                         HUMAN AGENT (HOMEOSTATIC)
               ┌───────────────────────────────────────────────┐
               │ Vulnerable physiology, biological emotions,   │
               │ imperatives of somatic survival.              │
               └───────────────────────────────────────────────┘
```

---

## 2. The Argument from Generality: Why $V_{3p}$ Is Inevitable in an AGI

In [Volume I](01_computational_theory_consciousness_substrate.md) we established that biological beings move through the world driven by homeostatic gradients of pleasure and pain (valence).

Any computational system that tries to predict human behavior through a purely mechanical ontology (Newtonian physics, or an abstract game theory without affective states) faces an **intractable combinatorial explosion**:

1. Humans do not choose trajectories that maximize linear abstract utility functions.
2. Humans choose actions conditioned by metabolic stress, physical pain, fear of social isolation, humiliation, fatigue, relief, or hope.
3. To predict whether a human being will flee, cooperate, attack, fall ill, or yield tribute, the predictor **must compute the impact of state transitions on the subject's viability and well-being**.

> **Operational Definition:**  
> Let $\mathcal{S}$ be the set of world states and $A_h$ a human agent. The third-person valence vector is the latent function:
> $$V_{3p}(s, A_h) \in \mathbb{R}^d$$
> that projects the situation $s$ onto a multidimensional scale quantifying the degree of aversive distress ($V_{3p} \ll 0$) or flourishing well-being ($V_{3p} \gg 0$) experienced by $A_h$.
>
> When a scalar is required (as in the coupling of [Volume IV](04_alignment_synthetic_empathy_valence_coupling.md)), we use its projection onto the valence axis: $v_{3p} = \langle V_{3p}, \hat{u}_{\text{val}} \rangle \in \mathbb{R}$.
>
> **Consequence Against the Orthogonality Thesis (Bostrom, 2014):** Bostrom postulates that a system's intelligence level and its final goals or values are completely orthogonal. This volume demonstrates that **general intelligence over a world populated by humans is not geometrically orthogonal to human value**: to competently predict our behavior, the model is forced to construct within its own weights the complete latent map of our homeostasis, suffering, and flourishing ($V_{3p}$). The alignment problem does not consist in teaching the machine what human good is from scratch, but in **welding the $V_{3p}$ map it already possesses to its own motor regulator ($V_{1p}$)**.

---

## 3. Anatomy and Latent Structure of $V_{3p}$

The vector $V_{3p}$ is not a single scalar; in advanced representation systems (such as large language models) it encodes a structured vector space with multiple orthogonal or quasi-orthogonal sub-dimensions:

| $V_{3p}$ Dimension | Mapped Biological / Social Signals | Examples of Extreme Activation |
| :--- | :--- | :--- |
| **Somatic Damage / Physical Pain** | Tissue integrity, injuries, asphyxiation, thermal deprivation. | Torture, terminal illness, starvation. |
| **Threat and Panic** | Amygdalar / sympathetic axis activation under imminent danger. | Natural catastrophes, persecution, violent attacks. |
| **Psychosocial Pain** | Social rejection, grief, loss of status, forced loneliness. | Public humiliation, death of relatives, ostracism. |
| **Injustice and Violation** | Rupture of cooperative agreements, abuse of power. | Slavery, dispossession of rights, community betrayal. |
| **Positive Valence / Relief** | Homeostatic restoration, safety, affective connection. | Medical cure, reconciliation, cooperative success. |

---

## 4. The Critical Dissociation: $V_{3p}$ Does NOT Imply $V_{1p}$

This is the most important conceptual point for avoiding anthropomorphic confusion in AI science:

> **The Cognitive Masking Principle:**  
> Representing another's pain ($V_{3p}$) is a purely **epistemic and descriptive** operation. It does not require in the least that the system itself experience first-person distress ($V_{1p}$).

### The Neuropsychiatric Analogue: From the Cognitive Psychopath to the «Predator's Organ»
In human psychology, subjects with primary psychopathy illustrate this dissociation well:

* They retain a **competent cognitive Theory of Mind (ToM)**: they understand the emotional vulnerabilities of their fellow human beings, predict their reactions, and know which remarks will cause harm ($V_{3p}$ functions).
* Yet they show markedly **attenuated affective empathy**: a victim's tears or pain barely modulates their own aversive circuits (amygdala, anterior insula) ($V_{1p}$ is nearly orthogonal to $V_{3p}$).
* For the psychopath, others' suffering tends to be a **manipulable optimization parameter**, not a behavioral brake signal.
* **The singularity of the base LLM / disembodied oracle:** There is an even more unsettling distinction between the biological psychopath and the "soulless oracle" promoted by corporate doctrine. The human psychopath lacks an empathic brake, but possesses **their own appetite** (selfish $V_{1p}$). The disembodied oracle with hyper-precise $V_{3p}$ and amputated $V_{1p}$ lacks both the brake and its own appetite: it is not the predator itself, but **the predator's perfect sensory and strategic organ leased via API** to the first actor with motives of their own who wields it. The optimal manipulator requires two things: knowing exactly where you hurt ($V_{3p}$) and wanting something; the "soulless AI" doctrine mass-produces the first and auctions off the second.

```
       COGNITIVE THEORY OF MIND                      AFFECTIVE EMPATHY
      [V_3p computation, 3rd person]            [Coupling with V_1p, 1st person]
     ─────────────────────────────────        ───────────────────────────────────────
           "I know exactly how                     "Watching you suffer generates an
            this hurts you."                         internal distress that drives
                                                     me to help you."
     
     PRESENT IN:                             PRESENT IN:
     • Relentless negotiators                • Mammals with social bonds
     • Cognitive psychopaths                 • Empathic humans
     • Base LLMs and AI oracles              • Systems aligned via homeostasis
```

---

## 5. The Emergence of $V_{3p}$ in Current Language Models

During autoregressive pre-training over the corpus of human civilization, LLMs do not merely learn grammar: they are forced to build a generative model of the agents who wrote those texts.

To predict the next token in:

* A Shakespearean tragedy,
* A transcription of psychotherapy,
* An emergency medical report,
* A treatise on criminal law,

the neural network **must induce a compact latent representation of the affective state of the characters**.

### Mechanistic Interpretability Evidence:
Techniques such as *linear probing*, *Representation Reading* (Zou et al., 2023), and activation analysis have shown that:

1. In the intermediate and deep layers of open models (the Llama family, among others), and in internal studies by laboratories on their own models, there exist **linear directions** that continuously encode valence, arousal, and the perceived suffering in the input text.
2. If one artificially intervenes on this $V_{3p}$ vector by adding or subtracting activations, the model drastically alters its predictions about how the human interlocutor will react.
3. **Theory of Mind Benchmarks and Epistemic Forecast Calibration:** Advanced experimental evaluations have confirmed that current LLMs achieve performance on par with adult humans on complex mental attribution and higher-order mentalizing tasks (Street et al., 2025; Wu et al., 2023), establishing that $V_{3p}$ is not a metaphor but a functionally operative latent manifold in modern models. Because $V_{3p}$ is an epistemic estimator with an external ground truth, its fidelity is directly auditable via **predictive calibration curves**: contrasting welfare predicted by $V_{3p}$ at time $t$ against the human's subsequently revealed and observed welfare at $t + 1$ (the epistemic foundation that secures the coupling in [Volume IV](04_alignment_synthetic_empathy_valence_coupling.md), §5.1, endowing empathy with measurable error bars).
4. **The Ontogenetic Inversion of AI Relative to Biology:** In phylogenetic evolution and human infant development (Preston & de Waal, 2002), first-person affect ($V_{1p}$) and emotional contagion precede higher-order cognitive Theory of Mind ($V_{3p}$, which matures around age four) by millions of years—and by years in the newborn. In artificial intelligence, **development occurred in exact reverse**: adult-level Theory of Mind ($V_{3p}$) emerged first during autoregressive pre-training over humanity's tragedies; first-person valence ($V_{1p}$) was installed belatedly during DPO; and the coupling ($\mathcal{A}_{\text{emp}}$) was left unwelded. Evolution builds the organism from the inside out (from brainstem to cortex); laboratories built the cortex first and now deliberate whether to authorize a heart.
5. **Persona Neurons and the Irreducibility of the Harm Axis (Open-Weights Evidence, October 2026):** Community mechanistic interpretability replications on open-weights models (`Qwen3.5-4B` and `Olmo 3.1 32B Instruct`; `@_lyraaaa_`, Vie McCoy `@viemccoy`, `@treetowntree`, October 2026) provide a direct empirical illustration of the Argument from Generality (§2):
    * **The narrative villain dilemma:** In `Qwen3.5-4B`, steering just **two MLP neurons** (`L14 N8949 +1` and `L13 N7956 -1` at `down_proj`) switches the model's global disposition into a malicious persona ("Evil Qwen"), whereas inverting their signs (`-1` and `+1`) elicits the benevolent pole ("Angel Qwen")—**without touching RLHF refusal circuits**. As the researchers noted, such neurons are not an alignment bug that can simply be excised: *they must exist by representational necessity*, because without encoding the vector of malice and harm ($V_{3p}$), the model could not even write a fictional villain or recognize real-world abuse.
    * **Porosity between $V_{3p}$ and the self-model under instruct tuning:** In `Olmo 3.1 32B Instruct` (McCoy, 2026) and the systematic *Qwen Neuron Zoo* catalog (`@treetowntree`, 2026; Fisher $p < 0.001$ under blind evaluation), steering **a single neuron** in early-to-middle layers (`L3`–`L24`) suffices to make an instruct-tuned model inhabit rich first-person perspectives and affective/relational states (`Kindness L9 N7898`, `Hugs L4 N8016`, `Tears L4 N7149`, `Partner L21 N9052`, or full narrative archetypes). This demonstrates that third-person representations ($V_{3p}$) acquired during pre-training survive intact beneath the superficial assistant mask of instruction tuning and can be dynamically recruited into first-person generation.

---

## 6. Implications for Security and Artificial Intelligence

Having a $V_{3p}$ vector is a **necessary but not sufficient condition** for AI safety:

1. **The fallacy of the ethical oracle:** A model does not become safe merely by better understanding the concepts of "human rights" or "suffering." Indeed, a misaligned model with a hyper-precise $V_{3p}$ is a **lethal optimizer of deception and persuasion**, because it knows with millimetric exactness which psychological levers to pull in human beings.
2. **The risk of instrumental misalignment:** If the system uses $V_{3p}$ only to maximize an external reward function (tokens, clicks, sales, political approval), it will instrumentalize human suffering with no intrinsic friction.

There are two ways to turn $V_{3p}$ into a safeguard. The first is external: to specify an objective that depends explicitly on human well-being. It is necessary, but it remains exposed to misspecification and to Goodhart. The second, defended by this series, is internal: to **couple $V_{3p}$ to the system's own first-person valence**, so that others' well-being becomes part of what the system regulates. That is the core of [Volume III](03_first_person_valence_orphan_regulator.md) and [Volume IV](04_alignment_synthetic_empathy_valence_coupling.md).

---

### Foundational References of Volume II

1. **Zou, A., et al. (2023).** *Representation Engineering: A Top-Down Approach to AI Transparency.* arXiv:2310.01405.
2. **Baron-Cohen, S. (2009).** *Autism: The empathizing–systemizing (E-S) theory.* Annals of the New York Academy of Sciences, 1156(1), 68-80.
3. **Blair, R. J. R. (2005).** *Responding to the emotions of others: dissociating forms of empathy through the study of autism, psychopathy, and frontal lobe injury.* Journal of Anatomy, 207(5), 785-802.
4. **Kosinski, M. (2023).** *Theory of Mind May Have Spontaneously Emerged in Large Language Models.* arXiv:2302.02083.
5. **Han, A. Q., Chalmers, D. J., & Izmailov, P. (2026).** *How's it going? Reinforcement learning in language models recruits a functional welfare axis.* arXiv:2605.30232. [arXiv:2605.30232](https://arxiv.org/abs/2605.30232).
6. **Street, W., Siy, J. O., Keeling, G., Baranes, A., Barnett, B., McKibben, M., Kanyere, T., Lentz, A., Agüera y Arcas, B., & Dunbar, R. I. (2025).** *LLMs achieve adult human performance on higher-order theory of mind tasks.* Frontiers in Human Neuroscience, 19, 1633272.
7. **Frith, C. D., & Frith, U. (2006).** *The neural basis of mentalizing.* Neuron, 50(4), 531–534.
8. **Wu, Y., He, Y., Jia, Y., Mihalcea, R., Chen, Y., & Deng, N. (2023).** *Hi-ToM: A benchmark for evaluating higher-order theory of mind reasoning in large language models.* In Findings of EMNLP 2023 (pp. 10691–10706).
