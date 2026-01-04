# unreal.AIESelectionSetItem

```python
class unreal.AIESelectionSetItem(item_name:Text='', names:None=\[\], view_data:AIESelectionSetItemViewData=Ellipsis)
```


**Bases:** ``StructBase``


Main selection set item, has it’s name, it’s view data, and array of names making up the set

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRigEditor

- **File**: SelectionSets.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `item_name` (Text): [Read-Write] The Name of the Set

- `names` (Array[AIESelectionSetItemName]): [Read-Write] The collection of set items that make up the set, basically an array of names with some metadata

- `view_data` (AIESelectionSetItemViewData): [Read-Write] Viewing Data for the set, like location and color



---

_property_ `item_name`: Text

[Read-Only] The Name of the Set

**Type:**

( Text)


---

_property_ `names`: None

[Read-Only] The collection of set items that make up the set, basically an array of names with some metadata

**Type:**

( Array\ [AIESelectionSetItemName])


---

_property_ `view_data`: AIESelectionSetItemViewData

[Read-Only] Viewing Data for the set, like location and color

**Type:**

( AIESelectionSetItemViewData)

### Table of Contents

- `unreal.AIESelectionSetItem`
  - `AIESelectionSetItem`
    - `AIESelectionSetItem.item_name`
    - `AIESelectionSetItem.names`
    - `AIESelectionSetItem.view_data`