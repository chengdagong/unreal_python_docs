# unreal.AITestSpawnSet

```python
class unreal.AITestSpawnSet(name:Name='None', enabled:bool=False, fallback_spawn_location:Actor=Ellipsis, spawn_info_container:None=\[\])
```


**Bases:** ``AITestSpawnSetBase``


FAITestSpawnSet

Generic AI Test Spawn Set that is used in regular AFunctionalAITest tests.

**C++ Source:**

- **Module**: FunctionalTesting

- **File**: FunctionalAITest.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `enabled` (bool): [Read-Write]

- `fallback_spawn_location` (Actor): [Read-Write] location used for spawning if spawn info doesn’t define one

- `name` (Name): [Read-Write] give the set a name to help identify it if need be

- `spawn_info_container` (Array[AITestSpawnInfo]): [Read-Write] what to spawn



---

_property_ `spawn_info_container`: None

[Read-Write] what to spawn

**Type:**

( Array\ [AITestSpawnInfo])

### Table of Contents

- `unreal.AITestSpawnSet`
  - `AITestSpawnSet`
    - `AITestSpawnSet.spawn_info_container`