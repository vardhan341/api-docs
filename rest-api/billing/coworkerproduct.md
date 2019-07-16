{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerproducts" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkerproducts based on one or more filter querystring parameters.
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
?CoworkerProduct\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker" type="Coworker" %}
?CoworkerProduct\_Coworker=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?CoworkerProduct\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="Product" type="Product" %}
?CoworkerProduct\_Product=...
{% endapi-method-parameter %}


{% api-method-parameter name="Notes" type="string" %}
?CoworkerProduct\_Notes=...
{% endapi-method-parameter %}


{% api-method-parameter name="OrderNumber" type="string" %}
?CoworkerProduct\_OrderNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="Activated" type="bool" %}
?CoworkerProduct\_Activated=...
{% endapi-method-parameter %}


{% api-method-parameter name="ActivateNow" type="bool" %}
?CoworkerProduct\_ActivateNow=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceThisCoworker" type="bool" %}
?CoworkerProduct\_InvoiceThisCoworker=...
{% endapi-method-parameter %}


{% api-method-parameter name="Price" type="decimal?" %}
?CoworkerProduct\_Price=...
{% endapi-method-parameter %}


{% api-method-parameter name="Quantity" type="int" %}
?CoworkerProduct\_Quantity=...
{% endapi-method-parameter %}


{% api-method-parameter name="RegularCharge" type="bool" %}
?CoworkerProduct\_RegularCharge=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatCycle" type="enum" %}
?CoworkerProduct\_RepeatCycle=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatUnit" type="int?" %}
?CoworkerProduct\_RepeatUnit=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceOn" type="DateTime?" %}
?CoworkerProduct\_InvoiceOn=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatFrom" type="DateTime?" %}
?CoworkerProduct\_RepeatFrom=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatUntil" type="DateTime?" %}
?CoworkerProduct\_RepeatUntil=...
{% endapi-method-parameter %}


{% api-method-parameter name="DueDate" type="DateTime?" %}
?CoworkerProduct\_DueDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="Invoiced" type="bool" %}
?CoworkerProduct\_Invoiced=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoicedOn" type="DateTime?" %}
?CoworkerProduct\_InvoicedOn=...
{% endapi-method-parameter %}


{% api-method-parameter name="FromTariff" type="bool" %}
?CoworkerProduct\_FromTariff=...
{% endapi-method-parameter %}


{% api-method-parameter name="ContractDepositUniqueId" type="Guid?" %}
?CoworkerProduct\_ContractDepositUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Product\_Name" type="string" %}
?CoworkerProduct\_Product\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="Product\_Price" type="string" %}
?CoworkerProduct\_Product\_Price=...
{% endapi-method-parameter %}


{% api-method-parameter name="Product\_Currency_Code" type="string" %}
?CoworkerProduct\_Product\_Currency_Code=...
{% endapi-method-parameter %}


{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "Coworker": null,
        "Business": null,
        "Product": null,
        "Notes": "Notes",
        "OrderNumber": "null",
        "Activated": false,
        "ActivateNow": true,
        "InvoiceThisCoworker": false,
        "Price": false,
        "Quantity": 1,
        "RegularCharge": false,
        "RepeatCycle": Nexudus.Coworking.Core.Enums.eRecurrentChargePattern.PricePlan,
        "RepeatUnit": 1,
        "InvoiceOn": null,
        "RepeatFrom": null,
        "RepeatUntil": null,
        "DueDate": null,
        "Invoiced": false,
        "InvoicedOn": null,
        "FromTariff": false,
        "ContractDepositUniqueId": ,
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

> 🔒 Requires user role `coworkerproduct-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerproducts" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkerproducts.
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
        "Coworker": null,
        "Business": null,
        "Product": null,
        "Notes": "Notes",
        "OrderNumber": "null",
        "Activated": false,
        "ActivateNow": true,
        "InvoiceThisCoworker": false,
        "Price": false,
        "Quantity": 1,
        "RegularCharge": false,
        "RepeatCycle": Nexudus.Coworking.Core.Enums.eRecurrentChargePattern.PricePlan,
        "RepeatUnit": 1,
        "InvoiceOn": null,
        "RepeatFrom": null,
        "RepeatUntil": null,
        "DueDate": null,
        "Invoiced": false,
        "InvoicedOn": null,
        "FromTariff": false,
        "ContractDepositUniqueId": ,
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

> 🔒 Requires user role `coworkerproduct-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerproducts" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of coworkerproducts based on a range of dates, integer or decimal properties.
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
?to\_CoworkerProduct\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_CoworkerProduct\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_CoworkerProduct\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_CoworkerProduct\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=false %}
?from\_CoworkerProduct\_Price=...
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal" required=false %}
?to\_CoworkerProduct\_Price=...
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="int" required=false %}
?from\_CoworkerProduct\_Quantity=...
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="int" required=false %}
?to\_CoworkerProduct\_Quantity=...
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatUnit" type="int" required=false %}
?from\_CoworkerProduct\_RepeatUnit=...
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatUnit" type="int" required=false %}
?to\_CoworkerProduct\_RepeatUnit=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceOn" type="datetime" required=false %}
?from\_CoworkerProduct\_InvoiceOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceOn" type="datetime" required=false %}
?to\_CoworkerProduct\_InvoiceOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatFrom" type="datetime" required=false %}
?from\_CoworkerProduct\_RepeatFrom=...
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatFrom" type="datetime" required=false %}
?to\_CoworkerProduct\_RepeatFrom=...
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatUntil" type="datetime" required=false %}
?from\_CoworkerProduct\_RepeatUntil=...
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatUntil" type="datetime" required=false %}
?to\_CoworkerProduct\_RepeatUntil=...
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="datetime" required=false %}
?from\_CoworkerProduct\_DueDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="datetime" required=false %}
?to\_CoworkerProduct\_DueDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoicedOn" type="datetime" required=false %}
?from\_CoworkerProduct\_InvoicedOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoicedOn" type="datetime" required=false %}
?to\_CoworkerProduct\_InvoicedOn=...
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
        "Coworker": null,
        "Business": null,
        "Product": null,
        "Notes": "Notes",
        "OrderNumber": "null",
        "Activated": false,
        "ActivateNow": true,
        "InvoiceThisCoworker": false,
        "Price": false,
        "Quantity": 1,
        "RegularCharge": false,
        "RepeatCycle": Nexudus.Coworking.Core.Enums.eRecurrentChargePattern.PricePlan,
        "RepeatUnit": 1,
        "InvoiceOn": null,
        "RepeatFrom": null,
        "RepeatUntil": null,
        "DueDate": null,
        "Invoiced": false,
        "InvoicedOn": null,
        "FromTariff": false,
        "ContractDepositUniqueId": ,
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

> 🔒 Requires user role `coworkerproduct-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerproducts/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one coworkerproduct record.
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
The ID of the coworkerproduct to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "Coworker": null,
        "Business": null,
        "Product": null,
        "Notes": "Notes",
        "OrderNumber": "null",
        "Activated": false,
        "ActivateNow": true,
        "InvoiceThisCoworker": false,
        "Price": false,
        "Quantity": 1,
        "RegularCharge": false,
        "RepeatCycle": Nexudus.Coworking.Core.Enums.eRecurrentChargePattern.PricePlan,
        "RepeatUnit": 1,
        "InvoiceOn": null,
        "RepeatFrom": null,
        "RepeatUntil": null,
        "DueDate": null,
        "Invoiced": false,
        "InvoicedOn": null,
        "FromTariff": false,
        "ContractDepositUniqueId": ,
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

> 🔒 Requires user role `coworkerproduct-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/coworkerproducts" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new coworkerproduct.
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
{% api-method-parameter name="CoworkerId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BusinessId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProductId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Notes" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ActivateNow" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceThisCoworker" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="RegularCharge" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatCycle" type="enum" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatUnit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceOn" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatFrom" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatUntil" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Invoiced" type="bool" required=false %}
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

> 🔒 Requires user role `coworkerproduct-create`

```javascript
{
	"Coworker": 12345678,
	"Business": 12345678,
	"Product": 12345678,
	"Notes": "Notes",
	"ActivateNow": true,
	"InvoiceThisCoworker": false,
	"Price": false,
	"Quantity": 1,
	"RegularCharge": false,
	"RepeatCycle": 1 (check Enumerated values section below),
	"RepeatUnit": 1,
	"InvoiceOn": null,
	"RepeatFrom": null,
	"RepeatUntil": null,
	"DueDate": null,
	"Invoiced": false,
}

```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/coworkerproducts" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing coworkerproduct.
  
Required User Role: `coworkerproduct-edit`
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
The id of the coworkerproduct to update
{% api-method-parameter name="CoworkerId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="BusinessId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProductId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Notes" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceThisCoworker" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="RegularCharge" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatCycle" type="enum" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatUnit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceOn" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatFrom" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatUntil" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Invoiced" type="bool" required=false %}
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

> 🔒 Requires user role `coworkerproduct-edit`

```javascript
{
	"Coworker": 12345678,
	"Business": 12345678,
	"Product": 12345678,
	"Notes": "Notes",
	"InvoiceThisCoworker": false,
	"Price": false,
	"Quantity": 1,
	"RegularCharge": false,
	"RepeatCycle": 1 (check Enumerated values section below),
	"RepeatUnit": 1,
	"InvoiceOn": null,
	"RepeatFrom": null,
	"RepeatUntil": null,
	"DueDate": null,
	"Invoiced": false,
}

```




{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/billing/coworkerproducts/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a coworkerproduct.  
  
Required User Roles: `coworkerproduct-delete`
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



> 🔒 Requires user role `coworkerproduct-delete`


## Commands

Commands allow to perform actions against one or more coworkerproduct records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerproducts/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for coworkerproduct records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerproducts/runcommand" %}
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

> 🔒 Requires user role `coworkerproduct-edit`

## Enumerated values

##### RepeatCycle:
> GET /api/utils/enums?name=eRecurrentChargePattern

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [Coworker](../spaces/coworker.md)
* [Business](../sys/business.md)
* [Product](../billing/product.md)
