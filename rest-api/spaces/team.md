{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/teams" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of teams based on one or more filter querystring parameters.
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
?Team\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?Team\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="Name" type="string" %}
?Team\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="Description" type="string" %}
?Team\_Description=...
{% endapi-method-parameter %}


{% api-method-parameter name="TunnelPrivateGroupId" type="string" %}
?Team\_TunnelPrivateGroupId=...
{% endapi-method-parameter %}


{% api-method-parameter name="CreateSingleInvoiceForTeam" type="bool" %}
?Team\_CreateSingleInvoiceForTeam=...
{% endapi-method-parameter %}


{% api-method-parameter name="UseSpecialPrices" type="bool" %}
?Team\_UseSpecialPrices=...
{% endapi-method-parameter %}


{% api-method-parameter name="PayingMember" type="Coworker" %}
?Team\_PayingMember=...
{% endapi-method-parameter %}


{% api-method-parameter name="TransferCreditsToPayingMember" type="bool" %}
?Team\_TransferCreditsToPayingMember=...
{% endapi-method-parameter %}


{% api-method-parameter name="ShareTimePasses" type="bool" %}
?Team\_ShareTimePasses=...
{% endapi-method-parameter %}


{% api-method-parameter name="ShareExtraServices" type="bool" %}
?Team\_ShareExtraServices=...
{% endapi-method-parameter %}


{% api-method-parameter name="ShareBookingCredit" type="bool" %}
?Team\_ShareBookingCredit=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountExtraServices" type="decimal?" %}
?Team\_DiscountExtraServices=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountTimePasses" type="decimal?" %}
?Team\_DiscountTimePasses=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountCharges" type="decimal?" %}
?Team\_DiscountCharges=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountTariffs" type="decimal?" %}
?Team\_DiscountTariffs=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProfileSummary" type="string" %}
?Team\_ProfileSummary=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProfileTags" type="string" %}
?Team\_ProfileTags=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProfileWebsite" type="string" %}
?Team\_ProfileWebsite=...
{% endapi-method-parameter %}


{% api-method-parameter name="GoogleMapsLink" type="string" %}
?Team\_GoogleMapsLink=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProfileIsPublic" type="bool" %}
?Team\_ProfileIsPublic=...
{% endapi-method-parameter %}


{% api-method-parameter name="Twitter" type="string" %}
?Team\_Twitter=...
{% endapi-method-parameter %}


{% api-method-parameter name="Facebook" type="string" %}
?Team\_Facebook=...
{% endapi-method-parameter %}


{% api-method-parameter name="Linkedin" type="string" %}
?Team\_Linkedin=...
{% endapi-method-parameter %}


{% api-method-parameter name="Skype" type="string" %}
?Team\_Skype=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerIds" type="string" %}
?Team\_CoworkerIds=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerFullNames" type="string" %}
?Team\_CoworkerFullNames=...
{% endapi-method-parameter %}


{% api-method-parameter name="CoworkerBillingNames" type="string" %}
?Team\_CoworkerBillingNames=...
{% endapi-method-parameter %}


{% api-method-parameter name="ActiveContracts" type="int" %}
?Team\_ActiveContracts=...
{% endapi-method-parameter %}


{% api-method-parameter name="PayingMember\_FullName" type="string" %}
?Team\_PayingMember\_FullName=...
{% endapi-method-parameter %}

{% api-method-parameter name="TeamMembers" type="int" required=false %}
?Team\_TeamMembers=...
{% endapi-method-parameter %}

{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "Business": null,
        "Name": "Name",
        "Description": "Descripción",
        "TunnelPrivateGroupId": "",
        "CreateSingleInvoiceForTeam": true,
        "UseSpecialPrices": true,
        "PayingMember": null,
        "TransferCreditsToPayingMember": true,
        "ShareTimePasses": true,
        "ShareExtraServices": true,
        "ShareBookingCredit": true,
        "DiscountExtraServices": null,
        "DiscountTimePasses": null,
        "DiscountCharges": null,
        "DiscountTariffs": null,
        "ProfileSummary": "null",
        "ProfileTags": "BusinessArea",
        "ProfileWebsite": "ProfileWebsite",
        "GoogleMapsLink": "GoogleMapsLink",
        "ProfileIsPublic": true,
        "Twitter": "Twitter",
        "Facebook": "Facebook",
        "Linkedin": "Linkedin",
        "Skype": "Skype",
        "CoworkerIds": "",
        "CoworkerFullNames": "",
        "CoworkerBillingNames": "",
        "ActiveContracts": ,
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

> 🔒 Requires user role `team-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/teams" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of teams.
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
        "Description": "Descripción",
        "TunnelPrivateGroupId": "",
        "CreateSingleInvoiceForTeam": true,
        "UseSpecialPrices": true,
        "PayingMember": null,
        "TransferCreditsToPayingMember": true,
        "ShareTimePasses": true,
        "ShareExtraServices": true,
        "ShareBookingCredit": true,
        "DiscountExtraServices": null,
        "DiscountTimePasses": null,
        "DiscountCharges": null,
        "DiscountTariffs": null,
        "ProfileSummary": "null",
        "ProfileTags": "BusinessArea",
        "ProfileWebsite": "ProfileWebsite",
        "GoogleMapsLink": "GoogleMapsLink",
        "ProfileIsPublic": true,
        "Twitter": "Twitter",
        "Facebook": "Facebook",
        "Linkedin": "Linkedin",
        "Skype": "Skype",
        "CoworkerIds": "",
        "CoworkerFullNames": "",
        "CoworkerBillingNames": "",
        "ActiveContracts": ,
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

> 🔒 Requires user role `team-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/teams" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of teams based on the date when they were created or updated.
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
?to\_Team\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_Team\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_Team\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_Team\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountExtraServices" type="decimal" required=false %}
?from\_Team\_DiscountExtraServices=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountExtraServices" type="decimal" required=false %}
?to\_Team\_DiscountExtraServices=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTimePasses" type="decimal" required=false %}
?from\_Team\_DiscountTimePasses=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTimePasses" type="decimal" required=false %}
?to\_Team\_DiscountTimePasses=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountCharges" type="decimal" required=false %}
?from\_Team\_DiscountCharges=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountCharges" type="decimal" required=false %}
?to\_Team\_DiscountCharges=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTariffs" type="decimal" required=false %}
?from\_Team\_DiscountTariffs=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTariffs" type="decimal" required=false %}
?to\_Team\_DiscountTariffs=...
{% endapi-method-parameter %}
{% api-method-parameter name="ActiveContracts" type="int" required=false %}
?from\_Team\_ActiveContracts=...
{% endapi-method-parameter %}
{% api-method-parameter name="ActiveContracts" type="int" required=false %}
?to\_Team\_ActiveContracts=...
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
        "Description": "Descripción",
        "TunnelPrivateGroupId": "",
        "CreateSingleInvoiceForTeam": true,
        "UseSpecialPrices": true,
        "PayingMember": null,
        "TransferCreditsToPayingMember": true,
        "ShareTimePasses": true,
        "ShareExtraServices": true,
        "ShareBookingCredit": true,
        "DiscountExtraServices": null,
        "DiscountTimePasses": null,
        "DiscountCharges": null,
        "DiscountTariffs": null,
        "ProfileSummary": "null",
        "ProfileTags": "BusinessArea",
        "ProfileWebsite": "ProfileWebsite",
        "GoogleMapsLink": "GoogleMapsLink",
        "ProfileIsPublic": true,
        "Twitter": "Twitter",
        "Facebook": "Facebook",
        "Linkedin": "Linkedin",
        "Skype": "Skype",
        "CoworkerIds": "",
        "CoworkerFullNames": "",
        "CoworkerBillingNames": "",
        "ActiveContracts": ,
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

> 🔒 Requires user role `team-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/teams/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one team record.
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
The ID of the team to fetch.
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
        "Name": "Name",
        "Description": "Descripción",
        "TunnelPrivateGroupId": "",
        "CreateSingleInvoiceForTeam": true,
        "UseSpecialPrices": true,
        "PayingMember": null,
        "TransferCreditsToPayingMember": true,
        "ShareTimePasses": true,
        "ShareExtraServices": true,
        "ShareBookingCredit": true,
        "DiscountExtraServices": null,
        "DiscountTimePasses": null,
        "DiscountCharges": null,
        "DiscountTariffs": null,
        "ProfileSummary": "null",
        "ProfileTags": "BusinessArea",
        "ProfileWebsite": "ProfileWebsite",
        "GoogleMapsLink": "GoogleMapsLink",
        "ProfileIsPublic": true,
        "Twitter": "Twitter",
        "Facebook": "Facebook",
        "Linkedin": "Linkedin",
        "Skype": "Skype",
        "CoworkerIds": "",
        "CoworkerFullNames": "",
        "CoworkerBillingNames": "",
        "ActiveContracts": ,
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

> 🔒 Requires user role `team-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/spaces/teams" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new team.
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
{% api-method-parameter name="TunnelPrivateGroupId" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CreateSingleInvoiceForTeam" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="UseSpecialPrices" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PayingMemberId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TransferCreditsToPayingMember" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShareTimePasses" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShareExtraServices" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShareBookingCredit" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountExtraServices" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTimePasses" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountCharges" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTariffs" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileSummary" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileTags" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileWebsite" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="GoogleMapsLink" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileIsPublic" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Twitter" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Facebook" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Linkedin" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Skype" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerIds" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerFullNames" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerBillingNames" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ActiveContracts" type="int" required=true %}
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

> 🔒 Requires user role `team-create`

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/spaces/teams" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing team.
  
Required User Role: `team-edit`
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
The id of the team to update
{% api-method-parameter name="BusinessId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Description" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TunnelPrivateGroupId" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CreateSingleInvoiceForTeam" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="UseSpecialPrices" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PayingMemberId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TransferCreditsToPayingMember" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShareTimePasses" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShareExtraServices" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShareBookingCredit" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountExtraServices" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTimePasses" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountCharges" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTariffs" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileSummary" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileTags" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileWebsite" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="GoogleMapsLink" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProfileIsPublic" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Twitter" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Facebook" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Linkedin" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Skype" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerIds" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerFullNames" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerBillingNames" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ActiveContracts" type="int" required=true %}
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

> 🔒 Requires user role `team-edit`


{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/spaces/teams/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a team.  
  
Required User Roles: `team-delete`
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



> 🔒 Requires user role `team-delete`


## Commands

Commands allow to perform actions against one or more team records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/teams/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for team records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/teams/runcommand" %}
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

> 🔒 Requires user role `team-edit`

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/teams/getteamlogo/:id" %}
{% api-method-summary %}
TeamLogo
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

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Team to get the teamlogo for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/teams/getteamimage1/:id" %}
{% api-method-summary %}
TeamImage1
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

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Team to get the teamimage1 for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/teams/getteamimage2/:id" %}
{% api-method-summary %}
TeamImage2
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

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Team to get the teamimage2 for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/teams/getteamimage3/:id" %}
{% api-method-summary %}
TeamImage3
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

{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Team to get the teamimage3 for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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
* [Business](../sys/business.md)
* [Coworker](../spaces/coworker.md)
