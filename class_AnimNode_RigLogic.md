# unreal.AnimNode_RigLogic

```python
class unreal.AnimNode_RigLogic(anim_sequence:PoseLink=\[\], cache_anim_curve_names:bool=False)
```


**Bases:** ``AnimNode_Base``


Anim Node Rig Logic

**C++ Source:**

- **Plugin**: RigLogic

- **Module**: RigLogicModule

- **File**: AnimNode\_RigLogic.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `anim_sequence` (PoseLink): [Read-Write]

- `cache_anim_curve_names` (bool): [Read-Write] \* Since the order of anim curves may change even on a frame by frame basis, it is not safe to cache and
\\* rely on cached indices by default, but if the blueprints feeding anim curves into RigLogic are set up
\\* in a controlled manner, such that no such runtime changes are expected to the order or number of anim
\\* curves, caching may improve the performance of the node, especially in low-LOD evaluations.

- `lod_threshold` (int32): [Read-Write] \* Max LOD level that RigLogic Node is evaluated.
\\* For example if you have the threshold set to 2, it will evaluate until including LOD 2 (based on 0 index). In case the LOD level gets set to 3, it will stop evaluating the Rig Logic.
\\* Setting it to -1 will always evaluate it.



---

_property_ `anim_sequence`: PoseLink

[Read-Write]

**Type:**

( PoseLink)


---

_property_ `cache_anim_curve_names`: bool

[Read-Write] \* Since the order of anim curves may change even on a frame by frame basis, it is not safe to cache and
\\* rely on cached indices by default, but if the blueprints feeding anim curves into RigLogic are set up
\\* in a controlled manner, such that no such runtime changes are expected to the order or number of anim
\\* curves, caching may improve the performance of the node, especially in low-LOD evaluations.

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_RigLogic`
  - `AnimNode_RigLogic`
    - `AnimNode_RigLogic.anim_sequence`
    - `AnimNode_RigLogic.cache_anim_curve_names`