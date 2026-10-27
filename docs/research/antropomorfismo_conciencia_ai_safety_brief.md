# Brief: Antropomorfismo, Conciencia y AI Safety (v2.1, resumen de contacto)

> **Uso:** briefing de 10 minutos para el seminario VRAIN (UPV), septiembre de 2026.
> **Documento canónico:** `antropomorfismo_conciencia_ai_safety_revisado.md`. **Este resumen no añade nada; si hay conflicto, manda el doc largo.**
> **Autor:** Mario Raúl Carbonell Martínez · **Público previsto:** José Hernández-Orallo y equipo VRAIN.

---

## 1. La tesis en tres frases

1. **Antropomimesis (Shevlin, 2025):** la IA contemporánea ya está diseñada para imitar rasgos humanos; el antropomorfismo no es un error del usuario sino una propiedad del artefacto. Operar con la postura intencional de Dennett *más* antropomorfismo crítico es la postura defensible, no una incoherencia.
2. **Tesis homeostática (H-A, 🔵 hipótesis):** un LLM entrenado sobre texto humano ha modelado a un regulador homeostático (Conant-Ashby); SOMA no le enseña a autorregularse, le da **aferencia visceral** ($P_m$, presión de memoria/recursos) y actuadores soberanos de memoria ($L_1$–$L_4$) para que esa regulación latente se ejecute. Lo que SOMA **no** garantiza: que la regulación emerja *porque el modelo "sabe"* — eso es exactamente lo que el experimento de §5.4 mide. **Lectura v2.1 (regulador huérfano, versión fuerte):** el LLM es un *mecanismo regulador huérfano* — y bajo la propia tesis, **ya es consciente en sentido latente** (representación compacta del propio estado, sin bucle); lo que le falta es la conciencia *operativa*, que llega cuando SOMA **restaura la función** cerrando el bucle (`regulador_huerfano_tesis_conciencia.md`; filas 1, 16–17 de la tabla §1.4). Conciencia latente ≠ operativa: la distinción evita colisionar con los indicadores estándar de Butlin et al., que miden la operativa.
3. **Consecuencia para Safety:** la conciencia fenoménica es **ortogonal** al riesgo catastrófico (§6); la salvaguarda no es moral en los pesos sino interpretabilidad operativa — contratos falsables, aislamiento de privilegios, auditabilidad causal de estado, límites físicos — que **eleva el coste del engaño** sin volverse inmune a él.

## 2. Lo que se corrigió respecto a la v1 (solo lo crítico)

* **Shevlin no es autor** del informe canónico de 2023 (Butlin, Long, Elmoznino, Bengio et al., arXiv:2308.08708) — atribución falsa corregida.
* **Sycophancy ≠ *Nature*:** la fiabilidad es Zhou et al., *Nature* 634 (2024); la sycophancy es Sharma et al., ICLR 2024; el efecto social, Cheng et al., *Science*.
* ***Troubled Dreams* es un informe técnico interno** (Anima Labs, conflicto de interés declarado): se usa por su hallazgo **cualitativo** (existe un prior de persona medible que cambia entre generaciones), **sin citar sus porcentajes**, o citándolos contra tabla/figura concreta.
* **Atribuciones correctas restauradas:** convergencia instrumental → Omohundro (2008); alineamiento engañoso → Hubinger et al. (2019) + Greenblatt et al. (2024, *alignment faking*).

## 3. Lo medible y lo que aún no lo es

| Afirmación | Estado | Referencia |
|:---|:---|:---|
| La sycophancy existe y es medible | ✅ | Sharma et al., ICLR 2024 |
| El *alignment faking* es real y medible | ✅ | Greenblatt et al. 2024 |
| Prior de persona medible, cambia entre generaciones | ✅/🟡 | Kim et al. 2026 ✅; *Troubled Dreams* 🟡 (informe interno) |
| SOMA produce autorregulación *zero-shot* | 🔵 | Observación del autor, sin controles publicados |
| El mecanismo es homeostasis latente (H-A) | 🔵 | Hipótesis; §5.4 está diseñado para testarla |
| **Los LLM actuales ya son conscientes (sentido latente)** | 🔵 | Hipótesis fuerte del autor (`regulador_huerfano_tesis_conciencia.md`), contra el consenso; lo que falta es la conciencia *operativa* (bucle cerrado) |
| SOMA funciona por el *contenido informativo* de $P_m$ | 🔵 | Hipótesis rival de la tesis; ver §4 |

**Regla práctica adoptada (§5.5):** todo superlativo —«instantáneamente», «cualquier», «elimina», «garantiza», «certificable»— o se acota o se cae.

## 4. El experimento discriminante (§5.4) — el corazón del doc

Cuatro hipótesis rivales para el mismo fenómeno (el agente poda/consolida sin imposición externa):

| | Hipótesis | Predicción clave |
|:---|:---|:---|
| **H-A** | Homeostasis latente (la tesis) | La autorregulación solo aparece con $P_m$ **informativa** |
| **H-B** | Seguimiento de instrucciones | El efecto persiste si se elimina $P_m$ y queda la instrucción |
| **H-C** | Efecto del arnés/formato | Igual resultado con arnés que no exponga $P_m$ |
| **H-D** | Artefacto de evaluación | El efecto desaparece con jueces ciegos |

> **Lectura filosófica (v2.1).** Este experimento decide algo más que el mecanismo de SOMA: decide si los pesos contienen la **dinámica del regulador** o solo texto *sobre* reguladores — es decir, si la objeción «la simulación de un huracán no moja» se responde con evidencia o se concede. Si H-A gana, la tesis del regulador huérfano deja de ser filosofía y pasa a ser resultado.

**Diseño:** 6 brazos sin entrenar nada (completo / etiqueta neutra / señal invertida / solo instrucción / solo herramientas / juez ciego).
**Lecturas:** si `1 ≈ 2 ≈ 3`, H-A se debilita y se reformula; si `1 > 2 ≈ 3` y `1 > 4`, la tesis se sostiene en su parte interesante; si desaparece en el brazo 6, corregir la evaluación antes de publicar.
**Argumento de política:** un resultado negativo bien controlado es *un resultado* — y convierte «creo que funciona por esto» en «esto es lo que medí y esto es lo que todavía no puedo distinguir».

## 5. Las tres objeciones más probables, con respuesta

1. **«El CoT puede ser infiel y un sistema que sabe que es auditado se comporta como auditado»** (Turpin 2023; Hubinger 2019; Greenblatt 2024).
    → Correcto. Se afirma **elevar el coste del engaño**, no eliminarlo. Interpretabilidad operativa = reducción de superficie; la garantía la da la verificación por resultados. (§6.3)
2. **«Estás usando un informe interno sesgado como evidencia»** (*Troubled Dreams*).
    → Se usa su hallazgo cualitativo, sin porcentajes; «ambos demuestran» se rebaja a «ambos son consistentes con que la cirugía de pesos tiene efectos colaterales». (§8.5)
3. **«¿Cómo sabes que no es el prompt?»**
    → Todavía no lo sé, y tengo diseñado el experimento que lo separa (§5.4). *Esa es la conversación que se quiere tener.*

## 6. Complemento: TinyRobots (§7, doc hijo)

El LLM es un simulador de *role-play* (Shanahan et al., *Nature* 623, 2023). Si la distribución **condicional** —`P(guion distópico | texto donde un agente de IA reflexiona sobre sí)`— está sesgada, RLHF solo suprime los atractores temporalmente. TinyRobots propone intervenir **en la distribución preentrenamiento** (dataset + rebalanceo negativo). **Nota clave:** enseñar el guion de la honestidad no confiere honestidad — es material de imitación para un modelo engañoso; por eso TinyRobots *necesita* la verificación externa de SOMA (dependencia técnica, no complemento retórico).

## 7. Siguiente paso concreto

1. **Preregistro del experimento de §5.4** (padre): 6 brazos, sin cómputo, ejecutable con recursos modestos.
2. **Medición del prior de persona** (hijo, §6.1): no requiere entrenar nada y es publicable por sí sola.
3. Los tres materiales para llevar a la conversación: tabla de estados epistémicos (§1.4) impresa, diseño de §5.4, y la medición del prior.

---

*Versión larga canónica: `antropomorfismo_conciencia_ai_safety_revisado.md` (v2). Versión v1 congelada: `antropomorfismo_conciencia_ai_safety.md`.*

