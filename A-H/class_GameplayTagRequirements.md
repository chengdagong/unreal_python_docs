# unreal.GameplayTagRequirements

```python
class unreal.GameplayTagRequirements(require_tags:GameplayTagContainer=Ellipsis, ignore_tags:GameplayTagContainer=Ellipsis, tag_query:GameplayTagQuery=\[\])
```


**Bases:** ``StructBase``


Encapsulate require and ignore tags

**C++ Source:**

- **Plugin**: GameplayAbilities

- **Module**: GameplayAbilities

- **File**: GameplayEffectTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `ignore_tags` (GameplayTagContainer): [Read-Write] None of these tags may be present

- `require_tags` (GameplayTagContainer): [Read-Write] All of these tags must be present

- `tag_query` (GameplayTagQuery): [Read-Write] Build up a more complex query that can’t be expressed with RequireTags/IgnoreTags alone



---

_property_ `ignore_tags`: GameplayTagContainer

[Read-Write] None of these tags may be present

**Type:**

( GameplayTagContainer)


---

_property_ `require_tags`: GameplayTagContainer

[Read-Write] All of these tags must be present

**Type:**

( GameplayTagContainer)


---

_property_ `tag_query`: GameplayTagQuery

[Read-Write] Build up a more complex query that can’t be expressed with RequireTags/IgnoreTags alone

**Type:**

( GameplayTagQuery)

### Table of Contents

- `unreal.GameplayTagRequirements`
  - `GameplayTagRequirements`
    - `GameplayTagRequirements.ignore_tags`
    - `GameplayTagRequirements.require_tags`
    - `GameplayTagRequirements.tag_query`