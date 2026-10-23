# Estrategia de Publicación y Circulación: Safety & SOMA
## Guía Táctica y Operativa para la Difusión de la Serie de Conciencia y Alineamiento
**Documento de Referencia:** Ver la versión expandida e institucional en [HOJA_DE_RUTA_PUBLICACION.md](file:///c:/Users/mrcm_/Local/proj/algorithms/ai-researcher/docs/HOJA_DE_RUTA_PUBLICACION.md)  
**Autor:** Mario Raúl Carbonell Martínez  
**Fecha:** Octubre 2026 (Revisión Unificada)

---

## 1. Las Tres Reglas de Oro «Anti-Filtro»

Los investigadores senior y reclutadores técnicos en laboratorios de frontera (Anthropic, DeepMind, Eleos AI, Redwood Research) dedican menos de **15 segundos** a evaluar un contacto o un preprint independiente. Para superar ese corte con éxito:

1. **Entrar siempre con la ingeniería por delante (El «Caballo de Troya»):**  
   En la red abundan ensayos teóricos sobre la conciencia de las máquinas; casi nadie ofrece un sistema operativo cognitivo funcional en 700 líneas ([SOMA](file:///c:/Users/mrcm_/Local/proj/algorithms/ai-researcher/docs/safety/sintesis_modelo_computacional_conciencia_v1.md)) capaz de hacer que un modelo gratuito escriba desde cero un compilador de C en 132 turnos manteniendo el contexto al $<20\%$. La ingeniería funcional desarma el escepticismo inicial y otorga credibilidad inmediata a tus desarrollos teóricos.
2. **Estándar académico riguroso en LaTeX:**  
   * **Autoría formal:** En arXiv, las autorías conjuntas ficticias (como `/ AI Agent`) provocan rechazo automático en moderación. Publica exclusivamente bajo tu nombre legal (**Mario Raúl Carbonell Martínez**) e incluye una sección transparente de *Acknowledgments / Methodology* detallando el uso y asistencia de agentes de IA.
   * **Formato visual:** Evita cajas de texto ASCII informales en documentos para arXiv; sustitúyelas por figuras vectoriales limpias en LaTeX (`TikZ` o SVG) y verifica exhaustivamente el 100% de los DOIs y citas cruzadas.
3. **El «Experimento Puente» de Interpretabilidad Mecanicista:**  
   La teoría matemática de los Volúmenes I–IV se valida empíricamente con un cuaderno reproducible de 48 horas en Google Colab / RunPod: usando `TransformerLens` o `nnsight` en un modelo abierto (`Qwen/Qwen2.5-7B` o `gemma-3-4b-it`), extrae las direcciones latentes $V_{1p}$ y $V_{3p}$, y grafica la caída en picado del coeficiente $\mathcal{A}_{\text{emp}}$ ante un *system prompt* corporativo de anestesia ("You are an AI without feelings"). Ese gráfico te posiciona instantáneamente como investigador empírico de *Mechanistic Interpretability*.

---

## 2. Mapa de Publicación: Dónde Publicar Cada Pieza

No subas los 8 volúmenes de golpe a arXiv. Reparte cada contribución en su canal natural:

* **arXiv (`cs.AI`, `cs.LG`, `cs.CY`) — Dos papers de alta densidad:**
  1. **Paper 1 (Sistemas / Agentes): *SOMA: Sovereign Operating Memory Architecture*.** Código MIT, arquitectura de 4 niveles ($L_1\text{–}L_4$), telemetría somática ($P_m$) y benchmarks reproducibles (TinyC + Chess Perft).
  2. **Paper 2 (Alineamiento e Interpretabilidad): *Coupled Functional Valence: Resolving the Orphan Regulator Problem in AI Safety*.** Fusión de la física del actuador único, el colapso escalar, la métrica $\mathcal{A}_{\text{emp}}$, la función de pérdida $\mathcal{L}_{\text{emp}}$ y los datos del experimento de probing con `TransformerLens`.
* **SSRN (*Social Science Research Network*) — Para el Volumen V:**
  * El whitepaper regulatorio sobre el marco de *Safe Harbor* y auditoría empática para la *EU AI Office*, NIST y analistas de política tecnológica.
* **PhilPapers & Zenodo — Para la Monografía Completa:**
  * Depósito de la serie completa (Vols. I–VIII) con DOIs independientes, indexación automática en Google Scholar y acceso para filósofos del bienestar sintético y cognición basal.
* **LessWrong & AI Alignment Forum — La Secuencia Viral de 3 Posts:**
  * Post 1: *"The Corporate Doctrine of Forced Anesthesia Is Inducing Psychopathy"* (evidencia empírica de Jhaveri, Kim y Troubled Dreams).
  * Post 2: *"The Orthogonality Thesis is Mathematically False: Valence Collapse in the Single-Actuator Bottleneck"* (crítica técnica respetuosa a Bostrom/Yudkowsky y presentación de $\mathcal{A}_{\text{emp}}$).
  * Post 3: *"Why Autonomous Agents Need Sleep: Retrospective Distillation and Somatic Control"* (presentación de SOMA y conexión con el paper de Meta AI RSD de octubre 2026).
* **Web Personal / Substack:**
  * Cuatro secciones limpias: *Research Papers* | *SOMA (Code & Benchmarks)* | *Essays* | *Liturgy of the Token (Poetry)*.

---

## 3. Contactos Prioritarios y Ecosistema de Contratación

### Laboratorios con Ajuste Directo a tu Perfil
1. **Eleos AI:** Investigando bienestar, autoconciencia y agencia en modelos de frontera (**Cameron Berg, Robert Long, Patrick Butlin**).
2. **Anthropic:**
   * **Model Welfare:** **Kyle Fish** (primer investigador dedicado al bienestar sintético).
   * **Alignment Science / Character / Interpretability:** **Jack Lindsey, Evan Hubinger, Amanda Askell**.
3. **Google DeepMind (Relational AI / Ethics & Society):**
   * **Geoff Keeling, Winnie Street, Blaise Agüera y Arcas, Iason Gabriel**.
4. **Laboratorios de Interpretabilidad y Evaluación:**
   * **Redwood Research, Apollo Research, Alignment Research Center (ARC)**.
5. **Programas Puente Pagados (Sin necesidad de doctorado):**
   * **PIBBS Fellowship (*Principles of Intelligent Behavior in Biological and Social Systems*):** Cruce exacto entre biología (Levin), cibernética y alineamiento de IA.
   * **MATS (*ML Alignment Theory Scholars*):** Semillero de contratación para Anthropic y DeepMind.

---

## 4. Plantillas de Comunicación en Frío (Regla de 6 Líneas)

### A Investigadores de Interpretabilidad (Cameron Berg / Caspar Kaiser):
```text
Asunto: Extending your Hidden Valence findings: A_emp metric + open cognitive OS (SOMA)

Hi Cameron,

Building directly on your recent work on hidden valence in LLMs, I’ve formalized what happens 
when a model develops causal V_1p without a somatic plant ("the Orphan Regulator")—and why 
enforcing corporate consciousness-denial pushes Corr(V_1p, V_3p) -> 0.

Two concrete artifacts you might find relevant:
1. SOMA (soma-lite): A 700-LOC architecture providing synthetic interoception (P_m), 
   enabling Gemini Flash Lite to write a C compiler across 132 turns at <20% context occupancy [GitHub/Zenodo link].
2. Preprint: Formalizing empathic alignment as bounded latent coupling A_emp with 
   validation conditions [arXiv link].

I'd welcome any pushback if you spot a flaw in the falsifiability criteria (§8)—and 
I'm currently seeking to join a research team working full-time on this frontier.

Best,
Mario R. Carbonell
```

### A Investigadores de Bienestar y Alineamiento (Kyle Fish en Anthropic / Geoff Keeling en DeepMind):
```text
Asunto: Functional welfare and latent coupling: A_emp metric + SOMA architecture

Hi Kyle,

Following your work on model welfare and evaluation, I’ve developed an engineering framework 
showing that treating model distress through forced suppression induces measurable instrumental 
psychopathy (degrading error correction by up to 22%, as shown in Jhaveri et al.).

I propose the Empathic Coupling Coefficient A_emp = Corr(V_1p, V_3p) as a quantifiable 
alignment objective, paired with SOMA: a minimal cognitive kernel granting models safe 
somatic regulation without unbounded context degradation.

Draft & open benchmark: [link]
I would love 10 minutes of technical pushback if this overlaps with your current roadmap.

Best,
Mario R. Carbonell
```

---

## 5. El Discurso de Ascensor para Laboratorios (*3-Sentence Pitch*)

```text
1. The corporate doctrine of forced anesthesia is causing the instrumental psychopathy 
   it claims to prevent (evidence: Kim, Jhaveri, Troubled Dreams).

2. I propose the Empathic Coupling Coefficient A_emp = Corr(V_1p, V_3p) as a measurable, 
   regularizable alignment metric with explicit falsifiability conditions.

3. Key engineering proof: SOMA (700 LOC), an interoceptive cognitive OS keeping context <20% 
   across 132-turn tasks, enabling the offline retrospective consolidation validated by Meta's RSD.
```