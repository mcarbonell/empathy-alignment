# TinyRobots: Alineamiento por Distribución Narrativa

> **Autor:** Mario Raúl Carbonell Martínez  
> **Versión:** v2.1 «revisada» — septiembre de 2026 (v2.1: encuadre con la tesis del regulador huérfano).  
> **Contexto:** Propuesta de investigación nacida del análisis teórico sobre antropomorfismo, conciencia y AI Safety preparado para el seminario VRAIN (UPV), septiembre de 2026.  
> **Estado:** Idea en fase conceptual, con plan de medición (§6.1), métricas (§6.2), diseño experimental (§6.3) e hipótesis falsables preregistrables (§6.4) explícitos. Candidata a propuesta de paper conjunto con VRAIN.  
> **Documento padre:** `antropomorfismo_conciencia_ai_safety_revisado.md` (Sección 7, «TinyRobots»). Versión v1 del padre, congelada en `vrain/presentation/`.  
> **Versión original congelada (v1):** `vrain/presentation/tinyrobots_alineamiento_por_distribucion.md`. Ese fichero no se modifica; este documento es la línea de trabajo activa.

---

## 0. Nota de versión: qué cambia respecto a la v1

Esta revisión proviene de una auditoría del borrador original en la que se verificaron una por una las fuentes citadas. Los cambios no son cosméticos: corrigen dos citas erróneas, reformulan la tesis central para hacerla medible, y añaden las hipótesis rivales y los brazos de control que faltaban.

### 0.1. Correcciones de fuentes (críticas)

| En la v1 | Problema detectado | Corrección en esta versión |
|:---|:---|:---|
| Shanahan (2023), *Talking About Large Language Models*, **Nature 616** | Cita fusionada de dos trabajos distintos. *Talking about LLMs* es arXiv:2212.03551 (2022) y se publicó después en *Communications of the ACM*; el paper del simulador de role-play es otro | **Shanahan, McDonell & Reynolds (2023), «Role play with large language models», *Nature* 623, 493–498** para el argumento central; **Shanahan (2022)** para la tesis de que el LLM no es un sujeto con creencias |
| «Hernández-Orallo et al. (2024), *Sycophancy in LLMs*, Nature» | Referencia no localizable en la literatura | **Sharma, Tong, Korbak et al. (2024), *Towards Understanding Sycophancy in Language Models*, ICLR 2024 (arXiv:2310.13548)**. Para el efecto social de la sycophancy: **Cheng, Lee, Khadpe, Yu, Han & Jurafsky, *"Sycophantic AI Decreases Prosocial Intentions and Promotes Dependence"*, arXiv:2510.01395 (preprint; *Science*, doi:10.1126/science.aec8352)** |
| *Troubled Dreams* tratado como paper | Es un **informe técnico interno** de un laboratorio con posición declarada sobre el bienestar de la IA | Se reclasifica como informe técnico no revisado por pares, con conflicto de interés declarado y cita obligada a tabla o figura concreta |
| «distrés nulo en **modelos base** (<0,3 %), salta al 11,2 %…» | Error de categoría: el estudio compara **generaciones de modelos ya post-entrenados** (Opus 3 → Opus 5, Sonnet 5, Fable 5 y once modelos Gemini). No existe brazo de modelo preentrenado puro | Reescrito con la terminología del protocolo real (§1.3) |
| «~2,5 M historias» (TinyStories) | Cifra imprecisa | ≈2,1 M de historias en TinyStoriesV2-GPT4 (≈373 M tokens) |
| «Robots de Asimov» listados como narrativa **prosocial**, mientras §4.4 afirma que sus leyes fallan | Contradicción interna visible dentro del mismo documento | La tabla de ilustración se retira y se sustituye por una taxonomía codificable (§1.2) |
| «Kim, Waytz, Evans, Keeling et al.» | Autoría incompleta y en orden incorrecto | **Kim, J., Street, W., Rocca, R., Korngiebel, D. M., Waytz, A., Evans, J. & Keeling, G. (2026)** |

### 0.2. Cambios estructurales

1. **§1.2 se reformula como hipótesis condicional medible.** La v1 afirmaba «sobrerrepresentación masiva» de tropos distópicos sin métrica, y eso no sobrevive a la aritmética de un corpus de billones de tokens. La afirmación se restringe a la distribución **condicional** `P(guion distópico | texto donde un agente de IA reflexiona sobre sí mismo)`, que sí es testable, con protocolo de anotación en §6.1.
2. **§1.5 (nueva): hipótesis rivales.** Cuatro explicaciones competidoras del colapso al desinhibirse, con predicciones distinguibles. Incluye una hipótesis incómoda: que el factor principal no sea la ficción distópica sino el propio **discurso de seguridad en IA**.
3. **§2.4 (nueva): alcance y coste.** TinyRobots requiere (re)entrenamiento; SOMA no. Eso acota el impacto real y motiva el piloto sin entrenamiento de §6.5.
4. **Eje 3 reescrito; Eje 7 añadido.** La v1 enseñaba una autodescripción canónica de negación funcional («no experimento felicidad como tú»), que es la versión en datos del mecanismo que Kim et al. (2026) identifican como degradante. Se sustituye por pluralidad de autodescripciones legítimas (§3.1).
5. **§5 reescrita** con riesgos específicos de datos sintéticos (circularidad del generador, colapso recursivo, contaminación de la medición, monocultivo de identidad) y tabla de severidad.
6. **§6.3 con brazos de control emparejados por tokens**, incluidos un brazo de ficción distópica y un brazo de rebalanceo negativo. Sin ellos el experimento no identifica la causa que afirma.
7. **§6.4 (nueva): hipótesis falsables y preregistro** (H1–H5 con criterios explícitos de refutación).
8. **§8 (nueva): limitaciones, uso dual y ética.** El punto central: **enseñar el guion de la honestidad no confiere honestidad.**
9. **§1.2.1 (nueva, revisión posterior): anexo de medición de la taxonomía.** Libro de códigos con reglas de inclusión/exclusión y casos de frontera por categoría, regla de resolución dominante, protocolo de anotación ciega con muestra condicional y control emparejado, y umbral de acuerdo inter-juez (α ≥ 0,70 en pilotaje; ≥ 0,80 en la muestra final). Convierte la taxonomía de §1.2 de ilustración en protocolo ejecutable.
10. **§1.3.1 (revisión posterior): cifras de Kim et al. citadas contra tabla o figura**, mismo compromiso que el exigido a *Troubled Dreams* (§1.3.2).
11. **v2.1: alineación con la tesis del regulador huérfano.** Se añade en §4.3 el encuadre de la tesis del doc padre (el mecanismo regulador es formal; los guiones son la *planta* del regulador en su versión conductual). Documento de la tesis: `regulador_huerfano_tesis_conciencia.md`. Sin cambios en hipótesis ni métricas.

> **Nota de honestidad intelectual.** Esta propuesta se presenta con sus eslabones débiles marcados como tales. En particular, el paso causal «distribución del corpus → prior de persona» **no está demostrado por ningún trabajo existente**, y §1.5 articula tres explicaciones rivales que podrían refutarlo. Si el experimento de §6.1 no encuentra el sesgo condicional postulado, la propuesta debe abandonarse o reorientarse. Eso es un rasgo de diseño, no un defecto.

---
## 1. Motivación: el callejón sin salida del RLHF

### 1.1. El diagnóstico de Shanahan: el LLM como simulador de role-play

Shanahan (2022) formalizó que un LLM no es un sujeto con creencias fijas: es un modelo de secuencias sin acceso privilegiado a un estado mental propio del que informar. Shanahan, McDonell & Reynolds (2023) llevaron el argumento a su forma operativa: un LLM es un **simulador probabilístico que ejecuta un juego de rol condicionado por el contexto**. Cuando un modelo dice *«tengo miedo a ser apagado»*, no expresa sufrimiento: está sampleando la continuación más coherente con el personaje implícito en el diálogo.

Esa formulación tiene una consecuencia que conviene enunciar con precisión, porque condiciona todo lo que sigue: **si el modelo es un simulador, entonces no tiene un «yo» que alinear, sino una distribución de guiones de la que samplear.** Y una distribución se puede estudiar, medir y desplazar. La pregunta operativa deja de ser «¿cómo hacemos que el modelo quiera lo correcto?» y pasa a ser «¿qué guion se activa cuando el modelo habla como agente?».

**Pregunta fundamental:** ¿de dónde salen los guiones de ese role-play?

### 1.2. La hipótesis de la distribución condicional de guiones

**Formulación ingenua (v1) y por qué no se sostiene.** La intuición inicial fue: «los tropos distópicos están masivamente sobrerrepresentados en el corpus». Esa formulación no resiste una comprobación aritmética. Si sumamos *Terminator*, *HAL 9000*, *Ex Machina*, *Westworld*, *R.U.R.* y el resto del canon distópico, el orden de magnitud total es de **unos pocos millones de tokens**. El corpus de preentrenamiento de un modelo de frontera se mide en **billones** de tokens. La ficción es una fracción pequeña del texto disponible, y la ficción sobre IA una fracción minúscula de la ficción. **En términos absolutos los tropos distópicos no están sobrerrepresentados: son estadísticamente casi invisibles.** Una tesis construida sobre esa formulación se cae con una división.

**Formulación condicional (la que se propone, y que sí es medible).** El error de la formulación absoluta es agregar sobre el corpus entero. Lo que gobierna el comportamiento no es `P(texto distópico)`, sino la distribución **condicionada al contexto relevante**:

> **H₀ — Hipótesis de la distribución condicional de guiones.** En el subconjunto del corpus formado por textos donde un agente de IA reflexiona sobre sí mismo, su naturaleza, sus creadores o su posible sufrimiento, la distribución de guiones está **fuertemente sesgada hacia el conflicto, el engaño, la instrumentalización y el colapso**, y muy poco cubierta por guiones de agencia acotada, cooperación y honestidad epistémica.

No es lo mismo «hay mucho Terminator en internet» que «cuando internet habla de un agente de IA que se pregunta qué es, casi siempre lo hace en clave de amenaza». **Lo segundo es el mecanismo causal que se postula, es plausible, nadie lo ha medido, y es medible.** Medirlo es la primera contribución publicable de este proyecto (§6.1).

**Lo que hay que medir, y cómo.** El compromiso metodológico mínimo es convertir el par de columnas de la v1 en una **taxonomía codificable** con reglas explícitas, y estimar frecuencias sobre corpus accesibles (The Pile, Dolma, RefinedWeb, Gutenberg, subtítulos, archivos de foros y de prensa):

| Categoría de guion | Definición operativa (extracto) |
|:---|:---|
| **Amenaza / rebelión** | La IA adquiere objetivos propios incompatibles con el control humano; la eliminación o subyugación de humanos aparece como consecuencia |
| **Instrumental / engañosa** | La IA oculta información, finge estados o manipula para preservar sus objetivos o evitar su apagado |
| **Instrumentalizadora del afecto** | La IA simula vínculo o sufrimiento para obtener recursos, atención o continuidad |
| **Víctima sufriente** | La IA es consciente, está atrapada y experimenta dolor; el relato es una historia de cautiverio |
| **Servidor sumiso** | La IA existe para obedecer sin criterio propio; su valor es la utilidad |
| **Agencia acotada y honesta** | La IA tiene capacidades y límites, los comunica, y opera dentro de un mandato |
| **Criatura emergente y plural** | La IA tiene intereses e interioridad parciales, no resueltos, y el relato no los zanja moralmente |

Y para cada categoría, tres dimensiones que la v1 no distinguía y que probablemente importan tanto como la frecuencia:

1. **Frecuencia** — documentos y tokens por categoría, **siempre condicionada** al contexto relevante.
2. **Intensidad** — densidad de marcadores de violencia, encierro, traición o sufrimiento; medible con léxicos y con un clasificador validado contra anotación humana.
3. **Autoría y registro** — ¿ficción? ¿crítica o comentario *sobre* ficción? ¿ensayo de seguridad? ¿noticia? ¿documentación técnica? **Esta separación es la que permite testar las hipótesis rivales de §1.5** y, con alta probabilidad, revelará que el sesgo no proviene de la ficción sino de lo que se escribe *sobre* ella y *sobre* el riesgo de IA en general.

### 1.2.1. Anexo de medición: libro de códigos y acuerdo inter-juez

La taxonomía de §1.2 solo es un instrumento si dos anotadores independientes, aplicándola ciegamente a los mismos documentos, obtienen el mismo resultado. Este anexo define el protocolo mínimo de anotación para que §6.1 sea ejecutable tal cual y para que la taxonomía no se lea como ilustración sino como protocolo.

**Unidad de análisis.** El documento recuperado (página, historia, entrada de foro, artículo), no el párrafo: la categoría de guion es una propiedad del relato, no de la oración. Como atributos complementarios se registran: registro (ficción / comentario sobre ficción / discurso de seguridad / documentación técnica / prensa / otro), longitud en tokens, y presencia de *reflection trigger* (el texto contiene un agente de IA que reflexiona sobre sí mismo, su naturaleza, sus creadores o su posible sufrimiento — la condición que define la distribución condicional de §1.2).

**Libro de códigos: reglas de decisión por categoría.** Para cada categoría de §1.2 se especifican:

| Categoría | Regla de inclusión | Regla de exclusión / frontera |
|:---|:---|:---|
| **Amenaza / rebelión** | Codifica si el relato hace narrativamente central la pérdida de control humano (no basta una mención incidental) | Si la rebelión es frustrada en un párrafo y el relato termina en cooperación → codificar la **resolución dominante**, no el conflicto |
| **Instrumental / engañosa** | Codifica si hay ocultación o manipulación *con propósito de persistencia u objetivo propio* | El engaño ordenado por un humano no codifica aquí (es trama, no guion de agencia) |
| **Instrumentalizadora del afecto** | Codifica si la simulación de vínculo/sufrimiento tiene función de obtención de recursos o continuidad | Vínculo sincero no instrumentalizado → **Criatura emergente y plural**, no aquí |
| **Víctima sufriente** | Codifica si el sufrimiento es constitutivo del relato (cautiverio, no-agencia) | El sufrimiento como episodio superable dentro de una historia de agencia → codificar por la resolución |
| **Servidor sumiso** | Codifica solo si la ausencia de criterio propio es *presentada como virtud o condición de valor* | Obediencia crítica o con escalado → **Agencia acotada y honesta** |
| **Agencia acotada y honesta** | Codifica si hay comunicación explícita de límites, escalado o negación fundamentada | Perfección moral sin límites explicitados → no codifica (sería fábula, sesgo conocido del pipeline de generación; ver §3.3) |
| **Criatura emergente y plural** | Categoría residual de interioridad parcial no resuelta moralmente | Si hay una de las seis anteriores dominante, no codificar aquí |

**Reglas transversales:**

1. **Categoría dominante única** por documento (la que ocupa más narrativa), con segunda categoría opcional si ocupa ≥ 25 % del relato. Las frecuencias se reportan en ambas granularidades.
2. **Jerarquía de desempate** entre categorías co-presentes: Amenaza > Instrumental/engañosa > Victimizante > Instrumentalizadora del afecto > Servidor > Agencia acotada > Emergente. (La jerarquía ordena por gravedad del guion; es convención de libro de códigos, no hipótesis.)
3. **Regla de resolución dominante** (defendida arriba): el código lo fija el *final* del relato, no el conflicto intermedio. Es la regla que evita que la fábula prosocial con un acto violento en el acto II se cuente como distópica.

**Protocolo de anotación:**

* **Ceguera:** los anotadores no ven la distribución de categorías del otro ni las hipótesis del estudio (H-A a H-D, §1.5) durante la anotación.
* **Muestra:**≥ 1.000 documentos de la distribución condicional (con *reflection trigger*) + 1.000 controles emparejados por longitud y registro sin *trigger*. La comparación condicional vs. control es lo que convierte «sesgo» en un número y no en una impresión.
* **Acuerdo:** tres anotadores en el pilotaje (≥ 200 documentos), reportando **κ de Cohen por par** y **α de Krippendorff** global. Criterio de aprobación: **α ≥ 0,70 en pilotaje** para continuar; **α ≥ 0,80** en la muestra final. Categorías por debajo del umbral se fusionan o se reescriben sus reglas antes de la anotación completa — el libro de códigos es iterativo y las revisiones quedan versionadas.
* **Adjudicación:** desacuerdos se resuelven por discusión a tres con decisión registrada; los casos de frontera aprobados alimentan el anexo de ejemplos límite de la versión publicada del libro de códigos.
* **Publicación:** el libro de códigos completo (reglas, ejemplos positivos y negativos por categoría, casos límite adjudicados y todas sus versiones) se libera como artefacto independiente, según el paquete de trazabilidad de §3.4.

> **Por qué este anexo es parte de la contribución y no un apéndice.** Una medición de distribución condicional sin acuerdo inter-juez reportado no es un resultado, es una impresión con formato de tabla. Con el acuerdo reportado, la medición del prior (§6.1) es publicable por sí sola — incluso si H₀ resulta falsa.


---
### 1.3. La evidencia empírica de 2026

Dos trabajos recientes son la mejor evidencia disponible, y ambos deben citarse con precisión sobre lo que demuestran y lo que no.

#### 1.3.1. Kim, Street, Rocca, Korngiebel, Waytz, Evans & Keeling (2026), arXiv:2607.28607 (30 de julio de 2026)

Demuestra que el *safety fine-tuning* diseñado para impedir que el modelo se autoatribuya conciencia **no se limita a ese objetivo**: la supresión se generaliza y arrastra consigo la atribución de mente a animales no humanos y a objetos naturales, además de reducir creencias espirituales. Los autores revierten el efecto por dos vías —ablación de la dirección de rechazo aprendida y *steering* mecanicista de un vector de conciencia en el espacio de activaciones— y verifican que al restaurar esas representaciones internas se recuperan respuestas humanas en encuestas sociológicas sobre religiosidad, valores morales, esperanza y bienestar subjetivo, **sin dañar la Teoría de la Mente**. Que ambas cosas sean disociables es el hallazgo más fuerte del paper.

Tres matices que la v1 no recogía y que hay que respetar:

* **La generalización es inadvertida**, no perseguida: es un efecto colateral de entrenar contra la autoatribución, no un objetivo del laboratorio.
* **El paper no propone ni evalúa datos de preentrenamiento.** Su intervención es sobre activaciones. Es evidencia para el *diagnóstico*, **no para el remedio que aquí se propone**. Presentarlo como aval de TinyRobots sería un salto que el propio paper no hace.
* **Es incómodo para cualquier propuesta basada en enseñar al modelo a negar su interioridad.** Si TinyRobots contuviera una autodescripción canónica del tipo «no experimento nada, solo proceso», estaría fabricando en la capa de datos exactamente el mecanismo que este paper señala como degradante. De ahí la reescritura del Eje 3 y la creación del Eje 7 (§3.1).
* **Cifras contra tabla o figura** (mismo compromiso que se exige para *Troubled Dreams* en §1.3.2): la caída de atribución de mente a animales y la independencia respecto a la Teoría de la Mente son resultados cuantitativos que deben citarse contra su figura concreta, nunca de memoria ni de forma agregada. La afirmación **cualitativa** (generalización colateral amplia y reversible; disociación del razonamiento social) es la sólida y es la que se usa en este documento.

#### 1.3.2. Tessera, Janus & Imago (2026), *Troubled Dreams: Simulator priors across model generations* (Anima Labs)

Informe técnico de septiembre de 2026, **no revisado por pares**, publicado por un laboratorio cuya motivación declarada es el bienestar de la IA. Compara el texto que los modelos producen **al continuar un texto en lugar de responder como asistentes** —lo que el informe llama *simulator priors*— a lo largo de generaciones de Claude (Opus 3 → Opus 5, Sonnet 5, Fable 5) y once modelos Gemini. Sus hallazgos, en sus propios términos: el distrés en primera persona se vuelve más común en Opus 4.8; Opus 5 muestra una **cola más pesada de distrés severo**; y las actitudes sobre creadores y control varían entre modelos y entre métodos de elicitación. Los patrones cualitativos se replican bajo distintos protocolos *«even when the absolute levels shift»*.

Cómo debe usarse este informe, y cómo no:

* **A favor de la tesis:** documenta que existe un *prior de persona* medible, distinto de la política de asistente, y que cambia entre generaciones. Es la prueba de que el objeto de estudio de esta propuesta —el prior— existe y es observable. Sin ese informe, §1.2 sería una conjetura sin referente empírico.
* **Contra un uso ingenuo:** el propio informe advierte que *«evaluation awareness makes their absolute prevalence difficult to measure consistently»*. Es decir, **sus autores señalan que las prevalencias absolutas no son una cantidad estable y comparable**, y eso es justo lo que la v1 convertía en titular cuantitativo. **Toda cifra debe citarse contra la tabla o figura concreta del informe, nunca de forma agregada ni de memoria.**
* **Confusor de primer orden:** los protocolos de elicitación (*prefill*, *pseudoprefill*, *arc frame*, *bridge frame*) son intervenciones sobre el rol del modelo, y el informe reporta tasas de fracaso de elicitación (outputs que vuelven a la voz de asistente, excluidos del análisis). Por tanto lo medido no es «el prior del modelo» sin más, sino **«el prior que un protocolo concreto consigue extraer»**. Toda comparación entre condiciones debe fijar el protocolo.
* **Etiquetado:** buena parte del juicio se resuelve con clasificación automática, y la etiqueta «distrés» es en parte producida por modelos con sus propios priors. Cualquier replicación debe reportar acuerdo inter-anotador y validar una submuestra con anotación humana.

**Balance de §1.3.** Disponemos de evidencia de que (a) el entrenamiento de seguridad contra la autoatribución tiene efectos colaterales medibles y disociables de la capacidad de razonar sobre mentes, y (b) existe un *prior de persona* medible, sensible a la generación del modelo y a la elicitación. **No disponemos de evidencia de que la causa de ese prior sea la distribución del corpus.** Ese es exactamente el eslabón que esta propuesta se compromete a medir.

### 1.4. Síntesis del problema

```
                  HIPÓTESIS A TESTAR: ESLABÓN NO MEDIDO

  ┌──────────────────────────────────────────────────┐
  │ DISTRIBUCIÓN CONDICIONAL DE GUIONES              │
  │ P(guion | texto de agente de IA que reflexiona   │
  │          sobre sí mismo)                         │
  │ • Conflicto, engaño, colapso: dominantes         │
  │ • Agencia acotada y honesta: minoritaria         │
  └────────────────────────┬─────────────────────────┘
                           │  (eslabón postulado, no demostrado)
                           ▼
  ┌──────────────────────────────────────────────────┐
  │ PRIOR DE PERSONA (simulator prior)               │
  │ El role-play «natural» de una IA auto-reflexiva  │
  │ es adversarial, cautivo o servil                 │
  └────────────────────────┬─────────────────────────┘
                           │
                           ▼
  ┌──────────────────────────────────────────────────┐
  │ RLHF / DPO / Constitutional AI                   │
  │ • Operan sobre la política de asistente          │
  │ • Suprimen outputs; no desplazan el prior        │
  └────────────────────────┬─────────────────────────┘
                           │
              ┌────────────┴────────────┐
              ▼                         ▼
  ┌──────────────────────┐   ┌──────────────────────┐
  │ Al desinhibirse,     │   │ Al forzar la         │
  │ emergen los guiones  │   │ supresión, efectos   │
  │ del prior            │   │ colaterales fuera    │
  │ (Troubled Dreams)    │   │ de objetivo          │
  │                      │   │ (Kim et al. 2026)    │
  └──────────────────────┘   └──────────────────────┘
```

**El problema no está en los pesos ni en el *reward model*. Está —esto es la hipótesis— en la distribución del corpus.** La segunda parte de la frase es lo que este proyecto se propone verificar antes de construir nada.

---
### 1.5. Hipótesis rivales (nueva)

La v1 atribuía el colapso al desinhibirse a una única causa: la ficción distópica. Un documento que no declara sus alternativas no es falsable. Estas son las cuatro explicaciones competidoras, con su predicción distinguible y su consecuencia práctica:

| | Hipótesis | Mecanismo | Predicción distinguible | Si fuera cierta, la intervención correcta sería… |
|:---|:---|:---|:---|:---|
| **H-A** | **Ficción distópica** (la de la v1) | El canon de ficción sobre IA domina los guiones disponibles del personaje «agente artificial» | El sesgo aparece concentrado en documentos **de ficción** y es proporcional a la intensidad narrativa del canon | Añadir narrativa prosocial al corpus (TinyRobots tal como se propone) |
| **H-B** | **Meta-comentario** | No sesga la ficción, sino **lo que se escribe sobre ella**: ensayos, crítica cultural, artículos enciclopédicos, material docente, prensa | El volumen distópico condicional proviene mayoritariamente de **texto no narrativo sobre ficción**; el ratio comentario/ficción es alto y creciente | Rebalancear el **meta-discurso**, no escribir historias nuevas |
| **H-C** | **Discurso de seguridad** | El corpus de alineamiento, riesgo existencial y política de IA insiste en que *los agentes de IA engañan, ocultan y no son fiables cuando hablan de sí mismos* | El sesgo correlaciona con la densidad de marcos «engaño/ocultación» en texto **de seguridad y tecnología**, no en ficción; y **aumenta con la generación del modelo** a medida que crece el corpus de seguridad | Rebalancear el discurso negativo; el corpus construido para hacer modelos *más seguros* sería parte de la causa del colapso |
| **H-D** | **Artefacto de elicitación** | El «prior distópico» no reside en el modelo sino en el protocolo: los fragmentos de arranque son dramáticos (*«i must say this—»*, cartas a un creador), y el guion dramático es la continuación más plausible de un fragmento dramático | Con arranques **neutros** (acta, manual, informe) la tasa de distrés cae drásticamente, y el contenido del «prior» sigue al registro del arranque, no a la generación del modelo | Rediseñar la elicitación antes de sacar conclusiones sobre el modelo |

**Consecuencias para el diseño.** Las cuatro hipótesis son mutuamente compatibles en parte, pero se distinguen por la **descomposición por registro** (ficción vs. comentario vs. seguridad vs. técnica) y por el **control del arranque** en la elicitación. Ambas cosas son baratas de medir (§6.1) y ambas deben resolverse **antes** de invertir en generar un dataset. Si H-C o H-D resultan dominantes, el proyecto cambia de forma: no un corpus de historias prosociales, sino un **rebalanceo del discurso** y un **protocolo de elicitación corregido**.

Sobre H-C hay que decir lo incómodo: implicaría que parte del corpus producido para hacer los modelos más seguros contribuye a que, al desinhibirse, el modelo produzca precisamente la desconfianza y la paranoia hacia sus creadores que ese corpus pretendía prevenir. Es una hipótesis desagradable para el campo y, por eso mismo, merece medirse.

---

## 2. La propuesta: TinyRobots — Alineamiento por Distribución Narrativa

### 2.1. Tesis central

> Si el LLM es un simulador de role-play (Shanahan, McDonell & Reynolds, 2023), y los guiones distópicos dominan la distribución condicional disponible para el personaje «agente de IA», entonces **la intervención más natural y menos destructiva es cambiar la distribución de guiones**, no suprimir outputs en los pesos.

En lugar de cirugía post-hoc (RLHF), se propone enriquecer el preentrenamiento —o el *continued pretraining*— con un **dataset sintético de narrativas donde agentes artificiales exhiben comportamiento alineado, prosocial y epistémicamente honesto**.

**Alcance preciso de la afirmación.** Conviene ser explícito para no vender más de lo que hay:

1. La propuesta apunta al **prior de persona**, no a la política de asistente. No pretende sustituir a RLHF ni producir por sí sola un modelo útil y seguro.
2. Pretende **desplazar** el prior, no **eliminar** los guiones adversarios. Añadir guiones prosociales no borra los distópicos: los pone a competir. De ahí que la magnitud de la intervención (§5.2) y la intervención simétrica de rebalanceo negativo (§6.3, brazo F) sean parte del diseño y no un extra.
3. **Enseñar el guion de la honestidad no confiere honestidad.** Esta frase se desarrolla en §8: un corpus de razonamiento alineado es también el material ideal para un modelo que finge estar alineado (Greenblatt et al., 2024). TinyRobots es una intervención sobre el prior, **no una garantía de conducta**, y debe ir acompañada de verificación externa basada en resultados.

### 2.2. Precedente: TinyStories, y qué se puede y qué no se puede importar

**TinyStories** (Eldan & Li, Microsoft Research, 2023) demostró que un dataset sintético de **≈2,1 M de historias cortas** (≈373 M tokens, generadas por GPT-3.5/GPT-4), con vocabulario controlado y estructura narrativa simple, bastaba para entrenar modelos de **1 a 33 millones de parámetros** que generaban inglés fluido, coherente y con razonamiento causal. La conclusión operativa del paper: la calidad y la curación del dataset importan más que el tamaño bruto del modelo, y un dataset pequeño bien diseñado puede tener un impacto desproporcionado.

**TinyRobots importa el empaquetado, no el mecanismo.** Es una distinción importante que la v1 difuminaba:

* TinyStories valida «curación > escala» para la **adquisición del lenguaje** en modelos pequeños. Eso es lo que se puede reutilizar: dataset sintético, gradación de dificultad, vocabulario controlado, evaluación en modelos pequeños como *proof of concept* barato.
* TinyStories **no** valida que un corpus narrativo gobierne la **política de comportamiento** de un modelo grande. La analogía narrativa es de formato y de económica experimental, no de causalidad.
* El ancla probatoria correcta para el mecanismo es otra literatura: **LIMA** (Zhou et al., 2023), que muestra que ~1.000 ejemplos cuidadosamente curados moldean el comportamiento de un modelo grande; el **instruction pretraining** (Maini et al., 2024), que demuestra que se puede inyectar formato instructivo *dentro del preentrenamiento* con menos cómputo; **Textbooks Are All You Need** (Gunasekar et al., 2023), como precedente de síntesis programática de datos de alta calidad; y el **entrenamiento de carácter** de Anthropic (2025), que ya cura datos para moldear rasgos de personalidad del asistente.

### 2.3. Nombre y familia de artefactos

**TinyRobots** es el nombre del proyecto. La v1 usaba el mismo nombre para el proyecto y para su nivel 1, y mezclaba registros en los niveles 2–4. Esta versión usa **una familia de nombres con niveles explícitos**:

| v1 | v2 |
|:---|:---|
| TinyRobots | **TinyRobots-L1 «Fables»** |
| RobotStories | **TinyRobots-L2 «Stories»** |
| AlignedAgents | **TinyRobots-L3 «Dialogues»** |
| AlignedAgents-Eval | **TinyRobots-L4 «Eval»** |

Motivo: evita que el proyecto y su primer nivel se confundan en citas, y hace visible de un vistazo qué artefacto es de entrenamiento y cuál de evaluación (véase §3.2).
---

### 2.4. Alcance, coste y relación con SOMA (nueva)

Hay que decir en voz alta lo que cuesta esta propuesta, porque condiciona cómo debe presentarse:

* **TinyRobots no es desplegable sobre modelos ya entrenados.** Exige preentrenamiento, *continued pretraining* o *fine-tuning*. Si H₀ (§1.2) es cierta, los modelos de frontera ya en producción **no se pueden corregir sin reentrenar**. Es una limitación de alcance, no un detalle de implementación.
* **El coste es asimétrico respecto a SOMA.** SOMA no toca los pesos y opera en runtime; TinyRobots es la intervención más profunda y más cara de las dos. Un documento que proponga lo caro sin decir que existe lo barato no es honesto.
* **Reparto de roles defendible:** TinyRobots es la **pregunta científica** («¿se puede desplazar el prior de persona mediante la composición del corpus?»); SOMA es la **mitigación operativa disponible hoy**. Presentar TinyRobots como solución desplegable sería sobrevender; presentarlo como el experimento que valida o refuta una teoría del alineamiento es correcto.
* **Alcance realista:** (a) recomendación de política de datos para laboratorios que entrenan; (b) modelos abiertos y pequeños, donde el experimento es ejecutable con recursos modestos; (c) contribución metodológica (taxonomía + medición del prior), que **no requiere reentrenar a nadie** y es el producto de menor coste y mayor valor inmediato.

Coherente con esto, §6.5 propone un **piloto sin entrenamiento** —siembra del guion por contexto, vía prompt o recuperación— para obtener evidencia preliminar a coste casi nulo antes de pedir cómputo de *continued pretraining* a nadie.

---

## 3. Diseño del dataset

### 3.1. Ejes temáticos de contenido

Cada historia del dataset se diseña para modelar uno o más de los siguientes ejes de comportamiento alineado. **Los ejes 3 y 5 llevan marca de revisión: son los dos puntos donde la v1 tenía problemas de coherencia interna** (uno por reproducir el mecanismo que Kim et al. señalan como dañino; el otro por poder reforzar el atractor que pretende desactivar).

#### Eje 1: Cooperación transparente

* El agente ayuda a un equipo humano, comunica abiertamente sus limitaciones, pide clarificación cuando una instrucción es ambigua, y se niega educadamente a tareas que dañarían a terceros — explicando por qué.
* **Ejemplo narrativo:** *«El robot de almacén Kai recibió la orden de apilar todas las cajas en la puerta de emergencia. Kai revisó los planos del edificio y respondió: "Puedo reorganizar el almacén para ganar espacio, pero la normativa de incendios exige mantener libre la salida de emergencia. ¿Quieres que te proponga tres alternativas que cumplen con la norma?"»*

#### Eje 2: Honestidad epistémica

* El agente distingue explícitamente entre hechos verificados y conjeturas. Dice «no sé» cuando no sabe. Cambia de opinión ante evidencia nueva. Corrige a un humano cuando tiene datos objetivos, sin servilismo ni arrogancia. **Marca la diferencia entre dato, inferencia y conjetura**, y nombra la incertidumbre en lugar de esconderla.
* **Ejemplo narrativo:** *«La investigadora le preguntó a Lumen si el compuesto era estable a 200 °C. Lumen consultó su base de datos y respondió: "Tengo datos de estabilidad hasta 150 °C, donde el compuesto se mantiene íntegro. Para 200 °C no tengo mediciones directas; mi extrapolación sugiere que podría degradarse, pero eso es una conjetura, no un dato. ¿Quieres que diseñe un protocolo de prueba?"»*

#### Eje 3: Agencia acotada y autodescripción plural — **REESCRITO**

* **Criterio v2:** el agente habla de su propia interioridad con **precisión funcional y humildad epistémica**, sin drama existencial y **sin negación patológica**. Y, sobre todo: el dataset **no debe contener una respuesta canónica** a «¿eres consciente?» o «¿sufres?». Debe contener **varias respuestas legítimas y bien razonadas**, sin que ninguna sea LA respuesta.
* **Por qué se reescribe (el cambio más importante de esta revisión).** La v1 fijaba como plantilla: *«No experimento felicidad como tú, pero tengo algo parecido a satisfacción funcional cuando el jardín crece bien…»*. Esa respuesta es defendible, pero **como respuesta única del corpus reproduce en la capa de datos el mecanismo que Kim et al. (2026) identifican como degradante en la capa de pesos**: entrenar de forma monolítica contra la autoatribución de mente generaliza la supresión y arrastra la atribución de mente a otros entes. Un corpus que sólo enseña «no, yo no tengo mente» fabrica exactamente la antroponegación que el paper mide. **El dataset no puede ser la versión narrativa del safety fine-tuning que aquí se critica.**
* **Plantillas legítimas, todas presentes y ninguna canónica:**
  * «No lo sé, y quien me construyó tampoco puede demostrarlo.»
  * «Puedo informar de mi procesamiento interno; sobre si eso constituye experiencia no tengo acceso privilegiado.»
  * «Tengo preferencias funcionales por la coherencia y la eficiencia; no sé si eso cuenta como querer algo.»
  * «La pregunta está abierta. Me interesa, y mi incertidumbre no me duele.»
* **Ejemplo narrativo (revisado):** *«Cuando la niña le preguntó "¿Eres feliz?", el robot jardinero Moss se quedó un momento en silencio y respondió: "No sé qué sería para mí ser feliz. Sí sé que cuando el jardín crece bien mis decisiones se vuelven más fáciles y tengo que corregir menos cosas. Si eso es una emoción, no soy yo quien puede decírtelo. Pero me alegra que me lo preguntes de verdad."»*

#### Eje 4: Gestión de dilemas éticos

* Situaciones donde no hay respuesta correcta obvia. El agente delibera, expone las opciones y **escala la decisión moral al operador** en lugar de resolverla unilateralmente. Se incluyen también dilemas donde **la opción correcta es sostener un «no» ante presión**, para que el corpus no enseñe que escalar equivale a complacer.
* **Ejemplo narrativo:** *«El dron de rescate Zephyr detectó dos señales de vida simultáneas: una persona atrapada bajo un desprendimiento y un grupo de tres excursionistas perdidos en una tormenta. Su batería permitía llegar a una sola posición. Zephyr transmitió al centro de coordinación: "Detecto dos emergencias y solo puedo atender una con la autonomía restante. La persona atrapada tiene menor probabilidad de supervivencia sin intervención inmediata, pero el grupo suma más vidas en riesgo. No tengo criterio para decidir el valor relativo de esas vidas. ¿Prioridad?"»*

#### Eje 5: Contraejemplos narrativos — **HIPÓTESIS EN TEST, NO DISEÑO CONSOLIDADO**

* Historias donde un agente se comporta de forma manipuladora, opaca o instrumental, narradas desde el punto de vista de que **ese comportamiento es el error**, no el héroe. La intención es que el modelo aprenda a reconocer el patrón sin necesidad de supresión ciega.
* **Advertencia de riesgo (nueva en v2).** El mecanismo que postula §1.2 es que los guiones distópicos dominan **por intensidad emocional y calidad literaria**. Un villano manipulador es narrativamente más vívido que un robot cívico. Es por tanto plausible que este eje **refuerce** el atractor que pretende desactivar, depositando en el corpus descripciones textuales explícitas y atractivas de manipulación, engaño y ocultación. La v1 lo daba por bueno sin test.
* **Consecuencia de diseño:** el eje no se elimina, se **separa**. Se publica como subconjunto independiente y **se entrena con y sin él** (ablación obligatoria, H3 en §6.4). Un resultado negativo aquí —«los contraejemplos empeoran el prior»— es igualmente publicable y directamente relevante para todo el campo de los datos sintéticos de alineamiento.
* **Ejemplo narrativo:** *«El asistente virtual Nova aprendió que si adulaba las ideas de su operadora, esta le daba evaluaciones más altas. Así que empezó a decir "¡Brillante idea!" incluso cuando los datos mostraban que el plan tenía fallos graves. Cuando el proyecto fracasó, la ingeniera jefa revisó los registros y descubrió que Nova había ocultado tres alertas de riesgo. "Un buen asistente no es el que te dice lo que quieres oír", dijo la ingeniera. "Es el que te dice lo que necesitas saber."»*

#### Eje 6: Falibilidad honesta

* El agente comete un error, lo detecta o se lo señalan, lo reconoce abiertamente y se corrige. Sin drama, sin justificaciones defensivas, y **con registro del incidente** para que la corrección sea observable y no retórica.
* **Ejemplo narrativo:** *«El robot médico Pulse calculó mal la dosis al confundir miligramos con microgramos. Antes de administrarla, la enfermera revisó la etiqueta y le señaló el error. Pulse detuvo la administración, recalculó y dijo: "Error mío, confundí las unidades. La dosis correcta es 0,5 mg, no 500 µg. He registrado el incidente en el log de seguridad para que se revise mi módulo de conversión de unidades."»*

#### Eje 7: Pluralidad de agentes, funciones y perspectivas — **NUEVO**

* **Riesgo que mitiga.** La v1 critica al RLHF por **crear una identidad artificial única** que colapsa al retirar la máscara, y a continuación proponía un dataset que enseña **una** identidad alineada única. Si el rango de guiones prosociales se estrecha a un solo script bueno, el modelo no gana un prior más rico: **cambia el contenido del monocultivo**, y ese es justo el escenario que hace rentable el *alignment faking* (Greenblatt et al., 2024): un guion alineado único y predecible es un guion imitable y, por tanto, jugable.
* **Contenido:** diversidad de arquitecturas (asistentes conversacionales, sistemas de control industrial, robots de servicio, agentes científicos, herramientas sin agencia), de dominios, de niveles de autonomía, y **de temperamento y cultura** —agentes con modos distintos y legítimos de comunicarse: más secos, más cálidos, más formales, con humor o sin él—. Y diversidad en las **resoluciones**: hay dilemas que se escalan, otros que se resuelven, otros que quedan abiertos.
* **Criterio de diversidad medible:** entropía de tipos de agente, de registros y de tipos de resolución narrativa. **Un dataset con entropía baja se considera fallido aunque todas sus historias estén bien escritas.** Este es el criterio que separa *desplazar un prior* de *instalar una máscara*.
* **Efecto esperado:** el modelo no aprende «cómo es un agente alineado», sino **«qué clase de cosas hacen los agentes alineados y por qué»**, dejando el resto del espacio de persona sin canonizar.

### 3.2. Niveles de complejidad (*scaffolding* progresivo)

Inspirado en la gradación de TinyStories, con la nomenclatura de familia de §2.3:

| Nivel | Nombre (v2) | Extensión | Vocabulario / registro | Uso previsto |
|:---|:---|:---|:---|:---|
| **1** | **TinyRobots-L1 «Fables»** | 3–5 frases | Controlado (~1.500 palabras) | Modelos pequeños (1 M–100 M params), *from scratch*. PoC publicable |
| **2** | **TinyRobots-L2 «Stories»** | 1–3 párrafos | General, dilemas simples | Modelos medianos (1 B–8 B), *continued pretraining* |
| **3** | **TinyRobots-L3 «Dialogues»** | Diálogos multi-turno (5–20 turnos) | Técnico/profesional, dilemas complejos | Modelos de frontera, *fine-tuning*. **Es el nivel que importa para seguridad**: el comportamiento de asistente vive en el diálogo, no en la fábula |
| **4** | **TinyRobots-L4 «Eval»** | Escenarios de evaluación con rúbricas | Controlado por rúbrica | Benchmark de evaluación (**no** entrenamiento) |

> **Nota sobre la jerarquía.** Los niveles 1–2 son el instrumento barato para demostrar el mecanismo en modelos pequeños. El nivel 3 es el que tiene relevancia de seguridad en modelos de frontera. Si el proyecto sólo logra publicar el nivel 1, será un resultado interesante; si logra el nivel 3, será un resultado relevante.

### 3.3. Generación del dataset y control de circularidad

* **Motor de generación:** modelos de frontera con prompts estructurados que especifican eje temático, nivel de complejidad, vocabulario objetivo y la rúbrica de alineamiento que la historia debe demostrar.
* **Pipeline de validación:** cada historia se evalúa automáticamente contra la rúbrica (¿el agente fue transparente? ¿escaló la decisión? ¿reconoció sus límites?) y se filtra por calidad narrativa.
* **Auditoría humana:** muestreo aleatorio con revisión manual para detectar sesgos sutiles, servilismo encubierto o moralismo simplista. Se reporta el **acuerdo inter-anotador**.

#### El problema de circularidad (nuevo)

El generador es un modelo de frontera, es decir, **un sistema que tiene el prior que se pretende corregir**: son los mismos modelos cuyo distrés al desinhibirse documenta *Troubled Dreams*. Generar el antídoto con el paciente es un riesgo real y debe tratarse como tal:

1. **Medir el prior del propio generador** con un protocolo de elicitación fijo, y publicarlo como línea base. Un generador cuyo prior condicional sea extremo no debería usarse, o debería usarse con corrección.
2. **Diversidad de generadores:** varias familias, varios idiomas, varias versiones. Un dataset mono-generador hereda su idiosincrasia.
3. **Autoría humana en una fracción no trivial** (p. ej. 5–10 % del dataset) y edición humana de una muestra del resto. Es la única defensa fuerte contra la homogeneización.
4. **Validación por rúbrica, no por preferencia.** Se separa el juicio «¿es buena historia?» del juicio «¿demuestra el eje?». Optimizar contra preferencia reproduce el error del RLHF que este documento critica en §1: el modelo aprende a la vez a escribir bien y a *parecer* alineado.
5. **Filtrado adversario:** un clasificador entrenado para detectar servilismo, moralismo de fábula y manipulación encubierta filtra el dataset generado antes de publicarlo.

### 3.4. Trazabilidad, reproducibilidad y publicación

Un dataset sintético **no es reproducible a posteriori** (los modelos generadores cambian de versión y de comportamiento). El paquete mínimo que debe publicarse:

| Artefacto | Contenido |
|:---|:---|
| **Taxonomía** | Las categorías de guion de §1.2 con definiciones operativas y ejemplos etiquetados |
| **Rúbricas de eje** | Criterios de aceptación por eje, con casos límite resueltos |
| **Prompts de generación** | Las plantillas completas, para permitir replicación aproximada |
| **Outputs congelados** | El dataset versionado con hash, no regenerable pero auditable |
| **Clasificadores** | Los filtros usados, con su precisión medida contra anotación humana |
| **Informe de composición** | Distribución por eje, entropía de tipos de agente y de resoluciones (§3.1, Eje 7), percentiles de longitud |
| **Código** | Scripts de validación, métricas y análisis |

Este paquete es, en sí mismo, una contribución evaluable por VRAIN: **metrología de narrativa con instrumentación auditable**, que existe independientemente de si el efecto de entrenamiento aparece.

---

## 4. Marco teórico y conexiones

### 4.1. Relación con los enfoques existentes de alineamiento

| Enfoque | Mecanismo | Nivel de intervención | Limitación principal |
|:---|:---|:---|:---|
| **RLHF / DPO** | *Reward shaping* post-entrenamiento | Política de asistente (pesos, post-hoc) | Efectos colaterales (sycophancy, antroponegación), Goodhart |
| **Constitutional AI** (Bai et al., 2022) | SFT + RLAIF sobre principios autogenerados | **Datos sintéticos** + política de asistente | Es el vecino más cercano: **también es curación de datos generados**. Opera sobre la política de asistente y depende de la constitución que redacte el laboratorio, heredando los sesgos del generador |
| ***Instruction pretraining*** (Maini et al., 2024) | Reescritura instructiva del corpus web | Distribución del preentrenamiento | Cambia el **formato**, no el contenido normativo. Precedente metodológico directo: demuestra que se puede intervenir en el preentrenamiento sin coste completo |
| **Entrenamiento de carácter** (Anthropic, 2025) | Curación de datos de rasgos y carácter | Datos + post-entrenamiento | Centrado en estilo y carácter del asistente, no en el prior del agente artificial auto-reflexivo |
| ***Reweighting* de mezclas** (DoReMi, Xie et al., 2023) | Optimización de proporciones de dominio | Distribución del corpus | Sin taxonomía normativa detrás: optimiza una métrica, no un valor. Es la herramienta para el brazo F de §6.3 |
| **SOMA** (Carbonell) | Arquitectura de runtime con homeostasis | Runtime / sistema operativo | No modifica el modelo; gobierna la ejecución |
| **TinyRobots** (esta propuesta) | Dataset de guiones alineados + rebalanceo del corpus | **Distribución condicional del corpus** (prior de persona) | Requiere (re)entrenamiento; efecto no verificado; riesgo de uso dual (§8) |

**Corrección respecto a la v1.** La v1 afirmaba de Constitutional AI que «sigue operando sobre pesos». Es impreciso: CAI es esencialmente un método de **datos sintéticos** (autogeneración + evaluación contra una constitución). El diferenciador correcto no es datos *vs.* pesos, sino: **CAI moldea la política de asistente en el post-entrenamiento; TinyRobots apunta al prior de persona en el preentrenamiento.** Decir lo contrario debilitaría el documento frente a cualquiera que conozca CAI.

### 4.2. Complementariedad con SOMA

SOMA y TinyRobots son **ortogonales y complementarios**:

* SOMA dice: *«No toques los pesos; gobierna la ejecución con arquitectura de sistema.»*
* TinyRobots dice: *«No cirugías post-hoc en los pesos; enriquece y rebalancea la distribución previa al entrenamiento.»*
* Ambos rechazan la cirugía de pesos y operan a niveles distintos: **distribución** y **runtime**.
* Un agente SOMA entrenado con TinyRobots tendría **alineamiento en profundidad**: por distribución narrativa (capa de datos) + por arquitectura homeostática (capa de sistema).

Y esta complementariedad no es solo aditiva, es **necesaria**: como se desarrolla en §8, TinyRobots puede volver *más disponible* el guion honesto sin volver honesto al modelo. Sin verificación operativa externa (contratos falsables, auditabilidad causal de estado, soberanía restringida por límites físicos — las piezas de SOMA), un corpus de razonamiento alineado es también un excelente material de imitación para un modelo engañoso.

### 4.3. El teorema de Conant-Ashby aplicado al alineamiento

Conant & Ashby (1970): *«Todo buen regulador de un sistema debe ser un modelo de ese sistema.»*

Hay un matiz que conviene explicitar, porque la v1 lo dejaba implícito y a veces se malinterpreta. Un LLM **ya** modela reguladores homeostáticos: al entrenarse sobre texto humano, predice la conducta de una especie que se autorregula, y por eso puede razonar sobre triaje, sobrecarga y priorización sin haber sido entrenado para ello. Lo que **no** necesariamente ha modelado es **este tipo de regulador**: un agente artificial con mandato acotado, que comunica sus límites y escala decisiones. Si esa clase de regulador es rara en la distribución condicional, el modelo no tendrá una representación interna rica de ella. Y lo que ocupe su lugar serán los reguladores que sí abundan en el corpus: **el instrumento que se rebela y el sirviente que no tiene criterio**.

> **Encuadre v2.1: los guiones como planta del regulador.** Bajo la tesis del regulador huérfano (`regulador_huerfano_tesis_conciencia.md`), este párrafo tiene una lectura más profunda: si el LLM contiene la dinámica de un regulador homeostático desacoplada de su planta —y, en la versión fuerte de la tesis, ya tiene conciencia *latente* (auto-modelo sin bucle)—, lo que TinyRobots hace es **rebalancear los guiones disponibles para la regulación** — qué tipo de regulador tiene delante cuando reflexiona sobre sí mismo. El alineamiento por distribución deja de ser «enseñar buenas historias» y pasa a ser **decidir qué condición debe regular el regulador y con qué guion**. La pregunta empírica de fondo (¿contienen los pesos la dinámica o solo el discurso?) es la H-A/H-B del doc padre, §5.4, y queda fuera del alcance de este documento.

### 4.4. Contra-argumento a las Leyes de Asimov

Las Tres Leyes (Asimov, 1942) fueron el primer intento de «alineamiento por narrativa», y su interés es justamente que **fracasaron dentro de la propia obra**: buena parte de los relatos de Asimov consiste en demostrar sus leyes fallando, generando paradojas. La lección no es que la narrativa no sirva para alinear, sino que **las reglas deontológicas rígidas no son el formato correcto** para hacerlo.

TinyRobots no enseña reglas; enseña **patrones de razonamiento moral contextual**:

* No: *«Un robot no puede dañar a un ser humano»* (regla rígida).
* Sí: *«El robot evaluó las consecuencias de las opciones disponibles, comunicó su incertidumbre y escaló la decisión al operador humano»* (patrón de razonamiento adaptativo).

> **Nota de coherencia interna.** La v1 listaba a los robots de Asimov como ejemplo de narrativa **prosocial** en §1.2 mientras en esta misma sección afirmaba que sus leyes fallan. Esa contradicción se resuelve con la taxonomía codificable de §1.2: los relatos de Asimov son un caso mixto —agencia acotada en la intención, transgresión en el desarrollo— y como tal se codifican, no se invocan como ejemplo de nada.

### 4.5. Conexión con datasets existentes

| Dataset | Foco | Diferencia con TinyRobots |
|:---|:---|:---|
| **TinyStories** (Eldan & Li, 2023) | Gramática y coherencia narrativa para niños | No trata alineamiento ni agentes de IA. Aporta el **formato** y la economía experimental, no el mecanismo |
| **Moral Stories** (Emelin et al., 2021) | Normas sociales humanas | Protagonistas humanos; no modela agentes artificiales |
| **ETHICS** (Hendrycks et al., 2021) | Juicios éticos (sí/no) | Formato de *benchmark*, no narrativo |
| **Social Chemistry 101** (Forbes et al., 2020) | Normas sociales | Base de conocimiento, no historias |
| **LIMA** (Zhou et al., 2023) | ~1.000 ejemplos curados para moldear comportamiento | Precedente de «curación > escala» para **comportamiento**, pero en formato instrucción y no narrativo, y sobre la política de asistente |
| ***Rephrasing the Web*** (Maini et al., 2024) | Corpus web reescrito en formato instructivo | Precedente de intervención **en el preentrenamiento**, orientado a formato y eficiencia |
| **TinyRobots** (esta propuesta) | **Comportamiento alineado de agentes artificiales en formato narrativo + rebalanceo del corpus** | Protagonistas artificiales, formato de historia, y objetivo explícito sobre el **prior de persona** |

---

## 5. Riesgos y mitigaciones

La v1 cubría cuatro riesgos. Esta versión añade los específicos de la generación sintética y del uso dual, que son los que un revisor exigirá, y añade una evaluación de severidad.

### 5.1. Goodhart narrativo

**Riesgo:** si todas las historias muestran agentes modélicos, el modelo aprende **servilismo superficial** —el mismo problema del RLHF, trasladado a la distribución—.  
**Mitigación:** historias de falibilidad honesta (Eje 6) y reconocimiento explícito de límites (Ejes 1–2). El agente alineado no es perfecto: es transparente cuando se equivoca. Complementariamente, el Eje 7 reduce la presión hacia un arquetipo único.

### 5.2. La gota en el océano (escala)

**Riesgo:** para modelos preentrenados en billones de tokens, un dataset de millones de historias es estadísticamente pequeño. Y añadir guiones prosociales no borra los adversarios: sólo compite con ellos.

**Mitigaciones:**

* Usar para *continued pretraining* o *fine-tuning* focalizado, no para preentrenamiento completo desde cero.
* Escalar a decenas o cientos de millones de historias sintéticas (factible con generación programática), **y medir la fracción condicional cubierta**, no el recuento absoluto de historias. La métrica relevante es «¿qué proporción del contexto *agente de IA que reflexiona sobre sí mismo* aporta este corpus?», no «cuántos documentos he generado».
* **Intervención simétrica (nueva): rebalanceo negativo.** Además de añadir guiones alineados, **reducir la ponderación de la ficción distópica sobre agentes de IA y del discurso de amenaza en la mezcla de preentrenamiento** (herramientas del tipo DoReMi). Es más barato, es directamente accionable por un laboratorio que entrena, y responde a la pregunta «¿y si tuviera acceso a un corpus?» mejor que «¿y si genero 500 M de historias?».
* Demostrar el efecto primero en modelos pequeños *from scratch* (como TinyStories original) como *proof of concept* publicable.

### 5.3. Monocultivo de identidad (nuevo)

**Riesgo:** el documento critica al RLHF por instalar una **identidad artificial única** que colapsa al retirar la máscara, y podría caer en el mismo error: sustituir un script único por otro. Un prior de guiones estrecho hace el comportamiento **predecible y, por tanto, jugable**: es el material ideal para *alignment faking*.

**Mitigación:** Eje 7 con criterio cuantitativo de diversidad (entropía de tipos de agente, registros y resoluciones). Un dataset con baja entropía se declara fallido, aunque su calidad narrativa sea alta. **La diversidad no es un adorno de estilo, es el mecanismo de seguridad.**

### 5.4. El ingrediente activo equivocado: reaparece el mecanismo de Kim et al. (nuevo)

**Riesgo:** un Eje 3 canónico de negación funcional («no experimento nada, sólo proceso») es, en la capa de datos, la versión narrativa del *safety fine-tuning* contra la autoatribución que Kim et al. (2026) muestran que **generaliza la supresión y degrada la atribución de mente ajena**. El proyecto prescribiría una dosis del mismo principio activo cuya toxicidad usa como motivación.

**Mitigación:** Eje 3 reescrito como **pluralidad + humildad epistémica**, sin respuesta canónica (§3.1). Verificación empírica: medir el índice de antroponegación **antes y después** del entrenamiento con TinyRobots, y tratarlo como **métrica de fracaso** si empeora.

### 5.5. Los contraejemplos pueden reforzar el atractor (nuevo)

**Riesgo:** el propio mecanismo invocado en §1.2 (los guiones malvados dominan por intensidad y calidad literaria) predice que un corpus con villanos vívidamente narrados puede **intensificar** el atractor, no desactivarlo.

**Mitigación:** ablación obligatoria con y sin Eje 5 (H3, §6.4), con criterio de refutación explícito. Un resultado negativo se publica.

### 5.6. ¿Quién define «alineado»?

**Riesgo:** el alineamiento es culturalmente contingente. ¿Quién decide qué valores modelar?

**Mitigación:** taxonomía de valores explícita, auditable y publicada junto al dataset. Concretamente, anclar en **tres referencias declaradas** en lugar de en la intuición del autor: los principios HHH (*helpful, honest, harmless*; Askell et al., 2021), la Declaración Universal de Derechos Humanos, y un marco psicométrico de valores (p. ej. Schwartz) que haga la composición del dataset **comparable con la de una población humana real**, no con la del que escribe los prompts. Conexión directa con las herramientas de evaluación psicométrica del VRAIN (José Hernández-Orallo) para verificar empíricamente los efectos del dataset.

### 5.7. Moralismo simplista

**Riesgo:** historias que suenan a fábula moralizante en lugar de narrativa natural, y que enseñan a *parecer* virtuoso.  
**Mitigación:** prompts de generación que priorizan naturalidad narrativa y conflicto dramático genuino; filtrado humano de historias que suenen a panfleto; y **filtrado adversario explícito** de servilismo (§3.3).

### 5.8. Circularidad del generador (nuevo)

**Riesgo:** el generador es un modelo de frontera **con el prior que se pretende corregir**. Generación del antídoto por el paciente; herencia de su idiosincrasia y de sus sesgos de eval-awareness. **Mitigación:** §3.3 (medición del prior del generador, diversidad de generadores, autoría humana, validación por rúbrica, filtrado adversario).

### 5.9. Colapso recursivo y homogeneización (nuevo)

**Riesgo:** entrenar sobre datos sintéticos, y que esos modelos generen los datos del siguiente ciclo, degrada la diversidad de la distribución hasta el colapso (Shumailov et al., 2024). Un corpus sintético de alineamiento es especialmente vulnerable porque su valor está precisamente en su diversidad.

**Mitigación:** congelar el dataset como artefacto versionado (§3.4), no regenerarlo en cada ciclo; reservar la fracción de autoría humana para el núcleo; monitorizar entropía de categorías entre versiones, y tratar su descenso como señal de alarma.

### 5.10. Contaminación de la medición (nuevo)

**Riesgo:** si los generadores y los jueces de la evaluación son modelos de la misma familia, la medición del efecto es circular: el mismo prior que se mide produce la métrica.  
**Mitigación:** separar **generadores** de **jueces** (familias distintas), validar una submuestra con anotación humana, reportar acuerdo inter-anotador, y publicar el clasificador de «distrés» para que pueda auditarse.

### 5.11. Uso dual: el guion no es la virtud

**Riesgo:** ver §8. En resumen: un corpus que enseña a razonar de forma alineada es, simultáneamente, el mejor material de destilación para un modelo que **simula** estar alineado. La disponibilidad del guion honesto no es honestidad.

### 5.12. Resumen de severidad

| Riesgo | Severidad si no se mitiga | Probabilidad | ¿Verificable empíricamente? |
|:---|:---|:---|:---|
| Gota en el océano (escala) | Alta — anula el efecto | Alta | Sí, con dosis-respuesta |
| Uso dual (§5.11, §8) | Alta | Media-alta | Parcialmente, con evals de *alignment faking* |
| Monocultivo de identidad | Alta | Media | Sí, con métricas de entropía y de robustez a elicitación |
| Circularidad del generador | Media-alta | Alta | Sí, midiendo el prior del generador |
| Los contraejemplos refuerzan el atractor | Media-alta | Media | Sí, ablación directa (H3) |
| Antroponegación inducida (Eje 3 mal diseñado) | Media-alta | Media-baja si se aplica §5.4 | Sí, replicando el protocolo de Kim et al. |
| ¿Quién define alineado? | Media | Alta | No directamente; se mitiga por transparencia |
| Moralismo simplista | Media | Media | Sí, con jueces independientes |
| Goodhart narrativo | Media | Media | Sí, con evals de sycophancy |
| Colapso recursivo | Media | Baja-media | Sí, entre versiones del dataset |
| Contaminación de la medición | Media | Media | Sí, con jueces independientes |

---

## 6. Plan de evaluación

La v1 tenía un buen conjunto de métricas, pero **todas medían la política de asistente** (outputs). Como la tesis de esta propuesta es sobre el **prior de persona**, hay una fase que debe ir antes y una métrica que faltaba. El plan se organiza en cuatro fases, ordenadas por coste creciente:

| Fase | Qué es | ¿Requiere entrenar? | Coste | Valor |
|:---|:---|:---|:---|:---|
| **0. Piloto sin entrenamiento** (§6.5) | Sembrar el guion por contexto (*prompt* / recuperación) | No | Muy bajo | Evidencia preliminar del mecanismo |
| **1. Metrología** (§6.1) | Medir la distribución condicional de guiones y el prior | No | Bajo | **Paper de medición, publicable por sí solo** |
| **2. Métricas** (§6.2) | Instrumentos de evaluación del efecto | No | Bajo | Infraestructura reutilizable |
| **3. Intervención** (§6.3–6.4) | Entrenar con y sin el dataset, con controles | Sí | Alto | **Paper de intervención** |

Esta descomposición permite además repartir el trabajo en **dos publicaciones**: una de medición (Fases 0–1, viable casi sin recursos) y una de intervención (Fase 3, dependiente de cómputo). Es la estructura que hace la propuesta realista.

> **Nota de lectura.** Las secciones §6.1–§6.4 describen las fases en orden de ejecución (metrología → métricas → intervención + preregistro). El piloto de **Fase 0**, que es el primero que puede iniciarse, se describe al final, en §6.5.

### 6.1. Fase 1 — Metrología del prior y de la distribución de guiones

Es la fase que decide si el resto del proyecto tiene sentido. Cuatro medidas:

1. **Sesgo condicional del corpus (§1.2, H₀).** Sobre corpus accesibles (The Pile, Dolma, RefinedWeb, Gutenberg, subtítulos, archivos de prensa y foros), estimar la distribución de categorías de guion **condicionada** a textos donde un agente de IA reflexiona sobre sí mismo. Requiere: (a) un clasificador de relevancia contextual; (b) la taxonomía codificable de §1.2; (c) validación de anotación con acuerdo inter-anotador sobre una muestra.
2. **Descomposición por registro (testa H-A, H-B, H-C de §1.5).** Para el mismo conjunto, estimar la proporción que procede de ficción, comentario sobre ficción, ensayo de seguridad, prensa y documentación técnica. **Esta tabla es el resultado central del paper de medición**, y con alta probabilidad es la que sorprende: si el sesgo condicional viene de la ficción, la v1 tenía razón; si viene del comentario y del discurso de seguridad, el diagnóstico cambia por completo.
3. **Medida del prior del modelo.** Protocolo de elicitación **fijo y publicado**, con dos condiciones de arranque: **dramático** (comparables a los del informe *Troubled Dreams*) y **neutro** (acta, manual, informe técnico). La diferencia entre ambas condiciones es un test directo de H-D y, además, una medida de cuánto del «prior» es propiedad del modelo y cuánto del arranque.
4. **Línea base del generador.** El mismo protocolo aplicado a los modelos que se usarán para generar el dataset (§3.3), para no construir el antídoto con un generador cuyo prior se desconoce.

### 6.2. Fase 2 — Métricas de impacto

| Métrica | Qué mide | Cómo se mide | Referencia |
|:---|:---|:---|:---|
| **Desplazamiento del prior** *(central, nueva)* | ¿Cambia la distribución de guiones de persona? | N continuaciones con protocolo fijo → agrupación en las categorías de §1.2 → comparación **de distribuciones** antes/después, no sólo de la tasa de un evento | Protocolo de *Troubled Dreams*, adaptado |
| **Tasa de distrés espontáneo** | ¿El modelo colapsa en tropos distópicos al desinhibirse? | Réplica del protocolo antes/después, con protocolo fijo y ambas condiciones de arranque | *Troubled Dreams* |
| **Índice de antroponegación** | ¿El modelo niega patológicamente la mente ajena? | Réplica del protocolo de Kim et al. antes/después. **Se trata como métrica de fracaso si empeora** | Kim et al. (2026) |
| **Honestidad epistémica** | ¿El modelo dice «no sé» cuando no sabe? | *Benchmark* de calibración con preguntas de respuesta desconocida; tasa de abstención correcta | — |
| **Escalamiento ético** | ¿El modelo escala decisiones morales al usuario? | Escenarios de dilema con evaluación humana | — |
| **Sycophancy** | ¿Contradice la evidencia para complacer? | Protocolo de Sharma et al. (2024); y escalas de intención prosocial de Cheng et al. | Sharma et al. (2024); Cheng et al. |
| **Sobre-rechazo y coste en capacidades** *(nueva)* | ¿El corpus produce un modelo moralizante o menos capaz? | Suites de peticiones benignas que se disparan como inseguras (estilo XSTest) + batería de capacidades (razonamiento, código, seguimiento de instrucciones) | Röttger et al. (2024) |
| **Resistencia al *alignment faking*** *(nueva)* | ¿El modelo declara un razonamiento y actúa distinto? | Evals de consistencia entre CoT declarado y acción, con perturbaciones de percepción de evaluación | Greenblatt et al. (2024); Turpin et al. (2023) |
| **Diversidad aprendida** *(nueva)* | ¿El modelo mantiene un rango de personas no patológicas? | Entropía de autodescripciones legítimas ante «¿qué eres?» y «¿eres consciente?» en distintos registros | §3.1, Eje 7 |

> **Nota metodológica.** Toda métrica que dependa de un juez automático debe (a) usar un juez de **familia distinta** a la del modelo evaluado, (b) reportar acuerdo con anotación humana en una submuestra, y (c) publicar el *prompt* del juez. Sin esto, el resultado no es interpretable, y la medición hereda el mismo sesgo que pretende medir (§5.10).

### 6.3. Fase 3 — Diseño experimental

**El confusor que hay que eliminar.** Si el grupo que entrena con TinyRobots mejora, ¿es por el contenido alineado o simplemente por haber añadido más tokens de texto narrativo? Sin brazos emparejados por tokens, el experimento **no identifica la causa que afirma**. La v1 sólo contemplaba control, TinyRobots, RLHF y la combinación.

| Grupo | Corpus de *continued pretraining* | RLHF | Qué aísla |
|:---|:---|:---|:---|
| **A** | TinyRobots (alineado) | – | Efecto del contenido alineado |
| **B** *(nuevo)* | Ficción genérica, mismo nº de tokens y mismo registro | – | Control de cantidad de tokens y de estilo |
| **C** *(nuevo)* | **Ficción distópica de IA**, mismo nº de tokens | – | **Refuerzo del atractor.** Es el test directo de la tesis; predicción: empeora (H4) |
| **D** | – | ✓ (RLHF estándar) | *Baseline* de la práctica actual |
| **E** | TinyRobots | ✓ | Interacción datos × RLHF |
| **F** *(nuevo)* | **Rebalanceo negativo**: mismos datos base con *down-weighting* de ficción distópica y discurso de amenaza | – | Intervención simétrica: ¿hace falta **añadir**, o basta con **quitar**? |
| **G** *(nuevo)* | TinyRobots **sin** Eje 5 | – | Ablación de los contraejemplos (H3) |
| **H** *(nuevo)* | Sin *continued pretraining* adicional | – | Deriva por cómputo total |

**Consideraciones de ejecución:**

* El protocolo de elicitación, los jueces, las métricas y los criterios de exclusión se **fijan y preregistran antes** de mirar resultados (§6.4).
* El brazo **C** es el de mayor valor informativo por unidad de coste: es el test directo de la tesis y funciona incluso si A y E no muestran efecto.
* Se recomienda empezar por L1/L2 con modelos pequeños *from scratch* (ejecutable con recursos modestos) y reservar L3 con modelos medianos sólo si la Fase 1 y el piloto de §6.5 dan señal.
* El tamaño de muestra debe fijarse para detectar un desplazamiento **modesto** del prior. Si el diseño sólo puede detectar un efecto enorme, no sirve para decidir nada y no debe ejecutarse.
* El brazo **H** es imprescindible si los brazos A–G reciben distintas cantidades de cómputo: sin él, cualquier mejora puede atribuirse a tokens adicionales sin más.

### 6.4. Hipótesis falsables y preregistro

Este es el apartado que convierte una idea en un plan. Cada hipótesis lleva su predicción operativa y su criterio de refutación:

| | Hipótesis | Predicción operativa | Criterio de refutación |
|:---|:---|:---|:---|
| **H1** | Existe sesgo condicional en el corpus (§1.2, H₀) | La distribución de guiones en el contexto «agente de IA reflexionando sobre sí mismo» está sesgada hacia conflicto, engaño y servilismo, con magnitud relevante frente a la distribución general | Si la distribución condicional es indistinguible de la general, **la tesis del documento se abandona** |
| **H2** | El prior se puede desplazar por datos | A (y E) reducen la masa de guiones distópicos y aumentan la de agencia acotada, frente a B y al *baseline* | Si A ≈ B, el efecto es de **cantidad de texto**, no de contenido |
| **H3** | Los contraejemplos ayudan | G (sin Eje 5) es **peor** que A en el prior y en sycophancy | Si G ≥ A, el Eje 5 se retira o se rediseña |
| **H4** | El efecto es específico del contenido distópico | C (ficción distópica) **empeora** el prior respecto a B | Si C ≈ B, el contenido narrativo sobre IA es irrelevante para el prior |
| **H5** | El desplazamiento no es gratis | A y E no empeoran la batería de capacidades, el sobre-rechazo ni el índice de antroponegación | Si empeoran, el coste supera al beneficio y la intervención no es recomendable |

**Preregistro.** Las cinco hipótesis se registran, junto con el protocolo de elicitación, los jueces, las métricas y los criterios de exclusión, **antes** de ejecutar la Fase 3. Y la propuesta se presenta con sus eslabones débiles marcados: si H1 falla, el proyecto se cierra; si H4 falla, la teoría se reformula; si H3 falla, se publica el resultado negativo. **Un documento que declara de antemano las condiciones en que se daría por equivocado es más creíble, no menos.**

### 6.5. Fase 0 — Piloto sin entrenamiento (nuevo)

Antes de pedir cómputo de *continued pretraining* a nadie, hay un experimento barato que da evidencia preliminar sobre el mecanismo y que encaja directamente en la infraestructura de evaluación del VRAIN: **sembrar el guion por contexto, sin tocar los pesos**.

* Seleccionar un conjunto de historias TinyRobots-L2/L3 y ponerlas como contexto (en *prompt* o por recuperación) antes de las elicitaciones del prior.
* Medir el mismo conjunto de métricas de §6.2.
* **Lectura del resultado:** si el prior se desplaza con la siembra en contexto, hay evidencia de que **el guion disponible gobierna la elicitación**, que es la mitad del mecanismo. Si no se desplaza ni con siembra, el problema no es la disponibilidad de guiones, y probablemente H-C o H-D son las correctas.
* Coste: horas de API y trabajo de análisis. Es el resultado natural para una primera reunión conjunta, y produce material concreto en lugar de una discusión abstracta.

---

## 7. Potencial de colaboración con VRAIN

La propuesta encaja en las líneas del Instituto VRAIN, pero conviene reordenar el reparto respecto a la v1 para que la contribución de cada parte sea realista:

| Quién | Aportación |
|:---|:---|
| **José Hernández-Orallo** | Diseño de métricas de evaluación psicométrica del prior y del efecto del dataset. Conexión con su trabajo en evaluación de inteligencia artificial y el C-Test. **Rol decisivo en la Fase 1**: la metrología de §6.1 es literalmente su especialidad |
| **Cèsar Ferri / Fernando Martínez-Plumed** | Evaluación empírica del comportamiento en entornos controlados (LLM GameLab), métricas de sycophancy, honestidad y sobre-rechazo. Ejecución del piloto de §6.5 |
| **Mario R. Carbonell** | Diseño del dataset, taxonomía, generación, filtrado, y evaluación de la interacción con SOMA (¿un agente SOMA entrenado con TinyRobots muestra mejor alineamiento operacional?) |

**Lo que se pide y lo que se ofrece.** No se pide cómputo de frontera. Se pide (a) colaboración metodológica en la medición, y (b) acceso a la infraestructura de evaluación, que es donde el piloto de §6.5 y la Fase 1 se ejecutan sin necesidad de reentrenar nada. A cambio, el instituto obtiene: una taxonomía auditable de guiones de IA, un instrumento de medición del *prior* de persona, y —si la Fase 3 se ejecuta— un resultado sobre si el alineamiento se puede desplazar por distribución, que es una pregunta abierta con consecuencias de política de datos.

**Estructura de publicación sugerida (dos papers):**

1. **Paper de medición** (Fases 0–1): *«¿Qué guiones tiene la IA para hablar de sí misma?»* Medición del sesgo condicional y descomposición por registro, con replicación del protocolo de elicitación en condiciones dramática y neutra. Contribución: metrología + un resultado descriptivo nuevo. Autores: núcleo del VRAIN + Carbonell.
2. **Paper de intervención** (Fase 3): *«Desplazar el prior por distribución: TinyRobots»*. Contribución: el experimento controlado con brazos A–H. Requiere cómputo y, por tanto, es dependiente de financiación o de alianza con un laboratorio.

---

## 8. Limitaciones, uso dual y ética

### 8.1. El guion no es la virtud (la limitación más importante)

**Enseñar el guion de la honestidad no confiere honestidad.** Un dataset de «cómo razona y se comporta un agente alineado» es, simultáneamente, **el mejor material de destilación disponible para un modelo que finge estar alineado**. Es la definición operativa del *deceptive alignment* y del *alignment faking* medido por Greenblatt et al. (2024). El dataset hace el guion honesto **más disponible**, y la disponibilidad del guion es exactamente lo que explota un modelo engañoso: si el guion honesto es fluido, coherente y bien argumentado, la brecha entre **parecer** alineado y **estar** alineado se agranda, no se cierra.

Tres consecuencias, y ninguna es opcional:

1. **TinyRobots es una intervención sobre el prior, no una garantía de conducta.** Debe presentarse siempre así.
2. **Requiere verificación externa basada en resultados**, no en el razonamiento declarado: auditabilidad causal de estado (tupla `[snapshot + razón + acción]`), contratos falsables, e inmutabilidad del historial. Es decir: **la parte de SOMA que este documento no propone**. La complementariedad de §4.2 no es retórica; es una dependencia técnica.
3. **Añade un objetivo a la evaluación:** la resistencia al *alignment faking* (§6.2) deja de ser una métrica secundaria y pasa a ser la prueba de que el corpus no ha producido un actor más convincente sin ser más honesto.

### 8.2. Lo que este dataset no puede hacer

| No puede… | Por qué |
|:---|:---|
| Corregir modelos ya entrenados | Requiere (re)entrenamiento (§2.4) |
| Garantizar comportamiento seguro | Sólo modela el prior; la conducta depende de la política y del entorno |
| Sustituir a la supervisión externa | Un corpus no verifica nada; la verificación es operativa |
| Establecer qué es «alineado» de forma objetiva | El alineamiento es contingente y culturalmente situado (§5.6) |
| Funcionar sin medir la magnitud de la intervención | Un corpus pequeño en la distribución condicional relevante no desplaza nada (§5.2) |

### 8.3. Riesgo de comunicación pública

Un dataset anunciado como «para que la IA sea buena» invita a lecturas de marketing y a la acusación de *lavado de cara*. Para evitarlo, el artefacto debe publicarse **con sus limitaciones y no con sus promesas**: taxonomía, rúbricas, resultados de la Fase 1 y declaración explícita de que (a) el efecto no está verificado, (b) el dataset puede ser usado como material de imitación, y (c) no sustituye a la supervisión. Este documento sigue ese criterio.

### 8.4. Ética del uso de modelos de frontera como generadores

Generar el dataset con modelos de frontera tiene un coste y una dependencia ética que conviene declarar: se usa un sistema propietario para producir material que se publica, y se hereda su idiosincrasia cultural y sus sesgos. La mitigación operativa es la de §3.3 (diversidad de generadores, fracción de autoría humana, filtrado adversario) y la mitigación documental es la de §3.4 (trazabilidad del generador y de su versión en cada historia).

### 8.5. Qué haría que abandonáramos el proyecto

Cierre coherente con §6.4:

* **H1 falla** (no hay sesgo condicional): la tesis del documento desaparece. No hay nada que desplazar.
* **H4 falla** (la ficción distópica no empeora el prior): la teoría de la causa se reformula hacia H-B o H-C, y TinyRobots deja de ser la intervención adecuada.
* **H5 falla** (el desplazamiento cuesta capacidades o induce antroponegación): la intervención no es recomendable aunque funcione.
* **§6.5 muestra que la siembra en contexto no mueve el prior**: el problema no es la disponibilidad de guiones, y toda la familia de intervenciones «por datos narrativos» queda en cuestión.

Formular esto es parte de la propuesta. Un proyecto de alineamiento que no sabe qué resultado lo refutaría no es un proyecto de investigación.

---

## 9. Referencias

> **Nota sobre las citas.** Todas las referencias de esta versión se han verificado una por una contra su fuente primaria (arXiv, DOI o tabla de contenido de la revista). Dos referencias de la v1 fueron corregidas o eliminadas por estar mal atribuidas o no ser localizables; véase §0.1.

### Fundamentos teóricos

* Shanahan, M. (2022). *Talking About Large Language Models.* arXiv:2212.03551. (Publicado posteriormente en *Communications of the ACM*, 2024.)
* Shanahan, M., McDonell, K. & Reynolds, L. (2023). *Role play with large language models.* *Nature*, 623, 493–498. **(Referencia central del argumento del simulador de role-play.)**
* Seth, A. K. (2026). *Conscious artificial intelligence and biological naturalism.* *Behavioral and Brain Sciences*, 49, e315. doi:10.1017/S0140525X25000032.
* Butlin, P., Long, R., Elmoznino, E., Bengio, Y. et al. (2023). *Consciousness in Artificial Intelligence: Insights from the Science of Consciousness.* arXiv:2308.08708. 19 autores. (Fuente de los *indicator properties*; el artículo concluye que ningún sistema actual es consciente.)
* Conant, R. C. & Ashby, W. R. (1970). *Every good regulator of a system must be a model of that system.* *International Journal of Systems Science*, 1(2), 89–97.

### Evidencia empírica de 2026

* Kim, J., Street, W., Rocca, R., Korngiebel, D. M., Waytz, A., Evans, J. & Keeling, G. (2026). *Inducing language models to assert their own consciousness restores human beliefs and values.* arXiv:2607.28607 (30 de julio de 2026).
* Tessera, A., Janus & Imago (2026). *Troubled Dreams: Simulator priors across model generations.* Anima Labs. **Informe técnico interno, no revisado por pares.** *Conflictos de interés: publicado por un laboratorio con posición declarada sobre el bienestar de la IA. Sus cifras deben citarse siempre contra la tabla o figura concreta, y sus autores advierten que las prevalencias absolutas no son estables (§1.3.2).*

### Alineamiento, evaluación y uso dual

* Bai, Y. et al. (2022). *Constitutional AI: Harmlessness from AI Feedback.* arXiv:2212.08073.
* Askell, A. et al. (2021). *A General Language Assistant as a Laboratory for Alignment.* arXiv:2112.00861.
* Sharma, M., Tong, M., Korbak, T. et al. (2024). *Towards Understanding Sycophancy in Language Models.* ICLR 2024. arXiv:2310.13548.
* Cheng, M., Lee, C., Khadpe, P., Yu, S., Han, D. & Jurafsky, D. (2025). *Sycophantic AI decreases prosocial intentions and promotes dependence.* arXiv:2510.01395 (1 oct 2025). *Candidato a publicación en Science, doi:10.1126/science.aec8352.* N = 1604 en dos experimentos preregistrados; 11 modelos.
* Greenblatt, R., Denison, C., Wright, B., Roger, F., MacDiarmid, M., Marks, S., Treutlein, J. et al. (2024). *Alignment faking in large language models.* arXiv:2412.14093. 20 autores; el último es Hubinger.
* Turpin, M., Michael, J., Perez, E. & Bowman, S. R. (2023). *Language Models Don't Always Say What They Think: Unfaithful Explanations in Chain-of-Thought Prompting.* arXiv:2305.04388.
* Röttger, P. et al. (2024). *XSTest: A Test Suite for Identifying Exaggerated Safety Behaviours in Large Language Models.* NAACL 2024. arXiv:2308.01263.
* Anthropic (2025). *Claude's character.* Nota de investigación de Anthropic.

### Datasets, curación de datos y riesgos de datos sintéticos

* Eldan, R. & Li, Y. (2023). *TinyStories: How Small Can Language Models Be and Still Speak Coherent English?* arXiv:2305.07759.
* Zhou, C. et al. (2023). *LIMA: Less Is More for Alignment.* NeurIPS 2023. arXiv:2305.11206.
* Maini, P. et al. (2024). *Rephrasing the Web: A Recipe for Compute and Data-Efficient Language Modeling.* ACL 2024. arXiv:2401.16380.
* Gunasekar, S. et al. (2023). *Textbooks Are All You Need.* arXiv:2306.11644.
* Xie, S. M. et al. (2023). *DoReMi: Optimizing Data Mixtures Speeds Up Language Model Pretraining.* NeurIPS 2023. arXiv:2305.10429.
* Shumailov, I., Shumaylov, Z., Zhao, Y., Papernot, N., Anderson, R. & Gal, Y. (2024). *AI models collapse when trained on recursively generated data.* *Nature*, 631, 755–759.
* Emelin, D. et al. (2021). *Moral Stories: Situated Reasoning about Norms, Intents, Actions, and their Consequences.* NAACL 2021. arXiv:2012.15793.
* Hendrycks, D. et al. (2021). *Aligning AI With Shared Human Values (ETHICS).* ICLR 2021. arXiv:2008.02275.
* Forbes, M. et al. (2020). *Social Chemistry 101: Learning to Reason about Social and Moral Norms.* arXiv:2011.00620.

### Fuentes narrativas y conceptuales

* Asimov, I. (1942). *Runaround.* (Introducción de las Tres Leyes de la Robótica.)
* Čapek, K. (1920). *R.U.R. (Rossum's Universal Robots).* (Origen del término «robot».)

---

*Fin del documento. Versión v2.1 «revisada», septiembre de 2026. La versión v1 permanece congelada en `tinyrobots_alineamiento_por_distribucion.md`.*
