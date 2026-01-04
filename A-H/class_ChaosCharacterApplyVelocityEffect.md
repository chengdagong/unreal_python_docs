# unreal.ChaosCharacterApplyVelocityEffect

```python
class unreal.ChaosCharacterApplyVelocityEffect(velocity_or_impulse_to_apply:Vector=Ellipsis, mode:ChaosMoverVelocityEffectMode=Ellipsis)
```


**Bases:** ``InstantMovementEffect``


Applies a velocity or impulse for a single tick

**C++ Source:**

- **Plugin**: ChaosMover

- **Module**: ChaosMover

- **File**: ChaosCharacterApplyVelocityEffect.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `mode` (ChaosMoverVelocityEffectMode): [Read-Write] Controls whether to apply velocity or impulse and if the velocity will be additive

- `velocity_or_impulse_to_apply` (Vector): [Read-Write] Velocity or impulse to apply to the actor.



---

_property_ `mode`: ChaosMoverVelocityEffectMode

[Read-Write] Controls whether to apply velocity or impulse and if the velocity will be additive

**Type:**

( ChaosMoverVelocityEffectMode)


---

_property_ `velocity_or_impulse_to_apply`: Vector

[Read-Write] Velocity or impulse to apply to the actor.

**Type:**

( Vector)

### Table of Contents

- `unreal.ChaosCharacterApplyVelocityEffect`
  - `ChaosCharacterApplyVelocityEffect`
    - `ChaosCharacterApplyVelocityEffect.mode`
    - `ChaosCharacterApplyVelocityEffect.velocity_or_impulse_to_apply`