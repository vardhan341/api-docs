{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/resellers" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
 This endpoint allows you to GET a list of resellers based on one or more filter querystring parameters.
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
?Reseller\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Name" type="string" %}
?Reseller\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="User" type="User" %}
?Reseller\_User=...
{% endapi-method-parameter %}


{% api-method-parameter name="Currency" type="Currency" %}
?Reseller\_Currency=...
{% endapi-method-parameter %}


{% api-method-parameter name="AgreedTermsOn" type="DateTime?" %}
?Reseller\_AgreedTermsOn=...
{% endapi-method-parameter %}


{% api-method-parameter name="Approved" type="bool" %}
?Reseller\_Approved=...
{% endapi-method-parameter %}


{% api-method-parameter name="NextPayoutDate" type="DateTime?" %}
?Reseller\_NextPayoutDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProfileIsPublic" type="bool" %}
?Reseller\_ProfileIsPublic=...
{% endapi-method-parameter %}


{% api-method-parameter name="Area" type="string" %}
?Reseller\_Area=...
{% endapi-method-parameter %}


{% api-method-parameter name="OperatesIn" type="string" %}
?Reseller\_OperatesIn=...
{% endapi-method-parameter %}


{% api-method-parameter name="WebAddress" type="string" %}
?Reseller\_WebAddress=...
{% endapi-method-parameter %}


{% api-method-parameter name="Email" type="string" %}
?Reseller\_Email=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProfileSummary" type="string" %}
?Reseller\_ProfileSummary=...
{% endapi-method-parameter %}


{% api-method-parameter name="PhoneNumber" type="string" %}
?Reseller\_PhoneNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="Testimonial1" type="string" %}
?Reseller\_Testimonial1=...
{% endapi-method-parameter %}


{% api-method-parameter name="Testimonial1Author" type="string" %}
?Reseller\_Testimonial1Author=...
{% endapi-method-parameter %}


{% api-method-parameter name="Testimonial2" type="string" %}
?Reseller\_Testimonial2=...
{% endapi-method-parameter %}


{% api-method-parameter name="Testimonial2Author" type="string" %}
?Reseller\_Testimonial2Author=...
{% endapi-method-parameter %}


{% api-method-parameter name="StripeAccountId" type="string" %}
?Reseller\_StripeAccountId=...
{% endapi-method-parameter %}


{% api-method-parameter name="User\_FullName" type="string" %}
?Reseller\_User\_FullName=...
{% endapi-method-parameter %}


{% api-method-parameter name="User\_Email" type="string" %}
?Reseller\_User\_Email=...
{% endapi-method-parameter %}


{% api-method-parameter name="Currency\_Code" type="string" %}
?Reseller\_Currency\_Code=...
{% endapi-method-parameter %}


{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "Name": "00001",
        "User": null,
        "Currency": null,
        "AgreedTermsOn": false,
        "Approved": false,
        "NextPayoutDate": false,
        "ProfileIsPublic": false,
        "Area": "00001",
        "OperatesIn": "00001",
        "WebAddress": "00001",
        "Email": "00001",
        "ProfileSummary": "BusinessArea",
        "PhoneNumber": "BusinessArea",
        "Testimonial1": "BusinessArea",
        "Testimonial1Author": "BusinessArea",
        "Testimonial2": "BusinessArea",
        "Testimonial2Author": "BusinessArea",
        "StripeAccountId": "false",
		"ResellerUserFullName": "...",
		"ResellerUserEmail": "...",
		"ResellerCurrencyCode": "...",

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

> 🔒 Requires user role `reseller-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/resellers" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of resellers.
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
        "Name": "00001",
        "User": null,
        "Currency": null,
        "AgreedTermsOn": false,
        "Approved": false,
        "NextPayoutDate": false,
        "ProfileIsPublic": false,
        "Area": "00001",
        "OperatesIn": "00001",
        "WebAddress": "00001",
        "Email": "00001",
        "ProfileSummary": "BusinessArea",
        "PhoneNumber": "BusinessArea",
        "Testimonial1": "BusinessArea",
        "Testimonial1Author": "BusinessArea",
        "Testimonial2": "BusinessArea",
        "Testimonial2Author": "BusinessArea",
        "StripeAccountId": "false",
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

> 🔒 Requires user role `reseller-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/resellers" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of resellers based on a range of dates, integer or decimal properties.
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
?to\_Reseller\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_Reseller\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_Reseller\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_Reseller\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="AgreedTermsOn" type="datetime" required=false %}
?from\_Reseller\_AgreedTermsOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="AgreedTermsOn" type="datetime" required=false %}
?to\_Reseller\_AgreedTermsOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="NextPayoutDate" type="datetime" required=false %}
?from\_Reseller\_NextPayoutDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="NextPayoutDate" type="datetime" required=false %}
?to\_Reseller\_NextPayoutDate=...
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
        "Name": "00001",
        "User": null,
        "Currency": null,
        "AgreedTermsOn": false,
        "Approved": false,
        "NextPayoutDate": false,
        "ProfileIsPublic": false,
        "Area": "00001",
        "OperatesIn": "00001",
        "WebAddress": "00001",
        "Email": "00001",
        "ProfileSummary": "BusinessArea",
        "PhoneNumber": "BusinessArea",
        "Testimonial1": "BusinessArea",
        "Testimonial1Author": "BusinessArea",
        "Testimonial2": "BusinessArea",
        "Testimonial2Author": "BusinessArea",
        "StripeAccountId": "false",
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

> 🔒 Requires user role `reseller-list`


{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/resellers?Reseller_Id=[:id1,:id2,...]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more reseller records based on their Id.
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

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every reseller to fetch. I.e. [123456,789102,...] 
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "Name": "00001",
        "User": null,
        "Currency": null,
        "AgreedTermsOn": false,
        "Approved": false,
        "NextPayoutDate": false,
        "ProfileIsPublic": false,
        "Area": "00001",
        "OperatesIn": "00001",
        "WebAddress": "00001",
        "Email": "00001",
        "ProfileSummary": "BusinessArea",
        "PhoneNumber": "BusinessArea",
        "Testimonial1": "BusinessArea",
        "Testimonial1Author": "BusinessArea",
        "Testimonial2": "BusinessArea",
        "Testimonial2Author": "BusinessArea",
        "StripeAccountId": "false",
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

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
"Not found"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `reseller-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/resellers/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one reseller record.
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

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the reseller to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "Name": "00001",
        "User": null,
        "Currency": null,
        "AgreedTermsOn": false,
        "Approved": false,
        "NextPayoutDate": false,
        "ProfileIsPublic": false,
        "Area": "00001",
        "OperatesIn": "00001",
        "WebAddress": "00001",
        "Email": "00001",
        "ProfileSummary": "BusinessArea",
        "PhoneNumber": "BusinessArea",
        "Testimonial1": "BusinessArea",
        "Testimonial1Author": "BusinessArea",
        "Testimonial2": "BusinessArea",
        "Testimonial2Author": "BusinessArea",
        "StripeAccountId": "false",
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
"Not found"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `reseller-read`


{% api-method method="post" host="https://spaces.nexudus.com/api" path="/sys/resellers" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new reseller.
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
{% api-method-parameter name="Name" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileIsPublic" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Area" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OperatesIn" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="WebAddress" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Email" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileSummary" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PhoneNumber" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Testimonial1" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Testimonial1Author" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Testimonial2" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Testimonial2Author" type="string" required=false %}
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

> 🔒 Requires user role `reseller-create`

```javascript
{
	"Name": "00001",
	"ProfileIsPublic": false,
	"Area": "00001",
	"OperatesIn": "00001",
	"WebAddress": "00001",
	"Email": "00001",
	"ProfileSummary": "BusinessArea",
	"PhoneNumber": "BusinessArea",
	"Testimonial1": "BusinessArea",
	"Testimonial1Author": "BusinessArea",
	"Testimonial2": "BusinessArea",
	"Testimonial2Author": "BusinessArea",
}

```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/sys/resellers" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing reseller. PUT requests require ALL record properties to be submitted with every request. Any missing properties will be cleared or set to false.
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

{% api-method-parameter name="Id" type="int" required="true" %}{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileIsPublic" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Area" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="OperatesIn" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="WebAddress" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Email" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileSummary" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="PhoneNumber" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Testimonial1" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Testimonial1Author" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Testimonial2" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Testimonial2Author" type="string" required="true" %}
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

> 🔒 Requires user role `reseller-edit`
> Note PUT requests, unlike PATCH requests, must include all properties as part of the request body. Any missing properties will be cleared or set to false.

```javascript
{
	"Id": 12345678,
	"Name": "00001",
	"ProfileIsPublic": false,
	"Area": "00001",
	"OperatesIn": "00001",
	"WebAddress": "00001",
	"Email": "00001",
	"ProfileSummary": "BusinessArea",
	"PhoneNumber": "BusinessArea",
	"Testimonial1": "BusinessArea",
	"Testimonial1Author": "BusinessArea",
	"Testimonial2": "BusinessArea",
	"Testimonial2Author": "BusinessArea",
}

```




{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/sys/resellers/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a reseller.  
  
Required User Roles: `reseller-delete`
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

{% api-method-path-parameters %}
{% api-method-parameter name="Id" type="integer" required=false %}

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

```
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



> 🔒 Requires user role `reseller-delete`


## Commands

Commands allow to perform actions against one or more reseller records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/resellers/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for reseller records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/resellers/runcommand" %}
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
A list of object with the structure below. The parameters required for each command are returned in the "RequiresParameters" array return by the "commands" endpoint.  
  
`[  
   {  
      "Name": "Name",   
      "Type":"Type",   
      "Value":recordId  
    }  
]`
{% endapi-method-parameter %}

{% api-method-parameter name="Ids" type="array" required=true %}
A list of integer IDs for each of the records to run this command for.  
  
`[987654321, 123565978]`
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
_Commands also return a status 200 when they fail to process one or more of the records. Use the 'WasSuccessful'  property to know if the command run succeeded._  
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

> 🔒 Requires user role `reseller-edit`

## Enumerated values

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/resellers/getavatar/:id" %}
{% api-method-summary %}
Avatar
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

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Reseller to get the avatar for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
Binary stream or null
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/resellers/getlogo/:id" %}
{% api-method-summary %}
Logo
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

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Reseller to get the logo for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
Binary stream or null
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


## Related Entities
* [User](../sys/user.md)
* [Currency](../sys/currency.md)
