---
description: >-
  Returns data and authentication tokens for a user based on their username and
  password.
---

# User

{% api-method method="post" host="https://spaces.nexudus.com" path="/sys/users/token" %}

**Request Body**

```javascript
{ 
  email: "..@..", 
  password: "xyz",
  validityInMinutes: 30
}
```

{% api-method method="post" host="https://spaces.nexudus.com" path="/sys/users/:id/token/refresh" %}

**Request Body**

```javascript
{ 
  email: "..@..", 
  password: "xyz",
  validityInMinutes: 30
}
```

**Request Body**

```javascript
{ 
  email: "..@..", 
  password: "xyz",
  validityInMinutes: 30
}
```

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:langauge/user/login" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="redirectUrl" type="string" required=false %}
A relative URL to send the user to after being logged in.
{% endapi-method-parameter %}

{% api-method-parameter name="t" type="string" required=true %}
The access token
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:langauge/user/resetPassword" %}
{% api-method-summary %}
Reset Password
{% endapi-method-summary %}

{% api-method-description %}
Sends a password reset email to a specific user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="email" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "Status": 200,
  "Message": "We have sent you an email with instructions on how to change your password.",
  "WasSuccessful": true
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
If user is not found
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

