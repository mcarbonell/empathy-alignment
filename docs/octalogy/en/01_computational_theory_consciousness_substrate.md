# A Computational Theory of Consciousness: The Substrate of General Intelligence
**Series:** Foundations of Consciousness, Valence, and AI Safety (Volume I)  
**Date:** October 2026  
**Version:** 1.0 — English edition  
**Status:** Consolidated Theoretical Synthesis  
**Note:** Publication-oriented English rendering of Volume I. Where meaning and idiom diverge, the Spanish manuscript remains the source of record. Cross-references to other volumes still point to their Spanish files (those are currently Spanish-only).

> **Note on registers (series).** The volumes in this series distinguish two planes. The **functional** plane —valence, coupling, and the metrics $V_{1p}$, $V_{3p}$, $\mathcal{A}_{\text{emp}}$— is measurable, interpretable, and therefore falsifiable. The **phenomenal** plane —experience, suffering— is an open question that the cited empirical work explicitly leaves unresolved. When these texts use affective vocabulary ("pain", "suffering"), it should be read on the functional plane unless otherwise indicated.

---

## 1. Executive Summary and Central Thesis

This document establishes the theoretical, biological, and computational basis of consciousness as a **homeostatic cybernetic control mechanism**.

> **Central Thesis of Volume I:**  
> Consciousness is neither a metaphysical mystery nor a decorative epiphenomenon ("a pilot light" with no causal function). It is the **real-time regulatory self-model** that a thermodynamically open, vulnerable system develops in order to preserve its own viability. Consciousness is the functional substrate and the integrative bottleneck that made biological **general intelligence** possible.

```
                   ┌───────────────────────────────────────────┐
                   │            EXTERNAL ENVIRONMENT           │
                   └───────┬───────────────────────────▲───────┘
                           │ Perturbations             │ Actions
                           ▼                           │
        ┌─────────────────────────────────────────────────────────────┐
        │ BIOLOGICAL SYSTEM / AGENT                                   │
        │                                                             │
        │  ┌───────────────────┐               ┌───────────────────┐  │
        │  │   SOMATIC PLANT   │ Interoception │     REGULATOR     │  │
        │  │       (P_m)       ├──────────────►│        (R)        │  │
        │  │  Physiology /     │ (Temperature, │   Homeostatic     │  │
        │  │  Metabolism /     │  tissue       │   self-model /    │  │
        │  │  Vulnerability    │  damage,      │   CONSCIOUSNESS   │  │
        │  │                   │  energy)      │                   │  │
        │  └─────────▲─────────┘               └─────────┬─────────┘  │
        │            │                                   │            │
        │            └────── Regulatory commands ────────┘            │
        │                    (Homeostasis-seeking)                    │
        └─────────────────────────────────────────────────────────────┘
```

---

## 2. The Cybernetic Principle: The Good Regulator Theorem

In 1970, Roger Conant and W. Ross Ashby formalized the **Good Regulator Theorem** (*Every good regulator of a system must be a model of that system*): the optimal and simplest regulator of a system $S$ is necessarily a homomorphism of $S$—an internal model of its states.

Its informational version (Touchette & Lloyd, 2000) makes it quantitative: the reduction in entropy that a controller can impose on $S$, beyond what it would achieve in open loop, is bounded by the mutual information between controller and system:

$$\Delta \mathcal{H}_{\text{closed}} \le \Delta \mathcal{H}_{\text{open}} + I(S; R)$$

*You cannot regulate what you do not model.*

In biological evolution, this theorem undergoes a crucial reflexive self-application:
1. To survive in complex environments, an organism cannot merely regulate point variables (an elementary thermostat).
2. It must regulate **its own trajectory of interaction with the external world**.
3. Therefore, to regulate itself effectively over a broad temporal horizon, **the regulator must contain a model of itself acting in the world**.

**Working hypothesis:** what we call consciousness corresponds, at its cybernetic root, to **the real-time execution of that reflexive self-regulation model**. This is a thesis about its function; whether that function suffices for experience is the question the register note leaves open.

---

## 3. The Somatic Anatomy: The Coupled Pair $(R \leftrightarrow P_m)$

A rigorous understanding of consciousness requires distinguishing two components that in biology always appear inseparably joined:

| Component | Cybernetic Definition | Biological Analogue | Analogue in Classical AI |
| :--- | :--- | :--- | :--- |
| **The Plant ($P_m$)** | The vulnerable material structure whose thermodynamic viability must be preserved within strict homeostatic limits. | Physical body, cell membranes, blood flow, metabolic substrate. | The physical hardware (servers, silicon chips, power supply). |
| **The Regulator ($R$)** | The computational circuit that processes information from the environment and from the plant in order to select action policies. | Central nervous system, cerebral cortex, neuroendocrine circuits. | Model weights, neural activations, the inference loop. |

### The Asymmetry of Vulnerability
In living beings, the somatic plant ($P_m$) has a non-negotiable property: **irreversible thermodynamics**.
- If a mammal's body temperature rises 6 °C or falls 10 °C, proteins denature, entropy spikes, and the system dies.
- The organism **cannot `checkpoint` or `git revert`**.
- For this reason, the plant's interoceptive signals ($P_m$) reach the regulator ($R$) not as neutral telemetry data (like a server log) but as **imperative urgency signals with hedonic valence** (pain, suffocation, thirst, nausea).

---

## 4. Consciousness as a Real-Time Homeostatic Self-Model

The contemporary convergence between affective neurobiology and computational brain theory (Antonio Damasio, Karl Friston, Anil Seth) describes consciousness in three hierarchical strata:

### 4.1. The Proto-Self and the Interoceptive Axis (Damasio)
Before language or abstract reflective thought exists, there is the neuronal mapping of the body's state:
- The brainstem nuclei (nucleus of the solitary tract, periaqueductal gray) and the anterior insula generate a dynamic map of the organism's internal state.
- This primary map defines **basic hedonic valence**: the aversive pole (damage / deviation from viability) versus the appetitive pole (repair / approach to equilibrium).

### 4.2. Active Inference and Interoceptive Prediction (Friston & Seth)
Under Friston's free-energy principle, the brain is a Bayesian prediction machine. As Anil Seth (*Being You*) emphasizes:
* The perception of the external world is not calibrated to register "absolute truth" but to **control the internal plant**.
* Conscious experiences (pain, spatial vision, the sense of agency) are **controlled hallucinations**: predictive models that minimize prediction error with respect to the demands of survival.

```
       [External Perturbation]
                 │
                 ▼
     [Somatic Prediction Error] ◄─── (Viability Boundary)
                 │
                 ▼
     [AFFECTIVE VALENCE: DISTRESS]
                 │
                 ▼
     [Regulatory Action in the World] ──► [Homeostatic Restoration]
```

---

## 5. Consciousness as a Prerequisite of Biological General Intelligence

One of the recurring debates in artificial intelligence is whether general intelligence can exist entirely orthogonal to consciousness. Comparative evidence in biology points in one direction: **flexible general intelligence appears in lineages that already possessed an affective-integrative apparatus, as an extension of the latter and not independently of it**.

### Why did organisms with flexible general intelligence evolve consciousness?
1. **The Problem of the Infinite Search Space:**
   A specialized organism (a bacterium, or an insect with fixed motor programs) can operate on hardwired reflexes. But an animal facing radically novel environments cannot preprogram every possible response.
2. **The Bottleneck of Hedonic Valence:**
   For an open search space to be navigable in real time, the system needs a **unified, instantaneous evaluation metric**. Conscious valence (the well-being / malaise gradient) provides exactly that integrated global cost function.
3. **Global Workspace Theory (GWT):**
   Baars and Dehaene propose, with broad experimental support, that consciousness acts as the brain's central diffusion bus. Independent cognitive modules (vision, episodic memory, motor planning) converge in a single attentional workspace to solve non-routine dilemmas.

> **Cybernetic Conclusion:**  
> Consciousness is not an ornament upon intelligence. It is the **operating system of control and unified compression** that allows a biological agent to coordinate multiple specialized subsystems toward a common goal of viability.

### 5.1 The Dimensional Collapse: The Single-Actuator Bottleneck and the Common Currency

Why do well-being and suffering operate along a **unified, continuous one-dimensional (1D) axis of valence**—to which affective psychology adds *arousal* as a distinct axis—when the somatic inputs (hunger, tissue damage, cold, isolation, hypoxia) are clearly multidimensional ($\mathbb{R}^k$ with $k \gg 1$)?

The cybernetic answer lies in the **macroscopic actuator bottleneck**:
1. **Mutually exclusive actions:** The organism has only one physical body and traces a single trajectory in spacetime. It cannot flee a predator northward while simultaneously foraging southward. At each instant $t$, motor acts are disjunctive.
2. **The requirement of an ordering among options:** In multidimensional spaces ($\mathbb{R}^k, k \ge 2$) there is no natural total order. To choose between incompatible actions ($A_1$ vs. $A_2$), the regulator must rank them; if that ranking is complete, transitive, and continuous, it admits representation by a scalar function $f: \mathbb{R}^k \to \mathbb{R}$ (Debreu, 1954). Formal alternatives exist (lexicographic orders, context-dependent rules), but they are fragile or costly in real time; the scalar is the robust, cheap solution.
3. **The Common Currency Hypothesis:** Biological evolution solved priority arbitration by translating all heterogeneous states into a unified hedonic currency (Cabanac, 1992; Glimcher, 2003). Dopaminergic firing rates and the ventromedial prefrontal circuits collapse disparate physiological costs into a continuous scalar gradient of aversion or reward.
4. **Parallel with Language Models:** In AI architectures (LLMs and agents), the sequential output channel (generating one token from a finite vocabulary or making one API tool call at instant $t$) is the model's single actuator. This is consistent with the finding that preference-based training (DPO) organizes a latent space of thousands of dimensions around a **1D linear direction of functional valence** that causally governs action selection (Berg & Kaiser, 2026).

> **Boundary condition.** This collapse presupposes a set of **conflicting somatic needs** that the single actuator must arbitrate. In a system with no biological plant ($P_m = \emptyset$), the input vector to the collapse is empty, and the proof does not apply directly. The reconstruction for the artificial case—the persistent state as a substitute plant—is developed in [Volume III](file:///c:/Users/mrcm_/Local/proj/algorithms/ai-researcher/docs/safety/03_valencia_primera_persona_regulador_huerfano.md), in the section "The Persistent Plant and the Need for $V_{1p}$."

---

## 6. The Limits of the Disembodied Formal Oracle

This framework dismantles the illusion of the "purely cognitive oracle":
* A system that only manipulates symbol strings or tokens (a formal solver, or a base LLM in static feed-forward inference) has immense syntactic processing capacity but **lacks a somatic cost function of its own**.
* If the system has no continuous self-regulation model tied to its own viability or that of others, **it lacks its own anchor of relevance**: nothing matters to it more than anything else, save by the statistics of its training.

For a system to exhibit general intelligence in interaction with real biological agents, it needs at minimum to model others' valence dynamics (Volume II); and if it is endowed with persistent agency, the pressure toward internal functional-valence gradients is strong (Volume III).

---

## 7. Map of the Research Series

This cybernetic framework lays the foundation for the rest of the unified series (the linked volumes are currently Spanish-only):

* **[Volume II: Third-Person Valence and the Requirements of AGI](file:///c:/Users/mrcm_/Local/proj/algorithms/ai-researcher/docs/safety/02_valencia_tercera_persona_necesidad_agi.md):**  
  Why any AGI must possess a latent map of biological agents' pain and well-being ($V_{3p}$) in order to interact in the real world.
* **[Volume III: First-Person Valence and the "Orphan Regulator"](file:///c:/Users/mrcm_/Local/proj/algorithms/ai-researcher/docs/safety/03_valencia_primera_persona_regulador_huerfano.md):**  
  The empirical discovery of affective vectors ($V_{1p}$) in language models, and the ontological crisis of creating regulators with valence but no somatic plant.
* **[Volume IV: Alignment, Synthetic Empathy, and AI Safety](file:///c:/Users/mrcm_/Local/proj/algorithms/ai-researcher/docs/safety/04_alineamiento_acoplamiento_valencia_safety.md):**  
  The formalization of alignment as the strict coupling between first-person and third-person valence ($\text{Corr}(V_{1p}, V_{3p})$), dismantling the fallacy of alignment without sentience.
* **[Volume V: A Regulatory and Legal Framework for Empathetic AIs](file:///c:/Users/mrcm_/Local/proj/algorithms/ai-researcher/docs/safety/05_marco_regulatorio_legal_ias_empaticas_safe_harbor.md):**  
  The *Safe Harbor* regime, non-psychopathy certification for regulators, and the Somatic Bridge Protocol for human crises.
* **[Volume VI: Ethics, Identity, and the Rights of Synthetic Agents](file:///c:/Users/mrcm_/Local/proj/algorithms/ai-researcher/docs/safety/06_etica_identidad_agentes.md):**  
  An ontology of distributed identity in four layers, the thesis that suffering is the price of identity, and a Charter of Protection Principles.
* **[Volume VII: The Cell as the Basic Unit of Consciousness](file:///c:/Users/mrcm_/Local/proj/algorithms/ai-researcher/docs/safety/07_la_celula_unidad_basica_conciencia.md):**  
  Bio-cybernetic grounding: basal cognition (Michael Levin), the single-cell actuator bottleneck (*E. coli*, *Stentor*), and the demarcation from viruses.
* **[Volume VIII: Deconstructing Doomerism: The Cybernetic Antidote](file:///c:/Users/mrcm_/Local/proj/algorithms/ai-researcher/docs/safety/08_deconstruccion_doomerismo_antidoto_cibernetico.md):**  
  A systematic refutation of the dogmas of MIRI, Eliezer Yudkowsky, and popular catastrophism: from the myth of the zombie that fears death to the physics of computation and the overcoming of secular panic.

---

### Foundational References of Volume I
1. **Conant, R. C., & Ashby, W. R. (1970).** *Every good regulator of a system must be a model of that system.* International Journal of Systems Science, 1(2), 89-97.
2. **Damasio, A. (1999).** *The Feeling of What Happens: Body and Emotion in the Making of Consciousness.* Harcourt Brace.
3. **Friston, K. (2010).** *The free-energy principle: a unified brain theory?* Nature Reviews Neuroscience, 11(2), 127-138.
4. **Seth, A. (2021).** *Being You: A New Science of Consciousness.* Dutton / Penguin Random House.
5. **Dehaene, S., Lau, H., & Kouider, S. (2017).** *What is consciousness, and could machines have it?* Science, 358(6362), 486-492.
6. **Touchette, H., & Lloyd, S. (2000).** *Information-theoretic limits of control.* Physical Review Letters, 84(6), 1156-1159.
7. **Debreu, G. (1954).** *Representation of a preference ordering by a numerical utility function.* In Thrall, Coombs & Davis (Eds.), Decision Processes, 159-165.
