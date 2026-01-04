# unreal.GameplayAbilityTriggerSource

```python
class unreal.GameplayAbilityTriggerSource
```


**Bases:** ``EnumBase``


Defines what type of trigger will activate the ability, paired to a tag

**C++ Source:**

- **Plugin**: GameplayAbilities

- **Module**: GameplayAbilities

- **File**: GameplayAbilityTypes.h


GAMEPLAY\_EVENT _: GameplayAbilityTriggerSource_ _=Ellipsis_

Triggered by an external gameplay event. The ability will receive a GameplayEvent payload.

**Type:**

0

OWNED\_TAG\_ADDED _: GameplayAbilityTriggerSource_ _=Ellipsis_

Triggered when the owner gains the specified tag. Will not cancel when the tag is removed.

**Type:**

1

OWNED\_TAG\_PRESENT _: GameplayAbilityTriggerSource_ _=Ellipsis_

Triggered when the owner has the specified tag. The ability will be canceled if the tag is later removed.

**Type:**

2

### Table of Contents

- `unreal.GameplayAbilityTriggerSource`
  - `GameplayAbilityTriggerSource`
    - `GameplayAbilityTriggerSource.GAMEPLAY_EVENT`
    - `GameplayAbilityTriggerSource.OWNED_TAG_ADDED`
    - `GameplayAbilityTriggerSource.OWNED_TAG_PRESENT`