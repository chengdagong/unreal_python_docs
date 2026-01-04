# unreal.MaterialAggregate

```python
class unreal.MaterialAggregate(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``DataAsset``


It defines a collection of arithmetic material values to be bundled together.
A material aggregate works similarly to a struct in C/C++. Each attribute has a name and specifies a type, either a
primitive one like float4 or another aggregate (for nested structures).

**C++ Source:**

- **Module**: Engine

- **File**: MaterialAggregate.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `attributes` (Array[MaterialAggregateAttribute]): [Read-Write] List of material aggregate attributes.


### Table of Contents

- `unreal.MaterialAggregate`
  - `MaterialAggregate`