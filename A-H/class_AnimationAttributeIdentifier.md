# unreal.AnimationAttributeIdentifier

```python
class unreal.AnimationAttributeIdentifier(name:Name='None', bone_name:Name='None', bone_index:int=0, script_struct:ScriptStruct=Ellipsis, script_struct_path:SoftObjectPath=Ellipsis)
```


**Bases:** ``StructBase``


Script-friendly structure for identifying an attribute (curve).
Wrapping the attribute name, bone name and index, and underlying data type for use within the AnimDataController API.

**C++ Source:**

- **Module**: Engine

- **File**: AttributeIdentifier.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bone_index` (int32): [Read-Write]

- `bone_name` (Name): [Read-Write]

- `name` (Name): [Read-Write]

- `script_struct` (ScriptStruct): [Read-Write]

- `script_struct_path` (SoftObjectPath): [Read-Write]



---

_property_ `bone_index`: int

[Read-Only]

**Type:**

(int32)


---

_property_ `bone_name`: Name

[Read-Only]

**Type:**

( Name)


---

**is_valid**() → `boolReturns:`

Whether or not the Attribute Identifier is valid

Return type:

bool


---

_property_ `name`: Name

[Read-Only]

**Type:**

( Name)


---

_property_ `script_struct`: ScriptStruct

[Read-Only]

**Type:**

( ScriptStruct)


---

_property_ `script_struct_path`: SoftObjectPath

[Read-Only]

**Type:**

( SoftObjectPath)

### Table of Contents

- `unreal.AnimationAttributeIdentifier`
  - `AnimationAttributeIdentifier`
    - `AnimationAttributeIdentifier.bone_index`
    - `AnimationAttributeIdentifier.bone_name`
    - `AnimationAttributeIdentifier.is_valid()`
    - `AnimationAttributeIdentifier.name`
    - `AnimationAttributeIdentifier.script_struct`
    - `AnimationAttributeIdentifier.script_struct_path`