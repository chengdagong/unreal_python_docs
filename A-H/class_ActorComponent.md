# unreal.ActorComponent

```python
class unreal.ActorComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


ActorComponent is the base class for components that define reusable behavior that can be added to different types of Actors.
ActorComponents that have a transform are known as SceneComponents and those that can be rendered are PrimitiveComponents.
see: \ActorComponent\
see: USceneComponent
see: UPrimitiveComponent

**C++ Source:**

- **Module**: Engine

- **File**: ActorComponent.h


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



---

**acquire_editor_element_handle**( _allow_create=True_) → `ScriptTypedElementHandle`

K2 Acquire Editor Component Element Handle

Parameters:

**allow\_create** ( _bool_)

Return type:

ScriptTypedElementHandle


---

**activate**( _reset=False_) → `None`

Activates the SceneComponent, should be overridden by native child classes.

Parameters:

**reset** ( _bool_) – Whether the activation should happen even if ShouldActivate returns false.


---

**add_asset_user_data_of_class**( _user_data_class_) → `bool`

Creates and adds an instance of the provided AssetUserData class to the target asset.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to create

Returns:

Whether or not an instance of InUserDataClass was succesfully added

Return type:

bool


---

**add_tick_prerequisite_actor**( _prerequisite_actor_) → `None`

Make this component tick after PrerequisiteActor

Parameters:

**prerequisite\_actor** ( _Actor_)


---

**add_tick_prerequisite_component**( _prerequisite_component_) → `None`

Make this component tick after PrerequisiteComponent.

Parameters:

**prerequisite\_component** ( _ActorComponent_)


---

_property_ `auto_activate`: bool

[Read-Only] Whether the component is activated at creation or must be explicitly activated.

**Type:**

( bool)


---

**component_has_tag**( _tag_) → `bool`

See if this component contains the supplied tag

Parameters:

**tag** ( _Name_)

Return type:

bool


---

_property_ `component_tags`: None

[Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

**Type:**

( Array\ [Name])


---

**deactivate**() → `None`

Deactivates the SceneComponent.


---

**destroy_component**( _object_) → `None`

Unregister and mark for pending kill a component. This may not be used to destroy a component that is owned by an actor unless the owning actor is calling the function.

Parameters:

**object** ( _Object_)


---

**get_asset_user_data_of_class**( _user_data_class_) → `AssetUserData`

Returns an instance of the provided AssetUserData class if it’s contained in the target asset.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to get

Returns:

The instance of the UAssetUserData class contained, or null if it doesn’t exist

Return type:

AssetUserData


---

**get_component_tick_interval**() → `float`

Returns the tick interval for this component’s primary tick function, which is the frequency in seconds at which it will be executed

Return type:

float


---

**get_owner**() → `Actor`

Follow the Outer chain to get the AActor that ‘Owns’ this component

Return type:

Actor


---

**has_asset_user_data_of_class**( _user_data_class_) → `bool`

Checks whether or not an instance of the provided AssetUserData class is contained.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to check for

Returns:

Whether or not an instance of InUserDataClass was found

Return type:

bool


---

**is_active**() → `bool`

Returns whether the component is active or not

Returns:

The active state of the component.

Return type:

bool


---

**is_being_destroyed**() → `bool`

Returns whether the component is in the process of being destroyed.

Return type:

bool


---

**is_component_tick_enabled**() → `bool`

Returns whether this component has tick enabled or not

Return type:

bool


---

_property_ `is_editor_only`: bool

[Read-Only] If true, the component will be excluded from non-editor builds

**Type:**

( bool)


---

_property_ `on_component_activated`: ActorComponentActivatedSignature

[Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

**Type:**

( ActorComponentActivatedSignature)


---

_property_ `on_component_deactivated`: ActorComponentDeactivateSignature

[Read-Write] Called when the component has been deactivated

**Type:**

( ActorComponentDeactivateSignature)


---

**receive_async_physics_tick**( _delta_seconds_, _sim_seconds_) → `None`

Event called every async physics tick if bAsyncPhysicsTickEnabled is true

Parameters:

- **delta\_seconds** ( _float_)

- **sim\_seconds** ( _float_)



---

**receive_begin_play**() → `None`

Blueprint implementable event for when the component is beginning play, called before its owning actor’s BeginPlay
or when the component is dynamically created if the Actor has already BegunPlay.


---

**receive_end_play**( _end_play_reason_) → `None`

Blueprint implementable event for when the component ends play, generally via destruction or its Actor’s EndPlay.

Parameters:

**end\_play\_reason** ( _EndPlayReason_)


---

**receive_initialize_component**() → `None`

deprecated: ‘receive\_initialize\_component’ was renamed to ‘receive\_begin\_play’.


---

**receive_tick**( _delta_seconds_) → `None`

Event called every frame if tick is enabled

Parameters:

**delta\_seconds** ( _float_)


---

**receive_uninitialize_component**( _end_play_reason:EndPlayReason_) → `None`

deprecated: ‘receive\_uninitialize\_component’ was renamed to ‘receive\_end\_play’.


---

**remove_tick_prerequisite_actor**( _prerequisite_actor_) → `None`

Remove tick dependency on PrerequisiteActor.

Parameters:

**prerequisite\_actor** ( _Actor_)


---

**remove_tick_prerequisite_component**( _prerequisite_component_) → `None`

Remove tick dependency on PrerequisiteComponent.

Parameters:

**prerequisite\_component** ( _ActorComponent_)


---

_property_ `replicate_using_registered_sub_object_list`: bool

[Read-Only] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

**Type:**

( bool)


---

_property_ `replicates`: bool

[Read-Only] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

**Type:**

( bool)


---

**set_active**( _new_active_, _reset=False_) → `None`

Sets whether the component is active or not

Parameters:

- **new\_active** ( _bool_) – The new active state of the component

- **reset** ( _bool_) – Whether the activation should happen even if ShouldActivate returns false.



---

**set_auto_activate**( _new_auto_activate_) → `None`

Sets whether the component should be auto activate or not. Only safe during construction scripts.

Parameters:

**new\_auto\_activate** ( _bool_) – The new auto activate state of the component


---

**set_component_tick_enabled**( _enabled_) → `None`

Set this component’s tick functions to be enabled or disabled. Only has an effect if the function is registered

Parameters:

**enabled** ( _bool_) – Whether it should be enabled or not


---

**set_component_tick_interval**( _tick_interval_) → `None`

Sets the tick interval for this component’s primary tick function. Does not enable the tick interval. Takes effect on next tick.

Parameters:

**tick\_interval** ( _float_) – The duration between ticks for this component’s primary tick function


---

**set_component_tick_interval_and_cooldown**( _tick_interval_) → `None`

Sets the tick interval for this component’s primary tick function. Does not enable the tick interval. Takes effect imediately.

Parameters:

**tick\_interval** ( _float_) – The duration between ticks for this component’s primary tick function


---

**set_is_replicated**( _should_replicate_) → `None`

Enable or disable replication. This is the equivalent of RemoteRole for actors (only a bool is required for components)

Parameters:

**should\_replicate** ( _bool_)


---

**set_tick_group**( _new_tick_group_) → `None`

Changes the ticking group for this component

Parameters:

**new\_tick\_group** ( _TickingGroup_)


---

**set_tickable_when_paused**( _tickable_when_paused_) → `None`

Sets whether this component can tick when paused.

Parameters:

**tickable\_when\_paused** ( _bool_)


---

**toggle_active**() → `None`

Toggles the active state of the component

### Table of Contents

- `unreal.ActorComponent`
  - `ActorComponent`
    - `ActorComponent.acquire_editor_element_handle()`
    - `ActorComponent.activate()`
    - `ActorComponent.add_asset_user_data_of_class()`
    - `ActorComponent.add_tick_prerequisite_actor()`
    - `ActorComponent.add_tick_prerequisite_component()`
    - `ActorComponent.auto_activate`
    - `ActorComponent.component_has_tag()`
    - `ActorComponent.component_tags`
    - `ActorComponent.deactivate()`
    - `ActorComponent.destroy_component()`
    - `ActorComponent.get_asset_user_data_of_class()`
    - `ActorComponent.get_component_tick_interval()`
    - `ActorComponent.get_owner()`
    - `ActorComponent.has_asset_user_data_of_class()`
    - `ActorComponent.is_active()`
    - `ActorComponent.is_being_destroyed()`
    - `ActorComponent.is_component_tick_enabled()`
    - `ActorComponent.is_editor_only`
    - `ActorComponent.on_component_activated`
    - `ActorComponent.on_component_deactivated`
    - `ActorComponent.receive_async_physics_tick()`
    - `ActorComponent.receive_begin_play()`
    - `ActorComponent.receive_end_play()`
    - `ActorComponent.receive_initialize_component()`
    - `ActorComponent.receive_tick()`
    - `ActorComponent.receive_uninitialize_component()`
    - `ActorComponent.remove_tick_prerequisite_actor()`
    - `ActorComponent.remove_tick_prerequisite_component()`
    - `ActorComponent.replicate_using_registered_sub_object_list`
    - `ActorComponent.replicates`
    - `ActorComponent.set_active()`
    - `ActorComponent.set_auto_activate()`
    - `ActorComponent.set_component_tick_enabled()`
    - `ActorComponent.set_component_tick_interval()`
    - `ActorComponent.set_component_tick_interval_and_cooldown()`
    - `ActorComponent.set_is_replicated()`
    - `ActorComponent.set_tick_group()`
    - `ActorComponent.set_tickable_when_paused()`
    - `ActorComponent.toggle_active()`