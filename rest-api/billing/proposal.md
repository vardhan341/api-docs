# Proposal

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/proposals" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of proposals based on one or more filter querystring parameters.
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
?Proposal_SystemId=...
{% endapi-method-parameter %}

{% api-method-parameter name="IssuedBy" type="Business" %}
?Proposal_IssuedBy=...
{% endapi-method-parameter %}

{% api-method-parameter name="Responsible" type="User" %}
?Proposal_Responsible=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker" type="Coworker" %}
?Proposal_Coworker=...
{% endapi-method-parameter %}

{% api-method-parameter name="Reference" type="string" %}
?Proposal_Reference=...
{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" %}
?Proposal_Notes=...
{% endapi-method-parameter %}

{% api-method-parameter name="ProposalStatus" type="enum" %}
?Proposal_ProposalStatus=...
{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSend" type="DocumentTemplate" %}
?Proposal_DocumentToSend=...
{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSign" type="DocumentTemplate" %}
?Proposal_DocumentToSign=...
{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSignHtml" type="string" %}
?Proposal_DocumentToSignHtml=...
{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSendHtml" type="string" %}
?Proposal_DocumentToSendHtml=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tariff" type="Tariff" %}
?Proposal_Tariff=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal?" %}
?Proposal_Price=...
{% endapi-method-parameter %}

{% api-method-parameter name="StartDate" type="DateTime?" %}
?Proposal_StartDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="CancellationLimitDays" type="int?" %}
?Proposal_CancellationLimitDays=...
{% endapi-method-parameter %}

{% api-method-parameter name="ContractTerm" type="DateTime?" %}
?Proposal_ContractTerm=...
{% endapi-method-parameter %}

{% api-method-parameter name="CancellationDate" type="DateTime?" %}
?Proposal_CancellationDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingDay" type="int" %}
?Proposal_BillingDay=...
{% endapi-method-parameter %}

{% api-method-parameter name="Quantity" type="int" %}
?Proposal_Quantity=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountCode" type="DiscountCode" %}
?Proposal_DiscountCode=...
{% endapi-method-parameter %}

{% api-method-parameter name="SentOn" type="DateTime?" %}
?Proposal_SentOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="IssuedBy\_Name" type="string" %}
?Proposal_IssuedBy_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="IssuedBy\_Currency_Code" type="string" %}
?Proposal_IssuedBy_Currency_Code=...
{% endapi-method-parameter %}

{% api-method-parameter name="Responsible\_FullName" type="string" %}
?Proposal_Responsible_FullName=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_CoworkerType" type="string" %}
?Proposal_Coworker_CoworkerType=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_FullName" type="string" %}
?Proposal_Coworker_FullName=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_CompanyName" type="string" %}
?Proposal_Coworker_CompanyName=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_BillingName" type="string" %}
?Proposal_Coworker_BillingName=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tariff\_Name" type="string" %}
?Proposal_Tariff_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Desks" type="int" required=false %}
?Proposal_Desks=...
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

```javascript
{
    "Records": [{
        "IssuedBy": null,
        "Responsible": null,
        "Coworker": null,
        "Reference": "00001",
        "Notes": "Notes",
        "ProposalStatus": Nexudus.Coworking.Core.Enums.eProposalStatus.Draft,
        "DocumentToSend": null,
        "DocumentToSign": null,
        "DocumentToSignHtml": "",
        "DocumentToSendHtml": "",
        "Tariff": null,
        "Price": false,
        "StartDate": null,
        "CancellationLimitDays": null,
        "ContractTerm": null,
        "CancellationDate": null,
        "BillingDay": 1,
        "Quantity": 1,
        "DiscountCode": null,
        "SentOn": false,
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

> 🔒 Requires user role `proposal-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/proposals" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of proposals.
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
        "Responsible": null,
        "Coworker": null,
        "Reference": "00001",
        "Notes": "Notes",
        "ProposalStatus": Nexudus.Coworking.Core.Enums.eProposalStatus.Draft,
        "DocumentToSend": null,
        "DocumentToSign": null,
        "DocumentToSignHtml": "",
        "DocumentToSendHtml": "",
        "Tariff": null,
        "Price": false,
        "StartDate": null,
        "CancellationLimitDays": null,
        "ContractTerm": null,
        "CancellationDate": null,
        "BillingDay": 1,
        "Quantity": 1,
        "DiscountCode": null,
        "SentOn": false,
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

> 🔒 Requires user role `proposal-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time.
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/proposals" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of proposals based on a range of dates, integer or decimal properties.
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
?to_Proposal_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from_Proposal_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to_Proposal_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from_Proposal_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=false %}
?from_Proposal_Price=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=false %}
?to_Proposal_Price=...
{% endapi-method-parameter %}

{% api-method-parameter name="StartDate" type="datetime" required=false %}
?from_Proposal_StartDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="StartDate" type="datetime" required=false %}
?to_Proposal_StartDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int" required=false %}
?from_Proposal_CancellationLimitDays=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int" required=false %}
?to_Proposal_CancellationLimitDays=...
{% endapi-method-parameter %}
{% api-method-parameter name="ContractTerm" type="datetime" required=false %}
?from_Proposal_ContractTerm=...
{% endapi-method-parameter %}
{% api-method-parameter name="ContractTerm" type="datetime" required=false %}
?to_Proposal_ContractTerm=...
{% endapi-method-parameter %}

{% api-method-parameter name="CancellationLimitDays" type="int" required=false %}
?from\_Proposal\_CancellationLimitDays=...
{% endapi-method-parameter %}

{% api-method-parameter name="CancellationLimitDays" type="int" required=false %}
?to\_Proposal\_CancellationLimitDays=...
{% endapi-method-parameter %}

{% api-method-parameter name="ContractTerm" type="datetime" required=false %}
?from\_Proposal\_ContractTerm=...
{% endapi-method-parameter %}

{% api-method-parameter name="ContractTerm" type="datetime" required=false %}
?to\_Proposal\_ContractTerm=...
{% endapi-method-parameter %}

{% api-method-parameter name="CancellationDate" type="datetime" required=false %}
?from_Proposal_CancellationDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="CancellationDate" type="datetime" required=false %}
?to_Proposal_CancellationDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingDay" type="int" required=false %}
?from_Proposal_BillingDay=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingDay" type="int" required=false %}
?to_Proposal_BillingDay=...
{% endapi-method-parameter %}

{% api-method-parameter name="Quantity" type="int" required=false %}
?from_Proposal_Quantity=...
{% endapi-method-parameter %}

{% api-method-parameter name="Quantity" type="int" required=false %}
?to_Proposal_Quantity=...
{% endapi-method-parameter %}

{% api-method-parameter name="SentOn" type="datetime" required=false %}
?from_Proposal_SentOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="SentOn" type="datetime" required=false %}
?to_Proposal_SentOn=...
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
        "Responsible": null,
        "Coworker": null,
        "Reference": "00001",
        "Notes": "Notes",
        "ProposalStatus": Nexudus.Coworking.Core.Enums.eProposalStatus.Draft,
        "DocumentToSend": null,
        "DocumentToSign": null,
        "DocumentToSignHtml": "",
        "DocumentToSendHtml": "",
        "Tariff": null,
        "Price": false,
        "StartDate": null,
        "CancellationLimitDays": null,
        "ContractTerm": null,
        "CancellationDate": null,
        "BillingDay": 1,
        "Quantity": 1,
        "DiscountCode": null,
        "SentOn": false,
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

> 🔒 Requires user role `proposal-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/proposals?Proposal_Id=[:id1,:id2,...]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more proposal records based on their Id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every proposal to fetch. I.e. \[123456,789102,...\]
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

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every proposal to fetch. I.e. [123456,789102,...]
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
        "Responsible": null,
        "Coworker": null,
        "Reference": "00001",
        "Notes": "Notes",
        "ProposalStatus": Nexudus.Coworking.Core.Enums.eProposalStatus.Draft,
        "DocumentToSend": null,
        "DocumentToSign": null,
        "DocumentToSignHtml": "",
        "DocumentToSendHtml": "",
        "Tariff": null,
        "Price": false,
        "StartDate": null,
        "CancellationLimitDays": null,
        "ContractTerm": null,
        "CancellationDate": null,
        "BillingDay": 1,
        "Quantity": 1,
        "DiscountCode": null,
        "SentOn": false,
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

```text
"Not found"
```

{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `proposal-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/proposals/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one proposal record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the proposal to fetch.
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
        "IssuedBy": null,
        "Responsible": null,
        "Coworker": null,
        "Reference": "00001",
        "Notes": "Notes",
        "ProposalStatus": Nexudus.Coworking.Core.Enums.eProposalStatus.Draft,
        "DocumentToSend": null,
        "DocumentToSign": null,
        "DocumentToSignHtml": "",
        "DocumentToSendHtml": "",
        "Tariff": null,
        "Price": false,
        "StartDate": null,
        "CancellationLimitDays": null,
        "ContractTerm": null,
        "CancellationDate": null,
        "BillingDay": 1,
        "Quantity": 1,
        "DiscountCode": null,
        "SentOn": false,
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

> 🔒 Requires user role `proposal-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/proposals" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new proposal.
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

{% api-method-parameter name="ResponsibleId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Reference" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ProposalStatus" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSendId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSignId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSignHtml" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSendHtml" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TariffId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="StartDate" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CancellationLimitDays" type="int?" required=false %}

{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationDate" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingDay" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Quantity" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountCodeId" type="int" required=false %}

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

> 🔒 Requires user role `proposal-create`

```javascript
{
	"IssuedBy": 12345678,
	"Responsible": 12345678,
	"Coworker": 12345678,
	"Reference": "00001",
	"Notes": "Notes",
	"ProposalStatus": 1 (check Enumerated values section below),
	"DocumentToSend": 12345678,
	"DocumentToSign": 12345678,
	"DocumentToSignHtml": "",
	"DocumentToSendHtml": "",
	"Tariff": 12345678,
	"Desks": [12345678, 87654321] (replaces entire list),
	"AddedDesks": [12345678, 87654321] (adds to list),
	"RemovedDesks": [12345678, 87654321] (removes from list),
	"Price": false,
	"StartDate": null,
	"CancellationLimitDays": null,
	"CancellationDate": null,
	"BillingDay": 1,
	"Quantity": 1,
	"DiscountCode": 12345678,
}
```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/proposals" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing proposal.

Required User Role: `proposal-edit`
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

{% api-method-parameter name="ResponsibleId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Reference" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ProposalStatus" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSendId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSignId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSignHtml" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DocumentToSendHtml" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CancellationLimitDays" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ContractTerm" type="DateTime?" required=false %}

{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ContractTerm" type="DateTime?" required=false %}
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

> 🔒 Requires user role `proposal-edit`

```javascript
{
	"IssuedBy": 12345678,
	"Responsible": 12345678,
	"Coworker": 12345678,
	"Reference": "00001",
	"Notes": "Notes",
	"ProposalStatus": 1 (check Enumerated values section below),
	"DocumentToSend": 12345678,
	"DocumentToSign": 12345678,
	"DocumentToSignHtml": "",
	"DocumentToSendHtml": "",
	"CancellationLimitDays": null,
	"ContractTerm": null,
}
```

{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/billing/proposals/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a proposal.

Required User Roles: `proposal-delete`
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

> 🔒 Requires user role `proposal-delete`

## Commands

Commands allow to perform actions against one or more proposal records. Some commands accept only one record while others can run an action for a number of records at the same time. Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/proposals/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for proposal records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/proposals/runcommand" %}
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

`[ { "Name": "Name", "Type":"Type", "Value":recordId } ]`
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

> 🔒 Requires user role `proposal-edit`

## Enumerated values

##### ProposalStatus:

> GET /api/utils/enums?name=eProposalStatus

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/proposals/getdocumenttosignbinarydocument/:id" %}
{% api-method-summary %}
DocumentToSignBinaryDocument
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Proposal to get the documenttosignbinarydocument for.
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
Binary stream or null
```

{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/proposals/getdocumenttosendbinarydocument/:id" %}
{% api-method-summary %}
DocumentToSendBinaryDocument
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Proposal to get the documenttosendbinarydocument for.
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
Binary stream or null
```

{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/proposals/getproposalfile/:id" %}
{% api-method-summary %}
ProposalFile
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Proposal to get the proposalfile for.
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
Binary stream or null
```

{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Related Entities

- [Business](../sys/business.md)
- [User](../sys/user.md)
- [Coworker](../spaces/coworker.md)
- [DocumentTemplate](../crm/documenttemplate.md)
- [DocumentTemplate](../crm/documenttemplate.md)
- [Tariff](../billing/tariff.md)
- [DiscountCode](../billing/discountcode.md)
