# Quality Gate

Inspect the actual generated image before returning it.

## Generated Image

- The result reads first as abstract watercolor, not cartoon illustration.
- Warm paper or paper-like texture remains visible.
- The main shapes are large, simple, irregular, and hand-painted.
- Color is bright and saturated rather than greyed out.
- Edges show watercolor softness, wobble, bleed, or pigment pooling.
- No facial features are visible.
- No realistic anatomy is visible.
- No detailed hands, fingers, hair strands, or clothing folds are visible.
- No black outlines or vector borders are visible.
- No clock, clock face, numbers, text, labels, signage, or icons were introduced unless explicitly requested.
- No glossy 3D rendering, hard shadows, cinematic lighting, or photorealistic background detail is present.
- The source remains faintly recognizable through composition, gesture, overlap, balance, or visual rhythm.
- Non-essential details have been removed.
- The image contains enough visible paper or breathing room to avoid looking cluttered.

## Composition Preservation

When a source photo is used:

- compare only broad placement, scale, overlap, direction, and balance
- do not judge success by face or object fidelity
- confirm major gestures survived abstraction
- confirm the result did not introduce new literal objects or icons
- confirm background simplification did not erase an essential compositional anchor

## Failure Handling

If the result is too literal:

- reduce figure detail
- remove small shapes
- strengthen “painted masses only”
- increase abstraction level

If the result is too vector-like:

- soften edges
- add pigment pooling and uneven tone
- remove geometric precision

If the result is too busy:

- remove secondary blocks
- expose more paper
- reduce background treatment

If the result is too muddy:

- reduce translucent overlap
- separate adjacent hues
- keep darker anchors limited

If a central check fails, revise and regenerate once. If the second result still fails, state the limitation rather than describing the output as fully successful.

## Reference Analysis

- Every claimed trait comes from an inspected file.
- Observations and interpretations are distinguishable.
- Fixed rules are supported by repetition or clearly labeled as single-reference observations.
- Variable rules represent real or safely proposed variation.
- Sample-specific content is isolated as residue.
- Confidence matches sample size and file quality.

## Prompt-only Output

- The prompt describes medium, surface, composition preservation, abstraction, palette, paint treatment, background simplification, and negatives.
- The response does not claim an image was generated or inspected.
