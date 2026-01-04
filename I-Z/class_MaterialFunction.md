# unreal.MaterialFunction

```python
class unreal.MaterialFunction(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MaterialFunctionInterface``


A Material Function is a collection of material expressions that can be reused in different materials

**C++ Source:**

- **Module**: Engine

- **File**: MaterialFunction.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `description` (str): [Read-Write] Description of the function which will be displayed as a tooltip wherever the function is used.

- `enable_exec_wire` (bool): [Read-Write]

- `enable_new_hlsl_generator` (bool): [Read-Write]

- `expose_to_library` (bool): [Read-Write] Whether to list this function in the material function library, which is a window in the material editor that lists categorized functions.

- `library_categories_text` (Array[Text]): [Read-Write] Categories that this function belongs to in the material function library.
Ideally categories should be chosen carefully so that there are not too many.

- `preview_blend_mode` (BlendMode): [Read-Write] Determines the blend mode when previewing a material function.

- `preview_material_domain` (MaterialDomain): [Read-Write] The domain to use when previewing a material function.

- `thumbnail_info` (ThumbnailInfo): [Read-Only] Information for thumbnail rendering

- `user_exposed_caption` (str): [Read-Write] Name of the function to be displayed on the node within the material editor instead of the asset name.


### Table of Contents

- `unreal.MaterialFunction`
  - `MaterialFunction`