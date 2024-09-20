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
        "name": "<name>",
        "access_code": <access_code>,
        "business_zip": "<business_zip>",
        "topics": "<topics>"
    },
    "user_data": {
        "user_id": "<user_id>",
        "user_type": "<user_type>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.name|string|Captures the human-friendly name of the form.|digital ready partner, small business parnter, learner registration, etc|||||||
|event_data.access_code|integer|Captures the access code entered from the partner registration flow||||||||
|event_data.business_zip|string|Zip code for the user's business|55555|||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Maximum of three topics, and topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\). For Learning Path events, set the value to the topic\(s\) that the Learning Path belongs to.|Branding,Managing money,Website design|||||||
|user_data.user_id|string|When authenticated, set to the hashed email of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use hashed email and not plain-text email when authenticated. Set to empty when not authenticated.|||||||
|user_data.user_type|string|Captures the type associated with the user \(i.e. guest, registered, prime, etc\).|employee, guest, agent, customer|||||||

## Attached Notes

<p>Record this event when the user completes registration and views the registration confirmation page</p>
