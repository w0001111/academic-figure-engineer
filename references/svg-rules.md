# SVG Construction Rules

## Document structure

Use a scalable root element:

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 900" role="img" aria-labelledby="title desc">
```

Include `<title>` and `<desc>` for accessibility.

Group the figure semantically:

```svg
<g id="panel-inputs" class="panel">...</g>
<g id="panel-method" class="panel">...</g>
<g id="panel-outputs" class="panel">...</g>
```

## Styles

Use CSS classes instead of repeating inline styles.

Keep style tokens at the top of the SVG:

- font family;
- text sizes;
- border widths;
- corner radius;
- semantic fills;
- line styles;
- arrow styles.

## Text

Use real `<text>` elements.

Use `<tspan>` for multiline labels.

Avoid labels longer than three short lines inside one node.

Prefer sentence case rather than all capitals.

## Nodes

Use consistent node widths within the same semantic level.

Use rounded rectangles for processing modules, plain rectangles for data objects, and explicit container boxes for subsystems.

Do not use arbitrary icons unless they carry domain meaning.

## Edges

Use `<path>` or `<polyline>` with reusable arrow markers.

Distinguish relationships:

- solid arrow: primary data or control flow;
- dashed arrow: feedback, supervision, or optional dependency;
- double arrow: genuine bidirectional exchange;
- thin annotation line: explanatory callout.

Every non-obvious arrow should have a label.

## Layout

Use a regular spacing grid.

Recommended minimum spacing:

- 24–40 SVG units between related nodes;
- 60–100 units between major stages;
- larger spacing between separate panels.

Avoid edge crossings. Route connections around containers when necessary.

## Color

Use a restrained semantic palette and maintain sufficient contrast.

The figure must remain understandable in grayscale.

Do not use gradients unless they encode a continuous quantity.

## Effects

Avoid heavy shadows, glows, glass effects, and three-dimensional extrusion.

A very subtle shadow may be used only to separate overlapping visual layers in presentation graphics, not as a default for paper figures.

## Export

The SVG must:

- use a `viewBox`;
- avoid external linked images when possible;
- avoid external fonts;
- preserve text as text;
- contain no unnecessary scripts;
- render correctly in browsers and common vector editors;
- use embedded styles;
- avoid unsupported filters when PDF export is expected.

## Accessibility

Include:

- `<title>`;
- `<desc>`;
- meaningful group IDs;
- sufficient contrast;
- textual labels for all important visual encodings.
