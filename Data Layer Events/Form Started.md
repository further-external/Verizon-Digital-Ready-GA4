# Form Started

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "form_start",
  "detailed_event": "Form Started",
    "event_data": {
        "name": "<name>",
        "profile_status": "<profile_status>",
        "form_type": "<form_type>",
    },
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.name|string|Captures the human-friendly name of the form.|partner registration, learner registration, referral form, profile update, superbowl grant, etc|||||||
|event_data.profile_status|string|When authenticated, set to whether profile is complete or incomplete. In guest experience, set to an empty value.|Use complete or incomplete|||||||
|event_data.form_type|string|The Form type used for grouping of similar forms.|Customer Support|||||||
|user_data.user_id|string|When authenticated, set to the UUID of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use the UUID when a user is authenticated. Set to empty when not authenticated.|||||||

## Attached Notes
<p>If certain fields don't apply (e.g. Profile Status in the customer support form) leave those fields blank </p>
<p>There is a max length of 500 chars for the parameter values.</p>
