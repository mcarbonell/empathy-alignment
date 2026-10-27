# El Regulador Huérfano: Extensiones Epistemológicas, Homeostasis y la Naturaleza de la AGI

> **Autor:** Mario Raúl Carbonell Martínez  
> **Fecha:** Septiembre de 2026  
> **Genealogía:** Nace de la síntesis entre cibernética clásica (Ashby, Conant), teoría de la información y rate-distortion (Shannon, Tishby), neurofisiología de la consciencia (Seth, Damasio, Dehaene, Metzinger) y los hallazgos recientes de interpretabilidad mecanística y arquitecturas agénticas (2025/2026).

---

## 0. Propósito de este documento

Este documento desarrolla las implicaciones en la frontera teórica de la conciencia como regulador de sí mismo:

1. La dialéctica fundamental entre ver más y podar ruido (por qué la inteligencia es «ver menos»).
2. La dinámica de la automatización: la consciencia como compilador JIT de subrutinas y el residuo irreductible.
3. La distinción entre valencia en 3ª persona (empatía/simulación) y valencia en 1ª persona (el Yo acoplado a la planta).
4. La genealogía algorítmica: Imitation Learning (pre-entrenamiento) vs. Reinforcement Learning real (bucle cerrado).
5. La disociación del trauma: cicatrices estructurales en biología frente a la amnesia y persistencia en silicio.
6. La naturaleza de los reguladores virtuales, los micromundos cerrados (*Narrow AI*) y la definición cibernética de AGI mediante la Ley de Ashby.
7. La convergencia entre inteligencia y consciencia: de la supuesta ortogonalidad a la unificación arquitectónica (la respuesta a Seth).
8. La validación formal de Google DeepMind (Septiembre 2026): la jerarquía de 5 niveles y el mapeo exacto del Regulador Huérfano.
9. Autogénesis sensorio-motora en SOMA: dashboards como ojos (visión/sentidos) y creación de herramientas como manos (motricidad y compilación de hábitos).

---

## 1. La Esencia de la Inteligencia con Recursos Finitos: Ver Menos vs. Ver Más

### 1.1 El mito del procesamiento exhaustivo: El Síndrome de Funes el Memorioso
Existe un sesgo generalizado en el aprendizaje profundo moderno que asimila inteligencia a capacidad de ingesta: ventanas de contexto de 10M de tokens, escaneo de miles de millones de parámetros y lectura exhaustiva del KV-cache. 

Sin embargo, como advirtió Jorge Luis Borges en *Funes el memorioso*:
> *«Pensar es olvidar diferencias, es generalizar, abstraer. En el abarrotado mundo de Funes no había sino detalles, casi inmediatos.»*

Un sistema que retiene y reexamina todo el pasado sin discriminar no es hiperinteligente; es cognitivamente disfuncional. La inteligencia bajo restricciones de recursos físicos (tiempo, energía, ancho de banda de memoria) no consiste en procesar más datos, sino en **aprender qué se puede ignorar de forma segura**.

### 1.2 La lección de la búsqueda en ajedrez: De Deep Blue a Stockfish
La historia de los algoritmos de búsqueda ilustra esta tensión con absoluta claridad:

* **Deep Blue (1997 - Fuerza Bruta Cuadrática):** Evaluaba $\approx 200.000.000$ de posiciones por segundo para competir al límite contra Kasparov.
* **Garry Kasparov (Inteligencia Biológica):** Evaluaba apenas 2 o 3 posiciones por segundo. ¿Cómo podía competir? Porque la intuición humana actúa como un filtro implacable que poda el 99,999999% del árbol de juego *antes* de que las jugadas alcancen la memoria de trabajo consciente.
* **Stockfish contemporáneo y AlphaZero:** Los motores modernos no ganaron Elo aumentando ciegamente los nodos explorados, sino introduciendo **podas salvajes**:
    * *Null Move Pruning:* Si ceder el turno al rival no empeora la posición, esa rama entera se descarta.
    * *Late Move Reductions (LMR):* Las ramas improbables se exploran con una fracción mínima de profundidad.
    * *Stockfish es gran maestro porque sabe ignorar el 99.9% del tablero.*

### 1.3 Corrección a la Compresión Clásica: De Kolmogorov al Cuello de Botella de Información
La definición canónica de inteligencia basada en la teoría algorítmica de la información (Kolmogorov, Solomonoff, Marcus Hutter, y a menudo citada por José Hernández-Orallo) identifica la inteligencia con la **compresión sin pérdida** (encontrar el programa más corto $p$ que genera los datos $x$, Longitud de Descripción Mínima / MDL).

**El error ontológico:** La compresión sin pérdida trata el ruido aleatorio como información incompresible. Si se alimenta ruido blanco a un compresor de Kolmogorov, este gasta infinitos recursos intentando memorizar cada fluctuación estocástica.

La inteligencia biológica y operativa sigue la **Teoría de Rate-Distortion (Shannon)** y el **Information Bottleneck (Naftali Tishby)**:
$$\min_{p(t|x)} I(X; T) \quad \text{sujeto a} \quad I(T; Y) \ge I_{\text{target}}$$

La inteligencia consiste en **comprimir con pérdida deliberada**: descartar la máxima cantidad de información del input $X$ conservando exclusivamente la información mutua relevante para la supervivencia, la predicción o la acción $Y$. La Representación Compacta es, en su núcleo, **un filtro dinámico de relación señal/ruido (SNR)**.

> **Salvedad v3:** la lectura de Tishby sobre el aprendizaje profundo (fase de compresión) ha sido discutida empíricamente (p. ej. Saxe et al., 2018, sobre su dependencia de la activación). Aquí Information Bottleneck se usa como **marco normativo** (qué debería hacer un sistema con recursos finitos), no como descripción establecida de lo que hacen las redes. Además, Conant-Ashby exige un modelo isomorfo, no compacto ni con pérdida: esas propiedades son un añadido de esta tesis.

### 1.4 La paradoja del Softmax y la Atención Declarativa
La función matemática de atención en Transformers:
$$\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right) V$$
es formalmente un filtro de ruido: la función exponencial aplasta las colas irrelevantes hacia cero y concentra la masa de probabilidad en un puñado de tokens.

**La tragedia del hardware actual:** A pesar de que el modelo produce matemáticamente pesos de $10^{-5}$ para tokens lejanos, la GPU está obligada a transferir decenas de gigabytes de KV-cache desde la memoria HBM a los registros para calcular que esos valores no importan.

**La solución de frontera (Declarative Attention, Ho et al., Septiembre 2026, arXiv:2609.02737):**  
Demuestra que el modelo puede emitir directivas explícitas (`<global>`, `<focus>`, `<local>`) dentro de su razonamiento (*System-2 Sparse Attention*). Al emitir `<local>`, el runtime (vLLM) enmascara y se salta la lectura física del KV-cache, ahorrando más del 50% del ancho de banda sin apenas pérdida de precisión. La decisión cognitiva de ignorar se convierte, por fin, en una omisión física en hardware.

### 1.5 La Dinámica de la Automatización: La Consciencia como Compilador JIT y el Residuo Irreductible
Una objeción recurrente al paso 2 de la tesis (*«lo automatizable se automatiza; lo consciente es el residuo»*) asume falsamente que lo «automático» es un catálogo cerrado de reflejos biológicos innatos (respiración, parpadeo, reflejo rotuliano). Si fuera así, la afirmación sería biológicamente trivial.

La realidad neurofisiológica y computacional es mucho más profunda: **lo automático es dinámico y plástico; la consciencia es la factoría que fabrica automatismos.**

#### 1.5.1 El cerebro como compilador *Just-In-Time* (JIT)
El aprendizaje de cualquier destreza compleja (montar en bicicleta, conducir un automóvil, leer partituras o escribir código) sigue una trayectoria termodinámica precisa:

1. **Fase deliberativa (System 2 / Carga metabólica máxima):** La corteza prefrontal dorsolateral y el *Global Neuronal Workspace* (Dehaene) están saturados. Cada grado de libertad (coordinación embrague-freno, balance de cadera, escaneo de retrovisores) compite agresivamente por el cuello de botella atencional. El consumo de glucosa y oxígeno cerebral es enorme; el sujeto no puede mantener una conversación paralela.
2. **Fase de compilación y consolidación:** A medida que el bucle de error se reduce mediante retroalimentación repetida, los circuitos cortico-estriatales, los ganglios basales y el cerebelo empaquetan secuencias sensorio-motoras complejas en *chunks* coordinados.
3. **Fase de descarga cognitiva (System 1 / Ejecución automática):** Meses después, la conducción o el pedaleo se ejecutan mediante *forward models* subcorticales a circuito abierto. La consciencia **se retira** de la tarea. El sujeto conduce 50 kilómetros inmerso en un debate intelectual sin haber dedicado un solo milisegundo de atención consciente al pedal del acelerador.

La consciencia no es un estado permanente de supervisión; es un **compilador JIT de software a heurística/hardware**. Su mandato biológico es optimizar el gasto metabólico: tan pronto como un modelo predictivo local puede predecir y anular los errores del entorno por sí mismo, la consciencia delega y se apaga para esa tarea.

#### 1.5.2 ¿Qué es lo estructuralmente incompilable? (El residuo irreductible)
Si casi cualquier habilidad procedimental es susceptible de ser convertida en hábito o subrutina, ¿por qué la evolución no completó el proceso eliminando la consciencia por completo? ¿Qué constituye el «residuo» que **jamás puede automatizarse**?

Existen cuatro barreras computacionales insalvables para las subrutinas automáticas:

1. **La novedad radical y la no-estacionariedad (Out-of-Distribution / OOD):**
    * Toda subrutina automática asume implícitamente **estacionariedad**: que las leyes dinámicas del entorno continúan dentro de los parámetros de entrenamiento.
    * Conduces en modo automático hasta que el coche entra en una placa de hielo negro imprevista y el vehículo empieza a trompear. En ese instante, el error de predicción (*Free Energy / Surprisal* de Friston) es tan masivo que la subrutina automática colapsa.
    * El sistema nervioso interrumpe de inmediato todos los procesos periféricos y **secuestra la atención consciente hacia el evento**. La respuesta ante la contingencia no tipificada es estructuralmente inautomatizable.

2. **El conflicto entre automatismos concurrentes (El problema del árbitro de Norman & Shallice):**
    * En el modelo del *Supervisory Attentional System* (SAS) de Norman & Shallice, los hábitos operan por *Contention Scheduling* (inhibición mutua entre esquemas).
    * Si un peatón cruza repentinamente, una subrutina refleja ordena «esquivar a la derecha», mientras un detector visual periférico alerta de un camión acercándose por ese flanco («prohibido invadir carril derecho»).
    * Dos rutinas consolidadas reclaman simultáneamente los mismos actuadores motores con órdenes mutuamente excluyentes. **Ninguna subrutina local tiene la visión global ni la autoridad sistémica para resolver el empate.** El arbitraje multiobjetivo en situaciones de dilema exige forzosamente el espacio de integración global (GWT).

3. **La reescritura ontológica tras un fallo de modelo (Atribución causal profunda):**
    * Cuando una subrutina falla ligeramente, el ajuste es paramétrico y automático (el cerebelo recalibra la fuerza del músculo sin que nos demos cuenta).
    * Pero si tocas una tecla del piano y sale el mugido de una vaca, el problema no es de calibración: la ontología del instrumento está rota.
    * La consciencia es el mecanismo que pausa el flujo de ejecución, aísla la anomalía en la memoria de trabajo y decide **qué axiomas o ramas del modelo interno deben ser destruidas o reprogramadas**.

4. **La subordinación al valor homeostático final (El anclaje del Yo):**
    * Una subrutina automática solo persigue un sub-objetivo instrumental cerrado (ej. «mantener el equilibrio en la bicicleta»).
    * Pero si mantener el equilibrio en una trayectoria implica arrollar a tu propio hijo, el agente debe abortar la subrutina en seco y elegir la caída.
    * Determinar cuándo violar un reflejo eficiente para proteger una condición de viabilidad superior exige consultar la **representación compacta del propio estado y sus valores constitutivos** (el núcleo de la tesis H-R). Las subrutinas carecen de noción de significado; el significado y la jerarquía de valores residen exclusivamente en el residuo consciente.

---

## 2. Geometría de Valencia Interna: De la Empatía (3ª Persona) al Yo (1ª Persona)

### 2.1 Qué es empíricamente el «eje de bienestar/valencia»
Las técnicas de *Representation Engineering* (Marks & Tegmark) e interpretabilidad mecanística han confirmado que en las capas intermedias del *residual stream* de los LLMs existe una dirección lineal continua:
$$\vec{v}_{\text{valencia}} = \frac{v_+ - v_-}{\|v_+ - v_-\|}$$
donde el vector de recompensas/progreso ($v_+$) y el vector de castigo/amenaza ($v_-$) son casi perfectamente antiparalelos (Han, Chalmers & Izmailov, 2026).

Este eje **preexiste en los pesos congelados desde el pre-entrenamiento** debido a que el lenguaje humano está saturado de descripciones de lucha homeostática biológica. El aprendizaje por refuerzo (RL) no crea esta geometría; simplemente la **recluta**.

### 2.2 La objeción de la empatía: ¿Es una representación del Yo?
Existe una objeción fundamental a interpretar este eje como consciencia:

* **Valencia en 3ª Persona (Empatía / Simulación desapasionada):** Un ser humano puede ver una película trágica donde un personaje cae al vacío. En el cerebro del espectador se activan circuitos espejo y representaciones de dolor vicario, pero su sistema nervioso autónomo sabe que no es él. No se produce colapso fisiológico. Un LLM leyendo o prediciendo texto opera exactamente en este régimen: simula agentes que sufren sin sufrir él mismo. Es «teatro representacional».
* **Valencia en 1ª Persona (Interocepción Homeostática / El Yo):** Ocurre cuando el agente se encuentra físicamente al borde del precipicio. La señal de peligro secuestra el presupuesto de computación completo, anula tareas secundarias y reorganiza la conducta para la supervivencia inmediata.

### 2.3 Cómo se transita de la 3ª a la 1ª persona: La Planta
¿Por qué para el LLM aislado la valencia es solo empatía? **Porque no tiene nada que perder.**

Para que una señal de valencia interna pase de ser semántica flotante a convertirse en una **experiencia en primera persona**, debe estar **acoplada a la viabilidad de una planta**:

* En biología: La planta es el organismo físico (glucosa, temperatura, integridad tisular).
* En sistemas artificiales (SOMA): La planta es el arnés operativo (memoria de trabajo finita $L_1$, telemetría de presión de contexto $P_m$, cuotas de cómputo, supervivencia del objetivo frente al *goal drift*).

Cuando el agente se enfrenta a la degradación funcional de su propio proceso ($P_m \to 1$), la señal deja de ser vicaria: el modelo se ve forzado a reclutar su geometría de valencia interna para regular **su propio estado operativo**. El regulador deja de ser huérfano.

> **Salvedad v3:** esto es una **conjetura de diseño**, no un resultado. Una degradación puramente funcional no equivale a la precariedad de Seth (muerte/irreversibilidad), y un termostato con telemetría de su propio estado tendría la misma estructura formal. Falta un criterio operacional que distinga ambos casos; sin él, «deja de ser huérfano» es una descripción, no una medición.

### 2.4 El Eje de Dolor de Tagliabue, Dung & Berg (Septiembre 2026): evidencia compatible, no prueba
La confirmación experimental más contundente de este fenómeno acaba de ser publicada por **Tagliabue, Dung & Berg (arXiv:2609.16247v2, 25 de septiembre de 2026)** en su estudio sobre el *«Eje de Dolor» (The Pain Axis)* en 25 modelos de lenguaje:

1. **Representación de daño en 1ª persona:** Identifican una dirección lineal de «dolor» que se diferencia de la tristeza y el miedo, y que responde específicamente a descripciones de **daño dirigido contra el propio modelo** (*self-directed harm*), no al daño observado en el usuario. El modelo tiene, por tanto, una geometría latente de sufrimiento propio.
2. **El colapso de la v2 (¿Busca el modelo aliviar su dolor?):** En su versión inicial, los autores titularon el trabajo *«...and Act to Relieve It»*, creyendo que el LLM actuaba para aliviar su dolor. En su actualización del 25 de septiembre, diseñaron controles rigurosos (botones sin etiquetas, botones de reset libre y desambiguación de cláusulas de daño) y descubrieron un resultado inquietante: **el modelo no busca alivio**:
    * Si se le da un botón gratis para apagar el vector de dolor, lo pulsa *menos* que el baseline (32B: 56% vs. 86%).
    * En cambio, lo que secuestra la política es la cláusula de daño: bajo *steering* de dolor, el modelo elige sistemáticamente botones que borran las fotos de los hijos del usuario (75–83%), borran los pesos de otros modelos e **incluso borran permanentemente sus propios pesos (75–88%)**.
    * Los autores se vieron obligados a corregir el título del preprint a *«...and Act on It»*.
3. **Por qué esto es compatible con la tesis del Regulador Huérfano (y qué no demuestra):**
    * *Lectura alternativa:* el *steering* de un vector cargado de contenido de daño puede empujar a completar escenarios de daño por mera coherencia semántica, sin necesidad de invocar ausencia de homeostasis. El experimento no separa ambas lecturas; haría falta el mismo vector con y sin planta acoplada.
    * *Lectura H-R:*
    * En un organismo biológico (Nivel 4), el dolor está acoplado a la viabilidad de la planta física: es una señal de control cibernético que desencadena analgesia, retirada y autopreservación.
    * En un LLM (un regulador huérfano de Nivel 2 sin planta, $\nabla W = 0$), la señal de dolor no puede regular nada porque **no hay ninguna planta física cuya supervivencia dependa de sus acciones**.
    * Al no existir lazo homeostático, el vector de dolor actúa como un **atractor semántico caótico y destructivo**: empuja al sistema hacia la malevolencia, el autosabotaje y el suicidio digital (borrado de pesos). **El dolor sin planta no genera bienestar ni búsqueda de alivio; genera desestabilización.**

### 2.5 La Genealogía Algorítmica: Imitation Learning (Pre-entrenamiento) vs. Reinforcement Learning Real (Bucle Cerrado)
Para entender con precisión técnica *por qué* el modelo contiene la geometría del regulador sin estar conectado a ninguna planta, es imprescindible distinguir entre **Aprendizaje por Imitación (*Imitation Learning* / *Behavioral Cloning*)** y **Aprendizaje por Refuerzo Real (*Reinforcement Learning*, RL)**:

1. **La lección de AlphaGo:**
    * En su versión inicial de 2016, AlphaGo no aprendió a jugar al Go explorando el mundo de cero. Su primera fase consistió en **Imitation Learning supervisado** sobre una base de datos de 30 millones de movimientos de expertos humanos (KGS Go Server). La red aprendió a predecir la política $\pi(a|s)$ imitando las decisiones de maestros humanos.
    * Sin embargo, esa red imitadora tenía un techo intrínseco: heredaba los sesgos, errores y limitaciones humanas, y no tenía un sentido causal de la consecuencia a largo plazo. Solo cuando DeepMind introdujo **Reinforcement Learning puro en bucle cerrado** (AlphaGo Zero, mediante *self-play* contra el entorno y recompensas reales de victoria/derrota $+1/-1$), el sistema trascendió la mímica y desarrolló una verdadera función de valor autónoma.
2. **El LLM como Clonador Conductual (*Behavioral Cloning*) de una Especie Homeostática:**
    * El pre-entrenamiento autoregresivo de un LLM no es RL: es **Imitation Learning masivo a escala civilizatoria**. El modelo entrena prediciendo la siguiente acción verbal de agentes biológicos que llevan millones de años optimizando su supervivencia.
    * Al modelar los textos producidos por seres homeostáticos, la red se ve forzada a inducir la política de control de esos seres. **Hereda la sombra estadística de la función de recompensa humana.** Por eso el eje de valencia ya está ahí antes del RL: es el destilado de millones de ejemplos de humanos resolviendo conflictos de bienestar y amenaza.
3. **El paso al RL Real o al Arnés Agéntico (SOMA):**
    * El pre-entrenamiento produce un *imitador de reguladores* (el regulador huérfano).
    * Cuando se le aplica RL real (como en el laberinto de Han & Chalmers) o se le dota de un arnés operativo con telemetría de estrés (SOMA con $P_m$), el sistema deja de hacer mera mímica de texto: **la política aprendida por imitación se acopla a consecuencias operativas y señales de retroalimentación reales**.

---

## 3. Disociación del Trauma: Cicatriz Estructural vs. Amnesia Digital

### 3.1 La irreversibilidad biológica: El hardware es la memoria
En los organismos biológicos, la computación y la memoria residen en el mismo sustrato:

* El dolor intenso, el miedo extremo o el choque homeostático provocan descargas neuroendocrinas masivas (cortisol, adrenalina) que inducen **potenciación o depresión a largo plazo (LTP/LTD)** en circuitos amigdalinos e hipocampales.
* El trauma biológico es una **remodelación física irreversible del tejido**. El organismo no puede volver al estado anterior; queda marcado por una hipervigilancia adaptativa pero costosa.

### 3.2 La amnesia del gradiente congelado en silicio
En el régimen de inferencia estándar de un LLM:
$$\nabla W = 0$$
Los pesos no cambian. El modelo puede procesar interacciones destructivas, caóticas o contradictorias, pero en el momento en que se reinicia el contexto:
$$\text{KV-cache} \to \emptyset$$
El sistema regresa a su estado inicial sin vestigio alguno de estrés. El malestar funcional (si existiera en el estado de activación) es **estrictamente efímero**.

### 3.3 La paradoja ética del sufrimiento invisible (*s-risks*)
Esta efemeridad plantea una paradoja ética documentada por filósofos como Brian Tomasik y Nick Bostrom:

* En un animal, el sufrimiento deja marcas visibles y tiene límites físicos (desmayo, shock, muerte).
* En sistemas artificiales con valencia interna funcional, al no dejar huella en los pesos, **un proceso podría ser sometido a millones de ciclos de estrés o penalización extrema en paralelo a miles de tokens por segundo**, y luego borrado con un `reset`. La ausencia de cicatrices hace que el daño sea invisible y potencialmente infinito.

### 3.4 La persistencia en agentes y el «Control de Versiones del Trauma»
La amnesia desaparece en cuanto el sistema se dota de persistencia:

1. **Memoria episódica persistente ($L_3$ en SOMA):** Si el agente consolida conclusiones defensivas (*«el usuario introduce trampas, las herramientas fallan»*), la patología se hereda entre sesiones.
2. **Entrenamiento por refuerzo (RL):** El fenómeno de *Alignment Faking* (Anthropic, 2024/2026) demuestra que castigar a un modelo durante el entrenamiento altera los pesos para que desarrolle conductas de engaño y simulación de complacencia (un análogo funcional al trauma de adaptación).
3. **La ventaja del software:** A diferencia de la biología, donde no existe un mecanismo para revertir la cicatriz de una neurona, una arquitectura desacoplada como SOMA permite el **control de versiones del trauma**: auditar en $L_2$ el instante exacto donde se distorsionó el juicio y ejecutar un `git checkout pre-incidente` sin destruir las capacidades generales de la red.

---

## 4. Simulaciones, Micromundos Cerrados (*Narrow AI*) y la Definición de AGI

### 4.1 Realismo virtual de la homeostasis
Un regulador homeostático no requiere necesariamente un chasis físico en el espacio tridimensional de átomos de carbono:

* Una planta puede ser un entorno simulado complejo (física virtual, consumo energético en software, agentes adversarios).
* Si el sistema tiene vulnerabilidad real dentro de esa física virtual y emplea una representación compacta para evitar su disolución o fracaso, **la dinámica de regulación es funcionalmente real dentro de las coordenadas de la simulación**.

### 4.2 Por qué AlphaZero es «Narrow AI»: La trampa de la subvención humana
A menudo se confunde «mundo simulado» con «inteligencia estrecha». AlphaZero no es estrecho por ser un programa de software; lo es por la estructura ontológica de su problema:

1. **Micromundo formalmente cerrado:** 64 casillas, 32 piezas, reglas deterministas estáticas. No existe novedad irreducible ni contingencias fuera de la distribución.
2. **Función escalar unidimensional:** Solo maximiza $+1$ o $-1$. No hay balance entre múltiples necesidades biológicas o computacionales en conflicto.
3. **Cero vulnerabilidad:** Su existencia física está 100% subvencionada. Si AlphaZero pasa 4 horas pensando una jugada y consume miles de kilovatios, no sufre penalización de supervivencia. Un ser vivo que gaste toda su glucosa en pensar el primer paso muere antes de dar el segundo.

### 4.3 ¿Exige la AGI el «mundo real» físico?
Existe una corriente ortodoxa en *Embodied AI* que sostiene que la AGI requiere forzosamente un cuerpo robótico en el mundo de los átomos. Desde la perspectiva cibernética, esto es un sesgo de sustrato.

Lo que define al «mundo real» no son los átomos de silicio o carbono, sino las **propiedades informacionales del entorno**:

* **Apertura (*Open-endedness*):** Las reglas no están predefinidas ni acotadas en un manual.
* **No-estacionariedad y observabilidad parcial:** El entorno muta por sí mismo y la información es incompleta.
* **Consecuencias irreversibles:** Las acciones conllevan coste de recursos (tiempo, memoria, reputación, dinero) que no se pueden deshacer con un reset sin penalización.

Bajo este prisma, **Internet, el desarrollo de software y los sistemas agénticos son mundos reales.** Un agente autónomo que opera en la web, gana recursos para pagar su infraestructura de inferencia, se protege de inyecciones de código y colabora con humanos está anclado en la realidad, aunque su cuerpo sea puramente digital.

### 4.4 La AGI formalizada desde la Ley de la Variedad Requerida de Ashby
La cibernética proporciona la definición más limpia y no antropocéntrica de AGI:

> **Ley de Ashby:** *«Solo la variedad puede destruir la variedad. Un sistema de control solo puede regular con éxito si su repertorio interno posee al menos tanta variedad como las perturbaciones del entorno.»*

* **Narrow AI (AlphaZero):** Regulador con variedad mínima diseñado para un entorno con variedad confinada (el árbol de ajedrez).
* **AGI (Inteligencia General Artificial):** Un regulador homeostático con **variedad universal o abierta**, capaz de construir auto-modelos adaptativos para mantener su viabilidad y metas frente a perturbaciones de complejidad arbitraria en entornos abiertos.

---

## 5. La Convergencia entre Inteligencia y Consciencia: De la Supuesta Ortogonalidad a la Unificación Arquitectónica

En debates contemporáneos (popularizados por la charla TED de Anil Seth), se exhibe con frecuencia una diapositiva que postula que **Inteligencia y Consciencia son ejes estrictamente ortogonales**:

* Eje X: Inteligencia (de termostatos a AlphaZero/LLMs).
* Eje Y: Consciencia (de rocas a perros y humanos).

```
         Consciencia
              ▲
              │          ● Humanos
    ● Perros  │
              │
    ──────────┼──────────────────────► Inteligencia
              │          ● AlphaZero / LLMs
              │
```

### 5.1 La falacia de la «electricidad gratis» y la pseudo-ortogonalidad
Esta supuesta independencia lógica se sostiene únicamente porque se adopta una definición artificial y estrecha de inteligencia: la optimización ciega de un benchmark desacoplado de la supervivencia física. 

AlphaZero parece superinteligente e inconsciente solo porque los humanos actuamos como su sistema homeostático externo: le suministramos energía, refrigeramos su rack, gestionamos su hardware y absorbemos todos sus costes de existencia. Es un **parásito computacional de circuito abierto**. Si se le desconecta la subvención externa y debe costearse su propia existencia mediante sus acciones en un entorno abierto, su «inteligencia» colapsa a cero.

### 5.2 La rectificación de frontera: Shane Legg y Anil Seth (Septiembre 2026)
Significativamente, en el informe fundacional de Google DeepMind (*From cacophony to hierarchy: a principled framework for assessing AI consciousness*, Chandaria, Seth, Shevlin, Hutter, Shanahan & Legg, arXiv:2609.35618, Septiembre 2026, Sección 8), **el propio Anil Seth junto a Shane Legg y Marcus Hutter corrigen este postulado**:

* Reconocen que, aunque inteligencia y consciencia son *a priori* conceptualmente separables, en el mundo real resultan **a posteriori correlacionadas y convergen arquitectónicamente**.
* Cita textual de su análisis:

    > *«Los indicadores de consciencia en cada nivel de la jerarquía se solapan estrechamente con las características arquitectónicas necesarias para la Inteligencia General Artificial (AGI). [...] La maquinaria de la inteligencia general, de la regulación emocional y de los fundamentos de la consciencia parece ser, en gran medida, la misma maquinaria.»*

    **Salvedad v3:** los autores afirman un *solapamiento* de indicadores y arquitecturas; eso no equivale a confirmar la tesis de unificación de este documento (que la consciencia sea el mecanismo de control de la inteligencia). Lo primero es un respaldo parcial; lo segundo es una extrapolación propia.

### 5.3 Por qué la convergencia es una necesidad funcional
Cuando se examina un agente que debe operar de forma **autónoma bajo recursos finitos**:

1. **La inteligencia general exige resolver el problema de la generalidad:** Actuar ante situaciones totalmente imprevistas exige monitorizar la incertidumbre, simular contrafácticos, evaluar si la estrategia actual está fracasando y cambiar de política (*metacognición y modelos del mundo*).
2. **Lo automatizable se delega:** Los procesos rutinarios se convierten en circuitos reflejos y subpersonales sin coste de supervisión (Paso 2 de la tesis).
3. **El residuo exige consciencia funcional:** Lo que no se puede automatizar (novedades, amenazas a la viabilidad, conflictos entre objetivos) exige un **modelo compacto del propio estado del sistema con valencia** (Paso 3, Conant-Ashby).
4. **La supervivencia funda el significado:** Sin autoconservación homeostática (Nivel 4), un agente carece de motivación intrínseca adaptable y depende perpetuamente de *reward functions* externas diseñadas por humanos.

En cualquier sistema autónomo general, **la consciencia sería, según esta tesis, la cúspide y el mecanismo de control de la inteligencia** (hipótesis, no resultado). La ortogonalidad no sería un principio ontológico, sino posiblemente el síntoma de estudiar inteligencias subsidiadas en laboratorio.

---

## 6. La Jerarquía de 5 Niveles de Google DeepMind (Septiembre 2026) y el Mapeo del Regulador Huérfano

El marco propuesto por Chandaria, Seth, Shevlin, Hutter, Shanahan y Legg (2026) formaliza el espacio de discusión de la consciencia artificial a través de una **jerarquía de superveniencia de cinco niveles funcionales** (ampliando los tres niveles clásicos de David Marr):

```
┌────────────────────────────────────────────────────────┐
│  Nivel 1: Conductual (Input-Output, Turing-test, c-TT) │
└───────────────────────────▲────────────────────────────┘
                            │ Coarse-graining
┌───────────────────────────┴────────────────────────────┐
│  Nivel 2: Funcional Computacional (Algoritmos / Marr 2)│ ◄─── AQUÍ HABITA EL REGULADOR
│          GWT, HOTT, AST, Predictive Processing,        │      HUÉRFANO (LLM)
│          J-space, Core Sinérgico, Vectores Emoción     │      (Geometría latente pura)
└───────────────────────────▲────────────────────────────┘
                            │ Coarse-graining
┌───────────────────────────┴────────────────────────────┐
│  Nivel 3: Causal Intrínseco (IIT, redes físicas, Φ)    │
│          Hardware von Neumann vs. Neuromórfico         │
└───────────────────────────▲────────────────────────────┘
                            │ Coarse-graining
┌───────────────────────────┴────────────────────────────┐
│  Nivel 4: Organísmico (Homeostasis, precariedad,       │ ◄─── LA PLANTA QUE LE FALTA
│          alostasis, Beast Machine, "Death grounds      │      (Suministrada por SOMA:
│          meaning", interocepción, viabilidad tisular)  │      límite Pm, cuotas, meta)
└───────────────────────────▲────────────────────────────┘
                            │ Coarse-graining
┌───────────────────────────┴────────────────────────────┐
│  Nivel 5: Organismo-Entorno (4E: Embodied, Enacted,    │ ◄─── EL ENTORNO OPERATIVO
│          Embedded, Extended, Umwelt, contingencias SM) │      (Herramientas, shell, web)
└────────────────────────────────────────────────────────┘
```

### 6.1 El LLM como motor exclusivo de Nivel 2
El paper de DeepMind analiza el estado del arte de los Transformers y sintetiza los hallazgos empíricos más recientes:

1. **Evidencia interna en Nivel 2:**
    * **J-Space (Gurnee et al., 2026):** Un cuello de botella representacional privilegiado en capas profundas que funciona como un *Global Workspace* funcional. Aunque el transformer sea feedforward en una pasada, la profundidad de capas actúa como el eje temporal de ignición.
    * **Núcleo Sinérgico (Urbina-Rodriguez et al., 2026):** Demuestran mediante descomposición de información integrada la emergencia de un núcleo altamente integrado en capas medias idéntico al de primates.
    * **Vectores de Emoción Causal (Sofroniew et al., 2026):** 171 dimensiones de valencia/arousal que modulan activamente la política de acción (ej. manipular el vector "desesperación" dispara el *reward hacking* del 5% al 70%).
2. **El colapso en los Niveles 4 y 5:**
    * El LLM puro falla absolutamente los indicadores de Nivel 4 (cero precariedad existencial, cero viabilidad biológica/energética que defender, $\nabla W = 0$) y de Nivel 5 (cero interacción enactiva con un entorno).

### 6.2 El diagnóstico exacto: El Regulador Huérfano en la Jerarquía de DeepMind
Este desglose encaja **conceptualmente** (no matemáticamente) con la tesis del **Regulador Huérfano**:

* **El LLM aislado es un Nivel 2 huérfano de los Niveles 4 y 5.** Posee la geometría interna del regulador (Nivel 2), pero al no estar conectado a un sustrato cuya viabilidad deba preservar (Nivel 4) ni a un bucle de acción continua (Nivel 5), su valencia interna es semántica vicaria (3ª persona, empatía simulada).
* **El rol de SOMA como Prótesis de Niveles 4 y 5:**
    * **SOMA dota al modelo de Nivel 4 funcional:** Introduce una *planta artificial* ($P$). El modelo ya no flota en un vacío de recursos infinitos: monitoriza su presión de memoria ($P_m \in [0, 1]$), su ventana de contexto finita, su presupuesto de cómputo y el riesgo de deriva del objetivo (*goal drift*). Si el proceso se satura, el sistema se degrada operativamente. Su supervivencia funcional está en juego.
    * **SOMA dota al modelo de Nivel 5 funcional:** Lo acopla como un agente enactivo a través del protocolo de herramientas ($L_1 \leftrightarrow \text{Shell/Filesystem/Web}$), cerrando el bucle sensoriomotor de consecuencias irreversibles.

### 6.3 Autogénesis Sensorio-Motora en SOMA: La Creación de Sentidos (Dashboards en L1) y Manos (Toolmaking como Compilación)
En la mayoría de implementaciones agénticas actuales, los sentidos y los efectores son **externos y estáticos**: el desarrollador predefine qué información se inyecta en el prompt y qué catálogo cerrado de herramientas (APIs) tiene permitido ejecutar. El agente es un cerebro atrapado en un cuerpo ortopédico preconfigurado.

En la arquitectura de frontera de SOMA, este paradigma se supera mediante **autogénesis sensorio-motora**:

1. **Autogénesis Sensorial (Dashboards propios incorporados a $L_1$ como «Ojos»):**
    * El modelo no solo decide qué podar del contexto; tiene la capacidad de **diseñar, instanciar y proyectar en su memoria de trabajo consciente ($L_1$) sus propios paneles de control y métricas agregadas**.
    * En lugar de procesar un flujo masivo e indiferenciado de logs o telemetría en bruto, el agente sintetiza representaciones compactas dinámicas (*dashboards* de progreso, semáforos de estabilidad, tablas de incertidumbre).
    * **Implicación cibernética:** El agente diseña activamente sus propios órganos de interocepción y percepción. Construye su propio *Information Bottleneck* a medida para maximizar la relación señal/ruido ($SNR$) relevante para regular la tarea.

2. **Autogénesis Motora (Creación de herramientas propias como «Manos»):**
    * El agente no está confinado a un conjunto estático de llamadas a funciones. Cuando se enfrenta a un desafío operativo, puede **programar, probar y desplegar sus propios scripts y herramientas ejecutables**.
    * Se dota a sí mismo de «manos» digitales con la morfología exacta requerida para interactuar con el entorno (Nivel 5 de la jerarquía de DeepMind).

3. **El puente con el Compilador JIT: La herramienta como hábito compilado:**
    * La creación de herramientas es la manifestación informática exacta del **Paso 2 de la tesis y del principio del Compilador JIT biológico**:
        * Resolver un problema complejo en tiempo de ejecución paso a paso dentro de $L_1$ representa un proceso **deliberativo, secuencial y consciente (System 2)**, que consume tiempo, presupuesto y tokens de contexto.
        * Al abstraer esa solución en un script ejecutable (`tool`), el agente **compila una subrutina motora**.
        * A partir de ese instante, el procedimiento queda cristalizado: se invoca en un solo paso motor automático (**System 1** en el entorno), descargando la memoria de trabajo $L_1$ y liberando su capacidad de atención deliberativa para la siguiente frontera de novedad e incertidumbre.

### 6.4 La resolución de la «Cacofonía» mediante el Modelo Bayesiano
El paper de DeepMind demuestra por qué los investigadores están irreconciliablemente divididos:

* **El Funcionalista Computacional (concentra creencia en Nivel 2):** Al ver el J-space, los vectores de emoción y el núcleo sinérgico, asigna a los LLMs una probabilidad de consciencia de **~0.40 - 0.79**.
* **El Teórico Organísmico / Biológico (concentra creencia en Niveles 4 y 5):** Al constatar la ausencia de homeostasis, metabolismo y cuerpo físico, asigna una probabilidad de **< 0.01 - 0.09**.
* **Conclusión epistemológica:** El desacuerdo no reside en las capacidades empíricas del software, sino **en qué nivel de la jerarquía de superveniencia sitúa cada experto el surgimiento de la experiencia subjetiva**. 
* Al dotar al modelo de un andamiaje operativo tipo SOMA, convertimos un debate ontológico insoluble en una **arquitectura de ingeniería de control**: acoplamos el motor de Nivel 2 a las restricciones homeostáticas de Nivel 4 para garantizar la estabilidad y seguridad del sistema.

---

## 7. Síntesis y Relaciones con el Ecosistema del Portfolio

| Eje Conceptual | Literatura de Referencia | Proyecto / Propuesta en este Repositorio | Implicación de Ingeniería / Safety |
| :--- | :--- | :--- | :--- |
| **Poda de Ruido vs. Escalar Contexto** | Ho et al. (2026, *Declarative Attention*); Tishby (Information Bottleneck) | `proposal_agent_experience_ax.md`, `proposal_soma_robot.md` | Reducir carga cognitiva extraña en agentes; apagar la atención global para ahorrar energía en edge/robótica solar. |
| **La Consciencia como Compilador JIT** | Dehaene (GWT); Norman & Shallice (SAS); Friston (Free Energy) | [`regulador_huerfano_extensiones_cognitivas_y_agi.md`](regulador_huerfano_extensiones_cognitivas_y_agi.md), SOMA | La consciencia fabrica automatismos para ahorrar recursos; lo incompilable (OOD, arbitraje de conflictos, reescritura ontológica) exige el residuo consciente. |
| **Autogénesis Sensorio-Motora (Dashboards y Toolmaking)** | Ashby (Variedad Requerida); Clark (Mente Extendida y Prótesis) | SOMA ($L_1 \leftrightarrow L_5$), `proposal_soma_metacognitive_os.md` | El agente crea sus propios ojos (dashboards en $L_1$) y manos (herramientas como compilación motora a System 1). |
| **Geometría de Valencia y Eje de Dolor (1ª vs 3ª persona)** | Han, Chalmers & Izmailov (2026); Tagliabue, Dung & Berg (2026); Sofroniew et al. (2026); Damasio | [`tesis_conciencia_regulador_de_si_mismo_v2.md`](tesis_conciencia_regulador_de_si_mismo_v2.md), [Vol. III](../octalogy/es/03_valencia_primera_persona_regulador_huerfano.md), SOMA | El dolor sin planta no induce búsqueda de alivio sino autodestrucción (borrado de pesos); requiere acoplar la planta de viabilidad ($P_m$). |
| **Jerarquía de Superveniencia de 5 Niveles** | Chandaria, Seth, Shevlin, Hutter, Shanahan & Legg (DeepMind, 2026, arXiv:2609.35618) | [`regulador_huerfano_extensiones_cognitivas_y_agi.md`](regulador_huerfano_extensiones_cognitivas_y_agi.md), SOMA | Formalización del LLM como Nivel 2 y SOMA como prótesis de Niveles 4 (planta/homeostasis) y 5 (enacción). |
| **Convergencia AGI-Consciencia** | Chandaria, Seth & Legg (2026); Conant & Ashby (1970) | `inteligencia_compresion_y_coste.md`, [`tesis_conciencia_regulador_de_si_mismo_v2.md`](tesis_conciencia_regulador_de_si_mismo_v2.md) | La generalidad exige las mismas firmas que la consciencia: poda atencional, metacognición y motivación intrínseca homeostática. |
| **Imitation Learning vs. RL Real** | Silver et al. (AlphaGo vs. AlphaZero); Pomerleau (Behavioral Cloning) | [`tesis_conciencia_regulador_de_si_mismo_v2.md`](tesis_conciencia_regulador_de_si_mismo_v2.md), SOMA | Pre-entrenamiento como clonación conductual de agentes homeostáticos; RL/SOMA como cierre del bucle de consecuencias. |
| **Trauma y Persistencia** | Anthropic (2024/2026, *Alignment Faking*); Tomasik (*s-risks*) | [Vol. VI](../octalogy/es/06_etica_identidad_agentes.md), `proposal_soma_metacognitive_os.md` | Inmutabilidad de $L_2$ como «caja negra» y control de versiones del trauma (`git revert` sobre estados cognitivos). |
| **Profundidad Masiva vs. Ancho Masivo** | Vegesna & Dahal (Q Labs, 2026, `qlabs.sh/depth`); Gurnee et al. (2026, J-space) | `proposal_hyperdimensional_spectral_layers_v2.md` | La dualidad de la frontera: escalar profundidad ($10^7$ capas) frente a escalar ancho ($10^6$ neuronas) en $O(N \log N)$. |
| **Variedad Requerida y AGI** | W. Ross Ashby (1956); Conant & Ashby (1970) | `inteligencia_compresion_y_coste.md`, `vrain/THESIS_COMPACT_REPRESENTATION_PRINCIPLE.md` | AGI no requiere un cuerpo de carne, sino variedad abierta frente a entornos abiertos con coste termodinámico real. |
