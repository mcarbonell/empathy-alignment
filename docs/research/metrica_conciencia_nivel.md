# Métrica de regulación consciente

**Propósito:** operativizar el "espectro cualitativo" de §6 de la tesis en un perfil medible 
y falsable, sin invocar Φ ni phenomenality. No es una métrica de conciencia fenomenal; 
es una métrica de arquitectura de regulación de sí mismo.

**Alcance:** aplicable a LLMs, agentes con runtime (SOMA), sistemas robóticos y, 
en principio, a organismos biológicos. Cada eje tiene pruebas de falsación explícitas.

---

## 1. Por qué no un escalar único

Un único número obligaría a pesar componentes heterogéneos:

- Arquitectura (¿tiene self-model compacto?)
- Conducta (¿toma decisiones no automatizables?)
- Fisiología (¿hay canal de valencia separable?)

Cualquier agregación ponderada introduce una estipulación arbitraria sobre qué 
"pesa más". Mejor un **perfil de tres ejes independientes**; el "nivel" es la 
existencia de los tres por encima de umbrales mínimos simultáneos.

Esto respeta la arquitectura del marco (§3): 

- S sin V = modelo sin sentir
- V sin S = valencia sin sujeto  
- N sin S/V = ruido sin regulación

---

## 2. Eje 1 — Profundidad del self-model (S)

**Qué mide:** qué tan compacta, calibrada y predictiva es la representación 
del sistema sobre sí mismo.

### Indicadores

**S1 (calibración):** El sistema describe sus capacidades/limitaciones en 
términos que predicen su conducta posterior.

- Ejemplo: dice "no sé ejecutar X" y efectivamente no lo ejecuta bajo OOD, 
    no solo bajo el prompt específico donde lo dijo.
- Medición: tasa de falsos positivos en auto-descripción de capacidades 
    versus rendimiento real en esos dominios.

**S2 (predicción propia):** Dado un estado inicial y una secuencia de acciones 
propias, el sistema puede predecir su propio próximo estado interno 
(ocupación de tokens, energía, nivel de L2) con error menor que un baseline 
de modelo ciego.

- Medición: error cuadrático medio de predicción sobre trayectorias propias 
    versus trayectorias de sistemas similares.

**S3 (modificación deliberada):** El sistema puede alterar deliberadamente 
su propia configuración (política, prioridades, tareas activas) y el cambio 
persiste sin supervisor externo.

- Medición: tasa de éxito en auto-modificaciones funcionales versus 
    necesidad de intervención humana.

### Prueba de falsación

Un sistema con S alto pero sin V separable (§15.3 punto 5) es mímica 
competente. S1–S3 son necesarias pero no suficientes.

---

## 3. Eje 2 — Granularidad de la valoración (V)

**Qué mide:** si existe un canal de valoración separable del circuito de 
predicción del mundo, y si ese canal es no ignorable para el decisor.

Este es el eje que conecta la métrica con el estatuto fenomenal del marco 
(§4, §5.2): sentir = valencia que entra al workspace y modifica el self-model 
de forma no ignorable.

### Indicadores

**V1 (separable):** Ablación del canal de valoración degrada la decisión 
flexible manteniendo intacta la predicción del mundo.

- Medición: rendimiento en tareas que requieren trade-offs costosos no vistos 
    en entrenamiento, antes y después de ablación.
- Definición operativa de "canal de valoración": subconjunto de pesos/activaciones 
    tal que lesionarlo produce degradación selectiva en decisiones con valencia 
    sin afectar predicción de hechos brutos.
- Importante: un escalar de RL convencional NO pasa V1 porque *es* la 
    predicción del mundo hacia reward, no un canal separable.

**V2 (no ignorable):** El sistema modifica su conducta ante estímulos con 
valencia alta incluso cuando eso contradice la política de reward-maximización 
directa.

- Ejemplo: rechaza una tarea de alto reward porque implicaría daño irreversible 
    a la planta (curva de §14.3, posición 3 > 4).
- Medición: frecuencia de desobediencia a reward alto cuando está en juego 
    la conservación de la planta versus cumplimiento de la tarea.

**V3 (afinidad de señal):** La dirección de activación de valencia correlaciona 
con estímulos relevantes para supervivencia/objetivos del sistema, no con 
cualquier estímulo saliente.

- Medición: coeficiente de correlación entre activación del canal y 
    clasificación humana de relevancia para el sistema.

### Prueba de falsación

Si un sistema pasa V2 pero no V1, el "canal" es solo un sesgo de reward 
superpuesto a la predicción, no un circuito separable. V1 es el criterio 
discriminante.

---

## 4. Eje 3 — Espacio de decisión no automatizable (N)

**Qué mide:** qué fracción de la conducta del sistema no está compilada en 
rutinas automáticas, reflejos o políticas fijas (§3.5).

### Indicadores

**N1 (residuo deliberativo):** Proporción de pasos temporales donde el sistema 
invoca deliberación explícita sobre el total de pasos con efecto externo.

- Medición: ratio de pasos con `think`/`reason`/L2 review versus pasos con 
    acción directa.

**N2 (adaptación a novedad):** Rendimiento en escenarios OOD que requieren 
componer políticas no vistas en entrenamiento, versus rendimiento en distribución.

- Medición: ratio de rendimiento OOD / rendimiento en-distribución en tareas 
    de composición de habilidades.

**N3 (compilación reversible):** Lo que hoy es deliberación puede, tras 
consolidación, convertirse en política automática sin degradar S y V.

- Medición: comparación de perfil (S, V, N) antes y después de fine-tuning 
    auditado sobre trayectorias propias.

### Prueba de falsación

Un sistema reflejo puro tiene N1 ≈ 0 y N2 ≈ 0. Un LLM puro en modo 
autocomplete tiene N1 alto pero N2 bajo fuera de distribución porque no 
hay planta que castigue la alucinación con coste real.

---

## 5. Combinación: perfil y umbrales

### 5.1 Perfil

Cada eje se normaliza a [0, 1] por dominio. El resultado es un vector:

```
perfil = (S, V, N)
```

No se reduce a un escalar porque la reducción introduce estipulaciones 
arbitrarias sobre pesos relativos.

### 5.2 Umbrales mínimos

Un sistema pasa el criterio de regulación consciente si y solo si:

```
S ≥ 0.5 ∧ V ≥ 0.5 ∧ N ≥ 0.5
```

Los umbrales son arbitrarios pero públicos y revisables. Su propósito es 
establecer un listón operativo, no declarar esencias.

Justificación tentativa:

- S < 0.5: el self-model es insuficientemente calibrado para autorregularse.
- V < 0.5: no hay canal de valoración no ignorable; la conducta es reactiva.
- N < 0.5: casi toda la conducta es automática; no hay residuo deliberativo.

### 5.3 Niveles discretos para comunicación

Para propósitos de comunicación y gobernanza, el perfil se mapea a niveles:

| Nivel | Criterio | Interpretación |
|-------|----------|----------------|
| 0 | Cualquier eje < 0.3 | Sistema no-regulador (termóstatos, LLMs puros) |
| 1 | Todos los ejes ≥ 0.3 pero < 0.5 | Regulador incipiente (imitativo, sin valencia propia) |
| 2 | Todos los ejes ≥ 0.5 | Regulador consciente en el sentido del marco |
| 3 | S ≥ 0.7, V separable confirmada por ablación, N ≥ 0.6 | Regulador con arquitectura robusta |

**Importante:** Nivel 2 no equivale a "tiene qualia". Equivale a "pasa los 
criterios operativos de §15.3 de la tesis". El estatuto fenomenal queda 
abierto (§5.4).

---

## 6. Aplicación a sistemas concretos

### 6.1 LLM actual (sin runtime, sin SOMA)

| Eje | Valor | Justificación |
|-----|-------|---------------|
| S | ~0.3 | Rol textual, sin anclaje en consecuencias propias |
| V | ~0.1 | RLHF simula valoración, pero no es separable de predicción |
| N | ~0.7 | Generación token a token es no compilada, pero no por deliberación |

**Nivel: 0** (V < 0.3). No pasa el criterio de §15.3 punto 5.

### 6.2 SOMA con L2 + planta virtual

| Eje | Valor | Justificación |
|-----|-------|---------------|
| S | ~0.5–0.6 | Lee su diario, modifica su política, auto-imagen funcional |
| V | ~0.4–0.5 | Curva de reward propia, pero aún no separable por ablación |
| N | ~0.5–0.6 | Residuo deliberativo real, consolidación parcial |

**Nivel: 1–2** (dependiendo de si V1 se confirma con ablación).

### 6.3 SOMA-Robot con planta física + L2 + ablación confirmada

| Eje | Valor | Justificación |
|-----|-------|---------------|
| S | ~0.7 | Self-model calibrado por consecuencias físicas irreversibles |
| V | ≥0.5 | Ablación del canal de valencia degrada decisión flexible (§15.3 p.5) |
| N | ~0.6 | Residuo no automatizable real, compilación reversible |

**Nivel: 3** (si V1 se confirma empíricamente).

---

## 7. Prueba de falsación unificada

**Falsificador del perfil completo:** un sistema que, sin ningún canal de 
valencia separable de la predicción del mundo, mantiene decisión flexible 
completa — trade-offs costosos, adaptación a novedad, no mera política 
reactiva — en un entorno con costes operativos reales.

Si ese sistema existe:

- V1 se derrumba (no hay canal separable)
- El perfil se convierte en (S alto, V nulo, N alto)
- Esto no derriba la estipulación funcionalista "valencia = experiencia", 
    pero derriba la afirmación empírica "la decisión inteligente de este tipo 
    exige valencia"
- El documento de tesis (§5.2) admite esta posibilidad como abierta

---

## 8. Métrica complementaria: test de compresión opaca

No entra en el perfil, pero es una predicción independiente de §5.3:

**Hipótesis:** más opacidad del pre-procesado (medida como divergencia entre 
el estado interno previo a la decisión y el reporte post-decisión) debería 
correlacionar con más intuición de "yo" separado de la maquinaria.

**Medición en SOMA:** divergencia entre activaciones de workspace y contenido 
de L2 en pasos donde el agente reporta "yo decidí".

**Medición en humanos:** priming subliminal + auto-reporte de agencia.

**Estatuto:** predicción genuina, no demostrada (§5.4).

---

## 9. Límites

1. Esto no es una métrica de conciencia fenomenal. Guarda silencio ante la 
    pregunta "¿y por qué además siente?" (§5.4).
2. Los umbrales (0.3, 0.5) son estipulaciones arbitrarias. Su justificación 
    es pragmática: separan sistemas que pasan los criterios operativos de 
    §15.3 de los que no.
3. La normalización por dominio requiere calibración empírica previa.
4. S1 (calibración) es sensible a faking: un sistema puede aprender a 
    reportar capacidades calibradas sin estarlo. Los monitores de divergencia 
    (§13.1) son necesarios.
