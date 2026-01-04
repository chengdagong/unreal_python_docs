# unreal.AIESelectionSetItemName

```python
class unreal.AIESelectionSetItemName(name:str='', mirror_name:str='', type:int=0, owner_actor_name:str='')
```


**Bases:** ``StructBase``


Individual ‘Name” within a Seletion Set, maybe Actor Labe or Control Rig Control Name

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRigEditor

- **File**: SelectionSets.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `mirror_name` (str): [Read-Write] The Name of the selection set mirrored item for Control Rig Controls that have them

- `name` (str): [Read-Write] The Name of the selection set item\*, maybe an Actor Label or a ControlRig Control Name

- `owner_actor_name` (str): [Read-Write] The Name of the Owner Actor for Multi-Sets containing multiple rigs, may not be set

- `type` (int32): [Read-Write] The EAIESelectionSetItemType, 0 is a Control Rig Control, 1 is an Actor



---

_property_ `mirror_name`: str

[Read-Only] The Name of the selection set mirrored item for Control Rig Controls that have them

**Type:**

( str)


---

_property_ `name`: str

[Read-Only] The Name of the selection set item\*, maybe an Actor Label or a ControlRig Control Name

**Type:**

( str)


---

_property_ `owner_actor_name`: str

[Read-Write] The Name of the Owner Actor for Multi-Sets containing multiple rigs, may not be set

**Type:**

( str)


---

_property_ `type`: int

[Read-Only] The EAIESelectionSetItemType, 0 is a Control Rig Control, 1 is an Actor

**Type:**

(int32)

### Table of Contents

- `unreal.AIESelectionSetItemName`
  - `AIESelectionSetItemName`
    - `AIESelectionSetItemName.mirror_name`
    - `AIESelectionSetItemName.name`
    - `AIESelectionSetItemName.owner_actor_name`
    - `AIESelectionSetItemName.type`