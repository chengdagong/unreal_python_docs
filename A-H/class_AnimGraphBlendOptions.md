# unreal.AnimGraphBlendOptions

```python
class unreal.AnimGraphBlendOptions
```


**Bases:** ``StructBase``


Blending options for animation graphs in Linked Animation Blueprints.

**C++ Source:**

- **Module**: Engine

- **File**: AnimClassInterface.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend_in_profile` (BlendProfile): [Read-Write] Optional blend profile to use when blending this graph in (if BlendInTime > 0)

- `blend_in_time` (float): [Read-Write] Time to blend this graph in using Inertialization. Specify -1.0 to defer to the BlendOutTime of the previous graph.
To blend this graph in you must place an Inertialization node after the Linked Anim Graph node or Linked Anim Layer node that uses this graph.

- `blend_out_profile` (BlendProfile): [Read-Write] Optional blend profile to use when blending this graph out (if BlendOutTime > 0)

- `blend_out_time` (float): [Read-Write] Time to blend this graph out using Inertialization. Specify -1.0 to defer to the BlendInTime of the next graph.
To blend this graph out you must place an Inertialization node after the Linked Anim Graph node or Linked Anim Layer node that uses this graph.


### Table of Contents

- `unreal.AnimGraphBlendOptions`
  - `AnimGraphBlendOptions`