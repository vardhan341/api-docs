{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoicelines" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkerinvoicelines based on one or more filter querystring parameters.
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
?CoworkerInvoiceLine\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerInvoice" type="CoworkerInvoice" %}
?CoworkerInvoiceLine\_CoworkerInvoice=...
{% endapi-method-parameter %}


{% api-method-parameter name="Description" type="string" %}
?CoworkerInvoiceLine\_Description=...
{% endapi-method-parameter %}


{% api-method-parameter name="TaxCategoryName" type="string" %}
?CoworkerInvoiceLine\_TaxCategoryName=...
{% endapi-method-parameter %}


{% api-method-parameter name="Quantity" type="int" %}
?CoworkerInvoiceLine\_Quantity=...
{% endapi-method-parameter %}


{% api-method-parameter name="SubTotal" type="decimal" %}
?CoworkerInvoiceLine\_SubTotal=...
{% endapi-method-parameter %}


{% api-method-parameter name="TaxAmount" type="decimal" %}
?CoworkerInvoiceLine\_TaxAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="TaxRate" type="decimal" %}
?CoworkerInvoiceLine\_TaxRate=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerContractUniqueId" type="Guid?" %}
?CoworkerInvoiceLine\_CoworkerContractUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="BookingUniqueId" type="Guid?" %}
?CoworkerInvoiceLine\_BookingUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerExtraServiceUniqueId" type="Guid?" %}
?CoworkerInvoiceLine\_CoworkerExtraServiceUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerTimePassUniqueId" type="Guid?" %}
?CoworkerInvoiceLine\_CoworkerTimePassUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerChargeUniqueId" type="Guid?" %}
?CoworkerInvoiceLine\_CoworkerChargeUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerProductUniqueId" type="Guid?" %}
?CoworkerInvoiceLine\_CoworkerProductUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="EventAttendeeUniqueId" type="Guid?" %}
?CoworkerInvoiceLine\_EventAttendeeUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="RefundedAmount" type="decimal?" %}
?CoworkerInvoiceLine\_RefundedAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="Refunded" type="bool" %}
?CoworkerInvoiceLine\_Refunded=...
{% endapi-method-parameter %}


{% api-method-parameter name="RefundedOn" type="DateTime?" %}
?CoworkerInvoiceLine\_RefundedOn=...
{% endapi-method-parameter %}


{% api-method-parameter name="SaleDate" type="DateTime?" %}
?CoworkerInvoiceLine\_SaleDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountCode" type="string" %}
?CoworkerInvoiceLine\_DiscountCode=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountAmount" type="decimal?" %}
?CoworkerInvoiceLine\_DiscountAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerExtraServiceName" type="string" %}
?CoworkerInvoiceLine\_CoworkerExtraServiceName=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerTimePassName" type="string" %}
?CoworkerInvoiceLine\_CoworkerTimePassName=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerProductName" type="string" %}
?CoworkerInvoiceLine\_CoworkerProductName=...
{% endapi-method-parameter %}


{% api-method-parameter name="EventAttendeeProductName" type="string" %}
?CoworkerInvoiceLine\_EventAttendeeProductName=...
{% endapi-method-parameter %}


{% api-method-parameter name="TariffName" type="string" %}
?CoworkerInvoiceLine\_TariffName=...
{% endapi-method-parameter %}


{% api-method-parameter name="FinancialAccountCode" type="string" %}
?CoworkerInvoiceLine\_FinancialAccountCode=...
{% endapi-method-parameter %}


{% api-method-parameter name="FinancialAccountName" type="string" %}
?CoworkerInvoiceLine\_FinancialAccountName=...
{% endapi-method-parameter %}


{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "CoworkerInvoice": null,
        "Description": "BillToName",
        "TaxCategoryName": "Joe",
        "Quantity": 1,
        "SubTotal": 0,
        "TaxAmount": 0,
        "TaxRate": 0,
        "CoworkerContractUniqueId": ,
        "BookingUniqueId": ,
        "CoworkerExtraServiceUniqueId": ,
        "CoworkerTimePassUniqueId": ,
        "CoworkerChargeUniqueId": ,
        "CoworkerProductUniqueId": ,
        "EventAttendeeUniqueId": ,
        "RefundedAmount": false,
        "Refunded": false,
        "RefundedOn": null,
        "SaleDate": null,
        "DiscountCode": "null",
        "DiscountAmount": null,
        "CoworkerExtraServiceName": "",
        "CoworkerTimePassName": "",
        "CoworkerProductName": "",
        "EventAttendeeProductName": "",
        "TariffName": "",
        "FinancialAccountCode": "",
        "FinancialAccountName": "",
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

> 🔒 Requires user role `coworkerinvoiceline-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoicelines" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkerinvoicelines.
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
        "CoworkerInvoice": null,
        "Description": "BillToName",
        "TaxCategoryName": "Joe",
        "Quantity": 1,
        "SubTotal": 0,
        "TaxAmount": 0,
        "TaxRate": 0,
        "CoworkerContractUniqueId": ,
        "BookingUniqueId": ,
        "CoworkerExtraServiceUniqueId": ,
        "CoworkerTimePassUniqueId": ,
        "CoworkerChargeUniqueId": ,
        "CoworkerProductUniqueId": ,
        "EventAttendeeUniqueId": ,
        "RefundedAmount": false,
        "Refunded": false,
        "RefundedOn": null,
        "SaleDate": null,
        "DiscountCode": "null",
        "DiscountAmount": null,
        "CoworkerExtraServiceName": "",
        "CoworkerTimePassName": "",
        "CoworkerProductName": "",
        "EventAttendeeProductName": "",
        "TariffName": "",
        "FinancialAccountCode": "",
        "FinancialAccountName": "",
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

> 🔒 Requires user role `coworkerinvoiceline-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoicelines" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of coworkerinvoicelines based on the date when they were created or updated.
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
?to\_CoworkerInvoiceLine\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_CoworkerInvoiceLine\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_CoworkerInvoiceLine\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Quantity" type="decimal" required=false %}
?from\_CoworkerInvoiceLine\_Quantity=...
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="decimal" required=false %}
?to\_CoworkerInvoiceLine\_Quantity=...
{% endapi-method-parameter %}
{% api-method-parameter name="SubTotal" type="decimal" required=false %}
?from\_CoworkerInvoiceLine\_SubTotal=...
{% endapi-method-parameter %}
{% api-method-parameter name="SubTotal" type="decimal" required=false %}
?to\_CoworkerInvoiceLine\_SubTotal=...
{% endapi-method-parameter %}
{% api-method-parameter name="TaxAmount" type="decimal" required=false %}
?from\_CoworkerInvoiceLine\_TaxAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="TaxAmount" type="decimal" required=false %}
?to\_CoworkerInvoiceLine\_TaxAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="TaxRate" type="decimal" required=false %}
?from\_CoworkerInvoiceLine\_TaxRate=...
{% endapi-method-parameter %}
{% api-method-parameter name="TaxRate" type="decimal" required=false %}
?to\_CoworkerInvoiceLine\_TaxRate=...
{% endapi-method-parameter %}
{% api-method-parameter name="RefundedAmount" type="decimal" required=false %}
?from\_CoworkerInvoiceLine\_RefundedAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="RefundedAmount" type="decimal" required=false %}
?to\_CoworkerInvoiceLine\_RefundedAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="RefundedOn" type="datetime" required=false %}
?from\_CoworkerInvoiceLine\_RefundedOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="RefundedOn" type="datetime" required=false %}
?to\_CoworkerInvoiceLine\_RefundedOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="SaleDate" type="datetime" required=false %}
?from\_CoworkerInvoiceLine\_SaleDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="SaleDate" type="datetime" required=false %}
?to\_CoworkerInvoiceLine\_SaleDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountAmount" type="decimal" required=false %}
?from\_CoworkerInvoiceLine\_DiscountAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountAmount" type="decimal" required=false %}
?to\_CoworkerInvoiceLine\_DiscountAmount=...
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
        "CoworkerInvoice": null,
        "Description": "BillToName",
        "TaxCategoryName": "Joe",
        "Quantity": 1,
        "SubTotal": 0,
        "TaxAmount": 0,
        "TaxRate": 0,
        "CoworkerContractUniqueId": ,
        "BookingUniqueId": ,
        "CoworkerExtraServiceUniqueId": ,
        "CoworkerTimePassUniqueId": ,
        "CoworkerChargeUniqueId": ,
        "CoworkerProductUniqueId": ,
        "EventAttendeeUniqueId": ,
        "RefundedAmount": false,
        "Refunded": false,
        "RefundedOn": null,
        "SaleDate": null,
        "DiscountCode": "null",
        "DiscountAmount": null,
        "CoworkerExtraServiceName": "",
        "CoworkerTimePassName": "",
        "CoworkerProductName": "",
        "EventAttendeeProductName": "",
        "TariffName": "",
        "FinancialAccountCode": "",
        "FinancialAccountName": "",
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

> 🔒 Requires user role `coworkerinvoiceline-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoicelines/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one coworkerinvoiceline record.
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
The ID of the coworkerinvoiceline to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "CoworkerInvoice": null,
        "Description": "BillToName",
        "TaxCategoryName": "Joe",
        "Quantity": 1,
        "SubTotal": 0,
        "TaxAmount": 0,
        "TaxRate": 0,
        "CoworkerContractUniqueId": ,
        "BookingUniqueId": ,
        "CoworkerExtraServiceUniqueId": ,
        "CoworkerTimePassUniqueId": ,
        "CoworkerChargeUniqueId": ,
        "CoworkerProductUniqueId": ,
        "EventAttendeeUniqueId": ,
        "RefundedAmount": false,
        "Refunded": false,
        "RefundedOn": null,
        "SaleDate": null,
        "DiscountCode": "null",
        "DiscountAmount": null,
        "CoworkerExtraServiceName": "",
        "CoworkerTimePassName": "",
        "CoworkerProductName": "",
        "EventAttendeeProductName": "",
        "TariffName": "",
        "FinancialAccountCode": "",
        "FinancialAccountName": "",
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

> 🔒 Requires user role `coworkerinvoiceline-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoicelines" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new coworkerinvoiceline.
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
{% api-method-parameter name="CoworkerInvoiceId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Description" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaxCategoryName" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="SubTotal" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaxAmount" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaxRate" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerContractUniqueId" type="Guid?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingUniqueId" type="Guid?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerExtraServiceUniqueId" type="Guid?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerTimePassUniqueId" type="Guid?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerChargeUniqueId" type="Guid?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerProductUniqueId" type="Guid?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="EventAttendeeUniqueId" type="Guid?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RefundedAmount" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Refunded" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RefundedOn" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="SaleDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountCode" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountAmount" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerExtraServiceName" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerTimePassName" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerProductName" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="EventAttendeeProductName" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TariffName" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FinancialAccountCode" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FinancialAccountName" type="string" required=false %}
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

> 🔒 Requires user role `coworkerinvoiceline-create`

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoicelines" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing coworkerinvoiceline.
  
Required User Role: `coworkerinvoiceline-edit`
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
The id of the coworkerinvoiceline to update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="CoworkerInvoiceId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Description" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaxCategoryName" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="SubTotal" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaxAmount" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaxRate" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="FinancialAccountCode" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FinancialAccountName" type="string" required=false %}
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

> 🔒 Requires user role `coworkerinvoiceline-edit`


## Commands

Commands allow to perform actions against one or more coworkerinvoiceline records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoicelines/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for coworkerinvoiceline records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerinvoicelines/runcommand" %}
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

> 🔒 Requires user role `coworkerinvoiceline-edit`

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [CoworkerInvoice](../billing/coworkerinvoice.md)
