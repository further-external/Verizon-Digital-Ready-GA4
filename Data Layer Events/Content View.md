# Content View

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "content_view",
  "detailed_event": "Content View",
    "event_data": {
        "link_text": "<link_text>",
        "link_url": "<link_url>",
        "topics": "<topics>",
        "content_category": "<content_category>"
    },
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.link_text|string|Text of the link viewed|Article name, "Sign Up"|||||||
|event_data.link_url|string|Captures the site destination of the navigation links used.|https:\/\/www.digitalready.verizonwireless.com, https:\/\/www.dashboard-digitalready.verizonwireless.com, etc|||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. A Topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\). For Learning Path events, set the value to the topic\(s\) that the Learning Path belongs to. For general content outside of course material, this will be the header of the object being viewed.|Branding,Managing money,Website design|||||||
|user_data.user_id|string|When authenticated, set to the UUID of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use the UUID when a user is authenticated. Set to empty when not authenticated.|||||||
|event_data.content_category|string|The categorization of the content that has been viewed or engaged with by the user. This is to be used to distinguish between other content that has been viewed and engaged with on a particular page/screen.|page_sub_section, event_widget_body_signup,event_widget_body_register, event_widget_sitcky_signup, event_widget_body_complete, event_widget_body_ended|||||||

## Attached Notes
<p>This event should only fire when the content is within the VISIBLE VIEWPORT of the page/screen on which the content has been loaded. This event WILL NOT fire on page/screen load. </p>
<p>Within the Info Hub, please limit the number of "topics" sent in the string to 3. There is a character limit of 100 characters, and we prefer this to be limited within the dataLayer.</p>
<p>There is a max length of 500 chars for the parameter values.</p>
