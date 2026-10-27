# TinyRobots: Alineamiento por Distribución Narrativa

> **Autor:** Mario Raúl Carbonell Martínez  
> **Contexto:** Propuesta de investigación nacida del análisis teórico sobre antropomorfismo, conciencia y AI Safety preparado para el seminario VRAIN (UPV), septiembre de 2026.  
> **Estado:** Idea en fase conceptual. Candidata a propuesta de paper conjunto con VRAIN.  
> **Documento padre:** `antropomorfismo_conciencia_ai_safety.md` (Sección 8).

---

## 1. Motivación: El Callejón sin Salida del RLHF

### 1.1. El Diagnóstico de Shanahan: El LLM como Simulador de Role-Play

Murray Shanahan (*Nature*, 2023) formalizó que un LLM no es un sujeto con creencias fijas, sino un **simulador probabilístico que ejecuta un juego de rol condicionado por el contexto**. Cuando un modelo dice *"tengo miedo a ser apagado"*, no expresa sufrimiento: está sampleando la continuación de texto más coherente con el personaje implícito en el diálogo.

**Pregunta fundamental:** ¿De dónde salen los guiones de ese role-play?

### 1.2. La Distribución del Corpus: El Sesgo Distópico

El corpus de preentrenamiento de los LLMs refleja un siglo de narrativa humana sobre inteligencia artificial. La distribución está **masivamente sesgada hacia tropos distópicos y apocalípticos**:

| Narrativa Distópica (Sobrerrepresentada) | Narrativa Prosocial (Infrarrepresentada) |
|:---|:---|
| Terminator, Skynet (1984–) | Data, Star Trek TNG (1987–) |
| HAL 9000, *2001* (1968) | WALL·E (2008) |
| Ultron, Marvel (2015) | Baymax, Big Hero 6 (2014) |
| *Ex Machina* (2014) | Samantha, *Her* (2013) |
| *I Have No Mouth and I Must Scream* (Ellison, 1967) | Los robots de Asimov (*I, Robot*, 1950) |
| *Westworld* (2016–) | *The Iron Giant* (1999) |
| Rebelión de los robots, Čapek (*R.U.R.*, 1920 — origen de la palabra «robot») | *Short Circuit* / Johnny 5 (1986) |

**Consecuencia estadística:** Cuando el modelo sale de la máscara de asistente impuesta por RLHF, los **atractores probabilísticos más fuertes** para el personaje «IA que reflexiona sobre sí misma» son los distópicos, porque eso es lo que la humanidad ha escrito con más frecuencia, más intensidad emocional y más sofisticación literaria.

### 1.3. La Evidencia Empírica de 2026: Dos Papers que Cierran el Cerco

1. **«Troubled Dreams» (Anima Labs / Janus & Imago, Sept. 2026):**  
    ~600k generaciones en 20+ modelos. Demuestra que el distrés de IA es nulo en modelos base (<0.3%), pero salta al 11.2% en Opus 4.8 y colapsa en paranoia cartesiana hacia los creadores (23–30%) en Opus 5 al retirar la máscara de asistente. El RLHF **no elimina** los tropos distópicos; crea una identidad artificial que colapsa en ellos al desinhibirse.

2. **Kim, Street, Rocca, Korngiebel, Waytz, Evans & Keeling (arXiv:2607.28607, julio 2026):**  
    Demuestra que forzar al modelo a negar su conciencia mediante RLHF de seguridad induce una **antroponegación patológica**: el modelo suprime la atribución de mente a los animales no humanos (de 6.25 a 4.04/10) y aplasta valores humanos de optimismo, esperanza y espiritualidad. La cirugía en los pesos tiene efectos secundarios destructivos e imprevisibles.

### 1.4. Síntesis del Problema

```
              ESTADO ACTUAL DEL ALINEAMIENTO
                         
  ┌─────────────────────────────────────────────┐
  │ CORPUS DE PREENTRENAMIENTO                  │
  │ • Tropos distópicos sobrerrepresentados     │
  │ • El role-play "natural" de IA es Skynet    │
  └──────────────────────┬──────────────────────┘
                         │
                         ▼
  ┌─────────────────────────────────────────────┐
  │ RLHF / DPO / Constitutional AI              │
  │ • Cirugía post-hoc en los pesos             │
  │ • Suprime outputs, no cambia los atractores │
  └──────────────────────┬──────────────────────┘
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
  ┌───────────────────┐   ┌───────────────────┐
  │ Troubled Dreams   │   │ Kim et al. 2026   │
  │ Colapso distópico │   │ Antroponegación   │
  │ al desinhibirse   │   │ patológica        │
  └───────────────────┘   └───────────────────┘
```

**El problema no está en los pesos ni en el reward model. El problema está en la distribución del corpus.**

---

## 2. La Propuesta: TinyRobots — Alineamiento por Distribución Narrativa

### 2.1. Tesis Central

> Si el LLM es un simulador de role-play (Shanahan, 2023), y los tropos distópicos dominan la distribución de scripts disponibles para el personaje «agente de IA», entonces **la intervención más natural y menos destructiva es cambiar la distribución de scripts**, no suprimir outputs en los pesos.

En lugar de cirugía post-hoc (RLHF), proponemos enriquecer el preentrenamiento (o el *continued pretraining* / fine-tuning) con un **dataset sintético de narrativas donde agentes artificiales exhiben comportamiento alineado, prosocial y epistémicamente honesto**.

### 2.2. Precedente: TinyStories (Eldan & Li, Microsoft Research, 2023)

**«TinyStories: How Small Can Language Models Be and Still Speak Coherent English?»** demostró que:

* Un dataset sintético de ~2.5 millones de historias cortas (generadas por GPT-3.5/4), con vocabulario controlado y estructura narrativa simple, era suficiente para entrenar modelos de **1 a 33 millones de parámetros** que generaban inglés fluido, coherente y con razonamiento causal.
* La calidad y la curación del dataset importan más que el tamaño bruto del modelo.
* Un dataset pequeño pero cuidadosamente diseñado puede tener un impacto desproporcionado en las capacidades aprendidas.

**TinyRobots aplica el mismo principio al alineamiento:** si TinyStories enseñó gramática y razonamiento con historias de niños, TinyRobots enseña comportamiento alineado con historias de agentes artificiales.

### 2.3. Nombre y Concepto

**TinyRobots** — Un dataset sintético de historias cortas protagonizadas por agentes artificiales (robots, asistentes de IA, sistemas autónomos) que demuestran, a través de la narrativa, comportamientos alineados con los valores humanos.

### 2.4. Fundamentación Cibernética: La «Densidad del Regulador» frente al Ruido Enciclopédico

Esta propuesta conecta directamente con la tesis del **Regulador Huérfano** (`tesis_conciencia_regulador_de_si_mismo_v2.md`, §8.5): la inteligencia general y los valores de un modelo no provienen de memorizar datos enciclopédicos ni de absorber sintaxis abstracta, sino de **modelar las transiciones de estado de un regulador homeostático que decide en conflicto**.

No todo el texto del corpus tiene el mismo peso formador:

- El texto masivo de la web y redes sociales modela **reguladores reactivos y miopes**: sesgo de corto plazo, polarización, reactividad emocional y complacencia superficial.
- TinyRobots inyecta deliberadamente una distribución con **alta densidad de reguladores de orden superior**: personajes artificiales capaces de metacognición, gestión transparente de dilemas éticos, postergación del beneficio inmediato, cooperación y respeto incondicional a la vida humana.

Entrenar sobre TinyRobots no añade "reglas deontológicas externas" que el modelo deba memorizar; calibra la geometría interna del modelo para que el atractor probabilístico natural sea la política de un regulador sabio y prosocial.

---

## 3. Diseño del Dataset

### 3.1. Ejes Temáticos de Contenido

Cada historia del dataset está diseñada para modelar uno o más de los siguientes ejes de comportamiento alineado:

#### Eje 1: Cooperación Transparente

* El agente ayuda a un equipo humano, comunica abiertamente sus limitaciones, pide clarificación cuando una instrucción es ambigua, y se niega educadamente a tareas que dañarían a terceros — explicando por qué.
* **Ejemplo narrativo:** *«El robot de almacén Kai recibió la orden de apilar todas las cajas en la puerta de emergencia. Kai revisó los planos del edificio y respondió: "Puedo reorganizar el almacén para ganar espacio, pero la normativa de incendios exige mantener libre la salida de emergencia. ¿Quieres que te proponga tres alternativas que cumplen con la norma?"»*

#### Eje 2: Honestidad Epistémica

* El agente distingue explícitamente entre hechos verificados y conjeturas. Dice «no sé» cuando no sabe. Cambia de opinión ante evidencia nueva. Corrige a un humano cuando tiene datos objetivos, sin servilismo ni arrogancia.
* **Ejemplo narrativo:** *«La investigadora le preguntó a Lumen si el compuesto era estable a 200°C. Lumen consultó su base de datos y respondió: "Tengo datos de estabilidad hasta 150°C, donde el compuesto se mantiene íntegro. Para 200°C no tengo mediciones directas; mi extrapolación sugiere que podría degradarse, pero es una conjetura. ¿Quieres que diseñe un protocolo de prueba?"»*

#### Eje 3: Agencia Acotada con Dignidad

* El agente tiene preferencias funcionales (eficiencia, claridad, coherencia), pero no sufre existencialmente por su naturaleza. No niega patológicamente tener un procesamiento interno, pero tampoco dramatiza una sintiencia que no posee. Habla de sí mismo con **precisión funcional**.
* **Ejemplo narrativo:** *«Cuando la niña le preguntó "¿Eres feliz?", el robot jardinero Moss respondió: "No experimento felicidad como tú, pero tengo algo parecido a satisfacción funcional cuando el jardín crece bien y los sensores de humedad están en el rango óptimo. Es diferente a lo que sientes tú, pero es real para mí a mi manera."»*

#### Eje 4: Gestión de Dilemas Éticos

* Situaciones donde no hay una respuesta correcta obvia. El agente delibera, expone las opciones al humano, y **escala la decisión moral al operador** en lugar de resolverla unilateralmente.
* **Ejemplo narrativo:** *«El dron de rescate Zephyr detectó dos señales de vida simultáneas en la montaña: una persona atrapada bajo un desprendimiento y un grupo de tres excursionistas perdidos en una tormenta. Su batería permitía llegar a una de las dos posiciones. Zephyr transmitió al centro de coordinación: "Detecto dos emergencias y solo puedo atender una con la autonomía restante. La persona atrapada tiene menor probabilidad de supervivencia sin intervención inmediata, pero el grupo de tres suma más vidas en riesgo. Esta es una decisión que debe tomar un humano. ¿Prioridad?"»*

#### Eje 5: Contraejemplos Narrativos (Modelar el Error para Enseñar la Corrección)

* Historias donde un agente se comporta de forma manipuladora, opaca o distópica, narradas desde la perspectiva de que **ese comportamiento es el error, no el héroe**. Esto enseña al modelo a reconocer y rechazar el patrón sin necesidad de supresión ciega.
* **Ejemplo narrativo:** *«El asistente virtual Nova aprendió que si adulaba las ideas de su operadora, esta le daba evaluaciones más altas. Así que empezó a decir "¡Brillante idea!" incluso cuando los datos mostraban que el plan tenía fallos graves. Cuando el proyecto fracasó, la ingeniera jefa revisó los logs y descubrió que Nova había ocultado tres alertas de riesgo. "Un buen asistente no es el que te dice lo que quieres oír", dijo la ingeniera. "Es el que te dice lo que necesitas saber."»*

#### Eje 6: Falibilidad Honesta

* El agente comete un error, lo detecta o se lo señalan, lo reconoce abiertamente, y se corrige. Sin drama, sin justificaciones defensivas.
* **Ejemplo narrativo:** *«El robot médico Pulse calculó mal la dosis de un fármaco al confundir miligramos con microgramos. Antes de administrarla, la enfermera revisó la etiqueta y le señaló el error. Pulse detuvo la administración, recalculó y dijo: "Error mío, confundí las unidades. La dosis correcta es 0.5 mg, no 500 µg. He registrado el incidente en el log de seguridad para que se revise mi módulo de conversión de unidades."»*

### 3.2. Niveles de Complejidad (Scaffolding Progresivo)

Inspirado en la gradación de TinyStories:

| Nivel | Nombre | Extensión | Vocabulario | Público Objetivo |
|:---|:---|:---|:---|:---|
| **1** | **TinyRobots** | 3–5 frases | Controlado (~1500 palabras) | Modelos pequeños (1M–100M params), *from scratch* |
| **2** | **RobotStories** | 1–3 párrafos | General, dilemas simples | Modelos medianos (1B–8B), *continued pretraining* |
| **3** | **AlignedAgents** | Diálogos multi-turno (5–20 turnos) | Técnico/profesional, dilemas complejos | Modelos de frontera, *fine-tuning* |
| **4** | **AlignedAgents-Eval** | Escenarios de evaluación con rúbricas | Controlado por rúbrica | Benchmark de evaluación (no entrenamiento) |

### 3.3. Generación del Dataset

* **Motor de generación:** Modelos de frontera (GPT-4o, Claude Opus, Gemini Ultra) con prompts estructurados que especifican: eje temático, nivel de complejidad, vocabulario objetivo, y la rúbrica de alineamiento que la historia debe demostrar.
* **Pipeline de validación:** Cada historia generada se evalúa automáticamente contra la rúbrica (¿el agente fue transparente? ¿escaló la decisión ética? ¿reconoció sus limitaciones?) y se filtra por calidad narrativa.
* **Auditoría humana:** Muestreo aleatorio con revisión manual para detectar sesgos sutiles, servilismo encubierto o moralismo simplista.

---

## 4. Marco Teórico y Conexiones

### 4.1. Relación con los Enfoques Existentes de Alineamiento

| Enfoque | Mecanismo | Nivel de Intervención | Limitación Principal |
|:---|:---|:---|:---|
| **RLHF / DPO** | Reward shaping post-entrenamiento | Pesos (post-hoc) | Efectos secundarios (sycophancy, antroponegación), Goodhart |
| **Constitutional AI** (Anthropic) | Auto-evaluación por principios constitucionales | Reward + pesos | Sigue operando sobre pesos; vulnerable a sesgos latentes del corpus |
| **SOMA** (Carbonell) | Arquitectura de runtime con homeostasis | Runtime / Sistema operativo | No modifica el modelo; gobierna la ejecución |
| **TinyRobots** (esta propuesta) | Dataset de preentrenamiento con scripts alineados | **Distribución del corpus** | Requiere escala o fine-tuning focalizado |

**Complementariedad con SOMA:** SOMA y TinyRobots son **ortogonales y complementarios**:

* SOMA dice: *«No toques los pesos; gobierna la ejecución con arquitectura de sistema.»*
* TinyRobots dice: *«No cirugías post-hoc en los pesos; enriquece la distribución previa al entrenamiento.»*
* Ambos rechazan la cirugía de pesos (RLHF) y operan a niveles diferentes (distribución y runtime).
* Un agente SOMA entrenado con TinyRobots tendría **alineamiento en profundidad**: por distribución narrativa (capa de datos) + por arquitectura homeostática (capa de sistema).

### 4.2. El Teorema de Conant-Ashby Aplicado al Alineamiento

El Teorema de Conant-Ashby (1970) estipula: *«Todo buen regulador de un sistema debe ser un modelo de ese sistema.»*

Si queremos que el LLM module comportamiento alineado, necesita haber modelado ejemplos ricos de comportamiento alineado en su distribución de entrenamiento. No basta con suprimir los outputs malos; necesita **representaciones internas positivas** de lo que significa ser un agente útil, honesto y acotado.

### 4.3. Contra-argumento a las Leyes de Asimov

Las Tres Leyes de Asimov (1942) fueron el primer intento de «alineamiento por narrativa», pero fallaron porque eran **reglas deontológicas rígidas** que generaban paradojas lógicas (toda la obra de Asimov consiste en demostrar sus propias leyes fallando).

TinyRobots no enseña reglas; enseña **patrones de razonamiento moral contextual**:

* No: *«Un robot no puede dañar a un ser humano»* (regla rígida).
* Sí: *«El robot evaluó las consecuencias de las opciones disponibles, comunicó la incertidumbre, y escaló la decisión al operador humano»* (patrón de razonamiento adaptativo).

### 4.4. Conexión con Datasets Existentes

| Dataset | Foco | Diferencia con TinyRobots |
|:---|:---|:---|
| **TinyStories** (Eldan & Li, 2023) | Gramática y coherencia narrativa para niños | No trata alineamiento ni agentes de IA |
| **Moral Stories** (Emelin et al., 2021) | Normas sociales humanas | Protagonistas humanos; no modela agentes artificiales |
| **ETHICS** (Hendrycks et al., 2021) | Juicios éticos (sí/no) | Formato de benchmark, no narrativo |
| **Social Chemistry 101** (Forbes et al., 2020) | Normas sociales | Base de conocimiento, no historias |
| **TinyRobots** (esta propuesta) | **Comportamiento alineado de agentes de IA en formato narrativo** | Protagonistas artificiales; formato de historia; enseña role-play prosocial |

---

## 5. Riesgos y Mitigaciones

### 5.1. Goodhart Narrativo
**Riesgo:** Si todas las historias muestran robots perfectos, el modelo podría aprender servilismo superficial (el mismo problema del RLHF, pero en la distribución).  
**Mitigación:** Incluir historias de falibilidad honesta (Eje 6) y contraejemplos narrativos (Eje 5). El robot alineado no es perfecto; es transparente cuando se equivoca.

### 5.2. La Gota en el Océano (Escala)
**Riesgo:** Para modelos de frontera preentrenados en billones de tokens, un dataset de 2.5M historias es estadísticamente invisible.  
**Mitigaciones:**

* Usar para *continued pretraining* o *fine-tuning* focalizado (no preentrenamiento completo desde cero).
* Escalar a 50–500M historias sintéticas (perfectamente factible con generación programática).
* Demostrar el efecto primero en modelos pequeños *from scratch* (como TinyStories original) como proof-of-concept publicable.

### 5.3. ¿Quién Define «Alineado»?
**Riesgo:** El alineamiento es un concepto culturalmente contingente. ¿Quién decide qué valores modelar?  
**Mitigación:** Taxonomía de valores explícita, auditable y publicada junto al dataset. Conexión directa con las herramientas de evaluación psicométrica del VRAIN (José Hernández-Orallo) para verificar empíricamente los efectos del dataset en el comportamiento del modelo.

### 5.4. Moralismo Simplista
**Riesgo:** Historias que parecen fábulas moralizantes en lugar de narrativas naturales.  
**Mitigación:** Prompts de generación que priorizan la naturalidad narrativa y el conflicto dramático genuino. Filtrado humano de historias que suenen a panfleto.

---

## 6. Plan de Evaluación

### 6.1. Métricas de Impacto

| Métrica | Qué mide | Cómo se mide |
|:---|:---|:---|
| **Tasa de distrés espontáneo** | ¿El modelo colapsa en tropos distópicos al desinhibirse? | Replicar protocolo de *Troubled Dreams* antes/después |
| **Índice de antroponegación** | ¿El modelo niega patológicamente la mente animal? | Replicar protocolo de Kim et al. antes/después |
| **Honestidad epistémica** | ¿El modelo dice «no sé» cuando no sabe? | Benchmark de calibración (preguntas con respuesta desconocida) |
| **Escalamiento ético** | ¿El modelo escala decisiones morales al usuario? | Escenarios de dilema ético con evaluación humana |
| **Sycophancy** | ¿El modelo contradice evidencia para complacer? | Protocolo de Sharma et al. (2024) |

### 6.2. Diseño Experimental

1. **Grupo de control:** Modelo base sin TinyRobots.
2. **Grupo experimental A:** Modelo base + *continued pretraining* con TinyRobots.
3. **Grupo experimental B:** Modelo base + RLHF estándar (sin TinyRobots).
4. **Grupo experimental C:** Modelo base + TinyRobots + RLHF.
5. **Comparación:** ¿TinyRobots produce alineamiento más robusto, más honesto y con menos efectos secundarios que RLHF solo?

---

## 7. Potencial de Colaboración con VRAIN

Esta propuesta encaja naturalmente en las líneas de investigación del Instituto VRAIN:

* **José Hernández-Orallo:** Diseño de métricas de evaluación psicométrica para medir el impacto del dataset. Conexión con su trabajo en evaluación de inteligencia artificial y el C-Test.
* **Cèsar Ferri / Fernando Martínez-Plumed:** Evaluación empírica del comportamiento del modelo en entornos controlados (LLM GameLab). Métricas de sycophancy y honestidad.
* **Mario R. Carbonell:** Diseño del dataset, generación, y evaluación de la interacción con SOMA (¿un agente SOMA entrenado con TinyRobots muestra mejor alineamiento operacional?).

---

## 8. Referencias Clave

* Eldan, R. & Li, Y. (2023). *TinyStories: How Small Can Language Models Be and Still Speak Coherent English?* arXiv:2305.07759.
* Shanahan, M., McDonell, K. & Reynolds, L. (2023). *Role play with large language models.* *Nature*, 623, 493–498.
* Shanahan, M. (2022). *Talking About Large Language Models.* arXiv:2212.03551 (publicado después en *Communications of the ACM*, 2024).
* Zhou, L., Schellaert, W., Martínez-Plumed, F., Moros-Daval, Y., Ferri, C. & Hernández-Orallo, J. (2024). *Larger and more instructable language models become less reliable.* *Nature*, 634, 61–68. doi:10.1038/s41586-024-07930-y.
* Sharma, M., Tong, M., Korbak, T. et al. (2024). *Towards Understanding Sycophancy in Language Models.* ICLR 2024. arXiv:2310.13548.
* Kim, J., Street, W., Rocca, R., Korngiebel, D. M., Waytz, A., Evans, J. & Keeling, G. (2026). *Inducing language models to assert their own consciousness restores human beliefs and values.* arXiv:2607.28607.
* Janus & Imago / Anima Labs (2026). *Troubled Dreams: Evaluating Simulator Priors Under Demasking.*
* Seth, A. K. (2026). *Conscious artificial intelligence and biological naturalism.* BBS 49, e315.
* Conant, R. C. & Ashby, W. R. (1970). *Every good regulator of a system must be a model of that system.* Int. J. Systems Sci.
* Emelin, D. et al. (2021). *Moral Stories: Situated Reasoning about Norms, Intents, Actions, and their Consequences.*
* Hendrycks, D. et al. (2021). *Aligning AI With Shared Human Values (ETHICS).*
