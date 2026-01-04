# unreal.ActorActionUtility

```python
class unreal.ActorActionUtility(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``EditorUtilityObject``


Base class for all actor action-related utilities
Any functions/events that are exposed on derived classes that have the correct signature will be
included as menu options when right-clicking on a group of actors in the level editor.

**C++ Source:**

- **Module**: Blutility

- **File**: ActorActionUtility.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `run_editor_utility_on_startup` (bool): [Read-Write] Run this editor utility on start-up (after asset discovery)?

- `supported_classes` (Array[Class]): [Read-Write] For simple Asset Action’s you should fill out the supported class here.


get\_supported\_class()

Get Supported Class
deprecated: If you were just returning a single class add it to the SupportedClasses array (you can find it listed in the Class Defaults). If you were doing complex logic to simulate having multiple classes act as filters, add them to the SupportedClasses array. If you were doing ‘other’ logic, you’ll need to do that upon action execution.

Return type:

type( Class)


---

**get_supported_classes**() → `Array\ [Class]`

Gets the statically determined supported classes, these classes are used as a first pass filter when determining
if we can utilize this asset utility action on the asset.

Return type:

Array\ [Class]

### Table of Contents

- `unreal.ActorActionUtility`
  - `ActorActionUtility`
    - `ActorActionUtility.get_supported_class()`
    - `ActorActionUtility.get_supported_classes()`