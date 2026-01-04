# unreal.AnimNode_BlendSpaceGraph

```python
class unreal.AnimNode_BlendSpaceGraph(x:float=0.0, y:float=0.0, group_name:Name='None', group_role:AnimGroupRole=Ellipsis)
```


**Bases:** ``AnimNode_BlendSpaceGraphBase``


Allows multiple animations to be blended between based on input parameters

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_BlendSpaceGraph.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `group_name` (Name): [Read-Write] The group name that we synchronize with (NAME\_None if it is not part of any group). Note that
this is the name of the group used to sync the output of this node - it will not force
syncing of animations contained by it. Animations inside this Blend Space have their own
options for syncing.

- `group_role` (AnimGroupRole): [Read-Write] The role this Blend Space can assume within the group (ignored if GroupName is not set). Note
that this is the role of the output of this node, not of animations contained by it.

- `x` (float): [Read-Write] The X coordinate to sample in the blendspace

- `y` (float): [Read-Write] The Y coordinate to sample in the blendspace


### Table of Contents

- `unreal.AnimNode_BlendSpaceGraph`
  - `AnimNode_BlendSpaceGraph`