# Final Quality Checklist

Run this checklist before claiming a figure is publication-ready.

## Scientific checks

- [ ] The central message can be stated in one sentence.
- [ ] Every node corresponds to a real component, variable group, dataset, physical subsystem, or algorithmic stage.
- [ ] Every arrow has a defensible meaning: data flow, control flow, dependency, feedback, supervision, or physical coupling.
- [ ] Training-only, inference-only, offline, and online elements are separated when relevant.
- [ ] Equations, dimensions, objectives, and constraints match the supplied sources.
- [ ] The proposed contribution is identifiable but not exaggerated.
- [ ] The figure does not invent modules, datasets, losses, constraints, or performance claims.
- [ ] Any source conflict or missing evidence is stated explicitly.

## Visual checks

- [ ] No label overlaps a node border, arrow, or another label.
- [ ] No arrow passes through a node unless it terminates there.
- [ ] Edge crossings are eliminated or justified by the system structure.
- [ ] Similar concepts use consistent shapes, colors, and line styles.
- [ ] The figure remains readable at 85 mm single-column or 175 mm double-column width.
- [ ] Grayscale printing preserves the main meaning.
- [ ] Text remains real SVG text, not rasterized images.
- [ ] The SVG has a viewBox, title, desc, semantic group IDs, and embedded styles.
- [ ] The caption explains the central message and the most important visual encodings.

## Delivery checks

- [ ] Editable SVG is provided.
- [ ] Figure specification is provided or summarized.
- [ ] Caption is provided.
- [ ] Assumptions and unresolved items are listed.
- [ ] Optional PNG/PDF exports are marked as derived from the SVG.
