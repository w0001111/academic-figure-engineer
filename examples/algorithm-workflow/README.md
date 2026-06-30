# Example: Algorithm Workflow Figure

## Input summary

An online dispatch algorithm repeatedly observes system state, predicts demand, solves a constrained assignment problem, executes decisions, and updates the state after realized travel and service outcomes.

## Central message

The figure should show the sequential online decision loop and where constraints and objectives enter the algorithm.

## Suggested figure type

Algorithm workflow or prediction-decision-control loop.

## Layout

Top-to-bottom or clockwise loop:

1. Observe state.
2. Forecast demand or availability.
3. Build candidate actions.
4. Solve constrained optimization.
5. Execute dispatch.
6. Observe realized outcomes.
7. Update state and repeat.

## Notes

- Use decision diamonds only for true branches.
- Use dashed feedback arrows for state update.
- Keep mathematical details in callouts, not inside every block.
