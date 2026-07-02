# Default Academic Figure Design System

Use these defaults unless the target venue or user specifies otherwise.

## Canvas

```yaml
landscape_double_column:
  viewBox: "0 0 1600 900"
  outer_margin: 64

landscape_single_column:
  viewBox: "0 0 1200 760"
  outer_margin: 56

portrait_algorithm:
  viewBox: "0 0 1000 1400"
  outer_margin: 56
```

## Typography

Use a common sans-serif stack:

```css
font-family: Inter, Arial, Helvetica, sans-serif;
```

Recommended sizes for a 1600 × 900 viewBox:

- figure title: 30–34;
- panel or major stage title: 23–26;
- node title: 18–20;
- node body: 14–16;
- annotation: 12–14;
- tensor shape or variable badge: 11–13.

Use at most three font weights.

## Spacing

- outer margin: 56–72;
- gap between major zones: 56–88;
- gap between related nodes: 24–36;
- internal padding: 16–22;
- minimum distance between edge and unrelated node: 14;
- minimum vertical separation between parallel arrows: 18.

## Shapes

- major subsystem: large container with 12–16 radius;
- method module: rounded rectangle with 10–14 radius;
- data object: rectangle with 4–8 radius;
- output: rectangle or capsule only when semantically useful;
- decision: diamond only for a real conditional branch;
- annotation: no box or a light badge.

Avoid using rounded cards for every item.

## Stroke

- container border: 1.5–2.0;
- node border: 1.6–2.2;
- primary arrow: 2.2–2.8;
- secondary or feedback arrow: 1.8–2.2;
- annotation line: 1.2–1.6.

## Palette

Use semantic roles rather than fixed decoration.

- neutral context fill: very light gray;
- neutral border: medium gray;
- primary contribution fill: one restrained accent tint;
- primary contribution border: darker accent;
- output or response fill: one secondary tint;
- text: near-black;
- tertiary text: dark gray.

Use no more than two accent hues in a normal paper figure.

## Visual hierarchy

- Level 1 blocks may use tinted container backgrounds and larger titles.
- Level 2 modules use stronger borders and consistent fills.
- Level 3 labels use smaller text, badges, or unboxed annotations.
- The proposed contribution may use one accent fill and a stronger border, not glow or heavy shadow.

## Effects

Default:

- no shadow;
- no gradient;
- no glow;
- no texture;
- no 3D perspective.

A subtle shadow is allowed only for presentation graphics, not default paper output.
