# unreal.ActorPerceptionUpdateInfo

```python
class unreal.ActorPerceptionUpdateInfo(target_id:int=0, target:Actor=Ellipsis, stimulus:AIStimulus=Ellipsis)
```


**Bases:** ``StructBase``


Actor Perception Update Info

**C++ Source:**

- **Module**: AIModule

- **File**: AIPerceptionComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `stimulus` (AIStimulus): [Read-Write] Updated stimulus

- `target` (Actor): [Read-Write] Actor associated to the stimulus (can be null)

- `target_id` (int32): [Read-Write] Id of to the stimulus source



---

_property_ `stimulus`: AIStimulus

[Read-Write] Updated stimulus

**Type:**

( AIStimulus)


---

_property_ `target`: Actor

[Read-Write] Actor associated to the stimulus (can be null)

**Type:**

( Actor)


---

_property_ `target_id`: int

[Read-Write] Id of to the stimulus source

**Type:**

(int32)

### Table of Contents

- `unreal.ActorPerceptionUpdateInfo`
  - `ActorPerceptionUpdateInfo`
    - `ActorPerceptionUpdateInfo.stimulus`
    - `ActorPerceptionUpdateInfo.target`
    - `ActorPerceptionUpdateInfo.target_id`