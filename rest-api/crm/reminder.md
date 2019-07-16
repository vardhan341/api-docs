{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/reminders" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of reminders based on one or more filter querystring parameters.
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
?Reminder\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?Reminder\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="Name" type="string" %}
?Reminder\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="ForAllContacts" type="bool" %}
?Reminder\_ForAllContacts=...
{% endapi-method-parameter %}


{% api-method-parameter name="ForAllMembers" type="bool" %}
?Reminder\_ForAllMembers=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker" type="Coworker" %}
?Reminder\_Coworker=...
{% endapi-method-parameter %}


{% api-method-parameter name="ReminderType" type="enum" %}
?Reminder\_ReminderType=...
{% endapi-method-parameter %}


{% api-method-parameter name="ReminderDate" type="DateTime?" %}
?Reminder\_ReminderDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="DaysAfterSignup" type="int?" %}
?Reminder\_DaysAfterSignup=...
{% endapi-method-parameter %}


{% api-method-parameter name="Product" type="Product" %}
?Reminder\_Product=...
{% endapi-method-parameter %}


{% api-method-parameter name="DaysAfterRenewal" type="int?" %}
?Reminder\_DaysAfterRenewal=...
{% endapi-method-parameter %}


{% api-method-parameter name="DaysBeforeRenewal" type="int?" %}
?Reminder\_DaysBeforeRenewal=...
{% endapi-method-parameter %}


{% api-method-parameter name="ReminderAction" type="enum" %}
?Reminder\_ReminderAction=...
{% endapi-method-parameter %}


{% api-method-parameter name="Email" type="string" %}
?Reminder\_Email=...
{% endapi-method-parameter %}


{% api-method-parameter name="CannedResponse" type="CannedResponse" %}
?Reminder\_CannedResponse=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tariffs" type="int" required=false %}
?Reminder\_Tariffs=...
{% endapi-method-parameter %}

{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "Business": null,
        "Name": "Joe",
        "ForAllContacts": false,
        "ForAllMembers": false,
        "Coworker": null,
        "ReminderType": eReminderType.FixedDate,
        "ReminderDate": null,
        "DaysAfterSignup": null,
        "Product": null,
        "DaysAfterRenewal": null,
        "DaysBeforeRenewal": null,
        "ReminderAction": eReminderAction.SendEmail,
        "Email": "joe@nexudus.com",
        "CannedResponse": null,
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

> 🔒 Requires user role `reminder-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/reminders" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of reminders.
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
        "Name": "Joe",
        "ForAllContacts": false,
        "ForAllMembers": false,
        "Coworker": null,
        "ReminderType": eReminderType.FixedDate,
        "ReminderDate": null,
        "DaysAfterSignup": null,
        "Product": null,
        "DaysAfterRenewal": null,
        "DaysBeforeRenewal": null,
        "ReminderAction": eReminderAction.SendEmail,
        "Email": "joe@nexudus.com",
        "CannedResponse": null,
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

> 🔒 Requires user role `reminder-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/reminders" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of reminders based on a range of dates, integer or decimal properties.
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
?to\_Reminder\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_Reminder\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_Reminder\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_Reminder\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="ReminderDate" type="datetime" required=false %}
?from\_Reminder\_ReminderDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="ReminderDate" type="datetime" required=false %}
?to\_Reminder\_ReminderDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="DaysAfterSignup" type="int" required=false %}
?from\_Reminder\_DaysAfterSignup=...
{% endapi-method-parameter %}
{% api-method-parameter name="DaysAfterSignup" type="int" required=false %}
?to\_Reminder\_DaysAfterSignup=...
{% endapi-method-parameter %}
{% api-method-parameter name="DaysAfterRenewal" type="int" required=false %}
?from\_Reminder\_DaysAfterRenewal=...
{% endapi-method-parameter %}
{% api-method-parameter name="DaysAfterRenewal" type="int" required=false %}
?to\_Reminder\_DaysAfterRenewal=...
{% endapi-method-parameter %}
{% api-method-parameter name="DaysBeforeRenewal" type="int" required=false %}
?from\_Reminder\_DaysBeforeRenewal=...
{% endapi-method-parameter %}
{% api-method-parameter name="DaysBeforeRenewal" type="int" required=false %}
?to\_Reminder\_DaysBeforeRenewal=...
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
        "Name": "Joe",
        "ForAllContacts": false,
        "ForAllMembers": false,
        "Coworker": null,
        "ReminderType": eReminderType.FixedDate,
        "ReminderDate": null,
        "DaysAfterSignup": null,
        "Product": null,
        "DaysAfterRenewal": null,
        "DaysBeforeRenewal": null,
        "ReminderAction": eReminderAction.SendEmail,
        "Email": "joe@nexudus.com",
        "CannedResponse": null,
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

> 🔒 Requires user role `reminder-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/reminders/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one reminder record.
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
The ID of the reminder to fetch.
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
        "Name": "Joe",
        "ForAllContacts": false,
        "ForAllMembers": false,
        "Coworker": null,
        "ReminderType": eReminderType.FixedDate,
        "ReminderDate": null,
        "DaysAfterSignup": null,
        "Product": null,
        "DaysAfterRenewal": null,
        "DaysBeforeRenewal": null,
        "ReminderAction": eReminderAction.SendEmail,
        "Email": "joe@nexudus.com",
        "CannedResponse": null,
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

> 🔒 Requires user role `reminder-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/crm/reminders" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new reminder.
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
{% api-method-parameter name="ForAllContacts" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ForAllMembers" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ReminderType" type="enum" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ReminderDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DaysAfterSignup" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProductId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DaysAfterRenewal" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DaysBeforeRenewal" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ReminderAction" type="enum" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Email" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CannedResponseId" type="int" required=false %}
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

> 🔒 Requires user role `reminder-create`

```javascript
{
	"Business": 12345678,
	"Name": "Joe",
	"ForAllContacts": false,
	"ForAllMembers": false,
	"Coworker": 12345678,
	"ReminderType": 1 (check Enumerated values section below),
	"ReminderDate": null,
	"DaysAfterSignup": null,
	"Product": 12345678,
	"DaysAfterRenewal": null,
	"DaysBeforeRenewal": null,
	"ReminderAction": 1 (check Enumerated values section below),
	"Email": "joe@nexudus.com",
	"CannedResponse": 12345678,
}

```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/crm/reminders" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing reminder.
  
Required User Role: `reminder-edit`
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
The id of the reminder to update
{% api-method-parameter name="BusinessId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="ForAllContacts" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ForAllMembers" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ReminderType" type="enum" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ReminderDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DaysAfterSignup" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProductId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DaysAfterRenewal" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DaysBeforeRenewal" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ReminderAction" type="enum" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Email" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CannedResponseId" type="int" required=false %}
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

> 🔒 Requires user role `reminder-edit`

```javascript
{
	"Business": 12345678,
	"Name": "Joe",
	"ForAllContacts": false,
	"ForAllMembers": false,
	"Coworker": 12345678,
	"ReminderType": 1 (check Enumerated values section below),
	"ReminderDate": null,
	"DaysAfterSignup": null,
	"Product": 12345678,
	"DaysAfterRenewal": null,
	"DaysBeforeRenewal": null,
	"ReminderAction": 1 (check Enumerated values section below),
	"Email": "joe@nexudus.com",
	"CannedResponse": 12345678,
}

```




{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/crm/reminders/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a reminder.  
  
Required User Roles: `reminder-delete`
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



> 🔒 Requires user role `reminder-delete`


## Commands

Commands allow to perform actions against one or more reminder records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/reminders/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for reminder records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/reminders/runcommand" %}
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

> 🔒 Requires user role `reminder-edit`

## Enumerated values

##### ReminderType:
> GET /api/utils/enums?name=eReminderType

##### ReminderAction:
> GET /api/utils/enums?name=eReminderAction

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [Business](../sys/business.md)
* [Coworker](../spaces/coworker.md)
* [Product](../billing/product.md)
* [CannedResponse](../crm/cannedresponse.md)
