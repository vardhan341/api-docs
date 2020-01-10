﻿{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/subscribergroups" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of subscribergroups based on one or more filter querystring parameters.
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
?SubscriberGroup\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?SubscriberGroup\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="Name" type="string" %}
?SubscriberGroup\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="AutoAddMembers" type="bool" %}
?SubscriberGroup\_AutoAddMembers=...
{% endapi-method-parameter %}


{% api-method-parameter name="AutoAddContacts" type="bool" %}
?SubscriberGroup\_AutoAddContacts=...
{% endapi-method-parameter %}


{% api-method-parameter name="AutoAddBookings" type="bool" %}
?SubscriberGroup\_AutoAddBookings=...
{% endapi-method-parameter %}


{% api-method-parameter name="AutoAddEvents" type="bool" %}
?SubscriberGroup\_AutoAddEvents=...
{% endapi-method-parameter %}


{% api-method-parameter name="AutoAddVisitors" type="bool" %}
?SubscriberGroup\_AutoAddVisitors=...
{% endapi-method-parameter %}


{% api-method-parameter name="AutoAddPayingMembers" type="bool" %}
?SubscriberGroup\_AutoAddPayingMembers=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business\_Name" type="string" %}
?SubscriberGroup\_Business\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="NewsLetterSubscribers" type="int" required=false %}
?SubscriberGroup\_NewsLetterSubscribers=...
{% endapi-method-parameter %}

{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "Business": null,
        "Name": "00001",
        "AutoAddMembers": true,
        "AutoAddContacts": true,
        "AutoAddBookings": true,
        "AutoAddEvents": true,
        "AutoAddVisitors": true,
        "AutoAddPayingMembers": true,
		"SubscriberGroupBusinessName": "...",

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

> 🔒 Requires user role `subscribergroup-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/subscribergroups" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of subscribergroups.
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
        "Name": "00001",
        "AutoAddMembers": true,
        "AutoAddContacts": true,
        "AutoAddBookings": true,
        "AutoAddEvents": true,
        "AutoAddVisitors": true,
        "AutoAddPayingMembers": true,
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

> 🔒 Requires user role `subscribergroup-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/subscribergroups" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of subscribergroups based on a range of dates, integer or decimal properties.
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
?to\_SubscriberGroup\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_SubscriberGroup\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_SubscriberGroup\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_SubscriberGroup\_UpdatedOn=...
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
        "Name": "00001",
        "AutoAddMembers": true,
        "AutoAddContacts": true,
        "AutoAddBookings": true,
        "AutoAddEvents": true,
        "AutoAddVisitors": true,
        "AutoAddPayingMembers": true,
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

> 🔒 Requires user role `subscribergroup-list`


{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/subscribergroups?SubscriberGroup_Id=[:id1,:id2,...]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more subscribergroup records based on their Id.
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
Comma-separated list of IDs of every subscribergroup to fetch. I.e. [123456,789102,...] 
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
        "Business": null,
        "Name": "00001",
        "AutoAddMembers": true,
        "AutoAddContacts": true,
        "AutoAddBookings": true,
        "AutoAddEvents": true,
        "AutoAddVisitors": true,
        "AutoAddPayingMembers": true,
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

> 🔒 Requires user role `subscribergroup-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/subscribergroups/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one subscribergroup record.
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
The ID of the subscribergroup to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "Business": null,
        "Name": "00001",
        "AutoAddMembers": true,
        "AutoAddContacts": true,
        "AutoAddBookings": true,
        "AutoAddEvents": true,
        "AutoAddVisitors": true,
        "AutoAddPayingMembers": true,
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

> 🔒 Requires user role `subscribergroup-read`


{% api-method method="post" host="https://spaces.nexudus.com/api" path="/content/subscribergroups" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new subscribergroup.
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
{% api-method-parameter name="Name" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddMembers" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddContacts" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddBookings" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddEvents" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddVisitors" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddPayingMembers" type="bool" required=false %}
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

> 🔒 Requires user role `subscribergroup-create`

```javascript
{
	"Business": 12345678,
	"Name": "00001",
	"NewsLetterSubscribers": [12345678, 87654321] (replaces entire list),
	"AddedNewsLetterSubscribers": [12345678, 87654321] (adds to list),
	"RemovedNewsLetterSubscribers": [12345678, 87654321] (removes from list),
	"AutoAddMembers": true,
	"AutoAddContacts": true,
	"AutoAddBookings": true,
	"AutoAddEvents": true,
	"AutoAddVisitors": true,
	"AutoAddPayingMembers": true,
}

```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/content/subscribergroups" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing subscribergroup. PUT requests require ALL record properties to be submitted with every request. Any missing properties will be cleared or set to false.
  
Required User Role: `subscribergroup-edit`
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

{% api-method-parameter name="Id" type="int" required="true" %}
{% api-method-parameter name="BusinessId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="NewsLetterSubscribers" type="int[]" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="AddedNewsLetterSubscribers" type="int[]" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="RemovedNewsLetterSubscribers" type="int[]" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddMembers" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddContacts" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddBookings" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddEvents" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddVisitors" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoAddPayingMembers" type="bool" required="true" %}
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

> 🔒 Requires user role `subscribergroup-edit`

```javascript
{
	"Business": 12345678,
	"Name": "00001",
	"NewsLetterSubscribers": [12345678, 87654321] (replaces entire list),
	"AddedNewsLetterSubscribers": [12345678, 87654321] (adds to list),
	"RemovedNewsLetterSubscribers": [12345678, 87654321] (removes from list),
	"AutoAddMembers": true,
	"AutoAddContacts": true,
	"AutoAddBookings": true,
	"AutoAddEvents": true,
	"AutoAddVisitors": true,
	"AutoAddPayingMembers": true,
}

```




{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/content/subscribergroups/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a subscribergroup.  
  
Required User Roles: `subscribergroup-delete`
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



> 🔒 Requires user role `subscribergroup-delete`


## Commands

Commands allow to perform actions against one or more subscribergroup records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/subscribergroups/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for subscribergroup records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/subscribergroups/runcommand" %}
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

> 🔒 Requires user role `subscribergroup-edit`

## Enumerated values

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [Business](../sys/business.md)
