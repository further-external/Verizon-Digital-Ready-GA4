# Learning Path Enroll

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "learning_path_enroll",
  "detailed_event": "Learning Path Enroll",
    "event_data": {
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
|event_data.learning_path_id|string|Captures the ID of the path title||||||||
|event_data.learning_path_title|string|Set with the start or completion of a learning path||||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Maximum of three topics, and topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\)|Branding,Managing money,Website design|||||||
|user_data.user_id|string|The hashed email of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||




