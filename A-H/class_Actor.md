# unreal.Actor

```python
class unreal.Actor(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Actor is the base class for an Object that can be placed or spawned in a level.
Actors may contain a collection of ActorComponents, which can be used to control how actors move, how they are rendered, etc.
The other main function of an Actor is the replication of properties and function calls across the network during play.

Actor initialization has multiple steps, here’s the order of important virtual functions that get called:
\- UObject::PostLoad: For actors statically placed in a level, the normal UObject PostLoad gets called both in the editor and during gameplay.

> This is not called for newly spawned actors.

- UActorComponent::OnComponentCreated: When an actor is spawned in the editor or during gameplay, this gets called for any native components.

For blueprint-created components, this gets called during construction for that component.
This is not called for components loaded from a level.

- AActor::PreRegisterAllComponents: For statically placed actors and spawned actors that have native root components, this gets called now.

For blueprint actors without a native root component, these registration functions get called later during construction.

- UActorComponent::RegisterComponent: All components are registered in editor and at runtime, this creates their physical/visual representation.

These calls may be distributed over multiple frames, but are always after PreRegisterAllComponents.
This may also get called later on after an UnregisterComponent call removes it from the world.

- AActor::PostRegisterAllComponents: Called for all actors both in the editor and in gameplay, this is the last function that is called in all cases.

- AActor::PostActorCreated: When an actor is created in the editor or during gameplay, this gets called right before construction.

This is not called for components loaded from a level.

- AActor::UserConstructionScript: Called for blueprints that implement a construction script.

- AActor::OnConstruction: Called at the end of ExecuteConstruction, which calls the blueprint construction script.

This is called after all blueprint-created components are fully created and registered.
This is only called during gameplay for spawned actors, and may get rerun in the editor when changing blueprints.

- AActor::PreInitializeComponents: Called before InitializeComponent is called on the actor’s components.

This is only called during gameplay and in certain editor preview windows.

- UActorComponent::Activate: This will be called only if the component has bAutoActivate set.

It will also got called later on if a component is manually activated.

- UActorComponent::InitializeComponent: This will be called only if the component has bWantsInitializeComponentSet.

This only happens once per gameplay session.

- AActor::PostInitializeComponents: Called after the actor’s components have been initialized, only during gameplay and some editor previews.

- AActor::BeginPlay: Called when the level starts ticking, only during actual gameplay.

This normally happens right after PostInitializeComponents but can be delayed for networked or child actors.


see: https://docs.unrealengine.com/Programming/UnrealArchitecture/Actors
see: https://docs.unrealengine.com/Programming/UnrealArchitecture/Actors/ActorLifecycle
see: UActorComponent

**C++ Source:**

- **Module**: Engine

- **File**: Actor.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `actor_guid` (Guid): [Read-Write] The GUID for this actor; this guid will be the same for actors from instanced streaming levels.
see: ActorInstanceGuid, FActorInstanceGuidMapper
note: Don’t use VisibleAnywhere here to avoid getting the CPF\_Edit flag and get this property reset when resetting to defaults. See FActorDetails::AddActorCategory and EditorUtilities::CopySingleProperty for details.

- `actor_instance_guid` (Guid): [Read-Write] The instance GUID for this actor; this guid will be unique for actors from instanced streaming levels.
see: ActorGuid
note: This is not guaranteed to be valid during PostLoad, but safe to access from RegisterAllComponents.

- `allow_tick_before_begin_play` (bool): [Read-Write] Whether we allow this Actor to tick before it receives the BeginPlay event.
Normally we don’t tick actors until after BeginPlay; this setting allows this behavior to be overridden.
This Actor must be able to tick for this setting to be relevant.

- `always_relevant` (bool): [Read-Write] Always relevant for network (overrides bOnlyRelevantToOwner).

- `async_physics_tick_enabled` (bool): [Read-Write] Whether to use use the async physics tick with this actor.

- `auto_destroy_when_finished` (bool): [Read-Write] If true then destroy self when “finished”, meaning all relevant components report that they are done and no timelines or timers are in flight.

- `auto_receive_input` (AutoReceiveInput): [Read-Write] Automatically registers this actor to receive input from a player.

- `block_input` (bool): [Read-Write] If true, all input on the stack below this actor will not be considered

- `call_pre_replication` (bool): [Read-Write]

- `call_pre_replication_for_replay` (bool): [Read-Write]

- `can_be_damaged` (bool): [Read-Write] Whether this actor can take damage. Must be true for damage events (e.g. ReceiveDamage()) to be called.
see: https://www.unrealengine.com/blog/damage-in-ue4
see: TakeDamage(), ReceiveDamage()

- `can_be_in_cluster` (bool): [Read-Write] If true, this actor can be put inside of a GC Cluster to improve Garbage Collection performance

- `content_bundle_guid` (Guid): [Read-Write] The GUID for this actor’s content bundle.

- `custom_time_dilation` (float): [Read-Write] Allow each actor to run at a different time speed. The DeltaTime for a frame is multiplied by the global TimeDilation (in WorldSettings) and this CustomTimeDilation for this actor’s tick.

- `data_layer_assets` (Array[DataLayerAsset]): [Read-Write] DataLayers assets the actor belongs to.

- `data_layers` (Array[ActorDataLayer]): [Read-Only] DataLayers the actor belongs to.

- `default_update_overlaps_method_during_level_streaming` (ActorUpdateOverlapsMethod): [Read-Only] Default value taken from config file for this class when ‘UseConfigDefault’ is chosen for
‘UpdateOverlapsMethodDuringLevelStreaming’. This allows a default to be chosen per class in the matching config.
For example, for Actor it could be specified in DefaultEngine.ini as:

[/Script/Engine.Actor]
DefaultUpdateOverlapsMethodDuringLevelStreaming = OnlyUpdateMovable

Another subclass could set their default to something different, such as:

[/Script/Engine.BlockingVolume]
DefaultUpdateOverlapsMethodDuringLevelStreaming = NeverUpdate
see: UpdateOverlapsMethodDuringLevelStreaming

- `enable_auto_lod_generation` (bool): [Read-Write] Whether this actor should be considered or not during HLOD generation.

- `external_data_layer_asset` (ExternalDataLayerAsset): [Read-Only]

- `find_camera_component_when_view_target` (bool): [Read-Write] If true, this actor should search for an owned camera component to view through when used as a view target.

- `generate_overlap_events_during_level_streaming` (bool): [Read-Write] If true, this actor will generate overlap Begin/End events when spawned as part of level streaming, which includes initial level load.
You might enable this is in the case where a streaming level loads around an actor and you want Begin/End overlap events to trigger.
see: UpdateOverlapsMethodDuringLevelStreaming

- `hidden` (bool): [Read-Write] Allows us to only see this Actor in the Editor, and not in the actual game.
see: SetActorHiddenInGame()

- `hlod_layer` (HLODLayer): [Read-Write] The UHLODLayer in which this actor should be included.

- `ignores_origin_shifting` (bool): [Read-Write] Whether this actor should not be affected by world origin shifting.

- `initial_life_span` (float): [Read-Write] How long this Actor lives before dying, 0=forever. Note this is the INITIAL value and should not be modified once play has begun.

- `input_priority` (int32): [Read-Write] The priority of this input component when pushed in to the stack.

- `instigator` (Pawn): [Read-Write] Pawn responsible for damage and other gameplay events caused by this actor.

- `is_editor_only_actor` (bool): [Read-Write] Whether this actor is editor-only. Use with care, as if this actor is referenced by anything else that reference will be NULL in cooked builds

- `is_main_world_only` (bool): [Read-Write] If checked, this Actor will only get loaded in a main world (persistent level), it will not be loaded through Level Instances.

- `is_spatially_loaded` (bool): [Read-Write] Determine if this actor is spatially loaded when placed in a partitioned world.

If true, this actor will be loaded when in the range of any streaming sources and if (1) in no data layers, or (2) one or more of its data layers are enabled.
If false, this actor will be loaded if (1) in no data layers, or (2) one or more of its data layers are enabled.

- `layers` (Array[Name]): [Read-Write] Layers the actor belongs to. This is outside of the editoronly data to allow hiding of LD-specified layers at runtime for profiling.

- `migrating_asset` (bool): [Read-Write] If true, this actor can be migrated to another server even if it’s been loaded from disk

- `min_net_update_frequency` (float): [Read-Write]

- `net_cull_distance_squared` (float): [Read-Write]

- `net_dormancy` (NetDormancy): [Read-Write] Dormancy setting for actor to take itself off of the replication list without being destroyed on clients.

- `net_load_on_client` (bool): [Read-Write] This actor will be loaded on network clients during map load

- `net_priority` (float): [Read-Write] Priority for this actor when checking for replication in a low bandwidth or saturated situation, higher priority means it is more likely to replicate

- `net_update_frequency` (float): [Read-Write]

- `net_use_owner_relevancy` (bool): [Read-Write] If actor has valid Owner, call Owner’s IsNetRelevantFor and GetNetPriority

- `on_actor_begin_overlap` (ActorBeginOverlapSignature): [Read-Write] Called when another actor begins to overlap this actor, for example a player walking into a trigger.
For events when objects have a blocking collision, for example a player hitting a wall, see ‘Hit’ events.
note: Components on both this and the other Actor must have bGenerateOverlapEvents set to true to generate overlap events.

- `on_actor_end_overlap` (ActorEndOverlapSignature): [Read-Write] Called when another actor stops overlapping this actor.
note: Components on both this and the other Actor must have bGenerateOverlapEvents set to true to generate overlap events.

- `on_actor_hit` (ActorHitSignature): [Read-Write] Called when this Actor hits (or is hit by) something solid. This could happen due to things like Character movement, using Set Location with ‘sweep’ enabled, or physics simulation.
For events when objects overlap (e.g. walking into a trigger) see the ‘Overlap’ event.
note: For collisions during physics simulation to generate hit events, ‘Simulation Generates Hit Events’ must be enabled.

- `on_begin_cursor_over` (ActorBeginCursorOverSignature): [Read-Write] Called when the mouse cursor is moved over this actor if mouse over events are enabled in the player controller.

- `on_clicked` (ActorOnClickedSignature): [Read-Write] Called when the left mouse button is clicked while the mouse is over this actor and click events are enabled in the player controller.

- `on_destroyed` (ActorDestroyedSignature): [Read-Write] Event triggered when the actor has been explicitly destroyed.

- `on_end_cursor_over` (ActorEndCursorOverSignature): [Read-Write] Called when the mouse cursor is moved off this actor if mouse over events are enabled in the player controller.

- `on_end_play` (ActorEndPlaySignature): [Read-Write] Event triggered when the actor is being deleted or removed from a level.

- `on_input_touch_begin` (ActorOnInputTouchBeginSignature): [Read-Write] Called when a touch input is received over this actor when touch events are enabled in the player controller.

- `on_input_touch_end` (ActorOnInputTouchEndSignature): [Read-Write] Called when a touch input is received over this component when touch events are enabled in the player controller.

- `on_input_touch_enter` (ActorBeginTouchOverSignature): [Read-Write] Called when a finger is moved over this actor when touch over events are enabled in the player controller.

- `on_input_touch_leave` (ActorEndTouchOverSignature): [Read-Write] Called when a finger is moved off this actor when touch over events are enabled in the player controller.

- `on_released` (ActorOnReleasedSignature): [Read-Write] Called when the left mouse button is released while the mouse is over this actor and click events are enabled in the player controller.

- `on_take_any_damage` (TakeAnyDamageSignature): [Read-Write] Called when the actor is damaged in any way.

- `on_take_point_damage` (TakePointDamageSignature): [Read-Write] Called when the actor is damaged by point damage.

- `on_take_radial_damage` (TakeRadialDamageSignature): [Read-Write] Called when the actor is damaged by radial damage.

- `only_relevant_to_owner` (bool): [Read-Write] If true, this actor is only relevant to its owner. If this flag is changed during play, all non-owner channels would need to be explicitly closed.

- `optimize_bp_component_data` (bool): [Read-Write] Whether to cook additional data to speed up spawn events at runtime for any Blueprint classes based on this Actor. This option may slightly increase memory usage in a cooked build.

- `physics_replication_mode` (PhysicsReplicationMode): [Read-Write] Which mode to replicate physics through for this actor. Only relevant if the actor replicates movement and has a component that simulate physics.

- `pivot_offset` (Vector): [Read-Write] Local space pivot offset for the actor, only used in the editor

- `primary_actor_tick` (ActorTickFunction): [Read-Write] Primary Actor tick function, which calls TickActor().
Tick functions can be configured to control whether ticking is enabled, at what time during a frame the update occurs, and to set up tick dependencies.
see: https://docs.unrealengine.com/API/Runtime/Engine/Engine/FTickFunction
see: AddTickPrerequisiteActor(), AddTickPrerequisiteComponent()

- `relevant_for_level_bounds` (bool): [Read-Write] If true, this actor’s component’s bounds will be included in the level’s
bounding box unless the Actor’s class has overridden IsLevelBoundsRelevant

- `remote_role` (NetRole): [Read-Only] Describes how much control the remote machine has over the actor.

- `replay_rewindable` (bool): [Read-Write] If true, this actor will only be destroyed during scrubbing if the replay is set to a time before the actor existed.
Otherwise, RewindForReplay will be called if we detect the actor needs to be reset.
Note, this Actor must not be destroyed by gamecode, and RollbackViaDeletion may not be used.

- `replicate_movement` (bool): [Read-Write] If true, replicate movement/location related properties.
Actor must also be set to replicate.
see: SetReplicates()
see: https://docs.unrealengine.com/InteractiveExperiences/Networking/Actors

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects and the replicated actor components list
When false the replication system will instead call the virtual ReplicateSubobjects() function where the subobjects and actor components need to be manually replicated.

- `replicated_movement` (RepMovement): [Read-Write] Used for replication of our RootComponent’s position and velocity

- `replicates` (bool): [Read-Write] If true, this actor will replicate to remote machines
see: SetReplicates()

- `role` (NetRole): [Read-Only] Describes how much control the local machine has over the actor.

- `root_component` (SceneComponent): [Read-Write] The component that defines the transform (location, rotation, scale) of this Actor in the world, all other components must be attached to this one somehow

- `runtime_grid` (Name): [Read-Write] Determine in which partition grid this actor will be placed in the partition (if the world is partitioned).
If None, the decision will be left to the partition.

- `spawn_collision_handling_method` (SpawnActorCollisionHandlingMethod): [Read-Write] Controls how to handle spawning this actor in a situation where it’s colliding with something else. “Default” means AlwaysSpawn here.

- `sprite_scale` (float): [Read-Write] The scale to apply to any billboard components in editor builds (happens in any WITH\_EDITOR build, including non-cooked games).

- `tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing.

- `update_overlaps_method_during_level_streaming` (ActorUpdateOverlapsMethod): [Read-Write] Condition for calling UpdateOverlaps() to initialize overlap state when loaded in during level streaming.
If set to ‘UseConfigDefault’, the default specified in ini (displayed in ‘DefaultUpdateOverlapsMethodDuringLevelStreaming’) will be used.
If overlaps are not initialized, this actor and attached components will not have an initial state of what objects are touching it,
and overlap events may only come in once one of those objects update overlaps themselves (for example when moving).
However if an object touching it _does_ initialize state, both objects will know about their touching state with each other.
This can be a potentially large performance savings during level loading and streaming, and is safe if the object and others initially
overlapping it do not need the overlap state because they will not trigger overlap notifications.

Note that if ‘bGenerateOverlapEventsDuringLevelStreaming’ is true, overlaps are always updated in this case, but that flag
determines whether the Begin/End overlap events are triggered.
see: bGenerateOverlapEventsDuringLevelStreaming, DefaultUpdateOverlapsMethodDuringLevelStreaming, GetUpdateOverlapsMethodDuringLevelStreaming()



---

**acquire_editor_element_handle**( _allow_create=True_) → `ScriptTypedElementHandle`

K2 Acquire Editor Actor Element Handle

Parameters:

**allow\_create** ( _bool_)

Return type:

ScriptTypedElementHandle


---

_property_ `actor_guid`: Guid

[Read-Only] The GUID for this actor; this guid will be the same for actors from instanced streaming levels.
see: ActorInstanceGuid, FActorInstanceGuidMapper
note: Don’t use VisibleAnywhere here to avoid getting the CPF\_Edit flag and get this property reset when resetting to defaults. See FActorDetails::AddActorCategory and EditorUtilities::CopySingleProperty for details.

**Type:**

( Guid)


---

**actor_has_tag**( _tag_) → `bool`

See if this actor’s Tags array contains the supplied name tag

Parameters:

**tag** ( _Name_)

Return type:

bool


---

_property_ `actor_instance_guid`: Guid

[Read-Only] The instance GUID for this actor; this guid will be unique for actors from instanced streaming levels.
see: ActorGuid
note: This is not guaranteed to be valid during PostLoad, but safe to access from RegisterAllComponents.

**Type:**

( Guid)


---

**add_actor_local_offset**( _delta_location_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the location of this component in its local reference frame.

Parameters:

- **delta\_location** ( _Vector_)

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the location without teleporting will not update the location of simulated child/attached components.


Returns:

sweep\_hit\_result (HitResult):

Return type:

HitResult


---

**add_actor_local_rotation**( _delta_rotation_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the rotation of this component in its local reference frame

Parameters:

- **delta\_rotation** ( _Rotator_) – The change in rotation in local space.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the rotation without teleporting will not update the rotation of simulated child/attached components.


Returns:

sweep\_hit\_result (HitResult):

Return type:

HitResult


---

**add_actor_local_transform**( _new_transform_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the transform of this component in its local reference frame

Parameters:

- **new\_transform** ( _Transform_) – The change in transform in local space.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the transform without teleporting will not update the transform of simulated child/attached components.


Returns:

sweep\_hit\_result (HitResult):

Return type:

HitResult


---

**add_actor_world_offset**( _delta_location_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the location of this actor in world space.

Parameters:

- **delta\_location** ( _Vector_) – The change in location.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the location without teleporting will not update the location of simulated child/attached components.


Returns:

sweep\_hit\_result (HitResult): The hit result from the move if swept.

Return type:

HitResult


---

**add_actor_world_rotation**( _delta_rotation_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the rotation of this actor in world space.

Parameters:

- **delta\_rotation** ( _Rotator_) – The change in rotation.

- **sweep** ( _bool_) – Whether to sweep to the target rotation (not currently supported for rotation).

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the rotation without teleporting will not update the rotation of simulated child/attached components.


Returns:

sweep\_hit\_result (HitResult): The hit result from the move if swept.

Return type:

HitResult


---

**add_actor_world_transform**( _delta_transform_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the transform of this actor in world space. Ignores scale and sets it to (1,1,1).

Parameters:

- **delta\_transform** ( _Transform_)

- **sweep** ( _bool_)

- **teleport** ( _bool_)


Returns:

sweep\_hit\_result (HitResult):

Return type:

HitResult


---

**add_actor_world_transform_keep_scale**( _delta_transform_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the transform of this actor in world space. Scale is unchanged.

Parameters:

- **delta\_transform** ( _Transform_)

- **sweep** ( _bool_)

- **teleport** ( _bool_)


Returns:

sweep\_hit\_result (HitResult):

Return type:

HitResult


---

**add_tick_prerequisite_actor**( _prerequisite_actor_) → `None`

Make this actor tick after PrerequisiteActor. This only applies to this actor’s tick function; dependencies for owned components must be set up separately if desired.

Parameters:

**prerequisite\_actor** ( _Actor_)


---

**add_tick_prerequisite_component**( _prerequisite_component_) → `None`

Make this actor tick after PrerequisiteComponent. This only applies to this actor’s tick function; dependencies for owned components must be set up separately if desired.

Parameters:

**prerequisite\_component** ( _ActorComponent_)


---

_property_ `always_relevant`: bool

[Read-Write] Always relevant for network (overrides bOnlyRelevantToOwner).

**Type:**

( bool)


---

**attach_to_actor**( _parent_actor_, _socket_name_, _location_rule_, _rotation_rule_, _scale_rule_, _weld_simulated_bodies=True_) → `bool`

Attaches the RootComponent of this Actor to the supplied actor, optionally at a named socket.

Parameters:

- **parent\_actor** ( _Actor_) – Actor to attach this actor’s RootComponent to

- **socket\_name** ( _Name_) – Socket name to attach to, if any

- **location\_rule** ( _AttachmentRule_) – How to handle translation when attaching.

- **rotation\_rule** ( _AttachmentRule_) – How to handle rotation when attaching.

- **scale\_rule** ( _AttachmentRule_) – How to handle scale when attaching.

- **weld\_simulated\_bodies** ( _bool_) – Whether to weld together simulated physics bodies.This transfers the shapes in the welded object into the parent (if simulated), which can result in permanent changes that persist even after subsequently detaching.


Returns:

Whether the attachment was successful or not

Return type:

bool


---

**attach_to_component**( _parent_, _socket_name_, _location_rule_, _rotation_rule_, _scale_rule_, _weld_simulated_bodies=True_) → `bool`

Attaches the RootComponent of this Actor to the supplied component, optionally at a named socket. It is not valid to call this on components that are not Registered.

Parameters:

- **parent** ( _SceneComponent_) – Parent to attach to.

- **socket\_name** ( _Name_) – Optional socket to attach to on the parent.

- **location\_rule** ( _AttachmentRule_) – How to handle translation when attaching.

- **rotation\_rule** ( _AttachmentRule_) – How to handle rotation when attaching.

- **scale\_rule** ( _AttachmentRule_) – How to handle scale when attaching.

- **weld\_simulated\_bodies** ( _bool_) – Whether to weld together simulated physics bodies. This transfers the shapes in the welded object into the parent (if simulated), which can result in permanent changes that persist even after subsequently detaching.


Returns:

Whether the attachment was successful or not

Return type:

bool


---

_property_ `auto_destroy_when_finished`: bool

[Read-Write] If true then destroy self when “finished”, meaning all relevant components report that they are done and no timelines or timers are in flight.

**Type:**

( bool)


---

_property_ `can_be_damaged`: bool

[Read-Write] Whether this actor can take damage. Must be true for damage events (e.g. ReceiveDamage()) to be called.
see: https://www.unrealengine.com/blog/damage-in-ue4
see: TakeDamage(), ReceiveDamage()

**Type:**

( bool)


---

**can_trigger_resimulation**() → `bool`

Can this body trigger a resimulation when Physics Prediction is enabled

Return type:

bool


---

_property_ `content_bundle_guid`: Guid

[Read-Only] The GUID for this actor’s content bundle.

**Type:**

( Guid)


---

**create_input_component**( _input_component_to_create_) → `None`

Creates an input component from the input component passed in

Parameters:

**input\_component\_to\_create** ( _type_ _(_ _Class_ _)_) – The UInputComponent to create.


---

**create_pcg_data_from_actor**( _parse_actor=True_) → `PCGData`

Create PCGData from Actor

Parameters:

**parse\_actor** ( _bool_)

Return type:

PCGData


---

_property_ `custom_time_dilation`: float

[Read-Write] Allow each actor to run at a different time speed. The DeltaTime for a frame is multiplied by the global TimeDilation (in WorldSettings) and this CustomTimeDilation for this actor’s tick.

**Type:**

( float)


---

**destroy_actor**() → `None`

Destroy the actor


---

**detach_from_actor**( _location_rule=DetachmentRule.KEEP_RELATIVE_, _rotation_rule=DetachmentRule.KEEP_RELATIVE_, _scale_rule=DetachmentRule.KEEP_RELATIVE_) → `None`

Detaches the RootComponent of this Actor from any SceneComponent it is currently attached to.

Parameters:

- **location\_rule** ( _DetachmentRule_) – How to handle translation when detaching.

- **rotation\_rule** ( _DetachmentRule_) – How to handle rotation when detaching.

- **scale\_rule** ( _DetachmentRule_) – How to handle scale when detaching.



---

**disable_input**( _player_controller_) → `None`

Removes this actor from the stack of input being handled by a PlayerController.

Parameters:

**player\_controller** ( _PlayerController_) – The PlayerController whose input events we no longer want to receive. If null, this actor will stop receiving input from all PlayerControllers.


---

_property_ `enable_auto_lod_generation`: bool

[Read-Write] Whether this actor should be considered or not during HLOD generation.

**Type:**

( bool)


---

**enable_input**( _player_controller_) → `None`

Pushes this actor on to the stack of input being handled by a PlayerController.

Parameters:

**player\_controller** ( _PlayerController_) – The PlayerController whose input events we want to receive.


---

_property_ `find_camera_component_when_view_target`: bool

[Read-Write] If true, this actor should search for an owned camera component to view through when used as a view target.

**Type:**

( bool)


---

**find_component_by_tag**( _component_class=None_, _tag_) → `ActorComponent`

Searches components array and returns first encountered component with a given tag.

Parameters:

- **component\_class** ( _type_ _(_ _Class_ _)_)

- **tag** ( _Name_)


Return type:

ActorComponent


---

**flush_net_dormancy**() → `None`

Forces dormant actor to replicate but doesn’t change NetDormancy state (i.e., they will go dormant again if left dormant)


---

**force_net_update**() → `None`

Force actor to be updated to clients/demo net drivers


---

_property_ `generate_overlap_events_during_level_streaming`: bool

[Read-Write] If true, this actor will generate overlap Begin/End events when spawned as part of level streaming, which includes initial level load.
You might enable this is in the case where a streaming level loads around an actor and you want Begin/End overlap events to trigger.
see: UpdateOverlapsMethodDuringLevelStreaming

**Type:**

( bool)

get\_actor\_bounds( _only\_colliding\_components_, _include\_from\_child\_actors=False)->(origin=Vector_, _box\_extent=Vector_)

Returns the bounding box of all components that make up this Actor (excluding ChildActorComponents).

Parameters:

- **only\_colliding\_components** ( _bool_) – If true, will only return the bounding box for components with collision enabled.

- **include\_from\_child\_actors** ( _bool_) – If true then recurse in to ChildActor components


Returns:

origin (Vector): Set to the center of the actor in world space

box\_extent (Vector): Set to half the actor’s size in 3d space

Return type:

tuple


---

**get_actor_bounds_pcg**( _ignore_pcg_created_components=True_) → `Box`

Get Actor Bounds PCG

Parameters:

**ignore\_pcg\_created\_components** ( _bool_)

Return type:

Box


---

**get_actor_enable_collision**() → `bool`

Get current state of collision for the whole actor

Return type:

bool

get\_actor\_eyes\_view\_point( _)->(out\_location=Vector_, _out\_rotation=Rotator_)

Returns the point of view of the actor.
Note that this doesn’t mean the camera, but the ‘eyes’ of the actor.
For example, for a Pawn, this would define the eye height location,
and view rotation (which is different from the pawn rotation which has a zeroed pitch component).
A camera first person view will typically use this view point. Most traces (weapon, AI) will be done from this view point.

Returns:

out\_location (Vector): location of view point

out\_rotation (Rotator): view rotation of actor.

Return type:

tuple


---

**get_actor_forward_vector**() → `Vector`

Get the forward (X) vector (length 1.0) from this Actor, in world space.

Return type:

Vector


---

**get_actor_label**( _create_if_none=True_) → `str`

Returns this actor’s current label. Actor labels are only available in development builds.

Parameters:

**create\_if\_none** ( _bool_)

Return type:

str


---

**get_actor_local_bounds_pcg**( _ignore_pcg_created_components=True_) → `Box`

Get Actor Local Bounds PCG

Parameters:

**ignore\_pcg\_created\_components** ( _bool_)

Return type:

Box


---

**get_actor_location**() → `Vector`

Returns the location of the RootComponent of this Actor

Return type:

Vector


---

**get_actor_relative_scale3d**() → `Vector`

Return the actor’s relative scale 3d

Return type:

Vector


---

**get_actor_right_vector**() → `Vector`

Get the right (Y) vector (length 1.0) from this Actor, in world space.

Return type:

Vector


---

**get_actor_rotation**() → `Rotator`

Returns rotation of the RootComponent of this Actor.

Return type:

Rotator


---

**get_actor_scale3d**() → `Vector`

Returns the Actor’s world-space scale.

Return type:

Vector


---

**get_actor_tick_interval**() → `float`

Returns the tick interval of this actor’s primary tick function

Return type:

float


---

**get_actor_time_dilation**() → `float`

Get ActorTimeDilation - this can be used for input control or speed control for slomo.
We don’t want to scale input globally because input can be used for UI, which do not care for TimeDilation.

Return type:

float


---

**get_actor_transform**() → `Transform`

Get the actor-to-world transform.

Returns:

The transform that transforms from actor space to world space.

Return type:

Transform


---

**get_actor_up_vector**() → `Vector`

Get the up (Z) vector (length 1.0) from this Actor, in world space.

Return type:

Vector


---

**get_all_child_actors**( _include_descendants=True_) → `Array\ [Actor]`

Returns a list of all actors spawned by our Child Actor Components, including children of children.
This does not return the contents of the Children array

Parameters:

**include\_descendants** ( _bool_)

Returns:

child\_actors (Array[Actor]):

Return type:

Array\ [Actor]


---

**get_attach_parent_actor**() → `Actor`

Walk up the attachment chain from RootComponent until we encounter a different actor, and return it. If we are not attached to a component in a different actor, returns nullptr

Return type:

Actor


---

**get_attach_parent_socket_name**() → `Name`

Walk up the attachment chain from RootComponent until we encounter a different actor, and return the socket name in the component. If we are not attached to a component in a different actor, returns NAME\_None

Return type:

Name


---

**get_attached_actors**( _reset_array=True_, _recursively_include_attached_actors=False_) → `Array\ [Actor]`

Find all Actors which are attached directly to a component in this actor

Parameters:

- **reset\_array** ( _bool_)

- **recursively\_include\_attached\_actors** ( _bool_)


Returns:

out\_actors (Array[Actor]):

Return type:

Array\ [Actor]


---

**get_component_by_class**( _component_class=None_) → `ActorComponent`

Searches components array and returns first encountered component of the specified class

Parameters:

**component\_class** ( _type_ _(_ _Class_ _)_)

Return type:

ActorComponent


---

**get_components_by_class**( _component_class=None_) → `Array\ [ActorComponent]`

Gets all the components that inherit from the given class.
Currently returns an array of UActorComponent which must be cast to the correct type.
This intended to only be used by blueprints. Use GetComponents() in C++.

Parameters:

**component\_class** ( _type_ _(_ _Class_ _)_)

Return type:

Array\ [ActorComponent]


---

**get_components_by_interface**( _interface_) → `Array\ [ActorComponent]`

Gets all the components that implements the given interface.

Parameters:

**interface** ( _type_ _(_ _Class_ _)_)

Return type:

Array\ [ActorComponent]


---

**get_components_by_tag**( _component_class=None_, _tag_) → `Array\ [ActorComponent]`

Gets all the components that inherit from the given class with a given tag.

Parameters:

- **component\_class** ( _type_ _(_ _Class_ _)_)

- **tag** ( _Name_)


Return type:

Array\ [ActorComponent]


---

**get_default_actor_label**() → `str`

Returns this actor’s default label (does not include any numeric suffix). Actor labels are only available in development builds.

Return type:

str


---

**get_distance_to**( _other_actor_) → `float`

Returns the distance from this Actor to OtherActor.

Parameters:

**other\_actor** ( _Actor_)

Return type:

float


---

**get_dot_product_to**( _other_actor_) → `float`

Returns the dot product from this Actor to OtherActor. Returns -2.0 on failure. Returns 0.0 for coincidental actors.

Parameters:

**other\_actor** ( _Actor_)

Return type:

float


---

**get_folder_path**() → `Name`

Returns this actor’s folder path. Actor folder paths are only available in development builds.

Return type:

Name


---

**get_game_time_since_creation**() → `float`

The number of seconds (in game time) since this Actor was created, relative to Get Game Time In Seconds.

Return type:

float


---

**get_horizontal_distance_to**( _other_actor_) → `float`

Returns the distance from this Actor to OtherActor, ignoring Z.

Parameters:

**other\_actor** ( _Actor_)

Return type:

float


---

**get_horizontal_dot_product_to**( _other_actor_) → `float`

Returns the dot product from this Actor to OtherActor, ignoring Z. Returns -2.0 on failure. Returns 0.0 for coincidental actors.

Parameters:

**other\_actor** ( _Actor_)

Return type:

float


---

**get_instigator**() → `Pawn`

Returns the instigator for this actor, or nullptr if there is none.

Return type:

Pawn


---

**get_instigator_controller**() → `Controller`

Returns the instigator’s controller for this actor, or nullptr if there is none.

Return type:

Controller


---

**get_level**() → `Level`

Return the ULevel that this Actor is part of.

Return type:

Level


---

**get_level_transform**() → `Transform`

Return the FTransform of the level this actor is a part of.

Return type:

Transform


---

**get_life_span**() → `float`

Get the remaining lifespan of this actor. If zero is returned the actor lives forever.

Return type:

float


---

**get_local_role**() → `NetRole`

Returns how much control the local machine has over this actor.

Return type:

NetRole


---

**get_overlapping_actors**( _class_filter=None_) → `Array\ [Actor]`

Returns list of actors this actor is overlapping (any component overlapping any component). Does not return itself.

Parameters:

**class\_filter** ( _type_ _(_ _Class_ _)_) – [optional] If set, only returns actors of this class or subclasses

Returns:

overlapping\_actors (Array[Actor]): [out] Returned list of overlapping actors

Return type:

Array\ [Actor]


---

**get_overlapping_components**() → `Array\ [PrimitiveComponent]`

Returns list of components this actor is overlapping.

Returns:

overlapping\_components (Array[PrimitiveComponent]):

Return type:

Array\ [PrimitiveComponent]


---

**get_owner**() → `Actor`

Get the owner of this Actor, used primarily for network replication.

Return type:

Actor


---

**get_parent_actor**() → `Actor`

If this Actor was created by a Child Actor Component returns the Actor that owns that Child Actor Component

Return type:

Actor


---

**get_parent_component**() → `ChildActorComponent`

If this Actor was created by a Child Actor Component returns that Child Actor Component

Return type:

ChildActorComponent


---

**get_physics_replication_mode**() → `PhysicsReplicationMode`

Get the physics replication mode of this body, via EPhysicsReplicationMode

Return type:

PhysicsReplicationMode


---

**get_ray_tracing_group_id**() → `int32`

Return the RayTracingGroupId for this actor.

Return type:

int32


---

**get_remote_role**() → `NetRole`

Returns how much control the remote machine has over this actor.

Return type:

NetRole


---

**get_resimulation_threshold**() → `float`

Get the error threshold in centimeters before this object should enforce a resimulation to trigger.

Return type:

float


---

**get_squared_distance_to**( _other_actor_) → `float`

Returns the squared distance from this Actor to OtherActor.

Parameters:

**other\_actor** ( _Actor_)

Return type:

float


---

**get_squared_horizontal_distance_to**( _other_actor_) → `float`

Returns the squared distance from this Actor to OtherActor, ignoring Z.

Parameters:

**other\_actor** ( _Actor_)

Return type:

float


---

**get_tickable_when_paused**() → `bool`

Gets whether this actor can tick when paused.

Return type:

bool


---

**get_touching_actors**( _class_filter:Class=Ellipsis_) → `None`

deprecated: ‘get\_touching\_actors’ was renamed to ‘get\_overlapping\_actors’.


---

**get_touching_components**() → `None`

deprecated: ‘get\_touching\_components’ was renamed to ‘get\_overlapping\_components’.


---

**get_velocity**() → `Vector`

Returns velocity (in cm/s (Unreal Units/second) of the rootcomponent if it is either using physics or has an associated MovementComponent

Return type:

Vector


---

**get_vertical_distance_to**( _other_actor_) → `float`

Returns the distance from this Actor to OtherActor, ignoring XY.

Parameters:

**other\_actor** ( _Actor_)

Return type:

float


---

**has_authority**() → `bool`

Returns whether this actor has network authority

Return type:

bool


---

**has_tag**( _tag:Name_) → `bool`

deprecated: ‘has\_tag’ was renamed to ‘actor\_has\_tag’.


---

_property_ `hidden`: bool

[Read-Only] Allows us to only see this Actor in the Editor, and not in the actual game.
see: SetActorHiddenInGame()

**Type:**

( bool)


---

_property_ `initial_life_span`: float

[Read-Only] How long this Actor lives before dying, 0=forever. Note this is the INITIAL value and should not be modified once play has begun.

**Type:**

( float)


---

_property_ `instigator`: Pawn

[Read-Write] Pawn responsible for damage and other gameplay events caused by this actor.

**Type:**

( Pawn)


---

**is_actor_being_destroyed**() → `bool`

Returns true if this actor is currently being destroyed, some gameplay events may be unsafe

Return type:

bool


---

**is_actor_tick_enabled**() → `bool`

Returns whether this actor has tick enabled or not

Return type:

bool


---

**is_child_actor**() → `bool`

Returns whether this Actor was spawned by a child actor component

Return type:

bool


---

**is_editable**() → `bool`

Returns true if this actor is allowed to be displayed, selected and manipulated by the editor.

Return type:

bool


---

**is_hidden_ed**() → `bool`

Returns true if this actor is hidden in the editor viewports, also checking temporary flags.

Return type:

bool


---

**is_hidden_ed_at_startup**() → `bool`

Returns true if the actor is hidden upon editor startup/by default, false if it is not

Return type:

bool


---

**is_overlapping_actor**( _other_) → `bool`

Check whether any component of this Actor is overlapping any component of another Actor.

Parameters:

**other** ( _Actor_) – The other Actor to test against

Returns:

Whether any component of this Actor is overlapping any component of another Actor.

Return type:

bool


---

**is_selectable**() → `bool`

Returns true if this actor can EVER be selected in a level in the editor. Can be overridden by specific actors to make them unselectable.

Return type:

bool


---

_property_ `is_spatially_loaded`: bool

[Read-Write] Determine if this actor is spatially loaded when placed in a partitioned world.
If true, this actor will be loaded when in the range of any streaming sources and if (1) in no data layers, or (2) one or more of its data layers are enabled.
If false, this actor will be loaded if (1) in no data layers, or (2) one or more of its data layers are enabled.

**Type:**

( bool)


---

**is_temporarily_hidden_in_editor**( _include_parent=False_) → `bool`

Returns whether or not this actor was explicitly hidden in the editor for the duration of the current editor session

Parameters:

**include\_parent** ( _bool_) – Whether to recurse up child actor hierarchy or not

Return type:

bool


---

_property_ `life_span`: float

‘life\_span’ was renamed to ‘initial\_life\_span’.

**Type:**

deprecated


---

**make_noise**( _loudness=1.000000_, _noise_instigator=None_, _noise_location=[0.000000, 0.000000, 0.000000]_, _max_range=0.000000_, _tag='None'_) → `None`

Trigger a noise caused by a given Pawn, at a given location.
Note that the NoiseInstigator Pawn MUST have a PawnNoiseEmitterComponent for the noise to be detected by a PawnSensingComponent.
Senders of MakeNoise should have an Instigator if they are not pawns, or pass a NoiseInstigator.

Parameters:

- **loudness** ( _float_) – The relative loudness of this noise. Usual range is 0 (no noise) to 1 (full volume). If MaxRange is used, this scales the max range, otherwise it affects the hearing range specified by the sensor.

- **noise\_instigator** ( _Pawn_) – Pawn responsible for this noise. Uses the actor’s Instigator if NoiseInstigator is null

- **noise\_location** ( _Vector_) – Position of noise source. If zero vector, use the actor’s location.

- **max\_range** ( _float_) – Max range at which the sound may be heard. A value of 0 indicates no max range (though perception may have its own range). Loudness scales the range. (Note: not supported for legacy PawnSensingComponent, only for AIPerception)

- **tag** ( _Name_) – Identifier for the noise.



---

_property_ `min_net_update_frequency`: float

[Read-Write]

**Type:**

( float)


---

_property_ `net_cull_distance_squared`: float

[Read-Write]

**Type:**

( float)


---

_property_ `net_dormancy`: NetDormancy

[Read-Only] Dormancy setting for actor to take itself off of the replication list without being destroyed on clients.

**Type:**

( NetDormancy)


---

_property_ `net_priority`: float

[Read-Write] Priority for this actor when checking for replication in a low bandwidth or saturated situation, higher priority means it is more likely to replicate

**Type:**

( float)


---

_property_ `net_update_frequency`: float

[Read-Write]

**Type:**

( float)


---

_property_ `net_use_owner_relevancy`: bool

[Read-Write] If actor has valid Owner, call Owner’s IsNetRelevantFor and GetNetPriority

**Type:**

( bool)


---

_property_ `on_actor_begin_overlap`: ActorBeginOverlapSignature

[Read-Write] Called when another actor begins to overlap this actor, for example a player walking into a trigger.
For events when objects have a blocking collision, for example a player hitting a wall, see ‘Hit’ events.
note: Components on both this and the other Actor must have bGenerateOverlapEvents set to true to generate overlap events.

**Type:**

( ActorBeginOverlapSignature)


---

_property_ `on_actor_end_overlap`: ActorEndOverlapSignature

[Read-Write] Called when another actor stops overlapping this actor.
note: Components on both this and the other Actor must have bGenerateOverlapEvents set to true to generate overlap events.

**Type:**

( ActorEndOverlapSignature)


---

_property_ `on_actor_hit`: ActorHitSignature

[Read-Write] Called when this Actor hits (or is hit by) something solid. This could happen due to things like Character movement, using Set Location with ‘sweep’ enabled, or physics simulation.
For events when objects overlap (e.g. walking into a trigger) see the ‘Overlap’ event.
note: For collisions during physics simulation to generate hit events, ‘Simulation Generates Hit Events’ must be enabled.

**Type:**

( ActorHitSignature)


---

_property_ `on_actor_touch`: ActorBeginOverlapSignature

‘on\_actor\_touch’ was renamed to ‘on\_actor\_begin\_overlap’.

**Type:**

deprecated


---

_property_ `on_actor_un_touch`: ActorEndOverlapSignature

‘on\_actor\_un\_touch’ was renamed to ‘on\_actor\_end\_overlap’.

**Type:**

deprecated


---

**on_become_view_target**( _pc_) → `None`

Event called when this Actor becomes the view target for the given PlayerController.

Parameters:

**pc** ( _PlayerController_)


---

_property_ `on_begin_cursor_over`: ActorBeginCursorOverSignature

[Read-Write] Called when the mouse cursor is moved over this actor if mouse over events are enabled in the player controller.

**Type:**

( ActorBeginCursorOverSignature)


---

_property_ `on_clicked`: ActorOnClickedSignature

[Read-Write] Called when the left mouse button is clicked while the mouse is over this actor and click events are enabled in the player controller.

**Type:**

( ActorOnClickedSignature)


---

_property_ `on_destroyed`: ActorDestroyedSignature

[Read-Write] Event triggered when the actor has been explicitly destroyed.

**Type:**

( ActorDestroyedSignature)


---

_property_ `on_end_cursor_over`: ActorEndCursorOverSignature

[Read-Write] Called when the mouse cursor is moved off this actor if mouse over events are enabled in the player controller.

**Type:**

( ActorEndCursorOverSignature)


---

_property_ `on_end_play`: ActorEndPlaySignature

[Read-Write] Event triggered when the actor is being deleted or removed from a level.

**Type:**

( ActorEndPlaySignature)


---

**on_end_view_target**( _pc_) → `None`

Event called when this Actor is no longer the view target for the given PlayerController.

Parameters:

**pc** ( _PlayerController_)


---

_property_ `on_input_touch_begin`: ActorOnInputTouchBeginSignature

[Read-Write] Called when a touch input is received over this actor when touch events are enabled in the player controller.

**Type:**

( ActorOnInputTouchBeginSignature)


---

_property_ `on_input_touch_end`: ActorOnInputTouchEndSignature

[Read-Write] Called when a touch input is received over this component when touch events are enabled in the player controller.

**Type:**

( ActorOnInputTouchEndSignature)


---

_property_ `on_input_touch_enter`: ActorBeginTouchOverSignature

[Read-Write] Called when a finger is moved over this actor when touch over events are enabled in the player controller.

**Type:**

( ActorBeginTouchOverSignature)


---

_property_ `on_input_touch_leave`: ActorEndTouchOverSignature

[Read-Write] Called when a finger is moved off this actor when touch over events are enabled in the player controller.

**Type:**

( ActorEndTouchOverSignature)


---

_property_ `on_released`: ActorOnReleasedSignature

[Read-Write] Called when the left mouse button is released while the mouse is over this actor and click events are enabled in the player controller.

**Type:**

( ActorOnReleasedSignature)


---

**on_reset**() → `None`

Event called when this Actor is reset to its initial state - used when restarting level without reloading.


---

_property_ `on_take_any_damage`: TakeAnyDamageSignature

[Read-Write] Called when the actor is damaged in any way.

**Type:**

( TakeAnyDamageSignature)


---

_property_ `on_take_point_damage`: TakePointDamageSignature

[Read-Write] Called when the actor is damaged by point damage.

**Type:**

( TakePointDamageSignature)


---

_property_ `on_take_radial_damage`: TakeRadialDamageSignature

[Read-Write] Called when the actor is damaged by radial damage.

**Type:**

( TakeRadialDamageSignature)


---

_property_ `only_relevant_to_owner`: bool

[Read-Only] If true, this actor is only relevant to its owner. If this flag is changed during play, all non-owner channels would need to be explicitly closed.

**Type:**

( bool)


---

_property_ `pivot_offset`: Vector

[Read-Only] Local space pivot offset for the actor, only used in the editor

**Type:**

( Vector)


---

**prestream_textures**( _seconds_, _enable_streaming_, _cinematic_texture_groups=0_) → `None`

Calls PrestreamTextures() for all the actor’s meshcomponents.

Parameters:

- **seconds** ( _float_) – Number of seconds to force all mip-levels to be resident

- **enable\_streaming** ( _bool_) – Whether to start (true) or stop (false) streaming

- **cinematic\_texture\_groups** ( _int32_) – Bitfield indicating which texture groups that use extra high-resolution mips



---

**receive_actor_begin_cursor_over**() → `None`

Event when this actor has the mouse moved over it with the clickable interface.


---

**receive_actor_begin_overlap**( _other_actor_) → `None`

Event when this actor overlaps another actor, for example a player walking into a trigger.
For events when objects have a blocking collision, for example a player hitting a wall, see ‘Hit’ events.
note: Components on both this and the other Actor must have bGenerateOverlapEvents set to true to generate overlap events.

Parameters:

**other\_actor** ( _Actor_)


---

**receive_actor_end_cursor_over**() → `None`

Event when this actor has the mouse moved off of it with the clickable interface.


---

**receive_actor_end_overlap**( _other_actor_) → `None`

Event when an actor no longer overlaps another actor, and they have separated.
note: Components on both this and the other Actor must have bGenerateOverlapEvents set to true to generate overlap events.

Parameters:

**other\_actor** ( _Actor_)


---

**receive_actor_on_clicked**( _button_pressed_) → `None`

Event when this actor is clicked by the mouse when using the clickable interface.

Parameters:

**button\_pressed** ( _Key_)


---

**receive_actor_on_input_touch_begin**( _finger_index_) → `None`

Event when this actor is touched when click events are enabled.

Parameters:

**finger\_index** ( _TouchIndex_)


---

**receive_actor_on_input_touch_end**( _finger_index_) → `None`

Event when this actor is under the finger when untouched when click events are enabled.

Parameters:

**finger\_index** ( _TouchIndex_)


---

**receive_actor_on_input_touch_enter**( _finger_index_) → `None`

Event when this actor has a finger moved over it with the clickable interface.

Parameters:

**finger\_index** ( _TouchIndex_)


---

**receive_actor_on_input_touch_leave**( _finger_index_) → `None`

Event when this actor has a finger moved off of it with the clickable interface.

Parameters:

**finger\_index** ( _TouchIndex_)


---

**receive_actor_on_released**( _button_released_) → `None`

Event when this actor is under the mouse when left mouse button is released while using the clickable interface.

Parameters:

**button\_released** ( _Key_)


---

**receive_actor_touch**( _other_actor:Actor_) → `None`

deprecated: ‘receive\_actor\_touch’ was renamed to ‘receive\_actor\_begin\_overlap’.


---

**receive_actor_untouch**( _other_actor:Actor_) → `None`

deprecated: ‘receive\_actor\_untouch’ was renamed to ‘receive\_actor\_end\_overlap’.


---

**receive_any_damage**( _damage_, _damage_type_, _instigated_by_, _damage_causer_) → `None`

Event when this actor takes ANY damage

Parameters:

- **damage** ( _float_)

- **damage\_type** ( _DamageType_)

- **instigated\_by** ( _Controller_)

- **damage\_causer** ( _Actor_)



---

**receive_async_physics_tick**( _delta_seconds_, _sim_seconds_) → `None`

Event called every physics tick if bAsyncPhysicsTickEnabled is true

Parameters:

- **delta\_seconds** ( _float_)

- **sim\_seconds** ( _float_)



---

**receive_begin_play**() → `None`

Event when play begins for this actor.


---

**receive_destroyed**() → `None`

Called when the actor has been explicitly destroyed.


---

**receive_end_play**( _end_play_reason_) → `None`

Event to notify blueprints this actor is being deleted or removed from a level.

Parameters:

**end\_play\_reason** ( _EndPlayReason_)


---

**receive_hit**( _my_comp_, _other_, _other_comp_, _self_moved_, _hit_location_, _hit_normal_, _normal_impulse_, _hit_) → `None`

Event when this actor bumps into a blocking object, or blocks another actor that bumps into it.
This could happen due to things like Character movement, using Set Location with ‘sweep’ enabled, or physics simulation.
For events when objects overlap (e.g. walking into a trigger) see the ‘Overlap’ event.
note: For collisions during physics simulation to generate hit events, ‘Simulation Generates Hit Events’ must be enabled.
note: When receiving a hit from another object’s movement (bSelfMoved is false), the directions of ‘Hit.Normal’ and ‘Hit.ImpactNormal’ will be adjusted to indicate force from the other object against this object.
note: NormalImpulse will be filled in for physics-simulating bodies, but will be zero for swept-component blocking collisions.

Parameters:

- **my\_comp** ( _PrimitiveComponent_)

- **other** ( _Actor_)

- **other\_comp** ( _PrimitiveComponent_)

- **self\_moved** ( _bool_)

- **hit\_location** ( _Vector_)

- **hit\_normal** ( _Vector_)

- **normal\_impulse** ( _Vector_)

- **hit** ( _HitResult_)



---

**receive_point_damage**( _damage_, _damage_type_, _hit_location_, _hit_normal_, _hit_component_, _bone_name_, _shot_from_direction_, _instigated_by_, _damage_causer_, _hit_info_) → `None`

Event when this actor takes POINT damage

Parameters:

- **damage** ( _float_)

- **damage\_type** ( _DamageType_)

- **hit\_location** ( _Vector_)

- **hit\_normal** ( _Vector_)

- **hit\_component** ( _PrimitiveComponent_)

- **bone\_name** ( _Name_)

- **shot\_from\_direction** ( _Vector_)

- **instigated\_by** ( _Controller_)

- **damage\_causer** ( _Actor_)

- **hit\_info** ( _HitResult_)



---

**receive_radial_damage**( _damage_received_, _damage_type_, _origin_, _hit_info_, _instigated_by_, _damage_causer_) → `None`

Event when this actor takes RADIAL damage

Parameters:

- **damage\_received** ( _float_)

- **damage\_type** ( _DamageType_)

- **origin** ( _Vector_)

- **hit\_info** ( _HitResult_)

- **instigated\_by** ( _Controller_)

- **damage\_causer** ( _Actor_)



---

**receive_tick**( _delta_seconds_) → `None`

Event called every frame, if ticking is enabled

Parameters:

**delta\_seconds** ( _float_)


---

**register_as_focal_point_in_physics_replication_lod**() → `None`

Register this actors root components physics object as a focal particle in Physics Repliocation LOD


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

[Read-Only] When true the replication system will only replicate the registered subobjects and the replicated actor components list
When false the replication system will instead call the virtual ReplicateSubobjects() function where the subobjects and actor components need to be manually replicated.

**Type:**

( bool)


---

_property_ `replicates`: bool

[Read-Only] If true, this actor will replicate to remote machines
see: SetReplicates()

**Type:**

( bool)


---

_property_ `root_component`: SceneComponent

[Read-Only] The component that defines the transform (location, rotation, scale) of this Actor in the world, all other components must be attached to this one somehow

**Type:**

( SceneComponent)


---

_property_ `runtime_grid`: Name

[Read-Write] Determine in which partition grid this actor will be placed in the partition (if the world is partitioned).
If None, the decision will be left to the partition.

**Type:**

( Name)


---

**set_actor_enable_collision**( _new_actor_enable_collision_) → `None`

Allows enabling/disabling collision for the whole actor

Parameters:

**new\_actor\_enable\_collision** ( _bool_)


---

**set_actor_hidden**( _new_hidden:bool_) → `None`

deprecated: ‘set\_actor\_hidden’ was renamed to ‘set\_actor\_hidden\_in\_game’.


---

**set_actor_hidden_in_game**( _new_hidden_) → `None`

Sets the actor to be hidden in the game

Parameters:

**new\_hidden** ( _bool_) – Whether or not to hide the actor and all its components


---

**set_actor_label**( _new_actor_label_, _mark_dirty=True_) → `None`

Assigns a new label to this actor. Actor labels are only available in development builds.

Parameters:

- **new\_actor\_label** ( _str_) – The new label string to assign to the actor. If empty, the actor will have a default label.

- **mark\_dirty** ( _bool_) – If true the actor’s package will be marked dirty for saving. Otherwise it will not be. You should pass false for this parameter if dirtying is not allowed (like during loads)



---

**set_actor_location**( _new_location_, _sweep_, _teleport_) → `HitResultorNone`

Move the Actor to the specified location.

Parameters:

- **new\_location** ( _Vector_) – The new location to move the Actor to.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the location without teleporting will not update the location of simulated child/attached components.


Returns:

Whether the location was successfully set (if not swept), or whether movement occurred at all (if swept).

sweep\_hit\_result (HitResult): The hit result from the move if swept.

Return type:

HitResult or None


---

**set_actor_location_and_rotation**( _new_location_, _new_rotation_, _sweep_, _teleport_) → `HitResultorNone`

Move the actor instantly to the specified location and rotation.

Parameters:

- **new\_location** ( _Vector_) – The new location to teleport the Actor to.

- **new\_rotation** ( _Rotator_) – The new rotation for the Actor.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the location without teleporting will not update the location of simulated child/attached components.


Returns:

Whether the rotation was successfully set.

sweep\_hit\_result (HitResult): The hit result from the move if swept.

Return type:

HitResult or None


---

**set_actor_relative_location**( _new_relative_location_, _sweep_, _teleport_) → `HitResult`

Set the actor’s RootComponent to the specified relative location.

Parameters:

- **new\_relative\_location** ( _Vector_) – New relative location of the actor’s root component

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the location without teleporting will not update the location of simulated child/attached components.


Returns:

sweep\_hit\_result (HitResult):

Return type:

HitResult


---

**set_actor_relative_rotation**( _new_relative_rotation_, _sweep_, _teleport_) → `HitResult`

Set the actor’s RootComponent to the specified relative rotation

Parameters:

- **new\_relative\_rotation** ( _Rotator_) – New relative rotation of the actor’s root component

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the rotation without teleporting will not update the rotation of simulated child/attached components.


Returns:

sweep\_hit\_result (HitResult):

Return type:

HitResult


---

**set_actor_relative_scale3d**( _new_relative_scale_) → `None`

Set the actor’s RootComponent to the specified relative scale 3d

Parameters:

**new\_relative\_scale** ( _Vector_) – New scale to set the actor’s RootComponent to


---

**set_actor_relative_transform**( _new_relative_transform_, _sweep_, _teleport_) → `HitResult`

Set the actor’s RootComponent to the specified relative transform

Parameters:

- **new\_relative\_transform** ( _Transform_) – New relative transform of the actor’s root component

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the transform without teleporting will not update the transform of simulated child/attached components.


Returns:

sweep\_hit\_result (HitResult):

Return type:

HitResult


---

**set_actor_rotation**( _new_rotation_, _teleport_physics_) → `bool`

Set the Actor’s rotation instantly to the specified rotation.

Parameters:

- **new\_rotation** ( _Rotator_) – The new rotation for the Actor.

- **teleport\_physics** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the rotation without teleporting will not update the rotation of simulated child/attached components.


Returns:

Whether the rotation was successfully set.

Return type:

bool


---

**set_actor_scale3d**( _new_scale3d_) → `None`

Set the Actor’s world-space scale.

Parameters:

**new\_scale3d** ( _Vector_)


---

**set_actor_tick_enabled**( _enabled_) → `None`

Set this actor’s tick functions to be enabled or disabled. Only has an effect if the function is registered
This only modifies the tick function on actor itself

Parameters:

**enabled** ( _bool_) – Whether it should be enabled or not


---

**set_actor_tick_interval**( _tick_interval_) → `None`

Sets the tick interval of this actor’s primary tick function. Will not enable a disabled tick function. Takes effect on next tick.

Parameters:

**tick\_interval** ( _float_) – The rate at which this actor should be ticking


---

**set_actor_transform**( _new_transform_, _sweep_, _teleport_) → `HitResultorNone`

Set the Actors transform to the specified one.

Parameters:

- **new\_transform** ( _Transform_) – The new transform.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire swept volume. Note that when teleporting, any child/attached components will be teleported too, maintaining their current offset even if they are being simulated. Setting the transform without teleporting will not update the transform of simulated child/attached components.


Returns:

sweep\_hit\_result (HitResult):

Return type:

HitResult or None


---

**set_folder_path**( _new_folder_path_) → `None`

Assigns a new folder to this actor. Actor folder paths are only available in development builds.

Parameters:

**new\_folder\_path** ( _Name_) – The new folder to assign to the actor.


---

**set_is_temporarily_hidden_in_editor**( _is_hidden_) → `None`

Explicitly sets whether or not this actor is hidden in the editor for the duration of the current editor session

Parameters:

**is\_hidden** ( _bool_) – True if the actor is hidden


---

**set_life_span**( _lifespan_) → `None`

Set the lifespan of this actor. When it expires the object will be destroyed. If requested lifespan is 0, the timer is cleared and the actor will not be destroyed.

Parameters:

**lifespan** ( _float_)


---

**set_net_dormancy**( _new_dormancy_) → `None`

Puts actor in dormant networking state

Parameters:

**new\_dormancy** ( _NetDormancy_)


---

**set_owner**( _new_owner_) → `None`

Set the owner of this Actor, used primarily for network replication.

Parameters:

**new\_owner** ( _Actor_) – The Actor who takes over ownership of this Actor


---

**set_physics_replication_mode**( _replication_mode_) → `None`

Set the physics replication mode of this body, via EPhysicsReplicationMode

Parameters:

**replication\_mode** ( _PhysicsReplicationMode_)


---

**set_ray_tracing_group_id**( _raytracing_group_id_) → `None`

Specify a RayTracingGroupId for this actors. Components with invalid RayTracingGroupId will inherit the actors.

Parameters:

**raytracing\_group\_id** ( _int32_)


---

**set_replicate_movement**( _replicate_movement_) → `None`

Set whether this actor’s movement replicates to network clients.

Parameters:

**replicate\_movement** ( _bool_) – Whether this Actor’s movement replicates to clients.


---

**set_replicates**( _replicates_) → `None`

Set whether this actor replicates to network clients. When this actor is spawned on the server it will be sent to clients as well.
Properties flagged for replication will update on clients if they change on the server.
Internally changes the RemoteRole property and handles the cases where the actor needs to be added to the network actor list.
see: https://docs.unrealengine.com/InteractiveExperiences/Networking/Actors

Parameters:

**replicates** ( _bool_) – Whether this Actor replicates to network clients.


---

**set_tick_enabled**( _enabled:bool_) → `None`

deprecated: ‘set\_tick\_enabled’ was renamed to ‘set\_actor\_tick\_enabled’.


---

**set_tick_group**( _new_tick_group_) → `None`

Sets the ticking group for this actor.

Parameters:

**new\_tick\_group** ( _TickingGroup_) – the new value to assign


---

**set_tick_prerequisite**( _prerequisite_actor:Actor_) → `None`

deprecated: ‘set\_tick\_prerequisite’ was renamed to ‘add\_tick\_prerequisite\_actor’.


---

**set_tickable_when_paused**( _tickable_when_paused_) → `None`

Sets whether this actor can tick when paused.

Parameters:

**tickable\_when\_paused** ( _bool_)


---

_property_ `spawn_collision_handling_method`: SpawnActorCollisionHandlingMethod

[Read-Write] Controls how to handle spawning this actor in a situation where it’s colliding with something else. “Default” means AlwaysSpawn here.

**Type:**

( SpawnActorCollisionHandlingMethod)


---

_property_ `sprite_scale`: float

[Read-Write] The scale to apply to any billboard components in editor builds (happens in any WITH\_EDITOR build, including non-cooked games).

**Type:**

( float)


---

_property_ `tags`: None

[Read-Write] Array of tags that can be used for grouping and categorizing.

**Type:**

( Array\ [Name])


---

**tear_off**() → `None`

Networking - Server - TearOff this actor to stop replication to clients. Will set bTearOff to true.


---

**teleport**( _dest_location_, _dest_rotation_) → `bool`

Teleport this actor to a new location. If the actor doesn’t fit exactly at the location specified, tries to slightly move it out of walls and such.

Parameters:

- **dest\_location** ( _Vector_) – The target destination point

- **dest\_rotation** ( _Rotator_) – The target rotation at the destination


Returns:

true if the actor has been successfully moved, or false if it couldn’t fit.

Return type:

bool


---

**unregister_as_focal_point_in_physics_replication_lod**() → `None`

Unregister this actors root components physics object from being a focal particle in Physics Repliocation LOD


---

**was_recently_rendered**( _tolerance=0.200000_) → `bool`

Returns true if this actor has been rendered “recently”, with a tolerance in seconds to define what “recent” means.
e.g.: If a tolerance of 0.1 is used, this function will return true only if the actor was rendered in the last 0.1 seconds of game time.

Parameters:

**tolerance** ( _float_) – How many seconds ago the actor last render time can be and still count as having been “recently” rendered.

Returns:

Whether this actor was recently rendered.

Return type:

bool

### Table of Contents

- `unreal.Actor`
  - `Actor`
    - `Actor.acquire_editor_element_handle()`
    - `Actor.actor_guid`
    - `Actor.actor_has_tag()`
    - `Actor.actor_instance_guid`
    - `Actor.add_actor_local_offset()`
    - `Actor.add_actor_local_rotation()`
    - `Actor.add_actor_local_transform()`
    - `Actor.add_actor_world_offset()`
    - `Actor.add_actor_world_rotation()`
    - `Actor.add_actor_world_transform()`
    - `Actor.add_actor_world_transform_keep_scale()`
    - `Actor.add_tick_prerequisite_actor()`
    - `Actor.add_tick_prerequisite_component()`
    - `Actor.always_relevant`
    - `Actor.attach_to_actor()`
    - `Actor.attach_to_component()`
    - `Actor.auto_destroy_when_finished`
    - `Actor.can_be_damaged`
    - `Actor.can_trigger_resimulation()`
    - `Actor.content_bundle_guid`
    - `Actor.create_input_component()`
    - `Actor.create_pcg_data_from_actor()`
    - `Actor.custom_time_dilation`
    - `Actor.destroy_actor()`
    - `Actor.detach_from_actor()`
    - `Actor.disable_input()`
    - `Actor.enable_auto_lod_generation`
    - `Actor.enable_input()`
    - `Actor.find_camera_component_when_view_target`
    - `Actor.find_component_by_tag()`
    - `Actor.flush_net_dormancy()`
    - `Actor.force_net_update()`
    - `Actor.generate_overlap_events_during_level_streaming`
    - `Actor.get_actor_bounds()`
    - `Actor.get_actor_bounds_pcg()`
    - `Actor.get_actor_enable_collision()`
    - `Actor.get_actor_eyes_view_point()`
    - `Actor.get_actor_forward_vector()`
    - `Actor.get_actor_label()`
    - `Actor.get_actor_local_bounds_pcg()`
    - `Actor.get_actor_location()`
    - `Actor.get_actor_relative_scale3d()`
    - `Actor.get_actor_right_vector()`
    - `Actor.get_actor_rotation()`
    - `Actor.get_actor_scale3d()`
    - `Actor.get_actor_tick_interval()`
    - `Actor.get_actor_time_dilation()`
    - `Actor.get_actor_transform()`
    - `Actor.get_actor_up_vector()`
    - `Actor.get_all_child_actors()`
    - `Actor.get_attach_parent_actor()`
    - `Actor.get_attach_parent_socket_name()`
    - `Actor.get_attached_actors()`
    - `Actor.get_component_by_class()`
    - `Actor.get_components_by_class()`
    - `Actor.get_components_by_interface()`
    - `Actor.get_components_by_tag()`
    - `Actor.get_default_actor_label()`
    - `Actor.get_distance_to()`
    - `Actor.get_dot_product_to()`
    - `Actor.get_folder_path()`
    - `Actor.get_game_time_since_creation()`
    - `Actor.get_horizontal_distance_to()`
    - `Actor.get_horizontal_dot_product_to()`
    - `Actor.get_instigator()`
    - `Actor.get_instigator_controller()`
    - `Actor.get_level()`
    - `Actor.get_level_transform()`
    - `Actor.get_life_span()`
    - `Actor.get_local_role()`
    - `Actor.get_overlapping_actors()`
    - `Actor.get_overlapping_components()`
    - `Actor.get_owner()`
    - `Actor.get_parent_actor()`
    - `Actor.get_parent_component()`
    - `Actor.get_physics_replication_mode()`
    - `Actor.get_ray_tracing_group_id()`
    - `Actor.get_remote_role()`
    - `Actor.get_resimulation_threshold()`
    - `Actor.get_squared_distance_to()`
    - `Actor.get_squared_horizontal_distance_to()`
    - `Actor.get_tickable_when_paused()`
    - `Actor.get_touching_actors()`
    - `Actor.get_touching_components()`
    - `Actor.get_velocity()`
    - `Actor.get_vertical_distance_to()`
    - `Actor.has_authority()`
    - `Actor.has_tag()`
    - `Actor.hidden`
    - `Actor.initial_life_span`
    - `Actor.instigator`
    - `Actor.is_actor_being_destroyed()`
    - `Actor.is_actor_tick_enabled()`
    - `Actor.is_child_actor()`
    - `Actor.is_editable()`
    - `Actor.is_hidden_ed()`
    - `Actor.is_hidden_ed_at_startup()`
    - `Actor.is_overlapping_actor()`
    - `Actor.is_selectable()`
    - `Actor.is_spatially_loaded`
    - `Actor.is_temporarily_hidden_in_editor()`
    - `Actor.life_span`
    - `Actor.make_noise()`
    - `Actor.min_net_update_frequency`
    - `Actor.net_cull_distance_squared`
    - `Actor.net_dormancy`
    - `Actor.net_priority`
    - `Actor.net_update_frequency`
    - `Actor.net_use_owner_relevancy`
    - `Actor.on_actor_begin_overlap`
    - `Actor.on_actor_end_overlap`
    - `Actor.on_actor_hit`
    - `Actor.on_actor_touch`
    - `Actor.on_actor_un_touch`
    - `Actor.on_become_view_target()`
    - `Actor.on_begin_cursor_over`
    - `Actor.on_clicked`
    - `Actor.on_destroyed`
    - `Actor.on_end_cursor_over`
    - `Actor.on_end_play`
    - `Actor.on_end_view_target()`
    - `Actor.on_input_touch_begin`
    - `Actor.on_input_touch_end`
    - `Actor.on_input_touch_enter`
    - `Actor.on_input_touch_leave`
    - `Actor.on_released`
    - `Actor.on_reset()`
    - `Actor.on_take_any_damage`
    - `Actor.on_take_point_damage`
    - `Actor.on_take_radial_damage`
    - `Actor.only_relevant_to_owner`
    - `Actor.pivot_offset`
    - `Actor.prestream_textures()`
    - `Actor.receive_actor_begin_cursor_over()`
    - `Actor.receive_actor_begin_overlap()`
    - `Actor.receive_actor_end_cursor_over()`
    - `Actor.receive_actor_end_overlap()`
    - `Actor.receive_actor_on_clicked()`
    - `Actor.receive_actor_on_input_touch_begin()`
    - `Actor.receive_actor_on_input_touch_end()`
    - `Actor.receive_actor_on_input_touch_enter()`
    - `Actor.receive_actor_on_input_touch_leave()`
    - `Actor.receive_actor_on_released()`
    - `Actor.receive_actor_touch()`
    - `Actor.receive_actor_untouch()`
    - `Actor.receive_any_damage()`
    - `Actor.receive_async_physics_tick()`
    - `Actor.receive_begin_play()`
    - `Actor.receive_destroyed()`
    - `Actor.receive_end_play()`
    - `Actor.receive_hit()`
    - `Actor.receive_point_damage()`
    - `Actor.receive_radial_damage()`
    - `Actor.receive_tick()`
    - `Actor.register_as_focal_point_in_physics_replication_lod()`
    - `Actor.remove_tick_prerequisite_actor()`
    - `Actor.remove_tick_prerequisite_component()`
    - `Actor.replicate_using_registered_sub_object_list`
    - `Actor.replicates`
    - `Actor.root_component`
    - `Actor.runtime_grid`
    - `Actor.set_actor_enable_collision()`
    - `Actor.set_actor_hidden()`
    - `Actor.set_actor_hidden_in_game()`
    - `Actor.set_actor_label()`
    - `Actor.set_actor_location()`
    - `Actor.set_actor_location_and_rotation()`
    - `Actor.set_actor_relative_location()`
    - `Actor.set_actor_relative_rotation()`
    - `Actor.set_actor_relative_scale3d()`
    - `Actor.set_actor_relative_transform()`
    - `Actor.set_actor_rotation()`
    - `Actor.set_actor_scale3d()`
    - `Actor.set_actor_tick_enabled()`
    - `Actor.set_actor_tick_interval()`
    - `Actor.set_actor_transform()`
    - `Actor.set_folder_path()`
    - `Actor.set_is_temporarily_hidden_in_editor()`
    - `Actor.set_life_span()`
    - `Actor.set_net_dormancy()`
    - `Actor.set_owner()`
    - `Actor.set_physics_replication_mode()`
    - `Actor.set_ray_tracing_group_id()`
    - `Actor.set_replicate_movement()`
    - `Actor.set_replicates()`
    - `Actor.set_tick_enabled()`
    - `Actor.set_tick_group()`
    - `Actor.set_tick_prerequisite()`
    - `Actor.set_tickable_when_paused()`
    - `Actor.spawn_collision_handling_method`
    - `Actor.sprite_scale`
    - `Actor.tags`
    - `Actor.tear_off()`
    - `Actor.teleport()`
    - `Actor.unregister_as_focal_point_in_physics_replication_lod()`
    - `Actor.was_recently_rendered()`