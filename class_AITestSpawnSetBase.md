# unreal.AITestSpawnSetBase

```python
class unreal.AITestSpawnSetBase(name:Name='None', enabled:bool=False, fallback_spawn_location:Actor=Ellipsis)
```


**Bases:** ``StructBase``


FAITestSpawnSetBase

Base struct defining an AI Test Spawn Set that are used in AFunctionalAITestBase tests.

**C++ Source:**

- **Module**: FunctionalTesting

- **File**: FunctionalAITest.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `enabled` (bool): [Read-Write]

- `fallback_spawn_location` (Actor): [Read-Write] location used for spawning if spawn info doesn’t define one

- `name` (Name): [Read-Write] give the set a name to help identify it if need be



---

_property_ `enabled`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `fallback_spawn_location`: Actor

[Read-Write] location used for spawning if spawn info doesn’t define one

**Type:**

( Actor)


---

_property_ `name`: Name

[Read-Write] give the set a name to help identify it if need be

**Type:**

( Name)

### Table of Contents

- `unreal.AITestSpawnSetBase`
  - `AITestSpawnSetBase`
    - `AITestSpawnSetBase.enabled`
    - `AITestSpawnSetBase.fallback_spawn_location`
    - `AITestSpawnSetBase.name`