# Navigation Link Clicked

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "click",
  "detailed_event": "Navigation Link Clicked",
    "event_data": {
        "identifier": "<identifier>",
        "link_text": "<link_text>",
        "link_url": "<link_url>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|Captures the name or ID of the navigation links used.|act now, cancel, ok, 3456, 8765|||||||
|event_data.link_text|string|Text of the link clicked|Article name, "Sign Up"|||||||
|event_data.link_url|string|Captures the site destination of the navigation links used.|https:\/\/www.example.com|||||||

## Attached Notes

<p>Recorded when the user clicks a navigation link - in the navigation header, the homepage button, or the footer. This can encompass any link that navigates a user to a sub-section of the site such as the "meet the instructors" page. &nbsp;</p>
<p>There is a max length of 500 chars for the parameter values.</p>
