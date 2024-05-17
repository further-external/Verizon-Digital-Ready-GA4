# Page Load Started

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({ page_data: null });  // Clear the previous page_data object.
dataLayer.push({
  "event": "page_load_started",
  "detailed_event": "Page Load Started",
    "event_data": {
        "profile_status": "<profile_status>",
        "topics": "<topics>"
    },
    "page_data": {
        "country": "<country>",
        "language": "<language>",
        "page_location": "<page_location>",
        "page_referrer": "<page_referrer>",
        "page_title": "<page_title>"
    },
    "user_data": {
        "user_id": "<user_id>",
        "user_login_state": "<user_login_state>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.profile_status|string|When authenticated, set to whether profile is complete or incomplete. In guest experience, set to an empty value.|Use complete or incomplete|||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Maximum of three topics, and topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\). For Learning Path events, set the value to the topic\(s\) that the Learning Path belongs to.|Branding,Managing money,Website design|||||||
|page_data.country|string|The country associated with the current page.|US, CA, FR, UK|||||||
|page_data.language|string|The language of the current page, usually pulled from the &lt;html&gt; tag lang attribute.|en-us, en-gb, ch-cn, fr-ca, fr-fr|||||||
|page_data.page_location|string|The full URL that the visitor was on when the event took place.|https:\/\/digitalready.verizonwireless.com\/onboarding, https:\/\/dashboard-digitalready.verizonwireless.com\/, https:\/\/dashboard-digitalready.verizonwireless.com\/course-details\/course:5255225|||||||
|page_data.page_referrer|string|Tracks the previous page before page load or history change of previous screen. Use full URL of previous page\/screen.|https:\/\/digitalready.verizonwireless.com\/onboarding or https:\/\/digitalready.verizonwireless.com\/grants|||||||
|page_data.page_title|string|The title of the page currently being viewed, generally available in &lt;title&gt;.||||||||
|user_data.user_id|string|When authenticated, set to the hashed email of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use hashed email and not plain-text email when authenticated. Set to empty when not authenticated.|||||||
|user_data.user_login_state|string|Captures the current sign in status for the user.|logged in, logged out|||||||

## Attached Notes

<p>Record Page Load Started when a new page begins to load - either when a page is initially loading, or when a new single-page app view starts to load. <br /><br />For the registration steps, these should also be considered as distinct screens and should be triggered with each new step. While these URLs are not truly accessible to the end-user, we need this level of detail because Google Analytics does not recognize single page applications consistently.&nbsp;<br /><br /><strong>Example of Values for Registration Steps</strong></p>
<table style="border-collapse: collapse; width: 100.047%;" border="1">
<tbody>
<tr>
<td style="width: 31.9833%;"><strong>Page Title</strong></td>
<td style="width: 31.9833%;"><strong>Example page_location</strong></td>
<td style="width: 31.9833%;"><strong>Example page_referrer [Previous page or null if they came directly to the site]</strong></td>
</tr>
<tr>
<td style="width: 31.9833%;">Hi. Let&rsquo;s find the topics that interest you.</td>
<td style="width: 31.9833%;">https://digitalready.verizonwireless.com/onboarding</td>
<td style="width: 31.9833%;">https://digitalready.verizonwireless.com</td>
</tr>
<tr>
<td style="width: 31.9833%;">Do you identify with any of the following groups?</td>
<td style="width: 31.9833%;">https://digitalready.verizonwireless.com/onboarding-step-2</td>
<td style="width: 31.9833%;">https://digitalready.verizonwireless.com/onboarding</td>
</tr>
<tr>
<td style="width: 31.9833%;">And where&rsquo;s your business located?</td>
<td style="width: 31.9833%;">https://digitalready.verizonwireless.com/onboarding-step-3</td>
<td style="width: 31.9833%;">https://digitalready.verizonwireless.com/onboarding-step-2</td>
</tr>
<tr>
<td style="width: 31.9833%;">Excellent. To finish registering, enter an email and password.</td>
<td style="width: 31.9833%;">https://digitalready.verizonwireless.com/onboarding-step-4</td>
<td style="width: 31.9833%;">https://digitalready.verizonwireless.com/onboarding-step-3</td>
</tr>
</tbody>
</table>
<p>There is a max length of 500 chars for the parameter values.</p>
