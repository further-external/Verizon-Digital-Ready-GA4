# Search Filter

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "search_filter",
  "detailed_event": "Search Filter",
    "event_data": {
        "filter_location":"<filter_location>"
        "language_filter": "<language_filter>"
        "topics": "<topics>",
        "skill_level":"<skill_level>",
        "status_filter": "<status_filter>",
        "type_filter":"<type_filter>",
        "dates_filter":"<dates_filter>"
        "filter_results":"<filter_results>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.filter_location|string|The section of the site where this filter search occured |Course, Events, Quick Tips|||||||
|event_data.language_filter|string|The language from filter selection component (e.g., "Available in Spanish", "Available in Chinese", or "View all".)| View All, Available in Spanish,Available in Chinese, English events, Spanish events, Bilingual events|||||||
|event_data.topics|string|All topics selected by the user or relevant to the current page, in a comma-separated format. Topics should be recorded in alphabetical order. \(Otherwise Branding,Managing money,Website design and Managing money,Branding,Website design will be two different values\). For Learning Path events, set the value to the topic\(s\) that the Learning Path belongs to.|View All, Branding,Managing money,Website design|||||||
|event_data.skill_level|string| The Skill level associate with filtering, in a comma-separated format |Foundational, Intermediate, View All|||||||
|event_data.status_filter|string| Indicates the status or statuses selected by the user in the search filterin a comma-separated for multiple selections. |Courses:View All,Not Started, In Progress, Completed, Added to favorites Events:View all,Seats available, Waitlist available, Registered for event, On waitlist for event, Recorded events, Added to favorites|||||||
|event_data.type_filter|string|The type of sub category associate with filtering in a comma-separated for multiple selections|Quick Tips:View All Articles, Audio clips , Videos. Events:View All, Ask the experts, Hands-on help, Networking sessions Courses:View All,Standard Courses, Mini Courses|||||||
|event_data.dates_filter|string| Captures the start and end date selected by the user to filter results within a specific date range.|Value formated as: "Start Date - End Date", View all|||||||
|event_data.filter_results|integer| The total number of results generated after a filter has been applied. |1,5,10,20,0|||||||