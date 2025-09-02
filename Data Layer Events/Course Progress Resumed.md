# Course Progress Resumed

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "course_progress_resumed",
  "detailed_event": "Course Progress Resumed",
    "event_data": {
        "course_id": "<course_id>",
        "course_progress_percentage": "<course_progress_percentage>",
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
|event_data.course_id|string|Captures the ID of the course within a learning path||||||||
|event_data.course_progress_percentage|string|Tracks the percentage of the course that the user has completed.|||||||
|event_data.course_title|string|Captures the title of the course within a learning path||||||||
|event_data.learning_path_id|string|Captures the ID of the path title||||||||
|event_data.learning_path_title|string|Set with the start or completion of a learning path||||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\). For Learning Path events, set the value to the topic\(s\) that the Learning Path belongs to.|Branding,Managing money,Website design|||||||
|user_data.user_id|string|When authenticated, set to the UUID of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use the UUID when a user is authenticated. Set to empty when not authenticated.|||||||

## Attached Notes
<p>This event should trigger on the course page only when a user selects the option to resume their course progress.</p>


