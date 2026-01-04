# unreal.VOIPTalker

```python
class unreal.VOIPTalker(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``ActorComponent``


**C++ Source:**

- **Module**: Engine

- **File**: VoiceConfig.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `settings` (VoiceSettings): [Read-Write] Configurable settings for this player’s voice. When set, this will update the next time the player speaks.



---

**bp_on_talking_begin**( _audio_component_) → `None`

Blueprint native event for when this player starts speaking.

Parameters:

**audio\_component** ( _AudioComponent_)


---

**bp_on_talking_end**() → `None`

Blueprint native event for when this player stops speaking.


---

_classmethod_ create_talker_for_player( _owning_state_)→VOIPTalker

function for creating and registering a UVOIPTalker.

Parameters:

**owning\_state** ( _PlayerState_)

Return type:

VOIPTalker


---

**get_voice_level**() → `float`

Get the current level of how loud this player is speaking. Will return 0.0
if player is not talking.

Return type:

float


---

**register_with_player_state**( _owning_state_) → `None`

This function sets up this talker with a specific player.
It is necessary to use this to properly control a specific player’s voice
and receive events.

Parameters:

**owning\_state** ( _PlayerState_)


---

_property_ `settings`: VoiceSettings

[Read-Write] Configurable settings for this player’s voice. When set, this will update the next time the player speaks.

**Type:**

( VoiceSettings)

### Table of Contents

- `unreal.VOIPTalker`
  - `VOIPTalker`
    - `VOIPTalker.bp_on_talking_begin()`
    - `VOIPTalker.bp_on_talking_end()`
    - `VOIPTalker.create_talker_for_player()`
    - `VOIPTalker.get_voice_level()`
    - `VOIPTalker.register_with_player_state()`
    - `VOIPTalker.settings`