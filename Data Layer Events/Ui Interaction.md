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
|event_data.identifier|string|Captures the name or ID of the ui element used.|act now, cancel, ok, 3456, 8765|||||||
|event_data.interaction_name|string|Text of the UI element that keeps you on the current page when clicked.| "Learning" on the navigation header|||||||


## Attached Notes

<p>Recorded when the user clicks a UI element on the page that doesn't navigate away from the current page (e.g., the "Learning" navigation element, which opens a dropdown menu without leaving the page).&nbsp;</p>
<p>There is a max length of 500 chars for the parameter values.</p>
