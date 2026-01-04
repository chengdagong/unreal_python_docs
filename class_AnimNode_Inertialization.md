# unreal.AnimNode_Inertialization

```python
class unreal.AnimNode_Inertialization
```


**Bases:** ``AnimNode_Base``


Anim Node Inertialization

**C++ Source:**

- **Module**: Engine

- **File**: AnimNode\_Inertialization.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `default_blend_profile` (BlendProfile): [Read-Write] Optional default blend profile to use when no blend profile is supplied with the inertialization request

- `filtered_bones` (Array[BoneReference]): [Read-Write] List of bones that should not use inertial blending. These bones will change instantly when the animation switches.

- `filtered_curves` (Array[Name]): [Read-Write] List of curves that should not use inertial blending. These curves will instantly change when inertialization begins.

- `forward_requests_through_skipped_cached_pose_nodes` (bool): [Read-Write] When enabled this option will forward inertialization requests through any downstream UseCachedPose nodes which
have had their update skipped (e.g. because they have already been updated in another location). This can be
useful in the case where the same cached pose is used in multiple places, and having an inertialization request
that goes with it caught in only one of those places would create popping.

- `preallocate_memory` (bool): [Read-Write]
deprecated: Preallocate Memory has been deprecated.

- `reset_on_becoming_relevant` (bool): [Read-Write] Clear any active blends if we just became relevant, to avoid carrying over undesired blends.

- `source` (PoseLink): [Read-Write]



---

_property_ `preallocate_memory`: bool

[Read-Write]
deprecated: Preallocate Memory has been deprecated.

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_Inertialization`
  - `AnimNode_Inertialization`
    - `AnimNode_Inertialization.preallocate_memory`