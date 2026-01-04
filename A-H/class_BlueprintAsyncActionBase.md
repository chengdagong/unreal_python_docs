# unreal.BlueprintAsyncActionBase

```python
class unreal.BlueprintAsyncActionBase(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


BlueprintCallable factory functions for classes which inherit from UBlueprintAsyncActionBase will have a special blueprint node created for it: UK2Node\_AsyncAction
You can stop this node spawning and create a more specific one by adding the UCLASS metadata “HasDedicatedAsyncNode”

**C++ Source:**

- **Module**: Engine

- **File**: BlueprintAsyncActionBase.h


### Table of Contents

- `unreal.BlueprintAsyncActionBase`
  - `BlueprintAsyncActionBase`