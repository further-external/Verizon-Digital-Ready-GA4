# User Registration Step Encountered

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "registration_step_view",
  "detailed_event": "User Registration Step Encountered",
    "event_data": {
        "step_name": "<step_name>",
        "step_number": <step_number>,
        "topics": "<topics>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.step_name|string|Captures the name \/ id of each user registration step encountered.||||||||
|event_data.step_number|integer|Captures the number or sequence of quiz steps.|1, 2, 3, 4||||1|||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Maximum of three topics, and topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\)|Branding,Managing money,Website design|||||||

## Attached Notes

<p>*Should we fire both this + pageview during registration?</p>
<p>There is a max length of 500 chars for the parameter values.</p>
