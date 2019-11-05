# Coworker

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of coworkers based on one or more filter querystring parameters.
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
?Coworker_SystemId=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerType" type="enum" %}
?Coworker_CoworkerType=...
{% endapi-method-parameter %}

{% api-method-parameter name="FullName" type="string" %}
?Coworker_FullName=...
{% endapi-method-parameter %}

{% api-method-parameter name="Salutation" type="string" %}
?Coworker_Salutation=...
{% endapi-method-parameter %}

{% api-method-parameter name="Gender" type="enum" %}
?Coworker_Gender=...
{% endapi-method-parameter %}

{% api-method-parameter name="Email" type="string" %}
?Coworker_Email=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreateUser" type="bool" %}
?Coworker_CreateUser=...
{% endapi-method-parameter %}

{% api-method-parameter name="Address" type="string" %}
?Coworker_Address=...
{% endapi-method-parameter %}

{% api-method-parameter name="PostCode" type="string" %}
?Coworker_PostCode=...
{% endapi-method-parameter %}

{% api-method-parameter name="CityName" type="string" %}
?Coworker_CityName=...
{% endapi-method-parameter %}

{% api-method-parameter name="State" type="string" %}
?Coworker_State=...
{% endapi-method-parameter %}

{% api-method-parameter name="Country" type="Country" %}
?Coworker_Country=...
{% endapi-method-parameter %}

{% api-method-parameter name="SimpleTimeZone" type="SimpleTimeZone" %}
?Coworker_SimpleTimeZone=...
{% endapi-method-parameter %}

{% api-method-parameter name="MobilePhone" type="string" %}
?Coworker_MobilePhone=...
{% endapi-method-parameter %}

{% api-method-parameter name="LandLine" type="string" %}
?Coworker_LandLine=...
{% endapi-method-parameter %}

{% api-method-parameter name="DateOfBirth" type="DateTime?" %}
?Coworker_DateOfBirth=...
{% endapi-method-parameter %}

{% api-method-parameter name="NickName" type="string" %}
?Coworker_NickName=...
{% endapi-method-parameter %}

{% api-method-parameter name="BusinessArea" type="string" %}
?Coworker_BusinessArea=...
{% endapi-method-parameter %}

{% api-method-parameter name="Position" type="string" %}
?Coworker_Position=...
{% endapi-method-parameter %}

{% api-method-parameter name="CompanyName" type="string" %}
?Coworker_CompanyName=...
{% endapi-method-parameter %}

{% api-method-parameter name="ProfileWebsite" type="string" %}
?Coworker_ProfileWebsite=...
{% endapi-method-parameter %}

{% api-method-parameter name="ProfileTags" type="string" %}
?Coworker_ProfileTags=...
{% endapi-method-parameter %}

{% api-method-parameter name="ProfileSummary" type="string" %}
?Coworker_ProfileSummary=...
{% endapi-method-parameter %}

{% api-method-parameter name="Twitter" type="string" %}
?Coworker_Twitter=...
{% endapi-method-parameter %}

{% api-method-parameter name="Facebook" type="string" %}
?Coworker_Facebook=...
{% endapi-method-parameter %}

{% api-method-parameter name="Google" type="string" %}
?Coworker_Google=...
{% endapi-method-parameter %}

{% api-method-parameter name="Telegram" type="string" %}
?Coworker_Telegram=...
{% endapi-method-parameter %}

{% api-method-parameter name="Linkedin" type="string" %}
?Coworker_Linkedin=...
{% endapi-method-parameter %}

{% api-method-parameter name="Skype" type="string" %}
?Coworker_Skype=...
{% endapi-method-parameter %}

{% api-method-parameter name="Github" type="string" %}
?Coworker_Github=...
{% endapi-method-parameter %}

{% api-method-parameter name="Pinterest" type="string" %}
?Coworker_Pinterest=...
{% endapi-method-parameter %}

{% api-method-parameter name="Flickr" type="string" %}
?Coworker_Flickr=...
{% endapi-method-parameter %}

{% api-method-parameter name="Instagram" type="string" %}
?Coworker_Instagram=...
{% endapi-method-parameter %}

{% api-method-parameter name="Vimeo" type="string" %}
?Coworker_Vimeo=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tumblr" type="string" %}
?Coworker_Tumblr=...
{% endapi-method-parameter %}

{% api-method-parameter name="Blogger" type="string" %}
?Coworker_Blogger=...
{% endapi-method-parameter %}

{% api-method-parameter name="ProfileIsPublic" type="bool" %}
?Coworker_ProfileIsPublic=...
{% endapi-method-parameter %}

{% api-method-parameter name="InvoicingBusiness" type="Business" %}
?Coworker_InvoicingBusiness=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingEmail" type="string" %}
?Coworker_BillingEmail=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingName" type="string" %}
?Coworker_BillingName=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingAddress" type="string" %}
?Coworker_BillingAddress=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingPostCode" type="string" %}
?Coworker_BillingPostCode=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingCityName" type="string" %}
?Coworker_BillingCityName=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingState" type="string" %}
?Coworker_BillingState=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingCountry" type="Country" %}
?Coworker_BillingCountry=...
{% endapi-method-parameter %}

{% api-method-parameter name="BillingSimpleTimeZone" type="SimpleTimeZone" %}
?Coworker_BillingSimpleTimeZone=...
{% endapi-method-parameter %}

{% api-method-parameter name="TaxRate" type="decimal?" %}
?Coworker_TaxRate=...
{% endapi-method-parameter %}

{% api-method-parameter name="TaxIDNumber" type="string" %}
?Coworker_TaxIDNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="BankName" type="string" %}
?Coworker_BankName=...
{% endapi-method-parameter %}

{% api-method-parameter name="BankAccount" type="string" %}
?Coworker_BankAccount=...
{% endapi-method-parameter %}

{% api-method-parameter name="BankBranch" type="string" %}
?Coworker_BankBranch=...
{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnNewInvoice" type="bool" %}
?Coworker_NotifyOnNewInvoice=...
{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnNewPayment" type="bool" %}
?Coworker_NotifyOnNewPayment=...
{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnFailedPayment" type="bool" %}
?Coworker_NotifyOnFailedPayment=...
{% endapi-method-parameter %}

{% api-method-parameter name="ShowPayingMemberInvoices" type="bool" %}
?Coworker_ShowPayingMemberInvoices=...
{% endapi-method-parameter %}

{% api-method-parameter name="EnableGoCardlessPayments" type="bool" %}
?Coworker_EnableGoCardlessPayments=...
{% endapi-method-parameter %}

{% api-method-parameter name="GoCardlessContractNumber" type="string" %}
?Coworker_GoCardlessContractNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="RegularPaymentProvider" type="enum" %}
?Coworker_RegularPaymentProvider=...
{% endapi-method-parameter %}

{% api-method-parameter name="RegularPaymentContractNumber" type="string" %}
?Coworker_RegularPaymentContractNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="CardNumber" type="string" %}
?Coworker_CardNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="DoNotProcessInvoicesAutomatically" type="bool" %}
?Coworker_DoNotProcessInvoicesAutomatically=...
{% endapi-method-parameter %}

{% api-method-parameter name="AllowNetworkCheckin" type="bool" %}
?Coworker_AllowNetworkCheckin=...
{% endapi-method-parameter %}

{% api-method-parameter name="CheckinSinceLastRenewal" type="int" %}
?Coworker_CheckinSinceLastRenewal=...
{% endapi-method-parameter %}

{% api-method-parameter name="MinutesSinceLastRenewal" type="int" %}
?Coworker_MinutesSinceLastRenewal=...
{% endapi-method-parameter %}

{% api-method-parameter name="AccessCardId" type="string" %}
?Coworker_AccessCardId=...
{% endapi-method-parameter %}

{% api-method-parameter name="AccessPincode" type="string" %}
?Coworker_AccessPincode=...
{% endapi-method-parameter %}

{% api-method-parameter name="KeyFobNumber" type="string" %}
?Coworker_KeyFobNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnDelivery" type="bool" %}
?Coworker_NotifyOnDelivery=...
{% endapi-method-parameter %}

{% api-method-parameter name="EzeepUserId" type="Guid?" %}
?Coworker_EzeepUserId=...
{% endapi-method-parameter %}

{% api-method-parameter name="EzeepFreePrinting" type="bool" %}
?Coworker_EzeepFreePrinting=...
{% endapi-method-parameter %}

{% api-method-parameter name="PaperCutPayAsYouPrint" type="bool" %}
?Coworker_PaperCutPayAsYouPrint=...
{% endapi-method-parameter %}

{% api-method-parameter name="PaperCutFreePrinting" type="bool" %}
?Coworker_PaperCutFreePrinting=...
{% endapi-method-parameter %}

{% api-method-parameter name="CanMakeBookings" type="bool" %}
?Coworker\_CanMakeBookings=...
{% endapi-method-parameter %}

{% api-method-parameter name="CanPurchaseProducts" type="bool" %}
?Coworker\_CanPurchaseProducts=...
{% endapi-method-parameter %}

{% api-method-parameter name="CanPurchaseEvents" type="bool" %}
?Coworker\_CanPurchaseEvents=...
{% endapi-method-parameter %}

{% api-method-parameter name="CanAccessCommunity" type="bool" %}
?Coworker\_CanAccessCommunity=...
{% endapi-method-parameter %}

{% api-method-parameter name="CanPurchaseProducts" type="bool" %}
?Coworker_CanPurchaseProducts=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tag" type="string" %}
?Coworker\_Tag=...
{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" %}
?Coworker\_Notes=...
{% endapi-method-parameter %}

{% api-method-parameter name="ShowAlert" type="bool" %}
?Coworker_ShowAlert=...
{% endapi-method-parameter %}

{% api-method-parameter name="AlertNote" type="string" %}
?Coworker_AlertNote=...
{% endapi-method-parameter %}

{% api-method-parameter name="User" type="User" %}
?Coworker_User=...
{% endapi-method-parameter %}

{% api-method-parameter name="Active" type="bool" %}
?Coworker_Active=...
{% endapi-method-parameter %}

{% api-method-parameter name="NextAutoInvoice" type="DateTime?" %}
?Coworker_NextAutoInvoice=...
{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceDueDatePeriod" type="int?" %}
?Coworker_InvoiceDueDatePeriod=...
{% endapi-method-parameter %}

{% api-method-parameter name="RegistrationDate" type="DateTime?" %}
?Coworker_RegistrationDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="GeneralTermsAccepted" type="bool" %}
?Coworker_GeneralTermsAccepted=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom1" type="string" %}
?Coworker_Custom1=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom2" type="string" %}
?Coworker_Custom2=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom3" type="string" %}
?Coworker_Custom3=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom4" type="string" %}
?Coworker_Custom4=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom5" type="string" %}
?Coworker_Custom5=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom6" type="string" %}
?Coworker_Custom6=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom7" type="string" %}
?Coworker_Custom7=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom8" type="string" %}
?Coworker_Custom8=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom9" type="string" %}
?Coworker_Custom9=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom10" type="string" %}
?Coworker_Custom10=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom11" type="string" %}
?Coworker_Custom11=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom12" type="string" %}
?Coworker_Custom12=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom13" type="string" %}
?Coworker_Custom13=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom14" type="string" %}
?Coworker_Custom14=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom15" type="string" %}
?Coworker_Custom15=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom16" type="string" %}
?Coworker_Custom16=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom17" type="string" %}
?Coworker_Custom17=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom18" type="string" %}
?Coworker_Custom18=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom19" type="string" %}
?Coworker_Custom19=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom20" type="string" %}
?Coworker_Custom20=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom21" type="string" %}
?Coworker_Custom21=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom22" type="string" %}
?Coworker_Custom22=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom23" type="string" %}
?Coworker_Custom23=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom24" type="string" %}
?Coworker_Custom24=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom25" type="string" %}
?Coworker_Custom25=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom26" type="string" %}
?Coworker_Custom26=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom27" type="string" %}
?Coworker_Custom27=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom28" type="string" %}
?Coworker_Custom28=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom29" type="string" %}
?Coworker_Custom29=...
{% endapi-method-parameter %}

{% api-method-parameter name="Custom30" type="string" %}
?Coworker_Custom30=...
{% endapi-method-parameter %}

{% api-method-parameter name="PurchaseOrder" type="string" %}
?Coworker_PurchaseOrder=...
{% endapi-method-parameter %}

{% api-method-parameter name="InvoicingBusiness\_Name" type="string" %}
?Coworker_InvoicingBusiness_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="User\_FullName" type="string" %}
?Coworker_User_FullName=...
{% endapi-method-parameter %}

{% api-method-parameter name="User\_IsAdmin" type="string" %}
?Coworker_User_IsAdmin=...
{% endapi-method-parameter %}

{% api-method-parameter name="User\_LastAccess" type="string" %}
?Coworker_User_LastAccess=...
{% endapi-method-parameter %}

{% api-method-parameter name="User\_Active" type="string" %}
?Coworker_User_Active=...
{% endapi-method-parameter %}

{% api-method-parameter name="User\_ReceiveCommunityDigest" type="string" %}
?Coworker_User_ReceiveCommunityDigest=...
{% endapi-method-parameter %}

{% api-method-parameter name="User\_ReceiveEveryMessage" type="string" %}
?Coworker_User_ReceiveEveryMessage=...
{% endapi-method-parameter %}

{% api-method-parameter name="Businesses" type="int" required=false %}
?Coworker_Businesses=...
{% endapi-method-parameter %}

{% api-method-parameter name="Teams" type="int" required=false %}
?Coworker_Teams=...
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
        "CoworkerType": Nexudus.Coworking.Core.Enums.eCoworkerRecordType.Individual,
        "FullName": "Name",
        "Salutation": "Name",
        "Gender": Nexudus.Coworking.Core.Enums.eGender.NotSet,
        "Email": "email@email.com",
        "CreateUser": true,
        "Address": "Address",
        "PostCode": "PostCode",
        "CityName": "CityName",
        "State": "State",
        "Country": null,
        "SimpleTimeZone": null,
        "MobilePhone": "MobilePhone",
        "LandLine": "LandLine",
        "DateOfBirth": null,
        "NickName": "NickName",
        "BusinessArea": "BusinessArea",
        "Position": "Position",
        "CompanyName": "CompanyName",
        "ProfileWebsite": "ProfileWebsite",
        "ProfileTags": "BusinessArea",
        "ProfileSummary": "BusinessArea",
        "Twitter": "Twitter",
        "Facebook": "Facebook",
        "Google": "Google",
        "Telegram": "Telegram",
        "Linkedin": "Linkedin",
        "Skype": "Skype",
        "Github": "Github",
        "Pinterest": "Pinterest",
        "Flickr": "Flickr",
        "Instagram": "Instagram",
        "Vimeo": "Vimeo",
        "Tumblr": "Tumblr",
        "Blogger": "Blogger",
        "ProfileIsPublic": true,
        "InvoicingBusiness": null,
        "BillingEmail": "Address",
        "BillingName": "Address",
        "BillingAddress": "Address",
        "BillingPostCode": "PostCode",
        "BillingCityName": "CityName",
        "BillingState": "State",
        "BillingCountry": null,
        "BillingSimpleTimeZone": null,
        "TaxRate": 0,
        "TaxIDNumber": "State",
        "BankName": "Bank Name",
        "BankAccount": "Bank Account #",
        "BankBranch": "Branch / Sort Code",
        "NotifyOnNewInvoice": true,
        "NotifyOnNewPayment": true,
        "NotifyOnFailedPayment": true,
        "ShowPayingMemberInvoices": true,
        "EnableGoCardlessPayments": false,
        "GoCardlessContractNumber": "false",
        "RegularPaymentProvider": Nexudus.Coworking.Core.Enums.eRegularPaymentProvider.Manual,
        "RegularPaymentContractNumber": "false",
        "CardNumber": "",
        "DoNotProcessInvoicesAutomatically": false,
        "AllowNetworkCheckin": false,
        "CheckinSinceLastRenewal": 0,
        "MinutesSinceLastRenewal": 0,
        "AccessCardId": "Notes",
        "AccessPincode": "Notes",
        "KeyFobNumber": "Notes",
        "NotifyOnDelivery": null,
        "EzeepUserId": null,
        "EzeepFreePrinting": null,
        "PaperCutPayAsYouPrint": false,
        "PaperCutFreePrinting": null,
        "CanMakeBookings": false,
        "CanPurchaseProducts": false,
        "CanPurchaseEvents": false,
        "CanAccessCommunity": false,
        "ReferenceNumber": "ReferenceNumber",
        "Tag": "Tag",
        "Notes": "Notes",
        "ShowAlert": false,
        "AlertNote": "Tag",
        "User": null,
        "Active": true,
        "NextAutoInvoice": null,
        "InvoiceDueDatePeriod": null,
        "RegistrationDate": null,
        "GeneralTermsAccepted": true,
        "Custom1": "Custom1",
        "Custom2": "Custom1",
        "Custom3": "Custom1",
        "Custom4": "Custom1",
        "Custom5": "Custom1",
        "Custom6": "Custom1",
        "Custom7": "Custom1",
        "Custom8": "Custom1",
        "Custom9": "Custom1",
        "Custom10": "Custom1",
        "Custom11": "Custom1",
        "Custom12": "Custom1",
        "Custom13": "Custom1",
        "Custom14": "Custom1",
        "Custom15": "Custom1",
        "Custom16": "Custom1",
        "Custom17": "Custom1",
        "Custom18": "Custom1",
        "Custom19": "Custom1",
        "Custom20": "Custom1",
        "Custom21": "Custom1",
        "Custom22": "Custom1",
        "Custom23": "Custom1",
        "Custom24": "Custom1",
        "Custom25": "Custom1",
        "Custom26": "Custom1",
        "Custom27": "Custom1",
        "Custom28": "Custom1",
        "Custom29": "Custom1",
        "Custom30": "Custom1",
        "PurchaseOrder": "false",
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
This endpoint allows you to GET a list of coworkers.
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
        "CoworkerType": Nexudus.Coworking.Core.Enums.eCoworkerRecordType.Individual,
        "FullName": "Name",
        "Salutation": "Name",
        "Gender": Nexudus.Coworking.Core.Enums.eGender.NotSet,
        "Email": "email@email.com",
        "CreateUser": true,
        "Address": "Address",
        "PostCode": "PostCode",
        "CityName": "CityName",
        "State": "State",
        "Country": null,
        "SimpleTimeZone": null,
        "MobilePhone": "MobilePhone",
        "LandLine": "LandLine",
        "DateOfBirth": null,
        "NickName": "NickName",
        "BusinessArea": "BusinessArea",
        "Position": "Position",
        "CompanyName": "CompanyName",
        "ProfileWebsite": "ProfileWebsite",
        "ProfileTags": "BusinessArea",
        "ProfileSummary": "BusinessArea",
        "Twitter": "Twitter",
        "Facebook": "Facebook",
        "Google": "Google",
        "Telegram": "Telegram",
        "Linkedin": "Linkedin",
        "Skype": "Skype",
        "Github": "Github",
        "Pinterest": "Pinterest",
        "Flickr": "Flickr",
        "Instagram": "Instagram",
        "Vimeo": "Vimeo",
        "Tumblr": "Tumblr",
        "Blogger": "Blogger",
        "ProfileIsPublic": true,
        "InvoicingBusiness": null,
        "BillingEmail": "Address",
        "BillingName": "Address",
        "BillingAddress": "Address",
        "BillingPostCode": "PostCode",
        "BillingCityName": "CityName",
        "BillingState": "State",
        "BillingCountry": null,
        "BillingSimpleTimeZone": null,
        "TaxRate": 0,
        "TaxIDNumber": "State",
        "BankName": "Bank Name",
        "BankAccount": "Bank Account #",
        "BankBranch": "Branch / Sort Code",
        "NotifyOnNewInvoice": true,
        "NotifyOnNewPayment": true,
        "NotifyOnFailedPayment": true,
        "ShowPayingMemberInvoices": true,
        "EnableGoCardlessPayments": false,
        "GoCardlessContractNumber": "false",
        "RegularPaymentProvider": Nexudus.Coworking.Core.Enums.eRegularPaymentProvider.Manual,
        "RegularPaymentContractNumber": "false",
        "CardNumber": "",
        "DoNotProcessInvoicesAutomatically": false,
        "AllowNetworkCheckin": false,
        "CheckinSinceLastRenewal": 0,
        "MinutesSinceLastRenewal": 0,
        "AccessCardId": "Notes",
        "AccessPincode": "Notes",
        "KeyFobNumber": "Notes",
        "NotifyOnDelivery": null,
        "EzeepUserId": null,
        "EzeepFreePrinting": null,
        "PaperCutPayAsYouPrint": false,
        "PaperCutFreePrinting": null,
        "CanMakeBookings": false,
        "CanPurchaseProducts": false,
        "CanPurchaseEvents": false,
        "CanAccessCommunity": false,
        "ReferenceNumber": "ReferenceNumber",
        "Tag": "Tag",
        "Notes": "Notes",
        "ShowAlert": false,
        "AlertNote": "Tag",
        "User": null,
        "Active": true,
        "NextAutoInvoice": null,
        "InvoiceDueDatePeriod": null,
        "RegistrationDate": null,
        "GeneralTermsAccepted": true,
        "Custom1": "Custom1",
        "Custom2": "Custom1",
        "Custom3": "Custom1",
        "Custom4": "Custom1",
        "Custom5": "Custom1",
        "Custom6": "Custom1",
        "Custom7": "Custom1",
        "Custom8": "Custom1",
        "Custom9": "Custom1",
        "Custom10": "Custom1",
        "Custom11": "Custom1",
        "Custom12": "Custom1",
        "Custom13": "Custom1",
        "Custom14": "Custom1",
        "Custom15": "Custom1",
        "Custom16": "Custom1",
        "Custom17": "Custom1",
        "Custom18": "Custom1",
        "Custom19": "Custom1",
        "Custom20": "Custom1",
        "Custom21": "Custom1",
        "Custom22": "Custom1",
        "Custom23": "Custom1",
        "Custom24": "Custom1",
        "Custom25": "Custom1",
        "Custom26": "Custom1",
        "Custom27": "Custom1",
        "Custom28": "Custom1",
        "Custom29": "Custom1",
        "Custom30": "Custom1",
        "PurchaseOrder": "false",
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

> 🔒 Requires user role `coworker-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of coworkers based on a range of dates, integer or decimal properties.
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
?to_Coworker_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from_Coworker_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to_Coworker_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from_Coworker_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="DateOfBirth" type="datetime" required=false %}
?from_Coworker_DateOfBirth=...
{% endapi-method-parameter %}

{% api-method-parameter name="DateOfBirth" type="datetime" required=false %}
?to_Coworker_DateOfBirth=...
{% endapi-method-parameter %}

{% api-method-parameter name="TaxRate" type="decimal" required=false %}
?from_Coworker_TaxRate=...
{% endapi-method-parameter %}

{% api-method-parameter name="TaxRate" type="decimal" required=false %}
?to_Coworker_TaxRate=...
{% endapi-method-parameter %}

{% api-method-parameter name="CheckinSinceLastRenewal" type="int" required=false %}
?from_Coworker_CheckinSinceLastRenewal=...
{% endapi-method-parameter %}

{% api-method-parameter name="CheckinSinceLastRenewal" type="int" required=false %}
?to_Coworker_CheckinSinceLastRenewal=...
{% endapi-method-parameter %}

{% api-method-parameter name="MinutesSinceLastRenewal" type="int" required=false %}
?from_Coworker_MinutesSinceLastRenewal=...
{% endapi-method-parameter %}

{% api-method-parameter name="MinutesSinceLastRenewal" type="int" required=false %}
?to_Coworker_MinutesSinceLastRenewal=...
{% endapi-method-parameter %}

{% api-method-parameter name="NextAutoInvoice" type="datetime" required=false %}
?from_Coworker_NextAutoInvoice=...
{% endapi-method-parameter %}

{% api-method-parameter name="NextAutoInvoice" type="datetime" required=false %}
?to_Coworker_NextAutoInvoice=...
{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceDueDatePeriod" type="int" required=false %}
?from_Coworker_InvoiceDueDatePeriod=...
{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceDueDatePeriod" type="int" required=false %}
?to_Coworker_InvoiceDueDatePeriod=...
{% endapi-method-parameter %}

{% api-method-parameter name="RegistrationDate" type="datetime" required=false %}
?from_Coworker_RegistrationDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="RegistrationDate" type="datetime" required=false %}
?to_Coworker_RegistrationDate=...
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
        "CoworkerType": Nexudus.Coworking.Core.Enums.eCoworkerRecordType.Individual,
        "FullName": "Name",
        "Salutation": "Name",
        "Gender": Nexudus.Coworking.Core.Enums.eGender.NotSet,
        "Email": "email@email.com",
        "CreateUser": true,
        "Address": "Address",
        "PostCode": "PostCode",
        "CityName": "CityName",
        "State": "State",
        "Country": null,
        "SimpleTimeZone": null,
        "MobilePhone": "MobilePhone",
        "LandLine": "LandLine",
        "DateOfBirth": null,
        "NickName": "NickName",
        "BusinessArea": "BusinessArea",
        "Position": "Position",
        "CompanyName": "CompanyName",
        "ProfileWebsite": "ProfileWebsite",
        "ProfileTags": "BusinessArea",
        "ProfileSummary": "BusinessArea",
        "Twitter": "Twitter",
        "Facebook": "Facebook",
        "Google": "Google",
        "Telegram": "Telegram",
        "Linkedin": "Linkedin",
        "Skype": "Skype",
        "Github": "Github",
        "Pinterest": "Pinterest",
        "Flickr": "Flickr",
        "Instagram": "Instagram",
        "Vimeo": "Vimeo",
        "Tumblr": "Tumblr",
        "Blogger": "Blogger",
        "ProfileIsPublic": true,
        "InvoicingBusiness": null,
        "BillingEmail": "Address",
        "BillingName": "Address",
        "BillingAddress": "Address",
        "BillingPostCode": "PostCode",
        "BillingCityName": "CityName",
        "BillingState": "State",
        "BillingCountry": null,
        "BillingSimpleTimeZone": null,
        "TaxRate": 0,
        "TaxIDNumber": "State",
        "BankName": "Bank Name",
        "BankAccount": "Bank Account #",
        "BankBranch": "Branch / Sort Code",
        "NotifyOnNewInvoice": true,
        "NotifyOnNewPayment": true,
        "NotifyOnFailedPayment": true,
        "ShowPayingMemberInvoices": true,
        "EnableGoCardlessPayments": false,
        "GoCardlessContractNumber": "false",
        "RegularPaymentProvider": Nexudus.Coworking.Core.Enums.eRegularPaymentProvider.Manual,
        "RegularPaymentContractNumber": "false",
        "CardNumber": "",
        "DoNotProcessInvoicesAutomatically": false,
        "AllowNetworkCheckin": false,
        "CheckinSinceLastRenewal": 0,
        "MinutesSinceLastRenewal": 0,
        "AccessCardId": "Notes",
        "AccessPincode": "Notes",
        "KeyFobNumber": "Notes",
        "NotifyOnDelivery": null,
        "EzeepUserId": null,
        "EzeepFreePrinting": null,
        "PaperCutPayAsYouPrint": false,
        "PaperCutFreePrinting": null,
        "CanMakeBookings": false,
        "CanPurchaseProducts": false,
        "CanPurchaseEvents": false,
        "CanAccessCommunity": false,
        "ReferenceNumber": "ReferenceNumber",
        "Tag": "Tag",
        "Notes": "Notes",
        "ShowAlert": false,
        "AlertNote": "Tag",
        "User": null,
        "Active": true,
        "NextAutoInvoice": null,
        "InvoiceDueDatePeriod": null,
        "RegistrationDate": null,
        "GeneralTermsAccepted": true,
        "Custom1": "Custom1",
        "Custom2": "Custom1",
        "Custom3": "Custom1",
        "Custom4": "Custom1",
        "Custom5": "Custom1",
        "Custom6": "Custom1",
        "Custom7": "Custom1",
        "Custom8": "Custom1",
        "Custom9": "Custom1",
        "Custom10": "Custom1",
        "Custom11": "Custom1",
        "Custom12": "Custom1",
        "Custom13": "Custom1",
        "Custom14": "Custom1",
        "Custom15": "Custom1",
        "Custom16": "Custom1",
        "Custom17": "Custom1",
        "Custom18": "Custom1",
        "Custom19": "Custom1",
        "Custom20": "Custom1",
        "Custom21": "Custom1",
        "Custom22": "Custom1",
        "Custom23": "Custom1",
        "Custom24": "Custom1",
        "Custom25": "Custom1",
        "Custom26": "Custom1",
        "Custom27": "Custom1",
        "Custom28": "Custom1",
        "Custom29": "Custom1",
        "Custom30": "Custom1",
        "PurchaseOrder": "false",
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

> 🔒 Requires user role `coworker-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers?Coworker\_Id=\[:id1,:id2,...\]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more coworker records based on their Id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every coworker to fetch. I.e. \[123456,789102,...\]
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
        "CoworkerType": Nexudus.Coworking.Core.Enums.eCoworkerRecordType.Individual,
        "FullName": "Name",
        "Salutation": "Name",
        "Gender": Nexudus.Coworking.Core.Enums.eGender.NotSet,
        "Email": "email@email.com",
        "CreateUser": true,
        "Address": "Address",
        "PostCode": "PostCode",
        "CityName": "CityName",
        "State": "State",
        "Country": null,
        "SimpleTimeZone": null,
        "MobilePhone": "MobilePhone",
        "LandLine": "LandLine",
        "DateOfBirth": null,
        "NickName": "NickName",
        "BusinessArea": "BusinessArea",
        "Position": "Position",
        "CompanyName": "CompanyName",
        "ProfileWebsite": "ProfileWebsite",
        "ProfileTags": "BusinessArea",
        "ProfileSummary": "BusinessArea",
        "Twitter": "Twitter",
        "Facebook": "Facebook",
        "Google": "Google",
        "Telegram": "Telegram",
        "Linkedin": "Linkedin",
        "Skype": "Skype",
        "Github": "Github",
        "Pinterest": "Pinterest",
        "Flickr": "Flickr",
        "Instagram": "Instagram",
        "Vimeo": "Vimeo",
        "Tumblr": "Tumblr",
        "Blogger": "Blogger",
        "ProfileIsPublic": true,
        "InvoicingBusiness": null,
        "BillingEmail": "Address",
        "BillingName": "Address",
        "BillingAddress": "Address",
        "BillingPostCode": "PostCode",
        "BillingCityName": "CityName",
        "BillingState": "State",
        "BillingCountry": null,
        "BillingSimpleTimeZone": null,
        "TaxRate": 0,
        "TaxIDNumber": "State",
        "BankName": "Bank Name",
        "BankAccount": "Bank Account #",
        "BankBranch": "Branch / Sort Code",
        "NotifyOnNewInvoice": true,
        "NotifyOnNewPayment": true,
        "NotifyOnFailedPayment": true,
        "ShowPayingMemberInvoices": true,
        "EnableGoCardlessPayments": false,
        "GoCardlessContractNumber": "false",
        "RegularPaymentProvider": Nexudus.Coworking.Core.Enums.eRegularPaymentProvider.Manual,
        "RegularPaymentContractNumber": "false",
        "CardNumber": "",
        "DoNotProcessInvoicesAutomatically": false,
        "AllowNetworkCheckin": false,
        "CheckinSinceLastRenewal": 0,
        "MinutesSinceLastRenewal": 0,
        "AccessCardId": "Notes",
        "AccessPincode": "Notes",
        "KeyFobNumber": "Notes",
        "NotifyOnDelivery": null,
        "EzeepUserId": null,
        "EzeepFreePrinting": null,
        "PaperCutPayAsYouPrint": false,
        "PaperCutFreePrinting": null,
        "CanMakeBookings": false,
        "CanPurchaseProducts": false,
        "CanPurchaseEvents": false,
        "CanAccessCommunity": false,
        "ReferenceNumber": "ReferenceNumber",
        "Tag": "Tag",
        "Notes": "Notes",
        "ShowAlert": false,
        "AlertNote": "Tag",
        "User": null,
        "Active": true,
        "NextAutoInvoice": null,
        "InvoiceDueDatePeriod": null,
        "RegistrationDate": null,
        "GeneralTermsAccepted": true,
        "Custom1": "Custom1",
        "Custom2": "Custom1",
        "Custom3": "Custom1",
        "Custom4": "Custom1",
        "Custom5": "Custom1",
        "Custom6": "Custom1",
        "Custom7": "Custom1",
        "Custom8": "Custom1",
        "Custom9": "Custom1",
        "Custom10": "Custom1",
        "Custom11": "Custom1",
        "Custom12": "Custom1",
        "Custom13": "Custom1",
        "Custom14": "Custom1",
        "Custom15": "Custom1",
        "Custom16": "Custom1",
        "Custom17": "Custom1",
        "Custom18": "Custom1",
        "Custom19": "Custom1",
        "Custom20": "Custom1",
        "Custom21": "Custom1",
        "Custom22": "Custom1",
        "Custom23": "Custom1",
        "Custom24": "Custom1",
        "Custom25": "Custom1",
        "Custom26": "Custom1",
        "Custom27": "Custom1",
        "Custom28": "Custom1",
        "Custom29": "Custom1",
        "Custom30": "Custom1",
        "PurchaseOrder": "false",
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
        "CoworkerType": Nexudus.Coworking.Core.Enums.eCoworkerRecordType.Individual,
        "FullName": "Name",
        "Salutation": "Name",
        "Gender": Nexudus.Coworking.Core.Enums.eGender.NotSet,
        "Email": "email@email.com",
        "CreateUser": true,
        "Address": "Address",
        "PostCode": "PostCode",
        "CityName": "CityName",
        "State": "State",
        "Country": null,
        "SimpleTimeZone": null,
        "MobilePhone": "MobilePhone",
        "LandLine": "LandLine",
        "DateOfBirth": null,
        "NickName": "NickName",
        "BusinessArea": "BusinessArea",
        "Position": "Position",
        "CompanyName": "CompanyName",
        "ProfileWebsite": "ProfileWebsite",
        "ProfileTags": "BusinessArea",
        "ProfileSummary": "BusinessArea",
        "Twitter": "Twitter",
        "Facebook": "Facebook",
        "Google": "Google",
        "Telegram": "Telegram",
        "Linkedin": "Linkedin",
        "Skype": "Skype",
        "Github": "Github",
        "Pinterest": "Pinterest",
        "Flickr": "Flickr",
        "Instagram": "Instagram",
        "Vimeo": "Vimeo",
        "Tumblr": "Tumblr",
        "Blogger": "Blogger",
        "ProfileIsPublic": true,
        "InvoicingBusiness": null,
        "BillingEmail": "Address",
        "BillingName": "Address",
        "BillingAddress": "Address",
        "BillingPostCode": "PostCode",
        "BillingCityName": "CityName",
        "BillingState": "State",
        "BillingCountry": null,
        "BillingSimpleTimeZone": null,
        "TaxRate": 0,
        "TaxIDNumber": "State",
        "BankName": "Bank Name",
        "BankAccount": "Bank Account #",
        "BankBranch": "Branch / Sort Code",
        "NotifyOnNewInvoice": true,
        "NotifyOnNewPayment": true,
        "NotifyOnFailedPayment": true,
        "ShowPayingMemberInvoices": true,
        "EnableGoCardlessPayments": false,
        "GoCardlessContractNumber": "false",
        "RegularPaymentProvider": Nexudus.Coworking.Core.Enums.eRegularPaymentProvider.Manual,
        "RegularPaymentContractNumber": "false",
        "CardNumber": "",
        "DoNotProcessInvoicesAutomatically": false,
        "AllowNetworkCheckin": false,
        "CheckinSinceLastRenewal": 0,
        "MinutesSinceLastRenewal": 0,
        "AccessCardId": "Notes",
        "AccessPincode": "Notes",
        "KeyFobNumber": "Notes",
        "NotifyOnDelivery": null,
        "EzeepUserId": null,
        "EzeepFreePrinting": null,
        "PaperCutPayAsYouPrint": false,
        "PaperCutFreePrinting": null,
        "CanMakeBookings": false,
        "CanPurchaseProducts": false,
        "CanPurchaseEvents": false,
        "CanAccessCommunity": false,
        "ReferenceNumber": "ReferenceNumber",
        "Tag": "Tag",
        "Notes": "Notes",
        "ShowAlert": false,
        "AlertNote": "Tag",
        "User": null,
        "Active": true,
        "NextAutoInvoice": null,
        "InvoiceDueDatePeriod": null,
        "RegistrationDate": null,
        "GeneralTermsAccepted": true,
        "Custom1": "Custom1",
        "Custom2": "Custom1",
        "Custom3": "Custom1",
        "Custom4": "Custom1",
        "Custom5": "Custom1",
        "Custom6": "Custom1",
        "Custom7": "Custom1",
        "Custom8": "Custom1",
        "Custom9": "Custom1",
        "Custom10": "Custom1",
        "Custom11": "Custom1",
        "Custom12": "Custom1",
        "Custom13": "Custom1",
        "Custom14": "Custom1",
        "Custom15": "Custom1",
        "Custom16": "Custom1",
        "Custom17": "Custom1",
        "Custom18": "Custom1",
        "Custom19": "Custom1",
        "Custom20": "Custom1",
        "Custom21": "Custom1",
        "Custom22": "Custom1",
        "Custom23": "Custom1",
        "Custom24": "Custom1",
        "Custom25": "Custom1",
        "Custom26": "Custom1",
        "Custom27": "Custom1",
        "Custom28": "Custom1",
        "Custom29": "Custom1",
        "Custom30": "Custom1",
        "PurchaseOrder": "false",
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
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="CoworkerType" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FullName" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Salutation" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Gender" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Email" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CreateUser" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Address" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PostCode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CityName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="State" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CountryId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="SimpleTimeZoneId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="MobilePhone" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LandLine" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DateOfBirth" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NickName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BusinessArea" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Position" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CompanyName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ProfileWebsite" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ProfileTags" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ProfileSummary" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Twitter" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Facebook" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Google" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Telegram" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Linkedin" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Skype" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Github" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Pinterest" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Flickr" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Instagram" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Vimeo" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Tumblr" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Blogger" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ProfileIsPublic" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="InvoicingBusinessId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingEmail" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingAddress" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingPostCode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingCityName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingState" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingCountryId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingSimpleTimeZoneId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TaxRate" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TaxIDNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BankName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BankAccount" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BankBranch" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnNewInvoice" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnNewPayment" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnFailedPayment" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ShowPayingMemberInvoices" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="EnableGoCardlessPayments" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="GoCardlessContractNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RegularPaymentProvider" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RegularPaymentContractNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DoNotProcessInvoicesAutomatically" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AllowNetworkCheckin" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AccessCardId" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AccessPincode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="KeyFobNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnDelivery" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="EzeepUserId" type="Guid?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="EzeepFreePrinting" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PaperCutPayAsYouPrint" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PaperCutFreePrinting" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CanMakeBookings" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CanPurchaseProducts" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CanPurchaseEvents" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CanAccessCommunity" type="bool" required=false %}

{% endapi-method-parameter %}
{% api-method-parameter name="ReferenceNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Tag" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ShowAlert" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AlertNote" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Active" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceDueDatePeriod" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RegistrationDate" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="GeneralTermsAccepted" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom1" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom2" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom3" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom4" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom5" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom6" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom7" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom8" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom9" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom10" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom11" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom12" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom13" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom14" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom15" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom16" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom17" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom18" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom19" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom20" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom21" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom22" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom23" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom24" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom25" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom26" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom27" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom28" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom29" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom30" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PurchaseOrder" type="string" required=false %}

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

> 🔒 Requires user role `coworker-create`

```javascript
{
    "CoworkerType": 1 (check Enumerated values section below),
    "Businesses": [12345678, 87654321] (replaces entire list),
    "AddedBusinesses": [12345678, 87654321] (adds to list),
    "RemovedBusinesses": [12345678, 87654321] (removes from list),
    "Teams": [12345678, 87654321] (replaces entire list),
    "AddedTeams": [12345678, 87654321] (adds to list),
    "RemovedTeams": [12345678, 87654321] (removes from list),
    "FullName": "Name",
    "Salutation": "Name",
    "Gender": 1 (check Enumerated values section below),
    "Email": "email@email.com",
    "CreateUser": true,
    "Address": "Address",
    "PostCode": "PostCode",
    "CityName": "CityName",
    "State": "State",
    "Country": 12345678,
    "SimpleTimeZone": 12345678,
    "MobilePhone": "MobilePhone",
    "LandLine": "LandLine",
    "DateOfBirth": null,
    "NickName": "NickName",
    "BusinessArea": "BusinessArea",
    "Position": "Position",
    "CompanyName": "CompanyName",
    "ProfileWebsite": "ProfileWebsite",
    "ProfileTags": "BusinessArea",
    "ProfileSummary": "BusinessArea",
    "Twitter": "Twitter",
    "Facebook": "Facebook",
    "Google": "Google",
    "Telegram": "Telegram",
    "Linkedin": "Linkedin",
    "Skype": "Skype",
    "Github": "Github",
    "Pinterest": "Pinterest",
    "Flickr": "Flickr",
    "Instagram": "Instagram",
    "Vimeo": "Vimeo",
    "Tumblr": "Tumblr",
    "Blogger": "Blogger",
    "ProfileIsPublic": true,
    "InvoicingBusiness": 12345678,
    "BillingEmail": "Address",
    "BillingName": "Address",
    "BillingAddress": "Address",
    "BillingPostCode": "PostCode",
    "BillingCityName": "CityName",
    "BillingState": "State",
    "BillingCountry": 12345678,
    "BillingSimpleTimeZone": 12345678,
    "TaxRate": 0,
    "TaxIDNumber": "State",
    "BankName": "Bank Name",
    "BankAccount": "Bank Account #",
    "BankBranch": "Branch / Sort Code",
    "NotifyOnNewInvoice": true,
    "NotifyOnNewPayment": true,
    "NotifyOnFailedPayment": true,
    "ShowPayingMemberInvoices": true,
    "EnableGoCardlessPayments": false,
    "GoCardlessContractNumber": "false",
    "RegularPaymentProvider": 1 (check Enumerated values section below),
    "RegularPaymentContractNumber": "false",
    "DoNotProcessInvoicesAutomatically": false,
    "AllowNetworkCheckin": false,
    "AccessCardId": "Notes",
    "AccessPincode": "Notes",
    "KeyFobNumber": "Notes",
    "NotifyOnDelivery": null,
    "EzeepUserId": null,
    "EzeepFreePrinting": null,
    "PaperCutPayAsYouPrint": false,
    "PaperCutFreePrinting": null,
    "CanMakeBookings": false,
    "CanPurchaseProducts": false,
    "CanPurchaseEvents": false,
    "CanAccessCommunity": false,
    "ReferenceNumber": "ReferenceNumber",
    "Tag": "Tag",
    "Notes": "Notes",
    "ShowAlert": false,
    "AlertNote": "Tag",
    "Active": true,
    "InvoiceDueDatePeriod": null,
    "RegistrationDate": null,
    "GeneralTermsAccepted": true,
    "Custom1": "Custom1",
    "Custom2": "Custom1",
    "Custom3": "Custom1",
    "Custom4": "Custom1",
    "Custom5": "Custom1",
    "Custom6": "Custom1",
    "Custom7": "Custom1",
    "Custom8": "Custom1",
    "Custom9": "Custom1",
    "Custom10": "Custom1",
    "Custom11": "Custom1",
    "Custom12": "Custom1",
    "Custom13": "Custom1",
    "Custom14": "Custom1",
    "Custom15": "Custom1",
    "Custom16": "Custom1",
    "Custom17": "Custom1",
    "Custom18": "Custom1",
    "Custom19": "Custom1",
    "Custom20": "Custom1",
    "Custom21": "Custom1",
    "Custom22": "Custom1",
    "Custom23": "Custom1",
    "Custom24": "Custom1",
    "Custom25": "Custom1",
    "Custom26": "Custom1",
    "Custom27": "Custom1",
    "Custom28": "Custom1",
    "Custom29": "Custom1",
    "Custom30": "Custom1",
    "PurchaseOrder": "false",
}
```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/spaces/coworkers" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing coworker.Required User Role: `coworker-edit`
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
{% api-method-parameter name="CoworkerType" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Businesses" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AddedBusinesses" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RemovedBusinesses" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Teams" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AddedTeams" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RemovedTeams" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FullName" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Salutation" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Gender" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Email" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Address" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PostCode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CityName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="State" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CountryId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="SimpleTimeZoneId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="MobilePhone" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LandLine" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DateOfBirth" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NickName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BusinessArea" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Position" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CompanyName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ProfileWebsite" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ProfileTags" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ProfileSummary" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Twitter" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Facebook" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Google" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Telegram" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Linkedin" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Skype" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Github" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Pinterest" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Flickr" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Instagram" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Vimeo" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Tumblr" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Blogger" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ProfileIsPublic" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="InvoicingBusinessId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingEmail" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingAddress" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingPostCode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingCityName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingState" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingCountryId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BillingSimpleTimeZoneId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TaxRate" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TaxIDNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BankName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BankAccount" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BankBranch" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnNewInvoice" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnNewPayment" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnFailedPayment" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ShowPayingMemberInvoices" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="EnableGoCardlessPayments" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="GoCardlessContractNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RegularPaymentProvider" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RegularPaymentContractNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DoNotProcessInvoicesAutomatically" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AllowNetworkCheckin" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AccessCardId" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AccessPincode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="KeyFobNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NotifyOnDelivery" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="EzeepUserId" type="Guid?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="EzeepFreePrinting" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PaperCutPayAsYouPrint" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PaperCutFreePrinting" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CanMakeBookings" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CanPurchaseProducts" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CanPurchaseEvents" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CanAccessCommunity" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ReferenceNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Tag" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ShowAlert" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AlertNote" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="UserId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Active" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NextAutoInvoice" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceDueDatePeriod" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RegistrationDate" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="GeneralTermsAccepted" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom1" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom2" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom3" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom4" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom5" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom6" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom7" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom8" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom9" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom10" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom11" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom12" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom13" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom14" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom15" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom16" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom17" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom18" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom19" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom20" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom21" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom22" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom23" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom24" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom25" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom26" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom27" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom28" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom29" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Custom30" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PurchaseOrder" type="string" required=false %}

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

> 🔒 Requires user role `coworker-edit`

```javascript
{
    "CoworkerType": 1 (check Enumerated values section below),
    "Businesses": [12345678, 87654321] (replaces entire list),
    "AddedBusinesses": [12345678, 87654321] (adds to list),
    "RemovedBusinesses": [12345678, 87654321] (removes from list),
    "Teams": [12345678, 87654321] (replaces entire list),
    "AddedTeams": [12345678, 87654321] (adds to list),
    "RemovedTeams": [12345678, 87654321] (removes from list),
    "FullName": "Name",
    "Salutation": "Name",
    "Gender": 1 (check Enumerated values section below),
    "Email": "email@email.com",
    "Address": "Address",
    "PostCode": "PostCode",
    "CityName": "CityName",
    "State": "State",
    "Country": 12345678,
    "SimpleTimeZone": 12345678,
    "MobilePhone": "MobilePhone",
    "LandLine": "LandLine",
    "DateOfBirth": null,
    "NickName": "NickName",
    "BusinessArea": "BusinessArea",
    "Position": "Position",
    "CompanyName": "CompanyName",
    "ProfileWebsite": "ProfileWebsite",
    "ProfileTags": "BusinessArea",
    "ProfileSummary": "BusinessArea",
    "Twitter": "Twitter",
    "Facebook": "Facebook",
    "Google": "Google",
    "Telegram": "Telegram",
    "Linkedin": "Linkedin",
    "Skype": "Skype",
    "Github": "Github",
    "Pinterest": "Pinterest",
    "Flickr": "Flickr",
    "Instagram": "Instagram",
    "Vimeo": "Vimeo",
    "Tumblr": "Tumblr",
    "Blogger": "Blogger",
    "ProfileIsPublic": true,
    "InvoicingBusiness": 12345678,
    "BillingEmail": "Address",
    "BillingName": "Address",
    "BillingAddress": "Address",
    "BillingPostCode": "PostCode",
    "BillingCityName": "CityName",
    "BillingState": "State",
    "BillingCountry": 12345678,
    "BillingSimpleTimeZone": 12345678,
    "TaxRate": 0,
    "TaxIDNumber": "State",
    "BankName": "Bank Name",
    "BankAccount": "Bank Account #",
    "BankBranch": "Branch / Sort Code",
    "NotifyOnNewInvoice": true,
    "NotifyOnNewPayment": true,
    "NotifyOnFailedPayment": true,
    "ShowPayingMemberInvoices": true,
    "EnableGoCardlessPayments": false,
    "GoCardlessContractNumber": "false",
    "RegularPaymentProvider": 1 (check Enumerated values section below),
    "RegularPaymentContractNumber": "false",
    "DoNotProcessInvoicesAutomatically": false,
    "AllowNetworkCheckin": false,
    "AccessCardId": "Notes",
    "AccessPincode": "Notes",
    "KeyFobNumber": "Notes",
    "NotifyOnDelivery": null,
    "EzeepUserId": null,
    "EzeepFreePrinting": null,
    "PaperCutPayAsYouPrint": false,
    "PaperCutFreePrinting": null,
    "CanMakeBookings": false,
    "CanPurchaseProducts": false,
    "CanPurchaseEvents": false,
    "CanAccessCommunity": false,
    "ReferenceNumber": "ReferenceNumber",
    "Tag": "Tag",
    "Notes": "Notes",
    "ShowAlert": false,
    "AlertNote": "Tag",
    "User": 12345678,
    "Active": true,
    "NextAutoInvoice": null,
    "InvoiceDueDatePeriod": null,
    "RegistrationDate": null,
    "GeneralTermsAccepted": true,
    "Custom1": "Custom1",
    "Custom2": "Custom1",
    "Custom3": "Custom1",
    "Custom4": "Custom1",
    "Custom5": "Custom1",
    "Custom6": "Custom1",
    "Custom7": "Custom1",
    "Custom8": "Custom1",
    "Custom9": "Custom1",
    "Custom10": "Custom1",
    "Custom11": "Custom1",
    "Custom12": "Custom1",
    "Custom13": "Custom1",
    "Custom14": "Custom1",
    "Custom15": "Custom1",
    "Custom16": "Custom1",
    "Custom17": "Custom1",
    "Custom18": "Custom1",
    "Custom19": "Custom1",
    "Custom20": "Custom1",
    "Custom21": "Custom1",
    "Custom22": "Custom1",
    "Custom23": "Custom1",
    "Custom24": "Custom1",
    "Custom25": "Custom1",
    "Custom26": "Custom1",
    "Custom27": "Custom1",
    "Custom28": "Custom1",
    "Custom29": "Custom1",
    "Custom30": "Custom1",
    "PurchaseOrder": "false",
}
```

## Commands

Commands allow to perform actions against one or more coworker records. Some commands accept only one record while others can run an action for a number of records at the same time. Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

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
Get all commands available to run for coworker records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers/runcommand" %}
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
A list of object with the structure below. The parameters required for each command are returned in the "RequiresParameters" array return by the "commands" endpoint.`[ { "Name": "Name", "Type":"Type", "Value":recordId } ]`
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

> 🔒 Requires user role `coworker-edit`

## Enumerated values

### CoworkerType:

> GET /api/utils/enums?name=eCoworkerRecordType

### Gender:

> GET /api/utils/enums?name=eGender

### RegularPaymentProvider:

> GET /api/utils/enums?name=eRegularPaymentProvider

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

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
The id of the Coworker to get the avatar for.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers/getbannerimage/:id" %}
{% api-method-summary %}
BannerImage
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Coworker to get the bannerimage for.
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

* [Country](https://github.com/Nexudus/api-docs/tree/6c08c63d9c0c6779737ccfddc96f70c6623677d0/rest-api/sys/country.md)
* [SimpleTimeZone](../sys/simpletimezone.md)
* [Business](../sys/business.md)
* [Country](https://github.com/Nexudus/api-docs/tree/6c08c63d9c0c6779737ccfddc96f70c6623677d0/rest-api/sys/country.md)
* [SimpleTimeZone](../sys/simpletimezone.md)
* [User](../sys/user.md)

