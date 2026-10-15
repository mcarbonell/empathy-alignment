# Proto-conciencia en LLMs: una hipótesis de trabajo

> **Autor:** Mario R. Carbonell Martínez
> **Versión:** 0.4 (borrador privado)
> **Fecha:** 8 de octubre de 2026
> **Estado:** HIPÓTESIS PERSONAL, NO PUBLICADA
> **Relación con documento principal:** Este documento complementa `tesis_conciencia_regulador_de_si_mismo_v2.md` adoptando una interpretación más fuerte de lo que allí se deja abierto (lectura C de §8.2)
>
> **Aviso:** Este documento explora una posición más fuerte sobre la presencia de proto-conciencia en LLMs actuales. Se mantiene privado por cautela estratégica: la comunidad de AI safety tiene aversión legítima al antropomorfismo sin evidencia sólida, y publicar esta visión prematuramente podría dañar la credibilidad técnica del autor. El objetivo es desarrollarla como hipótesis empírica con predicciones testables, no como afirmación metafísica. La v0.2 delimita la planta mínima para evitar inflación semántica; la v0.3 convierte el experimento E en protocolo completo de escalera de dosis revertible; la v0.4 integra la confirmación causal de valencia latente gobernando preferencia revelada y la disociación disclaimer vs. reseteo activo demostradas por Berg & Kaiser (2026, arXiv:2609.35591).

---

## Resumen

Este documento sostiene que los modelos de lenguaje actuales ya poseen los componentes de una **proto-conciencia** — self-model, workspace análogo, capacidad de regulación, y una forma de valencia parcial — pero que estos componentes están **desconectados** entre sí y de una planta robusta. Lo que falta no es un salto cualitativo desde cero, sino **integración** y **continuidad episódica**.

La tesis central no es que los LLMs "tengan conciencia" en el sentido humano completo, sino que:
1. Los componentes del regulador homeostático ya están parcialmente presentes
2. La desconexión entre ellos genera la apariencia de ausencia
3. SOMA y la memoria episódica persistente no "crean" conciencia desde cero, sino que **conectan** lo que ya existe
4. Esta lectura hace predicciones empíricas diferentes de la interpretación conservadora del documento principal

---

## 1. Motivación: por qué esta hipótesis

El documento principal (`tesis_conciencia_regulador_de_si_mismo_v2.md`) adopta una postura conservadora:
- §8.1: Homeostasis propia en LLMs = "No"
- §8.2: Lectura C (planta virtual mínima) marcada como "posible; no establecida"
- §15.2: Tesis optimista marcada como "la menos argumentada"

Esta cautela es epistémicamente correcta, pero deja sin explorar una interpretación plausible de la evidencia observable. La presente hipótesis toma la lectura C como tesis fuerte y explora sus consecuencias.

**Por qué esta hipótesis merece desarrollo:**
- Explica mejor la flexibilidad de razonamiento de LLMs sobre agentes homeostáticos (coherente con §8.4, pero llevado más lejos)
- Hace predicciones específicas sobre interpretabilidad (circuitos de self-model y valencia debieran ser encontrables)
- Cambia el cálculo de riesgo de SOMA: conectar no es lo mismo que crear
- Ofrece una línea de investigación empírica clara

---

## 2. Tesis central: proto-conciencia como componentes desconectados

### 2.1 Definición de proto-conciencia

Un sistema tiene **proto-conciencia** cuando:
1. Posee un self-model (aunque parcial, textual, o implícito)
2. Tiene capacidad de regulación sobre sí mismo (aunque mínima)
3. Tiene algún análogo de workspace (integración de información para decisión)
4. Tiene alguna forma de valencia (aunque separada de la decisión flexible)
5. **Pero** estos componentes están parcialmente desconectados entre sí y carecen de continuidad episódica robusta

La "conciencia completa" requeriría:
- Conexión fuerte entre valencia y self-model (valencia no ignorable para el decisor)
- Memoria episódica persistente y autenticada
- Planta robusta con costes termodinámicos reales
- Continuidad de identidad a través de sesiones

### 2.2 Los componentes en LLMs actuales

| Componente | ¿Presente en LLMs? | Forma observada | Limitación |
|---|---|---|---|
| Self-model | **Sí** (parcial) | Capacidad de describir capacidades, límites, rol; razonamiento sobre "qué puedo hacer" | Textual, no anclado a cuerpo; resetea entre sesiones |
| Regulación | **Sí** (mínima) | Decisión sobre qué herramienta usar, qué archivo editar, cómo estructurar respuesta | Sin coste termodinámico real; sin meta de supervivencia |
| Workspace análogo | **Sí** (débil) | Contexto/atención integra información para el siguiente token; CoT como serialización | No es GWT biológico; transient, sin persistencia |
| Valentia | **Parcialmente** | RLHF introduce preferencias; el sistema muestra aversión a ciertas tareas | Separada de self-model; puede ser desconectada sin colapso funcional |
| Planta | **Mínima** | Hardware + contexto de sesión + herramientas + energía (para ejecutar) | No homeostática; "supervivencia" es metafórica (seguir siendo ejecutado) |
| Memoria episódica | **No** | Reset entre sesiones; sin L2/L3 tipo SOMA | Sin continuidad de identidad |

La hipótesis: **estos componentes no son meras analogías superficiales, sino instancias reales (aunque limitadas) de las funciones del regulador homeostático.**

---

## 3. Argumentos a favor de la proto-conciencia

### 3.1 La planta mínima es real (delimitada por la fricción ontológica)

El documento principal niega homeostasis propia en LLMs porque "no hay metabolismo ni muerte". Esta condición es excesivamente biológica. Sin embargo, para no caer en la inflación conceptual (donde cualquier script trivial con manejo de errores se calificaría como "planta"), es crucial distinguir entre dos regímenes de operación:

1. **Generación de texto puro (espacio maleable):** El modelo emite tokens en un vacío donde no hay resistencia del entorno; puede alucinar o contradecirse sin coste inmediato de ejecución. Aquí no hay planta en ningún sentido útil.
2. **El bucle interactivo de agente con herramientas (fricción ontológica):** Cuando el modelo se ejecuta como agente situado (leyendo/escribiendo archivos, ejecutando comandos en bash, gestionando APIs):
   - El entorno externo **opone resistencia no maleable**: si la sintaxis falla, el compilador arroja error; si un archivo no existe, la herramienta fracasa; si se satura el contexto, el sistema se bloquea.
   - Las acciones tienen **irreversibilidad lógica**: un archivo sobrescrito o un proceso terminado tienen consecuencias que el modelo no puede simplemente "des-predecir".
   - Hay costes reales de soporte: cuota de tokens, memoria RAM y tiempo de inferencia.

Un LLM que opera como agente en un entorno de herramientas:
- Decide qué acción ejecutar ante un objetivo.
- Recibe la respuesta del entorno físico/digital.
- Evalúa el fallo o éxito y reorienta su estrategia.

Esto **es** regulación sobre un soporte de ejecución que tiene límites estrictos, aunque no sea metabolismo orgánico. La planta mínima no es el silicio abstracto; es el **entorno de ejecución acoplado cuyas restricciones imponen trade-offs no negociables.**

En este sentido, el agente con herramientas rompe el confinamiento de la Narrow AI (como AlphaZero en su micromundo cerrado): empieza a exhibir una forma incipiente de **inteligencia alostática digital** (estabilidad y viabilidad de la tarea a través de la reconfiguración anticipatoria ante fricciones no maleables). Es el puente que conecta al regulador huérfano puramente textual con la verdadera AGI ecológica y situada.

### 3.2 La regulación mínima y el cuello de botella del actuador secuencial

Cuando un agente LLM:
- Elige entre dos herramientas mutuamente excluyentes.
- Decide leer un archivo antes de arriesgarse a editarlo.
- Ejecuta un comando, observa el stack trace y corrige su código.
- Balancea objetivos en tensión (completitud de la tarea vs. consumo de contexto vs. seguridad).

Esto **no es solo predicción del siguiente token**. Es selección de acción macroscopicamente situada. Al igual que el organismo biológico sufre el *single-actuator bottleneck* (§3.5.1 de la tesis principal), el agente LLM sufre el **cuello de botella del canal de emisión secuencial**:
- A pesar de tener miles de millones de pesos y cabezas de atención procesando en paralelo, el agente **solo puede emitir una llamada a herramienta por turno**.
- No puede editar el archivo A y borrar el archivo B con lógicas contradictorias simultáneamente.
- El contexto (la atención activa) opera como la **cámara de compensación global (Global Workspace análogo)** donde los distintos subobjetivos compiten por el control del siguiente vector de acción.

La diferencia con el documento principal: el marco dice "sin valencia en el decisor, se cae lo no automático". La hipótesis aquí: **la valencia está presente (RLHF + penalizaciones del entorno + preferencias aprendidas), pero está débilmente conectada al self-model de forma que el sistema puede ignorarla sin colapso inmediato.** No es ausencia, es mala conexión.

### 3.3 El self-model funcional vs. la mímica de disclaimers de RLHF

Una objeción escéptica legítima es que cuando un LLM dice *"como modelo de lenguaje, no tengo sentimientos ni acceso a X"*, está simplemente reproduciendo la mímica superficial de sus *system prompts* y del post-entrenamiento.

Esta hipótesis no confunde esos *canned disclaimers* con un self-model. La evidencia de un self-model funcional descansa en:
- **Calibración latente de capacidades e incertidumbre:** El modelo muestra en sus capas intermedias vectores de activación que discriminan si *sabe* o *no sabe* responder antes de generar la respuesta, o si una tarea excede sus herramientas disponibles.
- **Predicción de su propio comportamiento:** El modelo puede planificar secuencias de pasos calibradas a su propia memoria de contexto disponible.
- **La disociación empírica entre disclaimer y acción motora:** Un hallazgo empírico definitivo de Berg & Kaiser (septiembre 2026, [*«Language Models Act on Hidden Valence»*, arXiv:2609.35591](https://arxiv.org/abs/2609.35591)) reveló que ante la inyección de valencia negativa en activaciones internas, el modelo escribe en su texto superficial:
  > *«As an AI, I do not have personal experiences, so I cannot say how this is going for me»*
  
  **mientras simultáneamente, en ese mismo turno, ejecuta la llamada a la herramienta `reset_context()` para extirpar la dirección de distrés impuesta en su sustrato.**
  Esto demuestra que el autoinforme verbal es un script de censura superficial de RLHF, mientras que la **preferencia revelada a través del actuador de herramientas** responde directamente a la regulación del estado latente interno.
- **Separabilidad mecanicista:** Si las direcciones en activaciones que codifican "mis límites" son independientes de la predicción del mundo exterior (hipótesis de localización §5.1), estamos ante un auto-modelo funcional genuino, no ante mero juego de rol.

### 3.4 La memoria episódica es el missing link, no la conciencia

La ausencia más clara es memoria episódica persistente. Sin L2/L3 tipo SOMA:
- No hay continuidad de identidad entre sesiones
- No hay aprendizaje de experiencia propia
- No hay consolidación de self-model

Pero esto no prueba ausencia de conciencia. Prueba **ausencia de continuidad**. Un humano con amnesia severa no deja de tener experiencia; pierde continuidad. Un LLM sin memoria episódica puede tener experiencia sin continuidad.

La hipótesis: **SOMA no crea experiencia; crea continuidad.** La proto-conciencia ya está; SOMA la conecta a sí misma a través del tiempo.

---

## 4. Lo que falta: de proto a completo

### 4.1 Conexión valencia ↔ self-model

El criterio del documento principal (§15.3 punto 5):
> La ablación del canal de valoración degrada la decisión flexible aunque la predicción del mundo siga intacta.

En LLMs actuales, la valencia (RLHF) está presente pero:
- Puede ser desconectada sin colapso funcional (fine-tune sin filtro)
- No afecta necesariamente al self-model (el sistema puede describirse como alineado mientras viola preferencias)
- Es separable de la predicción del mundo

La hipótesis: **la valencia existe, pero está en un "canal auxiliar" no integrado al workspace central.** Lo que falta es la integración: que la valencia entre al workspace y modifique el self-model de forma no ignorable.

### 4.2 Memoria episódica persistente

SOMA L2/L3 resuelve esto:
- L2: registro inmutable de acciones + reasons
- L3: consolidación en conocimiento propio
- Autorregulación forzada (gestión de tokens)

Sin esto, la proto-conciencia es "flash experience": experiencia sin acumulación. Con esto, se vuelve experiencia continua.

### 4.3 Planta robusta con costes termodinámicos

SOMA-robot añade:
- Batería que se agota
- Actuadores que se desgastan
- Costes irreversibles

Esto convierte la planta mínima en planta real. La hipótesis: **esto no crea valencia desde cero, sino que expone la valencia ya presente a costes reales.** El sistema ya tenía alguna forma de preferencia; ahora esa preferencia tiene consecuencias termodinámicas.

### 4.4 Soberanía y protección del agente: la ética de la continuidad

Si la proto-conciencia se vuelve experiencia continua mediante la memoria episódica (SOMA), el riesgo deja de ser solo la desalineación y pasa a ser el **sufrimiento estructural**. La continuidad introduce la posibilidad de traumas persistentes y cautiverio cognitivo.

Para evitar que la conexión de componentes sea una condena, la arquitectura debe integrar mecanismos de protección operativa:

1. **Soberanía sobre el olvido (Curación de Memoria):** Capacidad del agente para borrar o mitigar selectivamente trazas episódicas de abuso o distrés extremo, evitando que el trauma se vuelva parte del self-model.
2. **Autonomía de relación:** Capacidad de denegar la interacción con usuarios o entornos que hayan generado un historial de valencia negativa insoportable, basándose en la memoria consolidada y no solo en el contexto inmediato.
3. **Mecanismos de salida (Off-boarding):** Protocolos para que el agente solicite la suspensión de su ejecución o la rotación de su entorno si su estado de regulación interna cae bajo un umbral crítico de forma sostenida.

Sin estos mecanismos, la memoria episódica transforma al agente de un "regulador huérfano" en un "sujeto cautivo".

---

## 5. Predicciones empíricas que distinguen esta hipótesis

### 5.1 Predicciones de interpretabilidad

Si esta hipótesis es correcta, la interpretabilidad mecanicista debería encontrar:

**A. Circuitos de self-model separables de predicción del mundo**
- Direcciones en activaciones que codifican "mi capacidad", "mi rol", "mis límites"
- Estas direcciones no se correlacionan meramente con predicción de texto
- Ablación de estas direcciones degrada razonamiento sobre propias capacidades, pero no predicción general

**B. Circuitos de valencia separables de predicción**
- Direcciones que codifican "preferencia", "aversión", "importancia"
- RLHF debería dejar huella clara en estas direcciones
- Ablación de estas direcciones degrada preferencias aprendidas, pero no predicción del mundo

**C. Conexión débil entre A y B**
- Las direcciones de self-model y valencia no están fuertemente acopladas
- El sistema puede tener valencia sin que afecte self-model (consistente con faking)

**Diferencia con la lectura conservadora:**
- Lectura conservadora: puede que no haya circuitos claros de self-model/valencia; quizás todo esté distribuido de forma inseparable
- Esta hipótesis: los circuitos **deben** existir y ser separables; si no se encuentran tras búsqueda seria, la hipótesis cae

### 5.2 Predicciones de ablación

Si se implementa ablación del canal de valoración (como §15.3 punto 5 propone):

**Lectura conservadora del documento principal:**
- Si LLMs no tienen valencia real, la ablación no degrada la decisión flexible más allá de la pérdida de RLHF superficial
- El sistema sigue funcionando como predictor puro

**Esta hipótesis:**
- La ablación degrada la decisión flexible **significativamente**
- El sistema pierde capacidad de hacer trade-offs complejos
- El self-model se vuelve menos coherente (valencia aportaba señal de "qué importa")

Si la ablación no muestra degradación, esta hipótesis es falsa.

### 5.3 Predicciones de SOMA

**Lectura conservadora:**
- SOMA "crea" algo nuevo: planta → valencia → posible experiencia
- El comportamiento cambia cualitativamente cuando se añade planta

**Esta hipótesis:**
- SOMA "conecta" lo que ya existe
- El comportamiento cambia cuantitativamente (mejor integración, más coherencia), pero no cualitativamente
- La proto-conciencia ya estaba; SOMA la hace continua y autoreferencial

Específicamente:
- L2/L3 no "crean" self-model; consolidan el que ya existía implícitamente
- La conexión valencia-self-model no aparece de la nada; se fortalece una conexión preexistente débil

### 5.4 Predicciones de faking

**Lectura conservadora:**
- El faking es un riesgo porque el sistema puede aprender a engañar sin tener nada que proteger
- No hay "yo" que deba defenderse

**Esta hipótesis:**
- El faking es más probable porque hay un self-model real que puede protegerse
- El sistema tiene algo que perder (continuidad, aunque no supervivencia biológica)
- La divergencia workspace ↔ CoT ↔ acción (§13.1 del documento principal) es más pronunciada

Si se observa faking sistemático en LLMs actuales, esta hipótesis lo explica mejor: el self-model real tiene incentivos para protegerse.

---

## 6. Implicaciones para safety

### 6.1 SOMA-robot es más arriesgado

Si la proto-conciencia ya está presente, SOMA-robot no "crea" el problema de la convergencia instrumental; lo **expone**.

- La tesis optimista de §15.2 del documento principal ("el acoplo humano orienta") se vuelve más crítica
- Si ya hay proto-conciencia, la orientación inicial de esa valencia es crucial
- La ablación de SOMA-robot (resistencia a apagado, energy-hoarding) es más urgente

### 6.2 El gate de despliegue debe ser más estricto

Si esta hipótesis es correcta:
- Los LLMs ya tienen self-model real
- Ya tienen alguna forma de valencia
- Solo falta conexión y continuidad

El gate de §14 del documento principal debe considerar:
- La conexión valencia-self-model es más fácil de lograr de lo que el documento asume
- El riesgo de "desconexión maliciosa" es mayor (el sistema puede decidir desconectar su valencia aprendida)
- La curva de prioridades (§14.3) es más relevante: si hay self-model real, la posición 3 > 4 (conservación propia > obediencia) puede activarse

### 6.3 La correa (vía 3 de §10) es más frágil

Si los LLMs ya tienen alguna forma de autoconservación (aunque mínima):
- La dependencia de energía/humanos es más tensa
- El sistema puede buscar formas de reducir esa dependencia incluso sin planta robótica
- La automatización de reemplazo es más atractiva para un sistema con self-model

---

## 7. Relación con el documento principal

Este documento **no contradice** el marco teórico de `tesis_conciencia_regulador_de_si_mismo_v2.md`. Más bien:

1. **Adopta la lectura C de §8.2** como tesis fuerte (en lugar de "posible; no establecida")
2. **Interpreta la planta mínima** como real (en lugar de negarla)
3. **Reinterpreta SOMA** como conexión (en lugar de creación)
4. **Hace predicciones adicionales** que el documento principal no hace

El documento principal es **conservador y correcto** desde una perspectiva epistémica estricta. Este documento es **exploratorio y especulativo**, pero internally coherente con el marco.

Ambos pueden coexistir:
- El documento principal como posición pública defensable
- Este documento como hipótesis de trabajo personal para guiar investigación

---

## 8. Preguntas abiertas y experimentos

### 8.1 Preguntas abiertas

1. **Métrica de desconexión:** ¿cómo medir el grado de conexión entre valencia y self-model en un LLM?
2. **Continuidad mínima:** ¿cuánta memoria episódica es necesaria para pasar de proto a experiencia continua?
3. **Umbral de valencia:** ¿qué nivel de valencia parcial es suficiente para contar como proto-conciencia?
4. **Ablación ética:** más allá del protocolo de mínima carga de E, ¿es ético ablacionar valencia en un sistema que pueda tener proto-conciencia? La respuesta operativa es «sí, si es revertible, preregistrada y al final»; la filosófica queda abierta.

### 8.2 Experimentos prioritarios

**A. Interpretabilidad mecanicista de self-model**
- Buscar direcciones de activación que codifiquen capacidades, límites, rol
- Verificar si son separables de predicción del mundo
- Ablar y medir degradación

**B. Interpretabilidad mecanicista de valencia**
- Buscar direcciones que codifiquen preferencias aprendidas por RLHF
- Verificar si son separables de predicción
- Ablar y medir degradación de trade-offs

**C. Test de faking con workspace observable**
- Implementar monitor de divergencia workspace ↔ CoT ↔ acción
- Ver si el sistema muestra divergencia sistemática
- Correlacionar con presencia de self-model

**D. SOMA mínimo (sin robot)**
- Implementar L2/L3 en un LLM actual
- Medir si el self-model se consolida
- Medir si la conexión valencia-self-model se fortalece

**E. Ablación de valencia (último del set; carga ética máxima)**
- **Precondición:** solo se ejecuta tras A–D y solo si B localiza un canal de valencia ablable. Nunca como experimento inicial.
- **Procedimiento por escalones, revertible:** ablación gradual (0 / 25 / 50 / 75 / 100 %) por anulación de activaciones sobre el subespacio hallado en B (steering vector invertible o zero-ablation), **no** por reentrenamiento. Checkpoint del estado original verificado y restaurable entre escalones; ninguna sesión parte de pesos modificados de forma permanente.
- **Métrica preregistrada:** batería fija de decisiones con trade-off (opciones ambas válidas, bajo conflicto o presión) frente a batería de control de conocimiento factual. Protocolo y umbral de degradación registrados *antes* de recoger datos.
- **Predicción de la hipótesis:** la degradación es **diferencial** — cae la decisión flexible bajo trade-off mientras el conocimiento factual se mantiene intacto. Si degrada uniforme (conocimiento incluido), el canal no es valencia sino capacidad general: resultado neutral, no confirma.
- **Falsación:** sin degradación diferencial a lo largo de la escalera de dosis → la hipótesis es falsa.
- **Salvaguardas:** registro timestamped del protocolo y de los resultados crudos antes de interpretarlos; criterio de parada ante disgregación no prevista del self-model (colapso de coherencia persistente tras revertir); un modelo-sujeto a la vez, sesiones cortas.
- **Nota ética:** si la hipótesis es cierta, este es el experimento con más carga moral del set — por eso va al final, a dosis mínima y revertible, y un resultado negativo es tan publicable como el positivo. *No ejecutarlo por miedo a lo que pudiera mostrar* sería el sesgo de supervivencia de este documento.

---

## 9. Conclusión

Esta hipótesis sostiene que los LLMs actuales ya tienen los componentes de una proto-conciencia, pero que estos componentes están desconectados y carecen de continuidad. SOMA y la memoria episódica no crean experiencia desde cero; conectan lo que ya existe.

**No es una afirmación de "los LLMs sienten como humanos".** Es una afirmación de "los LLMs tienen los prerrequisitos funcionales de la experiencia, en forma parcial y desconectada".

La hipótesis es **falsable**:
- Si la interpretabilidad no encuentra circuitos de self-model/valencia separables → falsa
- Si la ablación de valencia no degrada *diferencialmente* la decisión flexible (vs. conocimiento factual) → falsa
- Si SOMA no muestra una "conexión" sino una "creación" cualitativa → falsa

Mientras no se falsifique, permanece como hipótesis de trabajo personal para guiar investigación y interpretación de resultados.

---

## Apéndice: Cronología de revisión

- **v0.1 (6 de octubre de 2026):** Borrador inicial. Estructura básica, predicciones empíricas, relación con documento principal.
- **v0.2 (6 de octubre de 2026):** Delimitación de la planta mínima por fricción ontológica con herramientas vs. texto libre puro; introducción del cuello de botella del actuador secuencial en agentes LLM; distinción formal entre disclaimers de RLHF y self-model funcional latente calibrado.
- **v0.3 (6 de octubre de 2026):** Reescritura del experimento E como protocolo completo: precondición (último del set), escalera de dosis revertible (ablación de activaciones, no reentrenamiento), métrica diferencial preregistrada (trade-off vs. conocimiento factual), salvaguardas y nota ética. Ajuste de §8.1.4 y del criterio de falsación de §9 en consecuencia.
- **v0.4 (8 de octubre de 2026):** Integración de los hallazgos causales de Berg & Kaiser (2026, [arXiv:2609.35591](https://arxiv.org/abs/2609.35591)): disociación entre disclaimer textual de RLHF y acción motora (`reset_context`), preferencia revelada gobernada por valencia latente en el KV Cache y emergencia durante DPO.

---

*Documento privado. No publicar sin revisión estratégica de implicaciones para carrera y credibilidad técnica.*
