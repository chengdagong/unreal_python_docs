# unreal.ActorDesc

```python
class unreal.ActorDesc(guid:Guid=\[\], native_class:Class=Ellipsis, class:SoftObjectPath=Ellipsis, name:Name='None', label:Name='None', bounds:Box=Ellipsis, runtime_grid:Name='None', is_spatially_loaded:bool=False, actor_is_editor_only:bool=False, actor_package:Name='None', actor_path:Name='None', data_layer_assets:None=\[\])
```


**Bases:** ``StructBase``


Snapshot of an actor descriptor, which represents the state of an actor on disk.
The actor may or may not be loaded.

**C++ Source:**

- **Module**: Engine

- **File**: WorldPartitionBlueprintLibrary.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `actor_is_editor_only` (bool): [Read-Only] Actor’s editor-only property.

- `actor_package` (Name): [Read-Only] Actor’s package name.

- `actor_path` (Name): [Read-Only] Actor’s path name.

- `bounds` (Box): [Read-Only] Streaming bounds of this actor.

- `class_` (SoftObjectPath): [Read-Only] Actor class, can point to a native or Blueprint class and may be redirected.

- `data_layer_assets` (Array[SoftObjectPath]): [Read-Only] Actor’s data layer assets.

- `guid` (Guid): [Read-Only] The actor GUID of this descriptor.

- `is_spatially_loaded` (bool): [Read-Only] Actor’s streaming state.

- `label` (Name): [Read-Only] Actor’s label.

- `name` (Name): [Read-Only] Internal name of the actor.

- `native_class` (type(Class)): [Read-Only] Actor first native class.

- `runtime_grid` (Name): [Read-Only] Actor’s target runtime grid.



---

_property_ `actor_is_editor_only`: bool

[Read-Only] Actor’s editor-only property.

**Type:**

( bool)


---

_property_ `actor_package`: Name

[Read-Only] Actor’s package name.

**Type:**

( Name)


---

_property_ `actor_path`: Name

[Read-Only] Actor’s path name.

**Type:**

( Name)


---

_property_ `bounds`: Box

[Read-Only] Streaming bounds of this actor.

**Type:**

( Box)


---

_property_ `class_`: SoftObjectPath

[Read-Only] Actor class, can point to a native or Blueprint class and may be redirected.

**Type:**

( SoftObjectPath)


---

_property_ `data_layer_assets`: None

[Read-Only] Actor’s data layer assets.

**Type:**

( Array\ [SoftObjectPath])


---

_property_ `guid`: Guid

[Read-Only] The actor GUID of this descriptor.

**Type:**

( Guid)


---

_property_ `is_spatially_loaded`: bool

[Read-Only] Actor’s streaming state.

**Type:**

( bool)


---

_property_ `label`: Name

[Read-Only] Actor’s label.

**Type:**

( Name)


---

_property_ `name`: Name

[Read-Only] Internal name of the actor.

**Type:**

( Name)


---

_property_ `native_class`: Class

[Read-Only] Actor first native class.

**Type:**

( type( Class))


---

_property_ `runtime_grid`: Name

[Read-Only] Actor’s target runtime grid.

**Type:**

( Name)

### Table of Contents

- `unreal.ActorDesc`
  - `ActorDesc`
    - `ActorDesc.actor_is_editor_only`
    - `ActorDesc.actor_package`
    - `ActorDesc.actor_path`
    - `ActorDesc.bounds`
    - `ActorDesc.class_`
    - `ActorDesc.data_layer_assets`
    - `ActorDesc.guid`
    - `ActorDesc.is_spatially_loaded`
    - `ActorDesc.label`
    - `ActorDesc.name`
    - `ActorDesc.native_class`
    - `ActorDesc.runtime_grid`