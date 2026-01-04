# unreal.GroomSolverSettings

```python
class unreal.GroomSolverSettings
```


**Bases:** ``StructBase``


Solver settings that will be used in dataflow/deformergraph

**C++ Source:**

- **Plugin**: HairStrands

- **Module**: HairStrandsSolver

- **File**: GroomSolverComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `max_lod_distance` (float): [Read-Write] Maximum LOD distance (if distance between the component and the views is higher that this threshold, no simulation)

- `max_points_count` (float): [Read-Write] Maximum number of points the solver is going to simulate

- `min_lod_distance` (float): [Read-Write] Minimum LOD distance (if distance between the component and the views is lower that this threshold, no simulation)


### Table of Contents

- `unreal.GroomSolverSettings`
  - `GroomSolverSettings`