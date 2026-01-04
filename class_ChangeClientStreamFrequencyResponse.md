# unreal.ChangeClientStreamFrequencyResponse

```python
class unreal.ChangeClientStreamFrequencyResponse(object_errors:None={}, default_change_error_code:type=())
```


**Bases:** ``StructBase``


Result about changing frequency.

**C++ Source:**

- **Plugin**: MultiUserClient

- **Module**: MultiUserClientLibrary

- **File**: ChangeClientBlueprintParams.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `default_change_error_code` (‘undefined’): [Read-Write] Error for changing the default replication frequency.

- `object_errors` (Map[SoftObjectPath, MultiUserChangeFrequencyErrorCode]): [Read-Write] Errors encountered for specific objects



---

_property_ `default_change_error_code`: type

[Read-Only] Error for changing the default replication frequency.

**Type:**

(‘undefined’)


---

_property_ `object_errors`: None

[Read-Only] Errors encountered for specific objects

**Type:**

( Map\ [SoftObjectPath, MultiUserChangeFrequencyErrorCode])

### Table of Contents

- `unreal.ChangeClientStreamFrequencyResponse`
  - `ChangeClientStreamFrequencyResponse`
    - `ChangeClientStreamFrequencyResponse.default_change_error_code`
    - `ChangeClientStreamFrequencyResponse.object_errors`