{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/invoices" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of invoices based on one or more filter querystring parameters.
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
?Invoice\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?Invoice\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceNumber" type="string" %}
?Invoice\_InvoiceNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToName" type="string" %}
?Invoice\_BillToName=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToAddress" type="string" %}
?Invoice\_BillToAddress=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToCity" type="string" %}
?Invoice\_BillToCity=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToTaxIDNumber" type="string" %}
?Invoice\_BillToTaxIDNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToPostCode" type="string" %}
?Invoice\_BillToPostCode=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToPhone" type="string" %}
?Invoice\_BillToPhone=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToFax" type="string" %}
?Invoice\_BillToFax=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToCountry" type="Country" %}
?Invoice\_BillToCountry=...
{% endapi-method-parameter %}


{% api-method-parameter name="Description" type="string" %}
?Invoice\_Description=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountAmount" type="decimal" %}
?Invoice\_DiscountAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="DueDate" type="DateTime?" %}
?Invoice\_DueDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceFromDate" type="DateTime?" %}
?Invoice\_InvoiceFromDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceToDate" type="DateTime?" %}
?Invoice\_InvoiceToDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="TotalAmount" type="decimal" %}
?Invoice\_TotalAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="Currency" type="Currency" %}
?Invoice\_Currency=...
{% endapi-method-parameter %}


{% api-method-parameter name="TaxAmount" type="decimal" %}
?Invoice\_TaxAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="Paid" type="bool" %}
?Invoice\_Paid=...
{% endapi-method-parameter %}


{% api-method-parameter name="PaidOn" type="DateTime?" %}
?Invoice\_PaidOn=...
{% endapi-method-parameter %}


{% api-method-parameter name="CustomData" type="string" %}
?Invoice\_CustomData=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillToCountry\_Name" type="string" %}
?Invoice\_BillToCountry\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="Currency\_Code" type="string" %}
?Invoice\_Currency\_Code=...
{% endapi-method-parameter %}


{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "Business": null,
        "InvoiceNumber": "00001",
        "BillToName": "BillToName",
        "BillToAddress": "BillToAddress",
        "BillToCity": "BillToCity",
        "BillToTaxIDNumber": "123456",
        "BillToPostCode": "BillToPostCode",
        "BillToPhone": "BillToPhone",
        "BillToFax": "BillToFax",
        "BillToCountry": null,
        "Description": "[DataType(DataType.MultilineText)]",
        "DiscountAmount": 0,
        "DueDate": null,
        "InvoiceFromDate": null,
        "InvoiceToDate": null,
        "TotalAmount": 0,
        "Currency": null,
        "TaxAmount": 0,
        "Paid": false,
        "PaidOn": null,
        "CustomData": "null",
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

> 🔒 Requires user role `invoice-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/invoices" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of invoices.
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
        "InvoiceNumber": "00001",
        "BillToName": "BillToName",
        "BillToAddress": "BillToAddress",
        "BillToCity": "BillToCity",
        "BillToTaxIDNumber": "123456",
        "BillToPostCode": "BillToPostCode",
        "BillToPhone": "BillToPhone",
        "BillToFax": "BillToFax",
        "BillToCountry": null,
        "Description": "[DataType(DataType.MultilineText)]",
        "DiscountAmount": 0,
        "DueDate": null,
        "InvoiceFromDate": null,
        "InvoiceToDate": null,
        "TotalAmount": 0,
        "Currency": null,
        "TaxAmount": 0,
        "Paid": false,
        "PaidOn": null,
        "CustomData": "null",
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

> 🔒 Requires user role `invoice-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/invoices" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of invoices based on the date when they were created or updated.
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
?to\_Invoice\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_Invoice\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_Invoice\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountAmount" type="decimal" required=false %}
?from\_Invoice\_DiscountAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountAmount" type="decimal" required=false %}
?to\_Invoice\_DiscountAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="datetime" required=false %}
?from\_Invoice\_DueDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="datetime" required=false %}
?to\_Invoice\_DueDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceFromDate" type="datetime" required=false %}
?from\_Invoice\_InvoiceFromDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceFromDate" type="datetime" required=false %}
?to\_Invoice\_InvoiceFromDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceToDate" type="datetime" required=false %}
?from\_Invoice\_InvoiceToDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceToDate" type="datetime" required=false %}
?to\_Invoice\_InvoiceToDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="TotalAmount" type="decimal" required=false %}
?from\_Invoice\_TotalAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="TotalAmount" type="decimal" required=false %}
?to\_Invoice\_TotalAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="TaxAmount" type="decimal" required=false %}
?from\_Invoice\_TaxAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="TaxAmount" type="decimal" required=false %}
?to\_Invoice\_TaxAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="PaidOn" type="datetime" required=false %}
?from\_Invoice\_PaidOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="PaidOn" type="datetime" required=false %}
?to\_Invoice\_PaidOn=...
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
        "InvoiceNumber": "00001",
        "BillToName": "BillToName",
        "BillToAddress": "BillToAddress",
        "BillToCity": "BillToCity",
        "BillToTaxIDNumber": "123456",
        "BillToPostCode": "BillToPostCode",
        "BillToPhone": "BillToPhone",
        "BillToFax": "BillToFax",
        "BillToCountry": null,
        "Description": "[DataType(DataType.MultilineText)]",
        "DiscountAmount": 0,
        "DueDate": null,
        "InvoiceFromDate": null,
        "InvoiceToDate": null,
        "TotalAmount": 0,
        "Currency": null,
        "TaxAmount": 0,
        "Paid": false,
        "PaidOn": null,
        "CustomData": "null",
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

> 🔒 Requires user role `invoice-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/invoices/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one invoice record.
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
The ID of the invoice to fetch.
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
        "InvoiceNumber": "00001",
        "BillToName": "BillToName",
        "BillToAddress": "BillToAddress",
        "BillToCity": "BillToCity",
        "BillToTaxIDNumber": "123456",
        "BillToPostCode": "BillToPostCode",
        "BillToPhone": "BillToPhone",
        "BillToFax": "BillToFax",
        "BillToCountry": null,
        "Description": "[DataType(DataType.MultilineText)]",
        "DiscountAmount": 0,
        "DueDate": null,
        "InvoiceFromDate": null,
        "InvoiceToDate": null,
        "TotalAmount": 0,
        "Currency": null,
        "TaxAmount": 0,
        "Paid": false,
        "PaidOn": null,
        "CustomData": "null",
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

> 🔒 Requires user role `invoice-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/invoices" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new invoice.
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
{% api-method-parameter name="InvoiceNumber" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToName" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToAddress" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToCity" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToTaxIDNumber" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToPostCode" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToPhone" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToFax" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToCountryId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Description" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountAmount" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceFromDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceToDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TotalAmount" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="CurrencyId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaxAmount" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Paid" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PaidOn" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CustomData" type="string" required=false %}
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

> 🔒 Requires user role `invoice-create`

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/invoices" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing invoice.
  
Required User Role: `invoice-edit`
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
{% api-method-parameter name="Id" type="integer" required=true %}
The id of the invoice to update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="BusinessId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceNumber" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToName" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToAddress" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToCity" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToTaxIDNumber" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToPostCode" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToPhone" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToFax" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillToCountryId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Description" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountAmount" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceFromDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceToDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TotalAmount" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="CurrencyId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaxAmount" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Paid" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PaidOn" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CustomData" type="string" required=false %}
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

> 🔒 Requires user role `invoice-edit`


## Commands

Commands allow to perform actions against one or more invoice records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/invoices/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for invoice records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/invoices/runcommand" %}
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

> 🔒 Requires user role `invoice-edit`

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [Business](../sys/business.md)
* [Country](../sys/country.md)
* [Currency](../sys/currency.md)
