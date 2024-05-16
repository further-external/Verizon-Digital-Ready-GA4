# User Signed In

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({
  "event": "login",
  "detailed_event": "User Signed In",
    "user_data": {
        "user_id": "<user_id>",
        "user_login_state": "<user_login_state>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user_data.user_id|string|When authenticated: Set to the hashed email of the user currently logged in to the site. 

When on guest experience: Set value to empty string when not authenticated.|Use hashed email and not plain-text email when authenticated. Set to empty when not authenticated.|||||||
|user_data.user_login_state|string|Captures the current sign in status for the user.|logged in, logged out|||||||

## Attached Notes

<p>Recorded when a user successfully completes sign-in</p>
<p>There is a max length of 500 chars for the parameter values.</p>
