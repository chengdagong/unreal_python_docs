# unreal.ControlRig

```python
class unreal.ControlRig(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``RigVMHost``


Runs logic for mapping input data to transforms (the “Rig”)

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: ControlRig.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `on_control_selected_bp` (OnControlSelectedBP): [Read-Write]



---

**clear_control_selection**( _setup_undo=False_) → `boolParameters:`

**setup\_undo** ( _bool_) – If set to true the stack will record the change for undo / redo

Return type:

bool


---

**create_transformable_control_handle**( _control_name_) → `TransformableControlHandleCreates a transformable control handle for the specified control to be used by the constraints system. Should use the UObject from`

ConstraintsScriptingLibrary::GetManager(UWorld\* InWorld)

Parameters:

**control\_name** ( _Name_)

Return type:

TransformableControlHandle


---

**current_control_selection**() → `Array\ [Name]`

Current Control Selection

Return type:

Array\ [Name]


---

_classmethod_ find_control_rigs( _outer_, _optional_class_)→Array\ [ControlRig]

Find Control Rigs

Parameters:

- **outer** ( _Object_)

- **optional\_class** ( _type_ _(_ _Class_ _)_)


Return type:

Array\ [ControlRig]


---

**get_hierarchy**() → `RigHierarchy`

Get Hierarchy

Return type:

RigHierarchy


---

**get_hosting_actor**() → `Actor`

Find the actor the rig is bound to, if any

Return type:

Actor


---

**is_control_selected**( _control_name_) → `bool`

Is Control Selected

Parameters:

**control\_name** ( _Name_)

Return type:

bool

_property_ on\_control\_selected\_bp _:OnControlSelectedBP_

[Read-Write]

**Type:**

(OnControlSelectedBP)


---

**request_construction**() → `None`

Requests to perform construction during the next execution


---

**select_control**( _control_name_, _select=True_, _setup_undo=False_) → `None`

Selects or deselects an element in the hierarchy

Parameters:

- **control\_name** ( _Name_) – The key of the element to select

- **select** ( _bool_) – If set to false the element will be deselected

- **setup\_undo** ( _bool_) – If set to true the stack will record the change for undo / redo



---

**supports_backwards_solve**() → `bool`

Contains a backwards solve event

Return type:

bool

### Table of Contents

- `unreal.ControlRig`
  - `ControlRig`
    - `ControlRig.clear_control_selection()`
    - `ControlRig.create_transformable_control_handle()`
    - `ControlRig.current_control_selection()`
    - `ControlRig.find_control_rigs()`
    - `ControlRig.get_hierarchy()`
    - `ControlRig.get_hosting_actor()`
    - `ControlRig.is_control_selected()`
    - `ControlRig.on_control_selected_bp`
    - `ControlRig.request_construction()`
    - `ControlRig.select_control()`
    - `ControlRig.supports_backwards_solve()`