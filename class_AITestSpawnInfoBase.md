# unreal.AITestSpawnInfoBase

```python
class unreal.AITestSpawnInfoBase(spawn_location:Actor=Ellipsis, number_to_spawn:int=0, spawn_delay:float=0.0, pre_spawn_delay:float=0.0)
```


**Bases:** ``StructBase``


FAITestSpawnInfoBase

Base struct defining where & when to spawn. Used within a FAITestSpawnSetBase class.

**C++ Source:**

- **Module**: FunctionalTesting

- **File**: FunctionalAITest.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `number_to_spawn` (int32): [Read-Write]

- `pre_spawn_delay` (float): [Read-Write] delay before attempting first spawn

- `spawn_delay` (float): [Read-Write] delay between consecutive spawn attempts

- `spawn_location` (Actor): [Read-Write] Where should AI be spawned



---

_property_ `number_to_spawn`: int

[Read-Write]

**Type:**

(int32)


---

_property_ `pre_spawn_delay`: float

[Read-Write] delay before attempting first spawn

**Type:**

( float)


---

_property_ `spawn_delay`: float

[Read-Write] delay between consecutive spawn attempts

**Type:**

( float)


---

_property_ `spawn_location`: Actor

[Read-Write] Where should AI be spawned

**Type:**

( Actor)

### Table of Contents

- `unreal.AITestSpawnInfoBase`
  - `AITestSpawnInfoBase`
    - `AITestSpawnInfoBase.number_to_spawn`
    - `AITestSpawnInfoBase.pre_spawn_delay`
    - `AITestSpawnInfoBase.spawn_delay`
    - `AITestSpawnInfoBase.spawn_location`