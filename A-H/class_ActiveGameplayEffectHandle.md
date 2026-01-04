# unreal.ActiveGameplayEffectHandle

```python
class unreal.ActiveGameplayEffectHandle
```


**Bases:** ``StructBase``


This handle is required for things outside of FActiveGameplayEffectsContainer to refer to a specific active GameplayEffect

For example if a skill needs to create an active effect and then destroy that specific effect that it created, it has to do so
through a handle. a pointer or index into the active list is not sufficient. These are not synchronized between clients and server.

**C++ Source:**

- **Plugin**: GameplayAbilities

- **Module**: GameplayAbilities

- **File**: ActiveGameplayEffectHandle.h



---

**__eq__**( _other:object_) → `bool`

**Overloads:**

- `ActiveGameplayEffectHandle` Equality operator for two Active Gameplay Effect Handles



---

**__ne__**( _other:object_) → `bool`

**Overloads:**

- `ActiveGameplayEffectHandle` Inequality operator for two Active Gameplay Effect Handles


### Table of Contents

- `unreal.ActiveGameplayEffectHandle`
  - `ActiveGameplayEffectHandle`
    - `ActiveGameplayEffectHandle.__eq__()`
    - `ActiveGameplayEffectHandle.__ne__()`