# unreal.ScopedEditorTransaction

```python
class unreal.ScopedEditorTransaction(desc:Text | str)
```


**Bases:** ``object``


Type used to create and managed a scoped editor transaction in Python


---

**__enter__**( _self_)→ScopedEditorTransaction--beginthistransaction__exit__(_self_, _type:Type[BaseException]| None_, _value:BaseException| None_, _traceback:TracebackType| None_)→bool--endthistransactioncancel(_self_) → `None--cancelthistransaction`

### Table of Contents

- `unreal.ScopedEditorTransaction`
  - `ScopedEditorTransaction`
    - `ScopedEditorTransaction.__enter__()`
    - `ScopedEditorTransaction.__exit__()`
    - `ScopedEditorTransaction.cancel()`