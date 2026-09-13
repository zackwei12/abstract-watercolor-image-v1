# Abstract Watercolor Image v1.0.0

A Codex-compatible image skill for transforming photographs, scenes, and visual references into **simple abstract watercolor compositions made from bright irregular color blocks on warm textured paper**.

The callable skill name is `abstract-watercolor-image-v1`.

## Visual Direction

The skill preserves only the source image's broad composition, overlap, movement, and visual rhythm. It deliberately removes literal detail.

Typical output characteristics:

- warm off-white watercolor paper
- bright saturated blocks such as hot pink, coral, orange, yellow, lime, teal, turquoise, sky blue, indigo, navy, grey-blue, and soft brown
- large irregular hand-painted shapes
- soft feathered watercolor edges
- visible pigment pooling and paper grain
- generous negative space
- no facial features
- no realistic anatomy
- no outlines or vector-clean geometry
- no typography, numbers, labels, signs, icons, or clock faces unless explicitly requested
- no photorealism or cartoon-character rendering

## What It Is For

Use this skill when you want to:

- turn a reference photo into abstract watercolor color blocks
- keep the broad gesture or spatial structure while removing identity-bearing detail
- convert people into a few overlapping painted shapes rather than illustrated figures
- simplify busy scenes into 5 to 12 dominant masses
- analyze reference images and extract a reusable watercolor-block style system
- generate a production-ready prompt for the same style

## Requirements

- Codex or another compatible Skill runtime
- image inspection when references are supplied
- image generation when Generate Mode is requested

The repository contains no API keys, external fonts, or required downloaded assets.

## Installation

Clone the repository into your Codex skills directory:

```bash
git clone https://github.com/zackwei12/abstract-watercolor-image-v1.git \
  ~/.codex/skills/abstract-watercolor-image-v1
```

Restart Codex if the skill does not appear immediately.

## Usage

Generate from a photo:

```text
Use $abstract-watercolor-image-v1 to turn this photo into bright abstract watercolor blocks.
```

Keep the composition but remove literal human detail:

```text
Use $abstract-watercolor-image-v1 to preserve the group arrangement and movement, but remove all facial features and anatomy.
```

Analyze references:

```text
Use $abstract-watercolor-image-v1 to analyze these references, separate fixed and variable style rules, and give me a reusable prompt.
```

Prompt only:

```text
Use $abstract-watercolor-image-v1 to return only the final production prompt.
```

## Request Modes

- **Generate:** source or description → composition map → abstraction recipe → image prompt → generated image → inspection
- **Photo Input:** inspect source → preserve large masses and gesture → remove identity-bearing detail → generate
- **Reference Analysis:** inspect files → fixed system / variable system / sample residue → reusable prompt
- **Prompt-only:** final production prompt + recipe + negative constraints
- **Analyze + Generate:** extract a visual system first, then generate a new result

## Repository Structure

- `SKILL.md`: routing, workflow, constraints, and output contract
- `references/style-system.md`: fixed visual identity and anti-style rules
- `references/prompt-compiler.md`: production prompt structure
- `references/variation-engine.md`: controlled variation axes
- `references/reference-analysis.md`: evidence-based analysis workflow
- `references/quality-gate.md`: checks before returning a result
- `agents/openai.yaml`: Codex UI metadata
- `evals/evals.json`: reusable evaluation cases
- `examples/README.md`: guidance for adding example outputs
- `LICENSE`: MIT license

## Style Summary

**Abstract watercolor + bright irregular color blocks + warm paper + no human features + no outlines + minimal detail + strong compositional resemblance to the source.**

## License

MIT. See [LICENSE](LICENSE).
