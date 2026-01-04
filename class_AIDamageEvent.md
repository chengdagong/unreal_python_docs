# unreal.AIDamageEvent

```python
class unreal.AIDamageEvent(amount:float=0.0, location:Vector=Ellipsis, hit_location:Vector=Ellipsis, damaged_actor:Actor=Ellipsis, instigator:Actor=Ellipsis, tag:Name='None')
```


**Bases:** ``StructBase``


AIDamage Event

**C++ Source:**

- **Module**: AIModule

- **File**: AISense\_Damage.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `amount` (float): [Read-Write] Damage taken by DamagedActor.
Note: 0-damage events do not get ignored

- `damaged_actor` (Actor): [Read-Write] Damaged actor

- `hit_location` (Vector): [Read-Write] Event’s additional spatial information
TODO: document

- `instigator` (Actor): [Read-Write] Actor that instigated damage. Can be None

- `location` (Vector): [Read-Write] Event’s “Location”, or what will be later treated as the perceived location for this sense.

If not set, HitLocation will be used, if that is unset too DamagedActor’s location

- `tag` (Name): [Read-Write] Optional named identifier for the damage.



---

_property_ `amount`: float

[Read-Write] Damage taken by DamagedActor.
Note: 0-damage events do not get ignored

**Type:**

( float)


---

_property_ `damaged_actor`: Actor

[Read-Write] Damaged actor

**Type:**

( Actor)


---

_property_ `hit_location`: Vector

[Read-Write] Event’s additional spatial information
TODO: document

**Type:**

( Vector)


---

_property_ `instigator`: Actor

[Read-Write] Actor that instigated damage. Can be None

**Type:**

( Actor)


---

_property_ `location`: Vector

[Read-Write] Event’s “Location”, or what will be later treated as the perceived location for this sense.
If not set, HitLocation will be used, if that is unset too DamagedActor’s location

**Type:**

( Vector)


---

_property_ `tag`: Name

[Read-Write] Optional named identifier for the damage.

**Type:**

( Name)

### Table of Contents

- `unreal.AIDamageEvent`
  - `AIDamageEvent`
    - `AIDamageEvent.amount`
    - `AIDamageEvent.damaged_actor`
    - `AIDamageEvent.hit_location`
    - `AIDamageEvent.instigator`
    - `AIDamageEvent.location`
    - `AIDamageEvent.tag`