# Video Started

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "video_start",
  "detailed_event": "Video Started",
    "event_data": {
        "identifier": "<identifier>",
        "video_duration": <video_duration>,
        "video_title": "<video_title>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|Captures the ID of video content viewed by visitor.|YT456789, BC4567890, 876546789|||||||
|event_data.video_duration|integer|Captures the length of the video file. For start events, this should be 0.|0||||0|||
|event_data.video_title|string|Captures the Name of video content viewed by visitor.|Twitch\_FPS, Age of Empires, Halo|||||||

## Attached Notes

<p>Record when a user clicks play to start watching a video</p>
<p>There is a max length of 500 chars for the parameter values.</p>
