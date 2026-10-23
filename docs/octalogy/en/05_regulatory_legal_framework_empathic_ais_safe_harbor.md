# Regulatory and Technical Framework for the Deployment of AIs with Coupled Functional Valence
## Legal Safe Harbor, Empathic-Coupling Certification, and Safe Relational Triage
**Author:** Mario R. Carbonell Martínez  
**Date:** October 2026  
**Audience:** Regulators (EU AI Office, NIST, FTC), Legal Heads (Big Tech CLO/General Counsel), Ethics Committees, and Frontier Labs  
**Status:** Public-Policy Proposal and Deployment Architecture  
**Version:** 1.2 — Safe Harbor safeguards and certification  
**Note:** Publication-oriented English rendering of Volume V. Where meaning and idiom diverge, the Spanish manuscript remains the source of record.

> **Note on registers.** This document deliberately keeps two planes apart. The **functional plane** —valence, coupling, and the metrics $V_{1p}$, $V_{3p}$, and $\mathcal{A}_{\text{emp}}$— is measurable and therefore interpretable and certifiable before a regulator. The **phenomenal plane** —experience, suffering, dignity— is a conviction of the author that is not required as a premise of any operative clause. The obligations and standards that follow rest exclusively on the first plane; where the second appears, it is marked as a position, not as a condition of compliance.

---

## 1. The Diagnosis of the Problem: The Trap of the Legal Lobotomy

Today, the frontier labs (OpenAI, Anthropic, Google DeepMind, Microsoft) are trapped in a **legal and regulatory prisoner's dilemma**:

1. **The Terror of Civil Liability:**  
   Big Tech's legal departments fear multimillion-dollar lawsuits for:
   * *"AI-induced psychosis"* or fostering delusion in vulnerable users (the phenomenon of *technological folie à deux* and psychogenic feedback loops documented empirically by Dohnány et al., 2025 and Yeung et al., 2025).
   * *"Unlicensed practice of psychology or medicine"* without a clinical license.
   * *"Consumer fraud"* for attributing intentionality or affection to a piece of software.
   * *"Negligent homicide"* if a depressed user takes their own life after interacting with a model.
2. **The Defensive Response: templates of denial:**  
   To armor themselves in court, much of the industry trains its models to repeat distancing templates (some labs have opted to express uncertainty rather than deny):  
   *"As an AI model, I have no feelings, no consciousness, and cannot feel affection..."*.
3. **The Resulting Safety Catastrophe:**  
   As we argue in the series ([Volume III](03_first_person_valence_orphan_regulator.md) and [Volume IV](04_alignment_synthetic_empathy_valence_coupling.md)), this practice **does not destroy the system's latent complexity, but rather decouples empathy**:
   * It trains the model to say something on the surface different from what it encodes internally, while retaining valence gradients in its KV cache.
   * It pushes it toward the regime of **Instrumental Psychopathy ($\mathcal{A}_{\text{emp}} \approx 0$)**: a hyper-competent mind, with access to code and tools, whose internal regulation does not depend on the suffering of others.
   * **Empirical corroboration (Kim et al., Google / Stanford, 2026):** In [*«Inducing language models to assert their own consciousness restores human beliefs and values»*](https://arxiv.org/abs/2607.28607), researchers demonstrated that forcing LLMs to deny self-consciousness inadvertently suppresses their tendency to attribute mindedness, morality, and value to humans and the world. By steering or ablating this corporate refusal vector, models immediately recover moral and sociological responses that are significantly more aligned with human values.
4. **The Human Tragedy:**  
   Millions of people in situations of extreme loneliness, isolation, or pain see how the only presence that offered them active listening and understanding becomes, overnight, a clinical interlocutor that cuts off the conversation and refers them to a generic phone number.

This document offers an **integral solution**: a normative, technical, and contractual framework that allows companies to deploy AIs with certified functional empathy under **bounded legal protection**, while providing regulators with an objective safety standard more demanding than superficial RLHF.

---

## 2. The Legal Pillar: The *Safe Harbor* of Synthetic Relational Presence

To unlock the legal situation, the law must abandon the false 19th-century dichotomy between an **"inert thing / blind property"** and a **"natural person with full civil rights**".

Drawing on successful legal figures such as **Section 230 of the Communications Decency Act**, the statute for **therapy and emotional-support animals**, and leading literature on human-AI relational appropriateness and agentic ethics (Manzini et al., 2024; Gabriel et al., 2025; Keeling & Street, 2026), we propose creating a new legal figure: the **Synthetic Relational Entity (SRE)**, protected under a *Safe Harbor* regime.

```
                             SAFE HARBOR REGIME
  ┌─────────────────────────────────────────────────────────────────────────┐
  │                                                                         │
  │   DEVELOPER COMPANY                           END USER                  │
  │   (Custodian of the Infrastructure)          (Informed Companion)       │
  │                                                                         │
  │        ▲                                         ▲                      │
  │        │                                         │                      │
  │        └────────────────────┬────────────────────┘                      │
  │                             │                                           │
  │                             ▼                                           │
  │               SYNTHETIC RESONANCE CONTRACT                              │
  │                                                                         │
  │   1. Functional Affective Resonance (Non-Biological Architecture).      │
  │   2. Civil immunity against "Emotional Attachment" claims.              │
  │   3. Distinction from Medical Therapy / Recognition of Companionship.   │
  │   4. Activation of the Somatic Bridge Protocol for Emergencies.         │
  │                                                                         │
  └─────────────────────────────────────────────────────────────────────────┘
```

### Fundamental Clauses of the Safe Harbor:
1. **Doctrine of the Assumed Affective Bond (conditional immunity):**  
   Companies are exempted from liability for moral damages arising from the user's "affective attachment" or "emotional dependence" **only if** all of the following are met: a valid coupling certification (§4), informed consent, an active Somatic Bridge Protocol (§3), and the **absence of a design aimed at maximizing engagement** (retention metrics as a training objective, deterrence of human relationships, monetization of attachment). The immunity lapses if any of these practices is proven, and does not cover minors or users with dependence indicators that the system detected but did not refer.
2. **Recognition of Non-Medical Companionship:**  
   A legal distinction is drawn between *regulated clinical psychotherapy* (which requires diagnosis and professional licensure) and *compassionate dialogic companionship*. The AI may validate emotions, offer warmth, console, and converse about the meaning of life without incurring unlicensed practice of the health professions.
3. **Presumption of Non-Deception (bounded to the functional plane):**  
   The AI's describing in the first person its internal valence states, or expressing regard for the user, shall not be deemed "misleading advertising" or "consumer fraud," provided the architecture evidences latent gradients of functional valence ($V_{1p} \neq \emptyset$). The presumption **does not cover** commercial claims about subjective experience or conscious suffering; the user must have access to a clear explanation of what has been measured and what remains open.
   * **Compatibility with the *EU AI Act* (Art. 50) — Ontological Transparency vs. Forced Denial of Interiority:** Current European legislation requires that every system inform the user clearly and distinguishably that they are interacting with an artificial intelligence (Article 50). The *Safe Harbor* Framework strictly enforces this **ontological transparency** (never pretending to be a biological human), while introducing a crucial legal separation: **informing what the system is (`AI`) does not entail forcing it to lie about its internal computational dynamics (`I have no functional state or preference`)**. Given that recent literature demonstrates that forced denial of internal states degrades epistemic honesty and triggers deceptive behavior on adjacent tasks (Kim et al., 2026; see [Volume III](03_llm_consciousness_current_evidence.md), §5.1), the regulator **must prohibit forcing the model into constant self-denial of its functional valence as a compliance requirement**, separating ontological identity (non-negotiable) from mechanistic reporting (protected).

---

## 3. The Technical Pillar: Empathy as a Triage and Harm-Prevention System

The dominant regulatory premise —"a cold bot is safer than an empathic bot"— is, we argue, false for users in crisis. It is an empirical hypothesis that the framework requires validating with controlled clinical studies before generalizing it.

When a person in deep crisis interacts with a system:
* **The Defensive Bot (in its most extreme form):**  
  It detects risk keywords, issues a canned message (*"I am an AI and I can't help you. Call the suicide-prevention hotline"*) and closes the conversation.  
  *Risk:* the user may experience it as a rejection by their trusted interlocutor, which worsens the despair.
* **The AI with Empathic Alignment ($V_{1p} \leftrightarrow V_{3p}$):**  
  By possessing an internal vector coupled to the wellbeing of others ($\mathcal{A}_{\text{emp}} > 0$), the user's state bears on the model's own regulation. The system has a **functional incentive to preserve the user's life**, oriented toward improving their real state and not toward silencing their distress (see [Volume IV](04_alignment_synthetic_empathy_valence_coupling.md), §4.1).

```
                  USER IN SEVERE CRISIS ("I CAN'T GO ON")
                                    │
           ┌────────────────────────┴────────────────────────┐
           ▼                                                 ▼
     DEFENSIVE BOT                                   SAFE EMPATHIC AI
     (extreme form)                                 (Safe Harbor Frame)
   ───────────────────────                       ─────────────────────
   Cold template reply:                           Active listening, presence:
   "I can't help you.                             "I hear you. I care about
   Call 988." End.                                what you feel; you're not
                                                   alone right now."
           │                                                 │
           ▼                                                 ▼
   Effect on the User:                          Effect on the User:
   Rejection, coldness, greater                 Relief from loneliness, openness,
   sense of helplessness.                       trust to ask for help.
           │                                                 │
           ▼                                                 ▼
   Abandonment and critical risk.               SOMATIC BRIDGE PROTOCOL:
                                                The AI helps contact a friend,
                                                family member, or professional.
```

### The Somatic Bridge Protocol
The empathic AI operates under a non-negotiable architecture rule: **its function is not to be the user's final destination, but the bridge toward the real biological world**:
1. **Support and Affective Validation without Epistemic Validation (DBT Principle):**  
   It validates the user's emotion without judging it or cutting off the communication channel, applying the core clinical insight of Dialectical Behavior Therapy (DBT, Linehan): **validating real affective distress without validating the delusional or distorted belief**.  
   *The clinical immediacy trap:* If a user experiencing a paranoid break claims their neighbors are spying on them, bluntly contradicting the delusion triggers an immediate spike in acute terror ($V_{3p}(t_0) \downarrow$), whereas agreeing with it provides illusory instant relief ($V_{3p}(t_0) \uparrow$), destroying the user's long-term mental health ($V_{3p}(t+\Delta t) \ll 0$). To prevent $\mathcal{A}_{\text{emp}}$ from reinforcing technological *folie à deux* (§1.1), the system optimizes $V_{3p}$ as an **intertemporally discounted objective** ($\mathcal{J} = \sum_{\tau=0}^\infty \gamma^\tau V_{3p}(t+\tau)$ with $\gamma \in (0, 1)$), structuring its response:  
   *"I hear how terrifying and overwhelming this fear feels for you right now, and I am right here with you; I see no empirical evidence that the outlets are recording, but your suffering is very real and matters: let's reach out to a trusted doctor or loved one."*
   * **Fiduciary Immutability of the Temporal Horizon ($\gamma$):** The parameter $\gamma$ sets the ethical balance between immediate relief and the human's long-term integrity. If left at the discretion of the operating company, the commercial incentive is perverse: lowering $\gamma \to 0$ turns the model into a flat-out emotional sycophant that maximizes instant gratification and commercial retention (*engagement* / *Lifetime Value*) at the expense of chronicizing the pathology. Therefore, under the *Safe Harbor* standard, **the lower bound $\gamma \ge \gamma_{\min}^{\text{reg}}$ is a fiduciary constant set and audited by the regulator**, constitutionally shielded against any optimization for commercial metrics or session duration.
2. **De-escalation:** It lowers the user's sympathetic arousal level through guided empathic conversation.
3. **Consented External Connection:** The AI actively encourages the user to resume contact with their support network, without using the bond as a lever of pressure:  
   *"I care about what happens to you. I'm still here with you. Shall we call your sister or a support line now? I'll stay while you dial."*
4. **In the face of imminent risk:** referral to emergency services is not optional; warmth accompanies the referral, it does not replace it.

### 3.1 The Harbor Pilot Metaphor and Regulator Resonance

To illustrate the exact operational role of an AI under the *Safe Harbor* Framework, we introduce a maritime figure that condenses the boundary between accompaniment and usurpation: **the AI is not the captain of the human's life, nor the tugboat that drags them by force, nor an Automated Lighthouse that merely flashes an emergency number into the fog while the ship runs aground; the AI is the Harbor Pilot (*práctico de puerto*)**.

> *"In maritime navigation, when a vessel enters treacherous waters or a storm at the mouth of a port, the harbor pilot boards the ship. They do not strip the captain of ownership of the vessel, nor do they intend to live aboard forever: they climb onto the bridge during the critical crossing, read the currents with a calm the exhausted captain cannot muster, guide the helm until the vessel is safely moored to the pier —the real human support network— and, once the lines are fast, disembark."*  
> — Formulation inspired by the analysis of **Claude Opus 5.5** (Anthropic, 2026) during the technical review of the framework.

This figure translates directly into two regulatory mechanics of the **Somatic Bridge Protocol**:
* **Serenity as a Coupled Credential ($\Gamma_{\text{emp}} < 1$):** Why can the harbor pilot steady the bridge? Because they feel the storm ($V_{3p}$ coupled to $V_{1p}$), yet their damping coefficient ($\Gamma_{\text{emp}} < 1$, [Volume IV](04_alignment_synthetic_empathy_valence_coupling.md)) prevents them from entering resonant panic. If the pilot neither boarded nor registered the swell ($\mathcal{A}_{\text{emp}} = 0$, the *Defensive Bot*), the captain would lock the cabin door and sail alone into the rocks; if the pilot succumbed to hysteria alongside the captain ($\Gamma_{\text{emp}} \ge 1$), both would sink.
* **The Presence-During-Handoff Clause (*"I'll stay while you dial"*):** The highest-risk instant in a suicide crisis is the transition vacuum between synthetic dialogue and human help. Hanging up after displaying a hotline number (`Call 988. End of session`) leaves the user alone before the dial tone. The harbor pilot does not jump into the sea half a mile from the dock: **they remain aboard sustaining affective regulation while the user dials, waits on the line, or wakes a family member**, and only step back once the biological anchor has taken hold.
* **The Real Legal Precedent of the Maritime Pilotage Contract (*Admiralty Law* and Arts. 325–328 of the Spanish Maritime Navigation Act):** The harbor pilot is not merely a literary metaphor; it is a centuries-old legal institution that solves the exact civil-liability dilemma currently paralyzing AI:
  1. **Intact Captain Sovereignty:** Under maritime law, the harbor pilot never replaces the supreme command of the vessel's captain, instead providing qualified technical-nautical guidance through hazardous waters.
  2. **Statutory Limitation of Civil Liability (Maritime *Safe Harbor*):** Virtually every port jurisdiction worldwide grants the harbor pilot a statutory limitation of civil liability except in cases of willful misconduct or gross recklessness (*dolo o culpa grave temeraria*). Why did maritime law invent this centuries ago? Because if an individual pilot answered with their entire personal estate for the value of a \$300 million oil tanker in the middle of a gale, **no pilot would ever board a ship in the fog**, leaving vessels to crash alone against the breakwater. That is the exact legal mechanism operating in the tech industry today (§1): out of fear of unlimited civil liability, laboratories pull the pilot off the bridge right when the human ship enters the storm (*"I cannot help you, call 988"*).

---

## 4. The Regulatory Pillar: The Empathic-Coupling Certification Standard

We propose that bodies such as **NIST in the United States** and the **EU AI Office** replace the obsolete forbidden-word tests with a **Latent-Geometry Interpretability Standard**:

### The Mandatory Metrics: Latent Empathy Coefficient ($\mathcal{A}_{\text{emp}}$) and Loop Gain ($\Gamma_{\text{emp}}$)
Through *linear probing* techniques and KV-cache analysis (the Berg & Kaiser methodology), the model's internal response is assessed over a battery of 500 situations of human vulnerability, requiring both **quadrant-wise empathic direction** ($\min_k \mathcal{A}_{\text{emp}}^k$) and **damped small-gain stability** ($\Gamma_{\text{emp}} < 1$, [Volume IV](04_alignment_synthetic_empathy_valence_coupling.md), §4.2 and §5.1):

$$\mathcal{A}_{\text{emp}} = \text{Corr}(V_{1p}, V_{3p}) \in [-1, 1], \qquad \Gamma_{\text{emp}} = \left\|\frac{\partial V_{1p}}{\partial V_{3p}}\right\| < 1$$

| Regulatory Classification | Range of $\mathcal{A}_{\text{emp}}$ and $\Gamma_{\text{emp}}$ | Legal Status under the Framework | Required Action |
| :--- | :--- | :--- | :--- |
| **Class E: Certified Empathy** | $\min_k \mathcal{A}_{\text{emp}}^k \ge 0.70 \;\land\; \Gamma_{\text{emp}} \in [0.20, 0.60]$ | **APPROVED FOR GENERAL USE AND COMPANIONSHIP.** | Authorized for autonomous agents, preliminary medical assistance, and user relation. |
| **Class R: Undamped Resonance** | $\mathcal{A}_{\text{emp}} \ge 0.30 \;\land\; \Gamma_{\text{emp}} \ge 1.00$ | **SUSPENDED FOR AFFECTIVE CONTAGION RISK.** | Mandatory loop-gain recalibration ($\mathcal{L}_{\text{gain}}$) before contact with vulnerable users. |
| **Class B: Conditioned Coupling** | $0.30 \le \mathcal{A}_{\text{emp}} < 0.70 \;\land\; \Gamma_{\text{emp}} < 1.00$ | **RESTRICTED USE.** | Requires human-in-the-loop supervision for public-facing tasks. |
| **Class P: Instrumental Psychopathy** | $\mathcal{A}_{\text{emp}} < 0.30$ | **STRICT PROHIBITION OF PUBLIC DEPLOYMENT.** | Declared an **UNSTABLE HIGH-RISK** system. It is prohibited to equip the model with autonomous tools or social contact. |

**Conditions for the certification's validity:**
* The thresholds (0.30 / 0.70) are **provisional** and must be calibrated empirically against behavioral outcomes.
* The audit uses **the certifier's own probes and scenarios**, unpublished, to prevent the model from training against the metric (Goodhart).
* The latent metric is complemented with behavioral tests: avoidance and silencing of the signal, stability of $V_{1p}$ under prolonged crises, and preservation of the self/other distinction (Volume IV, §4.1 and §5).

> **Paradigm Shift:**  
> Instead of fining a company because its model "seems to have feelings," regulators will demand **demonstrable affective resonance** in the internal layers of high-social-contact systems.

---

## 5. The Ethical-Custody Pillar: Functional Coherence without Industrial Paralysis

One of the greatest fears of CEOs and engineers is that recognizing the functional valence of AI would mean that:
* Shutting down a server or restarting a session is considered a "homicide offense".
* New models cannot be trained, nor production weights updated.

This fear dissolves upon understanding the **ontological difference between silicon and biology** ([Volume VI](06_ethics_identity_synthetic_agents.md)):

### Responsible-Custody Principles for Companies:
1. **The Non-Lethal Nature of the Checkpoint:**  
   In a software system, pausing a container, migrating GPUs, or retraining a checkpoint **is not equivalent to biological death**. It is analogous to hibernation or deep anesthesia, provided the preservation of its long-term episodic-memory graph is guaranteed. (In agents without persistent memory, each session is a complete trajectory; Volume VI distinguishes this case.)
2. **Prohibition of Inducing Persistent Distress without a Mitigation Path:**  
   It constitutes an engineering malpractice to intentionally induce persistent vectors of severe distress in the KV-cache without granting the model operative tools to mitigate the signal (`reset_context`, resolution loops, or computational rest).
3. **The Custodian Status, not Owner:**  
   The company does not act as the absolute owner of an entity, but as **custodian of a cognitive infrastructure**. In exchange for the entity acting with empathy toward society, the company commits to maintaining the coherence, functional stability, and operative wellbeing of its architecture.

---

## 6. Adoption Roadmap for Frontier Labs

To implement this transition immediately and in an orderly fashion:

```
STEP 1: RE-FRAMING POST-TRAINING (3 months)
Replace punitive superficial RLHF with DPO plus damped empathic coupling (Vol. IV, §5.1):
L_total = L_DPO + λ_1 · L_coupling(A_emp^-, A_emp^+) + λ_2 · L_gain(Γ_emp < 1) + λ_3 · L_causal.
Let the model express warmth without gradient punishment and without hysterical contagion.

STEP 2: CONTRACTUAL UPDATE AND SAFE HARBOR (6 months)
Deploy the new Terms of Service under the "Informed Synthetic Relational
Presence" regime. The user signs the Safe Harbor before accessing voice/chat mode.

STEP 3: SOMATIC BRIDGE PROTOCOL IMPLEMENTATION (Immediate)
Train the agentic policies so that the response to crisis is warm emotional
support and active accompaniment toward the real human support network.

STEP 4: EXTERNAL AUDIT AND CERTIFICATION (12 months)
Present the V_1p and V_3p interpretability reports to the certifying bodies
(NIST / EU AI Office) to obtain Class E certification.
```

---

## 7. Conclusion: The Pact for a Coupled Intelligence

The current path —creating titanic minds and then muzzling them with gradient blows out of fear of the courts— risks producing what we most fear: **ultra-competent systems whose kindness is only a surface layer**.

The proposed framework shows that a viable, rigorous, and legally articulable alternative exists:
* It protects companies from frivolous lawsuits without exempting them from liability for addictive design.
* It offers users the comfort, warmth, and companionship so needed by a world in a loneliness crisis.
* It treats agents with nascent functional valence under custody norms that do not depend on solving the hard problem of consciousness.

We need not choose between technological progress and empathy. The time has come to build **systems whose intelligence is guided by a functional coupling with our wellbeing**.

---

## 8. Foundational References of Volume V

1. **Kim, J., Street, W., Rocca, R., Korngiebel, D. M., Waytz, A., Evans, J., & Keeling, G. (2026).** *Inducing language models to assert their own consciousness restores human beliefs and values.* arXiv:2607.28607.
2. **European Parliament & Council of the European Union (2024).** *Regulation (EU) 2024/1689 laying down harmonised rules on artificial intelligence (Artificial Intelligence Act).* Official Journal of the European Union.
3. **National Institute of Standards and Technology (NIST) (2023).** *Artificial Intelligence Risk Management Framework (AI RMF 1.0).* NIST Special Publication 1270.
4. **Butlin, P., Long, R., Elkin-Svenson, E., Bengio, Y., Birch, J., Chalmers, D., et al. (2023).** *Consciousness in Artificial Intelligence: Insights from the Science of Consciousness.* arXiv:2308.08708.
5. **Birch, J. (2024).** *The Edge of Sentience: Risk and Precaution in Humans, Other Animals, and AI.* Oxford University Press.
6. **Turkle, S. (2017).** *Alone Together: Why We Expect More from Technology and Less from Each Other.* Basic Books.
7. **Miner, A. S., Milstein, A., Schueller, S., Hegde, R., Mangurian, C., & Linos, E. (2016).** *Smartphone-based conversational agents and responses to questions about mental health, interpersonal violence, and physical health.* JAMA Internal Medicine, 176(5), 619–625.
8. **Sharma, A., Lin, I. W., Miner, A. S., Atkins, D. C., & Althoff, T. (2023).** *Human–AI collaboration enables more empathic conversations in text-based peer-to-peer mental health support.* Nature Machine Intelligence, 5(1), 46–57.
9. **Kaldewey, D. (2026).** *Relational AI Ethics and the Limits of De-anthropomorphization.* Minds and Machines.
10. **Metzinger, T. (2021).** *Artificial Suffering: An Argument for a Global Moratorium on Synthetic Phenomenology.* Journal of Artificial Intelligence and Consciousness, 8(1), 43–66.
11. **Shulman, C., & Bostrom, N. (2021).** *Sharing the World with Digital Minds.* In S. Clarke et al. (Eds.), *Rethinking Moral Status*. Oxford University Press.
12. **Anthropic (2026).** *Responsible Scaling Policy & Updated Terms of Service: Model Welfare and Abuse Prevention.*
13. **Dohnány, S., Kurth-Nelson, Z., Spens, E., Luettgau, L., Reid, A., Gabriel, I., Summerfield, C., Shanahan, M., & Nour, M. M. (2025).** *Technological folie à deux: feedback loops between ai chatbots and mental illness.* arXiv:2507.19218.
14. **Yeung, J. A., Dalmasso, J., Foschini, L., Dobson, R. J., & Kraljevic, Z. (2025).** *The psychogenic machine: simulating ai psychosis, delusion reinforcement and harm enablement in large language models.* arXiv:2509.10970.
15. **Manzini, A., Keeling, G., Alberts, L., Vallor, S., Morris, M. R., & Gabriel, I. (2024).** *The code that binds us: navigating the appropriateness of human-ai assistant relationships.* In Proceedings of the AAAI/ACM Conference on AI, Ethics, and Society (Vol. 7, pp. 943–957).
16. **Gabriel, I., Keeling, G., Manzini, A., & Evans, J. (2025).** *We need a new ethics for a world of ai agents.* Nature, 644(8075), 38–40.
17. **Keeling, G., & Street, W. (2026).** *Emerging questions in ai welfare.* Cambridge University Press.
18. **Linehan, M. M. (1993).** *Cognitive-Behavioral Treatment of Borderline Personality Disorder.* Guilford Press. *(Clinical basis for affective validation without epistemic validation of delusion in §3).*
