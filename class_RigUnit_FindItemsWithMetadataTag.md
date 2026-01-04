# unreal.RigUnit_FindItemsWithMetadataTag

```python
class unreal.RigUnit_FindItemsWithMetadataTag(tag:Name='None', name_space:RigMetaDataNameSpace=Ellipsis, items:None=\[\])
```


**Bases:** ``RigUnit``


Returns all items with a specific tag

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_Metadata.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `items` (Array[RigElementKey]): [Read-Write] The items containing the metadata

- `name_space` (RigMetaDataNameSpace): [Read-Write] Defines in which namespace the metadata will be looked up

- `tag` (Name): [Read-Write] The name of the tag to find



---

_property_ `items`: None

[Read-Only] The items containing the metadata

**Type:**

( Array\ [RigElementKey])


---

_property_ `name_space`: RigMetaDataNameSpace

[Read-Write] Defines in which namespace the metadata will be looked up

**Type:**

( RigMetaDataNameSpace)


---

_property_ `tag`: Name

[Read-Write] The name of the tag to find

**Type:**

( Name)

### Table of Contents

- `unreal.RigUnit_FindItemsWithMetadataTag`
  - `RigUnit_FindItemsWithMetadataTag`
    - `RigUnit_FindItemsWithMetadataTag.items`
    - `RigUnit_FindItemsWithMetadataTag.name_space`
    - `RigUnit_FindItemsWithMetadataTag.tag`