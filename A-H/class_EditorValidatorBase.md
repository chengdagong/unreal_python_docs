# unreal.EditorValidatorBase

```python
class unreal.EditorValidatorBase(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


- The EditorValidatorBase is a class which verifies that an asset meets a specific ruleset.

- It should be used when checking engine-level classes, as UObject::IsDataValid requires

- overriding the base class. You can create project-specific version of the validator base,

- with custom logging and enabled logic.

- C++ and Blueprint validators will be gathered on editor start, while python validators need

- to register themselves


**C++ Source:**

- **Plugin**: DataValidation

- **Module**: DataValidation

- **File**: EditorValidatorBase.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `is_enabled` (bool): [Read-Write]

- `only_print_custom_message` (bool): [Read-Write] Whether we should also print out the source validator when printing validation errors.



---

**asset_fails**( _asset_, _message_) → `None`

Marks the validation as failed and adds an error message.

Parameters:

- **asset** ( _Object_)

- **message** ( _Text_)



---

**asset_passes**( _asset_) → `None`

Marks the validation as successful. Failure to call this will report the validator as not having checked the asset.

Parameters:

**asset** ( _Object_)


---

**asset_warning**( _asset_, _message_) → `None`

Adds a message to this validation but doesn’t mark it as failed.

Parameters:

- **asset** ( _Object_)

- **message** ( _Text_)



---

**can_validate**( _usecase:DataValidationUsecase_) → `bool`

deprecated: ‘can\_validate’ was renamed to ‘k2\_can\_validate’.


---

**can_validate_asset**( _asset:Object_) → `bool`

deprecated: ‘can\_validate\_asset’ was renamed to ‘k2\_can\_validate\_asset’.


---

**get_validation_result**() → `DataValidationResult`

Get Validation Result

Return type:

DataValidationResult


---

**k2_can_validate**( _usecase_) → `bool`

Override this to determine whether or not you can use this validator given this usecase

Parameters:

**usecase** ( _DataValidationUsecase_)

Return type:

bool


---

**k2_can_validate_asset**( _asset_) → `bool`

Override this to determine whether or not you can validate a given asset with this validator

Parameters:

**asset** ( _Object_)

Return type:

bool


---

**k2_validate_loaded_asset**( _asset_) → `DataValidationResult`

Override this in blueprint to validate assets

Parameters:

**asset** ( _Object_)

Return type:

DataValidationResult


---

**validate_loaded_asset**( _asset:Object_) → `DataValidationResult`

deprecated: ‘validate\_loaded\_asset’ was renamed to ‘k2\_validate\_loaded\_asset’.

### Table of Contents

- `unreal.EditorValidatorBase`
  - `EditorValidatorBase`
    - `EditorValidatorBase.asset_fails()`
    - `EditorValidatorBase.asset_passes()`
    - `EditorValidatorBase.asset_warning()`
    - `EditorValidatorBase.can_validate()`
    - `EditorValidatorBase.can_validate_asset()`
    - `EditorValidatorBase.get_validation_result()`
    - `EditorValidatorBase.k2_can_validate()`
    - `EditorValidatorBase.k2_can_validate_asset()`
    - `EditorValidatorBase.k2_validate_loaded_asset()`
    - `EditorValidatorBase.validate_loaded_asset()`