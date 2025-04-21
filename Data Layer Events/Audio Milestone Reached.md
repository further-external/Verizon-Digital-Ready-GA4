# Audio Milestone Reached

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "audio_progress",
  "detailed_event": "Audio Milestone Reached",
    "event_data": {
        "identifier": "<identifier>",
        "audio_duration": <audio_duration>,
        "audio_title": "<audio_title>",
        "audio_milestones_reached": <audio_milestones_reached>,
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|Captures the ID or file of the audio content being listened to by the visitor.|https://mb.verizonwireless.com/content/dam/vsbdr/videos/Craftingyourfoundersstory.mp4|||||||
|event_data.audio_duration|integer|Captures the length of the audio file listened to by the visitor.|36, 67, 178, 600||||0|||
|event_data.audio_title|string|Captures the Name of audio content listened to by a visitor.|Crafting your founder's story, How to build confidence as an entrepreneur |||||||
|event_data.audio_milestones_reached|integer|Count of audio milestones reached \(25%, 50%, 75%\).||||||||

## Attached Notes

<p>Record when a user hits notable milestones within a audio's playback like those found on quick tips</p>
<p>There is a max length of 500 chars for the parameter values.</p>
