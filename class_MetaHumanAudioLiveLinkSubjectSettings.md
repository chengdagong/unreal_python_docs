# unreal.MetaHumanAudioLiveLinkSubjectSettings

```python
class unreal.MetaHumanAudioLiveLinkSubjectSettings(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MetaHumanAudioBaseLiveLinkSubjectSettings``


MetaHuman Audio Live Link Subject Settings

**C++ Source:**

- **Plugin**: MetaHumanLiveLink

- **Module**: MetaHumanLocalLiveLinkSource

- **File**: MetaHumanAudioLiveLinkSubjectSettings.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write]

- `capture_neutral_frame_countdown` (int32): [Read-Write]

- `capture_neutral_head_pose_countdown` (int32): [Read-Write]

- `capture_neutral_head_translation_countdown` (int32): [Read-Write]
deprecated: CaptureNeutralHeadTranslationCountdown is deprecated. Use CaptureNeutralHeadPoseCountdown instead.

- `capture_neutrals_property` (int32): [Read-Write]

- `fps` (str): [Read-Only] Processing frame rate.

- `frame` (str): [Read-Only] Frame number being processed.

- `frame_rate` (FrameRate): [Read-Only] Last FrameRate estimated by the subject. If in Timecode mode, this will come directly from the QualifiedFrameTime.

- `interpolation_processor` (LiveLinkFrameInterpolationProcessor): [Read-Write] The interpolation processor the subject will use.

- `level` (float): [Read-Only] A very simplistic volume indicator to show if audio is being received - it is not a true audio level monitoring tool.

- `lookahead` (int32): [Read-Write] The amount of time, in milliseconds, that the audio solver looks ahead into the audio stream to produce the current frame of animation. A larger value will produce higher quality animation but will come at the cost of increased latency.

- `mood` (AudioDrivenAnimationMood): [Read-Write]

- `mood_intensity` (float): [Read-Write]

- `neutral_frame` (Array[float]): [Read-Write]

- `neutral_head_orientation` (Rotator): [Read-Write] Head orientation

- `neutral_head_translation` (Vector): [Read-Write] Head translation

- `outbound_name` (str): [Read-Write] Name override that will be transmitted to clients instead of the subject name.

- `parameters` (MetaHumanRealtimeSmoothingParams): [Read-Write] Smoothing

- `pre_processors` (Array[LiveLinkFramePreProcessor]): [Read-Write] List of available preprocessor the subject will use.

- `properties` (Array[Name]): [Read-Write] The properties to calibrate.

- `rebroadcast_subject` (bool): [Read-Write] If enabled, rebroadcast this subject

- `remapper` (LiveLinkSubjectRemapper): [Read-Write] Remapper used to modify incoming static and frame data for a subject.

- `remove` (str): [Read-Only]

- `source` (str): [Read-Only] Source that contains the subject.

- `state` (str): [Read-Only] The state of the processing.

- `state_led` (Color): [Read-Only]

- `subject_name` (str): [Read-Only] Name of this subject.

- `timecode` (str): [Read-Only]

- `translators` (Array[LiveLinkFrameTranslator]): [Read-Write] List of available translator the subject can use.

- `translators_proxy` (LiveLinkFrameTranslator): [Read-Write] Proxy property used edit the translators.


### Table of Contents

- `unreal.MetaHumanAudioLiveLinkSubjectSettings`
  - `MetaHumanAudioLiveLinkSubjectSettings`