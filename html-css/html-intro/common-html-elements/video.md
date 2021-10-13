# Video

## Video Element - \<video>

{% hint style="info" %}
The img element is not a self-closing element. You can supply text as the content of the video element, which will be display if the video does not display for some reason.
{% endhint %}

### Attributes

| Attribute    | Description                                                                                |
| ------------ | ------------------------------------------------------------------------------------------ |
|              | Embeds a video in the document                                                             |
| **src**      | The value of the src attribute can be a path to a local video or an URL to a remote video. |
| **alt**      | An alternative to identify the content of the video for screen readers.                    |
| **controls** | whether the control panel is visible                                                       |
| **autoplay** | whether it starts automatically                                                            |
| **muted**    | whether the audio is muted by default                                                      |
| **loop**     | whether the video plays in a loop                                                          |

The video element also has a src attribute, which is used to specify the location of the video. There are a couple of additional attributes that need to be set to control the video. These are a special kind of attribute, called boolean attributes.

### Boolean Attributes

Boolean attributes are attributes that do not have a value. Their presence or absence indicates their value. If they are absent, the value is false. If the attribute is present, the value is true.

The following is a list of the boolean attributes we are going to set on the video element.

**controls** - indicates whether the control panel is present on the video. this is the place where the user can interact with the video, such as starting and pausing.

**autoplay** - indicates whether the video should start immediately when the page loads.

**muted** - indicates that the sound should be turned off. this is require in some browsers for autoplay to work, as it can be problematic for videos with sound to autoplay unexpectedly.

**loop** - continually replay the video.
