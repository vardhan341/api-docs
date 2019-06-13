---
description: >-
  Returns bookings/reservations data and lets you create, update and cancel
  bookings/reservations.
---

# Bookings

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/bookings/calendar" %}
{% api-method-summary %}
Booking Calendar
{% endapi-method-summary %}

{% api-method-description %}
Gets essential data to build a booking calendar. This endpoint does not return actual booking data. Check the "FullCalendarBookings" endpoint to fetch bookings.
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
    "ResourceTypes": [
        {
            "Name": "Hot Desks",
            "Id": 539169648,
            "IdString": "539169648",
            "UpdatedOn": "2018-01-24T05:40:09",
            "CreatedOn": "2018-01-24T05:40:09",
            "UniqueId": "3678b774-bc59-40be-b739-c2e97c7bce97",
            "IsNull": false
        },
        {
            "Name": "Day room ",
            "Id": 1021660649,
            "IdString": "1021660649",
            "UpdatedOn": "2019-05-10T14:57:39",
            "CreatedOn": "2019-05-10T14:57:39",
            "UniqueId": "d06f8410-710f-4680-bcaf-952afe1ac894",
            "IsNull": false
        },
        {
            "Name": "Large Meeting Rooms (hourly)",
            "Id": 287951665,
            "IdString": "287951665",
            "UpdatedOn": "2017-01-27T10:30:17",
            "CreatedOn": "2017-01-27T10:30:17",
            "UniqueId": "0e841048-d59f-421d-bf3f-5fd5e5422eef",
            "IsNull": false
        },
        {
            "Name": "Small Meeting Rooms (hourly)",
            "Id": 287951666,
            "IdString": "287951666",
            "UpdatedOn": "2017-01-27T10:30:17",
            "CreatedOn": "2017-01-27T10:30:17",
            "UniqueId": "4ddd9975-0862-4a64-97b3-3995d7a33e42",
            "IsNull": false
        }
    ],
    "SelectedResourceType": null,
    "OnlyEvents": false,
    "ShowAll": true,
    "AllShifts": [
        {
            "ResourceId": 922186278,
            "Start": "09:00",
            "End": "18:00",
            "Name": "ALL DAY (9AM - 6PM)"
        },
        {
            "ResourceId": 1021761744,
            "Start": "09:00",
            "End": "18:00",
            "Name": "ALL DAY (9AM - 6PM)"
        }
    ],
    "CurrentMonthName": "May 2019",
    "PreviousMonth": "2019-04-27T00:00:00",
    "NextMonth": "2019-06-27T00:00:00",
    "CurrentDate": "2019-05-27T00:00:00",
    "Resources": [
        {
            "Name": "Nexudus Sample Meeting Room",
            "GroupName": null,
            "Description": null,
            "ResourceTypeName": "Hot Desks",
            "ResourceType": {},
            "HasImage": true,
            "Projector": false,
            "Internet": false,
            "ConferencePhone": false,
            "StandardPhone": false,
            "WhiteBoard": false,
            "LargeDisplay": false,
            "Catering": false,
            "TeaAndCoffee": false,
            "Drinks": false,
            "SecurityLock": false,
            "CCTV": false,
            "VoiceRecorder": false,
            "AirConditioning": false,
            "Heating": false,
            "NaturalLight": false,
            "AllowMultipleBookings": false,
            "Allocation": 5,
            "Shifts": [
                {}
            ],
            "IsAvailable": false,
            "AvailableUnits": 0,
            "Message": null,
            "Price": 0,
            "DisplayOrder": 0,
            "PriceFormatted": null,
            "ErrorCode": null,
            "Id": 922186278,
            "IdString": "922186278",
            "UpdatedOn": "2019-05-10T15:56:38",
            "CreatedOn": "2019-02-20T15:15:05",
            "UniqueId": "5f96ea9d-6c73-4b5b-93f0-7569f52806ec",
            "IsNull": false
        },
        {
            "Name": "Day Room ",
            "GroupName": null,
            "Description": null,
            "ResourceTypeName": "Day room ",
            "ResourceType": {},
            "HasImage": true,
            "Projector": false,
            "Internet": false,
            "ConferencePhone": false,
            "StandardPhone": false,
            "WhiteBoard": false,
            "LargeDisplay": false,
            "Catering": false,
            "TeaAndCoffee": false,
            "Drinks": false,
            "SecurityLock": false,
            "CCTV": false,
            "VoiceRecorder": false,
            "AirConditioning": false,
            "Heating": false,
            "NaturalLight": false,
            "AllowMultipleBookings": false,
            "Allocation": null,
            "Shifts": [
                {}
            ],
            "IsAvailable": false,
            "AvailableUnits": 0,
            "Message": null,
            "Price": 0,
            "DisplayOrder": 0,
            "PriceFormatted": null,
            "ErrorCode": null,
            "Id": 1021761744,
            "IdString": "1021761744",
            "UpdatedOn": "2019-05-14T12:52:13",
            "CreatedOn": "2019-05-10T14:58:13",
            "UniqueId": "13a97016-3260-4f62-8abb-dc010e47558d",
            "IsNull": false
        }
    ],
    "UnpaidBookings": [],
    "ShowAllBookings": true,
    "IncludeBookingCreditInPrice": true,
    "ChargeBooingImmediately": false,
    "Resource": null,
    "Group": null
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/bookings/fullCalendarBookings" %}
{% api-method-summary %}
Bookings Data
{% endapi-method-summary %}

{% api-method-description %}
Gets bookings within a date range
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
application/jso
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="" type="object" required=true %}
Return bookings starting after the passed in date.
{% endapi-method-parameter %}

{% api-method-parameter name="end" type="object" required=true %}
Return bookings ending before the passed in date.
{% endapi-method-parameter %}

{% api-method-parameter name="group" type="string" required=false %}
Return bookings only for resources in the passed in group name.
{% endapi-method-parameter %}

{% api-method-parameter name="resourcetypeid" type="integer" required=false %}
Return bookings only for the resource type of the passed in ResoruceTypeId
{% endapi-method-parameter %}

{% api-method-parameter name="resourceId" type="integer" required=false %}
Return bookings only for the resource with the passed in resourceId.
{% endapi-method-parameter %}

{% api-method-parameter name="showAll" type="boolean" required=false %}
Shows all bookings within the passed in period or just those for the logged in users. Default value: true.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
[
    {
        "id": 917876995,
        "resourceId": 287977693,
        "resourceName": "Callisto Meeting Room",
        "title": "Callisto Meeting Room",
        "start": "2019-02-01T00:00Z",
        "end": "2019-02-01T01:00Z",
        "allDay": false,
        "notes": null,
        "editable": false,
        "teamBooking": false,
        "groupName": "Small",
        "coworkerId": "289024940",
        "coworkerEmail": "david@example.net",
        "coworkerFullName": "David Hoch",
        "coworkerCompanyName": "Landing Limited",
        "private": true,
        "event": false,
        "ignoreTimezone": true
    },
    {
        "id": 898654072,
        "resourceId": 287977693,
        "resourceName": "Callisto Meeting Room",
        "title": "Callisto Meeting Room",
        "start": "2019-02-01T17:00Z",
        "end": "2019-02-01T18:15Z",
        "allDay": false,
        "notes": null,
        "editable": false,
        "teamBooking": false,
        "groupName": "Small",
        "coworkerId": "807938882",
        "coworkerEmail": "test@testemail.com",
        "coworkerFullName": "opportunity Test",
        "coworkerCompanyName": null,
        "private": true,
        "event": false,
        "ignoreTimezone": true
    },
    {
        "id": 917776003,
        "resourceId": 287977692,
        "resourceName": "Thebe Meeting Room",
        "title": "Thebe Meeting Room",
        "start": "2019-02-02T00:00Z",
        "end": "2019-02-02T01:15Z",
        "allDay": false,
        "notes": null,
        "editable": false,
        "teamBooking": false,
        "groupName": "Small",
        "coworkerId": "289024913",
        "coworkerEmail": "carlos+demoaccount01@example.net",
        "coworkerFullName": "Jane Royal",
        "coworkerCompanyName": "Acme Ltd",
        "private": true,
        "event": false,
        "ignoreTimezone": true
    },
    {
        "id": 907073247,
        "resourceId": 287977694,
        "resourceName": "Amalthea Meeting Room",
        "title": "Amalthea Meeting Room",
        "start": "2019-02-06T16:00Z",
        "end": "2019-02-06T17:00Z",
        "allDay": false,
        "notes": "Amalthea Meeting Room",
        "editable": false,
        "teamBooking": false,
        "groupName": "Large",
        "coworkerId": "303913610",
        "coworkerEmail": "demoaccount@nexudus.com",
        "coworkerFullName": "John Doe",
        "coworkerCompanyName": "Landing Limited",
        "private": false,
        "event": false,
        "ignoreTimezone": true
    },
    {
        "id": 907495589,
        "resourceId": 287977694,
        "resourceName": "Amalthea Meeting Room",
        "title": "Amalthea Meeting Room",
        "start": "2019-02-07T02:30Z",
        "end": "2019-02-07T03:30Z",
        "allDay": false,
        "notes": "Amalthea Meeting Room",
        "editable": false,
        "teamBooking": false,
        "groupName": "Large",
        "coworkerId": "303913610",
        "coworkerEmail": "demoaccount@nexudus.com",
        "coworkerFullName": "John Doe",
        "coworkerCompanyName": "Landing Limited",
        "private": false,
        "event": false,
        "ignoreTimezone": true
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/bookings/fullCalendarEvents" %}
{% api-method-summary %}
Events Data
{% endapi-method-summary %}

{% api-method-description %}
Gets events taking place within the passed in date range.
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

{% api-method-query-parameters %}
{% api-method-parameter name="" type="object" required=true %}
Return events starting after the passed in date.
{% endapi-method-parameter %}

{% api-method-parameter name="end" type="object" required=true %}
Return events ending before the passed in date.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
[
    {
        "id": 289121929,
        "resourceId": 287977697,
        "resourceName": "Europa Meeting Room",
        "title": "Pottery workshop",
        "businessName": "Demo Space A",
        "location": null,
        "venueAddress": "1-3 Brixton Road",
        "ticketsPage": null,
        "webAddress": null,
        "start": "2019-01-31T14:57Z",
        "end": "2019-01-31T14:57Z",
        "allDay": false,
        "editable": false,
        "ignoreTimezone": true,
        "event": true,
        "url": "/en/Events/View/289121929/pottery-workshop"
    },
    {
        "id": 931615685,
        "resourceId": 0,
        "resourceName": "",
        "title": "Monday siesta",
        "businessName": "Demo Space A",
        "location": null,
        "venueAddress": "c/ del Pozo, 2",
        "ticketsPage": null,
        "webAddress": null,
        "start": "2019-02-26T00:00Z",
        "end": "2019-02-27T00:00Z",
        "allDay": false,
        "editable": false,
        "ignoreTimezone": true,
        "event": true,
        "url": "/en/Events/View/931615685/monday-siesta"
    },
    {
        "id": 984304372,
        "resourceId": 0,
        "resourceName": "",
        "title": "photoshop",
        "businessName": "Demo Space A",
        "location": null,
        "venueAddress": null,
        "ticketsPage": null,
        "webAddress": null,
        "start": "2019-04-02T14:00Z",
        "end": "2019-04-10T17:00Z",
        "allDay": false,
        "editable": false,
        "ignoreTimezone": true,
        "event": true,
        "url": "/en/Events/View/984304372/photoshop"
    },
    {
        "id": 984925943,
        "resourceId": 0,
        "resourceName": "",
        "title": "Recurrent Event",
        "businessName": "Demo Space A",
        "location": null,
        "venueAddress": null,
        "ticketsPage": null,
        "webAddress": null,
        "start": "2019-04-09T00:59Z",
        "end": "2019-04-10T00:00Z",
        "allDay": false,
        "editable": false,
        "ignoreTimezone": true,
        "event": true,
        "url": "/en/Events/View/984925943/recurrent-event"
    },
    {
        "id": 988902947,
        "resourceId": 0,
        "resourceName": "",
        "title": "Copy of Recurrent Event",
        "businessName": "Demo Space A",
        "location": null,
        "venueAddress": null,
        "ticketsPage": null,
        "webAddress": null,
        "start": "2019-04-09T00:59Z",
        "end": "2019-04-10T00:00Z",
        "allDay": false,
        "editable": false,
        "ignoreTimezone": true,
        "event": true,
        "url": "/en/Events/View/988902947/copy-of-recurrent-event"
    },
    {
        "id": 984925944,
        "resourceId": 0,
        "resourceName": "",
        "title": "Recurrent Event",
        "businessName": "Demo Space A",
        "location": null,
        "venueAddress": null,
        "ticketsPage": null,
        "webAddress": null,
        "start": "2019-04-10T00:59Z",
        "end": "2019-04-11T00:00Z",
        "allDay": false,
        "editable": false,
        "ignoreTimezone": true,
        "event": true,
        "url": "/en/Events/View/984925944/recurrent-event"
    },
    {
        "id": 988902945,
        "resourceId": 0,
        "resourceName": "",
        "title": "Copy of Recurrent Event",
        "businessName": "Demo Space A",
        "location": null,
        "venueAddress": null,
        "ticketsPage": null,
        "webAddress": null,
        "start": "2019-04-10T00:59Z",
        "end": "2019-04-11T00:00Z",
        "allDay": false,
        "editable": false,
        "ignoreTimezone": true,
        "event": true,
        "url": "/en/Events/View/988902945/copy-of-recurrent-event"
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/bookings/search" %}
{% api-method-summary %}
Search
{% endapi-method-summary %}

{% api-method-description %}
Gets resources availability based on a date range and filter criteria.  
  
The available ErrorCodes for the search are.  
  
INVALID\_SHIFT  
NO\_PAST\_BOOKINGS  
HARD\_LIMIT\_WEEK  
HARD\_LIMIT\_MONTH  
INVALID\_TARIFF  
NOT\_AVAILABLE  
START\_TIME\_TOO\_EARLY  
START\_TIME\_TOO\_LATE  
TOO\_LONG  
TOO\_SHORT  
INVALID\_INTERVAL  
NO\_RETURN\_POLICY  
CUSTOM\_MESSAGE
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

{% api-method-query-parameters %}
{% api-method-parameter name="NaturalLight" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Heating" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AirConditioning" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="VoiceRecorder" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CCTV" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SecurityLock" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Drinks" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TeaAndCoffee" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Catering" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="LargeDisplay" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WhiteBoard" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="StandardPhone" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ConferencePhone" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Internet" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Projector" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=false %}
Searches rooms only in the passed in resource type.
{% endapi-method-parameter %}

{% api-method-parameter name="group" type="string" required=false %}
Searches rooms only in the passed in group.
{% endapi-method-parameter %}

{% api-method-parameter name="allocation" type="integer" required=false %}
Minimum capacity for the resources to return.
{% endapi-method-parameter %}

{% api-method-parameter name="start" type="object" required=true %}
Return events starting after the passed in date.
{% endapi-method-parameter %}

{% api-method-parameter name="end" type="object" required=true %}
Return events ending before the passed in date.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "AllShifts": [
        {
            "ResourceId": 922186278,
            "Start": "09:00",
            "End": "18:00",
            "Name": "ALL DAY (9AM - 6PM)"
        },
        {
            "ResourceId": 1021761744,
            "Start": "09:00",
            "End": "18:00",
            "Name": "ALL DAY (9AM - 6PM)"
        }
    ],
    "StartDate": "2019-02-01T00:00:00",
    "EndDate": "2019-02-10T00:00:00",
    "Resources": [
        {
            "Name": "Nexudus Sample Meeting Room",
            "GroupName": null,
            "Description": null,
            "ResourceTypeName": "Hot Desks",
            "ResourceType": {},
            "HasImage": true,
            "Projector": false,
            "Internet": false,
            "ConferencePhone": false,
            "StandardPhone": false,
            "WhiteBoard": false,
            "LargeDisplay": false,
            "Catering": false,
            "TeaAndCoffee": false,
            "Drinks": false,
            "SecurityLock": false,
            "CCTV": false,
            "VoiceRecorder": false,
            "AirConditioning": false,
            "Heating": false,
            "NaturalLight": false,
            "AllowMultipleBookings": false,
            "Allocation": 5,
            "Shifts": [
                {}
            ],
            "IsAvailable": false,
            "AvailableUnits": 1,
            "Message": "This resource can only be booked in the following shifts: ALL DAY (9AM - 6PM).",
            "Price": -1,
            "DisplayOrder": 0,
            "PriceFormatted": "£-1.00",
            "ErrorCode": "INVALID_SHIFT",
            "Id": 922186278,
            "IdString": "922186278",
            "UpdatedOn": "2019-05-10T15:56:38",
            "CreatedOn": "2019-02-20T15:15:05",
            "UniqueId": "5f96ea9d-6c73-4b5b-93f0-7569f52806ec",
            "IsNull": false
        },
        {
            "Name": "Day Room ",
            "GroupName": null,
            "Description": null,
            "ResourceTypeName": "Day room ",
            "ResourceType": {},
            "HasImage": true,
            "Projector": false,
            "Internet": false,
            "ConferencePhone": false,
            "StandardPhone": false,
            "WhiteBoard": false,
            "LargeDisplay": false,
            "Catering": false,
            "TeaAndCoffee": false,
            "Drinks": false,
            "SecurityLock": false,
            "CCTV": false,
            "VoiceRecorder": false,
            "AirConditioning": false,
            "Heating": false,
            "NaturalLight": false,
            "AllowMultipleBookings": false,
            "Allocation": null,
            "Shifts": [
                {}
            ],
            "IsAvailable": false,
            "AvailableUnits": 1,
            "Message": "This resource can only be booked in the following shifts: ALL DAY (9AM - 6PM).",
            "Price": -1,
            "DisplayOrder": 0,
            "PriceFormatted": "£-1.00",
            "ErrorCode": "INVALID_SHIFT",
            "Id": 1021761744,
            "IdString": "1021761744",
            "UpdatedOn": "2019-05-14T12:52:13",
            "CreatedOn": "2019-05-10T14:58:13",
            "UniqueId": "13a97016-3260-4f62-8abb-dc010e47558d",
            "IsNull": false
        },
        {
            "Name": "Thebe Meeting Room",
            "GroupName": "Small",
            "Description": "<p>This meeting room includes:</p>\r\n<ul>\r\n<li>Projector</li>\r\n<li>Conference phone</li>\r\n<li>Catering</li>\r\n<li>Coffee and Tea</li>\r\n<li>A/A</li>\r\n</ul>\r\n<p>Capacity <strong>10 people</strong>.</p>\r\n<p> </p>\r\n<p>\"Bookings with MyOffice 985 are non-refundable but may be converted to credits if changes to bookings must be made. This will be handled on a case-by-case basis. Please call for details.\"</p>",
            "ResourceTypeName": "Large Meeting Rooms (hourly)",
            "ResourceType": {},
            "HasImage": true,
            "Projector": true,
            "Internet": true,
            "ConferencePhone": true,
            "StandardPhone": false,
            "WhiteBoard": false,
            "LargeDisplay": false,
            "Catering": true,
            "TeaAndCoffee": true,
            "Drinks": false,
            "SecurityLock": false,
            "CCTV": false,
            "VoiceRecorder": false,
            "AirConditioning": false,
            "Heating": false,
            "NaturalLight": false,
            "AllowMultipleBookings": false,
            "Allocation": null,
            "Shifts": [],
            "IsAvailable": false,
            "AvailableUnits": 1,
            "Message": "This resource is already booked. Please choose a different start and end times.",
            "Price": -1,
            "DisplayOrder": 1,
            "PriceFormatted": "£-1.00",
            "ErrorCode": "BOOKING_CONFLICT",
            "Id": 287977692,
            "IdString": "287977692",
            "UpdatedOn": "2019-05-14T00:34:19",
            "CreatedOn": "2017-01-27T15:30:07",
            "UniqueId": "e9180734-9a34-4429-9346-47af763532c3",
            "IsNull": false
        },
        {
            "Name": "Callisto Meeting Room",
            "GroupName": "Small",
            "Description": "<p>GGo to this link for buying <a href=\"http://demoaccount.spaces.nexudus.com/en#products\">credits</a></p>\r\n<p> </p>\r\n<p>This meeting room includes:</p>\r\n<ul>\r\n<li>Projector</li>\r\n<li>Conference phone</li>\r\n<li>Catering</li>\r\n<li>Coffee and Tea</li>\r\n<li>Audio System</li>\r\n<li>WiFi</li>\r\n<li>Whiteboard</li>\r\n<li>Lock</li>\r\n<li>A/A</li>\r\n</ul>\r\n<p>Capacity <strong>12 people.</strong></p>",
            "ResourceTypeName": "Small Meeting Rooms (hourly)",
            "ResourceType": {},
            "HasImage": true,
            "Projector": true,
            "Internet": false,
            "ConferencePhone": true,
            "StandardPhone": false,
            "WhiteBoard": false,
            "LargeDisplay": false,
            "Catering": true,
            "TeaAndCoffee": true,
            "Drinks": false,
            "SecurityLock": true,
            "CCTV": false,
            "VoiceRecorder": false,
            "AirConditioning": true,
            "Heating": true,
            "NaturalLight": false,
            "AllowMultipleBookings": false,
            "Allocation": 8,
            "Shifts": [],
            "IsAvailable": false,
            "AvailableUnits": 1,
            "Message": "This resource is already booked. Please choose a different start and end times.",
            "Price": -1,
            "DisplayOrder": 2,
            "PriceFormatted": "£-1.00",
            "ErrorCode": "BOOKING_CONFLICT",
            "Id": 287977693,
            "IdString": "287977693",
            "UpdatedOn": "2019-05-16T11:38:39",
            "CreatedOn": "2017-01-27T15:41:32",
            "UniqueId": "2984f460-df71-415c-b25d-6d1200c3dfcd",
            "IsNull": false
        },
        {
            "Name": "Amalthea Meeting Room",
            "GroupName": "Large",
            "Description": "<p>This meeting room includes:</p>\r\n<ul>\r\n<li>Projector</li>\r\n<li>Conference phone</li>\r\n<li>Catering</li>\r\n<li>Coffee and Tea</li>\r\n<li>Audio System</li>\r\n<li>WiFi</li>\r\n<li>Whiteboard</li>\r\n</ul>\r\n<p>Capacity <strong>8 people.</strong></p>",
            "ResourceTypeName": "Large Meeting Rooms (hourly)",
            "ResourceType": {},
            "HasImage": true,
            "Projector": true,
            "Internet": true,
            "ConferencePhone": true,
            "StandardPhone": false,
            "WhiteBoard": true,
            "LargeDisplay": false,
            "Catering": true,
            "TeaAndCoffee": true,
            "Drinks": false,
            "SecurityLock": false,
            "CCTV": false,
            "VoiceRecorder": false,
            "AirConditioning": true,
            "Heating": false,
            "NaturalLight": false,
            "AllowMultipleBookings": false,
            "Allocation": 45,
            "Shifts": [],
            "IsAvailable": false,
            "AvailableUnits": 1,
            "Message": "This resource is already booked. Please choose a different start and end times.",
            "Price": -1,
            "DisplayOrder": 3,
            "PriceFormatted": "£-1.00",
            "ErrorCode": "BOOKING_CONFLICT",
            "Id": 287977694,
            "IdString": "287977694",
            "UpdatedOn": "2019-05-16T11:30:38",
            "CreatedOn": "2017-01-27T15:44:28",
            "UniqueId": "84bf8746-0a96-451e-a820-b1db0a2c0392",
            "IsNull": false
        }
    ],
    "SearchFields": [
        "Projector",
        "Internet",
        "ConferencePhone",
        "StandardPhone",
        "WhiteBoard",
        "LargeDisplay",
        "Catering",
        "TeaAndCoffee",
        "Drinks",
        "SecurityLock",
        "CCTV",
        "VoiceRecorder",
        "AirConditioning",
        "Heating",
        "NaturalLight"
    ],
    "SelectedTypes": null,
    "Group": null,
    "ChargeBooingImmediately": false,
    "ResourceTypes": [
        {
            "Name": "Hot Desks",
            "Id": 539169648,
            "IdString": "539169648",
            "UpdatedOn": "2018-01-24T05:40:09",
            "CreatedOn": "2018-01-24T05:40:09",
            "UniqueId": "3678b774-bc59-40be-b739-c2e97c7bce97",
            "IsNull": false
        },
        {
            "Name": "Day room ",
            "Id": 1021660649,
            "IdString": "1021660649",
            "UpdatedOn": "2019-05-10T14:57:39",
            "CreatedOn": "2019-05-10T14:57:39",
            "UniqueId": "d06f8410-710f-4680-bcaf-952afe1ac894",
            "IsNull": false
        },
        {
            "Name": "Large Meeting Rooms (hourly)",
            "Id": 287951665,
            "IdString": "287951665",
            "UpdatedOn": "2017-01-27T10:30:17",
            "CreatedOn": "2017-01-27T10:30:17",
            "UniqueId": "0e841048-d59f-421d-bf3f-5fd5e5422eef",
            "IsNull": false
        },
        {
            "Name": "Small Meeting Rooms (hourly)",
            "Id": 287951666,
            "IdString": "287951666",
            "UpdatedOn": "2017-01-27T10:30:17",
            "CreatedOn": "2017-01-27T10:30:17",
            "UniqueId": "4ddd9975-0862-4a64-97b3-3995d7a33e42",
            "IsNull": false
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://xyz.spaces.nexudus.com" path="/:language/bookings/getbookingprice" %}
{% api-method-summary %}
Booking Cost
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="langugage" type="string" required=true %}
'en' or any other valid langauge in your account
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=true %}
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
    "Resource": {
        "Name": "Thebe Meeting Room",
        "GroupName": "Small",
        "Description": "<p>This meeting room includes:</p>\r\n<ul>\r\n<li>Projector</li>\r\n<li>Conference phone</li>\r\n<li>Catering</li>\r\n<li>Coffee and Tea</li>\r\n<li>A/A</li>\r\n</ul>\r\n<p>Capacity <strong>10 people</strong>.</p>\r\n<p>&nbsp;</p>\r\n<p>\"Bookings with MyOffice 985 are non-refundable but may be converted to credits if changes to bookings must be made. This will be handled on a case-by-case basis. Please call for details.\"</p>",
        "ResourceTypeName": "Large Meeting Rooms (hourly)",
        "ResourceType": {
            "Name": "Large Meeting Rooms (hourly)",
            "Id": 287951665,
            "IdString": "287951665",
            "UpdatedOn": "2017-01-27T10:30:17Z",
            "CreatedOn": "2017-01-27T10:30:17Z",
            "UniqueId": "0e841048-d59f-421d-bf3f-5fd5e5422eef",
            "IsNull": false,
            "Context": null
        },
        "HasImage": true,
        "Projector": true,
        "Internet": true,
        "ConferencePhone": true,
        "StandardPhone": false,
        "WhiteBoard": false,
        "LargeDisplay": false,
        "Catering": true,
        "TeaAndCoffee": true,
        "Drinks": false,
        "SecurityLock": false,
        "CCTV": false,
        "VoiceRecorder": false,
        "AirConditioning": false,
        "Heating": false,
        "NaturalLight": false,
        "AllowMultipleBookings": false,
        "Allocation": null,
        "Shifts": [],
        "IsAvailable": false,
        "AvailableUnits": 0,
        "Message": null,
        "Price": 0,
        "DisplayOrder": 1,
        "PriceFormatted": null,
        "ErrorCode": null,
        "Id": 287977692,
        "IdString": "287977692",
        "UpdatedOn": "2019-05-14T00:34:19Z",
        "CreatedOn": "2017-01-27T15:30:07Z",
        "UniqueId": "e9180734-9a34-4429-9346-47af763532c3",
        "IsNull": false,
        "Context": null
    },
    "IsAvailable": true | false,
    "Message": null,
    "Price": "£97.83",
    "PriceDecimal": 97.8261,
    "discountCode": {
        "discountMessage": null,
        "code": null,
        "description": null
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Request Body:**

```javascript
{  
   "Booking":{  
      "Resource":{  
         "Id":287977692
      },
      "Tentative":false,
	   "Id":0,
	   "DiscountCode": null,
	   "FromTime":"2019-06-13T20:30Z",
	   "ToTime":"2019-06-13T22:00Z"
   },
   "Coworker":{  
      "FullName":"John Doe",
      "Email":"dasd@asdasd.com",
      "MobilePhone":"+1 555 555 555",
      "Address":"London Road",
      "PostCode":"90210",
      "CityName":"Los Angeles",
      "State":"California"
   },
   "Products":[  
      {  
         "ProductId":294480188,
         "Quantity":0,
         "Selected":true
      }
   ]
}
```

**Error Codes**

**NO\_RESOURCE  
NOT\_REGISTERED  
BOOKING\_CONFLICT  
EVENT\_CONFLICT  
RESOURCE\_FULL  
INVALID\_SHIFT  
NO\_PAST\_BOOKINGS  
HARD\_LIMIT\_WEEK  
HARD\_LIMIT\_MONTH  
START\_TIME\_TOO\_EARLY  
START\_TIME\_TOO\_LATE  
TOO\_LONG  
TOO\_SHORT  
INVALID\_INTERVAL**

{% api-method method="post" host="https://xyz.spaces.nexudus.com" path="/:language/bookings/newBookingJson" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a booking.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="langugage" type="string" required=true %}
'en' or any other valid language in your account.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Base64-encoding email:password
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=false %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

#### Request Body \(logged in customer\):

```javascript
{  
   "Booking":{  
      "Resource":{  
         "Id":287977692
      },
      "Tentative":false,
      "Id":0,
      "FromTime":"2019-05-27T21:30Z",
      "ToTime":"2019-05-27T22:30Z",
      "BookingVisitors":[  

      ]
   },

   "Products":[  
      {  
         "ProductId":294480188,
         "Quantity":"5",
         "Selected":true
      },
      {  
         "ProductId":392619261,
         "Quantity":"1",
         "Selected":true
      },
      {  
         "ProductId":583752071,
         "Quantity":"0",
         "Selected":false
      }
   ]
}
```

#### Request Body \(new customer\):

```javascript
{  
   "Booking":{  
      "Resource":{  
         "Id":287977692
      },
      "Tentative":false,
      "Id":0,
      "FromTime":"2019-05-27T21:30Z",
      "ToTime":"2019-05-28T00:30Z",
      "BookingVisitors":[  

      ]
   },
   "Coworker":{  
      "FullName":"John Doe",
      "Email":"john.doe.123@example.net",
      "MobilePhone":"555-555-555",
      "Address":"London Road",
      "PostCode":"L123456",
      "CityName":"London",
      "State":"London",
      "TaxIDNumber":"VAT00001",
      "BillingEmail":"finance@example.net",
   },
   "Products":[  
      {  
         "ProductId":294480188,
         "Quantity":"0",
         "Selected":false
      },
      {  
         "ProductId":392619261,
         "Quantity":"0",
         "Selected":false
      },
      {  
         "ProductId":583752071,
         "Quantity":"0",
         "Selected":false
      }
   ]
}
```

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/bookings/:id" %}
{% api-method-summary %}
Get One
{% endapi-method-summary %}

{% api-method-description %}
Gets events taking place within the passed in date range.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="langugage" type="string" required=true %}
'en' or any other valid language in your account.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Base64-encoded email:password
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=false %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the booking to get.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{  
   "Value":{  
      "ResourceId":287977694,
      "ResourceName":"Amalthea Meeting Room",
      "ResourceHideInCalendar":false,
      "CoworkerId":289024940,
      "CoworkerFullName":"David Hoch",
      "ExtraServiceId":0,
      "ExtraServiceName":null,
      "FromTime":"2019-05-28T12:30:00Z",
      "ToTime":"2019-05-28T14:00:00Z",
      "Notes":null,
      "InternalNotes":null,
      "ChargeNow":false,
      "InvoiceNow":false,
      "DoNotUseBookingCredit":false,
      "PurchaseOrder":null,
      "DiscountCode":null,
      "Tentative":false,
      "Online":true,
      "TeamsAtTheTimeOfBooking":"Infinity",
      "TariffAtTheTimeOfBooking":"24/7 Space Membership, 24/7 Space Membership, Virtual membership",
      "RepeatSeriesUniqueId":null,
      "RepeatBooking":false,
      "Repeats":0,
      "WhichBookingsToUpdate":0,
      "RepeatEvery":null,
      "RepeatUntil":null,
      "RepeatOnMondays":false,
      "RepeatOnTuesdays":false,
      "RepeatOnWednesdays":false,
      "RepeatOnThursdays":false,
      "RepeatOnFridays":false,
      "RepeatOnSaturdays":false,
      "RepeatOnSundays":false,
      "Invoiced":true,
      "InvoiceDate":"2019-05-27T19:23:03Z",
      "CoworkerInvoiceId":null,
      "CoworkerInvoiceNumber":null,
      "CoworkerInvoicePaid":false,
      "CoworkerExtraServiceIds":null,
      "CoworkerExtraServicePrice":null,
      "CoworkerExtraServiceCurrencyCode":null,
      "CoworkerExtraServiceChargePeriod":null,
      "CoworkerExtraServiceTotalUses":null,
      "CoworkerBillingName":"David Hoch",
      "MinutesToStart":1026,
      "OverrideResourceLimits":false,
      "DisableConfirmation":false,
      "SkipGoogleCalendarUpdate":false,
      "OverridePrice":null,
      "EstimatedCost":null,
      "EstimagedCost":null,
      "ChargedExtraServices":null,
      "BookingProducts":null,
      "BookingVisitors":[  

      ],
      "EstimatedExtraService":null,
      "Invoice":null,
      "AvailableCredit":0.0,
      "IsEvent":false,
      "IsTour":false,
      "DiscountAmount":null,
      "Id":1040617591,
      "UpdatedOn":"2019-05-27T19:23:04Z",
      "CreatedOn":"2019-05-27T19:23:03Z",
      "UniqueId":"256f955d-1676-4cb4-8c1f-f21c9669f28b",
      "UpdatedBy":"david@example.net",
      "IsNew":false,
      "SystemId":null,
      "ToStringText":"Amalthea Meeting Room",
      "LocalizationDetails":null
   },
   "Resource":{  
      "Name":"Amalthea Meeting Room",
      "GroupName":"Large",
      "Description":"<p>This meeting room includes:</p>\r\n<ul>\r\n<li>Projector</li>\r\n<li>Conference phone</li>\r\n<li>Catering</li>\r\n<li>Coffee and Tea</li>\r\n<li>Audio System</li>\r\n<li>WiFi</li>\r\n<li>Whiteboard</li>\r\n</ul>\r\n<p>Capacity <strong>8 people.</strong></p>",
      "ResourceTypeName":"Large Meeting Rooms (hourly)",
      "ResourceType":{  
         "Name":"Large Meeting Rooms (hourly)",
         "Id":287951665,
         "IdString":"287951665",
         "UpdatedOn":"2017-01-27T10:30:17Z",
         "CreatedOn":"2017-01-27T10:30:17Z",
         "UniqueId":"0e841048-d59f-421d-bf3f-5fd5e5422eef",
         "IsNull":false,
         "Context":null
      },
      "HasImage":true,
      "Projector":true,
      "Internet":true,
      "ConferencePhone":true,
      "StandardPhone":false,
      "WhiteBoard":true,
      "LargeDisplay":false,
      "Catering":true,
      "TeaAndCoffee":true,
      "Drinks":false,
      "SecurityLock":false,
      "CCTV":false,
      "VoiceRecorder":false,
      "AirConditioning":true,
      "Heating":false,
      "NaturalLight":false,
      "AllowMultipleBookings":false,
      "Allocation":45,
      "Shifts":[  

      ],
      "IsAvailable":false,
      "AvailableUnits":0,
      "Message":null,
      "Price":0.0,
      "DisplayOrder":3,
      "PriceFormatted":null,
      "ErrorCode":null,
      "Id":287977694,
      "IdString":"287977694",
      "UpdatedOn":"2019-05-16T11:30:38Z",
      "CreatedOn":"2017-01-27T15:44:28Z",
      "UniqueId":"84bf8746-0a96-451e-a820-b1db0a2c0392",
      "IsNull":false,
      "Context":null
   }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://xyz.spaces.nexudus.com" path="/:language/bookings" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Gets events taking place within the passed in date range.  
  
Note this is a **POST** request.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="langugage" type="string" required=true %}
'en' or any other valid language in your account.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Base64-encoded email:password
{% endapi-method-parameter %}

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
// When saved correctly
{  
   "Status":200,
   "Message":"Your booking has been updated",
   "Value":null,
   "OpenInDialog":false,
   "OpenInWindow":false,
   "RedirectURL":null,
   "JavaScript":null,
   "UpdatedOn":null,
   "UpdatedBy":null,
   "Errors":null,
   "WasSuccessful":true
}

//When could not save:
{  
   "Status":500,
   "Message":"This resource is not available to be booked at this time. Please choose other start and end times for the booking.",
   "Value":null,
   "OpenInDialog":false,
   "OpenInWindow":false,
   "RedirectURL":null,
   "JavaScript":null,
   "UpdatedOn":null,
   "UpdatedBy":null,
   "Errors":null,
   "WasSuccessful":false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

#### Request Body

```javascript
{  
   "Booking":{  
      "Notes":null,
      "Resource":{  
         "Id":287977694
      },
      "Tentative":false,
      "Id":1040617591,
      "FromTime":"2019-05-28T01:00Z",
      "ToTime":"2019-05-28T02:30Z",
      "BookingVisitors":[  

      ]
   },
   "Products":[  
      {  
         "ProductId":294480188,
         "Quantity":"0",
         "Selected":false
      },
      {  
         "ProductId":583752071,
         "Quantity":"0",
         "Selected":false
      },
      {  
         "ProductId":583751168,
         "Quantity":"0",
         "Selected":false
      }
   ]
}
```

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/bookings/deleteJson/:id" %}
{% api-method-summary %}
Delete One
{% endapi-method-summary %}

{% api-method-description %}
Deletes a booking
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="langugage" type="string" required=true %}
'en' or any other valid language in your account.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Base64-encoded email:password
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=false %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the booking to delete.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
//If the booking could be deleted
{  
   "Status":200,
   "Message":"Booking was successfully deleted.",
   "Value":null,
   "OpenInDialog":false,
   "OpenInWindow":false,
   "RedirectURL":null,
   "JavaScript":null,
   "UpdatedOn":null,
   "UpdatedBy":null,
   "Errors":null,
   "WasSuccessful":true
}

//When the booking could not be deleted:
{  
   "Status":500,
   "Message":"This booking has already been invoiced.",
   "Value":null,
   "OpenInDialog":false,
   "OpenInWindow":false,
   "RedirectURL":null,
   "JavaScript":null,
   "UpdatedOn":null,
   "UpdatedBy":null,
   "Errors":null,
   "WasSuccessful":false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/bookings/pay" %}
{% api-method-summary %}
Invoice Bookings
{% endapi-method-summary %}

{% api-method-description %}
Creates an invoice for any unpaid bookings.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="langugage" type="string" required=true %}
'en' or any other valid language in your account.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Base64-encoded email:password
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=false %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



