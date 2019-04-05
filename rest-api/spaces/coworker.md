
# Coworkers

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers" %}
{% api-method-summary %}
GET Coworkers
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
{% endapi-method-headers %}

{% api-method-query-parameters %}

{% api-method-parameter name="CoworkerType" type="integer" %}
?Coworker_CoworkerType=...
{% endapi-method-parameter %}
{% api-method-parameter name="FullName" type="string" %}
?Coworker_FullName=...
{% endapi-method-parameter %}
{% api-method-parameter name="Salutation" type="string" %}
?Coworker_Salutation=...
{% endapi-method-parameter %}
{% api-method-parameter name="Gender" type="integer" %}
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
{% api-method-parameter name="Country" type="int" %}
?Coworker_Country=...
{% endapi-method-parameter %}
{% api-method-parameter name="SimpleTimeZone" type="int" %}
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
{% api-method-parameter name="InvoicingBusiness" type="int" %}
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
{% api-method-parameter name="BillingCountry" type="int" %}
?Coworker_BillingCountry=...
{% endapi-method-parameter %}
{% api-method-parameter name="BillingSimpleTimeZone" type="int" %}
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
{% api-method-parameter name="UseGoCardlessProPayments" type="bool" %}
?Coworker_UseGoCardlessProPayments=...
{% endapi-method-parameter %}
{% api-method-parameter name="GoCardlessContractNumber" type="string" %}
?Coworker_GoCardlessContractNumber=...
{% endapi-method-parameter %}
{% api-method-parameter name="LastOverDueInvoiceReminder" type="DateTime?" %}
?Coworker_LastOverDueInvoiceReminder=...
{% endapi-method-parameter %}
{% api-method-parameter name="LastLowCreditReminder" type="DateTime?" %}
?Coworker_LastLowCreditReminder=...
{% endapi-method-parameter %}
{% api-method-parameter name="RefererGuid" type="Guid?" %}
?Coworker_RefererGuid=...
{% endapi-method-parameter %}
{% api-method-parameter name="RegularPaymentProvider" type="integer" %}
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
{% api-method-parameter name="ReferenceNumber" type="string" %}
?Coworker_ReferenceNumber=...
{% endapi-method-parameter %}
{% api-method-parameter name="Tag" type="string" %}
?Coworker_Tag=...
{% endapi-method-parameter %}
{% api-method-parameter name="Notes" type="string" %}
?Coworker_Notes=...
{% endapi-method-parameter %}
{% api-method-parameter name="ShowAlert" type="bool" %}
?Coworker_ShowAlert=...
{% endapi-method-parameter %}
{% api-method-parameter name="AlertNote" type="string" %}
?Coworker_AlertNote=...
{% endapi-method-parameter %}
{% api-method-parameter name="User" type="int" %}
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
{% api-method-parameter name="LastRenewal" type="DateTime?" %}
?Coworker_LastRenewal=...
{% endapi-method-parameter %}
{% api-method-parameter name="LastInvoiceAttempt" type="DateTime?" %}
?Coworker_LastInvoiceAttempt=...
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
{% api-method-parameter name="NextInvoiceLocal" type="DateTime?" %}
?Coworker_NextInvoiceLocal=...
{% endapi-method-parameter %}
{% api-method-parameter name="NextAutoInvoiceLocal" type="DateTime?" %}
?Coworker_NextAutoInvoiceLocal=...
{% endapi-method-parameter %}
{% api-method-parameter name="RegistrationDateLocal" type="DateTime?" %}
?Coworker_RegistrationDateLocal=...
{% endapi-method-parameter %}
{% api-method-parameter name="AccessControlDebounceTime" type="DateTime?" %}
?Coworker_AccessControlDebounceTime=...
{% endapi-method-parameter %}
{% api-method-parameter name="Office365AccessToken" type="string" %}
?Coworker_Office365AccessToken=...
{% endapi-method-parameter %}
{% api-method-parameter name="Office365RefreshToken" type="string" %}
?Coworker_Office365RefreshToken=...
{% endapi-method-parameter %}
{% api-method-parameter name="Office365SubscriptionId" type="string" %}
?Coworker_Office365SubscriptionId=...
{% endapi-method-parameter %}

{% endapi-method-query-parameters %}

{% api-method-parameter name="gluten" type="boolean" %}
Whether the cake should be gluten-free or not.
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
    "name": "Cake's name",
    "recipe": "Cake's recipe name",
    "cake": "Binary cake"
}
```

{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```

{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/coworkers" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
ID of the cake to get, for free of course.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="recipe" type="string" %}
The API will do its best to find a cake matching the provided recipe.
{% endapi-method-parameter %}

{% api-method-parameter name="gluten" type="boolean" %}
Whether the cake should be gluten-free or not.
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
    "name": "Cake's name",
    "recipe": "Cake's recipe name",
    "cake": "Binary cake"
}
```

{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```

{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


