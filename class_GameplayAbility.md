# unreal.GameplayAbility

```python
class unreal.GameplayAbility(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Abilities define custom gameplay logic that can be activated by players or external game logic

**C++ Source:**

- **Plugin**: GameplayAbilities

- **Module**: GameplayAbilities

- **File**: GameplayAbility.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `ability_tags` (GameplayTagContainer): [Read-Write]

- `ability_triggers` (Array[AbilityTriggerData]): [Read-Write] Triggers to determine if this ability should execute in response to an event

- `activation_blocked_tags` (GameplayTagContainer): [Read-Write] This ability is blocked if the activating actor/component has any of these tags

- `activation_owned_tags` (GameplayTagContainer): [Read-Write] Tags to apply to activating owner while this ability is active. These are replicated if ReplicateActivationOwnedTags is enabled in AbilitySystemGlobals.

- `activation_required_tags` (GameplayTagContainer): [Read-Write] This ability can only be activated if the activating actor/component has all of these tags

- `block_abilities_with_tag` (GameplayTagContainer): [Read-Write] Abilities with these tags are blocked while this ability is active

- `cancel_abilities_with_tag` (GameplayTagContainer): [Read-Write] Abilities with these tags are cancelled when this ability is executed

- `cooldown_gameplay_effect_class` (type(Class)): [Read-Write] This GameplayEffect represents the cooldown. It will be applied when the ability is committed and the ability cannot be used again until it is expired.

- `cost_gameplay_effect_class` (type(Class)): [Read-Write] This GameplayEffect represents the cost (mana, stamina, etc) of the ability. It will be applied when the ability is committed.

- `current_activation_info` (GameplayAbilityActivationInfo): [Read-Write] This is information specific to this instance of the ability. E.g, whether it is predicting, authoring, confirmed, etc.

- `current_event_data` (GameplayEventData): [Read-Write] Information specific to this instance of the ability, if it was activated by an event

- `instancing_policy` (GameplayAbilityInstancingPolicy): [Read-Write] How the ability is instanced when executed. This limits what an ability can do in its implementation.

- `mark_pending_kill_on_ability_end` (bool): [Read-Write]
deprecated: This is unsafe. Do not use.

- `net_execution_policy` (GameplayAbilityNetExecutionPolicy): [Read-Write] How does an ability execute on the network. Does a client “ask and predict”, “ask and wait”, “don’t ask (just do it)”.

- `net_security_policy` (GameplayAbilityNetSecurityPolicy): [Read-Write] What protections does this ability have? Should the client be allowed to request changes to the execution of the ability?

- `replicate_input_directly` (bool): [Read-Write] If true, this ability will always replicate input press/release events to the server.

- `replication_policy` (GameplayAbilityReplicationPolicy): [Read-Write] How an ability replicates state/events to everyone on the network. Replication is not required for NetExecutionPolicy.

- `retrigger_instanced_ability` (bool): [Read-Write] if true, and trying to activate an already active instanced ability, end it and re-trigger it.

- `server_respects_remote_ability_cancellation` (bool): [Read-Write] If this is set, the server-side version of the ability can be canceled by the client-side version. The client-side version can always be canceled by the server.

- `source_blocked_tags` (GameplayTagContainer): [Read-Write] This ability is blocked if the source actor/component has any of these tags

- `source_required_tags` (GameplayTagContainer): [Read-Write] This ability can only be activated if the source actor/component has all of these tags

- `target_blocked_tags` (GameplayTagContainer): [Read-Write] This ability is blocked if the target actor/component has any of these tags

- `target_required_tags` (GameplayTagContainer): [Read-Write] This ability can only be activated if the target actor/component has all of these tags



---

**activate_ability**() → `None`

The main function that defines what an ability does.
-Child classes will want to override this
-This function graph should call CommitAbility
-This function graph should call EndAbility

Latent/async actions are ok in this graph. Note that Commit and EndAbility calling requirements speak to the K2\_ActivateAbility graph.
In C++, the call to K2\_ActivateAbility() may return without CommitAbility or EndAbility having been called. But it is expected that this
will only occur when latent/async actions are pending. When K2\_ActivateAbility logically finishes, then we will expect Commit/End to have been called.


---

**activate_ability_from_event**( _event_data_) → `None`

K2 Activate Ability from Event

Parameters:

**event\_data** ( _GameplayEventData_)


---

**add_gameplay_cue**( _gameplay_cue_tag_, _context_, _remove_on_ability_end=True_) → `None`

Adds a persistent gameplay cue to the ability owner. Optionally will remove if ability ends

Parameters:

- **gameplay\_cue\_tag** ( _GameplayTag_)

- **context** ( _GameplayEffectContextHandle_)

- **remove\_on\_ability\_end** ( _bool_)



---

**add_gameplay_cue_with_params**( _gameplay_cue_tag_, _gameplay_cue_parameter_, _remove_on_ability_end=True_) → `None`

Adds a persistent gameplay cue to the ability owner. Optionally will remove if ability ends

Parameters:

- **gameplay\_cue\_tag** ( _GameplayTag_)

- **gameplay\_cue\_parameter** ( _GameplayCueParameters_)

- **remove\_on\_ability\_end** ( _bool_)



---

**apply_gameplay_effect_spec_to_owner**( _effect_spec_handle_) → `ActiveGameplayEffectHandle`

Apply a previously created gameplay effect spec to the owner of this ability

Parameters:

**effect\_spec\_handle** ( _GameplayEffectSpecHandle_)

Return type:

ActiveGameplayEffectHandle


---

**apply_gameplay_effect_spec_to_target**( _effect_spec_handle_, _target_data_) → `Array\ [ActiveGameplayEffectHandle]`

Apply a previously created gameplay effect spec to a target

Parameters:

- **effect\_spec\_handle** ( _GameplayEffectSpecHandle_)

- **target\_data** ( _GameplayAbilityTargetDataHandle_)


Return type:

Array\ [ActiveGameplayEffectHandle]


---

**apply_gameplay_effect_to_owner**( _gameplay_effect_class_, _gameplay_effect_level=1_, _stacks=1_) → `ActiveGameplayEffectHandle`

Apply a gameplay effect to the owner of this ability

Parameters:

- **gameplay\_effect\_class** ( _type_ _(_ _Class_ _)_)

- **gameplay\_effect\_level** ( _int32_)

- **stacks** ( _int32_)


Return type:

ActiveGameplayEffectHandle


---

**apply_gameplay_effect_to_target**( _target_data_, _gameplay_effect_class_, _gameplay_effect_level=1_, _stacks=1_) → `Array\ [ActiveGameplayEffectHandle]`

Apply a gameplay effect to a Target

Parameters:

- **target\_data** ( _GameplayAbilityTargetDataHandle_)

- **gameplay\_effect\_class** ( _type_ _(_ _Class_ _)_)

- **gameplay\_effect\_level** ( _int32_)

- **stacks** ( _int32_)


Return type:

Array\ [ActiveGameplayEffectHandle]


---

**can_activate_ability**( _actor_info_, _handle_) → `GameplayTagContainerorNone`

Returns true if this ability can be activated right now. Has no side effects

Parameters:

- **actor\_info** ( _GameplayAbilityActorInfo_)

- **handle** ( _GameplayAbilitySpecHandle_)


Returns:

relevant\_tags (GameplayTagContainer):

Return type:

GameplayTagContainer or None


---

**cancel_ability**() → `None`

Call from Blueprint to cancel the ability naturally


---

**cancel_task_by_instance_name**( _instance_name_) → `None`

Add any task with this instance name to a list to be canceled (not ended) next frame. See also EndTaskByInstanceName.

Parameters:

**instance\_name** ( _Name_)


---

**check_ability_cooldown**() → `bool`

Checks the ability’s cooldown, but does not apply it.

Return type:

bool


---

**check_ability_cost**() → `bool`

Checks the ability’s cost, but does not apply it.

Return type:

bool


---

**commit_ability**() → `bool`

Attempts to commit the ability (spend resources, etc). This our last chance to fail. Child classes that override ActivateAbility must call this themselves!

Return type:

bool


---

**commit_ability_cooldown**( _broadcast_commit_event=False_, _force_cooldown=False_) → `bool`

Attempts to commit the ability’s cooldown only. If BroadcastCommitEvent is true, it will broadcast the commit event that tasks like WaitAbilityCommit are listening for.

Parameters:

- **broadcast\_commit\_event** ( _bool_)

- **force\_cooldown** ( _bool_)


Return type:

bool


---

**commit_ability_cost**( _broadcast_commit_event=False_) → `bool`

Attempts to commit the ability’s cost only. If BroadcastCommitEvent is true, it will broadcast the commit event that tasks like WaitAbilityCommit are listening for.

Parameters:

**broadcast\_commit\_event** ( _bool_)

Return type:

bool


---

**commit_execute**() → `None`

BP event called from CommitAbility


---

**confirm_task_by_instance_name**( _instance_name_, _end_task_) → `None`

Finds all currently active tasks named InstanceName and confirms them. What this means depends on the individual task. By default, this does nothing other than ending if bEndTask is true.

Parameters:

- **instance\_name** ( _Name_)

- **end\_task** ( _bool_)



---

_property_ `current_activation_info`: GameplayAbilityActivationInfo

[Read-Only] This is information specific to this instance of the ability. E.g, whether it is predicting, authoring, confirmed, etc.

**Type:**

( GameplayAbilityActivationInfo)


---

_property_ `current_event_data`: GameplayEventData

[Read-Only] Information specific to this instance of the ability, if it was activated by an event

**Type:**

( GameplayEventData)


---

**end_ability**() → `None`

Call from blueprints to forcibly end the ability without canceling it. This will replicate the end ability to the client or server which can interrupt tasks


---

**end_ability_locally**() → `None`

Call from blueprints to end the ability naturally. This will only end predicted abilities locally, allowing it end naturally on the client or server


---

**end_ability_state**( _optional_state_name_to_end_) → `None`

Ends any active ability state task with the given name. If name is ‘None’ all active states will be ended (in an arbitrary order).

Parameters:

**optional\_state\_name\_to\_end** ( _Name_)


---

**end_task_by_instance_name**( _instance_name_) → `None`

Add any task with this instance name to a list to be ended (not canceled) next frame. See also CancelTaskByInstanceName.

Parameters:

**instance\_name** ( _Name_)


---

**execute_gameplay_cue**( _gameplay_cue_tag_, _context_) → `None`

Invoke a gameplay cue on the ability owner

Parameters:

- **gameplay\_cue\_tag** ( _GameplayTag_)

- **context** ( _GameplayEffectContextHandle_)



---

**execute_gameplay_cue_with_params**( _gameplay_cue_tag_, _gameplay_cue_parameters_) → `None`

Invoke a gameplay cue on the ability owner, with extra parameters

Parameters:

- **gameplay\_cue\_tag** ( _GameplayTag_)

- **gameplay\_cue\_parameters** ( _GameplayCueParameters_)



---

**get_ability_level**() → `int32`

Returns current level of the Ability

Return type:

int32


---

**get_ability_level_bp**( _handle_, _actor_info_) → `int32`

Returns current ability level for non instanced abilities. You must call this version in these contexts!

Parameters:

- **handle** ( _GameplayAbilitySpecHandle_)

- **actor\_info** ( _GameplayAbilityActorInfo_)


Return type:

int32


---

**get_ability_system_component_from_actor_info**() → `AbilitySystemComponent`

Returns the AbilitySystemComponent that is activating this ability

Return type:

AbilitySystemComponent


---

**get_actor_info**() → `GameplayAbilityActorInfo`

Returns the actor info associated with this ability, has cached pointers to useful objects

Return type:

GameplayAbilityActorInfo


---

**get_avatar_actor_from_actor_info**() → `Actor`

Returns the physical actor that is executing this ability. May be null

Return type:

Actor


---

**get_context_from_owner**( _optional_target_data_) → `GameplayEffectContextHandle`

Generates a GameplayEffectContextHandle from our owner and an optional TargetData.

Parameters:

**optional\_target\_data** ( _GameplayAbilityTargetDataHandle_)

Return type:

GameplayEffectContextHandle


---

**get_cooldown_time_remaining**() → `float`

Returns the time in seconds remaining on the currently active cooldown.

Return type:

float


---

**get_current_montage**() → `AnimMontage`

Returns the currently playing montage for this ability, if any

Return type:

AnimMontage


---

**get_current_source_object**() → `Object`

Retrieves the SourceObject associated with this ability. Can only be called on instanced abilities.

Return type:

Object


---

**get_granted_by_effect_context**() → `GameplayEffectContextHandle`

Retrieves the EffectContext of the GameplayEffect that granted this ability. Can only be called on instanced abilities.

Return type:

GameplayEffectContextHandle


---

**get_owning_actor_from_actor_info**() → `Actor`

Returns the actor that owns this ability, which may not have a physical location

Return type:

Actor


---

**get_owning_component_from_actor_info**() → `SkeletalMeshComponent`

Convenience method for abilities to get skeletal mesh component - useful for aiming abilities

Return type:

SkeletalMeshComponent


---

**get_source_object_bp**( _handle_, _actor_info_) → `Object`

Retrieves the SourceObject associated with this ability. Callable on non instanced

Parameters:

- **handle** ( _GameplayAbilitySpecHandle_)

- **actor\_info** ( _GameplayAbilityActorInfo_)


Return type:

Object


---

**invalidate_client_prediction_key**() → `None`

Invalidates the current prediction key. This should be used in cases where there is a valid prediction window, but the server is doing logic that only it can do, and afterwards performs an action that the client could predict (had the client been able to run the server-only code prior).
This returns instantly and has no other side effects other than clearing the current prediction key.


---

**is_locally_controlled**() → `bool`

True if the owning actor is locally controlled, true in single player

Return type:

bool


---

**k2_has_authority**() → `bool`

K2 Has Authority

Return type:

bool


---

**make_outgoing_gameplay_effect_spec**( _gameplay_effect_class_, _level=1.000000_) → `GameplayEffectSpecHandle`

Convenience method for abilities to get outgoing gameplay effect specs (for example, to pass on to projectiles to apply to whoever they hit)

Parameters:

- **gameplay\_effect\_class** ( _type_ _(_ _Class_ _)_)

- **level** ( _float_)


Return type:

GameplayEffectSpecHandle


---

**make_target_location_info_from_owner_actor**() → `GameplayAbilityTargetingLocationInfo`

Creates a target location from where the owner avatar is

Return type:

GameplayAbilityTargetingLocationInfo


---

**make_target_location_info_from_owner_skeletal_mesh_component**( _socket_name_) → `GameplayAbilityTargetingLocationInfo`

Creates a target location from a socket on the owner avatar’s skeletal mesh

Parameters:

**socket\_name** ( _Name_)

Return type:

GameplayAbilityTargetingLocationInfo


---

_property_ `mark_pending_kill_on_ability_end`: bool

[Read-Only]
deprecated: This is unsafe. Do not use.

**Type:**

( bool)


---

**montage_jump_to_section**( _section_name_) → `None`

Immediately jumps the active montage to a section

Parameters:

**section\_name** ( _Name_)


---

**montage_set_next_section_name**( _from_section_name_, _to_section_name_) → `None`

Sets pending section on active montage

Parameters:

- **from\_section\_name** ( _Name_)

- **to\_section\_name** ( _Name_)



---

**montage_stop**( _override_blend_out_time=-1.000000_) → `None`

Stops the current animation montage.

Parameters:

**override\_blend\_out\_time** ( _float_)


---

**on_end_ability**( _was_cancelled_) → `None`

Blueprint event, will be called if an ability ends normally or abnormally

Parameters:

**was\_cancelled** ( _bool_)


---

**remove_gameplay_cue**( _gameplay_cue_tag_) → `None`

Removes a persistent gameplay cue from the ability owner

Parameters:

**gameplay\_cue\_tag** ( _GameplayTag_)


---

**remove_gameplay_effect_from_owner_with_asset_tags**( _with_asset_tags_, _stacks_to_remove=-1_) → `None`

Removes GameplayEffects from owner which match the given asset level tags

Parameters:

- **with\_asset\_tags** ( _GameplayTagContainer_)

- **stacks\_to\_remove** ( _int32_)



---

**remove_gameplay_effect_from_owner_with_granted_tags**( _with_granted_tags_, _stacks_to_remove=-1_) → `None`

Removes GameplayEffects from owner which grant the given tags

Parameters:

- **with\_granted\_tags** ( _GameplayTagContainer_)

- **stacks\_to\_remove** ( _int32_)



---

**remove_gameplay_effect_from_owner_with_handle**( _handle_, _stacks_to_remove=-1_) → `None`

Removes GameplayEffect from owner that match the given handle

Parameters:

- **handle** ( _ActiveGameplayEffectHandle_)

- **stacks\_to\_remove** ( _int32_)



---

**remove_granted_by_effect**() → `None`

Removes the GameplayEffect that granted this ability. Can only be called on instanced abilities.


---

**send_gameplay_event**( _event_tag_, _payload_) → `None`

Sends a gameplay event, also creates a prediction window

Parameters:

- **event\_tag** ( _GameplayTag_)

- **payload** ( _GameplayEventData_)



---

**set_can_be_canceled**( _can_be_canceled_) → `None`

Sets whether the ability should ignore cancel requests. Only valid on instanced abilities

Parameters:

**can\_be\_canceled** ( _bool_)


---

**set_should_block_other_abilities**( _should_block_abilities_) → `None`

Sets rather ability block flags are enabled or disabled. Only valid on instanced abilities

Parameters:

**should\_block\_abilities** ( _bool_)


---

**should_ability_respond_to_event**( _actor_info_, _payload_) → `bool`

Returns true if this ability can be activated right now. Has no side effects

Parameters:

- **actor\_info** ( _GameplayAbilityActorInfo_)

- **payload** ( _GameplayEventData_)


Return type:

bool

### Table of Contents

- `unreal.GameplayAbility`
  - `GameplayAbility`
    - `GameplayAbility.activate_ability()`
    - `GameplayAbility.activate_ability_from_event()`
    - `GameplayAbility.add_gameplay_cue()`
    - `GameplayAbility.add_gameplay_cue_with_params()`
    - `GameplayAbility.apply_gameplay_effect_spec_to_owner()`
    - `GameplayAbility.apply_gameplay_effect_spec_to_target()`
    - `GameplayAbility.apply_gameplay_effect_to_owner()`
    - `GameplayAbility.apply_gameplay_effect_to_target()`
    - `GameplayAbility.can_activate_ability()`
    - `GameplayAbility.cancel_ability()`
    - `GameplayAbility.cancel_task_by_instance_name()`
    - `GameplayAbility.check_ability_cooldown()`
    - `GameplayAbility.check_ability_cost()`
    - `GameplayAbility.commit_ability()`
    - `GameplayAbility.commit_ability_cooldown()`
    - `GameplayAbility.commit_ability_cost()`
    - `GameplayAbility.commit_execute()`
    - `GameplayAbility.confirm_task_by_instance_name()`
    - `GameplayAbility.current_activation_info`
    - `GameplayAbility.current_event_data`
    - `GameplayAbility.end_ability()`
    - `GameplayAbility.end_ability_locally()`
    - `GameplayAbility.end_ability_state()`
    - `GameplayAbility.end_task_by_instance_name()`
    - `GameplayAbility.execute_gameplay_cue()`
    - `GameplayAbility.execute_gameplay_cue_with_params()`
    - `GameplayAbility.get_ability_level()`
    - `GameplayAbility.get_ability_level_bp()`
    - `GameplayAbility.get_ability_system_component_from_actor_info()`
    - `GameplayAbility.get_actor_info()`
    - `GameplayAbility.get_avatar_actor_from_actor_info()`
    - `GameplayAbility.get_context_from_owner()`
    - `GameplayAbility.get_cooldown_time_remaining()`
    - `GameplayAbility.get_current_montage()`
    - `GameplayAbility.get_current_source_object()`
    - `GameplayAbility.get_granted_by_effect_context()`
    - `GameplayAbility.get_owning_actor_from_actor_info()`
    - `GameplayAbility.get_owning_component_from_actor_info()`
    - `GameplayAbility.get_source_object_bp()`
    - `GameplayAbility.invalidate_client_prediction_key()`
    - `GameplayAbility.is_locally_controlled()`
    - `GameplayAbility.k2_has_authority()`
    - `GameplayAbility.make_outgoing_gameplay_effect_spec()`
    - `GameplayAbility.make_target_location_info_from_owner_actor()`
    - `GameplayAbility.make_target_location_info_from_owner_skeletal_mesh_component()`
    - `GameplayAbility.mark_pending_kill_on_ability_end`
    - `GameplayAbility.montage_jump_to_section()`
    - `GameplayAbility.montage_set_next_section_name()`
    - `GameplayAbility.montage_stop()`
    - `GameplayAbility.on_end_ability()`
    - `GameplayAbility.remove_gameplay_cue()`
    - `GameplayAbility.remove_gameplay_effect_from_owner_with_asset_tags()`
    - `GameplayAbility.remove_gameplay_effect_from_owner_with_granted_tags()`
    - `GameplayAbility.remove_gameplay_effect_from_owner_with_handle()`
    - `GameplayAbility.remove_granted_by_effect()`
    - `GameplayAbility.send_gameplay_event()`
    - `GameplayAbility.set_can_be_canceled()`
    - `GameplayAbility.set_should_block_other_abilities()`
    - `GameplayAbility.should_ability_respond_to_event()`