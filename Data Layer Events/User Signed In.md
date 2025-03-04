# User Signed In

### 

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({
  "event": "login",
  "detailed_event": "User Signed In",
  "event_data": {
        "login_method": "<login_method>"
    }
    "user_data": {
        "user_login_state": "<user_login_state>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|event_data.login_method|string|Records the system the user utilized to log in.|SSO,Native|||||||
|user_data.user_login_state|string|Captures the current sign in status for the user.|logged in, logged out|||||||

## Attached Notes

<p>Recorded when a user successfully completes sign-in</p>
<p>There is a max length of 500 chars for the parameter values.</p>
<p>With the introduction of SSO, it's important to understand the differences in login experiences that users encounter when signing in to VSBDR.</p>
