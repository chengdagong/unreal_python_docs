# Unreal Python Module

This module contains functions and decorators for interacting with the Unreal Engine Python API.

## Decorators and Type Definitions

### `unreal.uclass`

```python
unreal.uclass()
```

Decorator used to define `UClass` types from Python.

### `unreal.uenum`

```python
unreal.uenum()
```

Decorator used to define `UEnum` types from Python.

### `unreal.ufunction`

```python
unreal.ufunction(meta=None, ret=None, params=None, override=None, static=None, pure=None, getter=None, setter=None)
```

Decorator used to define `UFunction` fields from Python.

### `unreal.uproperty`

```python
unreal.uproperty(type, meta=None, getter=None, setter=None)
```

Function used to define `UProperty` fields from Python.

### `unreal.ustruct`

```python
unreal.ustruct()
```

Decorator used to define `UStruct` types from Python.

### `unreal.uvalue`

```python
unreal.uvalue(val, meta=None)
```

Function used to define constant values from Python.

---

## Functions

### `unreal._redirect_warning`

```python
unreal._redirect_warning(message, category, filename, lineno, file=None, line=None)
```

### `unreal.collect_garbage`

```python
unreal.collect_garbage() -> None
```

Run Unreal garbage collection.

### `unreal.create_python_object_handle`

```python
unreal.create_python_object_handle(obj: Any | None) -> Optional[PythonObjectHandle]
```

Create a `PythonObjectHandle` from the given `PyObject`.

### `unreal.destroy_python_object_handle`

```python
unreal.destroy_python_object_handle(handle: Optional[PythonObjectHandle])
```

Destroy a `PythonObjectHandle` (clearing its `PyObject` reference).

### `unreal.find_asset`

```python
unreal.find_asset(name: str, type: Class | type = Object.static_class(), follow_redirectors: bool = True) -> Any
```

Find an already loaded Unreal asset with the given name, optionally validating its type.

### `unreal.find_object`

```python
unreal.find_object(outer: Object | None, name: str, type: Class | type = Object.static_class(), follow_redirectors: bool = True) -> Any
```

Find an already loaded Unreal object with the given outer and name, optionally validating its type.

### `unreal.find_package`

```python
unreal.find_package(name: str) -> Optional[Package]
```

Find an already loaded Unreal package with the given name.

### `unreal.flush_generated_type_reinstancing`

```python
unreal.flush_generated_type_reinstancing() -> None
```

Flush any pending reinstancing requests for Python generated types.

### `unreal.generate_class`

```python
unreal.generate_class(class_type: type) -> None
```

Generate an Unreal class for the given Python type.

### `unreal.generate_enum`

```python
unreal.generate_enum(enum_type: type) -> None
```

Generate an Unreal enum for the given Python type.

### `unreal.generate_struct`

```python
unreal.generate_struct(struct_type: type) -> None
```

Generate an Unreal struct for the given Python type.

### `unreal.get_blueprint_generated_types`

```python
unreal.get_blueprint_generated_types(paths: Iterable[str]) -> Optional[Union[type, Tuple[type, ...]]]
```

Get the Python types (will return a tuple for multiple types) for the given set of Blueprint asset paths (may be a sequence type or set of arguments).

### `unreal.get_default_object`

```python
unreal.get_default_object(type: Class | type) -> Any
```

Get the Unreal class default object (CDO) of the given type.

### `unreal.get_editor_subsystem`

```python
unreal.get_editor_subsystem(subsystem: Class | type[_EditorSubsystemTypeVar]) -> Optional[_EditorSubsystemTypeVar]
```

Returns the requested Editor subsystem or `None`.

### `unreal.get_engine_subsystem`

```python
unreal.get_engine_subsystem(subsystem: Class | type[_EngineSubsystemTypeVar]) -> Optional[_EngineSubsystemTypeVar]
```

Returns the requested Engine subsystem or `None`.

### `unreal.get_interpreter_executable_path`

```python
unreal.get_interpreter_executable_path() -> str
```

Get the path to the Python interpreter executable of the Python SDK this plugin was compiled against.

### `unreal.get_type_from_class`

```python
unreal.get_type_from_class(class_: Class) -> type
```

Get the best matching Python type for the given Unreal class.

### `unreal.get_type_from_enum`

```python
unreal.get_type_from_enum(enum: Enum) -> type
```

Get the best matching Python type for the given Unreal enum.

### `unreal.get_type_from_struct`

```python
unreal.get_type_from_struct(struct: Struct) -> type
```

Get the best matching Python type for the given Unreal struct.

### `unreal.is_editor`

```python
unreal.is_editor() -> bool
```

Tells if the editor is running or not.

### `unreal.load_asset`

```python
unreal.load_asset(name: str, type: Class | type = Object.static_class(), follow_redirectors: bool = True) -> Any
```

Load an Unreal asset with the given name, optionally validating its type.

### `unreal.load_class`

```python
unreal.load_class(outer: Object | None, name: str, type: Class | type = Object.static_class()) -> Optional[Class]
```

Load an Unreal class with the given outer and name, optionally validating its base type.

### `unreal.load_module`

```python
unreal.load_module(module: str) -> None
```

Load the given Unreal module and generate any Python code for its reflected types.

### `unreal.load_object`

```python
unreal.load_object(outer: Object | None, name: str, type: Class | type = Object.static_class(), follow_redirectors: bool = True) -> Any
```

Load an Unreal object with the given outer and name, optionally validating its type.

### `unreal.load_package`

```python
unreal.load_package(name: str) -> Optional[Package]
```

Load an Unreal package with the given name.

### `unreal.LOCTABLE`

```python
unreal.LOCTABLE(id: Name | str, key: str) -> Text
```

Get a localized Text from the given string table id and key.

### `unreal.log`

```python
unreal.log(arg: Any) -> None
```

Log the given argument as information in the `LogPython` category.

### `unreal.log_error`

```python
unreal.log_error(arg: Any) -> None
```

Log the given argument as an error in the `LogPython` category.

### `unreal.log_flush`

```python
unreal.log_flush() -> None
```

Flush the log to disk.

### `unreal.log_warning`

```python
unreal.log_warning(arg: Any) -> None
```

Log the given argument as a warning in the `LogPython` category.

### `unreal.new_object`

```python
unreal.new_object(type: Class | type, outer: Object | None = None, name: Name | str = '', base_type: Object | None = None) -> Any
```

Create an Unreal object of the given class (and optional outer and name), optionally validating its type.

### `unreal.NSLOCTEXT`

```python
unreal.NSLOCTEXT(ns: str, key: str, source: str) -> Text
```

Create a localized Text from the given namespace, key, and source string.

### `unreal.parent_external_window_to_slate`

```python
unreal.parent_external_window_to_slate(external_window_handle: object, parent_search_method: SlateParentWindowSearchMethod = SlateParentWindowSearchMethod.ACTIVE_WINDOW) -> None
```

Parent the given OS specific external window handle to a suitable Slate window.

### `unreal.purge_object_references`

```python
unreal.purge_object_references(obj: Object, include_inners: bool = True) -> None
```

Purge all references to the given Unreal object from any living Python objects.

### `unreal.register_python_shutdown_callback`

```python
unreal.register_python_shutdown_callback(callable: Callable[[], None]) -> object
```

Register the given callable (with no input arguments) as a callback to execute immediately before Python shutdown.

### `unreal.register_slate_post_tick_callback`

```python
unreal.register_slate_post_tick_callback(callable: Callable[[float], None] | DelegateBase) -> object
```

Register the given callable (taking a single float) as a pre-tick callback in Slate.

### `unreal.register_slate_pre_tick_callback`

```python
unreal.register_slate_pre_tick_callback(callable: Callable[[float], None] | DelegateBase) -> object
```

Register the given callable (taking a single float) as a pre-tick callback in Slate.

### `unreal.register_ticker_callback`

```python
unreal.register_ticker_callback(callable: Callable[[float], bool] | DelegateBase, delay: float = 0.0) -> object
```

Register the given callable (taking a single float and returning a bool where true will continue ticking) as a ticker callback in `FTSTicker`, to run at most every `delay` seconds.

### `unreal.reload`

```python
unreal.reload(module: str) -> None
```

Reload the given Unreal Python module.

### `unreal.resolve_python_object_handle`

```python
unreal.resolve_python_object_handle(handle: PythonObjectHandle | None) -> Optional[Any]
```

Resolve a `PythonObjectHandle` to its `PyObject`, or `None`.

### `unreal.unregister_python_shutdown_callback`

```python
unreal.unregister_python_shutdown_callback(handle: object) -> None
```

Unregister the given handle from a previous call to `register_python_shutdown_callback`.

### `unreal.unregister_slate_post_tick_callback`

```python
unreal.unregister_slate_post_tick_callback(handle: object) -> None
```

Unregister the given handle from a previous call to `register_slate_post_tick_callback`.

### `unreal.unregister_slate_pre_tick_callback`

```python
unreal.unregister_slate_pre_tick_callback(handle: object) -> None
```

Unregister the given handle from a previous call to `register_slate_pre_tick_callback`.

### `unreal.unregister_ticker_callback`

```python
unreal.unregister_ticker_callback(handle: object) -> None
```

Unregister the given handle from a previous call to `register_ticker_callback`.
