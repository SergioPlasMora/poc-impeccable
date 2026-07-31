---
target: /impeccable critique the landing page
total_score: 21
max_score: 28
na_heuristics: 5,7,9
p0_count: 0
p1_count: 3
timestamp: 2026-07-31T03-04-55Z
slug: impeccable-poc-src-pages-index-astro
---
⚠️ DEGRADED: single-context (spawn_agent unavailable in this session; browser automation unavailable)

## Design Health Score

| # | Heuristic | Score | Key Issue |
|---|---|---:|---|
| 1 | Visibility of System Status | 2/4 | La página comunica el recorrido, pero no hay estado de compra o confirmación porque el catálogo aún es estático. |
| 2 | Match System / Real World | 4/4 | El lenguaje de piel, clima, salida, corazón, fondo y trazabilidad encaja con el usuario. |
| 3 | User Control and Freedom | 3/4 | Hay navegación por anclas y salida clara a inicio; no existe todavía control de selección o compra. |
| 4 | Consistency and Standards | 3/4 | El sistema visual es muy consistente; las acciones cambian entre “Ver decants”, “Explorar” y “Ver la selección”. |
| 5 | Error Prevention | n/a | No hay formularios ni transacciones implementadas todavía. |
| 6 | Recognition Rather Than Recall | 3/4 | La jerarquía es visible, pero los perfiles de ejemplo no permiten reconocer productos comprables. |
| 7 | Flexibility and Efficiency | n/a | No aplica todavía a una landing Persuade sin flujo operativo. |
| 8 | Aesthetic and Minimalist Design | 4/4 | La cartelera de dos tintas es enfocada y evita el catálogo de tarjetas genéricas. |
| 9 | Error Recovery | n/a | No hay estados de error ni acciones mutables en esta versión. |
| 10 | Help and Documentation | 2/4 | El proceso explica la idea, pero falta definir “decant” y resolver dudas de autenticidad, envío y compra. |
| **Total** |  | **21/28** | **Good — 75%; sólida base, pero aún no lista como tienda.** |

## Design Specificity Verdict

La landing sí se siente hecha para Estela: la cartelera tipográfica, la prueba en piel y el pasaporte de trazabilidad forman una combinación difícil de trasladar intacta a otra categoría. La dirección visual es memorable y coherente con el rechazo a la fotografía genérica.

La especificidad todavía está incompleta en la capa comercial. “Selección de ejemplo”, “[por confirmar]” y los tres perfiles sin producto, precio ni acción de compra hacen que el visitante entienda el punto de vista, pero no pueda completar el trabajo principal. El resultado se siente más manifiesto de marca que tienda en línea.

El detector determinista encontró 0 hallazgos en `impeccable-poc/src/pages/index.astro`. No hubo falsos positivos. No hay overlay visual disponible: el entorno no expuso un conector de navegador y el intento de Playwright no completó la apertura del navegador.

## Overall Impression

Es una landing con una voz propia, una primera pantalla clara y una metáfora visual bien traducida. Su oportunidad más grande es convertir la confianza editorial en una acción comercial real: el usuario debe poder pasar de “esto tiene sentido” a “quiero probar este decant” sin encontrarse con placeholders.

## What's Working

- **La primera pantalla tiene tesis y acción.** “Conoce el perfume antes de comprarlo” explica el valor en una línea y el CTA lleva a la selección.
- **La trazabilidad es una demostración, no solo una promesa.** El pasaporte convierte origen, lote, fecha y volumen en una interfaz concreta.
- **La gramática visual es distintiva.** Azul ultramar, marfil, Archivo Narrow, filas abiertas y una sola inversión tonal evitan el look de perfumería genérica.

## Priority Issues

### [P1] El catálogo no permite comprar ni evaluar un decant real

**Por qué importa:** El objetivo de Estela es probar y comprar en línea; hoy los tres perfiles son ejemplos, todos llevan a trazabilidad y ninguno muestra casa, notas reales, precio MXN, disponibilidad, producto o siguiente paso comercial.

**Arreglo:** Sustituir los perfiles por productos reales con nombre, casa, familia/notas, 5 ml y 10 ml, precio, disponibilidad y una acción “Ver decant” o “Agregar al carrito”. Si el backend aún no existe, usar una ruta de producto o un CTA de lista de espera, no una promesa de catálogo que no funciona.

**Suggested command:** `$impeccable harden` y `$impeccable clarify`

### [P1] El placeholder visible rompe la promesa de confianza

**Por qué importa:** “[por confirmar]” en el pasaporte y “El catálogo real se integra aquí” le dicen al primer visitante que está viendo una maqueta. En una categoría donde la desconfianza es el problema central, el vacío pesa más que la estética.

**Arreglo:** Integrar al menos una ficha real con origen, lote, fecha de llenado y volumen confirmados. Si aún no hay datos, convertir la sección en una explicación honesta de cómo funcionará la trazabilidad y quitar la apariencia de ficha ya lista para compra.

**Suggested command:** `$impeccable clarify`

### [P1] La promesa “8–12 horas” se lee como cifra absoluta

**Por qué importa:** `PRODUCT.md` prohíbe presentar longevidad o proyección como hechos absolutos; el marcador visual es tan grande que domina la interpretación del visitante.

**Arreglo:** Cambiarlo a “varios días de prueba” o acompañarlo de “referencia variable según piel, clima y aplicación” en el mismo bloque, no solo en la nota del catálogo.

**Suggested command:** `$impeccable clarify`

### [P2] “Muestra” contradice la terminología de marca

**Por qué importa:** El manifiesto dice “una muestra de treinta segundos”, aunque la marca decidió usar “decant” y evitar “muestra”/“sample”. Es un detalle pequeño, pero erosiona la precisión del tono.

**Arreglo:** Escribir “probar en papel durante treinta segundos” o “una prueba de treinta segundos en tienda”.

**Suggested command:** `$impeccable clarify`

### [P2] El recorrido móvil no conserva una acción comercial visible

**Por qué importa:** Casey puede llegar desde el review de un perfume, leer varios bloques y perder el CTA después del hero. La navegación queda arriba y el cierre repite una acción que todavía no conduce a compra.

**Arreglo:** Añadir una acción persistente o repetir “Ver decants” justo después de la selección, con un destino real. Mantener todos los objetivos táctiles en al menos 44×44 px.

**Suggested command:** `$impeccable adapt`

## Persona Red Flags

### Jordan — primera compra

- “Decant” no se define de forma literal en la primera pantalla; se entiende por contexto, no por una frase inequívoca.
- “Selección de ejemplo” y `[por confirmar]` hacen que no sepa qué puede comprar hoy.
- No hay una respuesta visible a “¿es auténtico?”, “¿cuánto cuesta?” o “¿cómo llega?”.

### Riley — usuario que prueba los bordes

- Los tres enlaces de catálogo llevan al mismo bloque de trazabilidad; no hay rutas diferenciadas ni estados de disponibilidad.
- No existe estado vacío, agotado, error de carga o recuperación si un producto deja de estar disponible.
- La cifra 8–12 puede parecer una garantía aunque el producto depende de piel, clima y aplicación.

### Casey — móvil y con prisa

- La acción principal está arriba; después de una página larga no hay un CTA comercial contextual junto a la selección.
- La navegación horizontal en móvil puede ocultar enlaces sin una señal visible de desplazamiento.
- La carga de Google Fonts externa puede cambiar la geometría de los titulares o penalizar una conexión lenta.

## Minor Observations

- Los nombres de acción podrían converger en una sola fórmula: “Ver decants” o “Explorar decants”.
- El selector `.passport-copy > p:not(.section-label)` quedó con una referencia obsoleta; no rompe la página, pero conviene limpiarlo.
- El foco visible está bien resuelto y el skip link es una buena base para teclado.
- La visualización no necesita fotografía para funcionar, pero cuando existan fotos propias deben entrar en el catálogo real, no en la hero como decoración.

## Questions to Consider

- ¿La siguiente prioridad es conectar un catálogo real o pulir la persuasión mientras llegan los datos?
- ¿“8–12 horas” es una cifra confirmada para el producto o debe pasar a una formulación condicionada?
- ¿Cuál será la primera acción comercial real: abrir un producto, agregar el primer decant al carrito o iniciar una selección guiada?
