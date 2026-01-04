# unreal.DataprepRecipe

```python
class unreal.DataprepRecipe(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Dataprep Recipe

**C++ Source:**

- **Plugin**: DataprepEditor

- **Module**: DataprepCore

- **File**: DataprepRecipe.h



---

**get_actors**() → `Array\ [Actor]`

DEPRECATED
Returns all actors contained in its attached world
deprecated: No use of Blueprint with Dataprep.

Return type:

Array\ [Actor]


---

**get_assets**() → `Array\ [Object]`

DEPRECATED
Returns all valid assets contained in attached world
deprecated: No use of Blueprint with Dataprep.

Return type:

Array\ [Object]


---

**trigger_pipeline_traversal**() → `None`

DEPRECATED
Function used to trigger the execution of the pipeline
An event node associated to this function must be in the pipeline graph to run it.
deprecated: No use of Blueprint with Dataprep.

### Table of Contents

- `unreal.DataprepRecipe`
  - `DataprepRecipe`
    - `DataprepRecipe.get_actors()`
    - `DataprepRecipe.get_assets()`
    - `DataprepRecipe.trigger_pipeline_traversal()`