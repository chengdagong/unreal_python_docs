# unreal.TextToSpeechEngineSubsystem

```python
class unreal.TextToSpeechEngineSubsystem(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``EngineSubsystem``


Subsystem for interacting with the text to speech system via blueprints.
The subsystem consists of a number of text to speech channels associated with a text to speech channel Id.
Each text to speech channel provides text to speech functionality such as vocalizing a string, stopping a vocalized string, controlling the audio settings of the channel and muting/unmuting a channel.
Most of the functions take a text to speech channel Id which allows you to request text to speech functionality on the requested channel.
All newly added text to speech channels start off deactivated and must be activated before any text to speech functionality can be used.

**C++ Source:**

- **Plugin**: TextToSpeech

- **Module**: TextToSpeech

- **File**: TextToSpeechEngineSubsystem.h



---

**activate_all_channels**() → `None`

Activates all text to speech channels to accept requests for text to speech functionality.


---

**activate_channel**( _channel_id_) → `None`

Activates a text to speech channel to accept requests to perform text to speech functionality.
If the provided channel Id does not exist, nothing will happen.

Parameters:

**channel\_id** ( _Name_) – The Id of the channel to activate.


---

**add_custom_channel**( _new_channel_id_) → `None`

Creates a new text to speech channel where text to speech requests are fulfilled by a user implemented C++ text to speech class.
If you have not specified a custom text to speech class to be used, use AddDefaultChannel instead.
This will not add a channel if the channel Id is not unique or if the user has not specified a custom text to speech class to be used in ITextToSpeechModule.
Newly added channels must be activated to use text to speech functionalities.
see: ITextToSpeechModule, AddDefaultChannel, ActivateChannel, ActivateAllChannels

Parameters:

**new\_channel\_id** ( _Name_)


---

**add_default_channel**( _new_channel_id_) → `None`

Creates a new channel for text to speech requests to be made to a platform C++ text to speech class.
This will not create the channel if the provided channel id is not unique.
Newly added channels must be activated to use text to speech functionalities.
For out-of-the-box text to speech support, this is most likely the channel creation method you want.
see: ActivateChannel, ActivateAllChannels

Parameters:

**new\_channel\_id** ( _Name_)


---

**deactivate_all_channels**() → `None`

Deactivates all text to speech channels making all requests for text to speech functionality do nothing.


---

**deactivate_channel**( _channel_id_) → `None`

Deactivates a text to speech channel and stops any vocalized strings on that channel. Future Requests for text to speech functionality will do nothing.
If the provided channel Id does not exist, nothing will happen.

Parameters:

**channel\_id** ( _Name_) – The Id for the channel to deactivate.


---

**does_channel_exist**( _channel_id_) → `bool`

Returns true if a text to speech channel associated with a channel Id exists. Otherwise, the function returns false.

Parameters:

**channel\_id** ( _Name_) – The channel Id to test if it is associated with a channel.

Return type:

bool


---

**get_num_channels**() → `int32`

Returns the number of text to speech channels that have been added.

Return type:

int32


---

**get_rate_on_channel**( _channel_id_) → `float`

Returns the current speech rate strings are vocalized on a text to speech channel. Value is between 0.0 and 1.0.
If the provided channel Id does not exist, 0.0f will be returned.

Parameters:

**channel\_id** ( _Name_) – The Id for the channel to get the speech rate from.

Return type:

float


---

**get_volume_on_channel**( _channel_id_) → `float`

Returns the current volume strings are vocalized on a text to speech channel. Value is between 0.0f and 1.0f.
If the provided channel Id doesn’t exist, 0.0f will be returned.

Parameters:

**channel\_id** ( _Name_) – The Id for the channel to retrieve the volume from.

Return type:

float


---

**is_channel_active**( _channel_id_) → `bool`

Returns true if the text to speech channel is active, otherwise false.

Parameters:

**channel\_id** ( _Name_) – The Id for the channel to check if it is active.

Return type:

bool


---

**is_channel_muted**( _channel_id_) → `bool`

Returns true if the text to speech channel is muted, otherwise false.

Parameters:

**channel\_id** ( _Name_) – The Id for the channel to check if it is muted.

Return type:

bool


---

**is_speaking_on_channel**( _channel_id_) → `bool`

Return true when the targeted text to speech channel is vocalising, otherwise false.

Parameters:

**channel\_id** ( _Name_) – The id of the channel to check if a string is being vocalized.

Return type:

bool


---

**mute_channel**( _channel_id_) → `None`

Mutes a text to speech channel so no vocalized strings are audible on that channel.
If the requested channel is already muted, nothing will happen.

Parameters:

**channel\_id** ( _Name_) – The Id for the channel to mute.


---

**remove_all_channels**() → `None`

Removes all text to speech channels, preventin future requests for text to speech functionality on all channels.


---

**remove_channel**( _channel_id_) → `None`

Removes a text to speech channel, preventing all further requests for text to speech functionality from the channel.
If the provided channel Id does not exist, nothing will happen.

Parameters:

**channel\_id** ( _Name_) – The Id for the channel you want removed.


---

**set_rate_on_channel**( _channel_id_, _rate_) → `None`

Sets the current speech rate strings should be vocalized on a text to speech channel.
If the provided channel does not exist, nothing will happen.

Parameters:

- **channel\_id** ( _Name_) – The Id for the channel to set the speech rate on.

- **rate** ( _float_) – The speech rate to set for the channel. Value will be clamped between 0.0f and 1.0f.



---

**set_volume_on_channel**( _channel_id_, _volume_) → `None`

Sets the volume for strings vocalized on a text to speech channel.
If the provided channel Id does not exist, nothing will happen.

Parameters:

- **channel\_id** ( _Name_) – The Id for the channel to set for.

- **volume** ( _float_) – The volume to be set on the channel. The value will be clamped between 0.0f and 1.0f.



---

**speak_on_channel**( _channel_id_, _string_to_speak_) → `str`

Immediately vocalizes the requested string asynchronously on the requested text to speech channel, interrupting any string that is already being vocalized on the channel.
If the provided channel Id does not exist, nothing will be vocalized.
Before executing this function, a text to speech channel must be added and activated.
To create a platform default text to speech channel, use AddDefaultChannel.
To create a custom text to speech channel with a user-implemented C++ text to speech class, use AddCustomChannel.
This function is not intended for long strings that span multiple sentences or paragraphs.
see: AddDefaultChannel, AddCustomChannel, ActivateChannel, ActivateAllChannels

Parameters:

- **channel\_id** ( _Name_) – The Id of the channel to speak on.

- **string\_to\_speak** ( _str_) – The string to speak on the requested channel.


Returns:

string\_to\_speak (str): The string to speak on the requested channel.

Return type:

str


---

**stop_speaking_on_all_channels**() → `None`

Immediately stops strings from being vocalized on all text to speech channels.


---

**stop_speaking_on_channel**( _channel_id_) → `None`

Immediately stops any currently vocalized string on the channel.
If the provided channel Id does not exist, nothing will happen.

Parameters:

**channel\_id** ( _Name_) – The Id of the channel speech should be stopped on.


---

**unmute_channel**( _channel_id_) → `None`

Unmutes a text to speech channel so vocalized strings are audible on the channel.
If the requested channel is already unmuted, nothing will happen.

Parameters:

**channel\_id** ( _Name_) – The Id for the channel to unmute.

### Table of Contents

- `unreal.TextToSpeechEngineSubsystem`
  - `TextToSpeechEngineSubsystem`
    - `TextToSpeechEngineSubsystem.activate_all_channels()`
    - `TextToSpeechEngineSubsystem.activate_channel()`
    - `TextToSpeechEngineSubsystem.add_custom_channel()`
    - `TextToSpeechEngineSubsystem.add_default_channel()`
    - `TextToSpeechEngineSubsystem.deactivate_all_channels()`
    - `TextToSpeechEngineSubsystem.deactivate_channel()`
    - `TextToSpeechEngineSubsystem.does_channel_exist()`
    - `TextToSpeechEngineSubsystem.get_num_channels()`
    - `TextToSpeechEngineSubsystem.get_rate_on_channel()`
    - `TextToSpeechEngineSubsystem.get_volume_on_channel()`
    - `TextToSpeechEngineSubsystem.is_channel_active()`
    - `TextToSpeechEngineSubsystem.is_channel_muted()`
    - `TextToSpeechEngineSubsystem.is_speaking_on_channel()`
    - `TextToSpeechEngineSubsystem.mute_channel()`
    - `TextToSpeechEngineSubsystem.remove_all_channels()`
    - `TextToSpeechEngineSubsystem.remove_channel()`
    - `TextToSpeechEngineSubsystem.set_rate_on_channel()`
    - `TextToSpeechEngineSubsystem.set_volume_on_channel()`
    - `TextToSpeechEngineSubsystem.speak_on_channel()`
    - `TextToSpeechEngineSubsystem.stop_speaking_on_all_channels()`
    - `TextToSpeechEngineSubsystem.stop_speaking_on_channel()`
    - `TextToSpeechEngineSubsystem.unmute_channel()`