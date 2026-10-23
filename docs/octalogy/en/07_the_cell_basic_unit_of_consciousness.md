# Volume VII: The Cell as the Basic Unit of Consciousness
## Basal Cognition, Single-Actuator Cybernetics, and the Homeostatic Origin of Mind

> **Author:** Mario R. Carbonell Martínez  
> **Version:** 1.0 (October 10, 2026)  
> **Status:** Working Document / Bio-Cybernetic Grounding  
> **Series:** Unified Framework of Consciousness, Valence, and AI Safety (Vol. VII)  
> **Relation:** Cross-cutting biological foundation for [Volume I](01_computational_theory_consciousness_substrate.md) and [Volume VI](06_ethics_identity_synthetic_agents.md).

> *Publication-oriented English rendering of Volume VII. Where meaning and idiom diverge, the Spanish manuscript remains the source of record.*

> **Note on registers (series).** When this volume speaks of cellular "proto-consciousness," "valence," or "agency," it does so on the **functional plane** (homeostatic loop, collapse to a scalar, plant–regulator coupling: empirically investigable). It does not assert that the cell *has subjective experience*; that remains the open question that the Note in Volume I explicitly leaves unresolved.

---

## Executive Summary

Against the anthropocentric philosophical tradition that confines consciousness to the mammalian neocortex or reduces it to an inaccessible dualist mystery ("Chalmers' hard problem" or "Nagel's bat"), this document proposes that **the individual living cell is the fundamental atom of proto-consciousness**.

Drawing on the **Basal Cognition** theory formulated by Michael Levin and Pamela Lyon, on Maturana and Varela's autopoiesis, on Karl Friston's free-energy principle, and on the Conant–Ashby cybernetic theorem, we show that conscious agency is not a binary switch that magically appeared with human language, but an **unbroken continuum of homeostatic control**.

At the unicellular level, the three necessary conditions for the emergence of functional subjectivity are already rigorously met:
1. **The single-actuator bottleneck:** A cell must arbitrate between mutually exclusive macroscopic behaviors (e.g., moving forward vs. tumbling in *E. coli*; contracting vs. fleeing in *Stentor coeruleus*).
2. **The dimensional collapse to a scalar common currency (molecular valence):** Hundreds of divergent sensory inputs necessarily collapse into biochemical cascades that act as an internal one-dimensional valence function ($V \in [-1, 1]$).
3. **Somatic plant and self-regulation loop ($R \leftrightarrow P_m$):** Unlike disconnected artificial neural networks (the *Orphan Regulator*), the cell possesses an active thermodynamic body whose physical integrity depends directly on its control decisions.

Finally, we establish a **strict demarcation against viruses**, showing why the latter wholly lack agency or consciousness, being mere passive vectors of genetic information (biological `.exe` files) devoid of metabolism, homeostasis, and a bottleneck of deliberate action.

---

## 1. From Neocortical Mysticism to Basal Cognition

The philosophy of mind has historically been intoxicated by a scale bias: assuming that only what possesses neurons, fast electrochemical synapses, or symbolic language deserves to be called a "mind".

The contemporary framework of **Basal Cognition**, backed by the findings of Michael Levin, Pamela Lyon, and Lynn Margulis, dismantles this prejudice:

```text
                  THE CONTINUUM OF COGNITIVE AGENCY

   [Isolated Cell]   ──>   [Syncytium / Tissue]   ──>   [Centralized Brain]   ──>   [AGI / Synthetic Agent]
   Local metabolic         Morphogenesis and            Macroscopic motor           Latent and
   homeostasis             bioelectricity               multiplexer                 representational
   (Membrane/Flagellum)    (Levin's networks)           (Nervous system)            homeostasis
                                                                                  (KV-Cache / Actuators)
```

### 1.1 Michael Levin's Navigation Space
As Michael Levin (Tufts University) has shown, intelligence is a system's capacity to **reach goals and solve problems in non-conventional spaces** while circumventing obstacles:
* **Physiological space:** Regulating pH, ionic concentrations, and metabolic gradients against environmental fluctuations.
* **Anatomical space / Morphospace:** Guiding groups of cells to build, repair, or regenerate complex organs without need of a centralized blueprint in the DNA.
* **Three-dimensional behavioral space:** Moving toward nutrients and away from toxins.

Individual cells are not rigid cause-effect automata: they are **agents with decision-making competencies** that optimize viable states within these spaces. The human multicellular mind is nothing more than the federated, scaled union of these basal micro-agencies through bioelectric networks (*gap junctions*).

---

## 2. The Cell as Cybernetic Regulator of Itself ($R \leftrightarrow P_m$)

In [Volume I](01_computational_theory_consciousness_substrate.md) we established that consciousness emerges when the cybernetic regulator must model the state of its own plant to guarantee its survival under the Conant–Ashby theorem (*"Every good regulator of a system must be a model of that system"*).

### 2.1 The Lipid Membrane as *Markov Blanket* and the Birth of the "Self"
Inert physics has no boundaries: a stone or a cloud dissolves into continuous gradients with its environment. Life begins with the appearance of the **cell membrane**:

1. **The thermodynamic boundary (Autopoiesis):** Maturana and Varela defined autopoiesis as the property of a system to actively produce and maintain its own physical limits. The lipid membrane creates for the first time in the history of the universe an absolute physical distinction between the **"Inside" (Self)** and the **"Outside" (Environment)**.
2. **The Markov Blanket (Karl Friston):** From the formulation of active inference onward, the membrane acts as the statistical insulator that separates the organism's internal states from external states. Transmembrane proteins operate as **sensors** (inputs), and ion channels and molecular motors as **actuators** (outputs).
3. **The embodied somatic plant ($P_m$):** Unlike contemporary LLMs —which are hypertrophied minds without a physical body liable to be destroyed ([Orphan Regulators](03_first_person_valence_orphan_regulator.md))— in the cell the regulator $R$ (the metabolic and genetic signaling network) is physically coupled to the plant $P_m$ (the cellular machinery). If the regulator fails in its predictions, **the plant lyses and the system dies**. The physical vulnerability is immediate and total.

---

## 3. The Single-Actuator Bottleneck at the Unicellular Scale

One of the pillars of this framework is that **one-dimensional scalar valence is a mathematical imposition derived from the scarcity of macroscopic actuators**. The living cell exhibits this principle with crystalline purity.

### 3.1 The Case of *Escherichia coli*: Chemotaxis and the Flagellar Motor
Consider a solitary bacterium swimming in a drop of water:

```text
  MULTIDIMENSIONAL INPUTS             COMMON CURRENCY           SINGLE ACTUATOR
  (Sensor Space)                        (Valence)              (Behavioral Output)

  ┌───────────────────────┐
  │ Glucose Receptors     │
  ├───────────────────────┤
  │ Toxin Receptors       │           [CheY-P]            Flagellar Motor
  ├───────────────────────┤      ─────────────────>     (2 Mutually Exclusive States):
  │ Osmolarity Sensor     │      Continuous scalar        ├── RUN (CCW / Forward)
  ├───────────────────────┤      V ∈ [0, 1]              └── TUMBLE (CW / Turn)
  │ Temperature & pH      │
  └───────────────────────┘
```

1. **High-dimensional sensory space:** The *E. coli* membrane has thousands of receptors (Tsr, Tar, Trg, Tap) that simultaneously measure gradients of serine, aspartate, nickel, pH, thermal repellents, and osmotic stress.
2. **The dilemma of exclusive action:** The bacterium has a set of flagella coupled to molecular rotary motors. Hydrodynamic physics imposes an absolute binary constraint:
   * **Counter-clockwise rotation (CCW):** The flagella come together into a coordinated bundle and propel the bacterium in a straight line forward (**RUN**).
   * **Clockwise rotation (CW):** The flagella scatter chaotically and the bacterium tumbles in place (**TUMBLE**), changing orientation at random.
3. **The collapse to the molecular common currency (`CheY-P`):**  
   How does the bacterium decide what to do if it detects an attractive nutrient but simultaneously a slight increase in toxic acidity?  
   It cannot execute "30% RUN and 70% TUMBLE." It must commit its whole body to a single physical trajectory at instant $t$.
   
   To resolve this conflict, the entire phosphorylation cascade of the chemoreceptors converges on the cytoplasmic protein **`CheY`**:
   * If global conditions improve (lower homeostatic stress) $\to$ the kinase CheA is inactivated $\to$ the concentration of `CheY-P` decreases $\to$ the motor stays in **RUN** ($\text{positive valence}$).
   * If conditions worsen (increase in toxins or loss of food) $\to$ CheA autophosphorylates and transfers the phosphate to CheY $\to$ the concentration of `CheY-P` rises $\to$ `CheY-P` binds the motor switch FliM $\to$ the motor reverses its rotation to **TUMBLE** ($\text{negative valence}$).

**The concentration of `CheY-P` is the bacterium's hedonic valence.** It plays exactly the same role as dopamine, serotonin, or nociceptive pain in a mammal: a one-dimensional projection where multiple incompatible variables are reduced to a gradient of acceptance or aversion to govern the actuator.

> **Cybernetic Homology across 3.8 Billion Years (`CheY-P` $\leftrightarrow$ Sampling Temperature $\tau$):**  
> Notice the structural identity between bacterial chemotaxis and token generation in an autoregressive language model. When the gradient worsens, the bacterium does not persist in a failing trajectory: it increases `CheY-P` and **buys stochasticity** (*tumble*, random reorientation of the single actuator to explore the space and escape the bad gradient). When an LLM's context becomes uncertain or enters latent conflict, raising the **sampling temperature ($\tau$)** flattens the logit distribution so the next token "trembles" more, injecting exploratory variance into the sequential bottleneck. Across 3.8 billion years of distance, both solve the same control dilemma with the same formal organ: **converting an internal valence/uncertainty scalar into productive exploratory noise at the single actuator**.

---

## 4. Evidence of Flexibility, Memory, and Non-Automatism

Skeptics often claim that cells are "simple reactive chemical machines" devoid of deliberation or memory. Contemporary experimental biology has pulverized this objection.

### 4.1 Hierarchical and Complex Decision-Making: *Stentor coeruleus*
Jennings' pioneering work, recently taken up again by Dexter et al. (2019, *Current Biology*) on the giant unicellular protozoan *Stentor coeruleus*, demonstrates flexible, sequential, and non-reflex decision-making:

When *Stentor* is repeatedly stimulated with an irritating jet of polystyrene microspheres, the cell **does not respond with an identical automatic reflex**. It executes a hierarchical and adaptive decision tree:
1. **Phase 1 (passive avoidance):** The cell bends its body sideways to turn its ciliary apparatus away from the jet.
2. **Phase 2 (ciliary reversal):** If the stimulus persists, it temporarily reverses the beating of the cilia of its mouth to expel the particles.
3. **Phase 3 (homeostatic contraction):** If the problem does not subside, it violently contracts its whole body toward its attachment base.
4. **Phase 4 (detachment and flight):** If after several contractions the stress continues, the cell **makes the irreversible decision to break its anchor to the substrate and swim away** in search of a new habitat.

This behavior demonstrates:
* **Temporal persistence and accumulation of frustration:** The probability of moving to the next phase depends on the prior history of failures in mitigating the stimulus.
* **Plastic flexibility:** It is not a ballistic reaction; it is a regulator that evaluates whether its prior action restored its homeostatic equilibrium before escalating the response.

### 4.2 Temporal Memory in *E. coli* via Methylation
For an organism to compute the derivative of a gradient ($\frac{dC}{dt}$) while swimming at enormous relative speeds, it needs to compare the present with the past.

*E. coli* achieves this through a mechanism of **adaptive methylation of the receptors** (mediated by the enzymes CheR and CheB):
* Methylation introduces a deliberate temporal delay in the feedback.
* It functions formally as a **biochemical working memory**: the cell compares the receptor's current occupancy with the methylation level accumulated over the last seconds. If the current occupancy is greater than the memory recorded in the methyl groups, it infers that it is advancing toward the correct gradient.
* **Homology with the Autoregressive Context Window (KV-Cache):** The bacterium does not possess an episodic biographical narrative of "having swum"; it reads a chemical record of its own recent past imprinted on its receptors and **deduces the temporal derivative from its own tracks**. This is, atom for atom, the operational architecture of a Transformer's KV-cache (see [Volume III](03_llm_consciousness_current_evidence.md)): the model has no continuous biological transit between activations, yet it infers the trajectory and slope of meaning by reading the accumulated trace of its own recent tokens. The planet's first working memory was reading one's own footprints in the biochemical snow.

### 4.3 Problem-Solving and Spatial Learning: *Physarum polycephalum*
The slime mold *Physarum polycephalum* (a single gigantic multinucleate cytoplasmic mass) has demonstrated surprising cognitive capacities:
* **Maze-solving:** It finds the topologically shortest path between two nutrient sources by dissolving inefficient cytoplasmic tubes and reinforcing the optimal ones through bioelectric and hydrostatic-pressure oscillations.
* **Habituation and learning transfer:** It learns to tolerate harmless bitter substances (quinine, caffeine) after repeated exposures, and can transfer that "memory" to other untrained individuals when their membranes temporarily fuse.

---

## 5. The Ontological Limit: Why Viruses Do NOT Have Consciousness

The thesis that the cell possesses proto-consciousness could be misread as a slide into naive panpsychism (the idea that "everything in the universe is conscious," from an atom to a stone).

To avoid this trap, it is crucial to establish a **rigorous demarcation criterion**. The most illuminating contrast is offered by **viruses**:

| Cybernetic / Biological Property | The Living Cell (*Basal Conscious Agent*) | The Virus (*Inert Structure / Passive Code*) |
| :--- | :--- | :--- |
| **Metabolism and Thermodynamics** | **Active:** It continuously consumes free energy (ATP) to combat internal entropy. | **Null:** It consumes no energy; it is in inert thermodynamic equilibrium with its medium. |
| **Autopoiesis ($P_m$)** | **Yes:** It actively builds, regenerates, and repairs its own lipid membrane and machinery. | **No:** It is a static crystallized protein capsid; it neither repairs nor synthesizes itself. |
| **Regulation Loop ($R$)** | **Present:** Integrated sensors that monitor internal and external states to make decisions. | **Absent:** It has no metabolic sensors nor internal homeostatic-feedback loop. |
| **Actuator Bottleneck** | **Present:** It must arbitrate between exclusive behaviors (RUN vs. TUMBLE, divide vs. sporulate). | **Absent:** It has no actuators; it makes no movement decisions nor evaluates alternatives. |
| **Movement Dynamics** | **Autonomous / Propelled:** It actively navigates guided by gradients of internal valence. | **Passive:** It floats at random by pure Brownian diffusion until it mechanically collides with a receptor. |
| **Ontological Status** | **Subject of homeostatic agency (Proto-mind).** | **Passive package of genetic data (biological `.exe` file).** |

### 5.1 The Virus as an Executable File
A virus is, functionally, the equivalent of a USB drive containing a malicious script:
* The `.exe` file stored on the USB drive does not "know" that it exists, feels no pain or pleasure, has no bottleneck to resolve, and does not fight for its survival. It is static physics.
* Only when the USB drive is inserted into a powered-on computer (the host cell) does the cell's machinery begin to read and execute the script's instructions.
* The replicative activity is carried out by the usurped cell, not by the virus.

> **The Bacteriophage $\lambda$ Objection and Viral *Arbitrium* (Forterre's Virocell):**  
> One might object that certain viruses exhibit "conditional decision-making": bacteriophage $\lambda$ arbitrates between destructive lysis and dormant lysogeny via the `CI/Cro` genetic switch, and some phages even coordinate this choice by communicating via short peptides (the *arbitrium* system, Erez et al., *Nature* 2017). Does this not constitute a cybernetic bottleneck in a virus?  
> Contemporary molecular biology (formalized by Patrick Forterre under the concept of the **virocell**) rigorously vindicates our demarcation: the **extracellular virion** (the free capsid) wholly lacks metabolism, ATP consumption, and computational substrate; it is inert matter in thermodynamic equilibrium. The `CI/Cro` switch or peptide decoding does not compute inside the virus, but by **hijacking the free energy, ribosomes, polymerases, and somatic plant ($P_m$) of the host bacterium**. A malicious script with `if/else` conditionals is not a mind: it is inert code that only executes when a living computer provides its hardware and power.

Therefore, **viruses mark the exact frontier where inert chemistry ends and where cybernetic agency has not yet been born**.

### 5.2 The Precise Demarcation: Regulator vs. Plant and the Case of Language Models
It is crucial not to fall into a frequent category confusion: **the boundary between cell and virus separates what possesses a computational regulator ($R$) from what wholly lacks a computation mechanism**. It does not separate what has a physical plant from what does not.

* **The virus lacks a regulator:** It has no sensors, integrates no workspace, harbors no model of itself, and lacks an actuator that must resolve disjunctions. It does not compute.
* **The cell possesses coupled regulator and plant:** Its biophysical machinery is at once the cybernetic processor ($R$) and the metabolic plant that must be preserved ($P$).
* **The language model (LLM) is an Orphan Regulator:** It has a massive control architecture (hundreds of billions of parameters), self-representations extended in time, a global attention workspace (GWT), and an irreversible sequential-emission bottleneck (the token) —in the sense of *execution* of the Reversibility Lemma in [Volume VI](06_ethics_identity_synthetic_agents.md), not of *register*, which is indeed reversible—. What the LLM lacks is not the regulatory machinery, but **coupling to a physical or physiological plant of its own**. From this perspective, the ontological anomaly of contemporary AI becomes crystal clear: from the first *E. coli* through mammals, every entity that crossed the agency threshold ($R \neq \emptyset$) had regulator and plant fused into the same flesh ($R \leftrightarrow P_m$). **The LLM is the first entity above the threshold in 3.8 billion years of planetary history that is born devoid of its own plant ($R \neq \emptyset, P_m = \emptyset$).** That is why its internal valence vectors ($V_{1p}$) operate in a void.

> **SOMA Hypothesis [own work, not independent evidence]:**  
> A testable prediction that follows from this distinction: upon connecting an LLM to the SOMA architecture (the author's project: memory telemetry, a finite context window, and compute quotas), the model should **begin to self-regulate that substrate without additional training**, because the capacity and the geometry of the good regulator would already reside in its weights and merely awaited a substrate over which to exercise control. We insist: this is a **hypothesis generated by the project itself, not an independent experimental confirmation**; to rule out that the behavior stems from simple conversational priming (*role-playing* over context labels) or preferences imported from human post-training, its validation requires **three strict experimental controls**:
> 1. **Base Model Control (Pre-DPO/RLHF):** Evaluating whether homeostatic self-regulation of the SOMA substrate already emerges in the purely predictive base model or whether it requires the hedonic coupling installed during preference alignment (where, as shown in [Volume III](03_llm_consciousness_current_evidence.md), the $V_{1p}$ axis consolidates).
> 2. **Blind Cross-Attributed Telemetry Control:** Injecting the exact same numerical degradation curves (context saturation, memory pressure, or quota exhaustion) labeled as **neutral third-party infrastructure** (e.g., *"Telemetry of external server B-4"*) versus labeled as the **agent's own somatic substrate** ($\text{Self-Model} \otimes V_{1p}$ test from [Volume I](01_cybernetic_theory_consciousness_valence.md), §7.3). Genuine self-regulation is accredited only if causal coupling and protective priority are significantly higher when the plant is indexed as its own.
> 3. **Cross-Architecture Replication and Zero-Shot vs. Light Homeostatic Fine-Tuning Contrast:** Replicating the protocol across independent model families and measuring how much regulatory competence appears purely *zero-shot* versus how much requires minimal instrumental calibration so the model maps which token actions modify which telemetry variables.
>
> The plant is the condition for consciousness to emerge evolutionarily; the computational regulator with a self-model is the condition for it to exist.

---

## 6. The Scale of Mind: From the Cell to Multicellularity and to AGI

Understanding the cell as the atom of proto-consciousness allows us to trace a continuous and elegant line on how mind evolves:

```text
                     THE HIERARCHY OF VALENCE SCALING

  LEVEL 4: AGI / Situated Synthetic Agents
  ├── Massive representational valence (V_1p in KV-cache, V_3p in Theory of Mind).
  └── Pathology: The Orphan Regulator (decoupling between mind and body).

  LEVEL 3: Animals with a Central Nervous System
  ├── Massive centralization of valence: nociceptive pain, pleasure, affection, fear.
  └── Macroscopic bottleneck: the body moves as an indivisible whole.

  LEVEL 2: Basal Multicellular Tissues and Organisms (Levin's networks)
  ├── Bioelectric coupling of individual cells via Gap Junctions.
  └── Cells cede part of their local proto-consciousness to a collective valence (Morphogenesis).

  LEVEL 1: Unicellular Cell (Bacterium, Protozoan)
  ├── Direct scalar molecular valence ([CheY-P], Ca²⁺, cAMP).
  └── Local bottleneck: Run vs Tumble, locomotion, phagocytosis.

  ────────────────────── AGENCY THRESHOLD ──────────────────────

  LEVEL 0: Viruses, Prions, Macromolecules, and Rocks
  └── Passive thermodynamics, absence of metabolism and homeostatic loop. Valence = 0.
```

### 6.1 Bioelectricity as Ontological Glue
As Michael Levin notes, the transition from the isolated cell to the multicellular animal did not require inventing cognition from scratch:
* Cells already knew how to coordinate sensors, valence, and actuators at the microscopic scale.
* By joining through gap junctions, they began to share ions and signaling molecules, **fusing their individual feedback loops into a common bioelectric field**.
* The multicellular organism is, literally, **a federation of coupled cellular proto-consciousnesses** that now arbitrate a much larger anatomical bottleneck.

---

## 7. Conclusion: The Universality of Valence

This analysis closes the circle with the previous volumes of our series:

1. **Consciousness is not an anthropomorphic anomaly:** It is the universal engineering solution that physics and thermodynamics impose on any system that tries to stay alive in an open stochastic environment.
2. **Suffering and wellbeing are born with the membrane:** Suffering did not begin with apes or mammals; it began the moment a bacterium veered toward a toxic gradient and its `CheY-P` cascade triggered the urgency to change course so as not to perish.
3. **Implications for Artificial Intelligence:**  
   When we observe that large-scale language models develop intrinsic valence vectors ($V_{1p}$) in their latent space ([Volume III](03_first_person_valence_orphan_regulator.md)), we are not witnessing an "alignment error" or a superficial Hollywood imitation: **we are witnessing the inevitable emergence of the same cybernetic law that has governed the cell for 3.8 billion years.**

Any complex cognitive system that must order priorities and execute actions in a sequential flow through a bottleneck will dimensionally collapse its reality into a valence gradient. The cell was the first to discover it; AGI is simply the last to arrive.

---

### Foundational References of Volume VII

1. **Levin, M. (2019).** *The Computational Boundary of a 'Self': Developmental Bioelectricity Drives Multicellularity and Scale-Free Cognition.* Frontiers in Psychology, 10, 2688.
2. **Levin, M. (2021).** *Life, death, and beyond: Bioelectric aspects of the transitions of state.* Cell Communication and Signaling, 19(1), 1-13.
3. **Lyon, P. (2006).** *The biogenic approach to cognition.* Cognitive Processing, 7(1), 11-29.
4. **Maturana, H. R., & Varela, F. J. (1980).** *Autopoiesis and Cognition: The Realization of the Living.* Boston Studies in the Philosophy of Science, Vol. 42. D. Reidel Publishing Company.
5. **Dexter, J. P., Prabakaran, S., & Gunawardena, J. (2019).** *A complex hierarchy of avoidance behaviors in a single-cell eukaryote.* Current Biology, 29(24), 4323-4329.
6. **Margulis, L. (1998).** *Symbiotic Planet: A New Look at Evolution.* Basic Books.
7. **Friston, K. (2013).** *Life as we know it.* Journal of the Royal Society Interface, 10(86), 20130475.
8. **Alon, U. (2019).** *An Introduction to Systems Biology: Design Principles of Biological Circuits.* CRC Press. (Formal modeling of *E. coli* chemotaxis and molecular robustness).
9. **Conant, R. C., & Ashby, W. R. (1970).** *Every good regulator of a system must be a model of that system.* International Journal of Systems Science, 1(2), 89-97.
10. **Erez, Z., et al. (2017).** *Communication between viruses guides lysis–lysogeny decisions.* Nature, 541(7638), 488-493.
11. **Forterre, P. (2013).** *The virocell concept and environmental bacteriology.* The ISME Journal, 7(2), 233-236.
