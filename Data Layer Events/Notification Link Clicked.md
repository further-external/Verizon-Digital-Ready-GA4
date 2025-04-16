# Notification Link Clicked

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "click",
  "detailed_event": "Notification Link Clicked",
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
|event_data.identifier|string|Captures the name or ID of the notification link clicked.|act now, cancel, ok, 3456, 8765|||||||
|event_data.link_text|string|Text of the link clicked|Thanks for completing the course, `Money mindset: Removing blockers`., Thanks for completing the course, `Social media marketing: Keeping the conversation going`., View All|||||||
|event_data.link_url|string|Captures the site destination of the notification link used.|https:\/\/www.example.com|||||||

## Attached Notes

<p>Track when a user clicks a notification link—whether from the bell icon or the notification section—that navigates them to another page.</p>
<p>There is a max length of 500 chars for the parameter values.</p>
