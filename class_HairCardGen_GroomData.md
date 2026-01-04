# unreal.HairCardGen_GroomData

```python
class unreal.HairCardGen_GroomData(basis_type:str='', curve_type:str='', strands:None=\[\], vertex_positions:None=\[\], vertex_widths:None=\[\], hairline_group_id:int=0)
```


**Bases:** ``StructBase``


With “Guide” data stipped out (since it isn’t used as part of the mesh generation algorithm)

**C++ Source:**

- **Plugin**: HairCardGenerator

- **Module**: HairCardGeneratorEditor

- **File**: HairCardGenControllerBase.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `basis_type` (str): [Read-Only]

- `curve_type` (str): [Read-Only]

- `hairline_group_id` (int32): [Read-Only]

- `strands` (Array[HairCardGen\_StrandData]): [Read-Only] Array of index buffers. Each buffer defines a distinct hair strand in the groom.

- `vertex_positions` (Array[float]): [Read-Only] Flattened Array of 3D vetex positions

- `vertex_widths` (Array[float]): [Read-Only]



---

_property_ `basis_type`: str

[Read-Only]

**Type:**

( str)


---

_property_ `curve_type`: str

[Read-Only]

**Type:**

( str)


---

_property_ `hairline_group_id`: int

[Read-Only]

**Type:**

(int32)


---

_property_ `strands`: None

[Read-Only] Array of index buffers. Each buffer defines a distinct hair strand in the groom.

**Type:**

( Array\ [HairCardGen\_StrandData])


---

_property_ `vertex_positions`: None

[Read-Only] Flattened Array of 3D vetex positions

**Type:**

( Array\ [float])


---

_property_ `vertex_widths`: None

[Read-Only]

**Type:**

( Array\ [float])

### Table of Contents

- `unreal.HairCardGen_GroomData`
  - `HairCardGen_GroomData`
    - `HairCardGen_GroomData.basis_type`
    - `HairCardGen_GroomData.curve_type`
    - `HairCardGen_GroomData.hairline_group_id`
    - `HairCardGen_GroomData.strands`
    - `HairCardGen_GroomData.vertex_positions`
    - `HairCardGen_GroomData.vertex_widths`