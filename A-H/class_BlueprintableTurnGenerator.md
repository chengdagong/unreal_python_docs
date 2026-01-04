# unreal.BlueprintableTurnGenerator

```python
class unreal.BlueprintableTurnGenerator(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Base class for blueprint-implemented turn generators. This is necessary due to the lack of support for specifying
EditInlineNew on a BP class, so it has to inherit the flag from a native parent.

**C++ Source:**

- **Plugin**: Mover

- **Module**: Mover

- **File**: ModularMovement.h



---

**get_turn**( _target_orientation_, _full_start_state_, _mover_state_, _time_step_, _proposed_move_, _sim_blackboard_) → `Vector`

Returns an additive angular velocity (degrees/second) based on the starting state and timestep. The vector points in the direction of the rotation axis

Parameters:

- **target\_orientation** ( _Rotator_)

- **full\_start\_state** ( _MoverTickStartData_)

- **mover\_state** ( _MoverDefaultSyncState_)

- **time\_step** ( _MoverTimeStep_)

- **proposed\_move** ( _ProposedMove_)

- **sim\_blackboard** ( _MoverBlackboard_)


Return type:

Vector

### Table of Contents

- `unreal.BlueprintableTurnGenerator`
  - `BlueprintableTurnGenerator`
    - `BlueprintableTurnGenerator.get_turn()`