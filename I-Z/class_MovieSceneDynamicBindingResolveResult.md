# unreal.MovieSceneDynamicBindingResolveResult

```python
class unreal.MovieSceneDynamicBindingResolveResult(objects:None=\[\], is_possessed_object:bool=False)
```


**Bases:** ``StructBase``


Movie Scene Dynamic Binding Resolve Result

**C++ Source:**

- **Module**: MovieScene

- **File**: MovieSceneDynamicBinding.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `is_possessed_object` (bool): [Read-Write] Whether the resolved object is external to the sequence

This property is ignored for possessables, who are always treated as external.
When resolving a spawnable, setting this to true will not destroy the object
when the spawnable track ends, or the sequence finishes.

- `object` (Object): [Read-Write]
deprecated: This property is deprecated, please use the array of Objects instead.

- `objects` (Array[Object]): [Read-Write] The resolved objects



---

_property_ `is_possessed_object`: bool

[Read-Write] Whether the resolved object is external to the sequence

This property is ignored for possessables, who are always treated as external.
When resolving a spawnable, setting this to true will not destroy the object
when the spawnable track ends, or the sequence finishes.

**Type:**

( bool)


---

_property_ `object`: Object

[Read-Write]
deprecated: This property is deprecated, please use the array of Objects instead.

**Type:**

( Object)


---

_property_ `objects`: None

[Read-Write] The resolved objects

**Type:**

( Array\ [Object])

### Table of Contents

- `unreal.MovieSceneDynamicBindingResolveResult`
  - `MovieSceneDynamicBindingResolveResult`
    - `MovieSceneDynamicBindingResolveResult.is_possessed_object`
    - `MovieSceneDynamicBindingResolveResult.object`
    - `MovieSceneDynamicBindingResolveResult.objects`