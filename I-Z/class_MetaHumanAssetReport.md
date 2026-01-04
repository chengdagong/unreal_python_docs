# unreal.MetaHumanAssetReport

```python
class unreal.MetaHumanAssetReport(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


A report generated when an asset is imported or tested for MetaHuman compatibility

**C++ Source:**

- **Plugin**: MetaHumanSDK

- **Module**: MetaHumanSDKEditor

- **File**: MetaHumanAssetReport.h



---

**add_error**( _message_) → `None`

Adds a user-facing message to appear in the report. This will flag the report as containing warnings and as
having failed.

Parameters:

**message** ( _MetaHumanAssetReportItem_) – The localized error message


---

**add_info**( _message_) → `None`

Adds a user-facing message to appear in the report. This will not flag the report as containing warnings or as
having failed.

Parameters:

**message** ( _MetaHumanAssetReportItem_) – The localized informational message


---

**add_verbose**( _message_) → `None`

Adds a user-facing message to appear in the report. This will not flag the report as containing warnings or as
having failed and will be discarded if SetVerbose is not called with a value of true

Parameters:

**message** ( _MetaHumanAssetReportItem_) – The localized informational message


---

**add_warning**( _message_) → `None`

Adds a user-facing message to appear in the report. This will flag the report as containing warnings but will
not flag it as having failed.

Parameters:

**message** ( _MetaHumanAssetReportItem_) – The localized warning message


---

**generate_html_report**() → `str`

Generates an HTML representation of the report

Return type:

str


---

**generate_json_report**() → `str`

Generates a JSON representation of the report

Return type:

str


---

**generate_raw_report**() → `str`

Generates a plain text representation of the report

Return type:

str


---

**generate_rich_text_report**() → `Text`

Generates a representation of the report suitable for use in an SRichText control

Return type:

Text


---

**get_report_result**() → `MetaHumanOperationResult`

Determine whether the report represents a successful operation or not

Return type:

MetaHumanOperationResult


---

**has_warnings**() → `bool`

Determine whether the report contains non-informational messages

Return type:

bool


---

**set_silent**( _value_) → `None`

Suppress logging of messages from the report

Parameters:

**value** ( _bool_)


---

**set_subject**( _subject_) → `None`

Set the subject for the report, typically the name of the asset being tested or imported

Parameters:

**subject** ( _str_) – The Name to appear in the title of the report


---

**set_verbose**( _value_) → `None`

Set whether to include verbose items in the report

Parameters:

**value** ( _bool_)


---

**set_warnings_as_errors**( _value_) → `None`

Set whether warnings should be reported as errors

Parameters:

**value** ( _bool_)

### Table of Contents

- `unreal.MetaHumanAssetReport`
  - `MetaHumanAssetReport`
    - `MetaHumanAssetReport.add_error()`
    - `MetaHumanAssetReport.add_info()`
    - `MetaHumanAssetReport.add_verbose()`
    - `MetaHumanAssetReport.add_warning()`
    - `MetaHumanAssetReport.generate_html_report()`
    - `MetaHumanAssetReport.generate_json_report()`
    - `MetaHumanAssetReport.generate_raw_report()`
    - `MetaHumanAssetReport.generate_rich_text_report()`
    - `MetaHumanAssetReport.get_report_result()`
    - `MetaHumanAssetReport.has_warnings()`
    - `MetaHumanAssetReport.set_silent()`
    - `MetaHumanAssetReport.set_subject()`
    - `MetaHumanAssetReport.set_verbose()`
    - `MetaHumanAssetReport.set_warnings_as_errors()`