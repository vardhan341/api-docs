{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/users" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of users based on one or more filter querystring parameters.
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
?User\_SystemId=...
{% endapi-method-parameter %}


{% api-method-parameter name="FullName" type="string" %}
?User\_FullName=...
{% endapi-method-parameter %}


{% api-method-parameter name="Email" type="string" %}
?User\_Email=...
{% endapi-method-parameter %}


{% api-method-parameter name="AccessToken" type="string" %}
?User\_AccessToken=...
{% endapi-method-parameter %}


{% api-method-parameter name="PreferredLanguage" type="Language" %}
?User\_PreferredLanguage=...
{% endapi-method-parameter %}


{% api-method-parameter name="NewPassword" type="string" %}
?User\_NewPassword=...
{% endapi-method-parameter %}


{% api-method-parameter name="PassportNumber" type="string" %}
?User\_PassportNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="PassportCardNumber" type="string" %}
?User\_PassportCardNumber=...
{% endapi-method-parameter %}


{% api-method-parameter name="EnablePassportAccess" type="bool" %}
?User\_EnablePassportAccess=...
{% endapi-method-parameter %}


{% api-method-parameter name="Active" type="bool" %}
?User\_Active=...
{% endapi-method-parameter %}


{% api-method-parameter name="IsAdmin" type="bool" %}
?User\_IsAdmin=...
{% endapi-method-parameter %}


{% api-method-parameter name="APIAccess" type="bool" %}
?User\_APIAccess=...
{% endapi-method-parameter %}


{% api-method-parameter name="Validated" type="bool" %}
?User\_Validated=...
{% endapi-method-parameter %}


{% api-method-parameter name="MustResetPassword" type="bool" %}
?User\_MustResetPassword=...
{% endapi-method-parameter %}


{% api-method-parameter name="LastAccess" type="DateTime?" %}
?User\_LastAccess=...
{% endapi-method-parameter %}


{% api-method-parameter name="Devices" type="string" %}
?User\_Devices=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnNewEmail" type="bool" %}
?User\_OnNewEmail=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnHelpDeskMsg" type="bool" %}
?User\_OnHelpDeskMsg=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnNewWallPost" type="bool" %}
?User\_OnNewWallPost=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnNewMember" type="bool" %}
?User\_OnNewMember=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnProfileChanges" type="bool" %}
?User\_OnProfileChanges=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnNewBlogComment" type="bool" %}
?User\_OnNewBlogComment=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnNewEventComment" type="bool" %}
?User\_OnNewEventComment=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnTariffChange" type="bool" %}
?User\_OnTariffChange=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnBookingChange" type="bool" %}
?User\_OnBookingChange=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnPurchases" type="bool" %}
?User\_OnPurchases=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnVisitorRegistration" type="bool" %}
?User\_OnVisitorRegistration=...
{% endapi-method-parameter %}


{% api-method-parameter name="OnPlaformInvoices" type="bool" %}
?User\_OnPlaformInvoices=...
{% endapi-method-parameter %}


{% api-method-parameter name="ReceiveCommunityDigest" type="bool" %}
?User\_ReceiveCommunityDigest=...
{% endapi-method-parameter %}


{% api-method-parameter name="ReceiveEveryMessage" type="bool" %}
?User\_ReceiveEveryMessage=...
{% endapi-method-parameter %}

{% api-method-parameter name="Businesses" type="int" required=false %}
?User\_Businesses=...
{% endapi-method-parameter %}
{% api-method-parameter name="UserRoles" type="int" required=false %}
?User\_UserRoles=...
{% endapi-method-parameter %}
{% api-method-parameter name="ChatRooms" type="int" required=false %}
?User\_ChatRooms=...
{% endapi-method-parameter %}

{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}


```javascript
{
    "Records": [{
        "FullName": "Full Name",
        "Email": "email@email.com",
        "AccessToken": "hush",
        "PreferredLanguage": null,
        "NewPassword": "password",
        "PassportNumber": "",
        "PassportCardNumber": "",
        "EnablePassportAccess": false,
        "Active": true,
        "IsAdmin": false,
        "APIAccess": false,
        "Validated": true,
        "MustResetPassword": true,
        "LastAccess": false,
        "Devices": "Devices",
        "OnNewEmail": true,
        "OnHelpDeskMsg": true,
        "OnNewWallPost": true,
        "OnNewMember": true,
        "OnProfileChanges": true,
        "OnNewBlogComment": true,
        "OnNewEventComment": true,
        "OnTariffChange": true,
        "OnBookingChange": true,
        "OnPurchases": true,
        "OnVisitorRegistration": true,
        "OnPlaformInvoices": true,
        "ReceiveCommunityDigest": true,
        "ReceiveEveryMessage": true,
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

> 🔒 Requires user role `user-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/users" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of users.
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
        "FullName": "Full Name",
        "Email": "email@email.com",
        "AccessToken": "hush",
        "PreferredLanguage": null,
        "NewPassword": "password",
        "PassportNumber": "",
        "PassportCardNumber": "",
        "EnablePassportAccess": false,
        "Active": true,
        "IsAdmin": false,
        "APIAccess": false,
        "Validated": true,
        "MustResetPassword": true,
        "LastAccess": false,
        "Devices": "Devices",
        "OnNewEmail": true,
        "OnHelpDeskMsg": true,
        "OnNewWallPost": true,
        "OnNewMember": true,
        "OnProfileChanges": true,
        "OnNewBlogComment": true,
        "OnNewEventComment": true,
        "OnTariffChange": true,
        "OnBookingChange": true,
        "OnPurchases": true,
        "OnVisitorRegistration": true,
        "OnPlaformInvoices": true,
        "ReceiveCommunityDigest": true,
        "ReceiveEveryMessage": true,
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

> 🔒 Requires user role `user-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. 
You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/users" %}
{% api-method-summary %}
By date or number range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of users based on a range of dates, integer or decimal properties.
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
?to\_User\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_User\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_User\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_User\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="LastAccess" type="datetime" required=false %}
?from\_User\_LastAccess=...
{% endapi-method-parameter %}
{% api-method-parameter name="LastAccess" type="datetime" required=false %}
?to\_User\_LastAccess=...
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
        "FullName": "Full Name",
        "Email": "email@email.com",
        "AccessToken": "hush",
        "PreferredLanguage": null,
        "NewPassword": "password",
        "PassportNumber": "",
        "PassportCardNumber": "",
        "EnablePassportAccess": false,
        "Active": true,
        "IsAdmin": false,
        "APIAccess": false,
        "Validated": true,
        "MustResetPassword": true,
        "LastAccess": false,
        "Devices": "Devices",
        "OnNewEmail": true,
        "OnHelpDeskMsg": true,
        "OnNewWallPost": true,
        "OnNewMember": true,
        "OnProfileChanges": true,
        "OnNewBlogComment": true,
        "OnNewEventComment": true,
        "OnTariffChange": true,
        "OnBookingChange": true,
        "OnPurchases": true,
        "OnVisitorRegistration": true,
        "OnPlaformInvoices": true,
        "ReceiveCommunityDigest": true,
        "ReceiveEveryMessage": true,
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

> 🔒 Requires user role `user-list`


{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/users?User_Id=[:id1,:id2,...]" %}
{% api-method-summary %}
List by Ids
{% endapi-method-summary %}

{% api-method-description %}
Gets one or more user records based on their Id.
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
Comma-separated list of IDs of every user to fetch. I.e. [123456,789102,...] 
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
        "FullName": "Full Name",
        "Email": "email@email.com",
        "AccessToken": "hush",
        "PreferredLanguage": null,
        "NewPassword": "password",
        "PassportNumber": "",
        "PassportCardNumber": "",
        "EnablePassportAccess": false,
        "Active": true,
        "IsAdmin": false,
        "APIAccess": false,
        "Validated": true,
        "MustResetPassword": true,
        "LastAccess": false,
        "Devices": "Devices",
        "OnNewEmail": true,
        "OnHelpDeskMsg": true,
        "OnNewWallPost": true,
        "OnNewMember": true,
        "OnProfileChanges": true,
        "OnNewBlogComment": true,
        "OnNewEventComment": true,
        "OnTariffChange": true,
        "OnBookingChange": true,
        "OnPurchases": true,
        "OnVisitorRegistration": true,
        "OnPlaformInvoices": true,
        "ReceiveCommunityDigest": true,
        "ReceiveEveryMessage": true,
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

> 🔒 Requires user role `user-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/users/:id" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one user record.
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
The ID of the user to fetch.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
        "FullName": "Full Name",
        "Email": "email@email.com",
        "AccessToken": "hush",
        "PreferredLanguage": null,
        "NewPassword": "password",
        "PassportNumber": "",
        "PassportCardNumber": "",
        "EnablePassportAccess": false,
        "Active": true,
        "IsAdmin": false,
        "APIAccess": false,
        "Validated": true,
        "MustResetPassword": true,
        "LastAccess": false,
        "Devices": "Devices",
        "OnNewEmail": true,
        "OnHelpDeskMsg": true,
        "OnNewWallPost": true,
        "OnNewMember": true,
        "OnProfileChanges": true,
        "OnNewBlogComment": true,
        "OnNewEventComment": true,
        "OnTariffChange": true,
        "OnBookingChange": true,
        "OnPurchases": true,
        "OnVisitorRegistration": true,
        "OnPlaformInvoices": true,
        "ReceiveCommunityDigest": true,
        "ReceiveEveryMessage": true,
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

> 🔒 Requires user role `user-read`


{% api-method method="post" host="https://spaces.nexudus.com/api" path="/sys/users" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new user.
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
{% api-method-parameter name="FullName" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Email" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="AccessToken" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PreferredLanguageId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Active" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="IsAdmin" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="APIAccess" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Validated" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="MustResetPassword" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="LastAccess" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Devices" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnNewEmail" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnHelpDeskMsg" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnNewWallPost" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnNewMember" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnProfileChanges" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnNewBlogComment" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnNewEventComment" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnTariffChange" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnBookingChange" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnPurchases" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnVisitorRegistration" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnPlaformInvoices" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ReceiveCommunityDigest" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ReceiveEveryMessage" type="bool" required=false %}
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

> 🔒 Requires user role `user-create`

```javascript
{
	"FullName": "Full Name",
	"Email": "email@email.com",
	"AccessToken": "hush",
	"PreferredLanguage": 12345678,
	"Active": true,
	"IsAdmin": false,
	"APIAccess": false,
	"Validated": true,
	"MustResetPassword": true,
	"LastAccess": false,
	"Devices": "Devices",
	"OnNewEmail": true,
	"OnHelpDeskMsg": true,
	"OnNewWallPost": true,
	"OnNewMember": true,
	"OnProfileChanges": true,
	"OnNewBlogComment": true,
	"OnNewEventComment": true,
	"OnTariffChange": true,
	"OnBookingChange": true,
	"OnPurchases": true,
	"OnVisitorRegistration": true,
	"OnPlaformInvoices": true,
	"ReceiveCommunityDigest": true,
	"ReceiveEveryMessage": true,
	"Businesses": [12345678, 87654321] (replaces entire list),
	"AddedBusinesses": [12345678, 87654321] (adds to list),
	"RemovedBusinesses": [12345678, 87654321] (removes from list),
	"UserRoles": [12345678, 87654321] (replaces entire list),
	"AddedUserRoles": [12345678, 87654321] (adds to list),
	"RemovedUserRoles": [12345678, 87654321] (removes from list),
}

```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/sys/users" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing user.
  
Required User Role: `user-edit`
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
The id of the user to update
{% api-method-parameter name="FullName" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="Email" type="string" required=true %}
{% endapi-method-parameter %}
{% api-method-parameter name="AccessToken" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="PreferredLanguageId" type="int" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="NewPassword" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Active" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="IsAdmin" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="APIAccess" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Validated" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="MustResetPassword" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="LastAccess" type="DateTime?" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Devices" type="string" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnNewEmail" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnHelpDeskMsg" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnNewWallPost" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnNewMember" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnProfileChanges" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnNewBlogComment" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnNewEventComment" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnTariffChange" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnBookingChange" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnPurchases" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnVisitorRegistration" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="OnPlaformInvoices" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ReceiveCommunityDigest" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="ReceiveEveryMessage" type="bool" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="Businesses" type="int[]" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AddedBusinesses" type="int[]" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RemovedBusinesses" type="int[]" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="UserRoles" type="int[]" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="AddedUserRoles" type="int[]" required=false %}
{% endapi-method-parameter %}
{% api-method-parameter name="RemovedUserRoles" type="int[]" required=false %}
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

> 🔒 Requires user role `user-edit`

```javascript
{
	"FullName": "Full Name",
	"Email": "email@email.com",
	"AccessToken": "hush",
	"PreferredLanguage": 12345678,
	"NewPassword": "password",
	"Active": true,
	"IsAdmin": false,
	"APIAccess": false,
	"Validated": true,
	"MustResetPassword": true,
	"LastAccess": false,
	"Devices": "Devices",
	"OnNewEmail": true,
	"OnHelpDeskMsg": true,
	"OnNewWallPost": true,
	"OnNewMember": true,
	"OnProfileChanges": true,
	"OnNewBlogComment": true,
	"OnNewEventComment": true,
	"OnTariffChange": true,
	"OnBookingChange": true,
	"OnPurchases": true,
	"OnVisitorRegistration": true,
	"OnPlaformInvoices": true,
	"ReceiveCommunityDigest": true,
	"ReceiveEveryMessage": true,
	"Businesses": [12345678, 87654321] (replaces entire list),
	"AddedBusinesses": [12345678, 87654321] (adds to list),
	"RemovedBusinesses": [12345678, 87654321] (removes from list),
	"UserRoles": [12345678, 87654321] (replaces entire list),
	"AddedUserRoles": [12345678, 87654321] (adds to list),
	"RemovedUserRoles": [12345678, 87654321] (removes from list),
}

```




{% api-method method="delete" host="https://spaces.nexudus.com/api" path="/sys/users/:id" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
Deletes a user.  
  
Required User Roles: `user-delete`
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



> 🔒 Requires user role `user-delete`


## Commands

Commands allow to perform actions against one or more user records. Some commands accept only one record while others can run an action for a number of records at the same time.  Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/users/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for user records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/users/runcommand" %}
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

> 🔒 Requires user role `user-edit`

## Enumerated values

##### Language:
> GET /api/utils/enums?name=eLanguage

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/users/getavatar/:id" %}
{% api-method-summary %}
Avatar
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
The id of the User to get the avatar for.
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
* [Language](../sys/language.md)
* [Application](../apps/application.md)
* [Business](../sys/business.md)
