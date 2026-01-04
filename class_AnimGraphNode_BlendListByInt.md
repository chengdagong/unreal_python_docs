# unreal.AnimGraphNode_BlendListByInt

```python
class unreal.AnimGraphNode_BlendListByInt(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimGraphNode_BlendListBase``


Anim Graph Node Blend List by Int

**C++ Source:**

- **Module**: AnimGraph

- **File**: AnimGraphNode\_BlendListByInt.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `become_relevant_function` (MemberReference): [Read-Write] Function called when the node becomes relevant, meaning it goes from having no weight to any weight.

- `binding` (AnimGraphNodeBinding): [Read-Write] Bindings for pins that this node exposes

- `initial_update_function` (MemberReference): [Read-Write] Function called before the node is updated for the first time

- `node` (AnimNode\_BlendListByInt): [Read-Write]

- `show_pin_for_properties` (Array[OptionalPinFromProperty]): [Read-Write]

- `tag` (Name): [Read-Write] Optional reference tag name. If this is set then this node can be referenced from elsewhere in this animation blueprint using an anim node reference

- `update_function` (MemberReference): [Read-Write] Function called when the node is updated


### Table of Contents

- `unreal.AnimGraphNode_BlendListByInt`
  - `AnimGraphNode_BlendListByInt`