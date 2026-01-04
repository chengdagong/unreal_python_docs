# unreal.AnimNextAnimationGraph

```python
class unreal.AnimNextAnimationGraph(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimNextSharedVariables``


A user-created collection of animation logic & data

**C++ Source:**

- **Plugin**: UAFAnimGraph

- **Module**: UAFAnimGraph

- **File**: AnimNextAnimationGraph.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `default_entry_point` (Name): [Read-Write] The entry point that this graph defaults to using

- `editor_data` (Object): [Read-Only]



---

**add_animation_graph**( _name_, _setup_undo_redo=True_, _print_python_command=True_) → `AnimNextAnimationGraphEntry`

Adds an animation graph to an AnimNext asset

Parameters:

- **name** ( _Name_)

- **setup\_undo\_redo** ( _bool_)

- **print\_python\_command** ( _bool_)


Return type:

AnimNextAnimationGraphEntry

### Table of Contents

- `unreal.AnimNextAnimationGraph`
  - `AnimNextAnimationGraph`
    - `AnimNextAnimationGraph.add_animation_graph()`