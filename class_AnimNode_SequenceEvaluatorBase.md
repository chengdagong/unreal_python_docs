# unreal.AnimNode_SequenceEvaluatorBase

```python
class unreal.AnimNode_SequenceEvaluatorBase(blend_weight:float=0.0, internal_time_accumulator:float=0.0)
```


**Bases:** ``AnimNode_AssetPlayerBase``


Abstract base class. Evaluates a point in an anim sequence, using a specific time input rather than advancing time internally.
Typically the playback position of the animation for this node will represent something other than time, like jump height.
This node will not trigger any notifies present in the associated sequence.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_SequenceEvaluator.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend_weight` (float): [Read-Write] Last encountered blendweight for this node

- `internal_time_accumulator` (float): [Read-Write] Accumulated time used to reference the asset in this node


### Table of Contents

- `unreal.AnimNode_SequenceEvaluatorBase`
  - `AnimNode_SequenceEvaluatorBase`