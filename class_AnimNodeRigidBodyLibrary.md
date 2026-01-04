# unreal.AnimNodeRigidBodyLibrary

```python
class unreal.AnimNodeRigidBodyLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Exposes operations to be performed on a rigid body anim node

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_RigidBody\_Library.h


_classmethod_ convert\_to\_rigid\_body\_anim\_node( _node)->(RigidBodyAnimNodeReference_, _result=AnimNodeReferenceConversionResult_)

Get a rigid body anim node context from an anim node context

Parameters:

**node** ( _AnimNodeReference_)

Returns:

result (AnimNodeReferenceConversionResult):

Return type:

AnimNodeReferenceConversionResult

_classmethod_ convert\_to\_rigid\_body\_anim\_node\_pure( _node)->(rigid\_body\_anim\_node=RigidBodyAnimNodeReference_, _result=bool_)

Get a rigid body anim node context from an anim node context (pure)

Parameters:

**node** ( _AnimNodeReference_)

Returns:

rigid\_body\_anim\_node (RigidBodyAnimNodeReference):

result (bool):

Return type:

tuple


---

_classmethod_ set_override_physics_asset( _node_, _physics_asset_)→RigidBodyAnimNodeReference

Set the physics asset on the rigid body anim graph node (RBAN).

Parameters:

- **node** ( _RigidBodyAnimNodeReference_)

- **physics\_asset** ( _PhysicsAsset_)


Return type:

RigidBodyAnimNodeReference

### Table of Contents

- `unreal.AnimNodeRigidBodyLibrary`
  - `AnimNodeRigidBodyLibrary`
    - `AnimNodeRigidBodyLibrary.convert_to_rigid_body_anim_node()`
    - `AnimNodeRigidBodyLibrary.convert_to_rigid_body_anim_node_pure()`
    - `AnimNodeRigidBodyLibrary.set_override_physics_asset()`