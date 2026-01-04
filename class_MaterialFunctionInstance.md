# unreal.MaterialFunctionInstance

```python
class unreal.MaterialFunctionInstance(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MaterialFunctionInterface``


A material function instance defines parameter overrides for a parent material function.

**C++ Source:**

- **Module**: Engine

- **File**: MaterialFunctionInstance.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `double_vector_parameter_values` (Array[DoubleVectorParameterValue]): [Read-Write] DoubleVector parameters.

- `font_parameter_values` (Array[FontParameterValue]): [Read-Write] Font parameters.

- `parameter_collection_parameter_values` (Array[ParameterCollectionParameterValue]): [Read-Write] Parameter Collection parameters.

- `parent` (MaterialFunctionInterface): [Read-Write] Parent function.

- `runtime_virtual_texture_parameter_values` (Array[RuntimeVirtualTextureParameterValue]): [Read-Write] Runtime virtual texture parameters.

- `scalar_parameter_values` (Array[ScalarParameterValue]): [Read-Write] Scalar parameters.

- `sparse_volume_texture_parameter_values` (Array[SparseVolumeTextureParameterValue]): [Read-Write] Sparse volume texture parameters.

- `static_component_mask_parameter_values` (Array[StaticComponentMaskParameter]): [Read-Write] Static component mask parameters.

- `static_switch_parameter_values` (Array[StaticSwitchParameter]): [Read-Write] Static switch parameters.

- `texture_collection_parameter_values` (Array[TextureCollectionParameterValue]): [Read-Write] Texture Collection parameters.

- `texture_parameter_values` (Array[TextureParameterValue]): [Read-Write] Texture parameters.

- `thumbnail_info` (ThumbnailInfo): [Read-Only] Information for thumbnail rendering

- `vector_parameter_values` (Array[VectorParameterValue]): [Read-Write] Vector parameters.



---

_property_ `parent`: MaterialFunctionInterface

[Read-Only] Parent function.

**Type:**

( MaterialFunctionInterface)

### Table of Contents

- `unreal.MaterialFunctionInstance`
  - `MaterialFunctionInstance`
    - `MaterialFunctionInstance.parent`