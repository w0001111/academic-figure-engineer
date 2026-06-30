# Academic Figure Types

## 1. Overall research framework

Use when the reader needs to understand the complete study from data to scientific conclusion.

Typical zones:

- real-world system or data sources;
- modeling and analysis;
- optimization, control, or inference;
- validation;
- outputs and scientific findings.

Avoid exposing low-level neural layers unless essential.

## 2. Model architecture

Use when the contribution is mainly architectural.

Typical zones:

- inputs;
- embedding or preprocessing;
- backbone;
- proposed module;
- fusion;
- prediction head;
- losses or supervision.

Show tensor shapes selectively.

## 3. Data processing pipeline

Use for preprocessing, feature construction, graph construction, augmentation, or sample generation.

Emphasize transformations and data availability boundaries.

## 4. Algorithm workflow

Use for sequential procedures, iterative optimization, online updating, or control loops.

Use top-to-bottom ordering and explicit decision diamonds only when true branching exists.

## 5. Multi-timescale coordination

Use when processes operate at distinct timescales.

Organize by aligned horizontal bands or vertical columns representing timescales. Clearly show which variables pass between levels.

## 6. Hierarchical or bilevel optimization

Use when upper and lower levels have separate objectives, variables, and feedback.

Show:

- upper-level decisions;
- lower-level responses;
- coupling variables;
- iterative or equilibrium relationship;
- final solution selection.

## 7. Prediction-decision-control loop

Use when forecasts influence optimization or control and realized outcomes feed back into future decisions.

Separate forecast generation, decision optimization, physical execution, observation, and update.

## 8. Traffic-energy coupling mechanism

Use when transportation states and power-system states influence one another.

Prefer separate layers:

- traffic layer;
- charging service layer;
- power or energy layer;
- information and control layer.

Use cross-layer arrows only for explicit coupling variables.

## 9. Experiment validation framework

Use to explain datasets, scenarios, baselines, metrics, and simulation platforms.

Do not confuse this with a results chart.

## 10. Graphical abstract

Use for a high-level visual summary of the scientific contribution.

Keep it simpler than the main method figure. Emphasize problem, proposed solution, and main outcome.
