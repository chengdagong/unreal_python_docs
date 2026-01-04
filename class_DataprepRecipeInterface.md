# unreal.DataprepRecipeInterface

```python
class unreal.DataprepRecipeInterface(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


A DataprepAssetInterface is composed of a set of producers, inputs, a consumer, output,
and a recipe, set of actions. The producers generate assets and populate a given world.
The pipeline modifies the assets and the actors of the given world. Finally, the consumer
converts the assets and the given world. An FBX exporter is a possible consumer.
This class is an abstract modeling the data preparation pipeline.

**C++ Source:**

- **Plugin**: DataprepEditor

- **Module**: DataprepCore

- **File**: DataprepAssetInterface.h


### Table of Contents

- `unreal.DataprepRecipeInterface`
  - `DataprepRecipeInterface`