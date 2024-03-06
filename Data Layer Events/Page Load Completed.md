# Page Load Completed

### Page Load Completed is part of the page load sequence, including virtual page loads in the case of single page apps, and must be the last event pushed in the page load event sequence.

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({
  "event": "page_view",
  "detailed_event": "Page Load Completed"
});
```





## Attached Notes

<p>Record this once the page is fully loaded, and scripts and content are done loading.&nbsp;</p>
<p>There is a max length of 500 chars for the parameter values.</p>
