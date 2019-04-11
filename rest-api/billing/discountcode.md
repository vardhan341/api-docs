# DiscountCode

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/discountcodes" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of discountcodes based on one or more filter querystring parameters.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="Id" type="int" %}
?Id=...
{% endapi-method-parameter %}

{% api-method-parameter name="UniqueId" type="Guid" %}
?UniqueId=...
{% endapi-method-parameter %}

{% api-method-parameter name="SystemId" type="string" %}
?DiscountCode\_SystemId=...
{% endapi-method-parameter %}

{% api-method-parameter name="Business" type="Business" %}
?DiscountCode\_Business=...
{% endapi-method-parameter %}

{% api-method-parameter name="Code" type="string" %}
?DiscountCode\_Code=...
{% endapi-method-parameter %}

{% api-method-parameter name="Description" type="string" %}
?DiscountCode\_Description=...
{% endapi-method-parameter %}

{% api-method-parameter name="Active" type="bool" %}
?DiscountCode\_Active=...
{% endapi-method-parameter %}

{% api-method-parameter name="PublishFrom" type="DateTime?" %}
?DiscountCode\_PublishFrom=...
{% endapi-method-parameter %}

{% api-method-parameter name="PublishTo" type="DateTime?" %}
?DiscountCode\_PublishTo=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountPercentage" type="decimal?" %}
?DiscountCode\_DiscountPercentage=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountAmount" type="decimal?" %}
?DiscountCode\_DiscountAmount=...
{% endapi-method-parameter %}

{% api-method-parameter name="ReferralDiscount" type="bool" %}
?DiscountCode\_ReferralDiscount=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountPricePlans" type="bool" %}
?DiscountCode\_DiscountPricePlans=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountBookings" type="bool" %}
?DiscountCode\_DiscountBookings=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountProducts" type="bool" %}
?DiscountCode\_DiscountProducts=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountEvents" type="bool" %}
?DiscountCode\_DiscountEvents=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxUsesPerUser" type="int?" %}
?DiscountCode\_MaxUsesPerUser=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxUses" type="int?" %}
?DiscountCode\_MaxUses=...
{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForContacts" type="bool" %}
?DiscountCode\_OnlyForContacts=...
{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForMembers" type="bool" %}
?DiscountCode\_OnlyForMembers=...
{% endapi-method-parameter %}

{% api-method-parameter name="ValidFrom" type="DateTime?" %}
?DiscountCode\_ValidFrom=...
{% endapi-method-parameter %}

{% api-method-parameter name="ValidTo" type="DateTime?" %}
?DiscountCode\_ValidTo=...
{% endapi-method-parameter %}

{% api-method-parameter name="ExpirationType" type="enum" %}
?DiscountCode\_ExpirationType=...
{% endapi-method-parameter %}

{% api-method-parameter name="ExpiresIn" type="int?" %}
?DiscountCode\_ExpiresIn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Business\_Name" type="string" %}
?DiscountCode\_Business\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Business\_Currency\_Code" type="string" %}
?DiscountCode\_Business\_Currency\_Code=...
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "Business": null,
        "Code": "Code",
        "Description": "Description",
        "Active": true,
        "PublishFrom": null,
        "PublishTo": null,
        "DiscountPercentage": 0,
        "DiscountAmount": 0,
        "ReferralDiscount": true,
        "DiscountPricePlans": true,
        "DiscountBookings": true,
        "DiscountProducts": true,
        "DiscountEvents": true,
        "MaxUsesPerUser": 1,
        "MaxUses": 1,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "ValidFrom": null,
        "ValidTo": null,
        "ExpirationType": Nexudus.Coworking.Core.Enums.eDiscountExpirePeriod.Day,
        "ExpiresIn": 0,
    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `discountcode-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/discountcodes" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of discountcodes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="dir" type="string" required=false %}
one of 'Ascending' or 'Ascending'
{% endapi-method-parameter %}

{% api-method-parameter name="orderby" type="string" required=false %}
?orderby=Id
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=false %}
?page=1
{% endapi-method-parameter %}

{% api-method-parameter name="size" type="integer" required=false %}
size=25 \(maximum=1000\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "Business": null,
        "Code": "Code",
        "Description": "Description",
        "Active": true,
        "PublishFrom": null,
        "PublishTo": null,
        "DiscountPercentage": 0,
        "DiscountAmount": 0,
        "ReferralDiscount": true,
        "DiscountPricePlans": true,
        "DiscountBookings": true,
        "DiscountProducts": true,
        "DiscountEvents": true,
        "MaxUsesPerUser": 1,
        "MaxUses": 1,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "ValidFrom": null,
        "ValidTo": null,
        "ExpirationType": Nexudus.Coworking.Core.Enums.eDiscountExpirePeriod.Day,
        "ExpiresIn": 0,
    }],
    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `discountcode-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/discountcodes" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of discountcodes based on the date when they were created or updated.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="CreatedOn" type="object" required=false %}
?to\_DiscountCode\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_DiscountCode\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_DiscountCode\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="PublishFrom" type="datetime" required=false %}
?from\_DiscountCode\_PublishFrom=...
{% endapi-method-parameter %}

{% api-method-parameter name="PublishFrom" type="datetime" required=false %}
?to\_DiscountCode\_PublishFrom=...
{% endapi-method-parameter %}

{% api-method-parameter name="PublishTo" type="datetime" required=false %}
?from\_DiscountCode\_PublishTo=...
{% endapi-method-parameter %}

{% api-method-parameter name="PublishTo" type="datetime" required=false %}
?to\_DiscountCode\_PublishTo=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountPercentage" type="decimal" required=false %}
?from\_DiscountCode\_DiscountPercentage=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountPercentage" type="decimal" required=false %}
?to\_DiscountCode\_DiscountPercentage=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountAmount" type="decimal" required=false %}
?from\_DiscountCode\_DiscountAmount=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountAmount" type="decimal" required=false %}
?to\_DiscountCode\_DiscountAmount=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxUsesPerUser" type="decimal" required=false %}
?from\_DiscountCode\_MaxUsesPerUser=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxUsesPerUser" type="decimal" required=false %}
?to\_DiscountCode\_MaxUsesPerUser=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxUses" type="decimal" required=false %}
?from\_DiscountCode\_MaxUses=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxUses" type="decimal" required=false %}
?to\_DiscountCode\_MaxUses=...
{% endapi-method-parameter %}

{% api-method-parameter name="ValidFrom" type="datetime" required=false %}
?from\_DiscountCode\_ValidFrom=...
{% endapi-method-parameter %}

{% api-method-parameter name="ValidFrom" type="datetime" required=false %}
?to\_DiscountCode\_ValidFrom=...
{% endapi-method-parameter %}

{% api-method-parameter name="ValidTo" type="datetime" required=false %}
?from\_DiscountCode\_ValidTo=...
{% endapi-method-parameter %}

{% api-method-parameter name="ValidTo" type="datetime" required=false %}
?to\_DiscountCode\_ValidTo=...
{% endapi-method-parameter %}

{% api-method-parameter name="ExpiresIn" type="decimal" required=false %}
?from\_DiscountCode\_ExpiresIn=...
{% endapi-method-parameter %}

{% api-method-parameter name="ExpiresIn" type="decimal" required=false %}
?to\_DiscountCode\_ExpiresIn=...
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "Business": null,
        "Code": "Code",
        "Description": "Description",
        "Active": true,
        "PublishFrom": null,
        "PublishTo": null,
        "DiscountPercentage": 0,
        "DiscountAmount": 0,
        "ReferralDiscount": true,
        "DiscountPricePlans": true,
        "DiscountBookings": true,
        "DiscountProducts": true,
        "DiscountEvents": true,
        "MaxUsesPerUser": 1,
        "MaxUses": 1,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "ValidFrom": null,
        "ValidTo": null,
        "ExpirationType": Nexudus.Coworking.Core.Enums.eDiscountExpirePeriod.Day,
        "ExpiresIn": 0,
    }],
    }],
    "CurrentPageSize": 25,
    "CurrentPage": 1,
    "CurrentOrderField": "Id",
    "CurrentSortDirection": 1,
    "FirstItem": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "LastItem": 25,
    "PageNumber": 1,
    "PageSize": 25,
    "TotalItems": 60,
    "TotalPages": 3
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `discountcode-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/discountcodes/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one discountcode record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the discountcode to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "Business": null,
        "Code": "Code",
        "Description": "Description",
        "Active": true,
        "PublishFrom": null,
        "PublishTo": null,
        "DiscountPercentage": 0,
        "DiscountAmount": 0,
        "ReferralDiscount": true,
        "DiscountPricePlans": true,
        "DiscountBookings": true,
        "DiscountProducts": true,
        "DiscountEvents": true,
        "MaxUsesPerUser": 1,
        "MaxUses": 1,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "ValidFrom": null,
        "ValidTo": null,
        "ExpirationType": Nexudus.Coworking.Core.Enums.eDiscountExpirePeriod.Day,
        "ExpiresIn": 0,
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
"Not found"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `discountcode-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/discountcodes" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new discountcode.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="BusinessId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Code" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Description" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Active" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PublishFrom" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PublishTo" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountPercentage" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountAmount" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ReferralDiscount" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountPricePlans" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountBookings" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountProducts" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountEvents" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MaxUsesPerUser" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MaxUses" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForContacts" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForMembers" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ValidFrom" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ValidTo" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ExpirationType" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ExpiresIn" type="int?" required=false %}

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
    "WasSuccessful": true,
    "Message": "Record 'Name of the record' has been succesfully created.",
    "Value": {
        "Id": 12354678,
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
_This response is an example, errors and messages will follow this structure but keys and descriptions may be different for each record._
{% endapi-method-response-example-description %}

```javascript
{
    "Status": 500,
    "Message": "Email: may not be null or empty",
    "Value": null,
    "WasSuccessful": false,
    "Errors": [
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "FullName"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "Email"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "Country"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "SimpleTimeZone"
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Message": "An error has occurred."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `discountcode-create`

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/discountcodes" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing discountcode.Required User Role: `discountcode-edit`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Id" type="integer" required=true %}
The id of the discountcode to update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="BusinessId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Code" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Description" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Active" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PublishFrom" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PublishTo" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountPercentage" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountAmount" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ReferralDiscount" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountPricePlans" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountBookings" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountProducts" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountEvents" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MaxUsesPerUser" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MaxUses" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForContacts" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForMembers" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ValidFrom" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ValidTo" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ExpirationType" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ExpiresIn" type="int?" required=false %}

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
    "WasSuccessful": true,
    "Message": "The record 'name of the record' was updated successfully,
    "Value": {
        "Id": 123456
    },
    "OpenInDialog": false,
    "Errors": null
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
_This response is an example, errors and messages will follow this structure but keys and descriptions may be different for each record._
{% endapi-method-response-example-description %}

```javascript
{
    "Status": 500,
    "Message": "Email: may not be null or empty",
    "Value": null,
    "WasSuccessful": false,
    "Errors": [
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "FullName"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null or empty",
            "PropertyName": "Email"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "Country"
        },
        {
            "AttemptedValue": null,
            "Message": "may not be null",
            "PropertyName": "SimpleTimeZone"
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Message": "An error has occurred."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `discountcode-edit`

{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/billing/discountcodes/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a discountcode.Required User Roles: `discountcode-delete`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Id" type="integer" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Status": 200,
    "WasSuccessful": true,
    "Message": "The record was deleted successfully.",
    "Value": null,
    "OpenInDialog": false,
    "RedirectURL": null,
    "JavaScript": null,
    "Errors": null
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
"Not found"
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Message": "An error has occurred."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `discountcode-delete`

## Commands

Commands allow to perform actions against one or more discountcode records. Some commands accept only one record while others can run an action for a number of records at the same time. Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/discountcodes/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for discountcode records.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
_This response is an example._
{% endapi-method-response-example-description %}

```javascript
[
    {
        "Key": "COMMAND_KEY_1",
        "Name": "Command English Description",
        "AppliesOnlyToMultipleEntities": false,
        "AppliesOnlyToOneEntity": false,
        "AppliesOnlyToTwoEntities": false,
        "NeedsEntitiesToRun": true,
        "Order": 1,
        "RequiresParameters": []
    },
    {
        "Key": "COMMAND_KEY_2",
        "Name": "Command 2 English Description",
        "AppliesOnlyToMultipleEntities": true
        "AppliesOnlyToOneEntity": false,
        "AppliesOnlyToTwoEntities": false,
        "NeedsEntitiesToRun": true,
        "Order": 2,
        "RequiresParameters": []
    },
    ...
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/discountcodes/runcommand" %}
{% api-method-summary %}
Run Command
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="Key" type="string" required=true %}
The command Key defining the command to run. `"COMMAND_KEY_1"`
{% endapi-method-parameter %}

{% api-method-parameter name="Parameters" type="array" required=false %}
A list of object with the structure below. The parameters required for each command are returned in the "RequiresParameters" array return by the "commands" endpoint.`[    
{    
"Name": "Name",    
"Type":"Type",    
"Value":recordId    
}    
]`
{% endapi-method-parameter %}

{% api-method-parameter name="Ids" type="array" required=true %}
A list of integer IDs for each of the records to run this command for.`[987654321, 123565978]`
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
_Commands also return a status 200 when they fail to process one or more of the records. Use the 'WasSuccessful' property to know if the command run succeeded._
{% endapi-method-response-example-description %}

```javascript
{  
   "Status":500 or 200,
   "Message":"Command error description",
   "Value":null,
   "Errors":null,
   "WasSuccessful":false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `discountcode-edit`

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

## Related Entities

* [Business](../sys/business.md)

