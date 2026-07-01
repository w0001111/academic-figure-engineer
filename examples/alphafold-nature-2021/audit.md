# Figure Audit

## Scientific audit

- The figure only includes high-level components supported by the public AlphaFold method description: sequence, MSA, templates, MSA/pair representations, Evoformer, recycling, structure module, 3D structure output, and confidence estimates.
- Every node and edge has an evidence field in `figure-spec.yaml`.
- The Evoformer block is highlighted as the central representation reasoning module, but the figure does not imply that all components are novel.
- The recycling arrow is dashed and marked as medium-confidence because the SVG abstracts implementation details into a simplified conceptual feedback path.

## Copyright and originality audit

- The SVG is not copied, traced, or adapted from any original figure in the Nature article.
- The layout, colors, shapes, and grouping are original to this repository.
- The example cites the original paper and clearly labels the output as an educational reconstruction.

## Visual audit

- The SVG uses real text elements.
- The SVG includes `viewBox`, `title`, `desc`, semantic group IDs, markers, and embedded styles.
- The layout is left-to-right and intended for double-column display.
- The diagram uses restrained colors and does not rely on color alone: the key module is also indicated by label and border weight.

## Omitted details

- Low-level attention equations.
- Training losses.
- Dataset curation details.
- Full implementation details of recycling.
- Original paper figure layout and styling.
