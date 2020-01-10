{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerextraservices" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkerextraservices based on one or more filter querystring parameters.
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
?CoworkerExtraService\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker" type="Coworker" %}
?CoworkerExtraService\_Coworker=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?CoworkerExtraService\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="ExtraService" type="ExtraService" %}
?CoworkerExtraService\_ExtraService=...
{% endapi-method-parameter %}


{% api-method-parameter name="Description" type="string" %}
?CoworkerExtraService\_Description=...
{% endapi-method-parameter %}


{% api-method-parameter name="Notes" type="string" %}
?CoworkerExtraService\_Notes=...
{% endapi-method-parameter %}


{% api-method-parameter name="RemainingUses" type="int" %}
?CoworkerExtraService\_RemainingUses=...
{% endapi-method-parameter %}


{% api-method-parameter name="TotalUses" type="int" %}
?CoworkerExtraService\_TotalUses=...
{% endapi-method-parameter %}


{% api-method-parameter name="Free" type="bool" %}
?CoworkerExtraService\_Free=...
{% endapi-method-parameter %}


{% api-method-parameter name="Price" type="decimal?" %}
?CoworkerExtraService\_Price=...
{% endapi-method-parameter %}


{% api-method-parameter name="ExpireDate" type="DateTime?" %}
?CoworkerExtraService\_ExpireDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="DueDate" type="DateTime?" %}
?CoworkerExtraService\_DueDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="PurchaseOrder" type="string" %}
?CoworkerExtraService\_PurchaseOrder=...
{% endapi-method-parameter %}


{% api-method-parameter name="ChargePeriod" type="enum" %}
?CoworkerExtraService\_ChargePeriod=...
{% endapi-method-parameter %}


{% api-method-parameter name="Invoiced" type="bool" %}
?CoworkerExtraService\_Invoiced=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceDate" type="DateTime?" %}
?CoworkerExtraService\_InvoiceDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="IsFromTariff" type="bool" %}
?CoworkerExtraService\_IsFromTariff=...
{% endapi-method-parameter %}


{% api-method-parameter name="TariffTimePassUniqueId" type="Guid?" %}
?CoworkerExtraService\_TariffTimePassUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerProductUniqueId" type="Guid?" %}
?CoworkerExtraService\_CoworkerProductUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="BookingUniqueId" type="Guid?" %}
?CoworkerExtraService\_BookingUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="AutomaticallyAdded" type="bool" %}
?CoworkerExtraService\_AutomaticallyAdded=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountCode" type="string" %}
?CoworkerExtraService\_DiscountCode=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountAmount" type="decimal?" %}
?CoworkerExtraService\_DiscountAmount=...
{% endapi-method-parameter %}


{% api-method-parameter name="BookingId" type="int?" %}
?CoworkerExtraService\_BookingId=...
{% endapi-method-parameter %}


{% api-method-parameter name="BookingFromTime" type="DateTime?" %}
?CoworkerExtraService\_BookingFromTime=...
{% endapi-method-parameter %}


{% api-method-parameter name="BookingToTime" type="DateTime?" %}
?CoworkerExtraService\_BookingToTime=...
{% endapi-method-parameter %}


{% api-method-parameter name="BookingResourceName" type="string" %}
?CoworkerExtraService\_BookingResourceName=...
{% endapi-method-parameter %}


{% api-method-parameter name="ExtraService\_Name" type="string" %}
?CoworkerExtraService\_ExtraService\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="ExtraService\_Currency_Code" type="string" %}
?CoworkerExtraService\_ExtraService\_Currency_Code=...
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
        "ExtraService": null,
        "Description": "Description",
        "Notes": "Notes",
        "RemainingUses": false,
        "TotalUses": false,
        "Free": false,
        "Price": false,
        "ExpireDate": null,
        "DueDate": null,
        "PurchaseOrder": "PurchaseOrder",
        "ChargePeriod": Nexudus.Coworking.Core.Enums.eChargePeriod.Minutes,
        "Invoiced": false,
        "InvoiceDate": ,
        "IsFromTariff": false,
        "TariffTimePassUniqueId": null,
        "CoworkerProductUniqueId": null,
        "BookingUniqueId": null,
        "AutomaticallyAdded": null,
        "DiscountCode": "Discount Code",
        "DiscountAmount": false,
        "BookingId": ,
        "BookingFromTime": ,
        "BookingToTime": ,
        "BookingResourceName": "",
		"CoworkerExtraServiceExtraServiceName": "...",
		"CoworkerExtraServiceExtraServiceCurrency_Code": "...",

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

> 🔒 Requires user role `coworkerextraservice-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerextraservices" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkerextraservices.
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
        "ExtraService": null,
        "Description": "Description",
        "Notes": "Notes",
        "RemainingUses": false,
        "TotalUses": false,
        "Free": false,
        "Price": false,
        "ExpireDate": null,
        "DueDate": null,
        "PurchaseOrder": "PurchaseOrder",
        "ChargePeriod": Nexudus.Coworking.Core.Enums.eChargePeriod.Minutes,
        "Invoiced": false,
        "InvoiceDate": ,
        "IsFromTariff": false,
        "TariffTimePassUniqueId": null,
        "CoworkerProductUniqueId": null,
        "BookingUniqueId": null,
        "AutomaticallyAdded": null,
        "DiscountCode": "Discount Code",
        "DiscountAmount": false,
        "BookingId": ,
        "BookingFromTime": ,
        "BookingToTime": ,
        "BookingResourceName": "",
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

> 🔒 Requires user role `coworkerextraservice-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerextraservices" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of coworkerextraservices based on a range of dates, integer or decimal properties.
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
?to\_CoworkerExtraService\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_CoworkerExtraService\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_CoworkerExtraService\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_CoworkerExtraService\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="RemainingUses" type="int" required=false %}
?from\_CoworkerExtraService\_RemainingUses=...
{% endapi-method-parameter %}
{% api-method-parameter name="RemainingUses" type="int" required=false %}
?to\_CoworkerExtraService\_RemainingUses=...
{% endapi-method-parameter %}
{% api-method-parameter name="TotalUses" type="int" required=false %}
?from\_CoworkerExtraService\_TotalUses=...
{% endapi-method-parameter %}
{% api-method-parameter name="TotalUses" type="int" required=false %}
?to\_CoworkerExtraService\_TotalUses=...
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal" required=false %}
?from\_CoworkerExtraService\_Price=...
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal" required=false %}
?to\_CoworkerExtraService\_Price=...
{% endapi-method-parameter %}
{% api-method-parameter name="ExpireDate" type="datetime" required=false %}
?from\_CoworkerExtraService\_ExpireDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="ExpireDate" type="datetime" required=false %}
?to\_CoworkerExtraService\_ExpireDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="datetime" required=false %}
?from\_CoworkerExtraService\_DueDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="datetime" required=false %}
?to\_CoworkerExtraService\_DueDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceDate" type="datetime" required=false %}
?from\_CoworkerExtraService\_InvoiceDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceDate" type="datetime" required=false %}
?to\_CoworkerExtraService\_InvoiceDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountAmount" type="decimal" required=false %}
?from\_CoworkerExtraService\_DiscountAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountAmount" type="decimal" required=false %}
?to\_CoworkerExtraService\_DiscountAmount=...
{% endapi-method-parameter %}
{% api-method-parameter name="BookingId" type="int" required=false %}
?from\_CoworkerExtraService\_BookingId=...
{% endapi-method-parameter %}
{% api-method-parameter name="BookingId" type="int" required=false %}
?to\_CoworkerExtraService\_BookingId=...
{% endapi-method-parameter %}
{% api-method-parameter name="BookingFromTime" type="datetime" required=false %}
?from\_CoworkerExtraService\_BookingFromTime=...
{% endapi-method-parameter %}
{% api-method-parameter name="BookingFromTime" type="datetime" required=false %}
?to\_CoworkerExtraService\_BookingFromTime=...
{% endapi-method-parameter %}
{% api-method-parameter name="BookingToTime" type="datetime" required=false %}
?from\_CoworkerExtraService\_BookingToTime=...
{% endapi-method-parameter %}
{% api-method-parameter name="BookingToTime" type="datetime" required=false %}
?to\_CoworkerExtraService\_BookingToTime=...
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
        "ExtraService": null,
        "Description": "Description",
        "Notes": "Notes",
        "RemainingUses": false,
        "TotalUses": false,
        "Free": false,
        "Price": false,
        "ExpireDate": null,
        "DueDate": null,
        "PurchaseOrder": "PurchaseOrder",
        "ChargePeriod": Nexudus.Coworking.Core.Enums.eChargePeriod.Minutes,
        "Invoiced": false,
        "InvoiceDate": ,
        "IsFromTariff": false,
        "TariffTimePassUniqueId": null,
        "CoworkerProductUniqueId": null,
        "BookingUniqueId": null,
        "AutomaticallyAdded": null,
        "DiscountCode": "Discount Code",
        "DiscountAmount": false,
        "BookingId": ,
        "BookingFromTime": ,
        "BookingToTime": ,
        "BookingResourceName": "",
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

> 🔒 Requires user role `coworkerextraservice-list`


{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerextraservices?CoworkerExtraService_Id=[:id1,:id2,...]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more coworkerextraservice records based on their Id.
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
Comma-separated list of IDs of every coworkerextraservice to fetch. I.e. [123456,789102,...] 
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
        "Coworker": null,
        "Business": null,
        "ExtraService": null,
        "Description": "Description",
        "Notes": "Notes",
        "RemainingUses": false,
        "TotalUses": false,
        "Free": false,
        "Price": false,
        "ExpireDate": null,
        "DueDate": null,
        "PurchaseOrder": "PurchaseOrder",
        "ChargePeriod": Nexudus.Coworking.Core.Enums.eChargePeriod.Minutes,
        "Invoiced": false,
        "InvoiceDate": ,
        "IsFromTariff": false,
        "TariffTimePassUniqueId": null,
        "CoworkerProductUniqueId": null,
        "BookingUniqueId": null,
        "AutomaticallyAdded": null,
        "DiscountCode": "Discount Code",
        "DiscountAmount": false,
        "BookingId": ,
        "BookingFromTime": ,
        "BookingToTime": ,
        "BookingResourceName": "",
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

> 🔒 Requires user role `coworkerextraservice-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerextraservices/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one coworkerextraservice record.
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
The ID of the coworkerextraservice to fetch.
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
        "ExtraService": null,
        "Description": "Description",
        "Notes": "Notes",
        "RemainingUses": false,
        "TotalUses": false,
        "Free": false,
        "Price": false,
        "ExpireDate": null,
        "DueDate": null,
        "PurchaseOrder": "PurchaseOrder",
        "ChargePeriod": Nexudus.Coworking.Core.Enums.eChargePeriod.Minutes,
        "Invoiced": false,
        "InvoiceDate": ,
        "IsFromTariff": false,
        "TariffTimePassUniqueId": null,
        "CoworkerProductUniqueId": null,
        "BookingUniqueId": null,
        "AutomaticallyAdded": null,
        "DiscountCode": "Discount Code",
        "DiscountAmount": false,
        "BookingId": ,
        "BookingFromTime": ,
        "BookingToTime": ,
        "BookingResourceName": "",
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

> 🔒 Requires user role `coworkerextraservice-read`


{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/coworkerextraservices" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new coworkerextraservice.
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
{% api-method-parameter name="ExtraServiceId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Notes" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TotalUses" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Free" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ExpireDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PurchaseOrder" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ChargePeriod" type="enum" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingId" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingFromTime" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingToTime" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingResourceName" type="string" required=false %}
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

> 🔒 Requires user role `coworkerextraservice-create`

```javascript
{
	"Coworker": 12345678,
	"Business": 12345678,
	"ExtraService": 12345678,
	"Notes": "Notes",
	"TotalUses": false,
	"Free": false,
	"Price": false,
	"ExpireDate": null,
	"DueDate": null,
	"PurchaseOrder": "PurchaseOrder",
	"ChargePeriod": 1 (check Enumerated values section below),
	"BookingId": ,
	"BookingFromTime": ,
	"BookingToTime": ,
	"BookingResourceName": "",
}

```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/coworkerextraservices" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing coworkerextraservice. PUT requests require ALL record properties to be submitted with every request. Any missing properties will be cleared or set to false.
  
Required User Role: `coworkerextraservice-edit`
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
{% api-method-parameter name="CoworkerId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BusinessId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="ExtraServiceId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Notes" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="TotalUses" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Free" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="ExpireDate" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="DueDate" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="PurchaseOrder" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="ChargePeriod" type="enum" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingId" type="int?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingFromTime" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingToTime" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingResourceName" type="string" required="true" %}
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

> 🔒 Requires user role `coworkerextraservice-edit`

```javascript
{
	"Coworker": 12345678,
	"Business": 12345678,
	"ExtraService": 12345678,
	"Notes": "Notes",
	"TotalUses": false,
	"Free": false,
	"Price": false,
	"ExpireDate": null,
	"DueDate": null,
	"PurchaseOrder": "PurchaseOrder",
	"ChargePeriod": 1 (check Enumerated values section below),
	"BookingId": ,
	"BookingFromTime": ,
	"BookingToTime": ,
	"BookingResourceName": "",
}

```




{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/billing/coworkerextraservices/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a coworkerextraservice.  
  
Required User Roles: `coworkerextraservice-delete`
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



> 🔒 Requires user role `coworkerextraservice-delete`


## Commands

Commands allow to perform actions against one or more coworkerextraservice records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerextraservices/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for coworkerextraservice records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkerextraservices/runcommand" %}
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

> 🔒 Requires user role `coworkerextraservice-edit`

## Enumerated values

##### ChargePeriod:
> GET /api/utils/enums?name=eChargePeriod

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [Coworker](../spaces/coworker.md)
* [Business](../sys/business.md)
* [ExtraService](../billing/extraservice.md)
