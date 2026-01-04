# unreal.HairGroupDesc

```python
class unreal.HairGroupDesc(hair\width:float=0.0, hair\width\override:bool=False, hair\root\scale:float=0.0, hair\root\scale\override:bool=False, hair\tip\scale:float=0.0, hair\tip\scale\override:bool=False, hair\shadow\density:float=0.0, hair\shadow\density\override:bool=False, hair\raytracing\radius\scale:float=0.0, hair\raytracing\radius\scale\override:bool=False, use\hair\raytracing\geometry:bool=False, use\hair\raytracing\geometry\override:bool=False, lod\bias:float=0.0, use\stable\rasterization:bool=False, use\stable\rasterization\override:bool=False, scatter\scene\lighting:bool=False, scatter\scene\lighting\override:bool=False, hair\length\scale:float=0.0, hair\length\scale\override:bool=False)
```


**Bases:** ``StructBase``


Note: If a new field is added to this struct, think to update GroomComponentDestailsCustomization.cpp to handle override flags

**C++ Source:**

- **Plugin**: HairStrands

- **Module**: HairStrandsCore

- **File**: GroomDesc.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `hair_length_scale` (float): [Read-Write] When enabled, Length Scale allow to scale the length of the hair.

- `hair_length_scale_override` (bool): [Read-Write]

- `hair_raytracing_radius_scale` (float): [Read-Write] Scale the hair geometry radius for ray tracing effects (e.g. shadow)

- `hair_raytracing_radius_scale_override` (bool): [Read-Write]

- `hair_root_scale` (float): [Read-Write] Scale the hair width at the root

- `hair_root_scale_override` (bool): [Read-Write]

- `hair_shadow_density` (float): [Read-Write] Override the hair shadow density factor (unit less).

- `hair_shadow_density_override` (bool): [Read-Write]

- `hair_tip_scale` (float): [Read-Write] Scale the hair width at the tip

- `hair_tip_scale_override` (bool): [Read-Write]

- `hair_width` (float): [Read-Write] Hair width (in centimeters)

- `hair_width_override` (bool): [Read-Write]

- `lod_bias` (float): [Read-Write] Bias the selected LOD. A value >0 will progressively select lower detailed lods. Used when r.HairStrands.Cluster.Culling = 1.

- `scatter_scene_lighting` (bool): [Read-Write] Light hair with the scene color. This is used for vellus/short hair to bring light from the surrounding surface, like skin.

- `scatter_scene_lighting_override` (bool): [Read-Write]

- `use_hair_raytracing_geometry` (bool): [Read-Write] Enable hair strands geomtry for raytracing

- `use_hair_raytracing_geometry_override` (bool): [Read-Write]

- `use_stable_rasterization` (bool): [Read-Write] Insure the hair does not alias. When enable, group of hairs might appear thicker. Isolated hair should remain thin.

- `use_stable_rasterization_override` (bool): [Read-Write]



---

_property_ `hair_length_scale`: float

[Read-Write] When enabled, Length Scale allow to scale the length of the hair.

**Type:**

( float)


---

_property_ `hair_length_scale_override`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `hair_raytracing_radius_scale`: float

[Read-Write] Scale the hair geometry radius for ray tracing effects (e.g. shadow)

**Type:**

( float)


---

_property_ `hair_raytracing_radius_scale_override`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `hair_root_scale`: float

[Read-Write] Scale the hair width at the root

**Type:**

( float)


---

_property_ `hair_root_scale_override`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `hair_shadow_density`: float

[Read-Write] Override the hair shadow density factor (unit less).

**Type:**

( float)


---

_property_ `hair_shadow_density_override`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `hair_tip_scale`: float

[Read-Write] Scale the hair width at the tip

**Type:**

( float)


---

_property_ `hair_tip_scale_override`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `hair_width`: float

[Read-Write] Hair width (in centimeters)

**Type:**

( float)


---

_property_ `hair_width_override`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `lod_bias`: float

[Read-Write] Bias the selected LOD. A value >0 will progressively select lower detailed lods. Used when r.HairStrands.Cluster.Culling = 1.

**Type:**

( float)


---

_property_ `scatter_scene_lighting`: bool

[Read-Only] Light hair with the scene color. This is used for vellus/short hair to bring light from the surrounding surface, like skin.

**Type:**

( bool)


---

_property_ `scatter_scene_lighting_override`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `use_hair_raytracing_geometry`: bool

[Read-Write] Enable hair strands geomtry for raytracing

**Type:**

( bool)


---

_property_ `use_hair_raytracing_geometry_override`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `use_stable_rasterization`: bool

[Read-Only] Insure the hair does not alias. When enable, group of hairs might appear thicker. Isolated hair should remain thin.

**Type:**

( bool)


---

_property_ `use_stable_rasterization_override`: bool

[Read-Write]

**Type:**

( bool)

### Table of Contents

- `unreal.HairGroupDesc`
  - `HairGroupDesc`
    - `HairGroupDesc.hair_length_scale`
    - `HairGroupDesc.hair_length_scale_override`
    - `HairGroupDesc.hair_raytracing_radius_scale`
    - `HairGroupDesc.hair_raytracing_radius_scale_override`
    - `HairGroupDesc.hair_root_scale`
    - `HairGroupDesc.hair_root_scale_override`
    - `HairGroupDesc.hair_shadow_density`
    - `HairGroupDesc.hair_shadow_density_override`
    - `HairGroupDesc.hair_tip_scale`
    - `HairGroupDesc.hair_tip_scale_override`
    - `HairGroupDesc.hair_width`
    - `HairGroupDesc.hair_width_override`
    - `HairGroupDesc.lod_bias`
    - `HairGroupDesc.scatter_scene_lighting`
    - `HairGroupDesc.scatter_scene_lighting_override`
    - `HairGroupDesc.use_hair_raytracing_geometry`
    - `HairGroupDesc.use_hair_raytracing_geometry_override`
    - `HairGroupDesc.use_stable_rasterization`
    - `HairGroupDesc.use_stable_rasterization_override`