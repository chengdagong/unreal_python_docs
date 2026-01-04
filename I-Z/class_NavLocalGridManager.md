# unreal.NavLocalGridManager

```python
class unreal.NavLocalGridManager(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Manager for local navigation grids

Builds non overlapping grid from multiple sources, that can be used later for pathfinding.
Check also: UGridPathFollowingComponent, FNavLocalGridData

**C++ Source:**

- **Module**: AIModule

- **File**: NavLocalGridManager.h



---

_classmethod_ add_local_navigation_grid_for_box( _world_context_object_, _location_, _extent=[1.000000,1.000000,1.000000]_, _rotation=[0.000000,0.000000,0.000000]_, _radius2d=5_, _height=100.000000_, _rebuild_grids=True_)→int32

Add Local Navigation Grid for Box

Parameters:

- **world\_context\_object** ( _Object_)

- **location** ( _Vector_)

- **extent** ( _Vector_)

- **rotation** ( _Rotator_)

- **radius2d** ( _int32_)

- **height** ( _float_)

- **rebuild\_grids** ( _bool_)


Return type:

int32


---

_classmethod_ add_local_navigation_grid_for_capsule( _world_context_object_, _location_, _capsule_radius_, _capsule_half_height_, _radius2d=5_, _height=100.000000_, _rebuild_grids=True_)→int32

Add Local Navigation Grid for Capsule

Parameters:

- **world\_context\_object** ( _Object_)

- **location** ( _Vector_)

- **capsule\_radius** ( _float_)

- **capsule\_half\_height** ( _float_)

- **radius2d** ( _int32_)

- **height** ( _float_)

- **rebuild\_grids** ( _bool_)


Return type:

int32


---

_classmethod_ add_local_navigation_grid_for_point( _world_context_object_, _location_, _radius2d=5_, _height=100.000000_, _rebuild_grids=True_)→int32

creates new grid data for single point

Parameters:

- **world\_context\_object** ( _Object_)

- **location** ( _Vector_)

- **radius2d** ( _int32_)

- **height** ( _float_)

- **rebuild\_grids** ( _bool_)


Return type:

int32


---

_classmethod_ add_local_navigation_grid_for_points( _world_context_object_, _locations_, _radius2d=5_, _height=100.000000_, _rebuild_grids=True_)→int32

creates single grid data for set of points

Parameters:

- **world\_context\_object** ( _Object_)

- **locations** ( _Array_ _\_ [_Vector_ _]_)

- **radius2d** ( _int32_)

- **height** ( _float_)

- **rebuild\_grids** ( _bool_)


Return type:

int32


---

_classmethod_ find_local_navigation_grid_path( _world_context_object_, _start_, _end_)→Array[Vector]orNone

Find Local Navigation Grid Path

Parameters:

- **world\_context\_object** ( _Object_)

- **start** ( _Vector_)

- **end** ( _Vector_)


Returns:

path\_points (Array[Vector]):

Return type:

Array\ [Vector] or None


---

_classmethod_ remove_local_navigation_grid( _world_context_object_, _grid_id_, _rebuild_grids=True_)→None

Remove Local Navigation Grid

Parameters:

- **world\_context\_object** ( _Object_)

- **grid\_id** ( _int32_)

- **rebuild\_grids** ( _bool_)



---

_classmethod_ set_local_navigation_grid_density( _world_context_object_, _cell_size_)→bool

Set Local Navigation Grid Density

Parameters:

- **world\_context\_object** ( _Object_)

- **cell\_size** ( _float_)


Return type:

bool

### Table of Contents

- `unreal.NavLocalGridManager`
  - `NavLocalGridManager`
    - `NavLocalGridManager.add_local_navigation_grid_for_box()`
    - `NavLocalGridManager.add_local_navigation_grid_for_capsule()`
    - `NavLocalGridManager.add_local_navigation_grid_for_point()`
    - `NavLocalGridManager.add_local_navigation_grid_for_points()`
    - `NavLocalGridManager.find_local_navigation_grid_path()`
    - `NavLocalGridManager.remove_local_navigation_grid()`
    - `NavLocalGridManager.set_local_navigation_grid_density()`