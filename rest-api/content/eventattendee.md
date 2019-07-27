{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/eventattendees" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of eventattendees based on one or more filter querystring parameters.
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
?EventAttendee\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?EventAttendee\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="CalendarEvent" type="CalendarEvent" %}
?EventAttendee\_CalendarEvent=...
{% endapi-method-parameter %}


{% api-method-parameter name="EventProduct" type="EventProduct" %}
?EventAttendee\_EventProduct=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker" type="Coworker" %}
?EventAttendee\_Coworker=...
{% endapi-method-parameter %}


{% api-method-parameter name="FullName" type="string" %}
?EventAttendee\_FullName=...
{% endapi-method-parameter %}


{% api-method-parameter name="Email" type="string" %}
?EventAttendee\_Email=...
{% endapi-method-parameter %}


{% api-method-parameter name="AttendeeCode" type="string" %}
?EventAttendee\_AttendeeCode=...
{% endapi-method-parameter %}


{% api-method-parameter name="CheckedIn" type="bool" %}
?EventAttendee\_CheckedIn=...
{% endapi-method-parameter %}


{% api-method-parameter name="CheckedInDate" type="DateTime?" %}
?EventAttendee\_CheckedInDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="Invoiced" type="bool" %}
?EventAttendee\_Invoiced=...
{% endapi-method-parameter %}


{% api-method-parameter name="DueDate" type="DateTime?" %}
?EventAttendee\_DueDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerInvoiceId" type="int?" %}
?EventAttendee\_CoworkerInvoiceId=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerInvoiceNumber" type="string" %}
?EventAttendee\_CoworkerInvoiceNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerInvoicePaid" type="bool" %}
?EventAttendee\_CoworkerInvoicePaid=...
{% endapi-method-parameter %}


{% api-method-parameter name="CalendarEvent\_Name" type="string" %}
?EventAttendee\_CalendarEvent\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="EventProduct\_Name" type="string" %}
?EventAttendee\_EventProduct\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="EventProduct\_Price" type="string" %}
?EventAttendee\_EventProduct\_Price=...
{% endapi-method-parameter %}


{% api-method-parameter name="EventProduct\_Currency_Code" type="string" %}
?EventAttendee\_EventProduct\_Currency_Code=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_FullName" type="string" %}
?EventAttendee\_Coworker\_FullName=...
{% endapi-method-parameter %}


{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "Business": null,
        "CalendarEvent": null,
        "EventProduct": null,
        "Coworker": null,
        "FullName": "Attendee FullName",
        "Email": "Attendee Email",
        "AttendeeCode": "012345",
        "CheckedIn": false,
        "CheckedInDate": ,
        "Invoiced": false,
        "DueDate": false,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
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

> 🔒 Requires user role `eventattendee-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/eventattendees" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of eventattendees.
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
        "CalendarEvent": null,
        "EventProduct": null,
        "Coworker": null,
        "FullName": "Attendee FullName",
        "Email": "Attendee Email",
        "AttendeeCode": "012345",
        "CheckedIn": false,
        "CheckedInDate": ,
        "Invoiced": false,
        "DueDate": false,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
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

> 🔒 Requires user role `eventattendee-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/eventattendees" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of eventattendees based on a range of dates, integer or decimal properties.
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
?to\_EventAttendee\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_EventAttendee\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_EventAttendee\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_EventAttendee\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CheckedInDate" type="datetime" required=false %}
?from\_EventAttendee\_CheckedInDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="CheckedInDate" type="datetime" required=false %}
?to\_EventAttendee\_CheckedInDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="datetime" required=false %}
?from\_EventAttendee\_DueDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="datetime" required=false %}
?to\_EventAttendee\_DueDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerInvoiceId" type="int" required=false %}
?from\_EventAttendee\_CoworkerInvoiceId=...
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerInvoiceId" type="int" required=false %}
?to\_EventAttendee\_CoworkerInvoiceId=...
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
        "CalendarEvent": null,
        "EventProduct": null,
        "Coworker": null,
        "FullName": "Attendee FullName",
        "Email": "Attendee Email",
        "AttendeeCode": "012345",
        "CheckedIn": false,
        "CheckedInDate": ,
        "Invoiced": false,
        "DueDate": false,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
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

> 🔒 Requires user role `eventattendee-list`


{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/eventattendees?EventAttendee_Id=[:id1,:id2,...]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more eventattendee records based on their Id.
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
Comma-separated list of IDs of every eventattendee to fetch. I.e. [123456,789102,...] 
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
        "CalendarEvent": null,
        "EventProduct": null,
        "Coworker": null,
        "FullName": "Attendee FullName",
        "Email": "Attendee Email",
        "AttendeeCode": "012345",
        "CheckedIn": false,
        "CheckedInDate": ,
        "Invoiced": false,
        "DueDate": false,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
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

> 🔒 Requires user role `eventattendee-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/eventattendees/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one eventattendee record.
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
The ID of the eventattendee to fetch.
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
        "CalendarEvent": null,
        "EventProduct": null,
        "Coworker": null,
        "FullName": "Attendee FullName",
        "Email": "Attendee Email",
        "AttendeeCode": "012345",
        "CheckedIn": false,
        "CheckedInDate": ,
        "Invoiced": false,
        "DueDate": false,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
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

> 🔒 Requires user role `eventattendee-read`


{% api-method method="post" host="https://spaces.nexudus.com/api" path="/content/eventattendees" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new eventattendee.
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
{% api-method-parameter name="CalendarEventId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="EventProductId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FullName" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Email" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="CheckedIn" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CheckedInDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Invoiced" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerInvoiceId" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerInvoiceNumber" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerInvoicePaid" type="bool" required=false %}
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

> 🔒 Requires user role `eventattendee-create`

```javascript
{
	"Business": 12345678,
	"CalendarEvent": 12345678,
	"EventProduct": 12345678,
	"Coworker": 12345678,
	"FullName": "Attendee FullName",
	"Email": "Attendee Email",
	"CheckedIn": false,
	"CheckedInDate": ,
	"Invoiced": false,
	"CoworkerInvoiceId": ,
	"CoworkerInvoiceNumber": "",
	"CoworkerInvoicePaid": ,
}

```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/content/eventattendees" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing eventattendee.
  
Required User Role: `eventattendee-edit`
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
The id of the eventattendee to update
{% api-method-parameter name="BusinessId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="CalendarEventId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="EventProductId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FullName" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Email" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="CheckedIn" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CheckedInDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerInvoiceId" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerInvoiceNumber" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerInvoicePaid" type="bool" required=false %}
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

> 🔒 Requires user role `eventattendee-edit`

```javascript
{
	"Business": 12345678,
	"CalendarEvent": 12345678,
	"EventProduct": 12345678,
	"Coworker": 12345678,
	"FullName": "Attendee FullName",
	"Email": "Attendee Email",
	"CheckedIn": false,
	"CheckedInDate": ,
	"CoworkerInvoiceId": ,
	"CoworkerInvoiceNumber": "",
	"CoworkerInvoicePaid": ,
}

```




{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/content/eventattendees/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a eventattendee.  
  
Required User Roles: `eventattendee-delete`
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



> 🔒 Requires user role `eventattendee-delete`


## Commands

Commands allow to perform actions against one or more eventattendee records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/eventattendees/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for eventattendee records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/eventattendees/runcommand" %}
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

> 🔒 Requires user role `eventattendee-edit`

## Enumerated values

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [Business](../sys/business.md)
* [CalendarEvent](../content/calendarevent.md)
* [EventProduct](../content/eventproduct.md)
* [Coworker](../spaces/coworker.md)
