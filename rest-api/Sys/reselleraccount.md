{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/reselleraccounts" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of reselleraccounts based on one or more filter querystring parameters.
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
?ResellerAccount\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Reseller" type="Reseller" %}
?ResellerAccount\_Reseller=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?ResellerAccount\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="Approved" type="bool" %}
?ResellerAccount\_Approved=...
{% endapi-method-parameter %}


{% api-method-parameter name="ComissionPercentage" type="decimal" %}
?ResellerAccount\_ComissionPercentage=...
{% endapi-method-parameter %}


{% api-method-parameter name="NextPayoutDate" type="DateTime?" %}
?ResellerAccount\_NextPayoutDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="ExpirationDate" type="DateTime?" %}
?ResellerAccount\_ExpirationDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="LastAccess" type="DateTime?" %}
?ResellerAccount\_LastAccess=...
{% endapi-method-parameter %}


{% api-method-parameter name="LastInvoiceAmount" type="decimal?" %}
?ResellerAccount\_LastInvoiceAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="AverageInvoiceAmount" type="decimal?" %}
?ResellerAccount\_AverageInvoiceAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="CanManageAccount" type="bool" %}
?ResellerAccount\_CanManageAccount=...
{% endapi-method-parameter %}


{% api-method-parameter name="Reseller\_Currency_Id" type="string" %}
?ResellerAccount\_Reseller\_Currency_Id=...
{% endapi-method-parameter %}


{% api-method-parameter name="Reseller\_Currency_Code" type="string" %}
?ResellerAccount\_Reseller\_Currency_Code=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business\_Name" type="string" %}
?ResellerAccount\_Business\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business\_PreAuthId" type="string" %}
?ResellerAccount\_Business\_PreAuthId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business\_Last4Digits" type="string" %}
?ResellerAccount\_Business\_Last4Digits=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business\_PreAuthLastError" type="string" %}
?ResellerAccount\_Business\_PreAuthLastError=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business\_Suspended" type="string" %}
?ResellerAccount\_Business\_Suspended=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business\_NextInvoice" type="string" %}
?ResellerAccount\_Business\_NextInvoice=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business\_TrialExpireDate" type="string" %}
?ResellerAccount\_Business\_TrialExpireDate=...
{% endapi-method-parameter %}


{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "Reseller": null,
        "Business": null,
        "Approved": false,
        "ComissionPercentage": 0,
        "NextPayoutDate": 2019-01-01,
        "ExpirationDate": 2019-01-01,
        "LastAccess": ,
        "LastInvoiceAmount": ,
        "AverageInvoiceAmount": ,
        "CanManageAccount": false,
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

> 🔒 Requires user role `reselleraccount-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/reselleraccounts" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of reselleraccounts.
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
        "Reseller": null,
        "Business": null,
        "Approved": false,
        "ComissionPercentage": 0,
        "NextPayoutDate": 2019-01-01,
        "ExpirationDate": 2019-01-01,
        "LastAccess": ,
        "LastInvoiceAmount": ,
        "AverageInvoiceAmount": ,
        "CanManageAccount": false,
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

> 🔒 Requires user role `reselleraccount-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/reselleraccounts" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of reselleraccounts based on the date when they were created or updated.
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
?to\_ResellerAccount\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_ResellerAccount\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_ResellerAccount\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_ResellerAccount\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="ComissionPercentage" type="decimal" required=false %}
?from\_ResellerAccount\_ComissionPercentage=...
{% endapi-method-parameter %}
{% api-method-parameter name="ComissionPercentage" type="decimal" required=false %}
?to\_ResellerAccount\_ComissionPercentage=...
{% endapi-method-parameter %}
{% api-method-parameter name="NextPayoutDate" type="datetime" required=false %}
?from\_ResellerAccount\_NextPayoutDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="NextPayoutDate" type="datetime" required=false %}
?to\_ResellerAccount\_NextPayoutDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="ExpirationDate" type="datetime" required=false %}
?from\_ResellerAccount\_ExpirationDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="ExpirationDate" type="datetime" required=false %}
?to\_ResellerAccount\_ExpirationDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="LastAccess" type="datetime" required=false %}
?from\_ResellerAccount\_LastAccess=...
{% endapi-method-parameter %}
{% api-method-parameter name="LastAccess" type="datetime" required=false %}
?to\_ResellerAccount\_LastAccess=...
{% endapi-method-parameter %}
{% api-method-parameter name="LastInvoiceAmount" type="decimal" required=false %}
?from\_ResellerAccount\_LastInvoiceAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="LastInvoiceAmount" type="decimal" required=false %}
?to\_ResellerAccount\_LastInvoiceAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="AverageInvoiceAmount" type="decimal" required=false %}
?from\_ResellerAccount\_AverageInvoiceAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="AverageInvoiceAmount" type="decimal" required=false %}
?to\_ResellerAccount\_AverageInvoiceAmount=...
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
        "Reseller": null,
        "Business": null,
        "Approved": false,
        "ComissionPercentage": 0,
        "NextPayoutDate": 2019-01-01,
        "ExpirationDate": 2019-01-01,
        "LastAccess": ,
        "LastInvoiceAmount": ,
        "AverageInvoiceAmount": ,
        "CanManageAccount": false,
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

> 🔒 Requires user role `reselleraccount-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/reselleraccounts/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one reselleraccount record.
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
The ID of the reselleraccount to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "Reseller": null,
        "Business": null,
        "Approved": false,
        "ComissionPercentage": 0,
        "NextPayoutDate": 2019-01-01,
        "ExpirationDate": 2019-01-01,
        "LastAccess": ,
        "LastInvoiceAmount": ,
        "AverageInvoiceAmount": ,
        "CanManageAccount": false,
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

> 🔒 Requires user role `reselleraccount-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/sys/reselleraccounts" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new reselleraccount.
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
{% api-method-parameter name="ResellerId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BusinessId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Approved" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ComissionPercentage" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="NextPayoutDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ExpirationDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="LastAccess" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="LastInvoiceAmount" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AverageInvoiceAmount" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CanManageAccount" type="bool" required=false %}
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

> 🔒 Requires user role `reselleraccount-create`

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/sys/reselleraccounts" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing reselleraccount.
  
Required User Role: `reselleraccount-edit`
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
The id of the reselleraccount to update
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

> 🔒 Requires user role `reselleraccount-edit`


{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/sys/reselleraccounts/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a reselleraccount.  
  
Required User Roles: `reselleraccount-delete`
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



> 🔒 Requires user role `reselleraccount-delete`


## Commands

Commands allow to perform actions against one or more reselleraccount records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/reselleraccounts/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for reselleraccount records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/reselleraccounts/runcommand" %}
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

> 🔒 Requires user role `reselleraccount-edit`

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [Reseller](../sys/reseller.md)
* [Business](../sys/business.md)
