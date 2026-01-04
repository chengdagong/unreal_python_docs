# unreal.AnimBankSequence

```python
class unreal.AnimBankSequence(sequence:AnimSequence=Ellipsis, looping:bool=False, auto_start:bool=False, position:float=0.0, play_rate:float=0.0, bounds_scale:float=0.0)
```


**Bases:** ``StructBase``


Anim Bank Sequence

**C++ Source:**

- **Module**: Engine

- **File**: AnimBank.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `auto_start` (bool): [Read-Write]

- `bounds_scale` (float): [Read-Write] Scales the bounds of the instances playing this sequence.
This is useful when the animation moves the vertices of the mesh outside of its bounds.
Warning: Increasing the bounds will reduce performance!

- `looping` (bool): [Read-Write]

- `play_rate` (float): [Read-Write]

- `position` (float): [Read-Write]

- `sequence` (AnimSequence): [Read-Write]



---

_property_ `auto_start`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `bounds_scale`: float

[Read-Write] Scales the bounds of the instances playing this sequence.
This is useful when the animation moves the vertices of the mesh outside of its bounds.
Warning: Increasing the bounds will reduce performance!

**Type:**

( float)


---

_property_ `looping`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `play_rate`: float

[Read-Write]

**Type:**

( float)


---

_property_ `position`: float

[Read-Write]

**Type:**

( float)


---

_property_ `sequence`: AnimSequence

[Read-Write]

**Type:**

( AnimSequence)

### Table of Contents

- `unreal.AnimBankSequence`
  - `AnimBankSequence`
    - `AnimBankSequence.auto_start`
    - `AnimBankSequence.bounds_scale`
    - `AnimBankSequence.looping`
    - `AnimBankSequence.play_rate`
    - `AnimBankSequence.position`
    - `AnimBankSequence.sequence`