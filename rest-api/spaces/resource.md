# Resource

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/resources" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of resources based on one or more filter querystring parameters.
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
?Resource\_SystemId=...
{% endapi-method-parameter %}

{% api-method-parameter name="Business" type="Business" %}
?Resource\_Business=...
{% endapi-method-parameter %}

{% api-method-parameter name="Name" type="string" %}
?Resource\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="ResourceType" type="ResourceType" %}
?Resource\_ResourceType=...
{% endapi-method-parameter %}

{% api-method-parameter name="Description" type="string" %}
?Resource\_Description=...
{% endapi-method-parameter %}

{% api-method-parameter name="EmailConfirmationContent" type="string" %}
?Resource\_EmailConfirmationContent=...
{% endapi-method-parameter %}

{% api-method-parameter name="Visible" type="bool" %}
?Resource\_Visible=...
{% endapi-method-parameter %}

{% api-method-parameter name="RequiresConfirmation" type="bool" %}
?Resource\_RequiresConfirmation=...
{% endapi-method-parameter %}

{% api-method-parameter name="DisplayOrder" type="int" %}
?Resource\_DisplayOrder=...
{% endapi-method-parameter %}

{% api-method-parameter name="GroupName" type="string" %}
?Resource\_GroupName=...
{% endapi-method-parameter %}

{% api-method-parameter name="Projector" type="bool" %}
?Resource\_Projector=...
{% endapi-method-parameter %}

{% api-method-parameter name="Internet" type="bool" %}
?Resource\_Internet=...
{% endapi-method-parameter %}

{% api-method-parameter name="ConferencePhone" type="bool" %}
?Resource\_ConferencePhone=...
{% endapi-method-parameter %}

{% api-method-parameter name="StandardPhone" type="bool" %}
?Resource\_StandardPhone=...
{% endapi-method-parameter %}

{% api-method-parameter name="WhiteBoard" type="bool" %}
?Resource\_WhiteBoard=...
{% endapi-method-parameter %}

{% api-method-parameter name="LargeDisplay" type="bool" %}
?Resource\_LargeDisplay=...
{% endapi-method-parameter %}

{% api-method-parameter name="Catering" type="bool" %}
?Resource\_Catering=...
{% endapi-method-parameter %}

{% api-method-parameter name="TeaAndCoffee" type="bool" %}
?Resource\_TeaAndCoffee=...
{% endapi-method-parameter %}

{% api-method-parameter name="Drinks" type="bool" %}
?Resource\_Drinks=...
{% endapi-method-parameter %}

{% api-method-parameter name="SecurityLock" type="bool" %}
?Resource\_SecurityLock=...
{% endapi-method-parameter %}

{% api-method-parameter name="CCTV" type="bool" %}
?Resource\_CCTV=...
{% endapi-method-parameter %}

{% api-method-parameter name="VoiceRecorder" type="bool" %}
?Resource\_VoiceRecorder=...
{% endapi-method-parameter %}

{% api-method-parameter name="AirConditioning" type="bool" %}
?Resource\_AirConditioning=...
{% endapi-method-parameter %}

{% api-method-parameter name="Heating" type="bool" %}
?Resource\_Heating=...
{% endapi-method-parameter %}

{% api-method-parameter name="NaturalLight" type="bool" %}
?Resource\_NaturalLight=...
{% endapi-method-parameter %}

{% api-method-parameter name="AllowMultipleBookings" type="bool" %}
?Resource\_AllowMultipleBookings=...
{% endapi-method-parameter %}

{% api-method-parameter name="Allocation" type="int?" %}
?Resource\_Allocation=...
{% endapi-method-parameter %}

{% api-method-parameter name="BookInAdvanceLimit" type="int?" %}
?Resource\_BookInAdvanceLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="LateBookingLimit" type="int?" %}
?Resource\_LateBookingLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="LateCancellationLimit" type="int?" %}
?Resource\_LateCancellationLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="IntervalLimit" type="int?" %}
?Resource\_IntervalLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicy" type="int?" %}
?Resource\_NoReturnPolicy=...
{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicyAllResources" type="int?" %}
?Resource\_NoReturnPolicyAllResources=...
{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicyAllUsers" type="int?" %}
?Resource\_NoReturnPolicyAllUsers=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxBookingLength" type="int?" %}
?Resource\_MaxBookingLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="MinBookingLength" type="int?" %}
?Resource\_MinBookingLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="Shifts" type="string" %}
?Resource\_Shifts=...
{% endapi-method-parameter %}

{% api-method-parameter name="Longitude" type="decimal?" %}
?Resource\_Longitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="Latitude" type="decimal?" %}
?Resource\_Latitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="HideInCalendar" type="bool" %}
?Resource\_HideInCalendar=...
{% endapi-method-parameter %}

{% api-method-parameter name="Archived" type="bool" %}
?Resource\_Archived=...
{% endapi-method-parameter %}

{% api-method-parameter name="ResourceType\_Name" type="string" %}
?Resource\_ResourceType\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tariffs" type="int" required=false %}
?Resource\_Tariffs=...
{% endapi-method-parameter %}

{% api-method-parameter name="LinkedResources" type="int" required=false %}
?Resource\_LinkedResources=...
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
        "ResourceType": null,
        "Description": "Descripción",
        "EmailConfirmationContent": "Descripción",
        "Visible": true,
        "RequiresConfirmation": true,
        "DisplayOrder": true,
        "GroupName": "GroupName",
        "Projector": true,
        "Internet": true,
        "ConferencePhone": true,
        "StandardPhone": true,
        "WhiteBoard": true,
        "LargeDisplay": true,
        "Catering": true,
        "TeaAndCoffee": true,
        "Drinks": true,
        "SecurityLock": true,
        "CCTV": true,
        "VoiceRecorder": true,
        "AirConditioning": true,
        "Heating": true,
        "NaturalLight": true,
        "AllowMultipleBookings": true,
        "Allocation": 0,
        "BookInAdvanceLimit": 0,
        "LateBookingLimit": 0,
        "LateCancellationLimit": 0,
        "IntervalLimit": 0,
        "NoReturnPolicy": 0,
        "NoReturnPolicyAllResources": 0,
        "NoReturnPolicyAllUsers": 0,
        "MaxBookingLength": 0,
        "MinBookingLength": 0,
        "Shifts": "null",
        "Longitude": 1,
        "Latitude": 1,
        "HideInCalendar": true,
        "Archived": true,
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

> 🔒 Requires user role `resource-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/resources" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of resources.
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
        "ResourceType": null,
        "Description": "Descripción",
        "EmailConfirmationContent": "Descripción",
        "Visible": true,
        "RequiresConfirmation": true,
        "DisplayOrder": true,
        "GroupName": "GroupName",
        "Projector": true,
        "Internet": true,
        "ConferencePhone": true,
        "StandardPhone": true,
        "WhiteBoard": true,
        "LargeDisplay": true,
        "Catering": true,
        "TeaAndCoffee": true,
        "Drinks": true,
        "SecurityLock": true,
        "CCTV": true,
        "VoiceRecorder": true,
        "AirConditioning": true,
        "Heating": true,
        "NaturalLight": true,
        "AllowMultipleBookings": true,
        "Allocation": 0,
        "BookInAdvanceLimit": 0,
        "LateBookingLimit": 0,
        "LateCancellationLimit": 0,
        "IntervalLimit": 0,
        "NoReturnPolicy": 0,
        "NoReturnPolicyAllResources": 0,
        "NoReturnPolicyAllUsers": 0,
        "MaxBookingLength": 0,
        "MinBookingLength": 0,
        "Shifts": "null",
        "Longitude": 1,
        "Latitude": 1,
        "HideInCalendar": true,
        "Archived": true,
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

> 🔒 Requires user role `resource-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/resources" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of resources based on a range of dates, integer or decimal properties.
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
?to\_Resource\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_Resource\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_Resource\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_Resource\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="DisplayOrder" type="int" required=false %}
?from\_Resource\_DisplayOrder=...
{% endapi-method-parameter %}

{% api-method-parameter name="DisplayOrder" type="int" required=false %}
?to\_Resource\_DisplayOrder=...
{% endapi-method-parameter %}

{% api-method-parameter name="Allocation" type="int" required=false %}
?from\_Resource\_Allocation=...
{% endapi-method-parameter %}

{% api-method-parameter name="Allocation" type="int" required=false %}
?to\_Resource\_Allocation=...
{% endapi-method-parameter %}

{% api-method-parameter name="BookInAdvanceLimit" type="int" required=false %}
?from\_Resource\_BookInAdvanceLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="BookInAdvanceLimit" type="int" required=false %}
?to\_Resource\_BookInAdvanceLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="LateBookingLimit" type="int" required=false %}
?from\_Resource\_LateBookingLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="LateBookingLimit" type="int" required=false %}
?to\_Resource\_LateBookingLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="LateCancellationLimit" type="int" required=false %}
?from\_Resource\_LateCancellationLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="LateCancellationLimit" type="int" required=false %}
?to\_Resource\_LateCancellationLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="IntervalLimit" type="int" required=false %}
?from\_Resource\_IntervalLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="IntervalLimit" type="int" required=false %}
?to\_Resource\_IntervalLimit=...
{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicy" type="int" required=false %}
?from\_Resource\_NoReturnPolicy=...
{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicy" type="int" required=false %}
?to\_Resource\_NoReturnPolicy=...
{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicyAllResources" type="int" required=false %}
?from\_Resource\_NoReturnPolicyAllResources=...
{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicyAllResources" type="int" required=false %}
?to\_Resource\_NoReturnPolicyAllResources=...
{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicyAllUsers" type="int" required=false %}
?from\_Resource\_NoReturnPolicyAllUsers=...
{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicyAllUsers" type="int" required=false %}
?to\_Resource\_NoReturnPolicyAllUsers=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxBookingLength" type="int" required=false %}
?from\_Resource\_MaxBookingLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="MaxBookingLength" type="int" required=false %}
?to\_Resource\_MaxBookingLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="MinBookingLength" type="int" required=false %}
?from\_Resource\_MinBookingLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="MinBookingLength" type="int" required=false %}
?to\_Resource\_MinBookingLength=...
{% endapi-method-parameter %}

{% api-method-parameter name="Longitude" type="decimal" required=false %}
?from\_Resource\_Longitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="Longitude" type="decimal" required=false %}
?to\_Resource\_Longitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="Latitude" type="decimal" required=false %}
?from\_Resource\_Latitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="Latitude" type="decimal" required=false %}
?to\_Resource\_Latitude=...
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
        "ResourceType": null,
        "Description": "Descripción",
        "EmailConfirmationContent": "Descripción",
        "Visible": true,
        "RequiresConfirmation": true,
        "DisplayOrder": true,
        "GroupName": "GroupName",
        "Projector": true,
        "Internet": true,
        "ConferencePhone": true,
        "StandardPhone": true,
        "WhiteBoard": true,
        "LargeDisplay": true,
        "Catering": true,
        "TeaAndCoffee": true,
        "Drinks": true,
        "SecurityLock": true,
        "CCTV": true,
        "VoiceRecorder": true,
        "AirConditioning": true,
        "Heating": true,
        "NaturalLight": true,
        "AllowMultipleBookings": true,
        "Allocation": 0,
        "BookInAdvanceLimit": 0,
        "LateBookingLimit": 0,
        "LateCancellationLimit": 0,
        "IntervalLimit": 0,
        "NoReturnPolicy": 0,
        "NoReturnPolicyAllResources": 0,
        "NoReturnPolicyAllUsers": 0,
        "MaxBookingLength": 0,
        "MinBookingLength": 0,
        "Shifts": "null",
        "Longitude": 1,
        "Latitude": 1,
        "HideInCalendar": true,
        "Archived": true,
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

> 🔒 Requires user role `resource-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/resources?Resource\_Id=\[:id1,:id2,...\]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more resource records based on their Id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every resource to fetch. I.e. \[123456,789102,...\]
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
        "Business": null,
        "Name": "Name",
        "ResourceType": null,
        "Description": "Descripción",
        "EmailConfirmationContent": "Descripción",
        "Visible": true,
        "RequiresConfirmation": true,
        "DisplayOrder": true,
        "GroupName": "GroupName",
        "Projector": true,
        "Internet": true,
        "ConferencePhone": true,
        "StandardPhone": true,
        "WhiteBoard": true,
        "LargeDisplay": true,
        "Catering": true,
        "TeaAndCoffee": true,
        "Drinks": true,
        "SecurityLock": true,
        "CCTV": true,
        "VoiceRecorder": true,
        "AirConditioning": true,
        "Heating": true,
        "NaturalLight": true,
        "AllowMultipleBookings": true,
        "Allocation": 0,
        "BookInAdvanceLimit": 0,
        "LateBookingLimit": 0,
        "LateCancellationLimit": 0,
        "IntervalLimit": 0,
        "NoReturnPolicy": 0,
        "NoReturnPolicyAllResources": 0,
        "NoReturnPolicyAllUsers": 0,
        "MaxBookingLength": 0,
        "MinBookingLength": 0,
        "Shifts": "null",
        "Longitude": 1,
        "Latitude": 1,
        "HideInCalendar": true,
        "Archived": true,
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

> 🔒 Requires user role `resource-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/resources/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one resource record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the resource to fetch.
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
        "Business": null,
        "Name": "Name",
        "ResourceType": null,
        "Description": "Descripción",
        "EmailConfirmationContent": "Descripción",
        "Visible": true,
        "RequiresConfirmation": true,
        "DisplayOrder": true,
        "GroupName": "GroupName",
        "Projector": true,
        "Internet": true,
        "ConferencePhone": true,
        "StandardPhone": true,
        "WhiteBoard": true,
        "LargeDisplay": true,
        "Catering": true,
        "TeaAndCoffee": true,
        "Drinks": true,
        "SecurityLock": true,
        "CCTV": true,
        "VoiceRecorder": true,
        "AirConditioning": true,
        "Heating": true,
        "NaturalLight": true,
        "AllowMultipleBookings": true,
        "Allocation": 0,
        "BookInAdvanceLimit": 0,
        "LateBookingLimit": 0,
        "LateCancellationLimit": 0,
        "IntervalLimit": 0,
        "NoReturnPolicy": 0,
        "NoReturnPolicyAllResources": 0,
        "NoReturnPolicyAllUsers": 0,
        "MaxBookingLength": 0,
        "MinBookingLength": 0,
        "Shifts": "null",
        "Longitude": 1,
        "Latitude": 1,
        "HideInCalendar": true,
        "Archived": true,
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

> 🔒 Requires user role `resource-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/spaces/resources" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new resource.
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

{% api-method-parameter name="ResourceTypeId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Description" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="EmailConfirmationContent" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Visible" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RequiresConfirmation" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DisplayOrder" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="GroupName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Projector" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Internet" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ConferencePhone" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="StandardPhone" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WhiteBoard" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LargeDisplay" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Catering" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TeaAndCoffee" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Drinks" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SecurityLock" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CCTV" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="VoiceRecorder" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AirConditioning" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Heating" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NaturalLight" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AllowMultipleBookings" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Allocation" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BookInAdvanceLimit" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LateBookingLimit" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LateCancellationLimit" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="IntervalLimit" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicy" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicyAllResources" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicyAllUsers" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MaxBookingLength" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MinBookingLength" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Shifts" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Longitude" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Latitude" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="HideInCalendar" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Archived" type="bool" required=false %}

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

> 🔒 Requires user role `resource-create`

```javascript
{
    "Business": 12345678,
    "Name": "Name",
    "ResourceType": 12345678,
    "Description": "Descripción",
    "EmailConfirmationContent": "Descripción",
    "Visible": true,
    "RequiresConfirmation": true,
    "DisplayOrder": true,
    "GroupName": "GroupName",
    "Projector": true,
    "Internet": true,
    "ConferencePhone": true,
    "StandardPhone": true,
    "WhiteBoard": true,
    "LargeDisplay": true,
    "Catering": true,
    "TeaAndCoffee": true,
    "Drinks": true,
    "SecurityLock": true,
    "CCTV": true,
    "VoiceRecorder": true,
    "AirConditioning": true,
    "Heating": true,
    "NaturalLight": true,
    "AllowMultipleBookings": true,
    "Allocation": 0,
    "BookInAdvanceLimit": 0,
    "LateBookingLimit": 0,
    "LateCancellationLimit": 0,
    "IntervalLimit": 0,
    "NoReturnPolicy": 0,
    "NoReturnPolicyAllResources": 0,
    "NoReturnPolicyAllUsers": 0,
    "MaxBookingLength": 0,
    "MinBookingLength": 0,
    "Tariffs": [12345678, 87654321] (replaces entire list),
    "AddedTariffs": [12345678, 87654321] (adds to list),
    "RemovedTariffs": [12345678, 87654321] (removes from list),
    "Shifts": "null",
    "LinkedResources": [12345678, 87654321] (replaces entire list),
    "AddedLinkedResources": [12345678, 87654321] (adds to list),
    "RemovedLinkedResources": [12345678, 87654321] (removes from list),
    "Longitude": 1,
    "Latitude": 1,
    "HideInCalendar": true,
    "Archived": true,
}
```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/spaces/resources" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing resource.Required User Role: `resource-edit`
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

{% api-method-parameter name="ResourceTypeId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Description" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="EmailConfirmationContent" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Visible" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RequiresConfirmation" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DisplayOrder" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="GroupName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Projector" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Internet" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ConferencePhone" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="StandardPhone" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WhiteBoard" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LargeDisplay" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Catering" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TeaAndCoffee" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Drinks" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SecurityLock" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CCTV" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="VoiceRecorder" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AirConditioning" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Heating" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NaturalLight" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AllowMultipleBookings" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Allocation" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="BookInAdvanceLimit" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LateBookingLimit" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LateCancellationLimit" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="IntervalLimit" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicy" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicyAllResources" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NoReturnPolicyAllUsers" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MaxBookingLength" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MinBookingLength" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Tariffs" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AddedTariffs" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RemovedTariffs" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Shifts" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LinkedResources" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AddedLinkedResources" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RemovedLinkedResources" type="int\[\]" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Longitude" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Latitude" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="HideInCalendar" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Archived" type="bool" required=false %}

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

> 🔒 Requires user role `resource-edit`

```javascript
{
    "Business": 12345678,
    "Name": "Name",
    "ResourceType": 12345678,
    "Description": "Descripción",
    "EmailConfirmationContent": "Descripción",
    "Visible": true,
    "RequiresConfirmation": true,
    "DisplayOrder": true,
    "GroupName": "GroupName",
    "Projector": true,
    "Internet": true,
    "ConferencePhone": true,
    "StandardPhone": true,
    "WhiteBoard": true,
    "LargeDisplay": true,
    "Catering": true,
    "TeaAndCoffee": true,
    "Drinks": true,
    "SecurityLock": true,
    "CCTV": true,
    "VoiceRecorder": true,
    "AirConditioning": true,
    "Heating": true,
    "NaturalLight": true,
    "AllowMultipleBookings": true,
    "Allocation": 0,
    "BookInAdvanceLimit": 0,
    "LateBookingLimit": 0,
    "LateCancellationLimit": 0,
    "IntervalLimit": 0,
    "NoReturnPolicy": 0,
    "NoReturnPolicyAllResources": 0,
    "NoReturnPolicyAllUsers": 0,
    "MaxBookingLength": 0,
    "MinBookingLength": 0,
    "Tariffs": [12345678, 87654321] (replaces entire list),
    "AddedTariffs": [12345678, 87654321] (adds to list),
    "RemovedTariffs": [12345678, 87654321] (removes from list),
    "Shifts": "null",
    "LinkedResources": [12345678, 87654321] (replaces entire list),
    "AddedLinkedResources": [12345678, 87654321] (adds to list),
    "RemovedLinkedResources": [12345678, 87654321] (removes from list),
    "Longitude": 1,
    "Latitude": 1,
    "HideInCalendar": true,
    "Archived": true,
}
```

{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/spaces/resources/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a resource.Required User Roles: `resource-delete`
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

> 🔒 Requires user role `resource-delete`

## Commands

Commands allow to perform actions against one or more resource records. Some commands accept only one record while others can run an action for a number of records at the same time. Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/resources/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for resource records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/resources/runcommand" %}
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

> 🔒 Requires user role `resource-edit`

## Enumerated values

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/resources/getpicture/:id" %}
{% api-method-summary %}
Picture
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Resource to get the picture for.
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

* [Business](../sys/business.md)
* [ResourceType](resourcetype.md)

