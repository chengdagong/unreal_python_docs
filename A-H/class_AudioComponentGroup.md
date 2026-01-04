# unreal.AudioComponentGroup

```python
class unreal.AudioComponentGroup(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SceneComponent``


- Automatic Handler for voices and parameters across any number of AudioComponents


**C++ Source:**

- **Plugin**: AudioGameplay

- **Module**: AudioGameplay

- **File**: AudioComponentGroup.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `components` (Array[AudioComponent]): [Read-Only]

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `hidden_in_game` (bool): [Read-Write] Whether to hide the primitive in game, if the primitive is Visible.

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `on_killed` (SoundGroupChanged): [Read-Write]

- `on_stopped` (SoundGroupChanged): [Read-Write]

- `on_unvirtualized` (SoundGroupChanged): [Read-Write]

- `on_virtualized` (SoundGroupChanged): [Read-Write]

- `persistent_params` (Array[AudioParameter]): [Read-Only]

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `relative_location` (Vector): [Read-Write] Location of the component relative to its parent

- `relative_rotation` (Rotator): [Read-Write] Rotation of the component relative to its parent

- `relative_scale3d` (Vector): [Read-Write] Non-uniform scaling of the component relative to its parent.
Note that scaling is always applied in local space (no shearing etc)

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `use_attach_parent_bound` (bool): [Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

- `visible` (bool): [Read-Write] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.



---

**add_extension**( _new_extension_) → `None`

Add Extension

Parameters:

**new\_extension** ( _AudioComponentGroupExtension_)


---

**add_external_component**( _component_to_add_) → `None`

Allow an externally created AudioComponent to share parameters with this SoundGroup

Parameters:

**component\_to\_add** ( _AudioComponent_)


---

**broadcast_event**( _event_name_) → `None`

Broadcast Event

Parameters:

**event\_name** ( _Name_)


---

**broadcast_kill**() → `None`

Broadcast Kill


---

**broadcast_stop_all**() → `None`

Broadcast Stop All


---

**disable_virtualization**() → `None`

Disable Virtualization


---

**enable_virtualization**() → `None`

Enable Virtualization


---

**get_bool_param_value**( _param_name_) → `bool`

Get Bool Param Value

Parameters:

**param\_name** ( _Name_)

Return type:

bool


---

**get_float_param_value**( _param_name_) → `float`

Get Float Param Value

Parameters:

**param\_name** ( _Name_)

Return type:

float


---

**get_string_param_value**( _param_name_) → `str`

Get String Param Value

Parameters:

**param\_name** ( _Name_)

Return type:

str


---

**is_playing_any**() → `bool`

Is Playing Any

Return type:

bool


---

**is_virtualized**() → `bool`

Is Virtualized

Return type:

bool


---

_property_ `on_killed`: SoundGroupChanged

[Read-Write]

**Type:**

( SoundGroupChanged)


---

_property_ `on_stopped`: SoundGroupChanged

[Read-Write]

**Type:**

( SoundGroupChanged)


---

_property_ `on_unvirtualized`: SoundGroupChanged

[Read-Write]

**Type:**

( SoundGroupChanged)


---

_property_ `on_virtualized`: SoundGroupChanged

[Read-Write]

**Type:**

( SoundGroupChanged)


---

_property_ `persistent_params`: None

[Read-Only]

**Type:**

( Array\ [AudioParameter])


---

**remove_extension**( _new_extension_) → `None`

Remove Extension

Parameters:

**new\_extension** ( _AudioComponentGroupExtension_)


---

**remove_external_component**( _component_to_remove_) → `None`

Remove External Component

Parameters:

**component\_to\_remove** ( _AudioComponent_)


---

**reset_parameters**() → `None`

Resets all parameters to their original values.


---

**set_bool_array_parameter**( _name_, _value_) → `None`

Sets a named Boolean Array

Parameters:

- **name** ( _Name_)

- **value** ( _Array_ _\_ [_bool_ _]_)



---

**set_bool_parameter**( _name_, _bool_) → `None`

Sets a named Boolean

Parameters:

- **name** ( _Name_)

- **bool** ( _bool_)



---

**set_float_array_parameter**( _name_, _value_) → `None`

Sets a named Float Array

Parameters:

- **name** ( _Name_)

- **value** ( _Array_ _\_ [_float_ _]_)



---

**set_float_parameter**( _name_, _float_) → `None`

Sets a named Float

Parameters:

- **name** ( _Name_)

- **float** ( _float_)



---

**set_int_array_parameter**( _name_, _value_) → `None`

Sets a named Int32 Array

Parameters:

- **name** ( _Name_)

- **value** ( _Array_ _[_ _int32_ _]_)



---

**set_int_parameter**( _name_, _int_) → `None`

Sets a named Int32

Parameters:

- **name** ( _Name_)

- **int** ( _int32_)



---

**set_low_pass_filter**( _frequency_) → `None`

Set Low Pass Filter

Parameters:

**frequency** ( _float_)


---

**set_object_array_parameter**( _name_, _value_) → `None`

Sets a named UObject Array

Parameters:

- **name** ( _Name_)

- **value** ( _Array_ _\_ [_Object_ _]_)



---

**set_object_parameter**( _name_, _value_) → `None`

Sets a named UObject

Parameters:

- **name** ( _Name_)

- **value** ( _Object_)



---

**set_parameters_blueprint**( _parameters_) → `None`

Sets an array of parameters as a batch

Parameters:

**parameters** ( _Array_ _\_ [_AudioParameter_ _]_)


---

**set_pitch_multiplier**( _pitch_) → `None`

Set Pitch Multiplier

Parameters:

**pitch** ( _float_)


---

**set_string_array_parameter**( _name_, _value_) → `None`

Sets a named String Array

Parameters:

- **name** ( _Name_)

- **value** ( _Array_ _\_ [_str_ _]_)



---

**set_string_parameter**( _name_, _value_) → `None`

Sets a named String

Parameters:

- **name** ( _Name_)

- **value** ( _str_)



---

**set_trigger_parameter**( _name_) → `None`

Executes a named trigger. Does _not_ cache trigger value, so only executes if the sound
is already playing. If the intent is for the trigger to execute immediately (if playing)
and be called on initialization for all future instances, call ‘SetBoolParameter’ with the
intended initial trigger behavior (true if trigger desired on initialization, false if not).

Parameters:

**name** ( _Name_)


---

**set_volume_multiplier**( _volume_) → `None`

Set Volume Multiplier

Parameters:

**volume** ( _float_)


---

_classmethod_ static_get_or_create_component_group( _actor_)→AudioComponentGroup

Static Get or Create Component Group

Parameters:

**actor** ( _Actor_)

Return type:

AudioComponentGroup


---

**stop_sound**( _sound_, _fade_time=0.000000_) → `None`

Stop all instances of this Sound on any internal or external components

Parameters:

- **sound** ( _SoundBase_)

- **fade\_time** ( _float_)



---

**subscribe_to_bool**( _param_name_, _delegate_) → `None`

Subscribe to Bool

Parameters:

- **param\_name** ( _Name_)

- **delegate** ( _BoolParamCallback_)



---

**subscribe_to_event**( _event_name_, _delegate_) → `None`

Subscribe to Event

Parameters:

- **event\_name** ( _Name_)

- **delegate** ( _SoundCallback_)



---

**subscribe_to_string_param**( _param_name_, _delegate_) → `None`

Subscribe to String Param

Parameters:

- **param\_name** ( _Name_)

- **delegate** ( _StringParamCallback_)



---

**unsubscribe_object**( _object_) → `None`

remove any string, event, and bool subscriptions that are bound to this object

Parameters:

**object** ( _Object_)

### Table of Contents

- `unreal.AudioComponentGroup`
  - `AudioComponentGroup`
    - `AudioComponentGroup.add_extension()`
    - `AudioComponentGroup.add_external_component()`
    - `AudioComponentGroup.broadcast_event()`
    - `AudioComponentGroup.broadcast_kill()`
    - `AudioComponentGroup.broadcast_stop_all()`
    - `AudioComponentGroup.disable_virtualization()`
    - `AudioComponentGroup.enable_virtualization()`
    - `AudioComponentGroup.get_bool_param_value()`
    - `AudioComponentGroup.get_float_param_value()`
    - `AudioComponentGroup.get_string_param_value()`
    - `AudioComponentGroup.is_playing_any()`
    - `AudioComponentGroup.is_virtualized()`
    - `AudioComponentGroup.on_killed`
    - `AudioComponentGroup.on_stopped`
    - `AudioComponentGroup.on_unvirtualized`
    - `AudioComponentGroup.on_virtualized`
    - `AudioComponentGroup.persistent_params`
    - `AudioComponentGroup.remove_extension()`
    - `AudioComponentGroup.remove_external_component()`
    - `AudioComponentGroup.reset_parameters()`
    - `AudioComponentGroup.set_bool_array_parameter()`
    - `AudioComponentGroup.set_bool_parameter()`
    - `AudioComponentGroup.set_float_array_parameter()`
    - `AudioComponentGroup.set_float_parameter()`
    - `AudioComponentGroup.set_int_array_parameter()`
    - `AudioComponentGroup.set_int_parameter()`
    - `AudioComponentGroup.set_low_pass_filter()`
    - `AudioComponentGroup.set_object_array_parameter()`
    - `AudioComponentGroup.set_object_parameter()`
    - `AudioComponentGroup.set_parameters_blueprint()`
    - `AudioComponentGroup.set_pitch_multiplier()`
    - `AudioComponentGroup.set_string_array_parameter()`
    - `AudioComponentGroup.set_string_parameter()`
    - `AudioComponentGroup.set_trigger_parameter()`
    - `AudioComponentGroup.set_volume_multiplier()`
    - `AudioComponentGroup.static_get_or_create_component_group()`
    - `AudioComponentGroup.stop_sound()`
    - `AudioComponentGroup.subscribe_to_bool()`
    - `AudioComponentGroup.subscribe_to_event()`
    - `AudioComponentGroup.subscribe_to_string_param()`
    - `AudioComponentGroup.unsubscribe_object()`