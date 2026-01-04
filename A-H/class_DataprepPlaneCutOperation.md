# unreal.DataprepPlaneCutOperation

```python
class unreal.DataprepPlaneCutOperation(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``DataprepEditingOperation``


Experimental - Plane cut input meshes

**C++ Source:**

- **Plugin**: DataprepGeometryOperations

- **Module**: DataprepGeometryOperations

- **File**: DataprepGeometryOperations.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `cut_plane_keep_side` (PlaneCutKeepSide): [Read-Write] Specify which section(s) of the cut to keep. If ‘Keep Both’ is selected, both sides of the

cut are computed and a new actor added with the negative side.

- `cut_plane_normal_angles` (Vector): [Read-Write] Euler angles of the normal to the cutting plane (default plane is XY plane)

- `cut_plane_origin` (Vector): [Read-Write] Origin of the cutting plane

- `export_separate_pieces` (bool): [Read-Write] If true, meshes cut into multiple pieces will be saved as separate assets.

- `fill_cut_hole` (bool): [Read-Write] If true, the cut surface is filled with simple planar hole fill surface(s)

- `spacing_between_halves` (float): [Read-Write] If keeping both halves, separate the two pieces by this amount


### Table of Contents

- `unreal.DataprepPlaneCutOperation`
  - `DataprepPlaneCutOperation`