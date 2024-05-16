# Unregistered Event

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "unregister_event",
  "detailed_event": "Unregistered Event",
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
|user_data.user_id|string|When authenticated: Set to the hashed email of the user currently logged in to the site. 

When on guest experience: Set value to empty string when not authenticated.|Use hashed email and not plain-text email when authenticated. Set to empty when not authenticated.|||||||

## Attached Notes

<p>There is a max length of 500 chars for the parameter values.</p>
