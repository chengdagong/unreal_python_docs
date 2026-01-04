# unreal.Text

```python
class unreal.Text(value:Text | str='')
```


**Bases:** ``_WrapperBase``


Type for all Unreal exposed text instances


---

_classmethod_ as_currency( _cls_, _val:int_, _code:str_)→Text--convertthegivennumber(specifiedinthesmallestunitforthegivencurrencyi.e.650for$6.50)toaculturecorrectUnrealtextcurrencyrepresentation_classmethod_ as_number( _cls_, _num:float_)→Text--convertthegivennumbertoaculturecorrectUnrealtextrepresentation_classmethod_ as_percent( _cls_, _num:float_)→Text--convertthegivennumbertoaculturecorrectUnrealtextpercentgagerepresentation_classmethod_ cast( _cls_, _object:object_)→Text--castthegivenobjecttothisUnrealtexttypeformat( _self,\*args:Union[Mapping[str,object],object],\*\*named_args:object)->Text--usethisUnrealtextasaformatpatternandgenerateanewtextusingtheformatarguments(maybeamapping[arg_name,arg]orcommasepared(optionallynamed)arguments_)is_culture_invariant( _self_)→bool--isthisUnrealtextcultureinvariant?is_empty( _self_)→bool--isthisUnrealtextempty?is_empty_or_whitespace( _self_)→bool--isthisUnrealtextemptyoronlywhitespace?is_from_string_table( _self_)→bool--isthisUnrealtextreferencingastringtableentry?is_transient( _self_)→bool--isthisUnrealtexttransient?to_lower( _self_)→Text--convertthisUnrealtexttolowercaseinaculturecorrectwayto_upper( _self_)→Text--convertthisUnrealtexttouppercaseinaculturecorrectway

### Table of Contents

- `unreal.Text`
  - `Text`
    - `Text.as_currency()`
    - `Text.as_number()`
    - `Text.as_percent()`
    - `Text.cast()`
    - `Text.format()`
    - `Text.is_culture_invariant()`
    - `Text.is_empty()`
    - `Text.is_empty_or_whitespace()`
    - `Text.is_from_string_table()`
    - `Text.is_transient()`
    - `Text.to_lower()`
    - `Text.to_upper()`