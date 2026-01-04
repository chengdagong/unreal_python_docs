# unreal.StreamableRenderAsset

```python
class unreal.StreamableRenderAsset(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Streamable Render Asset

**C++ Source:**

- **Module**: Engine

- **File**: StreamableRenderAsset.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `global_force_mip_levels_to_be_resident` (bool): [Read-Write] Global and serialized version of ForceMiplevelsToBeResident.

- `never_stream` (bool): [Read-Write]

- `num_cinematic_mip_levels` (int32): [Read-Write] Number of mip-levels to use for cinematic quality.



---

_property_ `global_force_mip_levels_to_be_resident`: bool

[Read-Only] Global and serialized version of ForceMiplevelsToBeResident.

**Type:**

( bool)


---

_property_ `never_stream`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `num_cinematic_mip_levels`: int

[Read-Write] Number of mip-levels to use for cinematic quality.

**Type:**

(int32)


---

**set_force_mip_levels_to_be_resident**( _seconds_, _cinematic_lod_group_mask=0_) → `None`

Tells the streaming system that it should force all mip-levels to be resident for a number of seconds.

Parameters:

- **seconds** ( _float_) – Duration in seconds

- **cinematic\_lod\_group\_mask** ( _int32_)


### Table of Contents

- `unreal.StreamableRenderAsset`
  - `StreamableRenderAsset`
    - `StreamableRenderAsset.global_force_mip_levels_to_be_resident`
    - `StreamableRenderAsset.never_stream`
    - `StreamableRenderAsset.num_cinematic_mip_levels`
    - `StreamableRenderAsset.set_force_mip_levels_to_be_resident()`