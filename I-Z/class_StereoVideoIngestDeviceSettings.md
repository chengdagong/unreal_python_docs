# unreal.StereoVideoIngestDeviceSettings

```python
class unreal.StereoVideoIngestDeviceSettings(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``LiveLinkDeviceSettings``


Stereo Video Ingest Device Settings

**C++ Source:**

- **Plugin**: CaptureManagerDevices

- **Module**: StereoVideoIngestDevice

- **File**: StereoVideoIngestDevice.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `audio_discovery_expression` (TakeDiscoveryExpression): [Read-Write] Format of the file name that the device expectsAvailable expressions:

- <Slate> - slate name

- <Name> - identifier for the camera in the stereo pair

- <Take> - take number

- <Any> - any string

- <Auto> - used alone to automatically figure out takes based on directory structure


Available delimiters: ‘\_’, ‘-’, ‘.’, ‘'

Examples:
Considering input audio MyTakeFolder/MySlate\_MyName\_SomeString-005.wav

Audio File Name Pattern <Auto> - will set Slate to the containing folder “MyTakeFolder”, Name will be set to the audio filename “MySlate\_MyName\_SomeString-005” and Take will be set to 1 by default

Audio File Name Pattern <Slate>\_<Name>\_<Any>-<Take> - will extract Slate as “MySlate”, Name as “MyName” and Take as 5. <Any> ensures that the “SomeString” part of the filename is ignored.

In both cases, extension ‘.wav’ is stripped out.

Note: when not using <Auto> expression, then both <Slate> and <Name> must be present in the pattern

- `display_name` (str): [Read-Write]

- `take_directory` (DirectoryPath): [Read-Write] Path to a directory containing the take(s) data

- `video_discovery_expression` (TakeDiscoveryExpression): [Read-Write] Format of the file name that the device expectsAvailable expressions:

- <Slate> - slate name

- <Name> - identifier for the camera in the stereo pair

- <Take> - take number

- <Any> - any string

- <Auto> - used alone to automatically figure out takes based on directory structure


Available delimiters: ‘\_’, ‘-’, ‘.’, ‘'

Examples:
Considering input video MyTakeFolder/MySlate\_MyName\_SomeString-005.mov

Video File Name Pattern <Auto> - will set Slate to the containing folder “MyTakeFolder”, Name will be set to the video filename “MySlate\_MyName\_SomeString-005” and Take will be set to 1 by default

Video File Name Pattern <Slate>\_<Name>\_<Any>-<Take> - will extract Slate as “MySlate”, Name as “MyName” and Take as 5. <Any> ensures that the “SomeString” part of the filename is ignored.

In both cases, extension ‘.mov’ is stripped out.

Note: when not using <Auto> expression, then both <Slate> and <Name> must be present in the pattern


---

_property_ `audio_discovery_expression`: TakeDiscoveryExpression

- <Slate> - slate name

- <Name> - identifier for the camera in the stereo pair

- <Take> - take number

- <Any> - any string

- <Auto> - used alone to automatically figure out takes based on directory structure


Available delimiters: ‘\_’, ‘-’, ‘.’, ‘'

Examples:
Considering input audio MyTakeFolder/MySlate\_MyName\_SomeString-005.wav

Audio File Name Pattern <Auto> - will set Slate to the containing folder “MyTakeFolder”, Name will be set to the audio filename “MySlate\_MyName\_SomeString-005” and Take will be set to 1 by default

Audio File Name Pattern <Slate>\_<Name>\_<Any>-<Take> - will extract Slate as “MySlate”, Name as “MyName” and Take as 5. <Any> ensures that the “SomeString” part of the filename is ignored.

In both cases, extension ‘.wav’ is stripped out.

Note: when not using <Auto> expression, then both <Slate> and <Name> must be present in the pattern

**Type:**

( TakeDiscoveryExpression)


---

_property_ `display_name`: str

[Read-Write]

**Type:**

( str)


---

_property_ `take_directory`: DirectoryPath

[Read-Write] Path to a directory containing the take(s) data

**Type:**

( DirectoryPath)


---

_property_ `video_discovery_expression`: TakeDiscoveryExpression

- <Slate> - slate name

- <Name> - identifier for the camera in the stereo pair

- <Take> - take number

- <Any> - any string

- <Auto> - used alone to automatically figure out takes based on directory structure


Available delimiters: ‘\_’, ‘-’, ‘.’, ‘'

Examples:
Considering input video MyTakeFolder/MySlate\_MyName\_SomeString-005.mov

Video File Name Pattern <Auto> - will set Slate to the containing folder “MyTakeFolder”, Name will be set to the video filename “MySlate\_MyName\_SomeString-005” and Take will be set to 1 by default

Video File Name Pattern <Slate>\_<Name>\_<Any>-<Take> - will extract Slate as “MySlate”, Name as “MyName” and Take as 5. <Any> ensures that the “SomeString” part of the filename is ignored.

In both cases, extension ‘.mov’ is stripped out.

Note: when not using <Auto> expression, then both <Slate> and <Name> must be present in the pattern

**Type:**

( TakeDiscoveryExpression)

### Table of Contents

- `unreal.StereoVideoIngestDeviceSettings`
  - `StereoVideoIngestDeviceSettings`
    - `StereoVideoIngestDeviceSettings.audio_discovery_expression`
    - `StereoVideoIngestDeviceSettings.display_name`
    - `StereoVideoIngestDeviceSettings.take_directory`
    - `StereoVideoIngestDeviceSettings.video_discovery_expression`