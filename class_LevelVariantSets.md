# unreal.LevelVariantSets

```python
class unreal.LevelVariantSets(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Level Variant Sets

**C++ Source:**

- **Plugin**: VariantManagerContent

- **Module**: VariantManagerContent

- **File**: LevelVariantSets.h



---

**add_variant_set**( _variant_set_) → `None`

Adds VariantSet to the LevelVariantSets’ list of VariantSets

Parameters:

**variant\_set** ( _VariantSet_)


---

**get_num_variant_sets**() → `int32`

Get Num Variant Sets

Return type:

int32


---

**get_variant_set**( _variant_set_index_) → `VariantSet`

Get Variant Set

Parameters:

**variant\_set\_index** ( _int32_)

Return type:

VariantSet


---

**get_variant_set_by_name**( _variant_set_name_) → `VariantSet`

Get Variant Set by Name

Parameters:

**variant\_set\_name** ( _str_)

Return type:

VariantSet


---

**remove_variant_set**( _variant_set_) → `None`

Removes VariantSet from LevelVariantSets, if that is its parent

Parameters:

**variant\_set** ( _VariantSet_)


---

**remove_variant_set_by_name**( _variant_set_name_) → `None`

Looks for a variant set with VariantSetName within LevelVariantSets and removes it, if it exists

Parameters:

**variant\_set\_name** ( _str_)

### Table of Contents

- `unreal.LevelVariantSets`
  - `LevelVariantSets`
    - `LevelVariantSets.add_variant_set()`
    - `LevelVariantSets.get_num_variant_sets()`
    - `LevelVariantSets.get_variant_set()`
    - `LevelVariantSets.get_variant_set_by_name()`
    - `LevelVariantSets.remove_variant_set()`
    - `LevelVariantSets.remove_variant_set_by_name()`