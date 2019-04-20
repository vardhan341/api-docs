---
description: Returns the data available on the allowances page.
---

# Allowances

🔓 This page requires authentication.

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/allowances" %}
{% api-method-summary %}
Allowances page
{% endapi-method-summary %}

{% api-method-description %}
Gets the data representing the about us page
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="langugage" type="string" required=true %}
'en' or any other valid language in your account.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=false %}
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
    "TariffTimePasses": [],
    "TariffExtraServices": [],
    "TariffBookingCredits": [],
    "BookingCredit": [],
    "OtherTimePasses": [
        {
            "TimePass": {},
            "Remaining": 0,
            "RemainingUses": 600,
            "CreditObject": {},
            "CreditName": "All Day Pass",
            "Count": 10,
            "PassesLeft": 0,
            "MinutesLeft": 600,
            "CreditDetailsList": [
            ]
        },
        {
            "TimePass": {},
            "Remaining": 37,
            "RemainingUses": 0,
            "CreditObject": {},
            "CreditName": "9 am to 5pm",
            "Count": 37,
            "PassesLeft": 37,
            "MinutesLeft": 0,
            "CreditDetailsList": [
                
            ]
        },
        {
            "TimePass": {},
            "Remaining": 0,
            "RemainingUses": 1080,
            "CreditObject": {},
            "CreditName": "hour pass",
            "Count": 18,
            "PassesLeft": 0,
            "MinutesLeft": 1080,
            "CreditDetailsList": [
                
            ]
        }
    ],
    "BookingCredits": [],
    "OtherExtraServices": [
        {
            "ExtraService": {},
            "Count": 2,
            "CreditName": "Copy of Copy of Meeting Room 3 - Full Day",
            "CreditDescription": "Half Day £160, Full Day £250",
            "Remaining": 240,
            "TotalMinutes": 240,
            "TotalHours": 4,
            "TotalDays": 0,
            "TotalMonths": 0,
            "TotalWeeks": 0,
            "TotalUses": 0,
            "MinutesLeft": 240,
            "HoursLeft": 4,
            "DaysLeft": 0,
            "MonthsLeft": 0,
            "WeeksLeft": 0,
            "UsesLeft": 0,
            "CreditDetailsList": [

            ]
        }
    ],
    "TariffProducts": [],
    "CurrentBalance": -224.46,
    "CheckinsThisWeek": 0,
    "CheckinsThisMonth": 0,
    "MinutesThisWeek": 0,
    "MinutesThisMonth": 0,
    "CheckinsPlan": 0,
    "MinutesPlan": 0,
    "TariffHasLimits": false,
    "CheckinsLeftPlan": 0,
    "MinutesLeftPlan": 0,
    "CheckinsLeftWeek": 0,
    "MinutesLeftWeek": 0,
    "CheckinsLeftMonth": 0,
    "MinutesLeftMonth": 0,
    "ActiveContracts": [],
    "NonCancelledContracts": []
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

