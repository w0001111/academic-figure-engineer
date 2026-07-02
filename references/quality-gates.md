# Quality Gates

## Gate A — Scientific correctness

Pass only when all answers are yes.

- Is the figure question explicit?
- Does every major block correspond to a real component?
- Does every arrow represent data, control, dependency, supervision, or feedback?
- Are offline, training, inference, and online stages correctly separated?
- Are equations, variables, and tensor dimensions consistent with the source?
- Is the actual contribution visually identified without exaggeration?
- Are the outputs and system responses correctly distinguished?
- Are physical and computational components grouped appropriately?

## Gate B — Information architecture

Pass only when all answers are yes.

- Is there one dominant storyline?
- Is the entry point obvious?
- Are there at most three hierarchy levels?
- Are semantically related variables grouped?
- Is the main path limited to approximately 5–9 major blocks?
- Can tertiary information be removed without damaging the logic?
- Is the figure simpler than the full method section?

## Gate C — Wireframe clarity

Pass only when all answers are yes.

- Can the central message be understood in grayscale?
- Can the proposed contribution be found within five seconds?
- Are the major zones visually separated?
- Are equivalent branches aligned?
- Are there no avoidable line crossings?
- Are feedback paths distinct from forward flow?
- Are labels short enough for the target node sizes?

## Gate D — Final rendering

Pass only when all answers are yes.

- No text is clipped or overflowing.
- No arrows intersect labels or pass through nodes.
- Node spacing is consistent.
- Typography is readable at target paper width.
- Borders and arrows use consistent weights.
- Color is not required to decode the structure.
- The SVG renders correctly in a browser and vector editor.
- The figure contains no unnecessary decorative effects.

## Revision trigger

Revise before delivery when:

- any item in Gate A fails;
- two or more items in Gate B or C fail;
- three or more items in Gate D fail;
- the self-critique cannot state the figure's central message in one sentence.
