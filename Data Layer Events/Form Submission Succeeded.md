# Form Submission Succeeded

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null });  // Clear the previous event_data object.
dataLayer.push({
  "event": "form_complete",
  "detailed_event": "Form Submission Succeeded",
    "event_data": {
        "name": "<name>",
        "profile_status": "<profile_status>"
    },
    "user_data": {
        "user_id": "<user_id>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.name|string|Captures the human-friendly name of the form.|Payment Info, Mailing Address, Payment Address, Contact Us|||||||
|event_data.profile_status|string|Sets whether profile is complete or incomplete|complete, incomplete|||||||
|user_data.user_id|string|The hashed email of the user currently logged in to the site, if the site offers authentication and the user is authenticated.|123456, abc123|||||||


## Attached Notes

<p>There is a max length of 500 chars for the parameter values.</p>

