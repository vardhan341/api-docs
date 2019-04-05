C

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
{% api-method-parameter name="Authentication" type="string" required=true %}
Basic Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}

{% api-method-parameter type="integer" %}
Coworker_CoworkerType
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_FullName" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Salutation" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Gender" type="integer" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Email" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_CreateUser" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Address" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_PostCode" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_CityName" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_State" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Country" type="int" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_SimpleTimeZone" type="int" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_MobilePhone" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_LandLine" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_DateOfBirth" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_NickName" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BusinessArea" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Position" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_CompanyName" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_ProfileWebsite" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_ProfileTags" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_ProfileSummary" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Twitter" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Facebook" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Google" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Telegram" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Linkedin" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Skype" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Github" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Pinterest" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Flickr" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Instagram" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Vimeo" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Tumblr" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Blogger" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_ProfileIsPublic" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_InvoicingBusiness" type="int" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BillingEmail" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BillingName" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BillingAddress" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BillingPostCode" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BillingCityName" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BillingState" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BillingCountry" type="int" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BillingSimpleTimeZone" type="int" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_TaxRate" type="decimal?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_TaxIDNumber" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BankName" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BankAccount" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_BankBranch" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_NotifyOnNewInvoice" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_NotifyOnNewPayment" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_NotifyOnFailedPayment" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_ShowPayingMemberInvoices" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_EnableGoCardlessPayments" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_UseGoCardlessProPayments" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_GoCardlessContractNumber" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_LastOverDueInvoiceReminder" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_LastLowCreditReminder" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_RefererGuid" type="Guid?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_RegularPaymentProvider" type="integer" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_RegularPaymentContractNumber" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_CardNumber" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_DoNotProcessInvoicesAutomatically" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_AllowNetworkCheckin" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_CheckinSinceLastRenewal" type="int" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_MinutesSinceLastRenewal" type="int" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_AccessCardId" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_AccessPincode" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_KeyFobNumber" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_NotifyOnDelivery" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_EzeepUserId" type="Guid?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_EzeepFreePrinting" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_PaperCutPayAsYouPrint" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_PaperCutFreePrinting" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_ReferenceNumber" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Tag" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Notes" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_ShowAlert" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_AlertNote" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_User" type="int" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Active" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_NextAutoInvoice" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_InvoiceDueDatePeriod" type="int?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_RegistrationDate" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_GeneralTermsAccepted" type="bool" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_LastRenewal" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_LastInvoiceAttempt" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom1" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom2" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom3" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom4" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom5" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom6" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom7" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom8" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom9" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom10" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom11" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom12" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom13" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom14" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom15" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom16" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom17" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom18" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom19" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom20" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom21" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom22" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom23" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom24" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom25" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom26" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom27" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom28" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom29" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Custom30" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_NextInvoiceLocal" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_NextAutoInvoiceLocal" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_RegistrationDateLocal" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_AccessControlDebounceTime" type="DateTime?" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Office365AccessToken" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Office365RefreshToken" type="string" %}
{% endapi-method-parameter %}
{% api-method-parameter name="Coworker_Office365SubscriptionId" type="string" %}
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
