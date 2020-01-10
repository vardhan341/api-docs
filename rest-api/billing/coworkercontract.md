﻿{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkercontracts" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkercontracts based on one or more filter querystring parameters.
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
?CoworkerContract\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="IssuedBy" type="Business" %}
?CoworkerContract\_IssuedBy=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker" type="Coworker" %}
?CoworkerContract\_Coworker=...
{% endapi-method-parameter %}


{% api-method-parameter name="Tariff" type="Tariff" %}
?CoworkerContract\_Tariff=...
{% endapi-method-parameter %}


{% api-method-parameter name="NextTariff" type="Tariff" %}
?CoworkerContract\_NextTariff=...
{% endapi-method-parameter %}


{% api-method-parameter name="Notes" type="string" %}
?CoworkerContract\_Notes=...
{% endapi-method-parameter %}


{% api-method-parameter name="StartDate" type="DateTime?" %}
?CoworkerContract\_StartDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="BillingDay" type="int" %}
?CoworkerContract\_BillingDay=...
{% endapi-method-parameter %}


{% api-method-parameter name="RenewalDate" type="DateTime?" %}
?CoworkerContract\_RenewalDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoicedPeriod" type="DateTime?" %}
?CoworkerContract\_InvoicedPeriod=...
{% endapi-method-parameter %}


{% api-method-parameter name="ContractTerm" type="DateTime?" %}
?CoworkerContract\_ContractTerm=...
{% endapi-method-parameter %}


{% api-method-parameter name="Price" type="decimal?" %}
?CoworkerContract\_Price=...
{% endapi-method-parameter %}


{% api-method-parameter name="Value" type="decimal?" %}
?CoworkerContract\_Value=...
{% endapi-method-parameter %}


{% api-method-parameter name="Quantity" type="int" %}
?CoworkerContract\_Quantity=...
{% endapi-method-parameter %}


{% api-method-parameter name="Active" type="bool" %}
?CoworkerContract\_Active=...
{% endapi-method-parameter %}


{% api-method-parameter name="MainContract" type="bool" %}
?CoworkerContract\_MainContract=...
{% endapi-method-parameter %}


{% api-method-parameter name="Cancelled" type="bool" %}
?CoworkerContract\_Cancelled=...
{% endapi-method-parameter %}


{% api-method-parameter name="IncludeSignupFee" type="bool" %}
?CoworkerContract\_IncludeSignupFee=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceAdvancedCycles" type="bool" %}
?CoworkerContract\_InvoiceAdvancedCycles=...
{% endapi-method-parameter %}


{% api-method-parameter name="ApplyProRating" type="bool" %}
?CoworkerContract\_ApplyProRating=...
{% endapi-method-parameter %}


{% api-method-parameter name="NextAutoInvoice" type="DateTime?" %}
?CoworkerContract\_NextAutoInvoice=...
{% endapi-method-parameter %}


{% api-method-parameter name="PricePlanTermsAccepted" type="bool" %}
?CoworkerContract\_PricePlanTermsAccepted=...
{% endapi-method-parameter %}


{% api-method-parameter name="PricePlanTermsAcceptedOn" type="DateTime?" %}
?CoworkerContract\_PricePlanTermsAcceptedOn=...
{% endapi-method-parameter %}


{% api-method-parameter name="CancellationDate" type="DateTime?" %}
?CoworkerContract\_CancellationDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="CancellationLimitDays" type="int?" %}
?CoworkerContract\_CancellationLimitDays=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProRateCancellation" type="bool" %}
?CoworkerContract\_ProRateCancellation=...
{% endapi-method-parameter %}


{% api-method-parameter name="CancelTeamContracts" type="bool" %}
?CoworkerContract\_CancelTeamContracts=...
{% endapi-method-parameter %}


{% api-method-parameter name="CancellationReason" type="enum" %}
?CoworkerContract\_CancellationReason=...
{% endapi-method-parameter %}


{% api-method-parameter name="CancellationNotes" type="string" %}
?CoworkerContract\_CancellationNotes=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProposalUniqueId" type="Guid?" %}
?CoworkerContract\_ProposalUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="FloorPlanDeskIds" type="string" %}
?CoworkerContract\_FloorPlanDeskIds=...
{% endapi-method-parameter %}


{% api-method-parameter name="FloorPlanDeskNames" type="string" %}
?CoworkerContract\_FloorPlanDeskNames=...
{% endapi-method-parameter %}


{% api-method-parameter name="IssuedBy\_Name" type="string" %}
?CoworkerContract\_IssuedBy\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_FullName" type="string" %}
?CoworkerContract\_Coworker\_FullName=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_CompanyName" type="string" %}
?CoworkerContract\_Coworker\_CompanyName=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_BillingName" type="string" %}
?CoworkerContract\_Coworker\_BillingName=...
{% endapi-method-parameter %}


{% api-method-parameter name="Coworker\_Email" type="string" %}
?CoworkerContract\_Coworker\_Email=...
{% endapi-method-parameter %}


{% api-method-parameter name="Tariff\_Name" type="string" %}
?CoworkerContract\_Tariff\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="Tariff\_InvoiceEvery" type="string" %}
?CoworkerContract\_Tariff\_InvoiceEvery=...
{% endapi-method-parameter %}


{% api-method-parameter name="Tariff\_InvoiceEveryWeeks" type="string" %}
?CoworkerContract\_Tariff\_InvoiceEveryWeeks=...
{% endapi-method-parameter %}


{% api-method-parameter name="Tariff\_Price" type="string" %}
?CoworkerContract\_Tariff\_Price=...
{% endapi-method-parameter %}


{% api-method-parameter name="Tariff\_Currency_Code" type="string" %}
?CoworkerContract\_Tariff\_Currency_Code=...
{% endapi-method-parameter %}


{% api-method-parameter name="NextTariff\_Name" type="string" %}
?CoworkerContract\_NextTariff\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Desks" type="int" required=false %}
?CoworkerContract\_Desks=...
{% endapi-method-parameter %}

{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "IssuedBy": null,
        "Coworker": null,
        "Tariff": null,
        "NextTariff": null,
        "Notes": "Notes",
        "StartDate": null,
        "BillingDay": 1,
        "RenewalDate": null,
        "InvoicedPeriod": null,
        "ContractTerm": null,
        "Price": false,
        "Value": false,
        "Quantity": 1,
        "Active": null,
        "MainContract": null,
        "Cancelled": null,
        "IncludeSignupFee": true,
        "InvoiceAdvancedCycles": true,
        "ApplyProRating": true,
        "NextAutoInvoice": null,
        "PricePlanTermsAccepted": true,
        "PricePlanTermsAcceptedOn": true,
        "CancellationDate": null,
        "CancellationLimitDays": null,
        "ProRateCancellation": true,
        "CancelTeamContracts": true,
        "CancellationReason": Nexudus.Coworking.Core.Enums.eCancellationReason.Price,
        "CancellationNotes": "Notes",
        "ProposalUniqueId": null,
        "FloorPlanDeskIds": "",
        "FloorPlanDeskNames": "",
		"CoworkerContractIssuedByName": "...",
		"CoworkerContractCoworkerFullName": "...",
		"CoworkerContractCoworkerCompanyName": "...",
		"CoworkerContractCoworkerBillingName": "...",
		"CoworkerContractCoworkerEmail": "...",
		"CoworkerContractTariffName": "...",
		"CoworkerContractTariffInvoiceEvery": "...",
		"CoworkerContractTariffInvoiceEveryWeeks": "...",
		"CoworkerContractTariffPrice": "...",
		"CoworkerContractTariffCurrency_Code": "...",
		"CoworkerContractNextTariffName": "...",

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

> 🔒 Requires user role `coworkercontract-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkercontracts" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkercontracts.
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
        "IssuedBy": null,
        "Coworker": null,
        "Tariff": null,
        "NextTariff": null,
        "Notes": "Notes",
        "StartDate": null,
        "BillingDay": 1,
        "RenewalDate": null,
        "InvoicedPeriod": null,
        "ContractTerm": null,
        "Price": false,
        "Value": false,
        "Quantity": 1,
        "Active": null,
        "MainContract": null,
        "Cancelled": null,
        "IncludeSignupFee": true,
        "InvoiceAdvancedCycles": true,
        "ApplyProRating": true,
        "NextAutoInvoice": null,
        "PricePlanTermsAccepted": true,
        "PricePlanTermsAcceptedOn": true,
        "CancellationDate": null,
        "CancellationLimitDays": null,
        "ProRateCancellation": true,
        "CancelTeamContracts": true,
        "CancellationReason": Nexudus.Coworking.Core.Enums.eCancellationReason.Price,
        "CancellationNotes": "Notes",
        "ProposalUniqueId": null,
        "FloorPlanDeskIds": "",
        "FloorPlanDeskNames": "",
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

> 🔒 Requires user role `coworkercontract-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkercontracts" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of coworkercontracts based on a range of dates, integer or decimal properties.
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
?to\_CoworkerContract\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_CoworkerContract\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_CoworkerContract\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_CoworkerContract\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="StartDate" type="datetime" required=false %}
?from\_CoworkerContract\_StartDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="StartDate" type="datetime" required=false %}
?to\_CoworkerContract\_StartDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="BillingDay" type="int" required=false %}
?from\_CoworkerContract\_BillingDay=...
{% endapi-method-parameter %}
{% api-method-parameter name="BillingDay" type="int" required=false %}
?to\_CoworkerContract\_BillingDay=...
{% endapi-method-parameter %}
{% api-method-parameter name="RenewalDate" type="datetime" required=false %}
?from\_CoworkerContract\_RenewalDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="RenewalDate" type="datetime" required=false %}
?to\_CoworkerContract\_RenewalDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoicedPeriod" type="datetime" required=false %}
?from\_CoworkerContract\_InvoicedPeriod=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoicedPeriod" type="datetime" required=false %}
?to\_CoworkerContract\_InvoicedPeriod=...
{% endapi-method-parameter %}
{% api-method-parameter name="ContractTerm" type="datetime" required=false %}
?from\_CoworkerContract\_ContractTerm=...
{% endapi-method-parameter %}
{% api-method-parameter name="ContractTerm" type="datetime" required=false %}
?to\_CoworkerContract\_ContractTerm=...
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal" required=false %}
?from\_CoworkerContract\_Price=...
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal" required=false %}
?to\_CoworkerContract\_Price=...
{% endapi-method-parameter %}
{% api-method-parameter name="Value" type="decimal" required=false %}
?from\_CoworkerContract\_Value=...
{% endapi-method-parameter %}
{% api-method-parameter name="Value" type="decimal" required=false %}
?to\_CoworkerContract\_Value=...
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="int" required=false %}
?from\_CoworkerContract\_Quantity=...
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="int" required=false %}
?to\_CoworkerContract\_Quantity=...
{% endapi-method-parameter %}
{% api-method-parameter name="NextAutoInvoice" type="datetime" required=false %}
?from\_CoworkerContract\_NextAutoInvoice=...
{% endapi-method-parameter %}
{% api-method-parameter name="NextAutoInvoice" type="datetime" required=false %}
?to\_CoworkerContract\_NextAutoInvoice=...
{% endapi-method-parameter %}
{% api-method-parameter name="PricePlanTermsAcceptedOn" type="datetime" required=false %}
?from\_CoworkerContract\_PricePlanTermsAcceptedOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="PricePlanTermsAcceptedOn" type="datetime" required=false %}
?to\_CoworkerContract\_PricePlanTermsAcceptedOn=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationDate" type="datetime" required=false %}
?from\_CoworkerContract\_CancellationDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationDate" type="datetime" required=false %}
?to\_CoworkerContract\_CancellationDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int" required=false %}
?from\_CoworkerContract\_CancellationLimitDays=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int" required=false %}
?to\_CoworkerContract\_CancellationLimitDays=...
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
        "IssuedBy": null,
        "Coworker": null,
        "Tariff": null,
        "NextTariff": null,
        "Notes": "Notes",
        "StartDate": null,
        "BillingDay": 1,
        "RenewalDate": null,
        "InvoicedPeriod": null,
        "ContractTerm": null,
        "Price": false,
        "Value": false,
        "Quantity": 1,
        "Active": null,
        "MainContract": null,
        "Cancelled": null,
        "IncludeSignupFee": true,
        "InvoiceAdvancedCycles": true,
        "ApplyProRating": true,
        "NextAutoInvoice": null,
        "PricePlanTermsAccepted": true,
        "PricePlanTermsAcceptedOn": true,
        "CancellationDate": null,
        "CancellationLimitDays": null,
        "ProRateCancellation": true,
        "CancelTeamContracts": true,
        "CancellationReason": Nexudus.Coworking.Core.Enums.eCancellationReason.Price,
        "CancellationNotes": "Notes",
        "ProposalUniqueId": null,
        "FloorPlanDeskIds": "",
        "FloorPlanDeskNames": "",
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

> 🔒 Requires user role `coworkercontract-list`


{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkercontracts?CoworkerContract_Id=[:id1,:id2,...]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more coworkercontract records based on their Id.
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
Comma-separated list of IDs of every coworkercontract to fetch. I.e. [123456,789102,...] 
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
        "IssuedBy": null,
        "Coworker": null,
        "Tariff": null,
        "NextTariff": null,
        "Notes": "Notes",
        "StartDate": null,
        "BillingDay": 1,
        "RenewalDate": null,
        "InvoicedPeriod": null,
        "ContractTerm": null,
        "Price": false,
        "Value": false,
        "Quantity": 1,
        "Active": null,
        "MainContract": null,
        "Cancelled": null,
        "IncludeSignupFee": true,
        "InvoiceAdvancedCycles": true,
        "ApplyProRating": true,
        "NextAutoInvoice": null,
        "PricePlanTermsAccepted": true,
        "PricePlanTermsAcceptedOn": true,
        "CancellationDate": null,
        "CancellationLimitDays": null,
        "ProRateCancellation": true,
        "CancelTeamContracts": true,
        "CancellationReason": Nexudus.Coworking.Core.Enums.eCancellationReason.Price,
        "CancellationNotes": "Notes",
        "ProposalUniqueId": null,
        "FloorPlanDeskIds": "",
        "FloorPlanDeskNames": "",
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

> 🔒 Requires user role `coworkercontract-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkercontracts/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one coworkercontract record.
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
The ID of the coworkercontract to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "IssuedBy": null,
        "Coworker": null,
        "Tariff": null,
        "NextTariff": null,
        "Notes": "Notes",
        "StartDate": null,
        "BillingDay": 1,
        "RenewalDate": null,
        "InvoicedPeriod": null,
        "ContractTerm": null,
        "Price": false,
        "Value": false,
        "Quantity": 1,
        "Active": null,
        "MainContract": null,
        "Cancelled": null,
        "IncludeSignupFee": true,
        "InvoiceAdvancedCycles": true,
        "ApplyProRating": true,
        "NextAutoInvoice": null,
        "PricePlanTermsAccepted": true,
        "PricePlanTermsAcceptedOn": true,
        "CancellationDate": null,
        "CancellationLimitDays": null,
        "ProRateCancellation": true,
        "CancelTeamContracts": true,
        "CancellationReason": Nexudus.Coworking.Core.Enums.eCancellationReason.Price,
        "CancellationNotes": "Notes",
        "ProposalUniqueId": null,
        "FloorPlanDeskIds": "",
        "FloorPlanDeskNames": "",
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

> 🔒 Requires user role `coworkercontract-read`


{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/coworkercontracts" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new coworkercontract.
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
{% api-method-parameter name="IssuedById" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TariffId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Notes" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="StartDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillingDay" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Value" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceAdvancedCycles" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ApplyProRating" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PricePlanTermsAccepted" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProRateCancellation" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancelTeamContracts" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationReason" type="enum" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationNotes" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProposalUniqueId" type="Guid?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FloorPlanDeskIds" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FloorPlanDeskNames" type="string" required=false %}
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

> 🔒 Requires user role `coworkercontract-create`

```javascript
{
	"IssuedBy": 12345678,
	"Coworker": 12345678,
	"Tariff": 12345678,
	"Notes": "Notes",
	"StartDate": null,
	"BillingDay": 1,
	"Price": false,
	"Value": false,
	"Desks": [12345678, 87654321] (replaces entire list),
	"AddedDesks": [12345678, 87654321] (adds to list),
	"RemovedDesks": [12345678, 87654321] (removes from list),
	"Quantity": 1,
	"InvoiceAdvancedCycles": true,
	"ApplyProRating": true,
	"PricePlanTermsAccepted": true,
	"CancellationDate": null,
	"CancellationLimitDays": null,
	"ProRateCancellation": true,
	"CancelTeamContracts": true,
	"CancellationReason": 1 (check Enumerated values section below),
	"CancellationNotes": "Notes",
	"ProposalUniqueId": null,
	"FloorPlanDeskIds": "",
	"FloorPlanDeskNames": "",
}

```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/coworkercontracts" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing coworkercontract. PUT requests require ALL record properties to be submitted with every request. Any missing properties will be cleared or set to false.
  
Required User Role: `coworkercontract-edit`
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
{% api-method-parameter name="IssuedById" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="TariffId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="NextTariffId" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Notes" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="StartDate" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="BillingDay" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="RenewalDate" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoicedPeriod" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="ContractTerm" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Value" type="decimal?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Desks" type="int[]" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="AddedDesks" type="int[]" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="RemovedDesks" type="int[]" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Quantity" type="int" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="IncludeSignupFee" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceAdvancedCycles" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="ApplyProRating" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="NextAutoInvoice" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="PricePlanTermsAccepted" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationDate" type="DateTime?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProRateCancellation" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancelTeamContracts" type="bool" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationReason" type="enum" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationNotes" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProposalUniqueId" type="Guid?" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="FloorPlanDeskIds" type="string" required="true" %}
{% endapi-method-parameter %}
{% api-method-parameter name="FloorPlanDeskNames" type="string" required="true" %}
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

> 🔒 Requires user role `coworkercontract-edit`

```javascript
{
	"IssuedBy": 12345678,
	"Coworker": 12345678,
	"Tariff": 12345678,
	"NextTariff": 12345678,
	"Notes": "Notes",
	"StartDate": null,
	"BillingDay": 1,
	"RenewalDate": null,
	"InvoicedPeriod": null,
	"ContractTerm": null,
	"Price": false,
	"Value": false,
	"Desks": [12345678, 87654321] (replaces entire list),
	"AddedDesks": [12345678, 87654321] (adds to list),
	"RemovedDesks": [12345678, 87654321] (removes from list),
	"Quantity": 1,
	"IncludeSignupFee": true,
	"InvoiceAdvancedCycles": true,
	"ApplyProRating": true,
	"NextAutoInvoice": null,
	"PricePlanTermsAccepted": true,
	"CancellationDate": null,
	"CancellationLimitDays": null,
	"ProRateCancellation": true,
	"CancelTeamContracts": true,
	"CancellationReason": 1 (check Enumerated values section below),
	"CancellationNotes": "Notes",
	"ProposalUniqueId": null,
	"FloorPlanDeskIds": "",
	"FloorPlanDeskNames": "",
}

```




## Commands

Commands allow to perform actions against one or more coworkercontract records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkercontracts/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for coworkercontract records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/coworkercontracts/runcommand" %}
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

> 🔒 Requires user role `coworkercontract-edit`

## Enumerated values

##### CancellationReason:
> GET /api/utils/enums?name=eCancellationReason

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.


## Related Entities
* [Business](../sys/business.md)
* [Coworker](../spaces/coworker.md)
* [Tariff](../billing/tariff.md)
* [Tariff](../billing/tariff.md)
