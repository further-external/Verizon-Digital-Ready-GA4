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
        "access_code": "<access_code>",
        "business_zip": "<business_zip>",
        "name": "<name>",
        "topics": "<topics>",
        "login_method": "<login_method>"
    },
    "user_data": {
        "user_id": "<user_id>",
        "user_type": "<user_type>"
    },
  "hashedEmail": "<hashedEmail>"
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.access_code|integer|Captures the access code entered from the partner registration flow||||||||
|event_data.business_zip|string|Zip code for the user's business|55555|||||||
|event_data.name|string|Captures the human-friendly name of the form.|partner registration, learner registration, profile update, superbowl grant, etc|||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Maximum of three topics, and topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\). For Learning Path events, set the value to the topic\(s\) that the Learning Path belongs to.|Branding,Managing money,Website design|||||||
|event_data.login_method|string|Records the system the user utilized to log in.|SSO,Native|||||||
|user_data.user_id|string|When authenticated, set to the UUID of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use the UUID when a user is authenticated. Set to empty when not authenticated.|||||||
|user_data.user_type|string|Captures the type associated with the user \(i.e. guest, registered, prime, etc\).|partner, learner|||||||
|hashedEmail|string|When authenticated, set to the hashed email of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use hashed email and not plain-text email when authenticated. Set to empty when not authenticated.|||||||

## Attached Notes

<p>Record this event when the user completes registration and views the registration confirmation page</p>
<p>With the introduction of SSO, it's important to understand the differences in login experiences that users encounter when signing in to VSBDR.</p>
