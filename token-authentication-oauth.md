---
description: >-
  Token authentication can be used to obtain a token that can be used in
  requests the Nexudus REST API without having to use admin credentials.
---

# Token Authentication \(oauth\)

The general process to use token authentication is as follows:

1. Get a short-lived authentication **access token** and a **refresh token**.
2. Refresh the token as needed.
3. Use the "Bearer" HTTP header to make requests to the [REST API](rest-api/).

Access tokens are generally short-lived and you should not assume they last for more than a few minutes or hours. 

{% hint style="danger" %}
You should always keep your refresh tokens secure, treat them as passwords.
{% endhint %}

{% api-method method="post" host="https://spaces.nexudus.com" path="/api/token" %}
{% api-method-summary %}
Authentication and Refresh Token
{% endapi-method-summary %}

{% api-method-description %}
Gets a short-lived access token and a long-lived refresh token.  
  
`grant_ype=password&username=EMAIL_ADDRESS&  
password=Demo1234&  
client_id=demoaccount@nexudus.com`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" %}
A unique identifier for the client making these requests. A single refresh tokens will be created per client.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="grant\_type" required=true type="string" %}
password
{% endapi-method-parameter %}

{% api-method-parameter name="username" type="string" required=true %}
your email
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
your password  
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "access_token": "v8hNJebN2....",
    "token_type": "bearer",
    "expires_in": 604799,
    "refresh_token": "2669808..."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
If you submit an invalid username and/or password
{% endapi-method-response-example-description %}

```javascript
{
    "error": "invalid_grant",
    "error_description": "The user name or password is incorrect."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://spaces.nexudus.com" path="/api/token" %}
{% api-method-summary %}
Refresh Access Token
{% endapi-method-summary %}

{% api-method-description %}
Gets a new short-lived access token based on a refresh token. Refreshing a token for a client ID will invalidate all previous refresh tokens for that client ID but not existing Access Tokens that may not have expired.  
  
Refresh Tokens are valid for 15 days. If you refresh token has expired, you will need to use a username and password to create a new access token.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Accept" required=true type="string" %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="client\_id" type="string" required=false %}
The client id to refresh the access token for. This must the same as the client id you passed in when creating the access token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="grant\_type" type="string" required=true %}
refresh\_token
{% endapi-method-parameter %}

{% api-method-parameter name="refresh\_token" type="string" required=true %}
2669808...
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "access_token": "5o8X7pSy....",
    "token_type": "bearer",
    "expires_in": 604799,
    "refresh_token": "c3c14715..."
}    
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "error": "invalid_grant"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

