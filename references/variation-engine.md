# Variation Engine

Variation changes how the same watercolor-block system is expressed without breaking its identity.

## Block Density

- **sparse:** 5 to 8 dominant blocks
- **medium:** 8 to 12 dominant blocks
- **dense:** 12 to 16 blocks, still with clear negative space

## Edge Treatment

- soft feathered bleed
- pooled pigment edge
- dry-brush interruption
- clean brush-loaded edge with slight wobble
- mixed soft and dry edges

## Transparency

- mostly opaque pigment
- opaque foreground + translucent supporting washes
- layered translucent overlap
- wash-heavy background + stronger foreground blocks

## Palette Strategy

- warm-led with cool anchors
- cool-led with coral/pink accents
- balanced rainbow-like distribution without becoming multicolor noise
- limited 5-hue set
- bright set + navy/indigo anchor

## Shape Logic

- rounded organic masses
- angular cut-paper-like masses painted in watercolor
- elongated bands for limbs or directional movement
- overlapping central cluster
- vertical stacked masses
- low crouched cluster
- dispersed figures with paper gaps

## Background Strategy

- bare paper
- one broad pale wash
- two broad washes defining depth
- one dark structural block
- almost no background, only subject masses

## Abstraction Strength

- **medium:** source remains easy to parse compositionally
- **high:** source reads through major gesture and balance only
- **extreme:** image becomes nearly non-figurative while retaining source rhythm

Default to **high** unless the user asks for more recognizable structure.

## Selection Rules

- Prefer fewer, larger shapes over many small ones.
- If the output feels illustrative, increase abstraction strength before changing palette.
- If the output feels vector-like, soften edges and add pigment variation.
- If it feels muddy, reduce overlap and restore paper gaps.
- If it feels too literal, remove secondary shapes and human-specific detail.
- If it feels chaotic, reduce the palette to 5 to 7 hues plus one dark anchor.
- Keep the source's spatial rhythm even when changing exact colors.

## Recipe Record

Record the chosen recipe as:

```text
[block density / abstraction strength / palette strategy / edge treatment / transparency / overlap / background strategy]
```
