# unreal.RigUnit_GetSocketTransform

```python
class unreal.RigUnit_GetSocketTransform(scene_component:SceneComponent=Ellipsis, socket_name:Name='None', transform_space:RelativeTransformSpace=Ellipsis, result:Transform=Ellipsis)
```


**Bases:** ``RigUnit_AnimNextBase``


Returns the transform for the specified socket. Note that this is not thread-safe, so must be
called at a point where you know that the target socket is not being updated.

**C++ Source:**

- **Plugin**: UAF

- **Module**: UAF

- **File**: RigUnit\_GetSocketTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `result` (Transform): [Read-Write]

- `scene_component` (SceneComponent): [Read-Write]

- `socket_name` (Name): [Read-Write]

- `transform_space` (RelativeTransformSpace): [Read-Write]



---

_property_ `result`: Transform

[Read-Only]

**Type:**

( Transform)


---

_property_ `scene_component`: SceneComponent

[Read-Write]

**Type:**

( SceneComponent)


---

_property_ `socket_name`: Name

[Read-Write]

**Type:**

( Name)


---

_property_ `transform_space`: RelativeTransformSpace

[Read-Write]

**Type:**

( RelativeTransformSpace)

### Table of Contents

- `unreal.RigUnit_GetSocketTransform`
  - `RigUnit_GetSocketTransform`
    - `RigUnit_GetSocketTransform.result`
    - `RigUnit_GetSocketTransform.scene_component`
    - `RigUnit_GetSocketTransform.socket_name`
    - `RigUnit_GetSocketTransform.transform_space`