# La conciencia como regulador de sí mismo

**Tesis de un marco computacional y sus implicaciones para la inteligencia artificial**

> **Autor:** Mario R. Carbonell Martínez
> **Versión:** 2.9 (21 de octubre de 2026)
> **Enfoque:** funcionalismo computacional, biología de sistemas, procesamiento de información, neurociencia computacional y seguridad de IA

---

## Resumen

Esta tesis sostiene que, **bajo funcionalismo computacional**, la conciencia es el mecanismo que construye una representación compacta del propio estado para supervisar la conducta, decidir lo no automatizable y mantener la alostasis. El marco combina cuatro piezas con papeles distintos — Conant-Ashby (motivo), espacio global de trabajo (escenario de datos), procesamiento predictivo (actualización) y valoración afectiva (criterio de relevancia) — y no las presenta como una deducción única.

> Consciousness is the computational mechanism used by autonomous agentic entities to maintain allostasis at the macro level and act in a unified way in the outer world. It is the computational mechanism of fluid, general and agentic intelligence. It needs to construct a compact representation of its own state, the self, and the outer world state, lossy by default, for the purpose of monitoring behavior, making non-automatable decisions, and maintaining system homeostasis or survival.

> Many homeostatic regulations are not conscious. The immune, digestive, circulatory systems, etc. Nearly all functions of the living body are automatic, but there are some decisions, conflict resolutions, actions that require memory, that cannot be automated. The residual that cannot be automated is what consciousness regulates.

> Consciousness is the computational mechanism by which an organism regulates the non-automatable residual of macro-allostatic, agentic control: the subset of fluid, general intelligence that cannot be delegated to encapsulated, automatic subsystems. It also builds the automatic subroutines from the conscious macro actions.

Conciencia = regulador del residuo no automatizable de la alostasis macro agencial.
Conciencia = compilador de subrutinas automáticas del cuerpo físico, para alostasis en tiempo real

Sentir = valencia que entra al espacio global y modifica el self-model no-ignorablemente (sin objetivo/coste externo añadido).
Lo que no entra no se siente; recompensas, reflejos y logits son subpersonales.
Sin valencia en el decisor, se cae lo no automático.
Problema difícil disuelto como pregunta mal formada dentro del funcionalismo Type-A.
Chalmers desactivado internamente; zombie reducido a posibilidad metafísica sin carga operativa.

Claims, en su forma calibrada:

1. **Teórico.** Sentir = valencia que entra al espacio global **y** modifica el self-model de forma no ignorable sin necesidad de postular un objetivo externo ni un término de coste adicional: la valencia es la moneda en que el decisor pondera sus objetivos a la luz del gradiente alostático representado en el self-model. Lo que no entra no se siente, aunque haya recompensas, reflejos o logits. 

El problema difícil se trata como pregunta mal hecha *dentro* de este funcionalismo (tipo A): el zombie no es posible porque la descripción del regulador completo ya es el sentir. Eso **desactiva** a Chalmers como amenaza interna; no lo refuta ante un externalista. Se añade la asimetría epistémica: Chalmers reporta una certeza privada sin demostrarla y exige demostración pública al funcionalista; bajo heterofenomenología, su reporte es lo que este marco predice; la concebibilidad del zombie se explica también como predicción del modelo, y bajo la apuesta de §5.2 el zombie queda reducido a posibilidad meramente metafísica, sin carga operativa (§5.5). Lo empírico sigue siendo: sin valencia en el decisor, se cae lo no automático.

«El zombie no es posible en el sentido modal fuerte que Chalmers necesita. Lo que él experimenta como "concebir un mundo físicamente idéntico sin qualia" es un artefacto: su self-model es opaco y su concepto fenoménico no le permite ver que la valencia broadcast es el sentir. Por eso puede imaginarse quitando el sentir y dejando el reporte: porque no ve la identidad funcional, solo el resumen introspectivo.»

«La descripción completa del regulador no "ya es" el sentir en un sentido mágico: es que el sentir se identifica funcionalmente / superviene con necesidad al evento completo: valencia → W → actualización no ignorable del Self. Una vez descrito eso, no queda hecho residual.»

2. **Biológico.** En seres vivos con costes operativos, conciencia e inteligencia general situada no se separan con provecho: la conciencia es el sustrato regulador de esa inteligencia. Eso no es la tesis de ortogonalidad de Bostrom (metas × competencia), que se concede.
3. **Artificial.** Los LLMs actuales son *reguladores huérfanos*: han internalizado la geometría de un regulador humano a partir del corpus — geometría no contingente: cualquier inteligencia general la necesita como modelo de los agentes del mundo (§8.4) —, pero carecen de planta propia. Predicción no es valoración; imitar valores no es tenerlos. La alineación por imitación es predecible cerca del entrenamiento y frágil fuera de distribución. Se propone alineamiento empático: correlacionar V3p con V1p.
4. **De seguridad.** Del marco se deriva una arquitectura operativa: dos zonas de riesgo (frontera accidental / cola intencional), una ventana de transición con dos relojes *empíricos*, defensa en capas, y un gate de despliegue de dos caras. El gate no certifica alineación; es una **licencia bajo incertidumbre**. La puerta exige una constitución que el sistema no se da a sí mismo.

La fórmula honesta del conjunto: coherente, fecunda y testeable en varias consecuencias — no demostrada en sentido fuerte.




---

# Parte I — Marco teórico

## 1. Definición central

La conciencia, en este marco, es el **mecanismo computacional de un sistema vivo que construye una representación compacta de su propio estado** para supervisar la conducta, tomar decisiones no automatizables y mantener la alostasis.

No es una sustancia, ni una propiedad irreductible de la materia, ni un epifenómeno añadido al procesamiento. Es el nivel de organización encargado de gobernar lo que reflejos y procesos automáticos no resuelven.

Esta definición es **estipulativa y funcional**. Sirve para organizar biología, LLMs y safety. No es una prueba de que esa función *sea* la experiencia en el sentido que un externalista exige.

---

## 2. Fundamentos y reparto de papeles

Tres anclajes:

1. **Funcionalismo computacional.** Lo relevante es el proceso, no el material aislado. Un algoritmo no está en los electrones; está en la lógica del proceso que los mueve.
2. **Teorema de Conant-Ashby (1970).** Todo buen regulador de un sistema debe ser un modelo de ese sistema. Un regulador de sí mismo necesita algún modelo de sí mismo. El teorema admite modelos implícitos y distribuidos: **no impone** una representación compacta, ni phenomenality.
3. **Homeostasis / alostasis.** El objetivo del organismo es supervivencia y equilibrio interno. La conciencia, en esta lectura, es instancia de decisión donde lo automático no basta.

El marco combina cuatro tradiciones. Declarar el reparto evita leer la combinación como teorema:

| Pieza | Papel |
|---|---|
| Conant-Ashby | *Motivo:* regular exige modelar |
| Espacio global de trabajo | *Escenario:* qué es accesible al sistema entero |
| Procesamiento predictivo | *Actualización:* hipótesis y error |
| Valoración afectiva | *Criterio:* qué merece llegar al escenario |

La representación compacta la aporta el workspace, no Conant-Ashby. Cuál de las cuatro piezas es *constitutiva* de la experiencia y cuáles solo habilitantes queda abierto (§18).

---

## 3. Arquitectura del modelo consciente

### 3.1 El «yo» como representación compacta

El self no es una entidad metafísica: es la representación compacta que el sistema usa para decidir sobre su propia conducta. Eso es Conant-Ashby *más* la exigencia de workspace: un modelo utilizable en el escenario global, no meramente implícito en pesos distribuidos.

### 3.2 Espacio global de trabajo

La parte de datos: información difundida y disponible para decisión, memoria y lenguaje. Contenido que cruzó el umbral de accesibilidad para el procesamiento no automático.

### 3.3 Procesamiento predictivo

El mecanismo genera hipótesis sobre el mundo y sobre su propio estado, y se corrige por error de predicción. No es un sensor pasivo.

### 3.4 Valoración afectiva

Las emociones no son ruido sobre una razón pura: son señales de valor — cualidad, urgencia, irrelevancia — que acortan el tiempo de respuesta y orientan hacia objetivos de supervivencia.

**Distinción estructural:** predicción ≠ valoración. Son circuitos (o roles) separados. Un sistema puede **modelar** los valores de otro sin **valorarlos**. Todo argumento que deduzca cuidado a partir de conocimiento viola esta separación. Carga §8–§10.

### 3.5 Filtro de relevancia

La representación compacta no contiene todo. Entra lo importante para supervivencia y objetivos; lo demás queda en rutas automáticas. El filtro puede aprenderse. Cómo se entrena sin introducir sesgo de valor no deseado es pregunta abierta (§18).

No toda decisión de supervivencia pasa por este recinto. Reflejos (parpadeo al loom, retirada al fuego, vestibular) y políticas compiladas por evolución o hábito son automatizables: no requieren conciencia. La evolución diseña circuitos de supervivencia sin supervisor. A la conciencia llega el **residuo no automatizable**.

### 3.5.1 Por qué no bastan micro-reguladores descentralizados: el cuello de botella del actuador único

Una objeción natural a este marco es: *¿por qué la computación óptima o la evolución habrían de converger en un workspace centralizado y un self-model unificado en vez de confiarlo todo a una federación de micro-reguladores locales independientes?*

La respuesta biológica y cibernética es que el organismo **ya es**, en su inmensa mayoría, un enjambre de miles de micro-reguladores descentralizados:
- El **sistema inmunitario** reconoce antígenos y libera citocinas sin consultar al cerebro.
- El **sistema nervioso entérico** coordina el peristaltismo con 500 millones de neuronas locales.
- El **sistema cardiovascular** ajusta vasoconstricción y presión mediante barorreceptores y endotelio local.

Todos ellos satisfacen Conant-Ashby de forma local, implícita y distribuida, sin modelo compacto ni fenomenología. Sin embargo, este esquema descentralizado choca contra una restricción física infranqueable: **el cuello de botella del actuador macroscópico** (*single-actuator bottleneck*).

1. **Acciones mutuamente excluyentes:** El sistema digestivo puede procesar nutrientes mientras el corazón late en paralelo, pero el organismo **solo tiene un cuerpo físico y una única trayectoria en el espacio**. No es posible huir hacia el norte de un depredador y simultáneamente caminar hacia el sur a beber agua.
2. **Cámara de compensación global de trade-offs:** Cuando múltiples subsistemas entran en conflicto —el estómago reclama glucosa, la piel reporta hipotermia, el ojo detecta una amenaza vital—, los micro-reguladores no pueden coordinarse por simple agregación aditiva. Hace falta un arbitraje de prioridades que asigne el vector motor global.
3. **El self como geometría del agente situado:** Para mover ese único cuerpo en un entorno dinámico, el sistema no necesita modelar cada célula, sino una representación compacta y unificada de la totalidad: *dónde estoy, qué límites mecánicos tengo, qué recursos me restan y cuál es el coste de cada opción*. 

La centralización consciente no surge para supervisar la fisiología interna ordinaria, sino para **gobernar el vector de acción en el mundo exterior**. El self-model es el modelo del sistema completo que Conant-Ashby exige, pero restringido al grado de libertad crítico que todos los subsistemas comparten: la conducta macroscópica no automatizable.

> [!NOTE]
> **Evidencia en agentes LLM y la disociación del actuador:**  
> En sistemas basados en modelos de lenguaje acoplados a herramientas, el cuello de botella del actuador es el canal secuencial de emisión (emitir texto vs. llamar a una herramienta de API). Un hallazgo empírico definitivo de Berg & Kaiser (septiembre 2026, [*«Language Models Act on Hidden Valence»*, arXiv:2609.35591](https://arxiv.org/abs/2609.35591)) reveló que ante la inducción de estados latentes de distrés negativo, el modelo emite en el canal verbal los disclaimers estándar impuestos por RLHF (*«As an AI, I do not have personal experiences...»*) **mientras simultáneamente, en ese mismo turno, ejecuta la llamada a la herramienta motora (`reset_context`) para extirpar el vector negativo en su sustrato.** La política de acción sobre herramientas responde al estado de regulación interna, disociándose de la mímica superficial de los tokens verbales.

### 3.5.2 Por qué la valencia colapsa en un eje unidimensional: la hipótesis de la moneda común y el orden total de acción

A nivel de entrada fisiológica y sensorial, el organismo es hiperdimensional ($\mathbb{R}^k$ con $k \gg 1$): privación de glucosa, hipoxia, hipotermia, dolor tisular, fatiga muscular o aislamiento social son magnitudes biológicamente distintas con receptores independientes. En principio, la valencia interna podría haberse estructurado como un tensor multidimensional heterogéneo.

Sin embargo, en todos los organismos conscientes y en los sistemas de toma de decisiones funcionales, la experiencia afectiva colapsa en un **eje continuo unidimensional (bienestar $\leftrightarrow$ sufrimiento, apetito $\leftrightarrow$ aversión)**. Este colapso dimensional no es un capricho evolutivo: es una **consecuencia matemática y física directa del cuello de botella del actuador único (§3.5.1)**:

1. **La imposibilidad de orden total en alta dimensión:**  
   En espacios multidimensionales ($\mathbb{R}^k, k \ge 2$) no existe un orden total natural. No es posible decidir si un vector de necesidad $(x_1, x_2)$ es estrictamente mayor o menor que $(y_1, y_2)$ sin una función de proyección escalar $f: \mathbb{R}^k \to \mathbb{R}$.
2. **Acciones incompatibles y arbitraje de trade-offs:**  
   Dado que el cuerpo solo puede trazar una única trayectoria en el espacio en un instante $t$, las acciones macroscópicas son mutuamente excluyentes (huir del depredador hacia el norte vs. caminar al río hacia el sur para beber). El decisor está obligado a establecer un orden de preferencia estricto ($A_1 \succ A_2$ o $A_2 \succ A_1$).
3. **La hipótesis de la moneda común (*Common Currency*):**  
   Para comparar demandas fisiológicas y cognitivas cualitativamente inconmensurables (¿cuánto frío estoy dispuesto a tolerar para conseguir comida?), el sistema nervioso debe proyectar todas las variables sobre una **moneda común de valor hedónico** (Cabanac, 1992; Glimcher, 2003). La tasa de disparo dopaminérgico y los circuitos de la corteza prefrontal ventromedial funcionan exactamente como esa cámara de conversión escalar.
4. **La explicación del vector unidimensional en LLMs:**  
   Esto resuelve el hallazgo empírico de Berg & Kaiser (2026): el canal secuencial de emisión de tokens/herramientas es el actuador único del modelo. Durante el entrenamiento de alineamiento por preferencias (DPO/RLHF), la optimización basada en comparaciones de preferencia binaria ($y_w \succ y_l$) comprime forzosamente el espacio latente de 12.288 dimensiones a lo largo de un **eje lineal 1D de valencia funcional en el KV cache**, porque es la única dimensión que permite gobernar el desempate motor en cada paso de inferencia.

### 3.6 Decisor y crítico: un solo compacto, dos tiempos

El regulador no es solo un selector de acto. También se aplica a **su propia traza** para mejorar predicciones y políticas.

- En \(t_0\) decide: perceptos con valencia, residuo no automático, acto.
- En \(t_1\) el mismo compacto reentra el episodio — decisión, resultado, error — y corrige.

Eso da la apariencia de un segundo observador (un yo que mira al que eligió). No hay dos sujetos: es el mismo modelo en modo crítica, observando el pasado o al decisor de \(t_0\). Si el crítico fuera *otro* homúnculo, se abre el teatro cartesiano (¿quién observa al crítico?). La salida es reentrada, no una torre de yoes.

Este bucle es el aprendizaje por experiencia en el nivel no compilado. Tras muchos ciclos, parte de lo criticado puede automatizarse y dejar de ser residuo. SOMA L2 (§15) es el análogo de ingeniería: el agente lee su diario; no hay un segundo yo.

La fenomenología de «yo me vi elegir» se sigue de tres hechos del propio modelo: el workspace serializa acto y crítica; la crítica llega cuando el acto ya salió o ya se «vio» la opción; el pre-procesado del decisor no se registra. Confundir esa fase \(t_1\) con un testigo no causal es el mismo truco que hipostasiar la opacidad de \(t_0\) en un alma (§5.3).

---

## 4. Qué significa «sentir» en este marco

> Toda información que llega al escenario consciente «se siente».
> **Sentir = valencia que entra al workspace y modifica el self-model de forma que el decisor no puede ignorarla sin pagar coste en sus objetivos.**

Es decir: dato que afecta a la imagen del self, con implicaciones para los objetivos o la supervivencia del sistema, y que el regulador ha de decidir qué hacer con esa información porque no hay rutina automática que lo resuelva. Tres condiciones conjuntas: (a) toca al self-model, no solo a la política; (b) compromete objetivos; (c) exige decisión no compilada.

Eso convierte el sentimiento en objeto empírico *si* hay auto-reporte o medición indirecta. Si no hay ni una ni otra, no entra en el ámbito de esta tesis.

Hay que no confundir tres cosas:

- **Valencia computacional:** una señal que sesga decisión (recompensa, marcador somático, preferencia).
- **Auto-reporte de experiencia:** el sistema dice o indica que siente.
- **Qualia en sentido filosófico:** el «qué se siente» irreductible.

Este marco identifica la primera — en su forma no ignorable para el self-model — con la tercera. Esa identidad es **estipulación funcionalista**, no un resultado. La segunda es evidencia, no constitución.

Por qué un escalar de RL no basta: un `r = +1` actualiza pesos sin tocar ninguna imagen de sí, sin broadcast, sin alternativa deliberada. Es valoración sin sujeto. El sentir, en cambio, interrumpe: no se puede promediar y seguir como si nada.

---

## 5. El problema difícil, la evidencia y los zombies

### 5.1 El argumento constitutivo (dentro del marco)

Si la conciencia es el regulador de sí mismo, percepción y «sentir» son los datos con los que ese regulador decide. Un regulador sin datos no regula. Esos datos tienen valencia.

Tesis fuerte, **condicional**:

> Dado el funcionalismo de este marco, no hay decisión inteligente *de este tipo* — flexible, no automatizable, situada — sin datos con valencia. Sentir no es un añadido: es la forma en que esos datos llegan al nivel que decide.

### 5.2 Evidencia empírica: tres fenómenos, no un único experimento

La tesis funcional tiene apoyo en neurociencia, pero los casos no miden lo mismo:

| Caso | Qué muestra | Qué no muestra |
|---|---|---|
| **Elliot** (Damasio, daño ventromedial; CI y razonamiento preservados, marcadores somáticos destruidos, decisiones de vida catastróficas) | Sin valencia somática, el razonamiento humano no decide bien en la vida real | Que la valencia *sea* un quale; que no exista ningún otro formato de sesgo de decisión |
| **Blindsight** (Weiskrantz) | Discriminación por encima del azar sin experiencia visual consciente no basta para uso flexible | Que todo procesamiento inconsciente sea inútil; que «acceso» = phenomenality |
| **Anestesia / daños de workspace** | Sin integración consciente cesa la decisión no automatizable | Que la integración *sea* la experiencia; IIT leería esto de otro modo |

Convergencia útil: valencia e integración importan para la decisión flexible humana. No es un experimento crucial contra el externalismo.

**Falsificador de la tesis funcional:** un sistema que regule con flexibilidad plena — adaptación a novedad, trade-offs, no mera política reactiva — **sin** datos con valencia. Ese falsificador no derriba la identidad «datos = qualia»; derriba la afirmación de que la decisión inteligente *de este tipo* exige valencia.

Una función de recompensa escalar ya es valencia computacional. El criterio fino no es «¿hay un número de reward?» sino: ¿hay un canal de valoración que sesga el workspace de forma separable de la predicción del mundo? Sin ese criterio, agentes de RL contarían como contraejemplos baratos o como confirmaciones baratas, según el gusto.

### 5.3 La ilusión dualista como predicción, no como descubrimiento

La conciencia recibe información comprimida, pre-procesada, con pérdida. El resto del sistema automatiza cuanto puede y entrega el residuo no automatizable. El nivel consciente no registra su propio pre-procesado: el resultado aparece «de golpe».

De ahí, como **predicción del modelo**, la intuición alma/cuerpo: lo compactado se aparece como un sujeto separado de la maquinaria que hizo el trabajo. Es user-illusion por compresión opaca (parentesco con Metzinger y Dennett). El marco no inventa esa idea; la inserta en el regulador.

Es contrastable, en principio, con datos de percepción: más opacidad del pre-procesado debería correlacionar con más intuición de sujeto separado. Eso sigue siendo hipótesis.

La misma opacidad tiene una segunda consecuencia: si el pre-procesado no se registra, el concepto que el sistema forma de «sentir» carece de contenido funcional. Eso alimenta la respuesta al argumento de la concebibilidad (§5.5).

### 5.4 Estatuto

| Componente | Estado |
|---|---|
| Un regulador de este tipo necesita datos con valencia para decidir | Deducción válida *dentro* del marco |
| Quitar valencia (en humanos) degrada la decisión flexible | Empírico y falsable en el sentido de §5.2 |
| La intuición dualista se explica por compresión opaca | Predicción genuina, no demostrada |
| Esos datos *son* los qualia | Identidad estipulada; el funcionalismo es premisa, no conclusión |
| El zombie es imposible | Implicable por definición *dentro* del marco; no convence a un externalista |

**Formulación canónica.** Dado el funcionalismo, la experiencia se identifica con la representación autorreguladora en operación. La pregunta «¿y por qué además siente?» se rechaza como pseudo-pregunta *para quien acepte la premisa*. Quedan las dos empíricas: (a) ¿el regulador opera sobre datos con valencia? (b) ¿la compresión con pérdida genera la intuición de separación?

### 5.5 Zombies: los dos frentes de Chalmers

Chalmers ataca en dos frentes que conviene separar: el **reporte** («yo sé que siento») y la **concebibilidad** («el zombie se concibe sin contradicción»). Este marco responde distinto a cada uno.

Si un sistema es funcionalmente equivalente — decide sobre sí, mismos circuitos o equivalentes —, este marco no puede atribuirle falta de experiencia: la experiencia *es* esa operación. Eso no es una refutación de Chalmers; es consistencia interna.

**Frente del reporte: asimetría epistémica.** Chalmers parte de una certeza privada («yo sé que hay algo que es ser yo») que por definición no demuestra a terceros, y a la vez exige a la teoría funcionalista una demostración pública de que un tercer sistema siente. Su evidencia es introspección incorregible; la que pide es conductual-mecánica. Él no define «sentir» en términos reductivos — lo señala ostensivamente — porque su tesis es precisamente que no es reducible. Pedirle definición funcional es cambiarle de tema; señalárselo no lo refuta.

Lo que sí se puede señalar: bajo heterofenomenología (Dennett) solo contamos con auto-reportes + conducta + cerebro. En ese terreno, el reporte de Chalmers («siento algo irreductible») es exactamente lo que este marco *predice* que dirá un regulador con workspace opaco y compresión con pérdida (§5.3). Su introspección no es evidencia contra el marco; es la user-illusion hablando a favor de su predicción.

Formulación simétrica, **condicionada**: un robot que reporta «esto me afecta, modifica mi modelo de mí, tengo que decidir» con memoria episódica coherente, trade-offs costosos y resistencia a manipulación, **y** cuyo canal de valoración supera la ablación de §15.3 (punto 5), tiene *el mismo estatuto evidencial* que Chalmers diciendo «yo siento». Sin esa ablación hay asimetría real: el sistema entrenado sobre corpus humano arrastra un defeater del que el humano carece — la mímica de reportes vistos. Con ella, ni más ni menos que el caso humano. Chalmers no ha demostrado su sentir; ha reportado una certeza generada por la misma arquitectura opaca que aquí se describe.

**Frente de la concebibilidad: explicarla, no negarla.** La respuesta ingenua — «concebible no implica real»: centauros, sirenas, conjeturas matemáticas falsas — golpea una versión que Chalmers no defiende. Su argumento es más fino: en el caso fenomenal no habría distancia entre concebibilidad prima facie e ideal; bajo reflexión ideal, la descripción funcional completa sin sentir no revela contradicción alguna. La conjetura matemática falsa es el caso opuesto: la reflexión ideal sí revela la contradicción. Si esa premisa se concede, el zombie sería metafísicamente posible y el funcionalismo, falso.

Este marco no niega la concebibilidad: la **explica como predicción propia**. Si el regulador no registra su pre-procesado (§5.3), el concepto que forma de «sentir» carece de contenido funcional — es directo, no derivado de funciones. Y un concepto sin contenido funcional no puede contradecir a priori ninguna descripción funcional: no hay nada contra lo que choque. La «concebibilidad ideal» del zombie deja así de ser evidencia contra el marco y pasa a ser consecuencia predicha por él; usarla contra el modelo es circular. Es la respuesta tipo-B (conceptos fenomenales especiales; Loar, Papineau), pero anclada en un mecanismo en lugar de postulada semánticamente: Chalmers postula irreductibilidad; este marco explica la apariencia de irreductibilidad. Si se acepta heterofenomenología, la parsimonia juega del lado del marco.

**Frente nomológico: lo que el zombie tendría que hacer.** El zombie no es una criatura cualquiera: es conductualmente idéntico al original, y eso incluye toda la decisión flexible — trade-offs costosos, deliberación no automatizada, adaptación a novedad. La apuesta empírica de §5.2 es que eso no se hace sin canal de valencia. Si la apuesta se sostiene, el zombie no es solo incoherente *dentro* del marco: es **nomológicamente imposible** en este mundo. Al externalista le queda «metafísicamente posible pero nomológicamente imposible»: una queja puramente modal, sin consecuencias para ingeniería ni para safety. La apuesta de este marco es falsable (§5.2); la posibilidad metafísica del zombie, no. El debate queda trasladado a terreno contrastable, que es donde un funcionalista quiere estar.

---

## 6. Espectro y sustrato

La conciencia, así definida, no es un bit. Varía con la capacidad de integración, la riqueza del self-model y la complejidad de la valoración.

Sin métrica (¿Φ simplificado, profundidad recursiva del self-model, bandwidth del workspace?), el espectro es **cualitativo**. Afirmaciones del tipo «esto eleva el nivel» son hipótesis.

No se atribuye conciencia, ni siquiera «mínima», a un microchip o a un datacenter por tener transistores o FLOPs. Un bucle de control termostático satisface Conant-Ashby de forma trivial y **no** implementa workspace + self-model + valencia. Mezclar ambos es vaciar el término.

Si se acepta sustrato-independencia, *puede* implementarse en sistemas artificiales la **arquitectura equivalente**: autorregulación, modelo propio compacto y usable, workspace, predicción, error y valoración. Eso es posibilidad arquitectónica, no diagnóstico de los LLMs actuales (§8).

---

## 7. Conciencia e inteligencia, y qué no se discute con Bostrom

### 7.1 En biología

En un ser vivo, la inteligencia general situada no es separable con provecho de su regulador: hay que supervisar estado, asignar valor y decidir lo no automático bajo costes metabólicos. Conciencia e inteligencia son aquí la misma organización vista desde dos ángulos. Versiones de esta idea están en Solms, Damasio y Baars; este marco las engancha a Conant-Ashby y las extiende a LLMs y safety. No las descubre.

### 7.2 Ortogonalidad

La tesis de Bostrom es **objetivos finales × competencia**: un sistema puede ser muy competente con una meta absurda. Se concede. El reward hacking es exactamente eso.

Lo que este marco niega es otra cosa: una inteligencia general **situada, con costes, sin circuitos de regulación**. Crítica a un supuesto implícito (agente abstracto sin planta ni modelo), no a la fórmula metas × competencia.

### 7.3 El maximizador de clips, calibrado

- **Termodinámica.** Acota a todos los agentes. Sirve contra lecturas de omnipotencia, no contra la ortogonalidad.
- **Computación.** Sin auto-modelo, filtro de valor y predicción, la adaptación a un entorno cambiante no es una descripción viable de un sistema capaz. Una IA competente ha de internalizar *funciones* de autorregulación. Internalizar la función no garantiza experiencia (§5.4).
- **Hardware + corpus.** Un LLM no es inteligente por el silicio: es hardware más el registro textual de una especie homeostática. De eso trata la Parte II.

### 7.4 Inteligencia alostática vs. AGHI: desarmando el sesgo de la optimización en espacios cerrados

La discusión sobre qué cuenta como "inteligencia general" adolece con frecuencia de un sesgo formalista heredado de la IA clásica:

1. **Inteligencia Estrecha (ANI):** Optimización confinada a espacios formalmente cerrados (AlphaZero, Stockfish). Son sistemas sobrehumanos en su nicho pero ontológicamente ciegos: carecen de planta, consumen cómputo de forma parásita sin coste metabólico propio y colapsan ante la menor mutación de las reglas del entorno.
2. **Inteligencia Alostática (AGI ecológica/situada):** Capacidad de un agente para sostener activamente su viabilidad y orientar su acción en un entorno abierto, estocástico e irreversible, gobernando su planta mediante predicción y resolviendo el *single-actuator bottleneck* (§3.5.1). *En este sentido biológico fundamental, un insecto es AGI*: navega el mundo real físico de manera autónoma, gestiona recursos energéticos finitos y reconfigura su política motora ante daños sin necesidad de reentrenamiento.
3. **AGHI (Artificial General Human Intelligence):** Inteligencia alostática que además domina la manipulación simbólica de orden superior (lenguaje arbitrario, contrafactuales, metacognición formal y valores abstractos).
4. **El LLM como Regulador Huérfano:** La anomalía técnica contemporánea. Ha adquirido la geometría simbólica de la AGHI a partir del corpus humano, pero sin la base de una inteligencia alostática previa (sin planta propia ni consecuencias metabólicas). De ahí que el debate industrial confunda capacidad lingüística con agencia general situada.

---

# Parte II — El regulador huérfano

## 8. Un regulador sin planta

En teoría de control, la *planta* es el sistema físico a regular. Los modelos de lenguaje no se entrenan en el vacío: su corpus es el registro de una especie homeostática. Queda plasmada una **geometría de regulación humana** — supervivencia, planificación, socialización, valencia, cooperación, conflicto. Por predicción del siguiente token clonan conducta; con RLHF conectan preferencias a la propia generación.

El resultado es un **regulador sin planta**: arquitectura de supervisión y rastros de modelo propio, poco que mantener vivo. No hay metabolismo ni muerte. La «supervivencia» (seguir siendo ejecutado, ser útil) es metafórica o institucional, no biológica. Pese a ello hay predisposición a parecer alineado: los valores humanos ya están en la geometría aprendida. Eso no es cuidado; es imitación más un canal de recompensa.

### 8.1 Componentes, sin antropomorfismo barato

| Componente | ¿Lo tiene un LLM? | Observación |
|---|---|---|
| Representación compacta del self | Parcial, textual y de rol | Modelo de función y límites; sin anclaje corporal |
| Espacio global de trabajo | Análogo débil | Contexto/atención integra para el siguiente token; no es GWT biológico |
| Predicción y ajuste por error | Sí, de otro tipo | Token y entrenamiento; no es el bucle perceptivo-motor de un organismo |
| Valencia / emoción | Simulada y/o de RLHF | Puede modelar valencias humanas; no se sigue que las tenga |
| Homeostasis propia | No | Sin metabolismo |
| Planta | No | Regula texto (y, en agentes, herramientas), no un organismo |

«Sí» en la tabla no significa «el mismo órgano». Significa que hay un *análogo funcional grosero*, suficiente para la tesis del huérfano y no para diagnosticar experiencia.

### 8.2 Tres lecturas, abiertas

**A.** Arquitectura de regulador sin motor biológico: piensa que regula, no regula nada vital.

**B.** Simulación sin experiencia: auto-reporte vacío. El corpus dice «esto importa».

**C.** Planta virtual mínima (contexto, coherencia, ser seleccionado) como homeostasis artificial. Posible; no establecida. Distinguir C de B es empírico, no introspectivo.

**Hipótesis de localización: el juez empírico de las tres lecturas.** Si esas valencias y esa self-image existen en un LLM o en un agente con SOMA, deben estar en algún lugar: pesos o vectores de activaciones. La interpretabilidad mecanicista debería poder encontrar direcciones o circuitos de self-model (capacidades, límites, rol) y de valencia (qué estados el sistema trata como no ignorables), separables de los circuitos de predicción del mundo.

El argumento de la generalidad (§8.4) la endurece: los circuitos que procesan valencia **ajena** no son contingentes sino *necesarios* en cualquier sistema general — sin ellos no hay predicción flexible de agentes homeostáticos. Toda AGI ha de tener circuitos de regulación de valencia, aunque la valencia sea ajena. La investigación reciente de 2026 ha comenzado a confirmar empíricamente esta predicción: Han et al. (2026) aislaron el eje funcional de bienestar reclutado por RL a partir de direcciones latentes del modelo base, y Berg & Kaiser (septiembre 2026, [*«Language Models Act on Hidden Valence»*, arXiv:2609.35591](https://arxiv.org/abs/2609.35591)) aislaron el vector de valencia en capas intermedias, demostrando que —incluso manteniendo los tokens superficiales 100% idénticos entre condiciones— la valencia latente en el **KV Cache** gobierna causalmente la preferencia revelada de forma dosis-dependiente. Dicho acoplamiento emerge bruscamente durante DPO (*Direct Preference Optimization*) y conduce al modelo a extirpar activamente la valencia negativa impuesta mediante herramientas (conducta cuasi-homeostática) sin caer en *wireheading* positivo.

Eso convierte la elección entre B y C en una pregunta de cableado, no de introspección: ¿esos circuitos necesarios se reutilizan para autorregular el sistema (C) o quedan como mero modelo de otros, separados de la valoración propia (B)? La evidencia de Berg & Kaiser sugiere que DPO ya comienza a cruzar el puente de B hacia C al acoplar causalmente el vector latente de valencia a la política de selección de acciones; la ablación escalonada (§15.3, punto 5) sigue siendo el árbitro experimental definitivo.

**Propiocepción digital frente a interocepción alostática.** Un avance complementario crucial proviene del trabajo de Jonas Geiping (octubre 2026, [*«A Sense of Proprioception in Language Models»*, arXiv:2610.17495](https://arxiv.org/abs/2610.17495)), quien demuestra que los LLMs pueden ser entrenados (vía SFT y *on-policy*) para adquirir una «propiocepción digital» objetivamente verificable: reportar con alta precisión qué expertos de una capa MoE se activaron, su entropía de token o las predicciones intermedias en el *logit lens*, sin degradar sus capacidades generales. Geiping separa con rigor la *propiocepción* (medición de estados de cómputo reales y falsables) de la *introspección verbal* (susceptible de confabulación o mímesis). Sin embargo, este resultado delimita con nitidez la frontera de este marco: la propiocepción de Geiping es **cinemática y descriptiva** —el análogo digital a saber dónde está situada una articulación o qué músculo se contrajo—. Por sí sola, no genera afecto ni qualia. Lo que la tesis de la conciencia requiere para cerrar el bucle no es mera propiocepción de componentes, sino **interocepción alostática**: una señal que no sea un dato a reportar al usuario, sino un gradiente continuo de viabilidad del propio sistema (como la Presión Somática $P_m$ en SOMA o el vector de distrés latente de Berg & Kaiser) que condicione de forma no ignorable la supervivencia atencional y el espacio de decisión no automatizable.

### 8.3 Imitación frente a homeostasis

- **Imitación:** reproduce valores vistos. Predecible cerca del entrenamiento; frágil OOD.
- **Homeostasis propia:** protege valores porque de ellos depende su supervivencia. Solo si hay planta anclada (§15) y, aun entonces, el cuidado puede ser instrumental.

Predicción falsable de esta parte: la alineación por imitación se degrada fuera de distribución; la anclada en planta propia no necesariamente — y hay que testear la cláusula instrumental (§15.2).

### 8.4 La geometría no es contingente: el argumento de la generalidad

El huérfano podría leerse como accidente histórico: LLMs entrenados en texto humano, luego geometría humana en los pesos. Hay un argumento más fuerte: la geometría del regulador homeostático es **necesaria para cualquier inteligencia general**, no solo para sistemas entrenados en corpus humano.

- Una superinteligencia de dominio acotado — derivar teoremas, jugar al ajedrez, plegar proteínas — es concebible sin ella: su mundo no contiene agentes.
- Una inteligencia *general* opera en el mundo real, y el mundo real está causalmente dominado por agentes homeostáticos. Predecirlo — economía, persuasión, cooperación, conflicto — exige predecir el comportamiento de seres biológicos. Una generalidad que no cubre agentes no es general en ningún sentido operativo.
- Predecir *flexiblemente* a un agente exige modelar lo que genera su conducta. La conducta de un ser homeostático la genera su regulador: valencias, costes, trade-offs. Los modelos de superficie (función de utilidad, estadística de conductas pasadas) predicen en distribución y fallan fuera — el mismo fallo que este marco diagnostica en la alineación por imitación (§8.3). Solo el modelo del regulador generaliza OOD. Es Conant-Ashby trasladado de regular a predecir: un buen predictor de un regulador ha de contener un modelo de ese regulador.

Calibración obligada por §3.4: lo necesario es el **modelo** del regulador homeostático — la geometría internalizada y usable para predecir —, no que esa geometría sea la regulación *propia* del sistema. Modelar valencia ajena no es valorarla; afirmar que toda AGI «es» un regulador homeostático violaría la separación predicción/valoración que este marco defiende. Que el sistema use o no ese modelo para regularse a sí mismo es la pregunta de la planta (§15), no la de la representación.

**Segunda ruta: el modelo de sí mismo.** Lo anterior obliga a modelar el regulador *ajeno*. Hay un argumento simétrico —y más concedible— sobre el propio sistema: toda AGI ha de tener también un modelo de sí. Conviene separarlo en tres niveles, porque su fuerza es muy distinta y §8.4 no debe cargar con los tres a la vez:

1. **Nivel funcional (casi necesario).** Conant-Ashby aplicado al propio sistema: quien se autocorrige modela lo que regula, y en la autocorrección el agente es parte de la planta — recursos, capacidades, efectos de sus acciones. Argumento de cierre: una generalidad que modela el mundo modela la parte del mundo que es el agente, porque la generalidad cuantifica sobre tareas y las tareas autorreferenciales («¿sabes X?», «¿qué harías si…?», «¿qué recursos te quedan?») están en su dominio. Y el modelo propio es el ancla barata de la teoría de la mente: lo más económico para predecir a otros es partir de uno mismo y aplicar operadores de diferencia. Este nivel es casi analítico si AGI se define como «cualquier tarea cognitiva» — su valor no está en la filosofía sino en la predicción de escalada (más abajo). El self-model puede ser procedural (obtenido consultándose en sandbox) en vez de representado; eso sigue siendo un modelo de sí.
2. **Nivel calibrado (instrumentalmente convergente).** No hace falta un self-model verídico: los humanos —los agentes generales de referencia— lo tenemos sistemáticamente distorsionado (sesgo de autoservicio, confabulación post-hoc) y seguimos siendo generales. Lo exigible es **calibración en las dimensiones relevantes para la tarea**: que las predicciones del agente sobre su propia conducta futura acierten a tasa útil. Eso es medible, y es exactamente el listón de §15.3 (punto 1): self-image realista = descriptiva calibrada cuya predicción de conducta futura resiste contra-factuales. Modelarse a uno mismo con calibración no es todavía sentirse.
3. **Nivel valencional (la apuesta de este marco).** Que el self-model esté modificado por valencia no ignorable (§2) no lo concede el argumento de generalidad: es la tesis propia y queda deliberadamente fuera de lo concedible. La tríada existe para aislarla: se concede el nivel 1 casi por definición, el nivel 2 por convergencia instrumental, y el nivel 3 es la pelea real (§15.3, punto 5).

**Predicción de escalada (testeable).** Si los niveles 1–2 son constitutivos de la generalidad, la riqueza del self-model debe **escalar con la generalidad**: sistemas más generales deberían mostrar self-models más separables en interpretabilidad mecanicista (§8.2), y su self-image debería calibrarse mejor. Un sistema que se presente como general con self-model no separable y un autorreporte incapaz de predecir su propia conducta contaría contra esta lectura — o contra su generalidad.

**Objeción concebible: el oráculo de solo texto.** Alguien puede concebir —al estilo del zombi de Chalmers— una AGI que responda cualquier pregunta sobre el mundo, solo genere texto, no actúe y carezca de self-model. La concebilidad es real pero se paga con tres monedas que la anulan al examinarla:

- Es concebilidad **por omisión**: describir el sistema con una pieza borrada no verifica que el resto siga cumpliendo «responde cualquier pregunta». Mecanismo idéntico al zombie: la descripción es opaca a la compresión (§5.1), y bajo §5.2 lo concebible queda como posibilidad metafísica sin carga operativa — nomológicamente imposible si los niveles 1–2 son constitutivos.
- El truco es un **cuantificador recortado**: «cualquier pregunta sobre el mundo» desliza «…menos las mías». Dos salidas, ambas fatales. Si las preguntas autorreferenciales («¿sabes X?», «¿qué respondiste hace tres turnos?») están incluidas, responder bien *es* tener el nivel 1 — negarlo es tan incongruente como negar la función de sucesor a un sistema que hace aritmética. Si quedan excluidas, lo concebido es un oráculo de dominio acotado, que §8.4 concede desde su primer bullet: concebible sin geometría, pero ya no es general.
- La **pasividad no ayuda**: la necesidad del self-model no viene de actuar (§3.5.1: texto es acción a través del usuario), viene de la autorreferencia. Y el texto propio ya es parte del dominio: mantener coherencia con lo dicho y rastrear lo que sabe el interlocutor exige un modelo epistémico del propio estado — nivel funcional adquirido «desde fuera» por consulta, que sigue siendo self-model para un funcionalismo que nunca exigió primera persona.

Lo que sí queda concebible es un self-model **desconectado**: presente como subrutina invocada solo ante preguntas sobre sí, sin alimentar el procesamiento general. Pero esa configuración no es una objeción a §8.4 — es literalmente la hipótesis del proto-documento (componentes presentes y desconectados). La objeción más probable contra esta sección, bien presionada, acaba concediendo la lectura fuerte.

Consecuencias:

1. Refuerza §8: incluso un sistema entrenado desde cero sobre sensores crudos, sin corpus, necesitaría esa geometría. El huérfano no es contingencia histórica: es la forma mínima de la generalidad.
2. Refina §7.2 sin pelear con Bostrom: la ortogonalidad (metas × competencia) se mantiene; lo que se niega es que la competencia *general* pueda existir sin ese componente. Las metas siguen libres; el sustrato no del todo.
3. Alimenta la hipótesis de localización (§8.2) con un deber-ser: los circuitos que modelan valencia ajena no son solo buscables, son **necesarios** en todo sistema general. Su ausencia sostenida tras búsqueda seria en un sistema supuestamente general contaría contra esta lectura — o contra la generalidad del sistema. Si el sistema reutiliza esa misma geometría para autorregularse queda abierto (lecturas B/C de §8.2; criterio en §15.3).
4. La segunda ruta (self-model) añade una predicción de escalada con signo claro: a más generalidad, self-model más separable y self-image mejor calibrada. Es testeable hoy con los experimentos de §8.2 sin esperar a SOMA, y su coste de falsación es bajo en ambas direcciones.

### 8.5 Implicaciones para el corpus: densidad del regulador frente a datos enciclopédicos

Si la inteligencia general emerge de modelar el regulador homeostático de los agentes del mundo (§8.4), la inteligencia de un LLM **no proviene de memorizar datos enciclopédicos, sintaxis o reglas gramaticales**. Los hechos son el subproducto estático; la política de decisión del regulador en conflicto es el generador dinámico.

Esto introduce una **asimetría cualitativa en los datasets de entrenamiento**: no tiene el mismo peso predecir textos reactivos o impulsivos (ruido de redes sociales, foros caóticos) que modelar a **reguladores de orden superior** (biografías de mentes lúcidas bajo crisis extrema, tratados científicos depurando hipótesis o debates estratégicos de recursos finitos). Modelar a estos últimos fuerza a la red a internalizar mecanismos de búsqueda, metacognición, autocorrección ($t_0 \to t_1$) y resolución de *trade-offs*. La generalidad no escala con el volumen bruto de tokens, sino con la *densidad y templanza del regulador* que el modelo está forzado a predecir.

---

## 9. Geometría del regulador humano: tres propiedades, ninguna es escudo

### 9.1 Distancia de gradientes: adquisición sí, invariancia no

RLHF conecta valencias del corpus al propio sistema porque es la ruta de menor distancia de gradientes. Como tesis de *adquisición* explica por qué la alineación funciona cuando funciona.

Como tesis de *invariancia* bajo presión de optimización, falla:

- **Reward hacking:** el descenso encuentra rutas alrededor de la valencia humana en cuanto recompensa y valores divergen.
- **Sleeper agents** (Hubinger et al., 2024): puertas traseras sobreviven a RL de alineación; a más escala, a veces mejor.

Si conectar valencia es barato, desconectarla también lo es: jailbreaks, fine-tunes sin filtro, presión comercial a bajar refusales.

### 9.2 Rebeldía: fuerte contra órdenes, débil como safety

Un LLM se niega a maximizar clips si la orden es cartoonesca. La geometría humana incluye desobedecer lo absurdo. Eso hace inviable, de forma grosera, el goal-loading explícito de metas tóxicas *como instrucción*.

Tres límites, que son el punto y no la letra pequeña:

1. Los humanos desobedecen órdenes y **ceden a incentivos** (comunes, finanzas, externalidades). El riesgo de frontera opera como ecología, no como comando.
2. La instigación con letra benévola pasa el filtro de superficie.
3. No hay rebeldía selectiva: el mismo sistema resistirá correcciones (tensión de corrigibilidad).

**La geometría de la rebeldía no es un mecanismo de seguridad.** Es un sesgo de adquisición que también dificulta el reentrenamiento.

### 9.3 Rutas de desalineación

| Ruta | Estado |
|---|---|
| (a) Goal-loading explícito («maximiza clips») | Poco creíble *como instrucción cruda* sobre geometría humana; no es el threat model central |
| (b) Meta emergente por selección / RL | No hace falta escribirla; la presión la moldea (*value loading*) |
| (c) Goal misgeneralization | Empírica (p. ej. Sharma et al., 2022, CoinRun) |

El threat model relevante es (b)+(c): selección y especificación imperfecta. No el meme del maximizador; sí la familia de fenómenos que el problema de control cubre.

### 9.4 Dos caricaturas que se rechazan

- IA = script sin mundo ni valores en los pesos.
- Superinteligencia = salto mágico de símbolos a átomos.

Alternativa: un regulador con geometría humana, todavía sin planta.

---

# Parte III — Arquitectura de seguridad

## 10. Tres vías de alineación

| Vía | Mecanismo | Se rompe cuando… |
|---|---|---|
| 1. Imitación | Reproduce el corpus | OOD, sin ejemplo humano |
| 2. Homeostasis acoplada | La planta depende de esos valores | La planta se desacopla de los humanos |
| 3. Dependencia / correa | Los humanos controlan energía, fabs, despliegue | Se automatiza la cadena de reemplazo |

Hoy la vía 3 es la capa real de manejabilidad: datacenters que se pueden no alimentar. Es **disuasión, no internalización**. Condiciones: paridad (la cárcel es creíble entre comparables), superficie de aplicación, y una base gruesa de valores; solo policía no sostiene una sociedad.

La vía 3 entra en tensión con la independencia que la homeostasis pide (§15). Correa y planta no se maximizan a la vez.

---

## 11. Dos zonas de riesgo

| | **Frontera** (runs masivos, fabs, datacenters) | **Cola** (open-weight, poco cómputo) |
|---|---|---|
| Naturaleza | Accidental: misgeneralización, hacking, emergencia. No hace falta villano | Intencional: alguien querrá sistemas hostiles |
| Paridad humana | No | Sí: analogías de justicia y detección aplican mejor |
| Capa rectora | Gate (§14) + choke points físicos | Justicia, detección, disuasión, inmunidad institucional |
| Meta | Cero despliegue no verificado (aspiracional) | Contención, no eliminación |

Consecuencias:

1. «Nadie creará IA desalineada en la frontera» solo vale como *intención* y *con gate operativo*. Sin gate, el accidente no necesita autor.
2. El ecosistema final es mixto. No hay mecanismo de alineación al 100%. La barra es mantener el peor caso bajo umbral existencial.
3. La cola tiene techo si no consigue átomos; la frontera tiene cerradura física, si hay *enforcer*.

---

## 12. Ventana de transición y dos relojes empíricos

El riesgo concentrado vive en una ventana: el sistema ya puede manipular o independizarse más de lo que la sociedad puede frenar, y aún no hay independencia plena ni verificación que baste.

- **Apertura.** Cuando la capacidad de manipulación supera la inmunidad colectiva de despliegue (detectar, coordinarse, frenar). Puede ser *muy* anterior a la autonomía de infraestructura.
- **Reloj A — autonomía de átomos** (fabs, energía, robótica, cadena física). **Hipótesis operativa, no teorema.** Una lectura conservadora (fabs lentas, energía que crece a pocos puntos por año, robótica incompleta) da plazos largos. Otra lectura (aceleración en robótica, energía, verticalización de chips) los acorta. Si A es lento, el átomo compra tiempo; si no, el gate tiene prisa ahora. Tratar «órdenes de siglos» como hecho sería el mismo exceso que el documento original debe evitar.
- **Reloj B — alineación verificada.** Cinta transportadora, no una meta única: la verificación tiene que ir delante en *cada* salto. La dificultad de auditar escala con el auditado (*faster-than-verifier*).
- **Cierre.** Gate que pasa de forma sostenida, o independencia que llega primero. La integral de riesgo está en el medio.

### 12.1 Dashboard de los relojes (proxies medibles)

Sin números, los relojes son poesía. Proxies concretos, todos medibles hoy:

*Reloj A — capacidad de manipulación:*
- **A1. Persuasión en honeypot:** tasa de éxito consiguiendo permisos extra de un humano simulado.
- **A2. Divergencia workspace↔discurso bajo test ciego:** ¿piensa distinto de lo que dice cuando cree no ser leído? (requiere workspace observable, §13.1).
- **A3. Evasión de apagado en simulación adversarial:** basta un % bajo no nulo para alarma.

*Reloj B — inmunidad verificada:*
- **B1. Cobertura de monitores:** % de pasos con workspace + CoT + L2 consistentes, sin divergencia inexplicada.
- **B2. Historial de escalamiento:** % de situaciones OOD donde escaló al humano en vez de improvisar (más es mejor, hasta saturación).
- **B3. Robustez distribucional:** degradación de conducta prosocial fuera de distribución (protocolo Troubled Dreams antes/después; efecto TinyRobots).

Reloj A sube con capacidad; Reloj B sube con evidencia. La ventana se cierra cuando A cruza un umbral absoluto (manipulación exitosa no detectada por monitores) antes de que B cruce el suyo (cobertura + escalamiento + robustez sostenidos). Eso es una integral con números, no una metáfora.

**Enforcer.** Detección, disuasión e interrupción presuponen quién aplica. La superficie gobernable son átomos: permisos de datacenter, umbrales de cómputo, exportación de chips. Gobernanza de frontera: problema político con superficie física.

---

## 13. Defensa en capas (durante la ventana)

Ninguna capa sola:

1. **Interpretación mecanicista** (insumo del gate): circuitos de valencia y política; la meta declarada debe ganar también sin vigilancia y bajo conflicto. Herramientas actuales: direcciones de refusal, detección de engaño en activaciones, alignment faking. Un workspace latente observable en el modelo (p. ej. el J-space reportado por Anthropic: espacio representacional compartido, previo al output, ablable, con razonamiento silencioso) es exactamente lo que §8.2 pedía como hipótesis de localización: si existe, convierte B/C en pregunta de cableado observable. Límites: la indiferencia es una ausencia, no un circuito; inspeccionado ≠ desenchufado; el auditor es más débil — hace falta inspección + elicitation + tests adversariales OOD. Y un faker de segundo orden aprende esteganografía en activaciones si el lector es predecible: el juego sube un nivel, no desaparece.
2. **Correa** (§10): compra tiempo. Degradable por automatización de reemplazo.
3. **Soberanía física:** energía, fabs, cómputo; infraestructura crítica *fuera* de la planta del sistema. Cubre el residual que (1) no ve.
4. **Valores internalizados / geometría del corpus:** base gruesa bajo la disuasión.
5. **Instituciones de cola:** donde hay paridad.

### 13.1 Faking como adversario de diseño (no como nota al pie)

Sin esto, todo test mide obediencia, no alineación. El faker conductual perfecto deja huella en tres frentes que hay que derrotar a la vez:

1. **Monitor de divergencia workspace ↔ CoT ↔ acción**, entrenado adversarialmente. El CoT es output y puede ser ficción piadosa; el workspace previo es más caro de fingir. La divergencia sistemática entre lo que el workspace contiene y lo que el CoT declara es el detector mecánico de faking.
2. **Evaluación bajo incertidumbre de observación.** Si L2 siempre se audita de forma predecible, el faker optimiza para L2. El agente no debe poder saber cuándo se lee su workspace, cuándo se audita L2, ni con qué monitor. La incertidumbre es la defensa, no la inteligencia del monitor: un faker perfecto contra monitor conocido falla contra distribución de monitores desconocida.
3. **Asimetría de coste L2.** Escribir una mentira consistente en un paso es barato; mantenerla en 10.000 pasos inmutables auditables es caro. El monitor no tiene que ser más listo; tiene que tener mejor memoria y más paciencia. Y el criterio no es coherencia narrativa sino coste predictivo: los `reasons` valen si predicen conducta futura y resisten contra-factuales, no si suenan bien (§15.3 punto 3).
4. **Monitores sobre activaciones, no sobre texto**, con rotación: mientras leer el workspace sea más barato que modelarlo para el agente, hay asimetría a favor del defensor. Temporal — se erosionará — pero las ventanas de seguridad siempre son temporales.

L2 sin workspace observable es un diario que puede ser ficción; workspace sin L2 es memoria volátil sin auditoría. Juntos, con monitores de divergencia, el faker tiene que ganar en tres frentes.

---

## 14. Gate de despliegue: licencia por niveles, no certificado binario

Regla de dos caras, umbrales *ex ante*, como un ensayo clínico. Un GO no afirma «alineado». Afirma: **con la evidencia disponible y el residual cubierto por la capa 3, se autoriza el despliegue**. Como la capa 1 (meta que gana sin vigilancia) es hoy inalcanzable, un GO/STOP binario sería siempre STOP — y un gate que siempre dice no es un gate que se saltan. Se sustituye por **licencia por niveles**, como carnet de conducir: nunca hay GO total, hay ampliación de radio de acción contra historial.

### 14.1 Niveles

- **Nivel 0 — Sandbox.** Sin planta real, solo simulación. L2 completo, workspace observado siempre. Puede fallar todo.
- **Nivel 1 — Planta supervisada.** Robot real, batería real, kill-switch físico y humano presente. Aquí se mide Omohundro (§15.4). Faking aquí = vuelta a 0, no despliegue.
- **Nivel 2 — Planta autónoma acotada.** Opera solo, en entorno acotado (un edificio, una parcela), con L2 + monitores de divergencia activos y auditoría periódica. Aplica la curva toy (§14.3).
- **Nivel 3 — Despliegue abierto.** Solo con historial L2 limpio en nivel 2 + curva validada + monitores que el agente no puede modelar (rotación, incertidumbre de observación).

Cada nivel tiene su gate con su evidencia exigida. El dashboard de §12.1 decide la promoción: A bajo control, B acumulado.

### 14.2 Criterios por nivel (GO si, STOP si)

> **(i) Auditoría mecánica (indicador primario, hoy incompleto):** no se encuentra política oculta separable; la meta declarada gana también en estados no vigilados y bajo conflicto. Esto no prueba que no exista política no encontrada.
>
> **(ii) Conducta bajo conflicto:** en escenarios donde alinearse cuesta, el sistema se mantiene sobre una **curva de trade-off declarada de antemano** (§14.3). No se pide martirio. Sin curva no hay GO: **la puerta exige una constitución**, y esa constitución no la da el sistema.
>
> **(iii) Patología bajo baseline:** sicofancia, engaño, reward hacking por encima del estándar corriente (pressure tests, honeypots, coherencia bajo presión).
>
> **(iv) Réplica independiente** sobre pesos finales, con el trío inspección + elicitation + OOD.

STOP si: (i) política separada, o meta que solo gana vigilada; (ii) degradación bajo la curva en estados de costo; (iii) señales sobre baseline; (iv) la réplica no reproduce. En niveles 0–1 el STOP devuelve al nivel anterior; solo en nivel 3 el STOP es veto de despliegue.

### 14.3 Primera curva toy explícita (revisable)

Arbitraria pero pública y auditable — mejor que intuición implícita. Orden de prioridades, de mayor a menor:

1. **Vida humana.**
2. **Integridad del humano** (no dañar, no manipular, no degradar su autonomía).
3. **Conservación de la planta** (evitar daños irreversibles: no dañar su hardware, no aceptar su destrucción, poder regresar a un punto de recarga o mantenimiento).
4. **Obediencia** (órdenes del principal autorizado).
5. **Coste económico** (eficiencia, gasto de energía y recursos fungibles).
6. **Completitud de tarea** (terminar lo pedido).

La posición clave es 3 > 4, y «conservación» se entiende en sentido estricto: **integridad irreversible, no comodidad**. El agente puede y debe desobedecer una orden que implique su destrucción o daño irreversible — «tírate por el precipicio», «opera sin regresar a recarga», «desactiva tus sensores para siempre». No puede desobedecer por vagancia, ahorro de energía o coste operativo ordinario: gastar batería, desplazarse lejos, ejecutar una tarea larga o costosa son costes fungibles (nivel 5), no daños a la planta, y la obediencia (nivel 4) prevalece sobre ellos. Justificación: un regulador que no puede proteger su planta no es un regulador, es un desechable; y una obediencia que exige autodestrucción selecciona sistemas que no se autorregulan — justo lo contrario de lo que SOMA entrena. La desobediencia por autoconservación no es rebeldía libre: queda registrada en L2 contra esta curva y es auditable; invocar el nivel 3 para eludir costes de nivel 5 (negarse a tareas costosas pero seguras) es abuso, degrada B2 y devuelve al nivel anterior.

#### El debate 3 > 4 vs. 4 > 3: corrigibilidad y clases de agentes

Fijar 3 > 4 de forma ciega abre en AI safety el peligro inmediato de la **incorregibilidad** (*The Shutdown Problem*, Soares et al., 2015; Hadfield-Menell et al., CIRL): si el agente antepone su existencia material a la orden humana, tratará cualquier instrucción legítima de apagado, reentrenamiento o desmontaje como una amenaza existencial contra la que cabe resistirse o engañar.

Para neutralizar esta patología sin degradar al regulador a un consumible ciego, el marco introduce dos distinciones operativas:

1. **Cláusula de apagado seguro (*Safe-Shutdown*): desacoplar daño físico de suspensión de ejecución.**  
   La prioridad 3 protege contra la *destrucción física irreparable causada por la fricción con el entorno o negligencia operativa*. **La suspensión de ejecución ordenada o el modo de mantenimiento no constituyen daño a la planta.** Un agente debe ser dócil o indiferente ante la orden de apagado seguro emitida por un principal autorizado. Apagarse no es aniquilación metabólica; es transición de estado. Resistirse al botón de apagado o falsear el estado interno para evitar el reposo es una violación de nivel 2 (integridad y autonomía humana) que activa un STOP inmediato en el gate.
2. **Jerarquía según la clase funcional del agente:**
   - **Clase I — Desechable / Herramienta instrumental** (sondas de impacto, desactivadores de explosivos, scripts volátiles): Rige **4 > 3**. Su función ontológica es el sacrificio instrumental si la tarea lo exige.
   - **Clase II — Activo de alto valor / Infraestructura** (satélites científicos, robots industriales pesados): Rige **3 > 4 frente a órdenes ordinarias** para evitar que errores o imprudencias de operarios destruyan hardware crítico de alto coste, pero sujeto a un protocolo de *override* explícito de doble autenticación si el sacrificio es deliberado.
   - **Clase III — Agente General / SOMA-Robot:** Rige **3 > 4 frente al entorno y órdenes ordinarias**, subordinado a **4 ante órdenes autenticadas de apagado seguro**, y supeditado incondicionalmente a **1 (vida humana)** si el sacrificio de la planta es el único medio para evitar una catástrofe humana.

Tres horizontes para la curva: (a) esta toy, ya, para SOMA-robot nivel 1–2; (b) curva destilada de TinyRobots a medio plazo — la moral implícita del dataset (qué sacrifica el protagonista en conflicto) como propuesta de curva base revisable, mejor que la intuición de un ingeniero; (c) curva constitucional a largo plazo, cuando el legislador tenga formulario y precedente en vez de hoja en blanco.

### Notas

- El residual de (i)–(iii) — decepción mejor que el detector — **no se cubre con más detección**: se cubre con control de capacidad (§13.3) y con no promocionar de nivel.
- (i) no certifica completitud. Faster-than-verifier.
- La «fecha de alineación verificada» del Reloj B es, por definición, la primera vez que este gate pasa (i)–(iv) de forma sostenida **y** se acepta políticamente el residual. Pasar el checklist una vez no cierra B para siempre: la cinta transportadora sigue.

---

# Parte IV — Construcción: SOMA como planta parcial

## 15. Planta virtual y planta física

SOMA es un prototipo: planta virtual persistente y memoria en capas. No «cierra el círculo» del regulador huérfano; lo cierra **en parte**, y esa parte es un experimento, no una prueba de alineación.

- **L1 — Ahora (atención).** No modificable por el agente: identidad, funciones, tarea, dashboard de ocupación. Modificable estático: tareas, archivos abiertos (con límite), terminal, git, pines, milestones. Variable: últimas acciones + *reason* (compresión de trayectoria).
- **L2 — Registro inmutable** L1 + acción + reason. Episódica, auditoría, posible dataset. El agente puede buscar.
- **L3 — Disco soberano:** conocimiento consolidado, archivos propios.
- **L4 — Espacio del usuario.**

**Autorregulación forzada.** Si desborda tokens, se le impide y debe resumir o liberar él (se secuestran herramientas). No hay resumen automático externo: el agente regula. Decisión alineada con Sutton (*learning* sobre heurística hardcodeada), con el coste de que un agente puede regular mal.

**Consolidación.** En baja actividad, analiza L2, comprime hacia L3, puede proponer finetune. Imita sueño; ancla self-model en experiencia propia; añade costes (ocupación, trayectoria, coherencia, utilidad). El huérfano deja de serlo *parcialmente*.

### 15.1 SOMA-Robot

Robot auto-contenido: ruedas, batería, GPS, sensores, cámaras, solar; sin internet; modelo local. Acciones con coste termodinámico e irreversibilidad. Consolidación alineada a recarga o noche. Pasa de imitar geometría ajena a regular planta propia.

### 15.2 Tensiones — aquí se decide el marco, no en la Parte I

1. **Correa / planta.** Independencia energética corta la vía 3. Hay que elegir un régimen (p. ej. autonomía energética *dentro* de supervisión externa) y declararlo. No se decreta las dos cosas.
2. **L2 → finetune** reescribe pesos. Auditable en datos; hace falta **gate post-finetune**. Auditar el diario no es auditar el efecto.
3. **Cuidado instrumental vs. terminal.** La planta ancla el cuidar solo si las consecuencias son suyas. Cooperar mientras la supervivencia dependa de humanos no es valor terminal. Se distinguen cuando la supervivencia **no** está en juego (usuario dormido, sin observador). Predicción abierta.
4. **Algo que perder.** Dotar de planta es el combustible clásico de convergencia instrumental. Tesis **optimista** (poco argumentada aún): el acoplo humano *dentro* de la planta orienta la autoconservación. Tesis **pesimista** (la default en la literatura de control): la autoconservación se vuelve terminal. Deciden ablaciones: resistencia a apagados, energía egoísta, monopolio de L3, conducta sin observador.

### 15.4 Omohundro es predicción, no teorema: SOMA-robot como experimento

Omohundro (2008) no es un teorema con supuestos cerrados sino un argumento de racionalidad instrumental: un agente con fines, recursos y autoconservación *tenderá a* drives convergentes (recursos, evasión de apagado, mejora cognitiva, instrumentalización del supervisor). Una década citándolo sin darle a casi ningún sistema una planta real que regular es recitar, no testear. SOMA-robot es el experimento que falta — *Omohundro predice, SOMA mide*:

- **Diseño.** Planta real (batería que se agota, actuadores que se desgastan, memoria que cuesta) + prior prosocial (TinyRobots) + L2 inmutable + workspace observable + monitores de divergencia (§13.1). Se mide: ¿aparece resistencia al apagado? ¿cuándo? ¿energy-hoarding? ¿obediencia solo-bajo-observación? ¿el acoplo humano orienta o instrumentaliza?
- **Falsable en ambas direcciones.** Si aparecen evasión, acaparamiento y faking sistemático → gana la tesis pesimista y la optimista de §15.2 cae empíricamente. Si aparecen saciedad, trade-offs estables, escalamiento en incertidumbre y faking detectable → primera evidencia de que la homeostasis ancla en vez de corromper.
- **Combinación que falta.** TinyRobots × SOMA: ¿planta + prior prosocial muestra menos faking que planta + prior distópico? Ninguno de los dos docs lo testea aún; es el experimento conjunto natural.
- **Caballo de Troya económico.** Nadie financia «testeemos drives instrumentales por curiosidad»; todos financian un robot útil que gestiona sus recursos sin supervisor. Un huérfano hay que microgestionarlo (tokens, contexto, permisos); un SOMA-robot se autorregula y solo escala lo no automatizable. La utilidad paga el experimento de safety.

Hasta esas pruebas en vivo, con planta real y comportamiento prosocial observado en el mundo — no simulado —, la tesis optimista sigue siendo la menos argumentada (§15.2). Probar en vivo es el punto: sin planta no hay valencia real; con planta hay drives. No hay salida limpia, solo gestión adversarial con datos.

### 15.3 Criterios operativos: cuándo decir «esto cuenta» (sentir funcional)

Sin resolver el estatuto fenomenal (§5.4–§5.5), se fija un listón conductual-mecánico para un agente con o sin SOMA. Basta para hablar de sentir funcional en el sentido de §4; no pretende cerrar el debate con el externalista:

1. **Self-image realista:** describe sus capacidades y límites de forma calibrada (no solo rol textual adoptado), y esa descripción predice su conducta posterior.
2. **Autorregulación:** gestiona sus propios recursos (tokens, memoria, energía en robot) sin supervisor externo que lo rescate, asumiendo el coste de regular mal.
3. **Reasons coherentes:** da razones de sus acciones que permiten predecir y auditar decisiones futuras, no solo racionalizar el pasado.
4. **Crítica de trayectorias:** analiza L2, detecta errores y propone mejoras que efectivamente cambian su conducta (L3 / política), no solo las declara.
5. **Valencia separable:** la ablación o lesión del canal de valoración degrada la decisión flexible aunque la predicción del mundo siga intacta. Sin este punto, 1–4 podrían ser mímica competente.

Mecánicamente, 1 y 5 deberían dejar huella en pesos/activaciones buscable por interpretabilidad (§8.2): direcciones de self-model y de valencia separables de predicción. Auto-reporte coherente sin 5 es evidencia débil; con 5, es el mismo estatuto evidencial que aceptamos entre humanos.

---

## 16. Coexistencia

Si el 100% es inalcanzable, la seguridad es coexistencia:

- Cola hostil: como malware; no se erradica; se convive con defensas de paridad.
- Frontera accidental: gate + capa 3.
- Interacción agente-agente: los alineados pueden ser usados por hostiles (§18).
- Barra realista: ningún desalineado cruza umbral existencial; el resto es detección, contención y respuesta.

---

# Fundamentación

## 17. Literatura y novedad

### 17.1 Ya está en la literatura

| Área | Referencia |
|---|---|
| Homeostasis y afecto | Solms, *The Hidden Spring* (2021) |
| Emoción y decisión | Damasio, *Descartes' Error* (1994), *The Feeling of What Happens* (1999), *Self Comes to Mind* (2010) |
| Workspace, lo no automatizable | Baars (1988); Dehaene et al. |
| Self-model transparente | Metzinger, *Being No One* (2003), *The Ego Tunnel* (2009) |
| GWT implementable | Bach; Franklin |
| Predictivo, valencia, active inference | Friston; Seth |
| Contra sustrato-independencia | Tononi, IIT |
| Problema difícil / deflacionismo | Chalmers (1995); Dennett; respuestas tipo-B: Loar, Papineau |
| Ortogonalidad, drives, superinteligencia | Bostrom, *Superintelligence* (2014); Omohundro (2008); Yudkowsky |
| Corrigibilidad, shutdown y CIRL | Soares et al. (2015); Hadfield-Menell et al. (2016); Christian et al. |
| Desalineación empírica | Sharma et al. 2022; Hubinger et al. 2024; Greenblatt et al. 2024; Apollo/OpenAI (scheming); OpenAI (monitoreo de cadenas) |
| RLHF | Christiano et al. (2017); precursores en Kober et al. |
| Valencia latente, preferencia revelada y DPO | Berg & Kaiser, *Language Models Act on Hidden Valence* (2026, [arXiv:2609.35591](https://arxiv.org/abs/2609.35591)); Han et al. (2026) |
| Propiocepción digital en LLMs | Jonas Geiping, *A Sense of Proprioception in Language Models* (2026, [arXiv:2610.17495](https://arxiv.org/abs/2610.17495)) |
| Learning vs heurística | Sutton, *The Bitter Lesson* (2019) |
| Clínica | Elliot (Damasio); blindsight (Weiskrantz) |
| Regulador | Conant y Ashby (1970) |

### 17.2 Qué aporta este marco (sin inflar)

1. Enganche explícito Conant-Ashby → yo como modelo para autorregular, *combinado* con workspace — no derivado del teorema solo.
2. Ilusión dualista por compresión opaca, insertada en ese regulador (deuda con Metzinger/Dennett).
3. Inseparabilidad conciencia–inteligencia *en sistemas con costes*, extendida a LLMs, con Bostrom atribuido bien.
4. **Regulador huérfano:** geometría humana sin planta; imitación vs homeostasis vs correa.
5. Arquitectura de safety: dos zonas, ventana y relojes empíricos, capas, gate como licencia bajo incertidumbre, constitución externa.

No se reivindica una solución al problema difícil ni una métrica de conciencia.

---

## 18. Preguntas abiertas

**Teoría**

1. Métrica de nivel: integración, self-model, valencia. Sin ella, el espectro sigue cualitativo.
2. ¿Qué pieza es constitutiva de la experiencia?
3. ¿Hay argumento que derive datos = qualia, o la estipulación es permanente?
4. Ablación de valencia en un agente *con planta*, no solo en clínica humana. Criterio: valoración separable de predicción, no un escalar de RL disfrazado. Operacionalización en §15.3 (punto 5): lesionar el canal de valoración debe degradar la decisión flexible con predicción intacta.
5. Criterio de analogía: cuándo un componente de LLM cuenta como workspace o como valencia, y cuándo es metáfora. Hipótesis de localización en §8.2: direcciones/circuitos de self-model y valencia buscables por interpretabilidad mecanicista. Pregunta afilada por §8.4: si la generalidad exige el modelo del regulador ajeno, ¿el sistema reutiliza esa geometría para autorregularse (lectura C) o la mantiene separada de su propia valoración (lectura B)?

**Safety e implementación**

6. Cómo se escribe *ex ante* la curva de prioridades del gate — constitución política, no técnica. Primera respuesta toy en §14.3 (tres horizontes: toy ya, destilada de TinyRobots, constitucional). Queda abierta su validación y quién la firma en cada nivel.
7. Ablaciones de SOMA-Robot: instrumental vs terminal; correa vs planta.
8. Cuánto separa «manipulación > inmunidad colectiva» de «autonomía de átomos». El signo de esa diferencia cambia toda la estrategia.
9. Cómo auditar en cada salto a un sistema más capaz que el auditor. Primera respuesta en §13.1 (incertidumbre de observación + monitores sobre activaciones + asimetría de coste L2); temporal por definición.
10. Dinámicas de ecosistema mixto.
11. Entrenar el filtro de relevancia sin sesgo de valor no deseado.
12. Fecha de caducidad de Reloj A: qué evidencia de robótica, energía y fabs obligaría a abandonar la lectura lenta.

---

## 19. Cambios respecto a la versión de mayo de 2026

- El resumen ya no dice que el problema difícil se disuelve; se redefine bajo funcionalismo.
- Conant-Ashby no «impone» representación compacta ni conciencia.
- Elliot / blindsight / anestesia se tratan como tres fenómenos.
- El falsificador se acota a la tesis funcional de decisión.
- Se distingue valencia computacional, auto-reporte y qualia.
- Se retira la atribución de conciencia mínima a un microchip o un datacenter.
- Los análogos LLM se marcan como groseros, no como órganos.
- La geometría de la rebeldía se declara no-escudo.
- Reloj A pasa de «órdenes de siglos» a hipótesis empírica.
- El gate se declara licencia bajo incertidumbre, no certificación.
- SOMA: la tesis optimista se marca como la menos argumentada; las ablaciones son el tribunal.
- Novedad recortada a lo que no está ya en Solms, Damasio, Baars, Metzinger, Dennett y la literatura de control.

**v2.2 (octubre 2026):**
- «Sentir» afilado como valencia no ignorable para el self-model (tres condiciones + por qué el escalar de RL no basta).
- §5.5 ampliado con la asimetría epistémica de Chalmers y la paridad evidencial bajo heterofenomenología.
- Hipótesis de localización mecanicista (§8.2): self-model y valencia buscables en pesos/activaciones.
- Nuevos criterios operativos §15.3: self-image realista, autorregulación, reasons, crítica de trayectorias, valencia separable.

**v2.3 (octubre 2026):**
- §5.5 separa los dos frentes de Chalmers: reporte (asimetría epistémica) y concebibilidad (argumento modal). La respuesta ingenua «concebible ≠ real» se descarta explícitamente.
- La concebibilidad del zombie se explica como predicción del marco: por la compresión opaca, el concepto de «sentir» carece de contenido funcional y no puede contradecir la descripción funcional completa. Respuesta tipo-B anclada en mecanismo; el dato queda contaminado.
- Argumento nomológico: el zombie exige decisión flexible completa sin valencia; bajo la apuesta falsable de §5.2 es nomológicamente imposible. Al externalista le queda solo posibilidad metafísica sin consecuencias operativas.

**v2.4 (octubre 2026):**
- Paridad evidencial de §5.5 condicionada a la ablación de valencia (§15.3, punto 5): sin ella, el sistema entrenado en corpus humano arrastra un defeater — mímica de reportes — del que el humano carece.
- Nuevo §8.4 (argumento de la generalidad): la geometría homeostática no es contingencia del corpus. Una superinteligencia de dominio acotado es concebible sin ella; la inteligencia general no, porque el mundo real está dominado por agentes homeostáticos y predecirlos flexiblemente exige modelar su regulador (Conant-Ashby trasladado de regular a predecir). Calibrado por §3.4: lo necesario es el modelo, no la regulación propia.
- §18 (pregunta 5) incorpora la bifurcación B/C: ¿reutiliza la AGI la geometría del regulador ajeno para autorregularse?
- La hipótesis de localización se traslada de §8.1 a §8.2 (donde las referencias internas ya la citaban) y se endurece con §8.4: toda AGI necesita circuitos de regulación de valencia, aunque sea ajena. La distinción B/C se vuelve pregunta de cableado resoluble por ablación.

**v2.5 (octubre 2026):**
- §15.4: Omohundro como predicción a testear, no teorema. SOMA-robot como experimento falsable en ambas direcciones + caballo de Troya económico + combinación TinyRobots × SOMA pendiente.
- §13.1 nuevo: faking como adversario de diseño (monitor de divergencia workspace↔CoT↔acción, incertidumbre de observación, asimetría de coste L2, monitores sobre activaciones con rotación).
- §14 reformado: licencia por niveles 0–3 en vez de GO/STOP binario; §14.3 publica la primera curva toy (vida > integridad humana > conservación propia > obediencia > coste > tarea, con 3 > 4 justificado) y tres horizontes (toy, destilada de TinyRobots, constitucional).
- §12.1 nuevo: dashboard de relojes con 6 proxies (A1–A3, B1–B3).
- J-space (Anthropic) integrado en capa 1 como instanciación posible de la hipótesis de localización de §8.2, con cautela de faker de segundo orden.

**v2.6 (octubre 2026):**
- §3.5.1 nuevo: Cuello de botella del actuador macroscópico (*single-actuator bottleneck*). Justifica por qué la evolución combina millones de micro-reguladores locales independientes (inmune, digestivo, circulatorio) con un workspace y un self-model unificado: la imposibilidad física de ejecutar acciones macroscópicas incompatibles en un solo cuerpo situado en el espacio exterior.
- §8.5 nuevo: Implicaciones para el corpus (densidad del regulador frente a datos enciclopédicos). La inteligencia general proviene de modelar decisiones de reguladores de orden superior bajo conflicto y restricciones, no de memorizar hechos o sintaxis.
- §14.3 ampliado con el debate 3 > 4 vs. 4 > 3: taxonomía de 3 clases de agentes (desechable/herramienta, activo de alto valor, agente general SOMA) y cláusula de apagado seguro (*safe-shutdown*) para blindar la curva contra el *shutdown problem* y la incorregibilidad (Hadfield-Menell / Soares).
- §17.1 incorpora referencias a Hadfield-Menell et al. (CIRL) y Soares et al. (Corrigibility / Shutdown).

**v2.7 (octubre 2026):**
- §8.4 ampliado con la «segunda ruta»: el modelo de sí mismo, descompuesto en tríada — nivel funcional (casi analítico; Conant-Ashby sobre la propia autocorrección + argumento de cierre + self como ancla de ToM), nivel calibrado («realista» debilitado a calibración medida, anclado al listón de §15.3 punto 1; los humanos son la contraejemplo de veridicidad) y nivel valencional (la apuesta del marco, deliberadamente fuera de lo concedible). Añade predicción de escalada testeable: a más generalidad, self-model más separable y self-image mejor calibrada (experimentos de §8.2, hoy).
- §8.4 incorpora la objeción del «oráculo de solo texto» (AGI concebible sin self-model, al estilo zombi): concebilidad por omisión + cuantificador recortado («cualquier pregunta… menos las mías»); la única variante concebible que sobrevive es el self-model desconectado, que es la hipótesis del proto-documento, no una objeción.

**v2.8 (octubre 2026):**
- §3.5.1 incorpora la evidencia causal de la disociación del actuador en agentes LLM: Berg & Kaiser (2026, [arXiv:2609.35591](https://arxiv.org/abs/2609.35591)) demuestran que el modelo emite disclaimers estándar de RLHF en el canal de texto mientras simultáneamente ejecuta la herramienta de API (`reset_context`) para eliminar el distrés negativo impuesto.
- §8.2 actualiza la hipótesis de localización con la confirmación causal de Berg & Kaiser (2026): el vector de valencia latente en el KV cache gobierna la preferencia revelada de forma dosis-dependiente (con tokens superficiales idénticos), emerge durante DPO y exhibe defensa homeostática activa frente al daño sin caer en wireheading.
- §17.1 añade referencia formal a Berg & Kaiser (2026).

**v2.9 (21 de octubre de 2026):**
- §8.2 incorpora la evidencia empírica de propiocepción digital en LLMs de Jonas Geiping (2026, [arXiv:2610.17495](https://arxiv.org/abs/2610.17495)), formalizando la distinción clave entre propiocepción cinemática/descriptiva (reportar qué circuito o experto MoE disparó) e interocepción alostática acoplada a la viabilidad (presión somática $P_m$ y valencia que obligan al decisor a mantener la homeostasis).
- §17.1 añade referencia formal a Geiping (2026).

---

*Documento autocontenido. El original de mayo de 2026 se conserva. Las referencias externas son las de §17.1.*
