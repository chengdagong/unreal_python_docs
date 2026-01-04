# unreal.EnhancedInputEditorSubsystem

```python
class unreal.EnhancedInputEditorSubsystem(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``EditorSubsystem``


The Enhanced Input Editor Subsystem can be used to process input outside of PIE within the editor.
Calling StartConsumingInput will allow the input preprocessor to drive Input Action delegates
to be fired in the editor.

This allows you to hook up Input Action delegates in Editor Utilities to make editor tools driven by
input.

**C++ Source:**

- **Plugin**: EnhancedInput

- **Module**: InputEditor

- **File**: EnhancedInputEditorSubsystem.h



---

**add_mapping_context**( _mapping_context_, _priority_, _options=[True, False, False]_) → `None`

Add a control mapping context.

Parameters:

- **mapping\_context** ( _InputMappingContext_) – A set of key to action mappings to apply to this player

- **priority** ( _int32_) – Higher priority mappings will be applied first and, if they consume input, will block lower priority mappings.

- **options** ( _ModifyContextOptions_) – Options to consider when adding this mapping context.



---

**add_tag_to_input_mode**( _tag_to_add_, _options=[True, False, False]_) → `None`

Adds the given “TagToAdd” to the current input mode tag container and triggers a rebuild of control mappings.

Parameters:

- **tag\_to\_add** ( _GameplayTag_) – The gameplay tag to add to the current input mode tag container

- **options** ( _ModifyContextOptions_) – Options for how to treat the control mappings rebuild



---

**append_tags_to_input_mode**( _tags_to_add_, _options=[True, False, False]_) → `None`

Appends the given “TagsToAdd” to the current input mode tag container and triggers a rebuild of control mappings.

Parameters:

- **tags\_to\_add** ( _GameplayTagContainer_) – The gameplay tag container to append

- **options** ( _ModifyContextOptions_) – Options for how to treat the control mappings rebuild



---

**clear_all_mappings**() → `None`

Remove all applied mapping contexts.


---

**get_all_player_mappable_action_key_mappings**() → `Array\ [EnhancedActionKeyMapping]`

Get an array of the currently applied key mappings that are marked as Player Mappable.

Return type:

Array\ [EnhancedActionKeyMapping]


---

**get_input_mode**() → `GameplayTagContainer`

Returns the current input mode set on Enhanced Input. This mode will control what mappings are
currently being processed by the player. If the Input Mapping Context’s InputModeQuery is
not empty and does not match this tag container, then it’s mappings will not be processed.

Return type:

GameplayTagContainer


---

**get_user_settings**() → `EnhancedInputUserSettings`

Get User Settings

Return type:

EnhancedInputUserSettings


---

**has_mapping_context**( _mapping_context_) → `int32orNone`

Check if a mapping context is applied to this subsystem’s owner.

Parameters:

**mapping\_context** ( _InputMappingContext_) – The mapping context to search for on the subsystem’s owner.

Returns:

True if the mapping context is applied

out\_found\_priority (int32): The priority of the mapping context if it is applied. -1 if the context is not applied

Return type:

int32 or None


---

**inject_input_for_action**( _action_, _raw_value_, _modifiers_, _triggers_) → `None`

Input simulation via injection. Runs modifiers and triggers delegates as if the input had come through the underlying input system as FKeys.
Applies action modifiers and triggers on top.

Parameters:

- **action** ( _InputAction_) – The Input Action to set inject input for

- **raw\_value** ( _InputActionValue_) – The value to set the action to

- **modifiers** ( _Array_ _\_ [_InputModifier_ _]_) – The modifiers to apply to the injected input.

- **triggers** ( _Array_ _\_ [_InputTrigger_ _]_) – The triggers to apply to the injected input.



---

**inject_input_for_player_mapping**( _mapping_name_, _raw_value_, _modifiers_, _triggers_) → `None`

Input simulation via injection. Runs modifiers and triggers delegates as if the input had come through the underlying input system as FKeys.
Applies action modifiers and triggers on top.

Parameters:

- **mapping\_name** ( _Name_) – The name of the player mapping that can be used for look up an associated UInputAction object.

- **raw\_value** ( _InputActionValue_) – The value to set the action to

- **modifiers** ( _Array_ _\_ [_InputModifier_ _]_) – The modifiers to apply to the injected input.

- **triggers** ( _Array_ _\_ [_InputTrigger_ _]_) – The triggers to apply to the injected input.



---

**inject_input_vector_for_action**( _action_, _value_, _modifiers_, _triggers_) → `None`

Input simulation via injection. Runs modifiers and triggers delegates as if the input had come through the underlying input system as FKeys.
Applies action modifiers and triggers on top.

Parameters:

- **action** ( _InputAction_) – The Input Action to set inject input for

- **value** ( _Vector_) – The value to set the action to (the type will be controlled by the Action)

- **modifiers** ( _Array_ _\_ [_InputModifier_ _]_) – The modifiers to apply to the injected input.

- **triggers** ( _Array_ _\_ [_InputTrigger_ _]_) – The triggers to apply to the injected input.



---

**inject_input_vector_for_player_mapping**( _mapping_name_, _value_, _modifiers_, _triggers_) → `None`

Input simulation via injection. Runs modifiers and triggers delegates as if the input had come through the underlying input system as FKeys.
Applies action modifiers and triggers on top.

Parameters:

- **mapping\_name** ( _Name_) – The name of the player mapping that can be used for look up an associated UInputAction object.

- **value** ( _Vector_) – The value to set the action to (the type will be controlled by the Action)

- **modifiers** ( _Array_ _\_ [_InputModifier_ _]_) – The modifiers to apply to the injected input.

- **triggers** ( _Array_ _\_ [_InputTrigger_ _]_) – The triggers to apply to the injected input.



---

**is_consuming_input**() → `bool`

Returns true if this subsystem is currently consuming input

Return type:

bool


---

**pop_input_component**( _input_component_) → `bool`

Removes this input component onto the stack to be processed by this subsystem’s tick function

Parameters:

**input\_component** ( _InputComponent_)

Return type:

bool


---

**push_input_component**( _input_component_) → `None`

Pushes this input component onto the stack to be processed by this subsystem’s tick function

Parameters:

**input\_component** ( _InputComponent_)


---

**query_keys_mapped_to_action**( _action_) → `Array\ [Key]`

Returns the keys mapped to the given action in the active input mapping contexts.

Parameters:

**action** ( _InputAction_)

Return type:

Array\ [Key]

query\_map\_key\_in\_active\_context\_set( _input\_context,action,key,blocking\_issues)->(MappingQueryResult,out\_issues=Array[MappingQueryIssue]_)

= DefaultMappingIssues::StandardFatal

Parameters:

- **input\_context** ( _InputMappingContext_)

- **action** ( _InputAction_)

- **key** ( _Key_)

- **blocking\_issues** ( _MappingQueryIssueFlag_)


Returns:

out\_issues (Array[MappingQueryIssue]):

Return type:

Array\ [MappingQueryIssue]

query\_map\_key\_in\_context\_set( _prioritized\_active\_contexts,input\_context,action,key,blocking\_issues)->(MappingQueryResult,out\_issues=Array[MappingQueryIssue]_)

= DefaultMappingIssues::StandardFatal

Parameters:

- **prioritized\_active\_contexts** ( _Array_ _\_ [_InputMappingContext_ _]_)

- **input\_context** ( _InputMappingContext_)

- **action** ( _InputAction_)

- **key** ( _Key_)

- **blocking\_issues** ( _MappingQueryIssueFlag_)


Returns:

out\_issues (Array[MappingQueryIssue]):

Return type:

Array\ [MappingQueryIssue]


---

**remove_mapping_context**( _mapping_context_, _options=[True, False, False]_) → `None`

Remove a specific control context.
This is safe to call even if the context is not applied.

Parameters:

- **mapping\_context** ( _InputMappingContext_) – Context to remove from the player

- **options** ( _ModifyContextOptions_) – Options to consider when removing this input mapping context



---

**remove_tag_from_input_mode**( _tag_to_remove_, _options=[True, False, False]_) → `None`

Removes the given tag from the current input mode and triggers a rebuild of control mappings.

Parameters:

- **tag\_to\_remove** ( _GameplayTag_) – The tag to remove from the current input mode

- **options** ( _ModifyContextOptions_) – Options for how to treat the control mappings rebuild



---

**remove_tags_from_input_mode**( _tags_to_remove_, _options=[True, False, False]_) → `None`

Removes tags from the current input mode and triggers a rebuild of control mappings.

Parameters:

- **tags\_to\_remove** ( _GameplayTagContainer_) – Tags to remove from the current input mode tag container

- **options** ( _ModifyContextOptions_) – Options for how to treat the control mappings rebuild



---

**request_rebuild_control_mappings**( _options=[True, False, False]_, _rebuild_type=InputMappingRebuildType.REBUILD_) → `None`

Flag player for reapplication of all mapping contexts at the end of this frame.
This is called automatically when adding or removing mappings contexts.

Parameters:

- **options** ( _ModifyContextOptions_) – Options to consider when removing this input mapping context

- **rebuild\_type** ( _InputMappingRebuildType_)



---

**set_input_mode**( _new_mode_, _options=[True, False, False]_) → `None`

Sets the current input mode on the player and triggers a rebuild of control mappings.

Parameters:

- **new\_mode** ( _GameplayTagContainer_) – The new input mode tag container to use

- **options** ( _ModifyContextOptions_) – Options for how to treat the control mappings rebuild.



---

**start_consuming_input**() → `None`

Start the consumption of input messages in this subsystem. This is required to have any Input Action delegates be fired.


---

**start_continuous_input_injection_for_action**( _action_, _raw_value_, _modifiers_, _triggers_) → `None`

Starts simulation of input via injection. This injects the given input every tick until it is stopped with StopContinuousInputInjectionForAction.

Parameters:

- **action** ( _InputAction_) – The Input Action to set inject input for

- **raw\_value** ( _InputActionValue_) – The value to set the action to (the type will be controlled by the Action)

- **modifiers** ( _Array_ _\_ [_InputModifier_ _]_) – The modifiers to apply to the injected input.

- **triggers** ( _Array_ _\_ [_InputTrigger_ _]_) – The triggers to apply to the injected input.



---

**start_continuous_input_injection_for_player_mapping**( _mapping_name_, _raw_value_, _modifiers_, _triggers_) → `None`

Starts simulation of input via injection. This injects the given input every tick until it is stopped with StopContinuousInputInjectionForAction.

Parameters:

- **mapping\_name** ( _Name_) – The name of the player mapping that can be used for look up an associated UInputAction object.

- **raw\_value** ( _InputActionValue_) – The value to set the action to (the type will be controlled by the Action)

- **modifiers** ( _Array_ _\_ [_InputModifier_ _]_) – The modifiers to apply to the injected input.

- **triggers** ( _Array_ _\_ [_InputTrigger_ _]_) – The triggers to apply to the injected input.



---

**stop_consuming_input**() → `None`

Tells this subsystem to stop ticking and consuming any input. This will stop any Input Action Delegates from being called.


---

**stop_continuous_input_injection_for_action**( _action_) → `None`

Stops continuous input injection for the given action.

Parameters:

**action** ( _InputAction_) – The action to stop injecting input for


---

**stop_continuous_input_injection_for_player_mapping**( _mapping_name_) → `None`

Stops continuous input injection for the given player mapping name.

Parameters:

**mapping\_name** ( _Name_) – The name of the player mapping that can be used for look up an associated UInputAction object.


---

**update_value_of_continuous_input_injection_for_action**( _action_, _raw_value_) → `None`

Update the value of a continuous input injection, preserving the state of triggers and modifiers.

Parameters:

- **action** ( _InputAction_) – The Input Action to set inject input for

- **raw\_value** ( _InputActionValue_) – The value to set the action to (the type will be controlled by the Action)



---

**update_value_of_continuous_input_injection_for_player_mapping**( _mapping_name_, _raw_value_) → `None`

Update the value of a continuous input injection for the given player mapping name, preserving the state of triggers and modifiers.

Parameters:

- **mapping\_name** ( _Name_) – The name of the player mapping that can be used for look up an associated UInputAction object.

- **raw\_value** ( _InputActionValue_) – The value to set the action to (the type will be controlled by the Action)


### Table of Contents

- `unreal.EnhancedInputEditorSubsystem`
  - `EnhancedInputEditorSubsystem`
    - `EnhancedInputEditorSubsystem.add_mapping_context()`
    - `EnhancedInputEditorSubsystem.add_tag_to_input_mode()`
    - `EnhancedInputEditorSubsystem.append_tags_to_input_mode()`
    - `EnhancedInputEditorSubsystem.clear_all_mappings()`
    - `EnhancedInputEditorSubsystem.get_all_player_mappable_action_key_mappings()`
    - `EnhancedInputEditorSubsystem.get_input_mode()`
    - `EnhancedInputEditorSubsystem.get_user_settings()`
    - `EnhancedInputEditorSubsystem.has_mapping_context()`
    - `EnhancedInputEditorSubsystem.inject_input_for_action()`
    - `EnhancedInputEditorSubsystem.inject_input_for_player_mapping()`
    - `EnhancedInputEditorSubsystem.inject_input_vector_for_action()`
    - `EnhancedInputEditorSubsystem.inject_input_vector_for_player_mapping()`
    - `EnhancedInputEditorSubsystem.is_consuming_input()`
    - `EnhancedInputEditorSubsystem.pop_input_component()`
    - `EnhancedInputEditorSubsystem.push_input_component()`
    - `EnhancedInputEditorSubsystem.query_keys_mapped_to_action()`
    - `EnhancedInputEditorSubsystem.query_map_key_in_active_context_set()`
    - `EnhancedInputEditorSubsystem.query_map_key_in_context_set()`
    - `EnhancedInputEditorSubsystem.remove_mapping_context()`
    - `EnhancedInputEditorSubsystem.remove_tag_from_input_mode()`
    - `EnhancedInputEditorSubsystem.remove_tags_from_input_mode()`
    - `EnhancedInputEditorSubsystem.request_rebuild_control_mappings()`
    - `EnhancedInputEditorSubsystem.set_input_mode()`
    - `EnhancedInputEditorSubsystem.start_consuming_input()`
    - `EnhancedInputEditorSubsystem.start_continuous_input_injection_for_action()`
    - `EnhancedInputEditorSubsystem.start_continuous_input_injection_for_player_mapping()`
    - `EnhancedInputEditorSubsystem.stop_consuming_input()`
    - `EnhancedInputEditorSubsystem.stop_continuous_input_injection_for_action()`
    - `EnhancedInputEditorSubsystem.stop_continuous_input_injection_for_player_mapping()`
    - `EnhancedInputEditorSubsystem.update_value_of_continuous_input_injection_for_action()`
    - `EnhancedInputEditorSubsystem.update_value_of_continuous_input_injection_for_player_mapping()`