# Example: Model Architecture Figure

## Input summary

A spatiotemporal forecasting model takes historical node features `X ∈ R^{B×T×N×F}` and a graph adjacency matrix. The model uses temporal embedding, graph message passing, a proposed cross-scale fusion block, and a prediction head for horizon `H`.

## Central message

The figure should show how historical spatiotemporal signals are transformed into multi-horizon forecasts, with the cross-scale fusion block marked as the key contribution.

## Suggested figure type

Model architecture.

## Layout

Left-to-right:

1. Inputs: historical features and graph structure.
2. Embedding: temporal and node embeddings.
3. Backbone: graph-temporal blocks.
4. Proposed module: cross-scale fusion.
5. Output: multi-horizon prediction.

## Notes

- Show tensor shapes only where they clarify the data flow.
- Do not show all repeated blocks if a compact `×L` notation is sufficient.
- Keep loss functions in a small training-only callout if needed.
