# Reference Analysis

Analyze actual supplied files before extracting rules. The goal is a reusable watercolor system, not imitation of one exact sample.

## Evidence Pass

For every usable reference, inspect:

- dimensions and canvas ratio when available
- paper tone and visible texture
- approximate block count
- block size distribution
- edge softness
- pigment transparency
- overlap behavior
- negative space
- dominant and supporting hues
- use of dark anchors
- background simplification
- degree of figurative readability
- presence or absence of outlines
- level of human or object detail
- sample-specific subjects, text, or compositions that should not be copied

Use metadata for exact dimensions. Treat percentages and visual estimates as approximate unless measured.

## Synthesis Rules

- A repeated trait may become a fixed rule.
- A trait that varies while family resemblance survives becomes a variable rule.
- A trait appearing only once remains sample residue.
- With one reference, report observed traits rather than claiming a broad style frequency.
- Separate observation from interpretation.
- Do not copy exact subjects, words, logos, or compositions into the reusable prompt.

## Output Structure

```markdown
## Style Name
[concise name]

## One-sentence Definition
[specific visual definition]

## Observed Evidence
- Paper:
- Shape language:
- Color:
- Edge behavior:
- Transparency:
- Overlap:
- Negative space:
- Human/object detail:
- Background:

## Fixed System
[non-negotiable traits]

## Variable System
[safe variation axes]

## Sample Residue — Do Not Reuse
[source-specific subjects, words, exact palettes, or layouts]

## Reusable Prompt
[base production prompt]

## Randomization Block
[variation axes]

## Avoid List
[negative constraints]

## Confidence and Limitations
[sample size, unreadable files, uncertain traits]
```

When analysis is followed by generation, preserve the fixed system while deliberately choosing a new combination of variable traits.
