# Layout Templates

Use one primary template unless the figure has clearly separated panels.

## T1 — Linear scientific pipeline

Best for model architecture, data processing, and method overview.

```text
Inputs → Representation → Core contribution → Prediction/decision → Outputs
```

Rules:
- one left-to-right entry path;
- parallel input branches may merge once;
- keep the proposed contribution near the visual center;
- limit the main path to 5–7 major blocks.

## T2 — Hierarchical optimization

Best for bilevel, Stackelberg, planning-operation, or supervisory-control structures.

```text
Upper level: objectives · variables · decisions
                    ↓ coupling variables
Lower level: response · operation · constraints
                    ↑ feedback or equilibrium response
```

Rules:
- use two large aligned bands;
- show only coupling variables between levels;
- do not scatter constraints around the canvas;
- distinguish iterative feedback from one-way execution.

## T3 — Prediction–decision–execution loop

Best for closed-loop control and online operation.

```text
Observation → Prediction → Optimization → Physical execution
     ↑                                      ↓
     └──────────── feedback/update ─────────┘
```

Rules:
- clockwise or left-to-right with one return path;
- feedback must be visually secondary but unambiguous;
- separate physical system from computational modules.

## T4 — Multi-source fusion

Best for heterogeneous data or multimodal inputs.

```text
Source A ─┐
Source B ─┼→ Encoders → Fusion → Proposed module → Output
Source C ─┘
```

Rules:
- align source branches;
- use consistent widths for equivalent branches;
- show source-specific processing only when scientifically meaningful;
- merge before the main contribution unless late fusion is the innovation.

## T5 — Multi-timescale coordination

Best for planning, scheduling, dispatch, and control at different horizons.

```text
Long-term planning     | slow variables
Day-ahead scheduling   | forecasts and schedules
Real-time control      | state correction and execution
```

Rules:
- use aligned horizontal lanes;
- show direction of information transfer between timescales;
- distinguish downward plans from upward measurements or corrections;
- label timescale and update frequency.

## T6 — Coupled-system layers

Best for traffic-energy, cyber-physical, or multi-domain systems.

```text
Information/control layer
Transportation/service layer
Energy/physical layer
```

Rules:
- use stacked layers;
- keep within-layer flows horizontal;
- use vertical arrows only for explicit coupling variables;
- label cross-layer exchanges.

## T7 — Algorithm sequence with decision points

Best for iterative procedures and conditional workflows.

```text
Initialize → Evaluate → Decision? → Update → Converged? → Output
```

Rules:
- top-to-bottom preferred;
- use diamonds only for actual branching;
- keep loops outside nodes;
- avoid turning every mathematical operation into a box.

## T8 — Problem–method–evidence graphical abstract

Best for a high-level summary.

```text
Problem and limitation → Proposed solution → Mechanism → Main outcome
```

Rules:
- 3–4 major zones only;
- avoid low-level architecture details;
- emphasize the scientific change produced by the method;
- use minimal text.
