{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/calendarevents" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of calendarevents based on one or more filter querystring parameters.
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
?CalendarEvent\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="Business" type="Business" %}
?CalendarEvent\_Business=...
{% endapi-method-parameter %}


{% api-method-parameter name="Name" type="string" %}
?CalendarEvent\_Name=...
{% endapi-method-parameter %}


{% api-method-parameter name="ShortDescription" type="string" %}
?CalendarEvent\_ShortDescription=...
{% endapi-method-parameter %}


{% api-method-parameter name="LongDescription" type="string" %}
?CalendarEvent\_LongDescription=...
{% endapi-method-parameter %}


{% api-method-parameter name="TicketNotes" type="string" %}
?CalendarEvent\_TicketNotes=...
{% endapi-method-parameter %}


{% api-method-parameter name="AskBuyerAddress" type="bool" %}
?CalendarEvent\_AskBuyerAddress=...
{% endapi-method-parameter %}


{% api-method-parameter name="ShowEventAttendees" type="bool" %}
?CalendarEvent\_ShowEventAttendees=...
{% endapi-method-parameter %}


{% api-method-parameter name="Location" type="string" %}
?CalendarEvent\_Location=...
{% endapi-method-parameter %}


{% api-method-parameter name="VenueAddress" type="string" %}
?CalendarEvent\_VenueAddress=...
{% endapi-method-parameter %}


{% api-method-parameter name="Resource" type="Resource" %}
?CalendarEvent\_Resource=...
{% endapi-method-parameter %}


{% api-method-parameter name="StartDate" type="DateTime" %}
?CalendarEvent\_StartDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="EndDate" type="DateTime" %}
?CalendarEvent\_EndDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="Allocation" type="int?" %}
?CalendarEvent\_Allocation=...
{% endapi-method-parameter %}


{% api-method-parameter name="PublishDate" type="DateTime?" %}
?CalendarEvent\_PublishDate=...
{% endapi-method-parameter %}


{% api-method-parameter name="ShowInHomeBanner" type="bool" %}
?CalendarEvent\_ShowInHomeBanner=...
{% endapi-method-parameter %}


{% api-method-parameter name="ShowInHomePage" type="bool" %}
?CalendarEvent\_ShowInHomePage=...
{% endapi-method-parameter %}


{% api-method-parameter name="AllowComments" type="bool" %}
?CalendarEvent\_AllowComments=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnlyForContacts" type="bool" %}
?CalendarEvent\_OnlyForContacts=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnlyForMembers" type="bool" %}
?CalendarEvent\_OnlyForMembers=...
{% endapi-method-parameter %}


{% api-method-parameter name="WebAddress" type="string" %}
?CalendarEvent\_WebAddress=...
{% endapi-method-parameter %}


{% api-method-parameter name="FacebookPage" type="string" %}
?CalendarEvent\_FacebookPage=...
{% endapi-method-parameter %}


{% api-method-parameter name="TicketsPage" type="string" %}
?CalendarEvent\_TicketsPage=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatSeriesUniqueId" type="Guid?" %}
?CalendarEvent\_RepeatSeriesUniqueId=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatEvent" type="bool" %}
?CalendarEvent\_RepeatEvent=...
{% endapi-method-parameter %}


{% api-method-parameter name="Repeats" type="enum" %}
?CalendarEvent\_Repeats=...
{% endapi-method-parameter %}


{% api-method-parameter name="WhichEventsToUpdate" type="enum" %}
?CalendarEvent\_WhichEventsToUpdate=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatEvery" type="int?" %}
?CalendarEvent\_RepeatEvery=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatUntil" type="DateTime?" %}
?CalendarEvent\_RepeatUntil=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatOnMondays" type="bool" %}
?CalendarEvent\_RepeatOnMondays=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatOnTuesdays" type="bool" %}
?CalendarEvent\_RepeatOnTuesdays=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatOnWednesdays" type="bool" %}
?CalendarEvent\_RepeatOnWednesdays=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatOnThursdays" type="bool" %}
?CalendarEvent\_RepeatOnThursdays=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatOnFridays" type="bool" %}
?CalendarEvent\_RepeatOnFridays=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatOnSaturdays" type="bool" %}
?CalendarEvent\_RepeatOnSaturdays=...
{% endapi-method-parameter %}


{% api-method-parameter name="RepeatOnSundays" type="bool" %}
?CalendarEvent\_RepeatOnSundays=...
{% endapi-method-parameter %}

{% api-method-parameter name="EventCategories" type="int" required=false %}
?CalendarEvent\_EventCategories=...
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
        "ShortDescription": "Description",
        "LongDescription": "Description",
        "TicketNotes": "TicketNotes",
        "AskBuyerAddress": ask buyer address,
        "ShowEventAttendees": show event attendees,
        "Location": "Location",
        "VenueAddress": "Location",
        "Resource": null,
        "StartDate": DateTime.Parse("2001-01-01"),
        "EndDate": DateTime.Parse("2001-01-01"),
        "Allocation": 0,
        "PublishDate": null,
        "ShowInHomeBanner": true,
        "ShowInHomePage": true,
        "AllowComments": true,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "WebAddress": "WebAddress",
        "FacebookPage": "TicketsPage",
        "TicketsPage": "TicketsPage",
        "RepeatSeriesUniqueId": ,
        "RepeatEvent": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eCalendarEventRepeatCycle.Weekly,
        "WhichEventsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedCalendarEventUpdateAction.UpdateThisEventOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
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

> 🔒 Requires user role `calendarevent-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/calendarevents" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of calendarevents.
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
        "ShortDescription": "Description",
        "LongDescription": "Description",
        "TicketNotes": "TicketNotes",
        "AskBuyerAddress": ask buyer address,
        "ShowEventAttendees": show event attendees,
        "Location": "Location",
        "VenueAddress": "Location",
        "Resource": null,
        "StartDate": DateTime.Parse("2001-01-01"),
        "EndDate": DateTime.Parse("2001-01-01"),
        "Allocation": 0,
        "PublishDate": null,
        "ShowInHomeBanner": true,
        "ShowInHomePage": true,
        "AllowComments": true,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "WebAddress": "WebAddress",
        "FacebookPage": "TicketsPage",
        "TicketsPage": "TicketsPage",
        "RepeatSeriesUniqueId": ,
        "RepeatEvent": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eCalendarEventRepeatCycle.Weekly,
        "WhichEventsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedCalendarEventUpdateAction.UpdateThisEventOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
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

> 🔒 Requires user role `calendarevent-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/calendarevents" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of calendarevents based on the date when they were created or updated.
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
?to\_CalendarEvent\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_CalendarEvent\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_CalendarEvent\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_CalendarEvent\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="StartDate" type="datetime" required=false %}
?from\_CalendarEvent\_StartDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="StartDate" type="datetime" required=false %}
?to\_CalendarEvent\_StartDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="EndDate" type="datetime" required=false %}
?from\_CalendarEvent\_EndDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="EndDate" type="datetime" required=false %}
?to\_CalendarEvent\_EndDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="Allocation" type="int" required=false %}
?from\_CalendarEvent\_Allocation=...
{% endapi-method-parameter %}
{% api-method-parameter name="Allocation" type="int" required=false %}
?to\_CalendarEvent\_Allocation=...
{% endapi-method-parameter %}
{% api-method-parameter name="PublishDate" type="datetime" required=false %}
?from\_CalendarEvent\_PublishDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="PublishDate" type="datetime" required=false %}
?to\_CalendarEvent\_PublishDate=...
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatEvery" type="int" required=false %}
?from\_CalendarEvent\_RepeatEvery=...
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatEvery" type="int" required=false %}
?to\_CalendarEvent\_RepeatEvery=...
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatUntil" type="datetime" required=false %}
?from\_CalendarEvent\_RepeatUntil=...
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatUntil" type="datetime" required=false %}
?to\_CalendarEvent\_RepeatUntil=...
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
        "ShortDescription": "Description",
        "LongDescription": "Description",
        "TicketNotes": "TicketNotes",
        "AskBuyerAddress": ask buyer address,
        "ShowEventAttendees": show event attendees,
        "Location": "Location",
        "VenueAddress": "Location",
        "Resource": null,
        "StartDate": DateTime.Parse("2001-01-01"),
        "EndDate": DateTime.Parse("2001-01-01"),
        "Allocation": 0,
        "PublishDate": null,
        "ShowInHomeBanner": true,
        "ShowInHomePage": true,
        "AllowComments": true,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "WebAddress": "WebAddress",
        "FacebookPage": "TicketsPage",
        "TicketsPage": "TicketsPage",
        "RepeatSeriesUniqueId": ,
        "RepeatEvent": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eCalendarEventRepeatCycle.Weekly,
        "WhichEventsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedCalendarEventUpdateAction.UpdateThisEventOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
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

> 🔒 Requires user role `calendarevent-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/calendarevents/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one calendarevent record.
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
The ID of the calendarevent to fetch.
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
        "ShortDescription": "Description",
        "LongDescription": "Description",
        "TicketNotes": "TicketNotes",
        "AskBuyerAddress": ask buyer address,
        "ShowEventAttendees": show event attendees,
        "Location": "Location",
        "VenueAddress": "Location",
        "Resource": null,
        "StartDate": DateTime.Parse("2001-01-01"),
        "EndDate": DateTime.Parse("2001-01-01"),
        "Allocation": 0,
        "PublishDate": null,
        "ShowInHomeBanner": true,
        "ShowInHomePage": true,
        "AllowComments": true,
        "OnlyForContacts": true,
        "OnlyForMembers": true,
        "WebAddress": "WebAddress",
        "FacebookPage": "TicketsPage",
        "TicketsPage": "TicketsPage",
        "RepeatSeriesUniqueId": ,
        "RepeatEvent": false,
        "Repeats": Nexudus.Coworking.Core.Enums.eCalendarEventRepeatCycle.Weekly,
        "WhichEventsToUpdate": Nexudus.Coworking.Core.Enums.eRepeatedCalendarEventUpdateAction.UpdateThisEventOnly,
        "RepeatEvery": ,
        "RepeatUntil": ,
        "RepeatOnMondays": false,
        "RepeatOnTuesdays": false,
        "RepeatOnWednesdays": false,
        "RepeatOnThursdays": false,
        "RepeatOnFridays": false,
        "RepeatOnSaturdays": false,
        "RepeatOnSundays": false,
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

> 🔒 Requires user role `calendarevent-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/content/calendarevents" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new calendarevent.
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
{% api-method-parameter name="ShortDescription" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="LongDescription" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TicketNotes" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AskBuyerAddress" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShowEventAttendees" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Location" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="VenueAddress" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ResourceId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="StartDate" type="DateTime" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="EndDate" type="DateTime" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Allocation" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PublishDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShowInHomeBanner" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShowInHomePage" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AllowComments" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnlyForContacts" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnlyForMembers" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="WebAddress" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FacebookPage" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TicketsPage" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatSeriesUniqueId" type="Guid?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatEvent" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Repeats" type="enum" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="WhichEventsToUpdate" type="enum" required=false %}
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

> 🔒 Requires user role `calendarevent-create`

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/content/calendarevents" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing calendarevent.
  
Required User Role: `calendarevent-edit`
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
The id of the calendarevent to update
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="BusinessId" type="int" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Name" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShortDescription" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="LongDescription" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TicketNotes" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AskBuyerAddress" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShowEventAttendees" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Location" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="VenueAddress" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ResourceId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="StartDate" type="DateTime" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="EndDate" type="DateTime" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Allocation" type="int?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PublishDate" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShowInHomeBanner" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ShowInHomePage" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AllowComments" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnlyForContacts" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnlyForMembers" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="WebAddress" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="FacebookPage" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="TicketsPage" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RepeatSeriesUniqueId" type="Guid?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Repeats" type="enum" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="WhichEventsToUpdate" type="enum" required=false %}
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

> 🔒 Requires user role `calendarevent-edit`


{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/content/calendarevents/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a calendarevent.  
  
Required User Roles: `calendarevent-delete`
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



> 🔒 Requires user role `calendarevent-delete`


## Commands

Commands allow to perform actions against one or more calendarevent records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/calendarevents/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for calendarevent records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/calendarevents/runcommand" %}
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

> 🔒 Requires user role `calendarevent-edit`

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/calendarevents/getsmalllogo/:id" %}
{% api-method-summary %}
SmallLogo
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
The id of the CalendarEvent to get the smalllogo for.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/content/calendarevents/getlargelogo/:id" %}
{% api-method-summary %}
LargeLogo
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
The id of the CalendarEvent to get the largelogo for.
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
* [Resource](../spaces/resource.md)
