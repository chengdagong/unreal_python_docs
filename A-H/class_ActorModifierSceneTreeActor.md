# unreal.ActorModifierSceneTreeActor

```python
class unreal.ActorModifierSceneTreeActor(reference_container:ActorModifierReferenceContainer=Ellipsis, reference_actor_weak:Actor=Ellipsis, skip_hidden_actors:bool=False)
```


**Bases:** ``StructBase``


Actor Modifier Scene Tree Actor

**C++ Source:**

- **Plugin**: ActorModifier

- **Module**: ActorModifier

- **File**: ActorModifierSceneTreeUpdateExtension.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `reference_actor_weak` (Actor): [Read-Write] The actor being followed by the modifier. This is user selectable if the Reference Container is set to “Other”

- `reference_container` (ActorModifierReferenceContainer): [Read-Write] The method for finding a reference actor based on it’s position in the parent’s hierarchy

- `skip_hidden_actors` (bool): [Read-Write] If true, will search for the next visible actor based on the selected reference container



---

_property_ `reference_actor_weak`: Actor

[Read-Write] The actor being followed by the modifier. This is user selectable if the Reference Container is set to “Other”

**Type:**

( Actor)


---

_property_ `reference_container`: ActorModifierReferenceContainer

[Read-Write] The method for finding a reference actor based on it’s position in the parent’s hierarchy

**Type:**

( ActorModifierReferenceContainer)


---

_property_ `skip_hidden_actors`: bool

[Read-Write] If true, will search for the next visible actor based on the selected reference container

**Type:**

( bool)

### Table of Contents

- `unreal.ActorModifierSceneTreeActor`
  - `ActorModifierSceneTreeActor`
    - `ActorModifierSceneTreeActor.reference_actor_weak`
    - `ActorModifierSceneTreeActor.reference_container`
    - `ActorModifierSceneTreeActor.skip_hidden_actors`