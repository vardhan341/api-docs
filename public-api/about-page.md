---
description: Returns the data available on the about us page.
---

# About Page

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/about" %}
{% api-method-summary %}
About page
{% endapi-method-summary %}

{% api-method-description %}
Gets the data representing the about us page
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="langugage" type="string" required=true %}
'en' or any other valid language in your account.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=false %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "Gallery": [
        {
            "Name": "ixhnbgtkjfw-crew.jpg",
            "Description": "ixhnbgtkjfw-crew",
            "UseInGallery": true,
            "Url": "/images/ixhnbgtkjfw-crew.jpg",
            "Id": 287944659,
            "IdString": "287944659",
            "UpdatedOn": "2019-03-26T11:28:46",
            "CreatedOn": "2017-01-27T11:20:02",
            "UniqueId": "00881309-3775-4f42-b045-6946b6891011",
            "IsNull": false
        }
    ],
    "ProfileTags": [
        "html",
        "webdesign",
        "architecture",
        "business management",
        "css",
        "editing",
        "finance",
        "javascript",
        "legal",
        "react",
        "resource acquisition",
        "startup",
        "surveying",
        "urbanism",
        "web design"
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

