{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmboardcolumns" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of crmboardcolumns based on one or more filter querystring parameters.
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
?CrmBoardColumn\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="CrmBoard" type="CrmBoard" %}
?CrmBoardColumn\_CrmBoard=...
{% endapi-method-parameter %}


{% api-method-parameter name="Name" type="string" %}
?CrmBoardColumn\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="Position" type="int" %}
?CrmBoardColumn\_Position=...
{% endapi-method-parameter %}


{% api-method-parameter name="TourRequests" type="bool" %}
?CrmBoardColumn\_TourRequests=...
{% endapi-method-parameter %}


{% api-method-parameter name="ToursConfirmed" type="bool" %}
?CrmBoardColumn\_ToursConfirmed=...
{% endapi-method-parameter %}


{% api-method-parameter name="TourCompleted" type="bool" %}
?CrmBoardColumn\_TourCompleted=...
{% endapi-method-parameter %}


{% api-method-parameter name="SignUps" type="bool" %}
?CrmBoardColumn\_SignUps=...
{% endapi-method-parameter %}


{% api-method-parameter name="Bookings" type="bool" %}
?CrmBoardColumn\_Bookings=...
{% endapi-method-parameter %}


{% api-method-parameter name="Cancellations" type="bool" %}
?CrmBoardColumn\_Cancellations=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProposalsSent" type="bool" %}
?CrmBoardColumn\_ProposalsSent=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProposalsAccepted" type="bool" %}
?CrmBoardColumn\_ProposalsAccepted=...
{% endapi-method-parameter %}


{% api-method-parameter name="DocumentsSigned" type="bool" %}
?CrmBoardColumn\_DocumentsSigned=...
{% endapi-method-parameter %}


{% api-method-parameter name="EventRegistrations" type="bool" %}
?CrmBoardColumn\_EventRegistrations=...
{% endapi-method-parameter %}


{% api-method-parameter name="ContactMessages" type="bool" %}
?CrmBoardColumn\_ContactMessages=...
{% endapi-method-parameter %}


{% api-method-parameter name="CannedResponse" type="CannedResponse" %}
?CrmBoardColumn\_CannedResponse=...
{% endapi-method-parameter %}


{% api-method-parameter name="TaskList" type="TaskList" %}
?CrmBoardColumn\_TaskList=...
{% endapi-method-parameter %}


{% api-method-parameter name="ActivateAccount" type="bool" %}
?CrmBoardColumn\_ActivateAccount=...
{% endapi-method-parameter %}


{% api-method-parameter name="DeactivateAccount" type="bool" %}
?CrmBoardColumn\_DeactivateAccount=...
{% endapi-method-parameter %}


{% api-method-parameter name="ConfirmTour" type="bool" %}
?CrmBoardColumn\_ConfirmTour=...
{% endapi-method-parameter %}


{% api-method-parameter name="CrmBoard\_Name" type="string" %}
?CrmBoardColumn\_CrmBoard\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="CrmBoard\_Business_Id" type="string" %}
?CrmBoardColumn\_CrmBoard\_Business_Id=...
{% endapi-method-parameter %}


{% api-method-parameter name="CrmBoard\_Business_Name" type="string" %}
?CrmBoardColumn\_CrmBoard\_Business_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="CrmBoard\_Business_Currency_Id" type="string" %}
?CrmBoardColumn\_CrmBoard\_Business_Currency_Id=...
{% endapi-method-parameter %}


{% api-method-parameter name="CrmBoard\_Business_Currency_Code" type="string" %}
?CrmBoardColumn\_CrmBoard\_Business_Currency_Code=...
{% endapi-method-parameter %}


{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "CrmBoard": null,
        "Name": "Joe",
        "Position": 1,
        "TourRequests": true,
        "ToursConfirmed": true,
        "TourCompleted": true,
        "SignUps": true,
        "Bookings": true,
        "Cancellations": true,
        "ProposalsSent": true,
        "ProposalsAccepted": true,
        "DocumentsSigned": true,
        "EventRegistrations": true,
        "ContactMessages": true,
        "CannedResponse": null,
        "TaskList": null,
        "ActivateAccount": true,
        "DeactivateAccount": false,
        "ConfirmTour": false,
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

> 🔒 Requires user role `crmboardcolumn-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmboardcolumns" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of crmboardcolumns.
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
        "CrmBoard": null,
        "Name": "Joe",
        "Position": 1,
        "TourRequests": true,
        "ToursConfirmed": true,
        "TourCompleted": true,
        "SignUps": true,
        "Bookings": true,
        "Cancellations": true,
        "ProposalsSent": true,
        "ProposalsAccepted": true,
        "DocumentsSigned": true,
        "EventRegistrations": true,
        "ContactMessages": true,
        "CannedResponse": null,
        "TaskList": null,
        "ActivateAccount": true,
        "DeactivateAccount": false,
        "ConfirmTour": false,
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

> 🔒 Requires user role `crmboardcolumn-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmboardcolumns" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of crmboardcolumns based on a range of dates, integer or decimal properties.
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
?to\_CrmBoardColumn\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_CrmBoardColumn\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_CrmBoardColumn\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_CrmBoardColumn\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Position" type="int" required=false %}
?from\_CrmBoardColumn\_Position=...
{% endapi-method-parameter %}
{% api-method-parameter name="Position" type="int" required=false %}
?to\_CrmBoardColumn\_Position=...
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
        "CrmBoard": null,
        "Name": "Joe",
        "Position": 1,
        "TourRequests": true,
        "ToursConfirmed": true,
        "TourCompleted": true,
        "SignUps": true,
        "Bookings": true,
        "Cancellations": true,
        "ProposalsSent": true,
        "ProposalsAccepted": true,
        "DocumentsSigned": true,
        "EventRegistrations": true,
        "ContactMessages": true,
        "CannedResponse": null,
        "TaskList": null,
        "ActivateAccount": true,
        "DeactivateAccount": false,
        "ConfirmTour": false,
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

> 🔒 Requires user role `crmboardcolumn-list`


{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmboardcolumns?CrmBoardColumn_Id=[:id1,:id2,...]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more crmboardcolumn records based on their Id.
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
Comma-separated list of IDs of every crmboardcolumn to fetch. I.e. [123456,789102,...] 
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "CrmBoard": null,
        "Name": "Joe",
        "Position": 1,
        "TourRequests": true,
        "ToursConfirmed": true,
        "TourCompleted": true,
        "SignUps": true,
        "Bookings": true,
        "Cancellations": true,
        "ProposalsSent": true,
        "ProposalsAccepted": true,
        "DocumentsSigned": true,
        "EventRegistrations": true,
        "ContactMessages": true,
        "CannedResponse": null,
        "TaskList": null,
        "ActivateAccount": true,
        "DeactivateAccount": false,
        "ConfirmTour": false,
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

> 🔒 Requires user role `crmboardcolumn-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmboardcolumns/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one crmboardcolumn record.
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
The ID of the crmboardcolumn to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "CrmBoard": null,
        "Name": "Joe",
        "Position": 1,
        "TourRequests": true,
        "ToursConfirmed": true,
        "TourCompleted": true,
        "SignUps": true,
        "Bookings": true,
        "Cancellations": true,
        "ProposalsSent": true,
        "ProposalsAccepted": true,
        "DocumentsSigned": true,
        "EventRegistrations": true,
        "ContactMessages": true,
        "CannedResponse": null,
        "TaskList": null,
        "ActivateAccount": true,
        "DeactivateAccount": false,
        "ConfirmTour": false,
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

> 🔒 Requires user role `crmboardcolumn-read`


{% api-method method="post" host="https://spaces.nexudus.com/api" path="/crm/crmboardcolumns" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new crmboardcolumn.
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
{% api-method-parameter name="CrmBoardId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Position" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TourRequests" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ToursConfirmed" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TourCompleted" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="SignUps" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Bookings" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Cancellations" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProposalsSent" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProposalsAccepted" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DocumentsSigned" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="EventRegistrations" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ContactMessages" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CannedResponseId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaskListId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ActivateAccount" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DeactivateAccount" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ConfirmTour" type="bool" required=false %}
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

> 🔒 Requires user role `crmboardcolumn-create`

```javascript
{
	"CrmBoard": 12345678,
	"Name": "Joe",
	"Position": 1,
	"TourRequests": true,
	"ToursConfirmed": true,
	"TourCompleted": true,
	"SignUps": true,
	"Bookings": true,
	"Cancellations": true,
	"ProposalsSent": true,
	"ProposalsAccepted": true,
	"DocumentsSigned": true,
	"EventRegistrations": true,
	"ContactMessages": true,
	"CannedResponse": 12345678,
	"TaskList": 12345678,
	"ActivateAccount": true,
	"DeactivateAccount": false,
	"ConfirmTour": false,
}

```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/crm/crmboardcolumns" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing crmboardcolumn.
  
Required User Role: `crmboardcolumn-edit`
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
The id of the crmboardcolumn to update
{% api-method-parameter name="CrmBoardId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Position" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TourRequests" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ToursConfirmed" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TourCompleted" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="SignUps" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Bookings" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Cancellations" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProposalsSent" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProposalsAccepted" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DocumentsSigned" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="EventRegistrations" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ContactMessages" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CannedResponseId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaskListId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ActivateAccount" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DeactivateAccount" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ConfirmTour" type="bool" required=false %}
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

> 🔒 Requires user role `crmboardcolumn-edit`

```javascript
{
	"CrmBoard": 12345678,
	"Name": "Joe",
	"Position": 1,
	"TourRequests": true,
	"ToursConfirmed": true,
	"TourCompleted": true,
	"SignUps": true,
	"Bookings": true,
	"Cancellations": true,
	"ProposalsSent": true,
	"ProposalsAccepted": true,
	"DocumentsSigned": true,
	"EventRegistrations": true,
	"ContactMessages": true,
	"CannedResponse": 12345678,
	"TaskList": 12345678,
	"ActivateAccount": true,
	"DeactivateAccount": false,
	"ConfirmTour": false,
}

```




{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/crm/crmboardcolumns/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a crmboardcolumn.  
  
Required User Roles: `crmboardcolumn-delete`
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



> 🔒 Requires user role `crmboardcolumn-delete`


## Commands

Commands allow to perform actions against one or more crmboardcolumn records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmboardcolumns/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for crmboardcolumn records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmboardcolumns/runcommand" %}
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

> 🔒 Requires user role `crmboardcolumn-edit`

## Enumerated values

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [CrmBoard](../crm/crmboard.md)
* [CannedResponse](../crm/cannedresponse.md)
* [TaskList](../crm/tasklist.md)
