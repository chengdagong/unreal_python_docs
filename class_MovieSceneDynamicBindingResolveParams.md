# unreal.MovieSceneDynamicBindingResolveParams

```python
class unreal.MovieSceneDynamicBindingResolveParams(sequence:MovieSceneSequence=Ellipsis, object_binding_id:Guid=\[\], root_sequence:MovieSceneSequence=Ellipsis)
```


**Bases:** ``StructBase``


Optional parameter struct for dynamic binding resolver functions.

**C++ Source:**

- **Module**: MovieScene

- **File**: MovieSceneDynamicBinding.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `object_binding_id` (Guid): [Read-Write] The ID of the object binding being resolved

- `root_sequence` (MovieSceneSequence): [Read-Write] The root sequence

- `sequence` (MovieSceneSequence): [Read-Write] The sequence that contains the object binding being resolved



---

_property_ `object_binding_id`: Guid

[Read-Write] The ID of the object binding being resolved

**Type:**

( Guid)


---

_property_ `root_sequence`: MovieSceneSequence

[Read-Write] The root sequence

**Type:**

( MovieSceneSequence)


---

_property_ `sequence`: MovieSceneSequence

[Read-Write] The sequence that contains the object binding being resolved

**Type:**

( MovieSceneSequence)

### Table of Contents

- `unreal.MovieSceneDynamicBindingResolveParams`
  - `MovieSceneDynamicBindingResolveParams`
    - `MovieSceneDynamicBindingResolveParams.object_binding_id`
    - `MovieSceneDynamicBindingResolveParams.root_sequence`
    - `MovieSceneDynamicBindingResolveParams.sequence`