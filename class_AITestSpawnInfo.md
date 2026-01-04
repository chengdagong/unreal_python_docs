# unreal.AITestSpawnInfo

```python
class unreal.AITestSpawnInfo(spawn_location:Actor=Ellipsis, number_to_spawn:int=0, spawn_delay:float=0.0, pre_spawn_delay:float=0.0, pawn_class:Class=Ellipsis, controller_class:Class=Ellipsis, team_id:GenericTeamId=Ellipsis, behavior_tree:BehaviorTree=Ellipsis)
```


**Bases:** ``AITestSpawnInfoBase``


FAITestSpawnInfo

Generic AI Test Spawn Info used in FAITestSpawnSet within a generic AFunctionalAITest test.

**C++ Source:**

- **Module**: FunctionalTesting

- **File**: FunctionalAITest.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `behavior_tree` (BehaviorTree): [Read-Write] if set will be applied to spawned AI

- `controller_class` (type(Class)): [Read-Write] class to override default pawn’s controller class. If None the default will be used

- `number_to_spawn` (int32): [Read-Write]

- `pawn_class` (type(Class)): [Read-Write] Determines AI to be spawned

- `pre_spawn_delay` (float): [Read-Write] delay before attempting first spawn

- `spawn_delay` (float): [Read-Write] delay between consecutive spawn attempts

- `spawn_location` (Actor): [Read-Write] Where should AI be spawned

- `team_id` (GenericTeamId): [Read-Write]



---

_property_ `behavior_tree`: BehaviorTree

[Read-Write] if set will be applied to spawned AI

**Type:**

( BehaviorTree)


---

_property_ `controller_class`: Class

[Read-Write] class to override default pawn’s controller class. If None the default will be used

**Type:**

( type( Class))


---

_property_ `pawn_class`: Class

[Read-Write] Determines AI to be spawned

**Type:**

( type( Class))


---

_property_ `team_id`: GenericTeamId

[Read-Write]

**Type:**

( GenericTeamId)

### Table of Contents

- `unreal.AITestSpawnInfo`
  - `AITestSpawnInfo`
    - `AITestSpawnInfo.behavior_tree`
    - `AITestSpawnInfo.controller_class`
    - `AITestSpawnInfo.pawn_class`
    - `AITestSpawnInfo.team_id`