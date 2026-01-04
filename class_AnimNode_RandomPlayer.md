# unreal.AnimNode_RandomPlayer

```python
class unreal.AnimNode_RandomPlayer(entries:None=\[\], blend_weight:float=0.0, shuffle_mode:bool=False)
```


**Bases:** ``AnimNode_AssetPlayerRelevancyBase``


Anim Node Random Player

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_RandomPlayer.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend_weight` (float): [Read-Write] Last encountered blend weight for this node

- `entries` (Array[RandomPlayerSequenceEntry]): [Read-Write] List of sequences to randomly step through

- `ignore_for_relevancy_test` (bool): [Read-Write] If true, “Relevant anim” nodes that look for the highest weighted animation in a state will ignore this node

- `shuffle_mode` (bool): [Read-Write] When shuffle mode is active we will never loop a sequence beyond MaxLoopCount
without visiting each sequence in turn (no repeats). Enabling this will ignore
ChanceToPlay for each entry



---

_property_ `blend_weight`: float

[Read-Write] Last encountered blend weight for this node

**Type:**

( float)


---

_property_ `entries`: None

[Read-Write] List of sequences to randomly step through

**Type:**

( Array\ [RandomPlayerSequenceEntry])


---

_property_ `shuffle_mode`: bool

[Read-Write] When shuffle mode is active we will never loop a sequence beyond MaxLoopCount
without visiting each sequence in turn (no repeats). Enabling this will ignore
ChanceToPlay for each entry

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_RandomPlayer`
  - `AnimNode_RandomPlayer`
    - `AnimNode_RandomPlayer.blend_weight`
    - `AnimNode_RandomPlayer.entries`
    - `AnimNode_RandomPlayer.shuffle_mode`