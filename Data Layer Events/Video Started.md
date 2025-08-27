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
        "video_duration": "<video_duration>",
        "video_title": "<video_title>",
        "video_type": "<video_type>",
        "video_tally": <video_tally>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|Captures the ID of video content viewed by visitor.|YT456789, BC4567890, 876546789|||||||
|event_data.video_duration|integer|Captures the length of the video file. For start events, this should be 0.|0||||0|||
|event_data.video_title|string|Captures the Name of video content viewed by visitor.|Twitch\_FPS, Age of Empires, Halo|||||||
|event_data.video_type|string|Captures the Type of video content viewed by visitor. Used to distinguish videos that are previewed or watched within a course.|preview, full length|||||||
|event_data.video_tally|integer|Captures the number of videos a user has viewed during their session.|1,2,5,10||||0|||

## Attached Notes

<p>Record when a user clicks play to start watching a video</p>
<p>When a video is uploaded and used in Adobe LMS: Data Pull from LMS (e.g. Full Courses)</p>
<p>When a video is uploaded and used in Adobe AEM: Data Pull from Google Analytics 4 (e.g. Quick Tips, Recorded Events)</p>
<p>There is a max length of 500 chars for the parameter values.</p>
