# Ui Interaction

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "click",
  "detailed_event": "Ui Interaction",
    "event_data": {
        "identifier": "<identifier>",
        "interaction_name": "<interaction_name>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.identifier|string|Captures the name or ID of the ui element used.|act now, cancel, ok, 3456, 8765, SMB Spotlight Profile|||||||
|event_data.interaction_name|string|Text of the UI element that keeps you on the current page when clicked.| "Learning" on the navigation header, On SMB spotlight when selecting a profile the mentor's name, On the updated course pages, elements within the Course Information Bar, such as 'Preview', 'Detail', 'Related', and 'Support'|||||||


## Attached Notes

<p>Recorded when the user clicks a UI element on the page that doesn't navigate away from the current page (e.g., the "Learning" navigation element, which opens a dropdown menu without leaving the page).&nbsp;</p>
<p>On the redesigned course pages, the Course Information Bar elements are now selectable. This event should be triggered when a user interacts with any of these elements on a course page.</p>
<p>In the Networking section of the site, this event should trigger when a user clicks on a profile within the 'Spotlight on Success' area.</p>
<p>There is a max length of 500 chars for the parameter values.</p>
