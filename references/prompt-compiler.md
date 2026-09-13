# Prompt Compiler

Use this reference for Generate and Prompt-only modes.

## Required Prompt Fields

Compile the final production prompt in this order:

1. **Medium and surface**
2. **Source-composition preservation**
3. **Abstraction behavior**
4. **Palette and paint treatment**
5. **Background simplification**
6. **Hard negative constraints**

## Production Prompt Template

```text
Transform the source into a simple abstract watercolor color-block painting on warm off-white textured paper.

Preserve only the broad composition, relative placement, overlap, movement, and visual rhythm of the source. Identify the largest visual masses and translate them into a small number of irregular painted blocks. Keep important left-right and foreground-background balance, but do not trace literal detail.

Reduce people and objects aggressively. People should become only a few overlapping painted masses with no facial features, realistic anatomy, fingers, hair strands, skin rendering, or detailed clothing. Objects should keep only the simplest necessary silhouette or mass. Omit non-essential details and background clutter.

Use bright saturated watercolor pigments such as hot pink, coral, orange, vermilion, yellow, lime, teal, turquoise, sky blue, indigo, navy, muted grey-blue, and soft brown. Use soft uneven edges, slight pigment pooling, subtle paper grain, natural tonal variation inside each block, and occasional translucent overlap. Leave visible paper around and between shapes.

No clock, no clock face, no numbers, no typography, no labels, no signage, no icons, no facial features, no realistic people, no detailed hands, no realistic anatomy, no outlines, no vector art, no comic line art, no cel shading, no photorealism, no 3D rendering, no glossy surfaces, no hard shadows, no synthetic glow, no detailed background, no clean geometric perfection.
```

## Compilation Rules

- Name the visible medium: watercolor pigment on textured paper.
- Describe composition preservation in spatial terms, not semantic terms.
- Use approximately 5 to 12 dominant masses for a typical photo.
- Do not ask the image model to preserve identity.
- If the source contains people, explicitly remove faces and realistic anatomy.
- If the source is busy, simplify the background before simplifying the main visual interaction.
- If one gesture matters, name that gesture structurally, for example: “preserve the long horizontal band created by the reaching arm.”
- Avoid vague wording such as “artistic”, “stylized”, or “minimal” without concrete visual constraints.
- Keep palette language saturated and physical. Do not weaken it with “pastel” or “muted” unless requested.
- State hard negatives explicitly when the source contains common failure triggers such as signage, clocks, text, faces, or architectural detail.

## Compact Negative Bank

```text
clock, clock face, numbers, text, labels, signage, icons, facial features, eyes, nose, mouth, ears, fingers, realistic hands, realistic people, realistic anatomy, detailed clothing, black outline, comic art, vector art, cel shading, photorealism, 3D, glossy surfaces, hard shadows, synthetic glow, detailed background, logos, clean geometric perfection
```
