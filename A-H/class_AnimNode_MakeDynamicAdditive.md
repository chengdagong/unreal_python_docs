# unreal.AnimNode_MakeDynamicAdditive

```python
class unreal.AnimNode_MakeDynamicAdditive(base:PoseLink=\[\], additive:PoseLink=\[\], mesh_space_additive:bool=False)
```


**Bases:** ``AnimNode_Base``


Anim Node Make Dynamic Additive

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_MakeDynamicAdditive.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `additive` (PoseLink): [Read-Write] Pose to make additive

- `base` (PoseLink): [Read-Write] Reference pose for additive delta calculation

- `mesh_space_additive` (bool): [Read-Write] Do additive delta calculation in mesh space



---

_property_ `additive`: PoseLink

[Read-Write] Pose to make additive

**Type:**

( PoseLink)


---

_property_ `base`: PoseLink

[Read-Write] Reference pose for additive delta calculation

**Type:**

( PoseLink)


---

_property_ `mesh_space_additive`: bool

[Read-Write] Do additive delta calculation in mesh space

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_MakeDynamicAdditive`
  - `AnimNode_MakeDynamicAdditive`
    - `AnimNode_MakeDynamicAdditive.additive`
    - `AnimNode_MakeDynamicAdditive.base`
    - `AnimNode_MakeDynamicAdditive.mesh_space_additive`