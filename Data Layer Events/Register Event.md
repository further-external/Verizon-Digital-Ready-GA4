# Register Event

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "register_event",
  "detailed_event": "Register Event",
    "event_data": {
        "calendar_event_title": "<calendar_event_title>"
    },
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.calendar_event_title|string|Sets the name of the calendar\_event||||||||
|user_data.user_id|string|The hashed email of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||




