# User Signed Out

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({
  "event": "logout",
  "detailed_event": "User Signed Out",
    "user_data": {
        "user_id": "<user_id>",
        "user_login_state": "<user_login_state>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user_data.user_id|string|When authenticated, set to the UUID of the user currently logged in to the site. When on guest experience \(non-authenticated\), set value to empty string.|Use the UUID when a user is authenticated. Set to empty when not authenticated.|||||||
|user_data.user_login_state|string|Captures the current sign in status for the user.|logged in, logged out|||||||

## Attached Notes

<p>Recorded when a user successfully signs out</p>
<p>There is a max length of 500 chars for the parameter values.</p>
