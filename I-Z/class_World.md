# unreal.World

```python
class unreal.World(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


The World is the top level object representing a map or a sandbox in which Actors and Components will exist and be rendered.

A World can be a single Persistent Level with an optional list of streaming levels that are loaded and unloaded via volumes and blueprint functions
or it can be a collection of levels organized with a World Composition.

In a standalone game, generally only a single World exists except during seamless area transitions when both a destination and current world exists.
In the editor many Worlds exist: The level being edited, each PIE instance, each editor tool which has an interactive rendered viewport, and many more.

**C++ Source:**

- **Module**: Engine

- **File**: World.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `thumbnail_info` (ThumbnailInfo): [Read-Only] Information for thumbnail rendering



---

**get_data_layer_manager**() → `DataLayerManager`

Returns the UDataLayerManager associated with this world.

Returns:

UDataLayerManager object associated with this world

Return type:

DataLayerManager


---

**get_world_settings**() → `WorldSettings`

Returns the AWorldSettings actor associated with this world.

Returns:

AWorldSettings actor associated with this world

Return type:

WorldSettings

### Table of Contents

- `unreal.World`
  - `World`
    - `World.get_data_layer_manager()`
    - `World.get_world_settings()`