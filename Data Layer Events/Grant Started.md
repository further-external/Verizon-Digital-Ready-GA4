# Grant Started

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "grant_start",
  "detailed_event": "Grant Started",
    "event_data": {
        "name": "<name>",
        "profile_status": "<profile_status>"
    },
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.name|string|Captures the human-friendly name of the form.|partner registration, learner registration, profile update, superbowl grant, etc|||||||
|event_data.profile_status|string|When authenticated, set to whether profile is complete or incomplete. In guest experience, set to an empty value.|Use complete or incomplete|||||||
|user_data.user_id|string|When authenticated, set to the hashed email of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use hashed email and not plain-text email when authenticated. Set to empty when not authenticated.|||||||




