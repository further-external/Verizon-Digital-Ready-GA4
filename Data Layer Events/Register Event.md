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
        "calendar_event_title": "<calendar_event_title>",
        "event_skill_level": "<event_skill_level>",
        "event_admission_cost": "<event_admission_cost>",
        "content_category": "<content_category>"
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
|event_data.event_skill_level|string|Sets the name of the event's skill level||||||||
|event_data.event_admission_cost|string|Sets the cost to attend the event||||||||
|event_data.content_category|string|The categorization of the content that has been viewed or engaged with by the user. This is to be used to distinguish between other content that has been viewed and engaged with on a particular page/screen.|For events, when a user visits an in-person event, we want this labeled as "events:in-person events," and for virtual events, labeled as "events:virtual event.|||||||
|user_data.user_id|string|When authenticated, set to the UUID of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use the UUID when a user is authenticated. Set to empty when not authenticated.|||||||

## Attached Notes
<p>This should be added to the "sign up for event" button on in-person registration pages and the "enroll" button on virtual pages.</p>
<p>There is a max length of 500 chars for the parameter values.</p>
