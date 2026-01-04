# unreal.AnimNode_TransitionPoseEvaluator

```python
class unreal.AnimNode_TransitionPoseEvaluator(frames_to_cache_pose:int=0, data_source:EvaluatorDataSource=Ellipsis, evaluator_mode:EvaluatorMode=Ellipsis)
```


**Bases:** ``AnimNode_Base``


Animation data node for state machine transitions.
Can be set to supply either the animation data from the transition source (From State) or the transition destination (To State).

**C++ Source:**

- **Module**: Engine

- **File**: AnimNode\_TransitionPoseEvaluator.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `data_source` (EvaluatorDataSource): [Read-Write]

- `evaluator_mode` (EvaluatorMode): [Read-Write]

- `frames_to_cache_pose` (int32): [Read-Write]



---

_property_ `data_source`: EvaluatorDataSource

[Read-Write]

**Type:**

( EvaluatorDataSource)


---

_property_ `evaluator_mode`: EvaluatorMode

[Read-Write]

**Type:**

( EvaluatorMode)


---

_property_ `frames_to_cache_pose`: int

[Read-Write]

**Type:**

(int32)

### Table of Contents

- `unreal.AnimNode_TransitionPoseEvaluator`
  - `AnimNode_TransitionPoseEvaluator`
    - `AnimNode_TransitionPoseEvaluator.data_source`
    - `AnimNode_TransitionPoseEvaluator.evaluator_mode`
    - `AnimNode_TransitionPoseEvaluator.frames_to_cache_pose`