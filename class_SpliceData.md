# unreal.SpliceData

```python
class unreal.SpliceData(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Splice Data

**C++ Source:**

- **Plugin**: GeneSplicer

- **Module**: GeneSplicerModule

- **File**: SpliceDataBP.h



---

**get_skeletal_mesh_component**() → `SkeletalMeshComponent`

Get Skeletal Mesh Component

Return type:

SkeletalMeshComponent


---

**register_gene_pool**( _name_, _gene_pool_asset_, _raf_) → `None`

Register Gene Pool

Parameters:

- **name** ( _str_)

- **gene\_pool\_asset** ( _GenePoolAsset_)

- **raf** ( _RegionAffiliationAsset_)



---

**set_archetype**( _path_) → `None`

Set Archetype

Parameters:

**path** ( _str_)


---

**set_skeletal_mesh_component**( _new_skel_mesh_component_) → `None`

Set Skeletal Mesh Component

Parameters:

**new\_skel\_mesh\_component** ( _SkeletalMeshComponent_)


---

**set_splice_weights**( _name_, _dna_start_index_, _weights_) → `None`

Set Splice Weights

Parameters:

- **name** ( _str_)

- **dna\_start\_index** ( _int32_)

- **weights** ( _Array_ _\_ [_float_ _]_)


### Table of Contents

- `unreal.SpliceData`
  - `SpliceData`
    - `SpliceData.get_skeletal_mesh_component()`
    - `SpliceData.register_gene_pool()`
    - `SpliceData.set_archetype()`
    - `SpliceData.set_skeletal_mesh_component()`
    - `SpliceData.set_splice_weights()`