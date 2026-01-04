# unreal.SkeletalMeshSocket

```python
class unreal.SkeletalMeshSocket(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Skeletal Mesh Socket

**C++ Source:**

- **Module**: Engine

- **File**: SkeletalMeshSocket.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bone_name` (Name): [Read-Only]

- `force_always_animated` (bool): [Read-Write] If true then the hierarchy of bones this socket is attached to will always be

evaluated, even if it had previously been removed due to the current lod setting

- `relative_location` (Vector): [Read-Write]

- `relative_rotation` (Rotator): [Read-Write]

- `relative_scale` (Vector): [Read-Write]

- `socket_name` (Name): [Read-Only] Defines a named attachment location on the USkeletalMesh.
These are set up in editor and used as a shortcut instead of specifying
everything explicitly to AttachComponent in the SkeletalMeshComponent.
The Outer of a SkeletalMeshSocket should always be the USkeletalMesh.



---

_property_ `bone_name`: Name

[Read-Only]

**Type:**

( Name)


---

_property_ `force_always_animated`: bool

[Read-Only] If true then the hierarchy of bones this socket is attached to will always be
evaluated, even if it had previously been removed due to the current lod setting

**Type:**

( bool)


---

**get_socket_local_transform**() → `Transform`

returns FTransform of Socket local transform

Return type:

Transform


---

**get_socket_location**( _skel_comp_) → `Vector`

Get Socket Location

Parameters:

**skel\_comp** ( _SkeletalMeshComponent_)

Return type:

Vector


---

**initialize_socket_from_location**( _skel_comp_, _world_location_, _world_normal_) → `None`

Sets BoneName, RelativeLocation and RelativeRotation based on closest bone to WorldLocation and WorldNormal

Parameters:

- **skel\_comp** ( _SkeletalMeshComponent_)

- **world\_location** ( _Vector_)

- **world\_normal** ( _Vector_)



---

_property_ `relative_location`: Vector

[Read-Only]

**Type:**

( Vector)


---

_property_ `relative_rotation`: Rotator

[Read-Only]

**Type:**

( Rotator)


---

_property_ `relative_scale`: Vector

[Read-Only]

**Type:**

( Vector)


---

**set_socket_local_transform**( _transform_) → `None`

Sets the relative transform parameters of the socket to the given local FTransform

Parameters:

**transform** ( _Transform_)


---

**set_socket_parent**( _skeletal_mesh_, _bone_name_) → `None`

Change the sockets parent to a new bone. The skeleton is used to validate that the bone exists

Parameters:

- **skeletal\_mesh** ( _SkeletalMesh_)

- **bone\_name** ( _Name_)



---

_property_ `socket_name`: Name

[Read-Only] Defines a named attachment location on the USkeletalMesh.
These are set up in editor and used as a shortcut instead of specifying
everything explicitly to AttachComponent in the SkeletalMeshComponent.
The Outer of a SkeletalMeshSocket should always be the USkeletalMesh.

**Type:**

( Name)

### Table of Contents

- `unreal.SkeletalMeshSocket`
  - `SkeletalMeshSocket`
    - `SkeletalMeshSocket.bone_name`
    - `SkeletalMeshSocket.force_always_animated`
    - `SkeletalMeshSocket.get_socket_local_transform()`
    - `SkeletalMeshSocket.get_socket_location()`
    - `SkeletalMeshSocket.initialize_socket_from_location()`
    - `SkeletalMeshSocket.relative_location`
    - `SkeletalMeshSocket.relative_rotation`
    - `SkeletalMeshSocket.relative_scale`
    - `SkeletalMeshSocket.set_socket_local_transform()`
    - `SkeletalMeshSocket.set_socket_parent()`
    - `SkeletalMeshSocket.socket_name`