# unreal.MovieSceneEvent

```python
class unreal.MovieSceneEvent
```


**Bases:** ``StructBase``


Movie Scene Event

**C++ Source:**

- **Module**: MovieSceneTracks

- **File**: MovieSceneEvent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bound_object_pin_name` (Name): [Read-Write]

- `payload_variables` (Map[Name, MovieSceneEventPayloadVariable]): [Read-Write] Array of payload variables to be added to the generated function

- `weak_endpoint` (Object): [Read-Write] Serialized weak pointer to the function entry (UK2Node\_FunctionEntry) or custom event node (UK2Node\_CustomEvent) within the blueprint graph for this event. Stored as an editor-only UObject so UHT can parse it when building for non-editor.


get\_bound\_object\_property\_class()

- Return the class of the bound object property


Returns:

The class of the bound object property

Return type:

type( Class)

### Table of Contents

- `unreal.MovieSceneEvent`
  - `MovieSceneEvent`
    - `MovieSceneEvent.get_bound_object_property_class()`