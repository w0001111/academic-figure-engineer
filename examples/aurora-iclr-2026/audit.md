# Figure Audit

## Scientific audit

- The figure includes the high-level Aurora components explicitly described in the supplied PDF: multimodal tokenization, ViT/BERT encoders, token distillation, modality-guided self-attention, modality fusion, condition decoding, prototype retrieval, prototype-guided flow matching, and probabilistic forecasting.
- Every major node and edge has an evidence field in `figure-spec.yaml`.
- Equations (1)-(25), Section 3.1, Section 3.2, and Algorithm 1 are used as evidence anchors.
- Benchmark results and dataset details are intentionally omitted because the figure's central message is model architecture, not experimental evaluation.

## Copyright and originality audit

- The SVG is not copied, traced, or adapted from the original paper figures.
- The layout, colors, grouping, and visual hierarchy are original to this repository.
- The example cites the paper and clearly labels the output as an educational reconstruction.

## Visual audit

- The SVG uses real text elements.
- The SVG includes `viewBox`, `title`, `desc`, semantic group IDs, markers, and embedded styles.
- Proposed Aurora components are highlighted with accent color and stronger border.
- The layout is left-to-right and intended for double-column display.

## Omitted details

- Exact tensor dimensions for every intermediate state.
- Corpus construction and evaluation summary.
- Low-level implementation details of each Transformer block.
- Original paper figure layouts and styling.
