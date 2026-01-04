# unreal.SubobjectDataSubsystem

```python
class unreal.SubobjectDataSubsystem(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``EngineSubsystem``


The Subobject Data Subsystem will produce the reflected subobject data
based on a given root object. A root object can be anything, an actor
instance clicked on via the level editor, a UBlueprint\* by opening an asset,
or something piped in from python or other scripting languages.

**C++ Source:**

- **Module**: SubobjectDataInterface

- **File**: SubobjectDataSubsystem.h


add\_new\_subobject( _params)->(SubobjectDataHandle_, _fail\_reason=Text_)

Add a new subobject as a child to the given parent object

Parameters:

**params** ( _AddNewSubobjectParams_) – Options to consider when adding this subobject

Returns:

FSubobjectDataHandle Handle to the newly created subobject, Invalid handle if creation failed

fail\_reason (Text):

Return type:

Text


---

**attach_subobject**( _owner_handle_, _child_to_add_handle_) → `bool`

Add the given subobject to a new owner. This will remove the subobject from its previous
owner if necessary.

Parameters:

- **owner\_handle** ( _SubobjectDataHandle_) – The new owner to attach to

- **child\_to\_add\_handle** ( _SubobjectDataHandle_) – Handle to the subobject that will become a child of the owner


Returns:

true if the child was added successfully

Return type:

bool


---

**can_copy_subobjects**( _handles_) → `bool`

Returns true if the given array of handles represents subobjects that
can be copied.

Parameters:

**handles** ( _Array_ _\_ [_SubobjectDataHandle_ _]_)

Return type:

bool


---

**can_paste_subobjects**( _root_handle_, _bp_context=None_) → `bool`

Can Paste Subobjects

Parameters:

- **root\_handle** ( _SubobjectDataHandle_)

- **bp\_context** ( _Blueprint_)


Return type:

bool


---

**change_subobject_class**( _handle_, _new_class_) → `bool`

Attempts to change the subclass of a native component

Parameters:

- **handle** ( _SubobjectDataHandle_) – Handle to the subobject to change class of

- **new\_class** ( _type_ _(_ _Class_ _)_) – The new class that is desired for the given subobject


Returns:

True if the class change was successful, false otherwise.

Return type:

bool


---

**copy_subobjects**( _handles_, _bp_context_) → `None`

Copy Subobjects

Parameters:

- **handles** ( _Array_ _\_ [_SubobjectDataHandle_ _]_)

- **bp\_context** ( _Blueprint_)


_classmethod_ create\_new\_bp\_component( _component\_class_, _new\_class\_path_, _new\_class\_name_)

Creates a new Blueprint component from the specified class type
The user will be prompted to pick a new subclass name and a blueprint asset will be created

Parameters:

- **component\_class** ( _type_ _(_ _Class_ _)_)

- **new\_class\_path** ( _str_)

- **new\_class\_name** ( _str_)


Returns:

The new class that was created

Return type:

type( Class)

_classmethod_ create\_new\_cpp\_component( _component\_class_, _new\_class\_path_, _new\_class\_name_)

Creates a new C++ component from the specified class type
The user will be prompted to pick a new subclass name and code will be recompiled

Parameters:

- **component\_class** ( _type_ _(_ _Class_ _)_)

- **new\_class\_path** ( _str_)

- **new\_class\_name** ( _str_)


Returns:

The new class that was created

Return type:

type( Class)


---

**delete_subobject**( _context_handle_, _subobject_to_delete_, _bp_context=None_) → `int32`

Attempts to delete the given subobject from its blueprint context

Parameters:

- **context\_handle** ( _SubobjectDataHandle_) – The owning context of the subobjects that should be removed

- **subobject\_to\_delete** ( _SubobjectDataHandle_) – The subobject handles that should be deleted

- **bp\_context** ( _Blueprint_) – The blueprint context for the given


Returns:

The number of subobjects successfully deleted

Return type:

int32


---

**delete_subobjects**( _context_handle_, _subobjects_to_delete_, _bp_context=None_) → `int32`

Attempts to delete the given array of subobjects from their context

Parameters:

- **context\_handle** ( _SubobjectDataHandle_) – The owning context of the subobjects that should be removed

- **subobjects\_to\_delete** ( _Array_ _\_ [_SubobjectDataHandle_ _]_) – Array of subobject handles that should be deleted

- **bp\_context** ( _Blueprint_) – The blueprint context for the given


Returns:

The number of subobjects successfully deleted

Return type:

int32


---

**detach_subobject**( _owner_handle_, _child_to_remove_) → `bool`

Remove the child subobject from the owner

Parameters:

- **owner\_handle** ( _SubobjectDataHandle_)

- **child\_to\_remove** ( _SubobjectDataHandle_)


Returns:

True if the child was successfully removed.

Return type:

bool


---

**duplicate_subobjects**( _context_, _subobjects_to_dup_, _bp_context_) → `Array\ [SubobjectDataHandle]`

Duplicate the given array of subobjects on the context.

Parameters:

- **context** ( _SubobjectDataHandle_) – The owning context that the subobjects to dup come from

- **subobjects\_to\_dup** ( _Array_ _\_ [_SubobjectDataHandle_ _]_) – Array of handles of existing subobjects you would like to have duplicated

- **bp\_context** ( _Blueprint_) – Pointer to the current blueprint context if necessary. Use nullptr if dealing with instances


Returns:

out\_new\_subobjects (Array[SubobjectDataHandle]): Array that will be populated with any newly created subobjects

Return type:

Array\ [SubobjectDataHandle]


---

**find_handle_for_object**( _context_, _object_to_find_, _bp_context=None_) → `SubobjectDataHandle`

Attempt to find an existing handle for the given object.

Parameters:

- **context** ( _SubobjectDataHandle_) – The context that the object to find is within

- **object\_to\_find** ( _Object_) – The object that you want to find the handle for within the context

- **bp\_context** ( _Blueprint_)


Returns:

FSubobjectDataHandle The subobject handle for the object, Invalid handle if not found.

Return type:

SubobjectDataHandle


---

**is_valid_rename**( _handle_, _new_text_) → `TextorNone`

Returns true if the given new text is a valid option to rename the
subobject with the given handle. Populates the OutErrorMessage if
it is not valid.

Parameters:

- **handle** ( _SubobjectDataHandle_) – Handle to the subobject that is being checked

- **new\_text** ( _Text_) – The new name that is desired


Returns:

True if the rename is valid

out\_error\_message (Text): The reasoning for an invalid name

Return type:

Text or None


---

**k2_delete_subobject_from_instance**( _context_handle_, _subobject_to_delete_) → `int32`

Attempts to delete the given subobject from its context

Parameters:

- **context\_handle** ( _SubobjectDataHandle_) – The owning context of the subobjects that should be removed

- **subobject\_to\_delete** ( _SubobjectDataHandle_) – The subobject handles that should be deleted


Returns:

The number of subobjects successfully deleted

Return type:

int32


---

**k2_delete_subobjects_from_instance**( _context_handle_, _subobjects_to_delete_) → `int32`

Attempts to delete the given array of subobjects from their context

Parameters:

- **context\_handle** ( _SubobjectDataHandle_) – The owning context of the subobjects that should be removed

- **subobjects\_to\_delete** ( _Array_ _\_ [_SubobjectDataHandle_ _]_) – Array of subobject handles that should be deleted


Returns:

The number of subobjects successfully deleted

Return type:

int32


---

**k2_find_subobject_data_from_handle**( _handle_) → `SubobjectDataorNone`

Attempt to find the subobject data for a given handle. OutData will only
be valid if the function returns true.

Parameters:

**handle** ( _SubobjectDataHandle_) – Handle of the subobject data you want to acquire

Returns:

bool true if the data was found

out\_data (SubobjectData): Reference to the subobject data to populate

Return type:

SubobjectData or None


---

**k2_gather_subobject_data_for_blueprint**( _context_) → `Array\ [SubobjectDataHandle]`

Gather all subobjects that the given Blueprint context has. Populates an array of
handles that will have the given context and all it’s subobjects.

Parameters:

**context** ( _Blueprint_) – Object to gather subobjects for

Returns:

out\_array (Array[SubobjectDataHandle]): Array to populate (will be emptied first)

Return type:

Array\ [SubobjectDataHandle]


---

**k2_gather_subobject_data_for_instance**( _context_) → `Array\ [SubobjectDataHandle]`

Gather all subobjects that the given actor instance has. Populates an array of
handles that will have the given context and all it’s subobjects.

Parameters:

**context** ( _Actor_) – Object to gather subobjects for

Returns:

out\_array (Array[SubobjectDataHandle]): Array to populate (will be emptied first)

Return type:

Array\ [SubobjectDataHandle]


---

**make_new_scene_root**( _context_, _new_scene_root_, _bp_context_) → `bool`

Make New Scene Root

Parameters:

- **context** ( _SubobjectDataHandle_)

- **new\_scene\_root** ( _SubobjectDataHandle_)

- **bp\_context** ( _Blueprint_)


Return type:

bool


---

**paste_subobjects**( _paste_to_context_, _new_parent_handles_, _bp_context_) → `Array\ [SubobjectDataHandle]`

Pastes the given subobjects to the PasteToContext.

Parameters:

- **paste\_to\_context** ( _SubobjectDataHandle_) – The subobject to paste things onto

- **new\_parent\_handles** ( _Array_ _\_ [_SubobjectDataHandle_ _]_) – Array of Subobject Handles that you would like to paste

- **bp\_context** ( _Blueprint_) – Blueprint to use, if you are pasting to a blueprint. Null if pasting to an instanced object


Returns:

out\_pasted\_handles (Array[SubobjectDataHandle]): Array populated with the handles to the newly pasted subobjects

Return type:

Array\ [SubobjectDataHandle]


---

**rename_subobject**( _handle_, _new_name_) → `bool`

Attempts to rename the given subobject to the new name.

Parameters:

- **handle** ( _SubobjectDataHandle_) – Handle to the subobject to rename

- **new\_name** ( _Text_) – The new name that is desired for the given subobject


Returns:

True if the rename was successful, false otherwise.

Return type:

bool


---

_classmethod_ rename_subobject_member_variable( _bp_context_, _handle_, _new_name_)→None

Rename Subobject Member Variable

Parameters:

- **bp\_context** ( _Blueprint_)

- **handle** ( _SubobjectDataHandle_)

- **new\_name** ( _Name_)



---

**reparent_subobject**( _params_, _to_reparent_handle_) → `bool`

Attempts to reparent the given subobject to the new parent

Parameters:

- **params** ( _ReparentSubobjectParams_)

- **to\_reparent\_handle** ( _SubobjectDataHandle_) – The handle of the subobject that will get moved


Returns:

True if the reparent was successful, false otherwise.

Return type:

bool


---

**reparent_subobjects**( _params_, _handles_to_move_) → `bool`

Attempts to reparent all subobjects in the HandlesToMove array to the new parent handle.

Parameters:

- **params** ( _ReparentSubobjectParams_)

- **handles\_to\_move** ( _Array_ _\_ [_SubobjectDataHandle_ _]_)


Return type:

bool

### Table of Contents

- `unreal.SubobjectDataSubsystem`
  - `SubobjectDataSubsystem`
    - `SubobjectDataSubsystem.add_new_subobject()`
    - `SubobjectDataSubsystem.attach_subobject()`
    - `SubobjectDataSubsystem.can_copy_subobjects()`
    - `SubobjectDataSubsystem.can_paste_subobjects()`
    - `SubobjectDataSubsystem.change_subobject_class()`
    - `SubobjectDataSubsystem.copy_subobjects()`
    - `SubobjectDataSubsystem.create_new_bp_component()`
    - `SubobjectDataSubsystem.create_new_cpp_component()`
    - `SubobjectDataSubsystem.delete_subobject()`
    - `SubobjectDataSubsystem.delete_subobjects()`
    - `SubobjectDataSubsystem.detach_subobject()`
    - `SubobjectDataSubsystem.duplicate_subobjects()`
    - `SubobjectDataSubsystem.find_handle_for_object()`
    - `SubobjectDataSubsystem.is_valid_rename()`
    - `SubobjectDataSubsystem.k2_delete_subobject_from_instance()`
    - `SubobjectDataSubsystem.k2_delete_subobjects_from_instance()`
    - `SubobjectDataSubsystem.k2_find_subobject_data_from_handle()`
    - `SubobjectDataSubsystem.k2_gather_subobject_data_for_blueprint()`
    - `SubobjectDataSubsystem.k2_gather_subobject_data_for_instance()`
    - `SubobjectDataSubsystem.make_new_scene_root()`
    - `SubobjectDataSubsystem.paste_subobjects()`
    - `SubobjectDataSubsystem.rename_subobject()`
    - `SubobjectDataSubsystem.rename_subobject_member_variable()`
    - `SubobjectDataSubsystem.reparent_subobject()`
    - `SubobjectDataSubsystem.reparent_subobjects()`