# Evidence Traceability

Evidence traceability means that every important node and arrow in an academic figure can be traced back to a source.

The purpose is to prevent attractive but unsupported diagrams.

## What needs evidence

Evidence should be attached to:

- major nodes;
- major arrows;
- equations or notation shown in the figure;
- claimed innovation modules;
- feedback loops;
- training-only or inference-only paths;
- physical coupling relationships;
- omitted or uncertain components.

## Evidence fields

Use the following fields in `figure-spec.yaml`.

```yaml
evidence:
  source_type: "paper | equation | algorithm | code | manuscript | note | inferred | missing"
  source_ref: "specific section, equation, algorithm, code path, or note"
  confidence: "high | medium | low"
```

## Node evidence example

```yaml
nodes:
  - id: "evoformer"
    label: "Evoformer"
    type: "model_module"
    innovation: true
    evidence:
      source_type: "paper"
      source_ref: "Jumper et al. 2021, AlphaFold architecture and method description"
      confidence: "high"
```

## Edge evidence example

```yaml
edges:
  - from: "msa-features"
    to: "evoformer"
    meaning: "evolutionary representation input"
    label: "MSA features"
    style: "solid"
    evidence:
      source_type: "paper"
      source_ref: "Jumper et al. 2021 describes MSA-derived features as model inputs"
      confidence: "high"
```

## Confidence levels

- `high`: directly supported by code, equation, algorithm, or explicit method text.
- `medium`: logically inferred from supplied material but not stated in exactly the same form.
- `low`: uncertain, incomplete, or only weakly supported.

Low-confidence nodes or arrows should usually be omitted from the SVG or explicitly marked as assumptions.

## Unresolved evidence

If evidence is missing or conflicting, record it in the figure specification and audit file.

```yaml
validation:
  unresolved_items:
    - "The supplied notes mention feedback from grid outcomes to dispatch, but no method section supports an explicit feedback controller. The feedback arrow is omitted."
```

## Rule of thumb

If an expert reviewer asks “why is this arrow here?”, the figure package should be able to answer with a source reference.
