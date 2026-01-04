# unreal.GameplayCueParameters

```python
class unreal.GameplayCueParameters(normalized\magnitude:float=0.0, raw\magnitude:float=0.0, effect\context:GameplayEffectContextHandle=\[\], matched\tag\name:GameplayTag=Ellipsis, original\tag:GameplayTag=Ellipsis, aggregated\source\tags:GameplayTagContainer=Ellipsis, aggregated\target\tags:GameplayTagContainer=Ellipsis, location:Vector=Ellipsis, normal:Vector=Ellipsis, instigator:Actor=Ellipsis, effect\causer:Actor=Ellipsis, source\object:Object=Ellipsis, physical\material:PhysicalMaterial=Ellipsis, gameplay\effect\level:int=1, ability\level:int=1, target\attach\component:SceneComponent=Ellipsis, replicate\location\when\using\minimal\rep\proxy:bool=False)
```


**Bases:** ``StructBase``


Metadata about a gameplay cue execution

**C++ Source:**

- **Plugin**: GameplayAbilities

- **Module**: GameplayAbilities

- **File**: GameplayEffectTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `ability_level` (int32): [Read-Write] If originating from an ability, this will be the level of that ability

- `aggregated_source_tags` (GameplayTagContainer): [Read-Write] The aggregated source tags taken from the effect spec

- `aggregated_target_tags` (GameplayTagContainer): [Read-Write] The aggregated target tags taken from the effect spec

- `effect_causer` (Actor): [Read-Write] The physical actor that actually did the damage, can be a weapon or projectile

- `effect_context` (GameplayEffectContextHandle): [Read-Write] Effect context, contains information about hit result, etc

- `gameplay_effect_level` (int32): [Read-Write] If originating from a GameplayEffect, the level of that GameplayEffect

- `instigator` (Actor): [Read-Write] Instigator actor, the actor that owns the ability system component

- `location` (Vector\_NetQuantize10): [Read-Write] Location cue took place at

- `matched_tag_name` (GameplayTag): [Read-Write] The tag name that matched this specific gameplay cue handler

- `normal` (Vector\_NetQuantizeNormal): [Read-Write] Normal of impact that caused cue

- `normalized_magnitude` (float): [Read-Write] Magnitude of source gameplay effect, normalzed from 0-1. Use this for “how strong is the gameplay effect” (0=min, 1=,max)

- `original_tag` (GameplayTag): [Read-Write] The original tag of the gameplay cue

- `physical_material` (PhysicalMaterial): [Read-Write] PhysMat of the hit, if there was a hit.

- `raw_magnitude` (float): [Read-Write] Raw final magnitude of source gameplay effect. Use this is you need to display numbers or for other informational purposes.

- `replicate_location_when_using_minimal_rep_proxy` (bool): [Read-Write] If we’re using a minimal replication proxy, should we replicate location for this cue

- `source_object` (Object): [Read-Write] Object this effect was created from, can be an actor or static object. Useful to bind an effect to a gameplay object

- `target_attach_component` (SceneComponent): [Read-Write] Could be used to say “attach FX to this component always”



---

_property_ `ability_level`: int

[Read-Write] If originating from an ability, this will be the level of that ability

**Type:**

(int32)


---

_property_ `aggregated_source_tags`: GameplayTagContainer

[Read-Write] The aggregated source tags taken from the effect spec

**Type:**

( GameplayTagContainer)


---

_property_ `aggregated_target_tags`: GameplayTagContainer

[Read-Write] The aggregated target tags taken from the effect spec

**Type:**

( GameplayTagContainer)


---

_property_ `effect_causer`: Actor

[Read-Write] The physical actor that actually did the damage, can be a weapon or projectile

**Type:**

( Actor)


---

_property_ `effect_context`: GameplayEffectContextHandle

[Read-Write] Effect context, contains information about hit result, etc

**Type:**

( GameplayEffectContextHandle)


---

_property_ `gameplay_effect_level`: int

[Read-Write] If originating from a GameplayEffect, the level of that GameplayEffect

**Type:**

(int32)


---

_property_ `instigator`: Actor

[Read-Write] Instigator actor, the actor that owns the ability system component

**Type:**

( Actor)


---

_property_ `location`: Vector\

[Read-Write] Location cue took place at

**Type:**

( Vector\_NetQuantize10)


---

_property_ `matched_tag_name`: GameplayTag

[Read-Write] The tag name that matched this specific gameplay cue handler

**Type:**

( GameplayTag)


---

_property_ `normal`: Vector\

[Read-Write] Normal of impact that caused cue

**Type:**

( Vector\_NetQuantizeNormal)


---

_property_ `normalized_magnitude`: float

[Read-Write] Magnitude of source gameplay effect, normalzed from 0-1. Use this for “how strong is the gameplay effect” (0=min, 1=,max)

**Type:**

( float)


---

_property_ `original_tag`: GameplayTag

[Read-Write] The original tag of the gameplay cue

**Type:**

( GameplayTag)


---

_property_ `physical_material`: PhysicalMaterial

[Read-Write] PhysMat of the hit, if there was a hit.

**Type:**

( PhysicalMaterial)


---

_property_ `raw_magnitude`: float

[Read-Write] Raw final magnitude of source gameplay effect. Use this is you need to display numbers or for other informational purposes.

**Type:**

( float)


---

_property_ `replicate_location_when_using_minimal_rep_proxy`: bool

[Read-Write] If we’re using a minimal replication proxy, should we replicate location for this cue

**Type:**

( bool)


---

_property_ `source_object`: Object

[Read-Write] Object this effect was created from, can be an actor or static object. Useful to bind an effect to a gameplay object

**Type:**

( Object)


---

_property_ `target_attach_component`: SceneComponent

[Read-Write] Could be used to say “attach FX to this component always”

**Type:**

( SceneComponent)

### Table of Contents

- `unreal.GameplayCueParameters`
  - `GameplayCueParameters`
    - `GameplayCueParameters.ability_level`
    - `GameplayCueParameters.aggregated_source_tags`
    - `GameplayCueParameters.aggregated_target_tags`
    - `GameplayCueParameters.effect_causer`
    - `GameplayCueParameters.effect_context`
    - `GameplayCueParameters.gameplay_effect_level`
    - `GameplayCueParameters.instigator`
    - `GameplayCueParameters.location`
    - `GameplayCueParameters.matched_tag_name`
    - `GameplayCueParameters.normal`
    - `GameplayCueParameters.normalized_magnitude`
    - `GameplayCueParameters.original_tag`
    - `GameplayCueParameters.physical_material`
    - `GameplayCueParameters.raw_magnitude`
    - `GameplayCueParameters.replicate_location_when_using_minimal_rep_proxy`
    - `GameplayCueParameters.source_object`
    - `GameplayCueParameters.target_attach_component`