# unreal.GameplayAbility_Interact

```python
class unreal.GameplayAbility_Interact(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``GameplayAbility``


Gameplay ability for interacting with a target(s).

This ability will trigger interactions on its current list of available targets
which are populated via the UpdateInteractions functions.

When UpdateInteractions is called, it provides a nice place to update
some UI or other things you may want to do to display to your player
that interactions are now available.

**C++ Source:**

- **Plugin**: InteractionInterface

- **Module**: InteractableInterface

- **File**: InteractionTask\_WaitForTargets.h


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

- `current_available_targets` (Array[InteractionTarget]): [Read-Write] Array of available interaction targets to interact with. This is populated by “UpdateInteractions”
and normally after an ability task to gather the available targets has completed.

- `current_event_data` (GameplayEventData): [Read-Write] Information specific to this instance of the ability, if it was activated by an event

- `instancing_policy` (GameplayAbilityInstancingPolicy): [Read-Write] How the ability is instanced when executed. This limits what an ability can do in its implementation.

- `interaction_scan_range` (float): [Read-Write] The range to scan for available targets. A sphere of this radius will be cast around this ability’s
owning actor to check for nearby interactions.

- `interaction_scan_rate` (float): [Read-Write] How often to scan for targets. A world OverlapMultiByChannel call will happen
at this rate to check for available interactions around us.

- `interaction_trace_channel` (CollisionChannel): [Read-Write] The collision channel to use when checking for interaction targets within the given area

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

_property_ `current_available_targets`: None

[Read-Only] Array of available interaction targets to interact with. This is populated by “UpdateInteractions”
and normally after an ability task to gather the available targets has completed.

**Type:**

( Array\ [InteractionTarget])


---

**on_available_interactions_updated**() → `None`

Called when this ability’s available interaction targets have been updated.

This is a good place to update some UI or display some message to the user
that they can now interact with the current targets.


---

**on_trigger_interaction**() → `None`

Triggers the interaction with one or more of the currently available targets.
Override this in blueprints or native C++ to decide which of the currently available targets
you would like to interact with and how.


---

**trigger_interaction**() → `None`

Attempts to begin the interaction with the current targets.


---

**update_interactions**( _available_targets_) → `None`

Update the available interactions that this ability can trigger.
This is normally populated via an async task running in the ability blueprint
to gather nearby targets.

Parameters:

**available\_targets** ( _Array_ _\_ [_InteractionTarget_ _]_)

### Table of Contents

- `unreal.GameplayAbility_Interact`
  - `GameplayAbility_Interact`
    - `GameplayAbility_Interact.current_available_targets`
    - `GameplayAbility_Interact.on_available_interactions_updated()`
    - `GameplayAbility_Interact.on_trigger_interaction()`
    - `GameplayAbility_Interact.trigger_interaction()`
    - `GameplayAbility_Interact.update_interactions()`