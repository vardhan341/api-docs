# Booking

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/bookings" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of bookings based on one or more filter querystring parameters.
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
?Booking\_SystemId=...
{% endapi-method-parameter %}

{% api-method-parameter name="Resource" type="Resource" %}
?Booking\_Resource=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker" type="Coworker" %}
?Booking\_Coworker=...
{% endapi-method-parameter %}

{% api-method-parameter name="ExtraService" type="ExtraService" %}
?Booking\_ExtraService=...
{% endapi-method-parameter %}

{% api-method-parameter name="FromTime" type="DateTime" %}
?Booking\_FromTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ToTime" type="DateTime" %}
?Booking\_ToTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" %}
?Booking\_Notes=...
{% endapi-method-parameter %}

{% api-method-parameter name="InternalNotes" type="string" %}
?Booking\_InternalNotes=...
{% endapi-method-parameter %}

{% api-method-parameter name="ChargeNow" type="bool" %}
?Booking\_ChargeNow=...
{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceNow" type="bool" %}
?Booking\_InvoiceNow=...
{% endapi-method-parameter %}

{% api-method-parameter name="DoNotUseBookingCredit" type="bool" %}
?Booking\_DoNotUseBookingCredit=...
{% endapi-method-parameter %}

{% api-method-parameter name="PurchaseOrder" type="string" %}
?Booking\_PurchaseOrder=...
{% endapi-method-parameter %}

{% api-method-parameter name="DiscountCode" type="string" %}
?Booking\_DiscountCode=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tentative" type="bool" %}
?Booking\_Tentative=...
{% endapi-method-parameter %}

{% api-method-parameter name="Online" type="bool" %}
?Booking\_Online=...
{% endapi-method-parameter %}

{% api-method-parameter name="TeamsAtTheTimeOfBooking" type="string" %}
?Booking\_TeamsAtTheTimeOfBooking=...
{% endapi-method-parameter %}

{% api-method-parameter name="TariffAtTheTimeOfBooking" type="string" %}
?Booking\_TariffAtTheTimeOfBooking=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatSeriesUniqueId" type="Guid?" %}
?Booking\_RepeatSeriesUniqueId=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatBooking" type="bool" %}
?Booking\_RepeatBooking=...
{% endapi-method-parameter %}

{% api-method-parameter name="Repeats" type="enum" %}
?Booking\_Repeats=...
{% endapi-method-parameter %}

{% api-method-parameter name="WhichBookingsToUpdate" type="enum" %}
?Booking\_WhichBookingsToUpdate=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatEvery" type="int?" %}
?Booking\_RepeatEvery=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatUntil" type="DateTime?" %}
?Booking\_RepeatUntil=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnMondays" type="bool" %}
?Booking\_RepeatOnMondays=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnTuesdays" type="bool" %}
?Booking\_RepeatOnTuesdays=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnWednesdays" type="bool" %}
?Booking\_RepeatOnWednesdays=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnThursdays" type="bool" %}
?Booking\_RepeatOnThursdays=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnFridays" type="bool" %}
?Booking\_RepeatOnFridays=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnSaturdays" type="bool" %}
?Booking\_RepeatOnSaturdays=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnSundays" type="bool" %}
?Booking\_RepeatOnSundays=...
{% endapi-method-parameter %}

{% api-method-parameter name="OverridePrice" type="decimal?" %}
?Booking\_OverridePrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="OverridePrice" type="decimal?" %}
?Booking\_OverridePrice=...
{% endapi-method-parameter %}


{% api-method-parameter name="Invoiced" type="bool" %}
?Booking\_Invoiced=...
{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceDate" type="DateTime?" %}
?Booking\_InvoiceDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoiceId" type="int?" %}
?Booking\_CoworkerInvoiceId=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoiceNumber" type="string" %}
?Booking\_CoworkerInvoiceNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoicePaid" type="bool" %}
?Booking\_CoworkerInvoicePaid=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceIds" type="string" %}
?Booking\_CoworkerExtraServiceIds=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServicePrice" type="decimal?" %}
?Booking\_CoworkerExtraServicePrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceCurrencyCode" type="string" %}
?Booking\_CoworkerExtraServiceCurrencyCode=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceChargePeriod" type="int?" %}
?Booking\_CoworkerExtraServiceChargePeriod=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceTotalUses" type="int?" %}
?Booking\_CoworkerExtraServiceTotalUses=...
{% endapi-method-parameter %}

{% api-method-parameter name="Resource\_Name" type="string" %}
?Booking\_Resource\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Resource\_HideInCalendar" type="string" %}
?Booking\_Resource\_HideInCalendar=...
{% endapi-method-parameter %}

{% api-method-parameter name="Resource\_ResourceType\_Id" type="string" %}
?Booking\_Resource\_ResourceType\_Id=...
{% endapi-method-parameter %}

{% api-method-parameter name="Resource\_ResourceType\_Name" type="string" %}
?Booking\_Resource\_ResourceType\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Coworker\_FullName" type="string" %}
?Booking\_Coworker\_FullName=...
{% endapi-method-parameter %}

{% api-method-parameter name="ExtraService\_Name" type="string" %}
?Booking\_ExtraService\_Name=...
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
        "Resource": null,
        "Coworker": null,
        "ExtraService": null,
        "FromTime": DateTime.Parse("FromTime"),
        "ToTime": DateTime.Parse("FromTime"),
        "Notes": "Notes",
        "InternalNotes": "Notes",
        "ChargeNow": false,
        "InvoiceNow": false,
        "DoNotUseBookingCredit": false,
        "PurchaseOrder": "PurchaseOrder",
        "DiscountCode": "DiscountCode",
        "Tentative": false,
        "Online": false,
        "TeamsAtTheTimeOfBooking": "false",
        "TariffAtTheTimeOfBooking": "false",
        "RepeatSeriesUniqueId": ,
        "RepeatBooking": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eBookingRepeatCycle.Weekly,
        "WhichBookingsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedBookingUpdateAction.UpdateThisBookingOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
        "OverridePrice": false,
        "Invoiced": false,
        "InvoiceDate": ,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
        "CoworkerExtraServiceIds": "",
        "CoworkerExtraServicePrice": ,
        "CoworkerExtraServiceCurrencyCode": "",
        "CoworkerExtraServiceChargePeriod": ,
        "CoworkerExtraServiceTotalUses": ,
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

> 🔒 Requires user role `booking-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/bookings" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of bookings.
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
        "Resource": null,
        "Coworker": null,
        "ExtraService": null,
        "FromTime": DateTime.Parse("FromTime"),
        "ToTime": DateTime.Parse("FromTime"),
        "Notes": "Notes",
        "InternalNotes": "Notes",
        "ChargeNow": false,
        "InvoiceNow": false,
        "DoNotUseBookingCredit": false,
        "PurchaseOrder": "PurchaseOrder",
        "DiscountCode": "DiscountCode",
        "Tentative": false,
        "Online": false,
        "TeamsAtTheTimeOfBooking": "false",
        "TariffAtTheTimeOfBooking": "false",
        "RepeatSeriesUniqueId": ,
        "RepeatBooking": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eBookingRepeatCycle.Weekly,
        "WhichBookingsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedBookingUpdateAction.UpdateThisBookingOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
        "OverridePrice": false,
        "Invoiced": false,
        "InvoiceDate": ,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
        "CoworkerExtraServiceIds": "",
        "CoworkerExtraServicePrice": ,
        "CoworkerExtraServiceCurrencyCode": "",
        "CoworkerExtraServiceChargePeriod": ,
        "CoworkerExtraServiceTotalUses": ,
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

> 🔒 Requires user role `booking-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/bookings" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of bookings based on a range of dates, integer or decimal properties.
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
?to\_Booking\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_Booking\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_Booking\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_Booking\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="FromTime" type="datetime" required=false %}
?from\_Booking\_FromTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="FromTime" type="datetime" required=false %}
?to\_Booking\_FromTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ToTime" type="datetime" required=false %}
?from\_Booking\_ToTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ToTime" type="datetime" required=false %}
?to\_Booking\_ToTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatEvery" type="int" required=false %}
?from\_Booking\_RepeatEvery=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatEvery" type="int" required=false %}
?to\_Booking\_RepeatEvery=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatUntil" type="datetime" required=false %}
?from\_Booking\_RepeatUntil=...
{% endapi-method-parameter %}

{% api-method-parameter name="RepeatUntil" type="datetime" required=false %}
?to\_Booking\_RepeatUntil=...
{% endapi-method-parameter %}
{% api-method-parameter name="OverridePrice" type="decimal" required=false %}
?from\_Booking\_OverridePrice=...
{% endapi-method-parameter %}
{% api-method-parameter name="OverridePrice" type="decimal" required=false %}
?to\_Booking\_OverridePrice=...
{% endapi-method-parameter %}
{% api-method-parameter name="InvoiceDate" type="datetime" required=false %}
?from\_Booking\_InvoiceDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceDate" type="datetime" required=false %}
?to\_Booking\_InvoiceDate=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoiceId" type="int" required=false %}
?from\_Booking\_CoworkerInvoiceId=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoiceId" type="int" required=false %}
?to\_Booking\_CoworkerInvoiceId=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServicePrice" type="decimal" required=false %}
?from\_Booking\_CoworkerExtraServicePrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServicePrice" type="decimal" required=false %}
?to\_Booking\_CoworkerExtraServicePrice=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceChargePeriod" type="int" required=false %}
?from\_Booking\_CoworkerExtraServiceChargePeriod=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceChargePeriod" type="int" required=false %}
?to\_Booking\_CoworkerExtraServiceChargePeriod=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceTotalUses" type="int" required=false %}
?from\_Booking\_CoworkerExtraServiceTotalUses=...
{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceTotalUses" type="int" required=false %}
?to\_Booking\_CoworkerExtraServiceTotalUses=...
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
        "Resource": null,
        "Coworker": null,
        "ExtraService": null,
        "FromTime": DateTime.Parse("FromTime"),
        "ToTime": DateTime.Parse("FromTime"),
        "Notes": "Notes",
        "InternalNotes": "Notes",
        "ChargeNow": false,
        "InvoiceNow": false,
        "DoNotUseBookingCredit": false,
        "PurchaseOrder": "PurchaseOrder",
        "DiscountCode": "DiscountCode",
        "Tentative": false,
        "Online": false,
        "TeamsAtTheTimeOfBooking": "false",
        "TariffAtTheTimeOfBooking": "false",
        "RepeatSeriesUniqueId": ,
        "RepeatBooking": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eBookingRepeatCycle.Weekly,
        "WhichBookingsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedBookingUpdateAction.UpdateThisBookingOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
        "OverridePrice": false,
        "Invoiced": false,
        "InvoiceDate": ,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
        "CoworkerExtraServiceIds": "",
        "CoworkerExtraServicePrice": ,
        "CoworkerExtraServiceCurrencyCode": "",
        "CoworkerExtraServiceChargePeriod": ,
        "CoworkerExtraServiceTotalUses": ,
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

> 🔒 Requires user role `booking-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/bookings?Booking\_Id=\[:id1,:id2,...\]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more booking records based on their Id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every booking to fetch. I.e. \[123456,789102,...\]
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
        "Resource": null,
        "Coworker": null,
        "ExtraService": null,
        "FromTime": DateTime.Parse("FromTime"),
        "ToTime": DateTime.Parse("FromTime"),
        "Notes": "Notes",
        "InternalNotes": "Notes",
        "ChargeNow": false,
        "InvoiceNow": false,
        "DoNotUseBookingCredit": false,
        "PurchaseOrder": "PurchaseOrder",
        "DiscountCode": "DiscountCode",
        "Tentative": false,
        "Online": false,
        "TeamsAtTheTimeOfBooking": "false",
        "TariffAtTheTimeOfBooking": "false",
        "RepeatSeriesUniqueId": ,
        "RepeatBooking": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eBookingRepeatCycle.Weekly,
        "WhichBookingsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedBookingUpdateAction.UpdateThisBookingOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
        "OverridePrice": false,
        "Invoiced": false,
        "InvoiceDate": ,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
        "CoworkerExtraServiceIds": "",
        "CoworkerExtraServicePrice": ,
        "CoworkerExtraServiceCurrencyCode": "",
        "CoworkerExtraServiceChargePeriod": ,
        "CoworkerExtraServiceTotalUses": ,
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

> 🔒 Requires user role `booking-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/bookings?Booking\_Id=\[:id1,:id2,...\]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more booking records based on their Id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every booking to fetch. I.e. \[123456,789102,...\]
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
        "Resource": null,
        "Coworker": null,
        "ExtraService": null,
        "FromTime": DateTime.Parse("FromTime"),
        "ToTime": DateTime.Parse("FromTime"),
        "Notes": "Notes",
        "InternalNotes": "Notes",
        "ChargeNow": false,
        "InvoiceNow": false,
        "DoNotUseBookingCredit": false,
        "PurchaseOrder": "PurchaseOrder",
        "DiscountCode": "DiscountCode",
        "Tentative": false,
        "Online": false,
        "TeamsAtTheTimeOfBooking": "false",
        "TariffAtTheTimeOfBooking": "false",
        "RepeatSeriesUniqueId": ,
        "RepeatBooking": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eBookingRepeatCycle.Weekly,
        "WhichBookingsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedBookingUpdateAction.UpdateThisBookingOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
        "OverridePrice": false,
        "Invoiced": false,
        "InvoiceDate": ,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
        "CoworkerExtraServiceIds": "",
        "CoworkerExtraServicePrice": ,
        "CoworkerExtraServiceCurrencyCode": "",
        "CoworkerExtraServiceChargePeriod": ,
        "CoworkerExtraServiceTotalUses": ,
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

```
"Not found"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> 🔒 Requires user role `booking-list`


{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/bookings?Booking_Id=[:id1,:id2,...]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more booking records based on their Id.
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
Comma-separated list of IDs of every booking to fetch. I.e. [123456,789102,...] 
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
        "Resource": null,
        "Coworker": null,
        "ExtraService": null,
        "FromTime": DateTime.Parse("FromTime"),
        "ToTime": DateTime.Parse("FromTime"),
        "Notes": "Notes",
        "InternalNotes": "Notes",
        "ChargeNow": false,
        "InvoiceNow": false,
        "DoNotUseBookingCredit": false,
        "PurchaseOrder": "PurchaseOrder",
        "DiscountCode": "DiscountCode",
        "Tentative": false,
        "Online": false,
        "TeamsAtTheTimeOfBooking": "false",
        "TariffAtTheTimeOfBooking": "false",
        "RepeatSeriesUniqueId": ,
        "RepeatBooking": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eBookingRepeatCycle.Weekly,
        "WhichBookingsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedBookingUpdateAction.UpdateThisBookingOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
        "Invoiced": false,
        "InvoiceDate": ,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
        "CoworkerExtraServiceIds": "",
        "CoworkerExtraServicePrice": ,
        "CoworkerExtraServiceCurrencyCode": "",
        "CoworkerExtraServiceChargePeriod": ,
        "CoworkerExtraServiceTotalUses": ,
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

> 🔒 Requires user role `booking-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/bookings/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one booking record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the booking to fetch.
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
        "Resource": null,
        "Coworker": null,
        "ExtraService": null,
        "FromTime": DateTime.Parse("FromTime"),
        "ToTime": DateTime.Parse("FromTime"),
        "Notes": "Notes",
        "InternalNotes": "Notes",
        "ChargeNow": false,
        "InvoiceNow": false,
        "DoNotUseBookingCredit": false,
        "PurchaseOrder": "PurchaseOrder",
        "DiscountCode": "DiscountCode",
        "Tentative": false,
        "Online": false,
        "TeamsAtTheTimeOfBooking": "false",
        "TariffAtTheTimeOfBooking": "false",
        "RepeatSeriesUniqueId": ,
        "RepeatBooking": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eBookingRepeatCycle.Weekly,
        "WhichBookingsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedBookingUpdateAction.UpdateThisBookingOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
        "OverridePrice": false,
        "Invoiced": false,
        "InvoiceDate": ,
        "CoworkerInvoiceId": ,
        "CoworkerInvoiceNumber": "",
        "CoworkerInvoicePaid": ,
        "CoworkerExtraServiceIds": "",
        "CoworkerExtraServicePrice": ,
        "CoworkerExtraServiceCurrencyCode": "",
        "CoworkerExtraServiceChargePeriod": ,
        "CoworkerExtraServiceTotalUses": ,
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

> 🔒 Requires user role `booking-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/spaces/bookings" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new booking.
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
{% api-method-parameter name="ResourceId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ExtraServiceId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FromTime" type="DateTime" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="ToTime" type="DateTime" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="InternalNotes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ChargeNow" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceNow" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DoNotUseBookingCredit" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PurchaseOrder" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountCode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Tentative" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TeamsAtTheTimeOfBooking" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TariffAtTheTimeOfBooking" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatSeriesUniqueId" type="Guid?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatBooking" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Repeats" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatEvery" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatUntil" type="DateTime?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnMondays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnTuesdays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnWednesdays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnThursdays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnFridays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnSaturdays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnSundays" type="bool" required=false %}

{% endapi-method-parameter %}
{% api-method-parameter name="OverridePrice" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerInvoiceId" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoiceNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoicePaid" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceIds" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServicePrice" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceCurrencyCode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceChargePeriod" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceTotalUses" type="int?" required=false %}

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

> 🔒 Requires user role `booking-create`

```javascript
{
	"Resource": 12345678,
	"Coworker": 12345678,
	"ExtraService": 12345678,
	"FromTime": DateTime.Parse("FromTime"),
	"ToTime": DateTime.Parse("FromTime"),
	"Notes": "Notes",
	"InternalNotes": "Notes",
	"ChargeNow": false,
	"InvoiceNow": false,
	"DoNotUseBookingCredit": false,
	"PurchaseOrder": "PurchaseOrder",
	"DiscountCode": "DiscountCode",
	"Tentative": false,
	"TeamsAtTheTimeOfBooking": "false",
	"TariffAtTheTimeOfBooking": "false",
	"RepeatSeriesUniqueId": ,
	"RepeatBooking": false,
	"Repeats": 1 (check Enumerated values section below),
	"RepeatEvery": ,
	"RepeatUntil": ,
	"RepeatOnMondays": false,
	"RepeatOnTuesdays": false,
	"RepeatOnWednesdays": false,
	"RepeatOnThursdays": false,
	"RepeatOnFridays": false,
	"RepeatOnSaturdays": false,
	"RepeatOnSundays": false,
	"OverridePrice": false,
	"CoworkerInvoiceId": ,
	"CoworkerInvoiceNumber": "",
	"CoworkerInvoicePaid": ,
	"CoworkerExtraServiceIds": "",
	"CoworkerExtraServicePrice": ,
	"CoworkerExtraServiceCurrencyCode": "",
	"CoworkerExtraServiceChargePeriod": ,
	"CoworkerExtraServiceTotalUses": ,
}
```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/spaces/bookings" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing booking.Required User Role: `booking-edit`
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
{% api-method-parameter name="ResourceId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ExtraServiceId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FromTime" type="DateTime" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="ToTime" type="DateTime" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Notes" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ChargeNow" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="InvoiceNow" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DoNotUseBookingCredit" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PurchaseOrder" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="DiscountCode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Tentative" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TeamsAtTheTimeOfBooking" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TariffAtTheTimeOfBooking" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatSeriesUniqueId" type="Guid?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Repeats" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WhichBookingsToUpdate" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnMondays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnTuesdays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnWednesdays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnThursdays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnFridays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnSaturdays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RepeatOnSundays" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="OverridePrice" type="decimal?" required=false %}

{% endapi-method-parameter %}
{% api-method-parameter name="OverridePrice" type="decimal?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="CoworkerInvoiceId" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoiceNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerInvoicePaid" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceIds" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServicePrice" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceCurrencyCode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceChargePeriod" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CoworkerExtraServiceTotalUses" type="int?" required=false %}

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

> 🔒 Requires user role `booking-edit`

```javascript
{
	"Resource": 12345678,
	"Coworker": 12345678,
	"ExtraService": 12345678,
	"FromTime": DateTime.Parse("FromTime"),
	"ToTime": DateTime.Parse("FromTime"),
	"Notes": "Notes",
	"ChargeNow": false,
	"InvoiceNow": false,
	"DoNotUseBookingCredit": false,
	"PurchaseOrder": "PurchaseOrder",
	"DiscountCode": "DiscountCode",
	"Tentative": false,
	"TeamsAtTheTimeOfBooking": "false",
	"TariffAtTheTimeOfBooking": "false",
	"RepeatSeriesUniqueId": ,
	"Repeats": 1 (check Enumerated values section below),
	"WhichBookingsToUpdate": 1 (check Enumerated values section below),
	"RepeatOnMondays": false,
	"RepeatOnTuesdays": false,
	"RepeatOnWednesdays": false,
	"RepeatOnThursdays": false,
	"RepeatOnFridays": false,
	"RepeatOnSaturdays": false,
	"RepeatOnSundays": false,
	"OverridePrice": false,
	"CoworkerInvoiceId": ,
	"CoworkerInvoiceNumber": "",
	"CoworkerInvoicePaid": ,
	"CoworkerExtraServiceIds": "",
	"CoworkerExtraServicePrice": ,
	"CoworkerExtraServiceCurrencyCode": "",
	"CoworkerExtraServiceChargePeriod": ,
	"CoworkerExtraServiceTotalUses": ,
}
```

{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/spaces/bookings/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a booking.Required User Roles: `booking-delete`
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

> 🔒 Requires user role `booking-delete`

## Commands

Commands allow to perform actions against one or more booking records. Some commands accept only one record while others can run an action for a number of records at the same time. Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/bookings/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for booking records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/spaces/bookings/runcommand" %}
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

> 🔒 Requires user role `booking-edit`

## Enumerated values

### Repeats:

> GET /api/utils/enums?name=eBookingRepeatCycle

### WhichBookingsToUpdate:

> GET /api/utils/enums?name=eRepeatedBookingUpdateAction

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

## Related Entities

* [Resource](resource.md)
* [Coworker](coworker.md)
* [ExtraService](../billing/extraservice.md)

