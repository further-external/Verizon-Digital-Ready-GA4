# User Registered

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "sign_up",
  "detailed_event": "User Registered",
    "event_data": {
        "business_zip": "<business_zip>",
        "topics": "<topics>"
    },
    "user_data": {
        "hashed_crm_id": "<hashed_crm_id>",
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.business_zip|string|Zip code for the user's business|55555|||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Maximum of three topics, and topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\). For Learning Path events, set the value to the topic\(s\) that the Learning Path belongs to.|Branding,Managing money,Website design|||||||
|user_data.hashed_crm_id|string|Captures the internal CRM or Data Warehouse segment associated with each user.||||||||
|user_data.user_id|string|When authenticated: Set to the hashed email of the user currently logged in to the site. When on guest experience: Set value to empty string when not authenticated.|Use hashed email and not plain-text email when authenticated. Set to empty when not authenticated.|||||||

## Attached Notes

<p>Record this event when the user completes registration and views the registration confirmation page</p>
