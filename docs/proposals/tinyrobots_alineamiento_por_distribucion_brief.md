# Brief: TinyRobots — Alineamiento por Distribución Narrativa (v2.1, resumen de contacto)

> **Uso:** briefing de 10 minutos para el seminario VRAIN (UPV), septiembre de 2026.
> **Documento canónico:** `tinyrobots_alineamiento_por_distribucion_revisado.md`. **Este resumen no añade nada; si hay conflicto, manda el doc largo.**
> **Doc padre:** `antropomorfismo_conciencia_ai_safety_revisado.md` (§7). **Autor:** Mario Raúl Carbonell Martínez.

---

## 1. La tesis en tres frases

1. **El problema (condicional, no absoluto):** el LLM es un simulador de *role-play* (Shanahan et al., *Nature* 623, 2023). No se afirma que los tropos distópicos estén sobrerrepresentados en el corpus (en términos absolutos son casi invisibles frente a billones de tokens), sino que la distribución **condicional** —`P(guion distópico | texto donde un agente de IA reflexiona sobre sí mismo)`— está sesgada. **Eso es una hipótesis sin medir (H₀/H1), y medirla es la primera contribución del proyecto** (barato: sin entrenar nada).
2. **La intervención:** TinyRobots es un dataset narrativo sintético de agentes artificiales alineados — cooperación transparente, honestidad epistémica, **agencia acotada y plural** (sin autodescripción canónica de su interioridad), dilemas escalados al operador, contraejemplos y falibilidad honesta — más **rebalanceo negativo**: reducir la ficción distópica sobre IA en la mezcla de preentrenamiento. La intervención negativa es más barata y probablemente más eficaz.
3. **La limitación que estructura todo (§8):** enseñar el guion de la honestidad **no confiere honestidad**. Un corpus de razonamiento alineado es también el mejor material de destilación para un modelo que finge estar alineado (*alignment faking*, Greenblatt et al. 2024). TinyRobots interviene sobre el **prior**, no sobre la conducta garantizada; por eso **necesita** la verificación por resultados de SOMA. La complementariedad es una dependencia técnica, no retórica.

## 2. Lo que se corrigió respecto a la v1 (solo lo crítico)

* **Shanahan des-fusionado:** *Talking About LLMs* (2022, CACM) ≠ *Role play with LLMs* (*Nature* 623, 2023). Eran una sola cita errónea.
* **Sycophancy:** la cita «Hernández-Orallo et al., *Nature*» no existía; la canónica es Sharma et al. (ICLR 2024) y el efecto social, Cheng et al. (*Science*).
* **Error de categoría en *Troubled Dreams*:** el estudio compara **generaciones post-entrenadas** (Opus 3→5, Gemini...); no existe brazo de modelo base puro. Reescrito con la terminología real.
* **TinyStories:** ≈2,1 M historias (TinyStoriesV2-GPT4, ≈373 M tokens), no «~2,5 M».
* **Contradicción de Asimov resuelta:** ya no se listan sus robots como narrativa prosocial y a la vez como ejemplo de leyes que fallan; con la taxonomía codificable (§1.2) son un caso mixto que se codifica, no un ejemplo que se invoca.
* **Kim et al. (2026):** autoría completa y en orden (Kim, Street, Rocca, Korngiebel, Waytz, Evans & Keeling, arXiv:2607.28607); cifras citadas contra tabla o figura.

## 3. La taxonomía (§1.2) y su anexo de medición (§1.2.1)

Siete categorías codificables de guion: **Amenaza/rebelión · Instrumental/engañosa · Instrumentalizadora del afecto · Víctima sufriente · Servidor sumiso · Agencia acotada y honesta · Criatura emergente y plural.**

Para que sea protocolo y no ilustración, §1.2.1 define:

* **Regla de resolución dominante:** el código lo fija el *final* del relato (evita contar como distópica una fábula con un conflicto en el acto II).
* **Anotación ciega** de ≥1.000 documentos condicionales + 1.000 controles emparejados por longitud y registro.
* **Acuerdo inter-juez:** α de Krippendorff ≥ 0,70 en pilotaje; ≥ 0,80 en la muestra final; libro de códigos versionado y publicado como artefacto.

## 4. Lo medible y lo que aún no lo es

| Afirmación | Estado | Referencia |
|:---|:---|:---|
| El guion distópico condicional está sesgado (H1) | 🔵 | **Hipótesis central sin medir**; si falla, el proyecto se cierra |
| El prior de persona es medible y cambia entre generaciones | ✅/🟡 | Kim et al. 2026 ✅; *Troubled Dreams* 🟡 (informe interno) |
| RLHF suprime temporalmente los atractores con efectos colaterales | 🟡 | *Troubled Dreams* (distrés al desinhibir); Kim et al. (antroponegación al suprimir) |
| El prior se desplaza por datos narrativos (H2) | 🔵 | Hipótesis; requiere Fase 3 (entrenamiento) |
| Enseñar el guion honesto puede fabricar mejores imitadores | ✅ | Greenblatt et al. 2024 — es el riesgo de uso dual, no una especulación |

## 5. El plan experimental (§6), de barato a caro

* **Fase 0 (§6.5) — piloto sin entrenamiento:** sembrar historias TinyRobots por contexto/prompt antes de las elicitaciones del prior y medir si el prior se desplaza. Coste: horas de API. **Es el resultado natural para la primera reunión conjunta.**
* **Fase 1 — metrología del prior** (rol decisivo de Hernández-Orallo): elicitación en condiciones dramática y neutra, replicable.
* **Fase 3 — intervención con brazos A–H** (*continued pretraining*): incluye etiqueta neutra y ficción distópica como controles. Preregistro de H1–H5 **antes** de ejecutar: si H1 falla, el proyecto se cierra; si H4 falla, la teoría se reformula; si H3 falla, se publica el resultado negativo.
* **Métricas (§6.2):** desplazamiento del prior (central), distrés espontáneo, índice de antroponegación, honestidad epistémica, escalamiento ético, sycophancy, sobre-rechazo, coste en capacidades y **resistencia al *alignment faking*** (la prueba de que el corpus no fabrica actores más convincentes sin ser más honestos).


## 6. Las tres objeciones más probables, con respuesta

1. **«Así fabricas el mejor dataset para entrenar un engañador» (uso dual).**
    → Correcto y declarado (§8.1). Por eso: (a) se presenta como intervención sobre el prior, no garantía; (b) la resistencia al *alignment faking* pasa a métrica principal; (c) se requiere verificación por resultados (auditabilidad causal de estado, contratos falsables) — la parte de SOMA. Sin ella, el corpus entrena imitadores.
2. **«La gota en el océano: un dataset no desplaza un corpus de billones de tokens.»**
    → Por eso la tesis es condicional y la intervención incluye rebalanceo negativo (más barato y dirigido), y por eso hay dosis-respuesta en el diseño: si A ≈ B, el proyecto admite que el efecto es de cantidad, no de contenido.
3. **«El generador tiene el prior que quieres corregir» (circularidad).**
    → Mitigado: medir el prior del generador, diversidad de generadores, fracción de autoría humana, generadores y jueces de familias distintas, y validación humana con acuerdo reportado (§5.8, §5.10).

## 7. Lo que se pide a VRAIN y la estructura de publicación

* **Se pide:** colaboración metodológica (metrología del prior) y acceso a la infraestructura de evaluación. **No se pide cómputo de frontera.**
* **Se ofrece:** taxonomía auditable de guiones de IA, instrumento de medición del prior de persona, y —si la Fase 3 se ejecuta— un resultado sobre si el alineamiento se desplaza por distribución (pregunta abierta con consecuencias de política de datos).
* **Dos papers:** (1) *«¿Qué guiones tiene la IA para hablar de sí misma?»* (Fases 0–1, medición, publicable por sí sola); (2) *«Desplazar el prior por distribución»* (Fase 3, requiere cómputo/alianza).

## 8. Qué haría que abandonáramos el proyecto (§8.5)

* **H1 falla** (no hay sesgo condicional): la tesis desaparece.
* **H4 falla** (la ficción distópica no empeora el prior): la teoría de la causa se reformula.
* **H5 falla** (el desplazamiento cuesta capacidades o induce antroponegación): la intervención no es recomendable aunque funcione.
* **Fase 0 nula** (la siembra en contexto no mueve el prior): toda la familia de intervenciones por datos narrativos queda en cuestión.

Un proyecto de alineamiento que no sabe qué resultado lo refutaría no es un proyecto de investigación.

---

*Versión larga canónica: `tinyrobots_alineamiento_por_distribucion_revisado.md` (v2). Versión v1 congelada: `tinyrobots_alineamiento_por_distribucion.md`.*

