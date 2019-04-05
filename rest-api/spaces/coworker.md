---
description: 'Coworkers represent your customers, both members and contacts.'
---

# Coworker

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkers based on one or more filter parameters
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="CoworkerType" type="integer" %}
?Coworker\_CoworkerType=...
{% endapi-method-parameter %}

{% api-method-parameter name="FullName" type="string" %}
?Coworker\_FullName=...
{% endapi-method-parameter %}

{% api-method-parameter name="Salutation" type="string" %}
?Coworker\_Salutation=...
{% endapi-method-parameter %}

{% api-method-parameter name="Gender" type="integer" %}
?Coworker\_Gender=...
{% endapi-method-parameter %}

{% api-method-parameter name="Email" type="string" %}
?Coworker\_Email=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreateUser" type="bool" %}
?Coworker\_CreateUser=...
{% endapi-method-parameter %}

{% api-method-parameter name="Address" type="string" %}
?Coworker\_Address=...
{% endapi-method-parameter %}

{% api-method-parameter name="PostCode" type="string" %}
?Coworker\_PostCode=...
{% endapi-method-parameter %}

{% api-method-parameter name="CityName" type="string" %}
?Coworker\_CityName=...
{% endapi-method-parameter %}

{% api-method-parameter name="State" type="string" %}
?Coworker\_State=...
{% endapi-method-parameter %}

{% api-method-parameter name="Country" type="int" %}
?Coworker\_Country=...
{% endapi-method-parameter %}

{% api-method-parameter name="SimpleTimeZone" type="int" %}
?Coworker\_SimpleTimeZone=...
{% endapi-method-parameter %}

{% api-method-parameter name="MobilePhone" type="string" %}
?Coworker\_MobilePhone=...
{% endapi-method-parameter %}

{% api-method-parameter name="LandLine" type="string" %}
?Coworker\_LandLine=...
{% endapi-method-parameter %}

{% api-method-parameter name="DateOfBirth" type="DateTime?" %}
?Coworker\_DateOfBirth=...
{% endapi-method-parameter %}

{% api-method-parameter name="NickName" type="string" %}
?Coworker\_NickName=...
{% endapi-method-parameter %}

{% api-method-parameter name="BusinessArea" type="string" %}
?Coworker\_BusinessArea=...
{% endapi-method-parameter %}

{% api-method-parameter name="Position" type="string" %}
?Coworker\_Position=...
{% endapi-method-parameter %}

{% api-method-parameter name="CompanyName" type="string" %}
?Coworker\_CompanyName=...
{% endapi-method-parameter %}

{% api-method-parameter name="ProfileWebsite" type="string" %}
?Coworker\_ProfileWebsite=...
{% endapi-method-parameter %}

{% api-method-parameter name="ProfileTags" type="string" %}
?Coworker\_ProfileTags=...
{% endapi-method-parameter %}

{% api-method-parameter name="ProfileSummary" type="string" %}
?Coworker\_ProfileSummary=...
{% endapi-method-parameter %}

{% api-method-parameter name="Twitter" type="string" %}
?Coworker\_Twitter=...
{% endapi-method-parameter %}

{% api-method-parameter name="Facebook" type="string" %}
?Coworker\_Facebook=...
{% endapi-method-parameter %}

{% api-method-parameter name="Google" type="string" %}
?Coworker\_Google=...
{% endapi-method-parameter %}

{% api-method-parameter name="Telegram" type="string" %}
?Coworker\_Telegram=...
{% endapi-method-parameter %}

{% api-method-parameter name="Linkedin" type="string" %}
?Coworker\_Linkedin=...
{% endapi-method-parameter %}

{% api-method-parameter name="Skype" type="string" %}
?Coworker\_Skype=...
{% endapi-method-parameter %}

{% api-method-parameter name="Github" type="string" %}
?Coworker\_Github=...
{% endapi-method-parameter %}

{% api-method-parameter name="Pinterest" type="string" %}
?Coworker\_Pinterest=...
{% endapi-method-parameter %}

{% api-method-parameter name="Flickr" type="string" %}
?Coworker\_Flickr=...
{% endapi-method-parameter %}

{% api-method-parameter name="Instagram" type="string" %}
?Coworker\_Instagram=...
{% endapi-method-parameter %}

{% api-method-parameter name="Vimeo" type="string" %}
?Coworker\_Vimeo=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tumblr" type="string" %}
?Coworker\_Tumblr=...
{% endapi-method-parameter %}

{% api-method-parameter name="Blogger" type="string" %}
?Coworker\_Blogger=...
{% endapi-method-parameter %}

{% api-method-parameter name="ProfileIsPublic" type="bool" %}
?Coworker\_ProfileIsPublic=...
{% endapi-method-parameter %}

{% api-method-parameter name="InvoicingBusiness" type="int" %}
?Coworker\_InvoicingBusiness=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingEmail" type="string" %}
?Coworker\_BillingEmail=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingName" type="string" %}
?Coworker\_BillingName=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingAddress" type="string" %}
?Coworker\_BillingAddress=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingPostCode" type="string" %}
?Coworker\_BillingPostCode=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingCityName" type="string" %}
?Coworker\_BillingCityName=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingState" type="string" %}
?Coworker\_BillingState=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingCountry" type="int" %}
?Coworker\_BillingCountry=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingSimpleTimeZone" type="int" %}
?Coworker\_BillingSimpleTimeZone=...
{% endapi-method-parameter %}

{% api-method-parameter name="TaxRate" type="decimal?" %}
?Coworker\_TaxRate=...
{% endapi-method-parameter %}

{% api-method-parameter name="TaxIDNumber" type="string" %}
?Coworker\_TaxIDNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="BankName" type="string" %}
?Coworker\_BankName=...
{% endapi-method-parameter %}

{% api-method-parameter name="BankAccount" type="string" %}
?Coworker\_BankAccount=...
{% endapi-method-parameter %}

{% api-method-parameter name="BankBranch" type="string" %}
?Coworker\_BankBranch=...
{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnNewInvoice" type="bool" %}
?Coworker\_NotifyOnNewInvoice=...
{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnNewPayment" type="bool" %}
?Coworker\_NotifyOnNewPayment=...
{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnFailedPayment" type="bool" %}
?Coworker\_NotifyOnFailedPayment=...
{% endapi-method-parameter %}

{% api-method-parameter name="ShowPayingMemberInvoices" type="bool" %}
?Coworker\_ShowPayingMemberInvoices=...
{% endapi-method-parameter %}

{% api-method-parameter name="EnableGoCardlessPayments" type="bool" %}
?Coworker\_EnableGoCardlessPayments=...
{% endapi-method-parameter %}

{% api-method-parameter name="UseGoCardlessProPayments" type="bool" %}
?Coworker\_UseGoCardlessProPayments=...
{% endapi-method-parameter %}

{% api-method-parameter name="GoCardlessContractNumber" type="string" %}
?Coworker\_GoCardlessContractNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="LastOverDueInvoiceReminder" type="DateTime?" %}
?Coworker\_LastOverDueInvoiceReminder=...
{% endapi-method-parameter %}

{% api-method-parameter name="LastLowCreditReminder" type="DateTime?" %}
?Coworker\_LastLowCreditReminder=...
{% endapi-method-parameter %}

{% api-method-parameter name="RefererGuid" type="Guid?" %}
?Coworker\_RefererGuid=...
{% endapi-method-parameter %}

{% api-method-parameter name="RegularPaymentProvider" type="integer" %}
?Coworker\_RegularPaymentProvider=...
{% endapi-method-parameter %}

{% api-method-parameter name="RegularPaymentContractNumber" type="string" %}
?Coworker\_RegularPaymentContractNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="CardNumber" type="string" %}
?Coworker\_CardNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="DoNotProcessInvoicesAutomatically" type="bool" %}
?Coworker\_DoNotProcessInvoicesAutomatically=...
{% endapi-method-parameter %}

{% api-method-parameter name="AllowNetworkCheckin" type="bool" %}
?Coworker\_AllowNetworkCheckin=...
{% endapi-method-parameter %}

{% api-method-parameter name="CheckinSinceLastRenewal" type="int" %}
?Coworker\_CheckinSinceLastRenewal=...
{% endapi-method-parameter %}

{% api-method-parameter name="MinutesSinceLastRenewal" type="int" %}
?Coworker\_MinutesSinceLastRenewal=...
{% endapi-method-parameter %}

{% api-method-parameter name="AccessCardId" type="string" %}
?Coworker\_AccessCardId=...
{% endapi-method-parameter %}

{% api-method-parameter name="AccessPincode" type="string" %}
?Coworker\_AccessPincode=...
{% endapi-method-parameter %}

{% api-method-parameter name="KeyFobNumber" type="string" %}
?Coworker\_KeyFobNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnDelivery" type="bool" %}
?Coworker\_NotifyOnDelivery=...
{% endapi-method-parameter %}

{% api-method-parameter name="EzeepUserId" type="Guid?" %}
?Coworker\_EzeepUserId=...
{% endapi-method-parameter %}

{% api-method-parameter name="EzeepFreePrinting" type="bool" %}
?Coworker\_EzeepFreePrinting=...
{% endapi-method-parameter %}

{% api-method-parameter name="PaperCutPayAsYouPrint" type="bool" %}
?Coworker\_PaperCutPayAsYouPrint=...
{% endapi-method-parameter %}

{% api-method-parameter name="PaperCutFreePrinting" type="bool" %}
?Coworker\_PaperCutFreePrinting=...
{% endapi-method-parameter %}

{% api-method-parameter name="ReferenceNumber" type="string" %}
?Coworker\_ReferenceNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tag" type="string" %}
?Coworker\_Tag=...
{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" %}
?Coworker\_Notes=...
{% endapi-method-parameter %}

{% api-method-parameter name="ShowAlert" type="bool" %}
?Coworker\_ShowAlert=...
{% endapi-method-parameter %}

{% api-method-parameter name="AlertNote" type="string" %}
?Coworker\_AlertNote=...
{% endapi-method-parameter %}

{% api-method-parameter name="User" type="int" %}
?Coworker\_User=...
{% endapi-method-parameter %}

{% api-method-parameter name="Active" type="bool" %}
?Coworker\_Active=...
{% endapi-method-parameter %}

{% api-method-parameter name="NextAutoInvoice" type="DateTime?" %}
?Coworker\_NextAutoInvoice=...
{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceDueDatePeriod" type="int?" %}
?Coworker\_InvoiceDueDatePeriod=...
{% endapi-method-parameter %}

{% api-method-parameter name="RegistrationDate" type="DateTime?" %}
?Coworker\_RegistrationDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="GeneralTermsAccepted" type="bool" %}
?Coworker\_GeneralTermsAccepted=...
{% endapi-method-parameter %}

{% api-method-parameter name="LastRenewal" type="DateTime?" %}
?Coworker\_LastRenewal=...
{% endapi-method-parameter %}

{% api-method-parameter name="LastInvoiceAttempt" type="DateTime?" %}
?Coworker\_LastInvoiceAttempt=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom1" type="string" %}
?Coworker\_Custom1=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom2" type="string" %}
?Coworker\_Custom2=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom3" type="string" %}
?Coworker\_Custom3=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom4" type="string" %}
?Coworker\_Custom4=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom5" type="string" %}
?Coworker\_Custom5=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom6" type="string" %}
?Coworker\_Custom6=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom7" type="string" %}
?Coworker\_Custom7=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom8" type="string" %}
?Coworker\_Custom8=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom9" type="string" %}
?Coworker\_Custom9=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom10" type="string" %}
?Coworker\_Custom10=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom11" type="string" %}
?Coworker\_Custom11=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom12" type="string" %}
?Coworker\_Custom12=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom13" type="string" %}
?Coworker\_Custom13=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom14" type="string" %}
?Coworker\_Custom14=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom15" type="string" %}
?Coworker\_Custom15=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom16" type="string" %}
?Coworker\_Custom16=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom17" type="string" %}
?Coworker\_Custom17=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom18" type="string" %}
?Coworker\_Custom18=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom19" type="string" %}
?Coworker\_Custom19=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom20" type="string" %}
?Coworker\_Custom20=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom21" type="string" %}
?Coworker\_Custom21=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom22" type="string" %}
?Coworker\_Custom22=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom23" type="string" %}
?Coworker\_Custom23=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom24" type="string" %}
?Coworker\_Custom24=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom25" type="string" %}
?Coworker\_Custom25=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom26" type="string" %}
?Coworker\_Custom26=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom27" type="string" %}
?Coworker\_Custom27=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom28" type="string" %}
?Coworker\_Custom28=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom29" type="string" %}
?Coworker\_Custom29=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom30" type="string" %}
?Coworker\_Custom30=...
{% endapi-method-parameter %}

{% api-method-parameter name="NextInvoiceLocal" type="DateTime?" %}
?Coworker\_NextInvoiceLocal=...
{% endapi-method-parameter %}

{% api-method-parameter name="NextAutoInvoiceLocal" type="DateTime?" %}
?Coworker\_NextAutoInvoiceLocal=...
{% endapi-method-parameter %}

{% api-method-parameter name="RegistrationDateLocal" type="DateTime?" %}
?Coworker\_RegistrationDateLocal=...
{% endapi-method-parameter %}

{% api-method-parameter name="AccessControlDebounceTime" type="DateTime?" %}
?Coworker\_AccessControlDebounceTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="Office365AccessToken" type="string" %}
?Coworker\_Office365AccessToken=...
{% endapi-method-parameter %}

{% api-method-parameter name="Office365RefreshToken" type="string" %}
?Coworker\_Office365RefreshToken=...
{% endapi-method-parameter %}

{% api-method-parameter name="Office365SubscriptionId" type="string" %}
?Coworker\_Office365SubscriptionId=...
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "Records": [{
        "FullName": "Name",
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

> 🔒 Requires user role `coworker-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
REPLACE\_WITH\_LIST\_DESCRIPTION
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
        "FullName": "Name",
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

> 🔒 Requires user role `coworker-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of coworkers based on the date when they were created or updated.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="CreatedOn" type="object" required=false %}
?to\_Coworker\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_Coworker\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_Coworker\_CreatedOn=...
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
        "FullName": "Name",
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

> 🔒 Requires user role `coworker-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one coworker record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the coworker to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "FullName": "Name"
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

> 🔒 Requires user role `coworker-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/spaces/coworkers" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new coworker.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="FullName" type="string" required=true %}

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
        "FullName": "Name",
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

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

> 🔒 Requires user role `coworker-create`

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/spaces/coworkers" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing coworker  
  
Required User Role: `coworker-edit`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="FullName" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Id" type="integer" required=true %}
The id of the record to update
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

> 🔒 Requires user role `coworker-edit`

{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/spaces/coworkers/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a coworker.  
  
Required User Roles: `coworker-delete`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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

> 🔒 Requires user role `coworker-delete`

## Commands

Commands allow to perform actions against one or more coworker records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all command available to run for coworker records.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
_This response is an example, commands are regularly added to different entities._  
{% endapi-method-response-example-description %}

```javascript
[
    {
        "Key": "COWORKER_SENDWELCOME",
        "Name": "Send welcome email",
        "AppliesOnlyToMultipleEntities": false,
        "AppliesOnlyToOneEntity": false,
        "AppliesOnlyToTwoEntities": false,
        "NeedsEntitiesToRun": true,
        "Order": 2,
        "RequiresParameters": []
    },
    {
        "Key": "COWORKER_NEW_USER",
        "Name": "Create user for this member",
        "AppliesOnlyToMultipleEntities": false,
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers/runcommand" %}
{% api-method-summary %}
Run Command
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="Key" type="string" required=true %}
The command Key defining the command to run.  
  
`"ADD_COWORKER_TO_GROUP"`
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
  
`[33892859, 123565978]`
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

> 🔒 Requires user role `coworker-edit`

## Binary files

The following endpoints return binary. Check the `ContentType` header to understand the type of file being returned in the response stream.

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers/getavatar/:id" %}
{% api-method-summary %}
Avatar
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the coworker to get the avatar for.
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

* [Business](../../)
* [Team](../../)

