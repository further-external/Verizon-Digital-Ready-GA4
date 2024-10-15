# Search Filter

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ page_data: null });  // Clear the previous page_data object.
dataLayer.push({
  "event": "search_filter",
  "detailed_event": "Search Filter",
    "page_data": {
        "language": "<language>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|page_data.language|string|The language of the current page, usually pulled from filter selection component (e.g., "Available in Spanish", "Available in Chinese", or "View all".)|en-US, es-ES, zh-CN|||||||




