# unreal.ActorModifierAlignBetweenWeightedActor

```python
class unreal.ActorModifierAlignBetweenWeightedActor(actor_weak:Actor=Ellipsis, weight:float=0.0, enabled:bool=False)
```


**Bases:** ``StructBase``


Represents an actor with a weight and an enabled state.

**C++ Source:**

- **Plugin**: ActorModifier

- **Module**: ActorModifierLayout

- **File**: ActorModifierAlignBetweenModifier.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `actor_weak` (Actor): [Read-Write] An actor that will effect the placement location.

- `enabled` (bool): [Read-Write] If true, will consider this weighted actor when calculating the placement location.

- `weight` (float): [Read-Write] How much effect this actor has on the placement location.



---

_property_ `actor_weak`: Actor

[Read-Write] An actor that will effect the placement location.

**Type:**

( Actor)


---

_property_ `enabled`: bool

[Read-Write] If true, will consider this weighted actor when calculating the placement location.

**Type:**

( bool)


---

_property_ `weight`: float

[Read-Write] How much effect this actor has on the placement location.

**Type:**

( float)

### Table of Contents

- `unreal.ActorModifierAlignBetweenWeightedActor`
  - `ActorModifierAlignBetweenWeightedActor`
    - `ActorModifierAlignBetweenWeightedActor.actor_weak`
    - `ActorModifierAlignBetweenWeightedActor.enabled`
    - `ActorModifierAlignBetweenWeightedActor.weight`