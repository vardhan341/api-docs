# CrmOpportunity

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmopportunities" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of crmopportunities based on one or more filter querystring parameters.
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
?CrmOpportunity\_SystemId=...
{% endapi-method-parameter %}

{% api-method-parameter name="CrmBoardColumn" type="CrmBoardColumn" %}
?CrmOpportunity\_CrmBoardColumn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker" type="Coworker" %}
?CrmOpportunity\_Coworker=...
{% endapi-method-parameter %}

{% api-method-parameter name="Team" type="Team" %}
?CrmOpportunity\_Team=...
{% endapi-method-parameter %}

{% api-method-parameter name="OpportunityType" type="OpportunityType" %}
?CrmOpportunity\_OpportunityType=...
{% endapi-method-parameter %}

{% api-method-parameter name="Responsible" type="User" %}
?CrmOpportunity\_Responsible=...
{% endapi-method-parameter %}

{% api-method-parameter name="Referrer" type="Coworker" %}
?CrmOpportunity\_Referrer=...
{% endapi-method-parameter %}

{% api-method-parameter name="Agent" type="Coworker" %}
?CrmOpportunity\_Agent=...
{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" %}
?CrmOpportunity\_Notes=...
{% endapi-method-parameter %}

{% api-method-parameter name="Completed" type="bool" %}
?CrmOpportunity\_Completed=...
{% endapi-method-parameter %}

{% api-method-parameter name="DueDate" type="DateTime?" %}
?CrmOpportunity\_DueDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="Value" type="decimal?" %}
?CrmOpportunity\_Value=...
{% endapi-method-parameter %}

{% api-method-parameter name="LeadSource" type="enum" %}
?CrmOpportunity\_LeadSource=...
{% endapi-method-parameter %}

{% api-method-parameter name="LossReason" type="enum" %}
?CrmOpportunity\_LossReason=...
{% endapi-method-parameter %}

{% api-method-parameter name="Status" type="enum" %}
?CrmOpportunity\_Status=...
{% endapi-method-parameter %}

{% api-method-parameter name="WonOn" type="DateTime?" %}
?CrmOpportunity\_WonOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="LostOn" type="DateTime?" %}
?CrmOpportunity\_LostOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Position" type="int" %}
?CrmOpportunity\_Position=...
{% endapi-method-parameter %}

{% api-method-parameter name="CrmBoardColumn\_Name" type="string" %}
?CrmOpportunity\_CrmBoardColumn\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="CrmBoardColumn\_CrmBoard\_Id" type="string" %}
?CrmOpportunity\_CrmBoardColumn\_CrmBoard\_Id=...
{% endapi-method-parameter %}

{% api-method-parameter name="CrmBoardColumn\_CrmBoard\_Name" type="string" %}
?CrmOpportunity\_CrmBoardColumn\_CrmBoard\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="CrmBoardColumn\_CrmBoard\_Business\_Id" type="string" %}
?CrmOpportunity\_CrmBoardColumn\_CrmBoard\_Business\_Id=...
{% endapi-method-parameter %}

{% api-method-parameter name="CrmBoardColumn\_CrmBoard\_Business\_Name" type="string" %}
?CrmOpportunity\_CrmBoardColumn\_CrmBoard\_Business\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="CrmBoardColumn\_CrmBoard\_Business\_Currency\_Id" type="string" %}
?CrmOpportunity\_CrmBoardColumn\_CrmBoard\_Business\_Currency\_Id=...
{% endapi-method-parameter %}

{% api-method-parameter name="CrmBoardColumn\_CrmBoard\_Business\_Currency\_Code" type="string" %}
?CrmOpportunity\_CrmBoardColumn\_CrmBoard\_Business\_Currency\_Code=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_FullName" type="string" %}
?CrmOpportunity\_Coworker\_FullName=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_CoworkerType" type="string" %}
?CrmOpportunity\_Coworker\_CoworkerType=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_CompanyName" type="string" %}
?CrmOpportunity\_Coworker\_CompanyName=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_Email" type="string" %}
?CrmOpportunity\_Coworker\_Email=...
{% endapi-method-parameter %}

{% api-method-parameter name="Team\_Name" type="string" %}
?CrmOpportunity\_Team\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Team\_Description" type="string" %}
?CrmOpportunity\_Team\_Description=...
{% endapi-method-parameter %}

{% api-method-parameter name="Team\_ProfileWebsite" type="string" %}
?CrmOpportunity\_Team\_ProfileWebsite=...
{% endapi-method-parameter %}

{% api-method-parameter name="OpportunityType\_Name" type="string" %}
?CrmOpportunity\_OpportunityType\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Responsible\_FullName" type="string" %}
?CrmOpportunity\_Responsible\_FullName=...
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
        "CrmBoardColumn": null,
        "Coworker": null,
        "Team": null,
        "OpportunityType": null,
        "Responsible": null,
        "Referrer": null,
        "Agent": null,
        "Notes": "Notes",
        "Completed": true,
        "DueDate": null,
        "Value": null,
        "LeadSource": Nexudus.Coworking.Core.Enums.eCrmOpportunitySource.Other,
        "LossReason": Nexudus.Coworking.Core.Enums.eCrmOpportunityLossReason.Other,
        "Status": Nexudus.Coworking.Core.Enums.eCrmOpportunityStatus.InProgress,
        "WonOn": null,
        "LostOn": null,
        "Position": 1,
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

> 🔒 Requires user role `crmopportunity-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmopportunities" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of crmopportunities.
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
        "CrmBoardColumn": null,
        "Coworker": null,
        "Team": null,
        "OpportunityType": null,
        "Responsible": null,
        "Referrer": null,
        "Agent": null,
        "Notes": "Notes",
        "Completed": true,
        "DueDate": null,
        "Value": null,
        "LeadSource": Nexudus.Coworking.Core.Enums.eCrmOpportunitySource.Other,
        "LossReason": Nexudus.Coworking.Core.Enums.eCrmOpportunityLossReason.Other,
        "Status": Nexudus.Coworking.Core.Enums.eCrmOpportunityStatus.InProgress,
        "WonOn": null,
        "LostOn": null,
        "Position": 1,
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

> 🔒 Requires user role `crmopportunity-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmopportunities" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of crmopportunities based on a range of dates, integer or decimal properties.
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
?to\_CrmOpportunity\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_CrmOpportunity\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_CrmOpportunity\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_CrmOpportunity\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="DueDate" type="datetime" required=false %}
?from\_CrmOpportunity\_DueDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="DueDate" type="datetime" required=false %}
?to\_CrmOpportunity\_DueDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="Value" type="decimal" required=false %}
?from\_CrmOpportunity\_Value=...
{% endapi-method-parameter %}

{% api-method-parameter name="Value" type="decimal" required=false %}
?to\_CrmOpportunity\_Value=...
{% endapi-method-parameter %}

{% api-method-parameter name="WonOn" type="datetime" required=false %}
?from\_CrmOpportunity\_WonOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="WonOn" type="datetime" required=false %}
?to\_CrmOpportunity\_WonOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="LostOn" type="datetime" required=false %}
?from\_CrmOpportunity\_LostOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="LostOn" type="datetime" required=false %}
?to\_CrmOpportunity\_LostOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Position" type="int" required=false %}
?from\_CrmOpportunity\_Position=...
{% endapi-method-parameter %}

{% api-method-parameter name="Position" type="int" required=false %}
?to\_CrmOpportunity\_Position=...
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
        "CrmBoardColumn": null,
        "Coworker": null,
        "Team": null,
        "OpportunityType": null,
        "Responsible": null,
        "Referrer": null,
        "Agent": null,
        "Notes": "Notes",
        "Completed": true,
        "DueDate": null,
        "Value": null,
        "LeadSource": Nexudus.Coworking.Core.Enums.eCrmOpportunitySource.Other,
        "LossReason": Nexudus.Coworking.Core.Enums.eCrmOpportunityLossReason.Other,
        "Status": Nexudus.Coworking.Core.Enums.eCrmOpportunityStatus.InProgress,
        "WonOn": null,
        "LostOn": null,
        "Position": 1,
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

> 🔒 Requires user role `crmopportunity-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmopportunities?CrmOpportunity\_Id=\[:id1,:id2,...\]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more crmopportunity records based on their Id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every crmopportunity to fetch. I.e. \[123456,789102,...\]
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
    "Records": [{
        "CrmBoardColumn": null,
        "Coworker": null,
        "Team": null,
        "OpportunityType": null,
        "Responsible": null,
        "Referrer": null,
        "Agent": null,
        "Notes": "Notes",
        "Completed": true,
        "DueDate": null,
        "Value": null,
        "LeadSource": Nexudus.Coworking.Core.Enums.eCrmOpportunitySource.Other,
        "LossReason": Nexudus.Coworking.Core.Enums.eCrmOpportunityLossReason.Other,
        "Status": Nexudus.Coworking.Core.Enums.eCrmOpportunityStatus.InProgress,
        "WonOn": null,
        "LostOn": null,
        "Position": 1,
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

> 🔒 Requires user role `crmopportunity-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmopportunities/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one crmopportunity record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the crmopportunity to fetch.
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
        "CrmBoardColumn": null,
        "Coworker": null,
        "Team": null,
        "OpportunityType": null,
        "Responsible": null,
        "Referrer": null,
        "Agent": null,
        "Notes": "Notes",
        "Completed": true,
        "DueDate": null,
        "Value": null,
        "LeadSource": Nexudus.Coworking.Core.Enums.eCrmOpportunitySource.Other,
        "LossReason": Nexudus.Coworking.Core.Enums.eCrmOpportunityLossReason.Other,
        "Status": Nexudus.Coworking.Core.Enums.eCrmOpportunityStatus.InProgress,
        "WonOn": null,
        "LostOn": null,
        "Position": 1,
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

> 🔒 Requires user role `crmopportunity-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/crm/crmopportunities" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new crmopportunity.
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
{% api-method-parameter name="CrmBoardColumnId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="TeamId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OpportunityTypeId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ResponsibleId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ReferrerId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AgentId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Completed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DueDate" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Value" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LeadSource" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LossReason" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Status" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WonOn" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LostOn" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Position" type="int" required=true %}

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

> 🔒 Requires user role `crmopportunity-create`

```javascript
{
    "CrmBoardColumn": 12345678,
    "Coworker": 12345678,
    "Team": 12345678,
    "OpportunityType": 12345678,
    "Responsible": 12345678,
    "Referrer": 12345678,
    "Agent": 12345678,
    "Notes": "Notes",
    "Completed": true,
    "DueDate": null,
    "Value": null,
    "LeadSource": 1 (check Enumerated values section below),
    "LossReason": 1 (check Enumerated values section below),
    "Status": 1 (check Enumerated values section below),
    "WonOn": null,
    "LostOn": null,
    "Position": 1,
}
```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/crm/crmopportunities" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing crmopportunity.Required User Role: `crmopportunity-edit`
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
{% api-method-parameter name="CrmBoardColumnId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="TeamId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OpportunityTypeId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ResponsibleId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ReferrerId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AgentId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Completed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DueDate" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Value" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LeadSource" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LossReason" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Status" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WonOn" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LostOn" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Position" type="int" required=true %}

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

> 🔒 Requires user role `crmopportunity-edit`

```javascript
{
    "CrmBoardColumn": 12345678,
    "Coworker": 12345678,
    "Team": 12345678,
    "OpportunityType": 12345678,
    "Responsible": 12345678,
    "Referrer": 12345678,
    "Agent": 12345678,
    "Notes": "Notes",
    "Completed": true,
    "DueDate": null,
    "Value": null,
    "LeadSource": 1 (check Enumerated values section below),
    "LossReason": 1 (check Enumerated values section below),
    "Status": 1 (check Enumerated values section below),
    "WonOn": null,
    "LostOn": null,
    "Position": 1,
}
```

{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/crm/crmopportunities/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a crmopportunity.Required User Roles: `crmopportunity-delete`
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

> 🔒 Requires user role `crmopportunity-delete`

## Commands

Commands allow to perform actions against one or more crmopportunity records. Some commands accept only one record while others can run an action for a number of records at the same time. Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmopportunities/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for crmopportunity records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/crm/crmopportunities/runcommand" %}
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

> 🔒 Requires user role `crmopportunity-edit`

## Enumerated values

### LeadSource:

> GET /api/utils/enums?name=eCrmOpportunitySource

### LossReason:

> GET /api/utils/enums?name=eCrmOpportunityLossReason

### Status:

> GET /api/utils/enums?name=eCrmOpportunityStatus

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

## Related Entities

* [CrmBoardColumn](https://github.com/Nexudus/api-docs/tree/6c08c63d9c0c6779737ccfddc96f70c6623677d0/rest-api/crm/crmboardcolumn.md)
* [Coworker](../spaces/coworker.md)
* [Team](../spaces/team.md)
* [OpportunityType](https://github.com/Nexudus/api-docs/tree/6c08c63d9c0c6779737ccfddc96f70c6623677d0/rest-api/crm/opportunitytype.md)
* [User](../sys/user.md)
* [Coworker](../spaces/coworker.md)
* [Coworker](../spaces/coworker.md)

