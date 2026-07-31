---
name: Estela
description: Cartelera olfativa para probar decants antes del frasco completo.
colors:
  primary: "#1726b8"
  primary-deep: "#111b8d"
  signal: "#f2b134"
  ink: "#f4f0e6"
  ink-soft: "#d9d8ce"
  line: "rgba(244, 240, 230, 0.38)"
  line-signal: "rgba(23, 38, 184, 0.38)"
typography:
  display:
    fontFamily: "Archivo Narrow, Arial Narrow, Arial, sans-serif"
    fontSize: "clamp(4.2rem, 10.3vw, 10.2rem)"
    fontWeight: 600
    lineHeight: 0.82
    letterSpacing: "-0.045em"
  body:
    fontFamily: "DM Sans, Helvetica Neue, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "DM Sans, Helvetica Neue, Arial, sans-serif"
    fontSize: "0.72rem"
    fontWeight: 600
    lineHeight: 1.1
    letterSpacing: "0.08em"
spacing:
  sm: "1.25rem"
  md: "2rem"
  lg: "clamp(5rem, 11vw, 11rem)"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.primary}"
    typography: "700 1rem DM Sans"
    padding: "1rem 1.15rem"
  button-primary-hover:
    backgroundColor: "{colors.primary-deep}"
    textColor: "{colors.ink}"
    padding: "1rem 1.15rem"
  catalogue-row:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.ink}"
    padding: "1.35rem 0"
  catalogue-row-featured:
    backgroundColor: "{colors.signal}"
    textColor: "{colors.primary}"
    padding: "1.35rem 1.25rem"
  passport:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.primary}"
    padding: "clamp(1.25rem, 3vw, 2rem)"
---

# Design System: Estela

## Overview

**Creative North Star: “La cartelera olfativa”**

Estela se expresa como una hoja de lineup que se lee desde lejos: una tinta dominante, una tinta de contraste, una señal azafrán y una jerarquía tipográfica que hace que el producto se entienda antes de adornarlo. La superficie usa azul ultramar como campo continuo, marfil como voz y azafrán solo donde una prueba o una recomendación necesita tomar el frente; la página se siente impresa, directa y segura, no perfumada ni aspiracional.

El sistema se apoya en tipografía condensada para nombres, titulares y marcadores, y en una sans de lectura para explicar notas, clima y trazabilidad. Las filas, reglas finas y cambios de escala hacen visible la clasificación sin llenar la pantalla de tarjetas. El pasaporte del decant es la firma funcional: la confianza se muestra con campos concretos.

**Key Characteristics:**

- Una superficie azul continua con tinta marfil de alto contraste.
- Una señal azafrán reservada para prueba, recomendación y puntuación visual.
- Jerarquía por escala y saltos de línea, no por imágenes o adornos.
- Filas editoriales con una sola variación invertida para señalar énfasis.
- Geometría CSS y tipografía como contenido; fotografía omitida cuando no es real.

## Colors

La paleta mantiene dos tintas estructurales y suma una señal azafrán: el azul lleva el campo, el marfil lleva la información y el azafrán marca lo que merece una segunda mirada. El azul profundo solo aparece en estados de interacción.

### Primary

- **Azul ultramar** (#1726b8): superficie principal, texto sobre tinta clara y ancla de la marca.
- **Azul profundo** (#111b8d): estado hover de acciones y profundidad tonal sin introducir otro color.
- **Azafrán de señal** (#f2b134): marcador de prueba, fila recomendada, puntuación de trazabilidad y puntuación final de marca.

### Neutral

- **Marfil de impresión** (#f4f0e6): texto principal, CTA, fila destacada y pasaporte.
- **Marfil suave** (#d9d8ce): texto secundario en el campo azul.
- **Regla translúcida** (rgba(244, 240, 230, 0.38)): separadores estructurales y bordes de control.
- **Regla sobre azafrán** (rgba(23, 38, 184, 0.38)): separadores dentro de superficies azafrán.

**The Signal Rule.** El azafrán aparece en regiones con una función clara —prueba, recomendación o trazabilidad—; no se dispersa como confeti decorativo.

## Typography

**Display Font:** Archivo Narrow (with Arial Narrow, Arial, sans-serif)

**Body Font:** DM Sans (with Helvetica Neue, Arial, sans-serif)

**Character:** La display es comprimida, contundente y editorial; la sans de cuerpo baja la velocidad para explicar sin perder precisión.

### Hierarchy

- **Display** (600, `clamp(4.2rem, 10.3vw, 10.2rem)`, 0.82): titulares de apertura y cierre, con tracking negativo hasta `-0.045em`.
- **Headline** (500, `clamp(3rem, 6.6vw, 7.1rem)`, 0.86): encabezados de sección y tesis.
- **Title** (600, `clamp(2.4rem, 5vw, 5.5rem)`, 0.85): nombres de perfiles dentro de la cartelera.
- **Body** (400, 16px, 1.5): explicación y evidencia, en medidas cortas de aproximadamente 65–75ch.
- **Label** (600, 0.72rem, 0.08em, uppercase): metadatos, estado y navegación secundaria.

**The Headline-First Rule.** Los bloques entran por su titular; no usar etiquetas tipo eyebrow antes de una cabeza para fabricar jerarquía.

## Layout

El contenedor ocupa como máximo `92rem` y usa padding lateral fluido (`clamp(1.25rem, 2.6vw, 2.75rem)`). La apertura es una composición de dos columnas: titular y acción a la izquierda, marcador de prueba a la derecha. En móvil se convierte en una secuencia vertical con navegación desplazable horizontalmente.

Las secciones alternan composición de dos columnas y listas de ancho completo. El ritmo vertical amplio (`clamp(5rem, 11vw, 11rem)`) separa tesis, catálogo, proceso, trazabilidad y cierre. Las filas de catálogo conservan una columna de rango, una columna dominante de nombre, una columna de metadatos y una acción.

## Elevation & Depth

El sistema es plano por defecto: no usa sombras ni glass. La profundidad se comunica por continuidad del campo azul, inversión marfil o azafrán en la fila destacada y separación mediante reglas de 1px. El único gesto de movimiento con peso es la revelación vertical del marcador de prueba en la primera pantalla.

**The Flat-By-Default Rule.** Una superficie gana jerarquía por tono, tipografía y separación; no por cajas flotantes.

## Shapes

La forma es ortogonal y editorial. No hay radios en la interfaz actual: los CTA, las filas y el pasaporte usan bordes rectos. Las reglas son finas, los controles mantienen altura táctil y el recorte aparece solo en la animación de revelación del cartel.

## Components

### Buttons

- **Shape:** recto, sin radio, con padding de `1rem 1.15rem`.
- **Primary:** marfil sobre azul ultramar; texto DM Sans de peso 700 y una flecha SVG de trazo fino.
- **Hover / Focus:** cambia a azul profundo con texto marfil; focus-visible usa un contorno marfil de 3px con offset de 5px.
- **Secondary:** enlaces de texto sin caja, con subrayado desplazado al pasar el cursor.

### Cards / Containers

- **Catalogue rows:** filas abiertas por reglas, no tarjetas. La fila destacada invierte a marfil y conserva el mismo contenido.
- **Passport:** una sola superficie marfil con campos de definición y un pie de estado; no anidar contenedores.
- **Internal Padding:** filas con `1.35rem` vertical; pasaporte con `clamp(1.25rem, 3vw, 2rem)`.

### Navigation

La navegación es una línea de enlaces centrada entre la palabra-marca y el CTA. En móvil pasa a una segunda línea con desplazamiento horizontal; el CTA permanece visible en la primera fila.

### Signature Component

**Pasaporte del decant:** una ficha editorial que expone origen, lote, fecha de llenado y volumen. Los datos no confirmados permanecen visibles como `[por confirmar]` hasta que el catálogo real los sustituya.

## Do's and Don'ts

### Do:

- **Do** dejar que la escala tipográfica organice la página.
- **Do** usar contenido real de catálogo y trazabilidad cuando esté disponible.
- **Do** mantener el español de México y la terminología de decants, estela, proyección y longevidad.
- **Do** conservar contraste WCAG AA y el comportamiento móvil como criterio de acabado.
- **Do** usar el azafrán para orientar una decisión, no para competir con el CTA principal.

### Don't:

- **Don't** introducir fotos de banco, escenas de lujo o frascos flotando como sustituto de activos reales.
- **Don't** usar nombres, logos o imágenes de marcas de diseñador para vender una interpretación.
- **Don't** prometer duración, proyección o equivalencia absoluta.
- **Don't** volver a un sistema de tarjetas iguales con icono, título y párrafo como estructura de página.
- **Don't** repartir el azafrán en cada enlace, borde o etiqueta hasta volverlo ruido.
