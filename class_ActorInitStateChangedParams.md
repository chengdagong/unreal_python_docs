# unreal.ActorInitStateChangedParams

```python
class unreal.ActorInitStateChangedParams(owning_actor:Actor=Ellipsis, feature_name:Name='None', implementer:Object=Ellipsis, feature_state:GameplayTag=Ellipsis)
```


**Bases:** ``StructBase``


Parameters struct for Init State change functions

**C++ Source:**

- **Plugin**: ModularGameplay

- **Module**: ModularGameplay

- **File**: GameFrameworkComponentDelegates.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `feature_name` (Name): [Read-Write] Name of the feature that changed

- `feature_state` (GameplayTag): [Read-Write] The new state of the feature

- `implementer` (Object): [Read-Write] The object (often a component) that implements the feature

- `owning_actor` (Actor): [Read-Write] The actor owning the feature that changed



---

_property_ `feature_name`: Name

[Read-Write] Name of the feature that changed

**Type:**

( Name)


---

_property_ `feature_state`: GameplayTag

[Read-Write] The new state of the feature

**Type:**

( GameplayTag)


---

_property_ `implementer`: Object

[Read-Write] The object (often a component) that implements the feature

**Type:**

( Object)


---

_property_ `owning_actor`: Actor

[Read-Write] The actor owning the feature that changed

**Type:**

( Actor)

### Table of Contents

- `unreal.ActorInitStateChangedParams`
  - `ActorInitStateChangedParams`
    - `ActorInitStateChangedParams.feature_name`
    - `ActorInitStateChangedParams.feature_state`
    - `ActorInitStateChangedParams.implementer`
    - `ActorInitStateChangedParams.owning_actor`