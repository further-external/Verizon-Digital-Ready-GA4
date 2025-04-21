# Site Search

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "view_search_results",
  "detailed_event": "Site Search",
    "event_data": {
        "search_term":"<search_term>",
        "search_location":"<search_location>",
        "search_results":"<search_results>",
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.search_term|string|This field captures the actual search query entered by the user. |Branding,Managing money,Website design, Business|||||||
|event_data.search_location|string|The section of the site where this search occured |Course, Events|||||||
|event_data.search_results|integer|The total number of results generated after a search is conducted.|1,5,10,20,0||||||

## Attached Notes

<p>This event should fire whenever a user performs a search action on the site using a search bar.</p>
<p>There is a max length of 500 chars for the parameter values.</p>
