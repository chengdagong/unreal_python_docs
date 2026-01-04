# unreal.ScopedSlowTask

```python
class unreal.ScopedSlowTask(work:float, desc:Text | str='', enabled:bool=True)
```


**Bases:** ``object``


Type used to create and managed a scoped slow task in Python


---

**__enter__**( _self_)→ScopedSlowTask--beginthisslowtask__exit__(_self_, _type:Type[BaseException]| None_, _value:BaseException| None_, _traceback:TracebackType| None_)→bool--endthisslowtaskenter_progress_frame(_self_, _work:float=1.0_, _desc:Union[Text_, _str]="")->None--indicatethatwearetoenteraframethatwilltakeupthespecifiedamountofwork(completesanypreviousframes_)make_dialog(_self_, _can_cancel:bool=False_, _allow_in_pie:bool=False_)→None--createsanewdialogforthisslowtask, ifthereiscurrentlynotoneopenmake_dialog_delayed(_self_, _delay:float_, _can_cancel:bool=False_, _allow_in_pie:bool=False_)→None--createsanewdialogforthisslowtaskafterthegiventimedelay(inseconds).Ifthetaskcompletesbeforethistime, nodialogwillbeshownshould_cancel(_self_)→bool--Trueiftheuserhasrequestedthattheslowtaskbecanceledtick_progress(_self_) → `None--LettheUIrefreshbutdoesn'tadvanceprogress`

### Table of Contents

- `unreal.ScopedSlowTask`
  - `ScopedSlowTask`
    - `ScopedSlowTask.__enter__()`
    - `ScopedSlowTask.__exit__()`
    - `ScopedSlowTask.enter_progress_frame()`
    - `ScopedSlowTask.make_dialog()`
    - `ScopedSlowTask.make_dialog_delayed()`
    - `ScopedSlowTask.should_cancel()`
    - `ScopedSlowTask.tick_progress()`