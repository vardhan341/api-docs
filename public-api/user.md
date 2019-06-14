---
description: >-
  Returns data and authentication tokens for a user based on their username and
  password.
---

# User

{% api-method method="post" host="https://spaces.nexudus.com" path="/sys/users/token" %}
{% api-method-summary %}
Get User Token
{% endapi-method-summary %}

{% api-method-description %}
Gets a JWT token for a user based on their username and password. JWT tokens can be used to authenticate against the PUBLIC API or to log a user in the member portal \(once\) without having to ask for their credentials.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "Status": 200,
  "Message": "OK",
  "Value": "1350eXAiOiJKV1QiLCJhbGciOiJIUzI11J9.[truncated].dfE1dtaeOfqhasdasd23hCJUn_RMW9usu9oUdE",
  "WasSuccessful": true
}

or 

{
  "Status": 500,
  "Message": "The email address or password you entered is not valid.",
  "WasSuccessful": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Request Body**

```javascript
{ 
  email: "..@..", 
  password: "xyz",
  validityInMinutes: 30
}
```

{% api-method method="post" host="https://spaces.nexudus.com" path="/sys/users/:id/token/refresh" %}
{% api-method-summary %}
Refresh Access Token
{% endapi-method-summary %}

{% api-method-description %}
Gets a new authentication token based on a set of REST API user credentials. This method requires you to pass REST authentication details, not the email and password of the user you are obtaining the token for!
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "Status": 200,
  "Message": "OK",
  "Value": "1350eXAiOiJKV1QiLCJhbGciOiJIUzI11J9.[truncated].dfE1dtaeOfqhasdasd23hCJUn_RMW9usu9oUdE",
  "WasSuccessful": true
}
      
or
      
{
  "Status": 500,
  "Message": "The email address or password you entered is not valid.",
  "WasSuccessful": false
}#
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:langauge/user/login" %}
{% api-method-summary %}
Log User By Token
{% endapi-method-summary %}

{% api-method-description %}
Logs a user in on your members portal based on a authentication token. This action will immediately invalidate the access token.
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

```

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



