---
description: Let's you submit a contact message to an administrator.
---

# Contact

🔓 This page requires authentication.

{% api-method method="post" host="https://xyz.spaces.nexudus.com" path="/:langauge/newUserMessage" %}
{% api-method-summary %}
User Message
{% endapi-method-summary %}

{% api-method-description %}
Submits a contact message to the enquiries section. You can review contact messages from https://platform.nexudus.com/messages. Users with the option "Send a notification about contact messages." in https://platform.nexudus.com/settings/userssecurity will receive a notification about these messages.  
  
The response of this endpoint will always be a 200 status, even if the message was not sent correctly. Make sure you inspect the response and look for a "SuccessMessage" property in the returned JSON object.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic ZGVtb2....
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "InfoMessage": null,
    "ErrorMessage": null,
    "SuccessMessage": "Message was sent.",
    "RedirectTo": "/en/Contact"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

