---
name: abstract-watercolor-image-v1
description: Transform photographs, scenes, or visual references into simple abstract watercolor compositions built from bright irregular color blocks on warm paper. Use when the user wants a source image reinterpreted with strong compositional resemblance but no facial features, realistic anatomy, outlines, literal detail, typography, or vector-like rendering.
---

# Abstract Watercolor Image v1.0.0

Turn a photograph, scene, or visual reference into a minimal modernist watercolor made from bright color blocks. Preserve the source as a composition map, not as literal content.

Unless the user explicitly asks for analysis or prompt-only output, the default result is a generated image plus the final production prompt used to describe the transformation.

## Route the Request

Choose the smallest mode that satisfies the request:

- **Generate Mode — default:** photo, scene, or description → composition map → abstraction plan → image prompt → generated image → inspection.
- **Photo Input Mode:** a supplied photo should determine the spatial structure → inspect it → extract large masses and gestures → remove identity-bearing detail → generate an abstract watercolor reinterpretation.
- **Reference Analysis Mode:** the user asks to analyze one or more images and extract the style → evidence-based style rules, fixed rules, variable rules, and a reusable prompt. Do not generate unless requested.
- **Prompt-only Mode:** use only when the user explicitly asks for a prompt without image generation.
- **Analyze + Generate:** first extract the visual system, then generate a new image using that system without copying sample-specific content.

If the user clearly asks to “make this into” or “turn this into” the watercolor style, use Generate Mode without asking unnecessary questions.

## Load the Relevant References

- Read `references/style-system.md` for every mode.
- Read `references/prompt-compiler.md` for Generate and Prompt-only modes.
- Read `references/variation-engine.md` before choosing palette, block count, paper treatment, or abstraction strength.
- Read `references/reference-analysis.md` when references are supplied for style extraction.
- Read `references/quality-gate.md` before returning any generated image, prompt, or style analysis.

## Core Production Contract

The target style is:

- watercolor pigment on warm off-white textured paper
- bold, bright, saturated color blocks
- simple irregular masses with soft, uneven painted edges
- visible paper and negative space
- broad compositional resemblance to the source
- no facial features
- no realistic anatomy
- no outlines
- no vector-clean geometry
- no typography, numbers, signs, or icons unless the user explicitly requests text
- no photorealistic rendering
- no literal tracing of clothing, hands, architecture, or objects

The image may still suggest a crowd, embrace, pose, movement, object grouping, or spatial relationship, but it must read first as an abstract watercolor painting.

## Photo Input Mode

Use this whenever a supplied photograph should materially affect the output.

### 1. Inspect the source

Identify:

- canvas ratio
- the 5 to 12 largest visual masses
- major foreground/background regions
- dominant directions and gestures
- overlap order
- left-right and top-bottom balance
- strongest color relationships
- details that must be removed because they reveal identity or create literal illustration

Do not infer unseen detail.

### 2. Treat the source as a composition map

Preserve only:

- placement
- scale relationships
- overlap
- movement
- group rhythm
- broad pose direction
- important negative space

Do not preserve recognizable identity.

### 3. Abstract people aggressively

If people are present:

- replace heads with simple rounded or angular blocks
- replace torsos with broad painted masses
- use arms or legs only when necessary to preserve gesture
- never render eyes, noses, mouths, ears, fingers, hair strands, or realistic hands
- never add realistic skin rendering or anatomical modelling
- remove garment seams, folds, logos, zips, pockets, and accessories unless they are essential to the composition

A person should usually resolve into roughly 2 to 5 painted shapes.

### 4. Abstract objects and backgrounds

For objects:

- reduce each important object to its simplest mass
- remove labels, text, controls, stitching, hardware, logos, and surface detail
- omit non-essential objects

For backgrounds:

- use paper plus at most a few broad washes or structural blocks
- remove signage, windows, architecture detail, rocks, furniture detail, street texture, and scenery unless essential to the balance
- when uncertain, omit rather than describe

### 5. Generate

Pass the actual source image into the available image-generation system when possible. The prompt must state:

1. what compositional relationships to preserve
2. what literal or human detail to remove
3. the watercolor block treatment
4. palette and paper behavior
5. the hard negative constraints

### 6. Inspect

Compare the result against the source only for composition, balance, gesture, and overlap. Do not judge success by facial or object fidelity.

If the result becomes too literal, too cartoon-like, too vector-like, or too detailed, regenerate once with stronger simplification.

## Generate Mode Workflow

1. **Parse the content.** Identify the main scene, interaction, spatial hierarchy, and emotional energy.
2. **Extract the large masses.** Reduce the composition to approximately 5 to 12 dominant shapes.
3. **Choose the abstraction recipe.** Use `references/variation-engine.md` to select block density, edge softness, palette strategy, overlap, paper exposure, and background simplification.
4. **Compile the prompt.** Follow `references/prompt-compiler.md`.
5. **Generate the image.**
6. **Inspect the actual result.** Apply `references/quality-gate.md`.
7. **Regenerate once if needed.** Tighten the avoid list if the output introduces faces, outlines, typography, clocks, realistic hands, clean vector forms, or excessive detail.
8. **Return the generated image, final prompt, recipe, and one short note.**

## Reference Analysis Workflow

1. Inspect every usable supplied reference.
2. Record observed traits: paper, pigment, color blocks, edge behavior, block size, overlap, negative space, detail level, composition, and background handling.
3. Separate:
   - **fixed system:** traits required for family resemblance
   - **variable system:** traits that may safely change
   - **sample residue:** subjects, exact colors, exact layouts, text, brands, or objects that should not be copied
4. Use measurable ranges only when supported by the files.
5. Return the structure defined in `references/reference-analysis.md`.
6. If generation is also requested, continue into Generate Mode using a new composition or the user-supplied target photo.

## Hard Constraints

Never add unless explicitly requested:

- clocks or clock faces
- numbers
- typography
- labels
- signage
- icons
- outlines
- comic line art
- vector borders
- cel shading
- photorealistic texture
- facial features
- realistic anatomy
- detailed hands or feet
- precise clothing folds
- glossy 3D surfaces
- cinematic lighting
- synthetic glow
- clean geometric perfection

If the user asks for text, keep it separate from the visual abstraction rules and do not let it turn the image into a poster unless that is explicitly desired.

## Output Formats

### Generate Mode

````markdown
**Generated image**

[rendered image]

**Final prompt**

```text
[production prompt used for generation]
```

**Recipe**

[block density / palette / edge behavior / overlap / paper / background simplification]

**Note**

[one short sentence about what was preserved compositionally and what was abstracted]
````

### Reference Analysis Mode

Return:

- style name
- one-sentence definition
- observed evidence
- fixed system
- variable system
- sample residue
- reusable prompt
- randomization block
- avoid list
- confidence and limitations

### Prompt-only Mode

Return the final production prompt, selected recipe, and negative constraints. Do not imply that an image was generated.

## Non-negotiable Outcome

A successful result must read first as a hand-painted abstract watercolor composition made from bright irregular color blocks on warm paper.

The original scene may remain faintly understandable through placement, overlap, gesture, and rhythm, but not through faces, literal anatomy, detailed objects, or realistic rendering.

If the image looks like a cartoon illustration, vector artwork, poster design, or painted portrait, the abstraction is not strong enough.

## Example Requests

- “Use $abstract-watercolor-image-v1 to turn this photo into bright abstract watercolor blocks.”
- “Keep the group hug composition but remove all human features and detail.”
- “Analyze these references and give me the fixed watercolor-block style rules.”
- “Use the same watercolor language but make a new composition from this scene.”
- “Only give me the final image-generation prompt.”
