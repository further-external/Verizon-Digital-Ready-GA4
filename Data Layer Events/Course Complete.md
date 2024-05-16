# Course Complete

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "course_complete",
  "detailed_event": "Course Complete",
    "event_data": {
        "count_course_complete": <count_course_complete>,
        "course_id": "<course_id>",
        "course_title": "<course_title>",
        "learning_path_id": "<learning_path_id>",
        "learning_path_title": "<learning_path_title>",
        "topics": "<topics>"
    },
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.count_course_complete|integer|Measure the total courses completed|1|||||||
|event_data.course_id|string|Captures the ID of the course within a learning path||||||||
|event_data.course_title|string|Captures the title of the course within a learning path||||||||
|event_data.learning_path_id|string|Captures the ID of the path title||||||||
|event_data.learning_path_title|string|Set with the start or completion of a learning path||||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Maximum of three topics, and topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\).

For Learning Path events, set the value to the topic\(s\) that the Learning Path belongs to.|Branding,Managing money,Website design|||||||
|user_data.user_id|string|When authenticated: Set to the hashed email of the user currently logged in to the site. 

When on guest experience: Set value to empty string when not authenticated.|Use hashed email and not plain-text email when authenticated. Set to empty when not authenticated.|||||||




