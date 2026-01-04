# unreal.GeometryScript_MeshPoolUtility

```python
class unreal.GeometryScript_MeshPoolUtility(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Geometry Script Library Mesh Pool Functions

**C++ Source:**

- **Plugin**: GeometryScripting

- **Module**: GeometryScriptingCore

- **File**: MeshPoolFunctions.h



---

_classmethod_ discard_global_mesh_pool()→None

Fully clear/destroy the current global mesh pool, allowing it and all its meshes to be garbage collected


---

_classmethod_ get_global_mesh_pool()→DynamicMeshPool

Access a global compute mesh pool (created on first access)

Return type:

DynamicMeshPool

### Table of Contents

- `unreal.GeometryScript_MeshPoolUtility`
  - `GeometryScript_MeshPoolUtility`
    - `GeometryScript_MeshPoolUtility.discard_global_mesh_pool()`
    - `GeometryScript_MeshPoolUtility.get_global_mesh_pool()`