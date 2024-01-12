# User Registration Click

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "user_registration_click",
  "detailed_event": "User Registration Click",
    "event_data": {
        "click_location": "<click_location>",
        "link_text": "<link_text>",
        "link_url": "<link_url>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.click_location|string|The location where a user clicked a CTA|Header, Sidebar, etc|||||||
|event_data.link_text|string|Text of the link clicked|Article name, "Sign Up"|||||||
|event_data.link_url|string|Captures the site destination of the navigation links used.|https:\/\/www.example.com|||||||

## Attached Notes

<p>The user clicks on a CTA to start the registration process</p>
