# ExtraService

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/extraservices" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of extraservices based on one or more filter querystring parameters.
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
?ExtraService\_SystemId=...
{% endapi-method-parameter %}

{% api-method-parameter name="Business" type="Business" %}
?ExtraService\_Business=...
{% endapi-method-parameter %}

{% api-method-parameter name="Name" type="string" %}
?ExtraService\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Description" type="string" %}
?ExtraService\_Description=...
{% endapi-method-parameter %}

{% api-method-parameter name="Visible" type="bool" %}
?ExtraService\_Visible=...
{% endapi-method-parameter %}

{% api-method-parameter name="DisplayOrder" type="int" %}
?ExtraService\_DisplayOrder=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" %}
?ExtraService\_Price=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreditPrice" type="decimal?" %}
?ExtraService\_CreditPrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="ChargePeriod" type="enum" %}
?ExtraService\_ChargePeriod=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaximumPrice" type="decimal?" %}
?ExtraService\_MaximumPrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="IsDefaultPrice" type="bool" %}
?ExtraService\_IsDefaultPrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="Currency" type="Currency" %}
?ExtraService\_Currency=...
{% endapi-method-parameter %}

{% api-method-parameter name="TaxRate" type="TaxRate" %}
?ExtraService\_TaxRate=...
{% endapi-method-parameter %}

{% api-method-parameter name="FinancialAccount" type="FinancialAccount" %}
?ExtraService\_FinancialAccount=...
{% endapi-method-parameter %}

{% api-method-parameter name="FromTime" type="int?" %}
?ExtraService\_FromTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ToTime" type="int?" %}
?ExtraService\_ToTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="MinLength" type="int?" %}
?ExtraService\_MinLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxLength" type="int?" %}
?ExtraService\_MaxLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="OnlyWithinAvailableTimes" type="bool" %}
?ExtraService\_OnlyWithinAvailableTimes=...
{% endapi-method-parameter %}

{% api-method-parameter name="FixedCostLength" type="int?" %}
?ExtraService\_FixedCostLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="FixedCostPrice" type="decimal?" %}
?ExtraService\_FixedCostPrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForContacts" type="bool" %}
?ExtraService\_OnlyForContacts=...
{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForMembers" type="bool" %}
?ExtraService\_OnlyForMembers=...
{% endapi-method-parameter %}

{% api-method-parameter name="IsBookingCredit" type="bool" %}
?ExtraService\_IsBookingCredit=...
{% endapi-method-parameter %}

{% api-method-parameter name="IsPrintingCredit" type="bool" %}
?ExtraService\_IsPrintingCredit=...
{% endapi-method-parameter %}

{% api-method-parameter name="ResourceTypeNames" type="string" %}
?ExtraService\_ResourceTypeNames=...
{% endapi-method-parameter %}

{% api-method-parameter name="Currency\_Code" type="string" %}
?ExtraService\_Currency\_Code=...
{% endapi-method-parameter %}

{% api-method-parameter name="ResourceTypes" type="int" required=false %}
?ExtraService\_ResourceTypes=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tariffs" type="int" required=false %}
?ExtraService\_Tariffs=...
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
        "Name": "Name",
        "Description": "Description",
        "Visible": true,
        "DisplayOrder": true,
        "Price": 0,
        "CreditPrice": ,
        "ChargePeriod": Nexudus.Coworking.Core.Enums.eChargePeriod.Minutes,
        "MaximumPrice": null,
        "IsDefaultPrice": true,
        "Currency": null,
        "TaxRate": null,
        "FinancialAccount": null,
        "FromTime": null,
        "ToTime": null,
        "MinLength": null,
        "MaxLength": null,
        "OnlyWithinAvailableTimes": true,
        "FixedCostLength": null,
        "FixedCostPrice": null,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "IsBookingCredit": true,
        "IsPrintingCredit": true,
        "ResourceTypeNames": "",
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

> 🔒 Requires user role `extraservice-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/extraservices" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of extraservices.
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
        "Name": "Name",
        "Description": "Description",
        "Visible": true,
        "DisplayOrder": true,
        "Price": 0,
        "CreditPrice": ,
        "ChargePeriod": Nexudus.Coworking.Core.Enums.eChargePeriod.Minutes,
        "MaximumPrice": null,
        "IsDefaultPrice": true,
        "Currency": null,
        "TaxRate": null,
        "FinancialAccount": null,
        "FromTime": null,
        "ToTime": null,
        "MinLength": null,
        "MaxLength": null,
        "OnlyWithinAvailableTimes": true,
        "FixedCostLength": null,
        "FixedCostPrice": null,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "IsBookingCredit": true,
        "IsPrintingCredit": true,
        "ResourceTypeNames": "",
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

> 🔒 Requires user role `extraservice-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/extraservices" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of extraservices based on the date when they were created or updated.
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
?to\_ExtraService\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_ExtraService\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_ExtraService\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_ExtraService\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="DisplayOrder" type="int" required=false %}
?from\_ExtraService\_DisplayOrder=...
{% endapi-method-parameter %}

{% api-method-parameter name="DisplayOrder" type="int" required=false %}
?to\_ExtraService\_DisplayOrder=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=false %}
?from\_ExtraService\_Price=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=false %}
?to\_ExtraService\_Price=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreditPrice" type="decimal" required=false %}
?from\_ExtraService\_CreditPrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreditPrice" type="decimal" required=false %}
?to\_ExtraService\_CreditPrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaximumPrice" type="decimal" required=false %}
?from\_ExtraService\_MaximumPrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaximumPrice" type="decimal" required=false %}
?to\_ExtraService\_MaximumPrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="FromTime" type="int" required=false %}
?from\_ExtraService\_FromTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="FromTime" type="int" required=false %}
?to\_ExtraService\_FromTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ToTime" type="int" required=false %}
?from\_ExtraService\_ToTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ToTime" type="int" required=false %}
?to\_ExtraService\_ToTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="MinLength" type="int" required=false %}
?from\_ExtraService\_MinLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="MinLength" type="int" required=false %}
?to\_ExtraService\_MinLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxLength" type="int" required=false %}
?from\_ExtraService\_MaxLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxLength" type="int" required=false %}
?to\_ExtraService\_MaxLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="FixedCostLength" type="int" required=false %}
?from\_ExtraService\_FixedCostLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="FixedCostLength" type="int" required=false %}
?to\_ExtraService\_FixedCostLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="FixedCostPrice" type="decimal" required=false %}
?from\_ExtraService\_FixedCostPrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="FixedCostPrice" type="decimal" required=false %}
?to\_ExtraService\_FixedCostPrice=...
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
        "Name": "Name",
        "Description": "Description",
        "Visible": true,
        "DisplayOrder": true,
        "Price": 0,
        "CreditPrice": ,
        "ChargePeriod": Nexudus.Coworking.Core.Enums.eChargePeriod.Minutes,
        "MaximumPrice": null,
        "IsDefaultPrice": true,
        "Currency": null,
        "TaxRate": null,
        "FinancialAccount": null,
        "FromTime": null,
        "ToTime": null,
        "MinLength": null,
        "MaxLength": null,
        "OnlyWithinAvailableTimes": true,
        "FixedCostLength": null,
        "FixedCostPrice": null,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "IsBookingCredit": true,
        "IsPrintingCredit": true,
        "ResourceTypeNames": "",
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

> 🔒 Requires user role `extraservice-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/extraservices/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one extraservice record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the extraservice to fetch.
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
        "Name": "Name",
        "Description": "Description",
        "Visible": true,
        "DisplayOrder": true,
        "Price": 0,
        "CreditPrice": ,
        "ChargePeriod": Nexudus.Coworking.Core.Enums.eChargePeriod.Minutes,
        "MaximumPrice": null,
        "IsDefaultPrice": true,
        "Currency": null,
        "TaxRate": null,
        "FinancialAccount": null,
        "FromTime": null,
        "ToTime": null,
        "MinLength": null,
        "MaxLength": null,
        "OnlyWithinAvailableTimes": true,
        "FixedCostLength": null,
        "FixedCostPrice": null,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "IsBookingCredit": true,
        "IsPrintingCredit": true,
        "ResourceTypeNames": "",
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

> 🔒 Requires user role `extraservice-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/extraservices" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new extraservice.
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

{% api-method-parameter name="Description" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Visible" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DisplayOrder" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CreditPrice" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ChargePeriod" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MaximumPrice" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="IsDefaultPrice" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CurrencyId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="TaxRateId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FinancialAccountId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FromTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ToTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MinLength" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MaxLength" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OnlyWithinAvailableTimes" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FixedCostLength" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FixedCostPrice" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForContacts" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForMembers" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="IsBookingCredit" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="IsPrintingCredit" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ResourceTypeNames" type="string" required=false %}

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

> 🔒 Requires user role `extraservice-create`

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/extraservices" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing extraservice.Required User Role: `extraservice-edit`
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

{% api-method-parameter name="Description" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Visible" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DisplayOrder" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CreditPrice" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ChargePeriod" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MaximumPrice" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="IsDefaultPrice" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CurrencyId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="TaxRateId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FinancialAccountId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FromTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ToTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MinLength" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MaxLength" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OnlyWithinAvailableTimes" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FixedCostLength" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FixedCostPrice" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForContacts" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OnlyForMembers" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="IsBookingCredit" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="IsPrintingCredit" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ResourceTypeNames" type="string" required=false %}

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

> 🔒 Requires user role `extraservice-edit`

{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/billing/extraservices/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a extraservice.Required User Roles: `extraservice-delete`
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

> 🔒 Requires user role `extraservice-delete`

## Commands

Commands allow to perform actions against one or more extraservice records. Some commands accept only one record while others can run an action for a number of records at the same time. Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/extraservices/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for extraservice records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/extraservices/runcommand" %}
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

> 🔒 Requires user role `extraservice-edit`

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

## Related Entities

* [Business](../sys/business.md)
* [Currency](../sys/currency.md)
* [TaxRate](https://github.com/Nexudus/api-docs/tree/69f22bafd51fdd0980388760b60e7af681cf5f57/rest-api/sys/taxrate.md)
* [FinancialAccount](financialaccount.md)

