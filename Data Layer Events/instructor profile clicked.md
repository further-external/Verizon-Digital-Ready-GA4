# Instructor profile clicked

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "click",
  "detailed_event": "instructor profile clicked",
    "event_data": {
        "identifier": "<identifier>",
        "link_text": "<link_text>",
        "link_url": "<link_url>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|Captures the name or ID of the instructor profile link clicked.|act now, cancel, ok, 3456, 8765|||||||
|event_data.link_text|string|Text of the link clicked|Allison McInstructor|||||||
|event_data.link_url|string|Captures the site destination of the instructor profile link used.|https:\/\/www.example.com|||||||

## Attached Notes

<p>Track when a user clicks on an instructor's name to visit their profile.</p>
<p>There is a max length of 500 chars for the parameter values.</p>
