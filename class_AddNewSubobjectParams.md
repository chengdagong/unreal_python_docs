# unreal.AddNewSubobjectParams

```python
class unreal.AddNewSubobjectParams(parent_handle:SubobjectDataHandle=\[\], new_class:Class=Ellipsis, blueprint_context:Blueprint=Ellipsis, skip_mark_blueprint_modified:bool=False, conform_transform_to_parent:bool=False)
```


**Bases:** ``StructBase``


Options when adding a new subobject

**C++ Source:**

- **Module**: SubobjectDataInterface

- **File**: SubobjectDataSubsystem.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blueprint_context` (Blueprint): [Read-Write] Pointer to the blueprint context that this subobject is in. If this is null, it is assumed that
this subobject is being added to an instance.

- `conform_transform_to_parent` (bool): [Read-Write] Whether the newly created component should keep its transform, or conform it to its parent

- `new_class` (type(Class)): [Read-Write] The class of the new subobject that will be added

- `parent_handle` (SubobjectDataHandle): [Read-Write]

- `skip_mark_blueprint_modified` (bool): [Read-Write] Optionally skip marking this blueprint as modified (e.g. if we’re handling that externally



---

_property_ `blueprint_context`: Blueprint

[Read-Write] Pointer to the blueprint context that this subobject is in. If this is null, it is assumed that
this subobject is being added to an instance.

**Type:**

( Blueprint)


---

_property_ `conform_transform_to_parent`: bool

[Read-Write] Whether the newly created component should keep its transform, or conform it to its parent

**Type:**

( bool)


---

_property_ `new_class`: Class

[Read-Write] The class of the new subobject that will be added

**Type:**

( type( Class))


---

_property_ `parent_handle`: SubobjectDataHandle

[Read-Write]

**Type:**

( SubobjectDataHandle)


---

_property_ `skip_mark_blueprint_modified`: bool

[Read-Write] Optionally skip marking this blueprint as modified (e.g. if we’re handling that externally

**Type:**

( bool)

### Table of Contents

- `unreal.AddNewSubobjectParams`
  - `AddNewSubobjectParams`
    - `AddNewSubobjectParams.blueprint_context`
    - `AddNewSubobjectParams.conform_transform_to_parent`
    - `AddNewSubobjectParams.new_class`
    - `AddNewSubobjectParams.parent_handle`
    - `AddNewSubobjectParams.skip_mark_blueprint_modified`