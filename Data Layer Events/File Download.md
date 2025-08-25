# File Download

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "file_download",
  "detailed_event": "File Download",
    "event_data": {
        "name": "<name>",
        "type": "<type>",
        "link_url": "<link_url>"
    },
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.name|string|Captures the human-friendly name of the file.|course_12345_recap,event_12345_overview|||||||
|event_data.type|string|Captures the type of file.|pdf, mov, docx, wav|||||||
|event_data.link_url|string|Captures the site destination of the download links used.|https:\/\/www.digitalready.verizonwireless.com, https:\/\/www.dashboard-digitalready.verizonwireless.com, etc|||||||
|user_data.user_id|string|When authenticated, set to the UUID of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use the UUID when a user is authenticated. Set to empty when not authenticated.|||||||

## Attached Notes
<p>Fires when a user performs an action that downloads an asset to the user's device.
<p>If certain fields don't apply (e.g. Profile Status in the customer support form) leave those fields blank </p>
<p>There is a max length of 500 chars for the parameter values.</p>
