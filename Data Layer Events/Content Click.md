# Content Click

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "content_click",
  "detailed_event": "Content Click",
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
|event_data.link_text|string|Text of the link clicked|Article name, "Sign Up"|||||||
|event_data.link_url|string|Captures the site destination of the navigation links used.|https:\/\/www.digitalready.verizonwireless.com, https:\/\/www.dashboard-digitalready.verizonwireless.com, etc|||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Maximum of three topics, and topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\). For Learning Path events, set the value to the topic\(s\) that the Learning Path belongs to. <br><br>For general content outside of course material, this will be the header of the object being viewed.|Branding,Managing money,Website design|||||||
|user_data.user_id|string|When authenticated, set to the UUID of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use the UUID when a user is authenticated. Set to empty when not authenticated.|||||||
|event_data.content_category|string|The categorization of the content that has been viewed or engaged with by the user. This is to be used to distinguish between other content that has been viewed and engaged with on a particular page/screen.|page_sub_section, events_widget_body_signup,events_widget_body_register, events_widget_sitcky_signup, events_widget_body_complete, events_widget_body_ended, courses_widger_body_register, courses_social_modal|||||||

## Attached Notes
<p>Additionally fire this event for CTA button click (e.g. "Go to section" button in the Course sections of a course overview). </p>
<p>Within the Info Hub, please limit the number of "topics" sent in the string to 3. There is a character limit of 100 characters, and we prefer this to be limited within the dataLayer.</p>
<p>In the Networking section of the site, this event should trigger when a user clicks on a spotlighted user's top recommended courses or learning path.</p>
<p>There is a max length of 500 chars for the parameter values.</p>
