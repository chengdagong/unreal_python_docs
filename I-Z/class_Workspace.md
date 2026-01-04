# unreal.Workspace

```python
class unreal.Workspace(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


**C++ Source:**

- **Plugin**: Workspace

- **Module**: WorkspaceEditor

- **File**: Workspace.h



---

**add_asset**( _asset_, _setup_undo_redo=True_, _print_python_command=True_) → `bool`

Adds an asset to the workspace

Parameters:

- **asset** ( _Object_)

- **setup\_undo\_redo** ( _bool_)

- **print\_python\_command** ( _bool_)


Returns:

true if the asset was added

Return type:

bool


---

**add_assets**( _assets_, _setup_undo_redo=True_, _print_python_command=True_) → `bool`

Adds assets to the workspace

Parameters:

- **assets** ( _Array_ _\_ [_Object_ _]_)

- **setup\_undo\_redo** ( _bool_)

- **print\_python\_command** ( _bool_)


Returns:

true if an asset was added

Return type:

bool


---

**remove_asset**( _asset_, _setup_undo_redo=True_, _print_python_command=True_) → `bool`

Removes an asset from the workspace

Parameters:

- **asset** ( _Object_)

- **setup\_undo\_redo** ( _bool_)

- **print\_python\_command** ( _bool_)


Returns:

true if the asset was removed

Return type:

bool


---

**remove_assets**( _assets_, _setup_undo_redo=True_, _print_python_command=True_) → `bool`

Removes assets from the workspace

Parameters:

- **assets** ( _Array_ _\_ [_Object_ _]_)

- **setup\_undo\_redo** ( _bool_)

- **print\_python\_command** ( _bool_)


Returns:

true if the asset was removed

Return type:

bool

### Table of Contents

- `unreal.Workspace`
  - `Workspace`
    - `Workspace.add_asset()`
    - `Workspace.add_assets()`
    - `Workspace.remove_asset()`
    - `Workspace.remove_assets()`