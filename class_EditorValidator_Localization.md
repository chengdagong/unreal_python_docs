# unreal.EditorValidator_Localization

```python
class unreal.EditorValidator_Localization(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``EditorValidatorBase``


- Validates that localized assets (within the L10N folder) conform to a corresponding source asset of the correct type.

- Localized assets that fail this validation will never be loaded as localized variants at runtime.


**C++ Source:**

- **Plugin**: DataValidation

- **Module**: DataValidation

- **File**: EditorValidator\_Localization.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `is_enabled` (bool): [Read-Write]

- `only_print_custom_message` (bool): [Read-Write] Whether we should also print out the source validator when printing validation errors.


### Table of Contents

- `unreal.EditorValidator_Localization`
  - `EditorValidator_Localization`