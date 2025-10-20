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
        "new_content_added": "<new_content_added>",
        "profile_status": "<profile_status>",
        "topics": "<topics>"
    },
    "page_data": {
        "country": "<country>",
        "language": "<language>",
        "page_location": "<page_location>",
        "page_referrer": "<page_referrer>",
        "page_title": "<page_title>",
        "content_name": "<content_name>",
        "content_category": "<content_category>",
        "event_skill_level_id": "<event_skill_level_id>",
        "event_admission_cost": "<event_admission_cost>"

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
|event_data.new_content_added|boolean|Captures if the content course or event was just added to the resources.\(yes or no\) <br><br> \(This is managed exclusively on VSBDR pages.\) |yes, no|||||||
|event_data.profile_status|string|When authenticated, set to whether profile is complete or incomplete. In guest experience, set to an empty value.|Use complete or incomplete|||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\). For Learning Path events, set the value to the topic\(s\) that the Learning Path belongs to.|Branding,Managing money,Website design|||||||
|page_data.country|string|The country associated with the current page.|US, CA, FR, UK|||||||
|page_data.language|string|The language of the current page, usually pulled from the &lt;html&gt; tag lang attribute.|en-us, es-es, zh-cn|||||||
|page_data.page_location|string|The full URL that the visitor was on when the event took place.|https:\/\/digitalready.verizonwireless.com\/onboarding, https:\/\/dashboard-digitalready.verizonwireless.com\/, https:\/\/dashboard-digitalready.verizonwireless.com\/course-details\/course:5255225|||||||
|page_data.page_referrer|string|Tracks the previous page before page load or history change of previous screen. Use full URL of previous page\/screen. Ensure URL is carried through for when the url has a page path.\/onboarding; the value sometimes is wiped clear.|https:\/\/digitalready.verizonwireless.com\/onboarding or https:\/\/digitalready.verizonwireless.com\/grants|||||||
|page_data.content_name|string| When available, this value will contain the name/title of the content currently being viewed on a page, usually the name of the course, the event/virtual event, learning path, or another value that is used to address the content on the page being viewed. | Defining your brand: Connecting to customers, Activate cutting-edge marketing strategies with the power of AI, Mastering social media marketing|||||||
|page_data.content_category|string| When available, this value describes the type of page content the user is interacting with. For example Quick Tips, this can include Articles, Videos, and Audio pages . Similarly, Courses can be categorized as either full Courses or Mini Courses pages. For events, when a user visits an in-person event, we want this labeled as "events:in-person events," and for virtual events, labeled as "events:virtual event.". These values will align with the "type" filter provided on content category pages. | Quicktips: Articles, Videos, Audio. Courses: Course, Mini Course. Events:Virtual Event, Events:In-Person Events.|||||||
|page_data.event_skill_level_id|string|Sets the ID of the event's skill level||||||||
|page_data.event_admission_cost|string|Sets the cost to attend the event||||||||
|page_data.page_title|string|The title of the page currently being viewed, generally available in &lt;title&gt;.||||||||
|user_data.user_id|string|When authenticated, set to the UUID of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string. <br><br> \(This is managed exclusively on VSBDR pages.\)|Use the UUID when a user is authenticated. Set to empty when not authenticated.|||||||
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
