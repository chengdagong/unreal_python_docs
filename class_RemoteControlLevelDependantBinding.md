# unreal.RemoteControlLevelDependantBinding

```python
class unreal.RemoteControlLevelDependantBinding(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``RemoteControlBinding``


Remote Control Level Dependant Binding

**C++ Source:**

- **Plugin**: RemoteControl

- **Module**: RemoteControl

- **File**: RemoteControlBinding.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bound_object_map` (Map[Level, Object]): [Read-Write]
deprecated: BoundObjectMap is deprecated, please use BoundObjectMapByPath instead.

- `name` (str): [Read-Write] The name of this binding. Defaults to the bound object’s name.

- `sub_level_selection_map` (Map[World, Level]): [Read-Write]
deprecated: SubLevelSelectionMap is deprecated, please use SubLevelSelectionMapByPath instead.



---

_property_ `bound_object_map`: None

[Read-Write]
deprecated: BoundObjectMap is deprecated, please use BoundObjectMapByPath instead.

**Type:**

( Map\ [Level, Object])


---

_property_ `sub_level_selection_map`: None

[Read-Write]
deprecated: SubLevelSelectionMap is deprecated, please use SubLevelSelectionMapByPath instead.

**Type:**

( Map\ [World, Level])

### Table of Contents

- `unreal.RemoteControlLevelDependantBinding`
  - `RemoteControlLevelDependantBinding`
    - `RemoteControlLevelDependantBinding.bound_object_map`
    - `RemoteControlLevelDependantBinding.sub_level_selection_map`