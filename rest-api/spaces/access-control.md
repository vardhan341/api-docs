---
description: >-
  This API endpoint lets you check a coworker in and out based on their
  username/password, a access card ID or a access token.
---

# Access Control

{% hint style="info" %}
When testing this endpoint, ensure the coworker you are trying these requests for has at least one unused time pass in their account. 

You can manually add a time pass to a member from the "Time Passes" tab in their account
{% endhint %}

{% api-method method="post" host="https://xyz.spaces.nexudus.com/api/" path="public/checkin" %}
{% api-method-summary %}
By access card
{% endapi-method-summary %}

{% api-method-description %}
"xyz" is your account sub-domain. It is the prefix before ".spaces.nexudus.com" in your member portal.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="Disconnect" type="boolean" required=false %}
Checks the coworker out.
{% endapi-method-parameter %}

{% api-method-parameter name="Toggle" type="boolean" required=false %}
If 'true', the coworker will be checked out if they are currently checked in and will be checked in if they are currently checked out.
{% endapi-method-parameter %}

{% api-method-parameter name="AccessCardId" type="string" required=true %}
The access card associated with the coworker to be checked in.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Status": 200,
    "Message": "2015-09-11T21:59:59 UTC",
    "Value": {
        "SessionExpire": "2015-09-11T21:59:59 UTC",
        "SessionTimeOut": 46455.3521501
    },
    "Errors": null,
    "WasSuccessful": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

🔒 Required roles: `none`

{% api-method method="post" host="https://xyz.spaces.nexudus.com/api/" path="public/checkin" %}
{% api-method-summary %}
By credentials
{% endapi-method-summary %}

{% api-method-description %}
"xyz" is your account sub-domain. It is the prefix before ".spaces.nexudus.com" in your member portal.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="Disconnect" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Toggle" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Email" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Password" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Mac" type="string" required=false %}
AA:BB:CC:DD:EE:FF
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Status": 200,
    "Message": "2015-09-11T21:59:59 UTC",
    "Value": {
        "SessionExpire": "2015-09-11T21:59:59 UTC",
        "SessionTimeOut": 46455.3521501
    },
    "Errors": null,
    "WasSuccessful": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

🔒 Required roles: `none`

{% api-method method="post" host="https://xyz.spaces.nexudus.com/api/" path="public/checkin" %}
{% api-method-summary %}
By access token
{% endapi-method-summary %}

{% api-method-description %}
"xyz" is your account sub-domain. It is the prefix before ".spaces.nexudus.com" in your member portal.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="Disconnect" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Toggle" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Token" type="string" required=true %}
A valid access token. Check "AccessToken" endpoint in the "Spaces" section.
{% endapi-method-parameter %}

{% api-method-parameter name="Mac" type="string" required=false %}
AA:BB:CC:DD:EE:FF
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Status": 200,
    "Message": "2015-09-11T21:59:59 UTC",
    "Value": {
        "SessionExpire": "2015-09-11T21:59:59 UTC",
        "SessionTimeOut": 46455.3521501
    },
    "Errors": null,
    "WasSuccessful": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

🔒 Required roles: `none`



