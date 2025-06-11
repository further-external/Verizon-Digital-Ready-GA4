# Audio Started

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "audio_start",
  "detailed_event": "Audio Started",
    "event_data": {
        "identifier": "<identifier>",
        "audio_duration": <audio_duration>,
        "audio_title": "<audio_title>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|Captures the ID or file of the audio content being listened to by the visitor.|https://mb.verizonwireless.com/content/dam/vsbdr/videos/Craftingyourfoundersstory.mp4|||||||
|event_data.audio_duration|integer|Captures the length of the audio file. For start events, this should be 0.|0||||0|||
|event_data.audio_title|string|Captures the Name of audio content listened to by a visitor.|Crafting your founder's story, How to build confidence as an entrepreneur |||||||

## Attached Notes

<p>Record when a user clicks play to start listening to an audio file like those found on quick tips</p>
<p>There is a max length of 500 chars for the parameter values.</p>
