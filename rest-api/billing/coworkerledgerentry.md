# CoworkerLedgerEntry

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerledgerentries" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkerledgerentries based on one or more filter querystring parameters.
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
?CoworkerLedgerEntry\_SystemId=...
{% endapi-method-parameter %}

{% api-method-parameter name="Business" type="Business" %}
?CoworkerLedgerEntry\_Business=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker" type="Coworker" %}
?CoworkerLedgerEntry\_Coworker=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoice" type="CoworkerInvoice" %}
?CoworkerLedgerEntry\_CoworkerInvoice=...
{% endapi-method-parameter %}

{% api-method-parameter name="Description" type="string" %}
?CoworkerLedgerEntry\_Description=...
{% endapi-method-parameter %}

{% api-method-parameter name="Code" type="string" %}
?CoworkerLedgerEntry\_Code=...
{% endapi-method-parameter %}

{% api-method-parameter name="Debit" type="decimal" %}
?CoworkerLedgerEntry\_Debit=...
{% endapi-method-parameter %}

{% api-method-parameter name="Credit" type="decimal" %}
?CoworkerLedgerEntry\_Credit=...
{% endapi-method-parameter %}

{% api-method-parameter name="PaymentGatewayName" type="enum" %}
?CoworkerLedgerEntry\_PaymentGatewayName=...
{% endapi-method-parameter %}

{% api-method-parameter name="PaymentMethodNumber" type="string" %}
?CoworkerLedgerEntry\_PaymentMethodNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="TransactionDate" type="DateTime?" %}
?CoworkerLedgerEntry\_TransactionDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="Balance" type="decimal" %}
?CoworkerLedgerEntry\_Balance=...
{% endapi-method-parameter %}

{% api-method-parameter name="ConnectedTransactionGuid" type="Guid?" %}
?CoworkerLedgerEntry\_ConnectedTransactionGuid=...
{% endapi-method-parameter %}

{% api-method-parameter name="Business\_Name" type="string" %}
?CoworkerLedgerEntry\_Business\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Business\_Currency\_Code" type="string" %}
?CoworkerLedgerEntry\_Business\_Currency\_Code=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_FullName" type="string" %}
?CoworkerLedgerEntry\_Coworker\_FullName=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoice\_InvoiceNumber" type="string" %}
?CoworkerLedgerEntry\_CoworkerInvoice\_InvoiceNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoice\_TotalAmount" type="string" %}
?CoworkerLedgerEntry\_CoworkerInvoice\_TotalAmount=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoice\_BillToName" type="string" %}
?CoworkerLedgerEntry\_CoworkerInvoice\_BillToName=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoice\_Paid" type="string" %}
?CoworkerLedgerEntry\_CoworkerInvoice\_Paid=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoice\_PaidOn" type="string" %}
?CoworkerLedgerEntry\_CoworkerInvoice\_PaidOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoice\_Refunded" type="string" %}
?CoworkerLedgerEntry\_CoworkerInvoice\_Refunded=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoice\_RefundedOn" type="string" %}
?CoworkerLedgerEntry\_CoworkerInvoice\_RefundedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoice\_DueDate" type="string" %}
?CoworkerLedgerEntry\_CoworkerInvoice\_DueDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoice\_Draft" type="string" %}
?CoworkerLedgerEntry\_CoworkerInvoice\_Draft=...
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
        "Coworker": null,
        "CoworkerInvoice": null,
        "Description": "Descripción",
        "Code": "00001",
        "Debit": 0,
        "Credit": 0,
        "PaymentGatewayName": Nexudus.Coworking.Core.Enums.ePaymentProvider.Manual,
        "PaymentMethodNumber": "0",
        "TransactionDate": 0,
        "Balance": 0,
        "ConnectedTransactionGuid": ,
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

> 🔒 Requires user role `coworkerledgerentry-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerledgerentries" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkerledgerentries.
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
        "Coworker": null,
        "CoworkerInvoice": null,
        "Description": "Descripción",
        "Code": "00001",
        "Debit": 0,
        "Credit": 0,
        "PaymentGatewayName": Nexudus.Coworking.Core.Enums.ePaymentProvider.Manual,
        "PaymentMethodNumber": "0",
        "TransactionDate": 0,
        "Balance": 0,
        "ConnectedTransactionGuid": ,
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

> 🔒 Requires user role `coworkerledgerentry-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerledgerentries" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of coworkerledgerentries based on the date when they were created or updated.
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
?to\_CoworkerLedgerEntry\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_CoworkerLedgerEntry\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_CoworkerLedgerEntry\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Debit" type="decimal" required=false %}
?from\_CoworkerLedgerEntry\_Debit=...
{% endapi-method-parameter %}

{% api-method-parameter name="Debit" type="decimal" required=false %}
?to\_CoworkerLedgerEntry\_Debit=...
{% endapi-method-parameter %}

{% api-method-parameter name="Credit" type="decimal" required=false %}
?from\_CoworkerLedgerEntry\_Credit=...
{% endapi-method-parameter %}

{% api-method-parameter name="Credit" type="decimal" required=false %}
?to\_CoworkerLedgerEntry\_Credit=...
{% endapi-method-parameter %}

{% api-method-parameter name="TransactionDate" type="datetime" required=false %}
?from\_CoworkerLedgerEntry\_TransactionDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="TransactionDate" type="datetime" required=false %}
?to\_CoworkerLedgerEntry\_TransactionDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="Balance" type="decimal" required=false %}
?from\_CoworkerLedgerEntry\_Balance=...
{% endapi-method-parameter %}

{% api-method-parameter name="Balance" type="decimal" required=false %}
?to\_CoworkerLedgerEntry\_Balance=...
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
        "Coworker": null,
        "CoworkerInvoice": null,
        "Description": "Descripción",
        "Code": "00001",
        "Debit": 0,
        "Credit": 0,
        "PaymentGatewayName": Nexudus.Coworking.Core.Enums.ePaymentProvider.Manual,
        "PaymentMethodNumber": "0",
        "TransactionDate": 0,
        "Balance": 0,
        "ConnectedTransactionGuid": ,
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

> 🔒 Requires user role `coworkerledgerentry-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerledgerentries/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one coworkerledgerentry record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the coworkerledgerentry to fetch.
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
        "Coworker": null,
        "CoworkerInvoice": null,
        "Description": "Descripción",
        "Code": "00001",
        "Debit": 0,
        "Credit": 0,
        "PaymentGatewayName": Nexudus.Coworking.Core.Enums.ePaymentProvider.Manual,
        "PaymentMethodNumber": "0",
        "TransactionDate": 0,
        "Balance": 0,
        "ConnectedTransactionGuid": ,
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

> 🔒 Requires user role `coworkerledgerentry-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/coworkerledgerentries" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new coworkerledgerentry.
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

{% api-method-parameter name="CoworkerId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoiceId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Description" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Code" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Debit" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Credit" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="PaymentGatewayName" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PaymentMethodNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TransactionDate" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Balance" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="ConnectedTransactionGuid" type="Guid?" required=false %}

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

> 🔒 Requires user role `coworkerledgerentry-create`

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/coworkerledgerentries" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing coworkerledgerentry.Required User Role: `coworkerledgerentry-edit`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="Id" type="integer" required=true %}
The id of the coworkerledgerentry to update
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

{% api-method-parameter name="CoworkerId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoiceId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Description" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Code" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Debit" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Credit" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="PaymentMethodNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TransactionDate" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Balance" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="ConnectedTransactionGuid" type="Guid?" required=false %}

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

> 🔒 Requires user role `coworkerledgerentry-edit`

{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/billing/coworkerledgerentries/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a coworkerledgerentry.Required User Roles: `coworkerledgerentry-delete`
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

> 🔒 Requires user role `coworkerledgerentry-delete`

## Commands

Commands allow to perform actions against one or more coworkerledgerentry records. Some commands accept only one record while others can run an action for a number of records at the same time. Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerledgerentries/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for coworkerledgerentry records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerledgerentries/runcommand" %}
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

> 🔒 Requires user role `coworkerledgerentry-edit`

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

## Related Entities

* [Business](../sys/business.md)
* [Coworker](../spaces/coworker.md)
* [CoworkerInvoice](coworkerinvoice.md)

