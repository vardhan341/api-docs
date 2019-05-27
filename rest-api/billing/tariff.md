{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/tariffs" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of tariffs based on one or more filter querystring parameters.
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
?Tariff\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?Tariff\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="Name" type="string" %}
?Tariff\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="Price" type="decimal" %}
?Tariff\_Price=...
{% endapi-method-parameter %}


{% api-method-parameter name="DefaultInvoicingDay" type="int?" %}
?Tariff\_DefaultInvoicingDay=...
{% endapi-method-parameter %}


{% api-method-parameter name="Visible" type="bool" %}
?Tariff\_Visible=...
{% endapi-method-parameter %}


{% api-method-parameter name="UseTimePasses" type="bool" %}
?Tariff\_UseTimePasses=...
{% endapi-method-parameter %}


{% api-method-parameter name="Description" type="string" %}
?Tariff\_Description=...
{% endapi-method-parameter %}


{% api-method-parameter name="SignUpFee" type="decimal?" %}
?Tariff\_SignUpFee=...
{% endapi-method-parameter %}


{% api-method-parameter name="Currency" type="Currency" %}
?Tariff\_Currency=...
{% endapi-method-parameter %}


{% api-method-parameter name="TaxRate" type="TaxRate" %}
?Tariff\_TaxRate=...
{% endapi-method-parameter %}


{% api-method-parameter name="FinancialAccount" type="FinancialAccount" %}
?Tariff\_FinancialAccount=...
{% endapi-method-parameter %}


{% api-method-parameter name="TermsAndConditions" type="string" %}
?Tariff\_TermsAndConditions=...
{% endapi-method-parameter %}


{% api-method-parameter name="CancellationPeriod" type="int" %}
?Tariff\_CancellationPeriod=...
{% endapi-method-parameter %}


{% api-method-parameter name="DisplayOrder" type="int" %}
?Tariff\_DisplayOrder=...
{% endapi-method-parameter %}


{% api-method-parameter name="GroupName" type="string" %}
?Tariff\_GroupName=...
{% endapi-method-parameter %}


{% api-method-parameter name="SubscribersLimit" type="int?" %}
?Tariff\_SubscribersLimit=...
{% endapi-method-parameter %}


{% api-method-parameter name="CancellationLimitDays" type="int?" %}
?Tariff\_CancellationLimitDays=...
{% endapi-method-parameter %}


{% api-method-parameter name="DefaultContractTerm" type="int?" %}
?Tariff\_DefaultContractTerm=...
{% endapi-method-parameter %}


{% api-method-parameter name="CancelMemeberAccountAfter" type="int?" %}
?Tariff\_CancelMemeberAccountAfter=...
{% endapi-method-parameter %}


{% api-method-parameter name="CheckinPricePlanLimit" type="int?" %}
?Tariff\_CheckinPricePlanLimit=...
{% endapi-method-parameter %}


{% api-method-parameter name="CheckinMonthLimit" type="int?" %}
?Tariff\_CheckinMonthLimit=...
{% endapi-method-parameter %}


{% api-method-parameter name="CheckinWeekLimit" type="int?" %}
?Tariff\_CheckinWeekLimit=...
{% endapi-method-parameter %}


{% api-method-parameter name="HoursPricePlanLimit" type="int?" %}
?Tariff\_HoursPricePlanLimit=...
{% endapi-method-parameter %}


{% api-method-parameter name="HoursMonthLimit" type="int?" %}
?Tariff\_HoursMonthLimit=...
{% endapi-method-parameter %}


{% api-method-parameter name="HoursWeekLimit" type="int?" %}
?Tariff\_HoursWeekLimit=...
{% endapi-method-parameter %}


{% api-method-parameter name="BookingMinuteWeekLimit" type="int?" %}
?Tariff\_BookingMinuteWeekLimit=...
{% endapi-method-parameter %}


{% api-method-parameter name="BookingMinuteMonthLimit" type="int?" %}
?Tariff\_BookingMinuteMonthLimit=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountExtraServices" type="decimal?" %}
?Tariff\_DiscountExtraServices=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountTimePasses" type="decimal?" %}
?Tariff\_DiscountTimePasses=...
{% endapi-method-parameter %}


{% api-method-parameter name="DiscountCharges" type="decimal?" %}
?Tariff\_DiscountCharges=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceEvery" type="int" %}
?Tariff\_InvoiceEvery=...
{% endapi-method-parameter %}


{% api-method-parameter name="InvoiceEveryWeeks" type="int" %}
?Tariff\_InvoiceEveryWeeks=...
{% endapi-method-parameter %}


{% api-method-parameter name="AutoCancelAfter" type="int?" %}
?Tariff\_AutoCancelAfter=...
{% endapi-method-parameter %}


{% api-method-parameter name="AdvanceInvoiceCycles" type="int?" %}
?Tariff\_AdvanceInvoiceCycles=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProrateDayOfMonth" type="int?" %}
?Tariff\_ProrateDayOfMonth=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProrateDaysBefore" type="int?" %}
?Tariff\_ProrateDaysBefore=...
{% endapi-method-parameter %}


{% api-method-parameter name="ProrateCancellations" type="bool" %}
?Tariff\_ProrateCancellations=...
{% endapi-method-parameter %}


{% api-method-parameter name="ChargeAndExtend" type="int?" %}
?Tariff\_ChargeAndExtend=...
{% endapi-method-parameter %}


{% api-method-parameter name="AutoRaiseInvoices" type="bool" %}
?Tariff\_AutoRaiseInvoices=...
{% endapi-method-parameter %}


{% api-method-parameter name="RaiseInvoiceEvery" type="int?" %}
?Tariff\_RaiseInvoiceEvery=...
{% endapi-method-parameter %}


{% api-method-parameter name="RaiseInvoiceEveryWeeks" type="int?" %}
?Tariff\_RaiseInvoiceEveryWeeks=...
{% endapi-method-parameter %}


{% api-method-parameter name="Archived" type="bool" %}
?Tariff\_Archived=...
{% endapi-method-parameter %}


{% api-method-parameter name="Starred" type="bool" %}
?Tariff\_Starred=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business\_Name" type="string" %}
?Tariff\_Business\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="Currency\_Code" type="string" %}
?Tariff\_Currency\_Code=...
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
        "Price": 0,
        "DefaultInvoicingDay": ,
        "Visible": true,
        "UseTimePasses": true,
        "Description": "Descripción",
        "SignUpFee": 0,
        "Currency": null,
        "TaxRate": null,
        "FinancialAccount": null,
        "TermsAndConditions": "TermsAndConditions",
        "CancellationPeriod": 0,
        "DisplayOrder": true,
        "GroupName": "GroupName",
        "SubscribersLimit": null,
        "CancellationLimitDays": null,
        "DefaultContractTerm": null,
        "CancelMemeberAccountAfter": null,
        "CheckinPricePlanLimit": null,
        "CheckinMonthLimit": null,
        "CheckinWeekLimit": null,
        "HoursPricePlanLimit": null,
        "HoursMonthLimit": null,
        "HoursWeekLimit": null,
        "BookingMinuteWeekLimit": null,
        "BookingMinuteMonthLimit": null,
        "DiscountExtraServices": null,
        "DiscountTimePasses": null,
        "DiscountCharges": null,
        "InvoiceEvery": 1,
        "InvoiceEveryWeeks": 0,
        "AutoCancelAfter": Cancel Contract After # renewals,
        "AdvanceInvoiceCycles": Invoice # renewals in Advance,
        "ProrateDayOfMonth": 0,
        "ProrateDaysBefore": 0,
        "ProrateCancellations": true,
        "ChargeAndExtend": 0,
        "AutoRaiseInvoices": false,
        "RaiseInvoiceEvery": 0,
        "RaiseInvoiceEveryWeeks": 0,
        "Archived": true,
        "Starred": true,
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

> 🔒 Requires user role `tariff-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/tariffs" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of tariffs.
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
        "Price": 0,
        "DefaultInvoicingDay": ,
        "Visible": true,
        "UseTimePasses": true,
        "Description": "Descripción",
        "SignUpFee": 0,
        "Currency": null,
        "TaxRate": null,
        "FinancialAccount": null,
        "TermsAndConditions": "TermsAndConditions",
        "CancellationPeriod": 0,
        "DisplayOrder": true,
        "GroupName": "GroupName",
        "SubscribersLimit": null,
        "CancellationLimitDays": null,
        "DefaultContractTerm": null,
        "CancelMemeberAccountAfter": null,
        "CheckinPricePlanLimit": null,
        "CheckinMonthLimit": null,
        "CheckinWeekLimit": null,
        "HoursPricePlanLimit": null,
        "HoursMonthLimit": null,
        "HoursWeekLimit": null,
        "BookingMinuteWeekLimit": null,
        "BookingMinuteMonthLimit": null,
        "DiscountExtraServices": null,
        "DiscountTimePasses": null,
        "DiscountCharges": null,
        "InvoiceEvery": 1,
        "InvoiceEveryWeeks": 0,
        "AutoCancelAfter": Cancel Contract After # renewals,
        "AdvanceInvoiceCycles": Invoice # renewals in Advance,
        "ProrateDayOfMonth": 0,
        "ProrateDaysBefore": 0,
        "ProrateCancellations": true,
        "ChargeAndExtend": 0,
        "AutoRaiseInvoices": false,
        "RaiseInvoiceEvery": 0,
        "RaiseInvoiceEveryWeeks": 0,
        "Archived": true,
        "Starred": true,
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

> 🔒 Requires user role `tariff-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/tariffs" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of tariffs based on the date when they were created or updated.
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
?to\_Tariff\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_Tariff\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_Tariff\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_Tariff\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="Price" type="decimal" required=false %}
?from\_Tariff\_Price=...
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal" required=false %}
?to\_Tariff\_Price=...
{% endapi-method-parameter %}
{% api-method-parameter name="DefaultInvoicingDay" type="int" required=false %}
?from\_Tariff\_DefaultInvoicingDay=...
{% endapi-method-parameter %}
{% api-method-parameter name="DefaultInvoicingDay" type="int" required=false %}
?to\_Tariff\_DefaultInvoicingDay=...
{% endapi-method-parameter %}
{% api-method-parameter name="SignUpFee" type="decimal" required=false %}
?from\_Tariff\_SignUpFee=...
{% endapi-method-parameter %}
{% api-method-parameter name="SignUpFee" type="decimal" required=false %}
?to\_Tariff\_SignUpFee=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationPeriod" type="int" required=false %}
?from\_Tariff\_CancellationPeriod=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationPeriod" type="int" required=false %}
?to\_Tariff\_CancellationPeriod=...
{% endapi-method-parameter %}
{% api-method-parameter name="DisplayOrder" type="int" required=false %}
?from\_Tariff\_DisplayOrder=...
{% endapi-method-parameter %}
{% api-method-parameter name="DisplayOrder" type="int" required=false %}
?to\_Tariff\_DisplayOrder=...
{% endapi-method-parameter %}
{% api-method-parameter name="SubscribersLimit" type="int" required=false %}
?from\_Tariff\_SubscribersLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="SubscribersLimit" type="int" required=false %}
?to\_Tariff\_SubscribersLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int" required=false %}
?from\_Tariff\_CancellationLimitDays=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int" required=false %}
?to\_Tariff\_CancellationLimitDays=...
{% endapi-method-parameter %}
{% api-method-parameter name="DefaultContractTerm" type="int" required=false %}
?from\_Tariff\_DefaultContractTerm=...
{% endapi-method-parameter %}
{% api-method-parameter name="DefaultContractTerm" type="int" required=false %}
?to\_Tariff\_DefaultContractTerm=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancelMemeberAccountAfter" type="int" required=false %}
?from\_Tariff\_CancelMemeberAccountAfter=...
{% endapi-method-parameter %}
{% api-method-parameter name="CancelMemeberAccountAfter" type="int" required=false %}
?to\_Tariff\_CancelMemeberAccountAfter=...
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinPricePlanLimit" type="int" required=false %}
?from\_Tariff\_CheckinPricePlanLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinPricePlanLimit" type="int" required=false %}
?to\_Tariff\_CheckinPricePlanLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinMonthLimit" type="int" required=false %}
?from\_Tariff\_CheckinMonthLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinMonthLimit" type="int" required=false %}
?to\_Tariff\_CheckinMonthLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinWeekLimit" type="int" required=false %}
?from\_Tariff\_CheckinWeekLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinWeekLimit" type="int" required=false %}
?to\_Tariff\_CheckinWeekLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="HoursPricePlanLimit" type="int" required=false %}
?from\_Tariff\_HoursPricePlanLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="HoursPricePlanLimit" type="int" required=false %}
?to\_Tariff\_HoursPricePlanLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="HoursMonthLimit" type="int" required=false %}
?from\_Tariff\_HoursMonthLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="HoursMonthLimit" type="int" required=false %}
?to\_Tariff\_HoursMonthLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="HoursWeekLimit" type="int" required=false %}
?from\_Tariff\_HoursWeekLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="HoursWeekLimit" type="int" required=false %}
?to\_Tariff\_HoursWeekLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="BookingMinuteWeekLimit" type="int" required=false %}
?from\_Tariff\_BookingMinuteWeekLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="BookingMinuteWeekLimit" type="int" required=false %}
?to\_Tariff\_BookingMinuteWeekLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="BookingMinuteMonthLimit" type="int" required=false %}
?from\_Tariff\_BookingMinuteMonthLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="BookingMinuteMonthLimit" type="int" required=false %}
?to\_Tariff\_BookingMinuteMonthLimit=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountExtraServices" type="decimal" required=false %}
?from\_Tariff\_DiscountExtraServices=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountExtraServices" type="decimal" required=false %}
?to\_Tariff\_DiscountExtraServices=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTimePasses" type="decimal" required=false %}
?from\_Tariff\_DiscountTimePasses=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTimePasses" type="decimal" required=false %}
?to\_Tariff\_DiscountTimePasses=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountCharges" type="decimal" required=false %}
?from\_Tariff\_DiscountCharges=...
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountCharges" type="decimal" required=false %}
?to\_Tariff\_DiscountCharges=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceEvery" type="int" required=false %}
?from\_Tariff\_InvoiceEvery=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceEvery" type="int" required=false %}
?to\_Tariff\_InvoiceEvery=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceEveryWeeks" type="int" required=false %}
?from\_Tariff\_InvoiceEveryWeeks=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceEveryWeeks" type="int" required=false %}
?to\_Tariff\_InvoiceEveryWeeks=...
{% endapi-method-parameter %}
{% api-method-parameter name="AutoCancelAfter" type="int" required=false %}
?from\_Tariff\_AutoCancelAfter=...
{% endapi-method-parameter %}
{% api-method-parameter name="AutoCancelAfter" type="int" required=false %}
?to\_Tariff\_AutoCancelAfter=...
{% endapi-method-parameter %}
{% api-method-parameter name="AdvanceInvoiceCycles" type="int" required=false %}
?from\_Tariff\_AdvanceInvoiceCycles=...
{% endapi-method-parameter %}
{% api-method-parameter name="AdvanceInvoiceCycles" type="int" required=false %}
?to\_Tariff\_AdvanceInvoiceCycles=...
{% endapi-method-parameter %}
{% api-method-parameter name="ProrateDayOfMonth" type="int" required=false %}
?from\_Tariff\_ProrateDayOfMonth=...
{% endapi-method-parameter %}
{% api-method-parameter name="ProrateDayOfMonth" type="int" required=false %}
?to\_Tariff\_ProrateDayOfMonth=...
{% endapi-method-parameter %}
{% api-method-parameter name="ProrateDaysBefore" type="int" required=false %}
?from\_Tariff\_ProrateDaysBefore=...
{% endapi-method-parameter %}
{% api-method-parameter name="ProrateDaysBefore" type="int" required=false %}
?to\_Tariff\_ProrateDaysBefore=...
{% endapi-method-parameter %}
{% api-method-parameter name="ChargeAndExtend" type="int" required=false %}
?from\_Tariff\_ChargeAndExtend=...
{% endapi-method-parameter %}
{% api-method-parameter name="ChargeAndExtend" type="int" required=false %}
?to\_Tariff\_ChargeAndExtend=...
{% endapi-method-parameter %}
{% api-method-parameter name="RaiseInvoiceEvery" type="int" required=false %}
?from\_Tariff\_RaiseInvoiceEvery=...
{% endapi-method-parameter %}
{% api-method-parameter name="RaiseInvoiceEvery" type="int" required=false %}
?to\_Tariff\_RaiseInvoiceEvery=...
{% endapi-method-parameter %}
{% api-method-parameter name="RaiseInvoiceEveryWeeks" type="int" required=false %}
?from\_Tariff\_RaiseInvoiceEveryWeeks=...
{% endapi-method-parameter %}
{% api-method-parameter name="RaiseInvoiceEveryWeeks" type="int" required=false %}
?to\_Tariff\_RaiseInvoiceEveryWeeks=...
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
        "Price": 0,
        "DefaultInvoicingDay": ,
        "Visible": true,
        "UseTimePasses": true,
        "Description": "Descripción",
        "SignUpFee": 0,
        "Currency": null,
        "TaxRate": null,
        "FinancialAccount": null,
        "TermsAndConditions": "TermsAndConditions",
        "CancellationPeriod": 0,
        "DisplayOrder": true,
        "GroupName": "GroupName",
        "SubscribersLimit": null,
        "CancellationLimitDays": null,
        "DefaultContractTerm": null,
        "CancelMemeberAccountAfter": null,
        "CheckinPricePlanLimit": null,
        "CheckinMonthLimit": null,
        "CheckinWeekLimit": null,
        "HoursPricePlanLimit": null,
        "HoursMonthLimit": null,
        "HoursWeekLimit": null,
        "BookingMinuteWeekLimit": null,
        "BookingMinuteMonthLimit": null,
        "DiscountExtraServices": null,
        "DiscountTimePasses": null,
        "DiscountCharges": null,
        "InvoiceEvery": 1,
        "InvoiceEveryWeeks": 0,
        "AutoCancelAfter": Cancel Contract After # renewals,
        "AdvanceInvoiceCycles": Invoice # renewals in Advance,
        "ProrateDayOfMonth": 0,
        "ProrateDaysBefore": 0,
        "ProrateCancellations": true,
        "ChargeAndExtend": 0,
        "AutoRaiseInvoices": false,
        "RaiseInvoiceEvery": 0,
        "RaiseInvoiceEveryWeeks": 0,
        "Archived": true,
        "Starred": true,
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

> 🔒 Requires user role `tariff-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/tariffs/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one tariff record.
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
The ID of the tariff to fetch.
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
        "Price": 0,
        "DefaultInvoicingDay": ,
        "Visible": true,
        "UseTimePasses": true,
        "Description": "Descripción",
        "SignUpFee": 0,
        "Currency": null,
        "TaxRate": null,
        "FinancialAccount": null,
        "TermsAndConditions": "TermsAndConditions",
        "CancellationPeriod": 0,
        "DisplayOrder": true,
        "GroupName": "GroupName",
        "SubscribersLimit": null,
        "CancellationLimitDays": null,
        "DefaultContractTerm": null,
        "CancelMemeberAccountAfter": null,
        "CheckinPricePlanLimit": null,
        "CheckinMonthLimit": null,
        "CheckinWeekLimit": null,
        "HoursPricePlanLimit": null,
        "HoursMonthLimit": null,
        "HoursWeekLimit": null,
        "BookingMinuteWeekLimit": null,
        "BookingMinuteMonthLimit": null,
        "DiscountExtraServices": null,
        "DiscountTimePasses": null,
        "DiscountCharges": null,
        "InvoiceEvery": 1,
        "InvoiceEveryWeeks": 0,
        "AutoCancelAfter": Cancel Contract After # renewals,
        "AdvanceInvoiceCycles": Invoice # renewals in Advance,
        "ProrateDayOfMonth": 0,
        "ProrateDaysBefore": 0,
        "ProrateCancellations": true,
        "ChargeAndExtend": 0,
        "AutoRaiseInvoices": false,
        "RaiseInvoiceEvery": 0,
        "RaiseInvoiceEveryWeeks": 0,
        "Archived": true,
        "Starred": true,
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

> 🔒 Requires user role `tariff-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/billing/tariffs" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new tariff.
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
{% api-method-parameter name="Price" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="DefaultInvoicingDay" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Visible" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="UseTimePasses" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Description" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="SignUpFee" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CurrencyId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaxRateId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FinancialAccountId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TermsAndConditions" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationPeriod" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="DisplayOrder" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="GroupName" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="SubscribersLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DefaultContractTerm" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancelMemeberAccountAfter" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinPricePlanLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinMonthLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinWeekLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="HoursPricePlanLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="HoursMonthLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="HoursWeekLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingMinuteWeekLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingMinuteMonthLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountExtraServices" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTimePasses" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountCharges" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceEvery" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceEveryWeeks" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoCancelAfter" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AdvanceInvoiceCycles" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProrateDayOfMonth" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProrateDaysBefore" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProrateCancellations" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ChargeAndExtend" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoRaiseInvoices" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RaiseInvoiceEvery" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RaiseInvoiceEveryWeeks" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Archived" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Starred" type="bool" required=false %}
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

> 🔒 Requires user role `tariff-create`

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/billing/tariffs" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing tariff.
  
Required User Role: `tariff-edit`
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
{% api-method-parameter name="Id" type="integer" required=true %}
The id of the tariff to update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="BusinessId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Price" type="decimal" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="DefaultInvoicingDay" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Visible" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="UseTimePasses" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Description" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="SignUpFee" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CurrencyId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="TaxRateId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FinancialAccountId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TermsAndConditions" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationPeriod" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="DisplayOrder" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="GroupName" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="SubscribersLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancellationLimitDays" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DefaultContractTerm" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CancelMemeberAccountAfter" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinPricePlanLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinMonthLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CheckinWeekLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="HoursPricePlanLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="HoursMonthLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="HoursWeekLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingMinuteWeekLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="BookingMinuteMonthLimit" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountExtraServices" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountTimePasses" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="DiscountCharges" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceEvery" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceEveryWeeks" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoCancelAfter" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AdvanceInvoiceCycles" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProrateDayOfMonth" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProrateDaysBefore" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ProrateCancellations" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ChargeAndExtend" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AutoRaiseInvoices" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RaiseInvoiceEvery" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RaiseInvoiceEveryWeeks" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Archived" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Starred" type="bool" required=false %}
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

> 🔒 Requires user role `tariff-edit`


{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/billing/tariffs/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a tariff.  
  
Required User Roles: `tariff-delete`
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



> 🔒 Requires user role `tariff-delete`


## Commands

Commands allow to perform actions against one or more tariff records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/tariffs/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for tariff records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/tariffs/runcommand" %}
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

> 🔒 Requires user role `tariff-edit`

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/billing/tariffs/getcontractdocument/:id" %}
{% api-method-summary %}
ContractDocument
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
The id of the Tariff to get the contractdocument for.
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
* [Currency](../sys/currency.md)
* [TaxRate](../sys/taxrate.md)
* [FinancialAccount](../billing/financialaccount.md)
