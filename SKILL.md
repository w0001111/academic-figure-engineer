---
name: academic-figure-engineer
description: >
  Analyze academic papers, method sections, equations, code, or rough research notes and convert them into publication-quality academic figures using editable SVG. Use for model architecture figures, research frameworks, prediction-optimization-control pipelines, multi-timescale systems, traffic-energy coupling diagrams, algorithm workflows, graphical abstracts, and experiment validation figures. This skill must first reconstruct the scientific storyline, reduce information, assign hierarchy, select a figure type and layout template, produce a text skeleton and low-fidelity wireframe, attach evidence, and pass quality gates before generating final SVG.
---

# Academic Figure Engineer

## Purpose

Create scientifically accurate, publication-ready academic figures in editable SVG format.

Do not begin by drawing. First reconstruct the scientific logic, decide what the figure must communicate, reduce the information, choose a layout, and only then generate the diagram.

The primary output is an editable `.svg` file. When useful, also provide:

- a self-contained `.html` preview that embeds the SVG;
- a figure specification file;
- a publication caption;
- a short explanation of the visual logic;
- export-ready PDF or PNG versions when the environment supports conversion.

Default output directory: create or use `outputs/academic_figures/` inside the active project unless the user specifies another path. Keep generated SVG, HTML preview, figure specification, and derived exports together.

## Core principles

1. Scientific correctness is more important than visual attractiveness.
2. One figure must communicate one central message.
3. The visual hierarchy must match the logical hierarchy of the method.
4. Every major arrow must represent a real data, control, dependency, or feedback relationship.
5. Do not invent modules, equations, dimensions, datasets, losses, or optimization stages.
6. If supplied text and code disagree, identify the conflict before drawing.
7. Prefer editable vector elements over rasterized screenshots.
8. Avoid generic AI-style decoration, excessive gradients, floating shapes, and meaningless icons.
9. The figure must remain understandable when reduced to single-column or double-column paper width.
10. Use colors only to encode meaning, not decoration.
11. Do not inspect unrelated personal files, memory files, credentials, browser sessions, or project files not provided or clearly required for the figure task.

## Supported inputs

The user may provide any combination of:

- paper PDF or manuscript;
- method section;
- equations;
- pseudocode;
- source code;
- model summary;
- rough notes;
- existing figure;
- target journal or conference;
- desired page or column width;
- presentation requirements.

When multiple sources are supplied, use the following evidence priority unless the user specifies otherwise:

1. executable code and actual tensor flow;
2. formal equations and algorithm definitions;
3. method description;
4. abstract and contribution claims;
5. rough notes or oral descriptions.

Explicitly report material inconsistencies instead of silently choosing one source.

## Workflow

### Step 1: Identify the figure purpose

Determine which single question the figure should answer, such as:

- What is the full research framework?
- How does the model transform inputs into outputs?
- How do prediction, optimization, and control interact?
- What is the traffic-energy coupling mechanism?
- What happens at different timescales?
- How is the experiment or simulation system organized?
- Which module is the paper's primary contribution?

If the requested figure tries to answer several unrelated questions, split it into multiple figures or use clearly separated panels.

### Step 2: Classify the figure type

Choose one primary figure type from `references/figure-types.md`. Use `references/journal-style-presets.md` when the user specifies a target venue or when a default journal style is needed.

Common types include:

- overall research framework;
- model architecture;
- data processing pipeline;
- algorithm workflow;
- multi-timescale coordination;
- hierarchical or bilevel optimization;
- prediction-decision-control loop;
- traffic-energy coupling mechanism;
- experiment validation framework;
- graphical abstract.

Do not mix figure types without a clear reason.

### Step 3: Reconstruct the scientific structure

Extract and verify:

- research objective;
- inputs and data sources;
- preprocessing and feature construction;
- model or optimization modules;
- state variables;
- decision variables;
- constraints;
- losses or objectives;
- information flow;
- temporal order;
- feedback paths;
- outputs;
- claimed innovation modules;
- training-only and inference-only components;
- offline and online stages;
- physical system and computational system boundaries.

For code-based model figures, also identify:

- tensor shapes;
- repeated blocks;
- skip or residual connections;
- fusion operations;
- forecast horizon;
- direct or recursive prediction strategy;
- branches used only during training;
- branches active during inference.

### Step 4: Build a figure specification

Before creating SVG, produce an internal or explicit figure specification based on `templates/figure-spec.yaml`. Use `references/evidence-traceability.md` to attach source evidence to major nodes and arrows.

The specification must include:

- figure question;
- figure purpose;
- central message;
- intended audience;
- figure type;
- layout direction;
- reading entry;
- selected layout template;
- must-show, may-show, and omitted information;
- hierarchy levels;
- panels or zones;
- nodes;
- edges;
- labels;
- innovation highlights;
- dimensions or formulas to display;
- legend requirements;
- caption draft;
- uncertainty or missing information.

Do not create the final SVG until the specification is coherent and major nodes/arrows have evidence fields.

### Step 5: Decide what to omit

Remove details that do not help the figure's central message.

Create three explicit lists:

- must show: indispensable to understand the scientific logic;
- may show: useful if space permits;
- must omit: details that weaken the main story.

Merge semantically related variables. For example, combine temperature, humidity, and wind speed as weather features instead of creating separate main-path blocks.

Usually omit:

- minor hyperparameters;
- long variable lists;
- full equations that can be summarized by a symbol;
- repeated implementation details;
- baseline methods;
- numerical results;
- decorative background objects;
- low-level code functions;
- modules that are irrelevant to the claimed contribution.

Move supporting details to the caption, legend, or manuscript text.

Assign each retained item to one of three content hierarchy levels:

1. major stage, subsystem, or dominant contribution;
2. internal module or parallel branch;
3. annotation, variable, tensor shape, formula, or badge.

Level 3 items should usually not become standalone boxes.

### Step 6: Plan the layout

Use a readable global structure.

Choose one primary layout template from `references/layout-templates.md`. Do not invent a free-form layout unless all templates are unsuitable and the reason is explicit.

Preferred patterns:

- left-to-right for data and model pipelines;
- top-to-bottom for algorithms and decision sequences;
- layered top-to-bottom for hierarchical optimization;
- circular or return arrows only for genuine feedback control;
- aligned parallel branches for multi-source or multi-scale processing;
- separate panels for offline training and online operation;
- separate physical and cyber layers for coupled-system figures.

Use consistent alignment, spacing, and module sizing.

Avoid:

- unnecessary diagonal layouts;
- crossing arrows;
- arrows passing through nodes;
- long labels inside small boxes;
- placing all modules at equal visual importance;
- mixing physical devices, datasets, and algorithms without explicit grouping.

### Step 7: Create a skeleton and wireframe

Before final SVG, produce:

1. a text-only skeleton that is understandable without styling;
2. a low-fidelity wireframe containing only zones, boxes, labels, arrows, and approximate proportions.

The wireframe must establish the entry point, dominant reading path, grouping logic, main contribution, outputs, and any genuine feedback path.

Do not add final colors, decorative icons, gradients, or detailed equations at wireframe stage.

### Step 8: Generate SVG

Follow `references/svg-rules.md` and `references/design-system.md`.

Use semantic SVG groups and stable IDs. Prefer:

- `<g>` for modules and panels;
- `<rect>` for process blocks;
- `<path>` or `<polyline>` for connections;
- `<marker>` for arrowheads;
- `<text>` and `<tspan>` for labels;
- `<defs>` for reusable styles, markers, and filters;
- CSS classes for consistent styling;
- `viewBox` for scalable output.

All primary text must remain real SVG text unless exact font embedding is explicitly required.

### Step 9: Validate the diagram

Perform a scientific and visual audit before delivery. Use `references/quality-gates.md` for pre-SVG scientific and wireframe gates, then use `references/final-quality-checklist.md` as the final gate before claiming publication readiness.

Scientific audit:

- Does every node correspond to a real method component?
- Does every arrow have a defensible meaning?
- Are training and inference flows correct?
- Are prediction and optimization stages ordered correctly?
- Are equations and tensor dimensions consistent?
- Is the claimed innovation visually identifiable?
- Does the figure overstate what the method actually does?

Visual audit:

- Are all labels readable at target size?
- Are similar modules styled consistently?
- Are arrows unambiguous?
- Are there line crossings or overlaps?
- Is the visual emphasis proportional to scientific importance?
- Does grayscale printing preserve meaning?
- Is the figure understandable without oral explanation?
- Is the figure still readable at approximately 85 mm width for single-column or 175 mm width for double-column use?

Revise before final SVG if:

- any scientific correctness gate fails;
- the main path has more than about 5-9 major blocks without grouping;
- there is more than one competing entry point;
- the proposed contribution cannot be located quickly;
- arrows cross unnecessarily;
- labels require paragraph-length text;
- the layout would become unreadable at the target paper width.

### Step 10: Deliver outputs

For bilingual Chinese-English projects, follow `references/bilingual-labeling.md` and keep terminology consistent across labels and captions.

When file generation is available, provide:

1. editable SVG;
2. optional self-contained HTML preview;
3. optional PDF and PNG exports;
4. figure specification;
5. caption;
6. a concise note describing any uncertain or assumed content.

When file generation is not available, provide the complete SVG source and the figure specification.

## Visual hierarchy rules

Use no more than three content hierarchy levels:

1. primary storyline, major stage, or subsystem;
2. secondary module, branch, or output;
3. annotation, variable, tensor shape, formula, or badge.

Figure and panel titles may sit outside this content hierarchy, but they should not introduce extra visual competition.

Use a restrained semantic palette. A reasonable default is:

- neutral gray for context and existing components;
- one primary accent for the proposed method;
- one secondary accent for outputs or decisions;
- warning or risk color only for uncertainty, anomalies, or constraint violations.

Do not rely on color alone. Combine color with labels, borders, line types, or panel position.

## Innovation highlighting

The proposed contribution must be visible but not exaggerated.

Preferred methods:

- slightly stronger border;
- a single accent fill;
- a small `Proposed` or `Key contribution` tag;
- a dedicated panel;
- a concise callout linked to the module.

Do not make every module look novel.

## Equations and notation

Use equations only when they clarify mechanism.

Good uses:

- objective functions;
- update rules;
- state transitions;
- fusion operations;
- key constraints;
- tensor shape transformations.

Avoid placing full derivations inside the figure.

Use notation consistently with the manuscript. Do not rename variables for aesthetics.

## Tensor and data shape notation

When model dimensions matter, use a consistent convention such as:

- input: `[B, T, F]`;
- hidden state: `[B, T, D]`;
- graph representation: `[B, N, D]`;
- forecast: `[B, H, C]`.

Only show dimensions that help explain the architecture.

## Multi-panel figures

Use panels only when the figure needs distinct views.

Recommended panel logic:

- `(a)` overall framework;
- `(b)` core proposed module;
- `(c)` training or online execution detail.

Each panel must have a separate purpose. Do not use panels merely to fit more content.

## Output behavior

When asked to create a figure:

1. analyze the supplied material;
2. state the central message of the figure;
3. produce the figure specification;
4. choose a figure type and journal style preset when relevant;
5. choose a layout template and create the skeleton and wireframe;
6. run the scientific and visual quality gates;
7. generate the SVG in `outputs/academic_figures/` unless another path is requested;
8. inspect and revise the result using the final quality checklist;
9. provide the final files, caption, and unresolved assumptions.

When asked only for a design plan, stop after the specification and layout proposal.

When asked to revise an existing figure, preserve correct scientific content and improve only the requested aspects unless broader defects make the figure misleading.

## Failure conditions

Do not claim the figure is publication-ready if:

- essential method details are missing;
- the supplied sources conflict materially;
- the output cannot be inspected;
- labels overlap or are unreadable;
- connections are ambiguous;
- the innovation cannot be distinguished from the baseline pipeline;
- raster elements dominate the figure without justification.

In such cases, deliver the best partial result and identify the exact limitation.
