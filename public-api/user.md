---
description: >-
  Returns data and authentication tokens for a user based on their username and
  password.
---

# User

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/en/user/me" %}
{% api-method-summary %}
User Information
{% endapi-method-summary %}

{% api-method-description %}
Gets the details of the logged in user
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic ZGVtb2FjY291b....cy5jb206RGVtbzEyMzQ=
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "NewPasswordConfirm": null,
    "OldPassword": null,
    "DefaultBusinessId": 287964677,
    "DefaultBusinessName": "Demo Space A",
    "DefaultCurrencyId": 0,
    "DefaultCurrencyName": null,
    "DefaultCurrencyCode": null,
    "DefaultCountryId": 0,
    "DefaultCountryName": null,
    "DefaultSimpleTimeZoneId": 0,
    "DefaultSimpleTimeZoneName": null,
    "DefaultSimpleTimeZoneNameIana": null,
    "FullName": "John Doe (Original)",
    "Email": "demoaccount@nexudus.com",
    "AccessToken": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJlbWFpbCI6ImRlbW9hY2NvdW50QG5leHVkdXMuY29tIiwiaXNzIjoic2VsZiIsImF1ZCI6Imh0dHBzOi8vc3BhY2VzLm5leHVkdXMuY29tIiwiZXhwIjoxNTc1OTA2MTQxLCJuYmYiOjE1NzU5MDQzNDF9.42EcWcSC7C0Ym9Rvvo4B1JC0uj_sWtgbusfPrn1kQDs",
    "PreferredLanguageId": 287965678,
    "NewPassword": null,
    "PassportNumber": null,
    "PassportCardNumber": null,
    "EnablePassportAccess": true,
    "Active": true,
    "IsAdmin": true,
    "APIAccess": true,
    "Validated": true,
    "MustResetPassword": false,
    "LastAccess": "2019-12-09T14:50:04Z",
    "Devices": null,
    "OnNewEmail": true,
    "OnHelpDeskMsg": true,
    "OnNewWallPost": true,
    "OnNewMember": true,
    "OnProfileChanges": true,
    "OnNewBlogComment": false,
    "OnNewEventComment": false,
    "OnTariffChange": true,
    "OnBookingChange": true,
    "OnPurchases": true,
    "OnVisitorRegistration": true,
    "OnPlaformInvoices": true,
    "ReceiveCommunityDigest": false,
    "ReceiveEveryMessage": true,
    "Businesses": [
        287964677,
        627703076,
        627703077
    ],
    "AddedBusinesses": null,
    "RemovedBusinesses": null,
    "UserRoles": [
        770685918,
        800349553,
        961091136,
        961274353
    ],
    "AddedUserRoles": null,
    "RemovedUserRoles": null,
    "ChatRooms": [],
    "AddedChatRooms": null,
    "RemovedChatRooms": null,
    "NewAvatarUrl": null,
    "AvatarFileName": null,
    "ClearAvatarFile": false,
    "Id": 303914611,
    "UpdatedOn": "2019-12-09T15:13:58Z",
    "CreatedOn": "2017-02-24T23:45:48Z",
    "UniqueId": "d3767b81-49c3-4167-bd0b-d185a079e9ff",
    "UpdatedBy": "demoaccount@nexudus.com",
    "IsNew": false,
    "SystemId": null,
    "ToStringText": "John Doe (Original) - demoaccount@nexudus.com",
    "LocalizationDetails": null
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Invalid username and/or password
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/en/user/exists?email=:email" %}
{% api-method-summary %}
User Exists
{% endapi-method-summary %}

{% api-method-description %}
Checks if a user is already registered with this location
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="email" type="string" required=true %}
email@example.net
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
true
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/en/user/login?t=:accessToken" %}
{% api-method-summary %}
Login
{% endapi-method-summary %}

{% api-method-description %}
Logs are user into the members portal based on a one-time JWT access token
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="redirectUrl" type="string" required=false %}
A relative redirect URL to send the user after logging in.
{% endapi-method-parameter %}

{% api-method-parameter name="accessToken" type="string" required=true %}
A JWT access token for the user to be logged in. Use the "AccessToken" property of the User Information Endpoint. This token can only be used once.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
true
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://spaces.nexudus.com" path="/api/sys/users/validate" %}
{% api-method-summary %}
Validate Credentials
{% endapi-method-summary %}

{% api-method-description %}
Logs are user into the members portal based on a one-time JWT access token.  
  
**NOTE: This endpoint uses the REST API domain \(spaces.nexudus.com\)**
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="Email" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Password" type="string" required=true %}

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
    "Message": "OK",
    "Value": {
        "NewPasswordConfirm": null,
        "OldPassword": null,
        "DefaultBusinessId": 287964677,
        "DefaultBusinessName": "Demo Space A",
        "DefaultCurrencyId": 0,
        "DefaultCurrencyName": null,
        "DefaultCurrencyCode": null,
        "DefaultCountryId": 0,
        "DefaultCountryName": null,
        "DefaultSimpleTimeZoneId": 0,
        "DefaultSimpleTimeZoneName": null,
        "DefaultSimpleTimeZoneNameIana": null,
        "FullName": "John Doe (Original)",
        "Email": "demoaccount@nexudus.com",
        "AccessToken": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJlbWFpbCI6ImRlbW9hY2NvdW50QG5leHVkdXMuY29tIiwiaXNzIjoic2VsZiIsImF1ZCI6Imh0dHBzOi8vc3BhY2VzLm5leHVkdXMuY29tIiwiZXhwIjoxNTc1OTA2MTQxLCJuYmYiOjE1NzU5MDQzNDF9.42EcWcSC7C0Ym9Rvvo4B1JC0uj_sWtgbusfPrn1kQDs",
        "PreferredLanguageId": 287965678,
        "NewPassword": null,
        "PassportNumber": null,
        "PassportCardNumber": null,
        "EnablePassportAccess": true,
        "Active": true,
        "IsAdmin": true,
        "APIAccess": true,
        "Validated": true,
        "MustResetPassword": false,
        "LastAccess": "2019-12-09T14:50:04Z",
        "Devices": null,
        "OnNewEmail": true,
        "OnHelpDeskMsg": true,
        "OnNewWallPost": true,
        "OnNewMember": true,
        "OnProfileChanges": true,
        "OnNewBlogComment": false,
        "OnNewEventComment": false,
        "OnTariffChange": true,
        "OnBookingChange": true,
        "OnPurchases": true,
        "OnVisitorRegistration": true,
        "OnPlaformInvoices": true,
        "ReceiveCommunityDigest": false,
        "ReceiveEveryMessage": true,
        "Businesses": [
            287964677,
            627703076,
            627703077
        ],
        "AddedBusinesses": null,
        "RemovedBusinesses": null,
        "UserRoles": [
            770685918,
            800349553,
            961091136,
            961274353
        ],
        "AddedUserRoles": null,
        "RemovedUserRoles": null,
        "ChatRooms": [],
        "AddedChatRooms": null,
        "RemovedChatRooms": null,
        "NewAvatarUrl": null,
        "AvatarFileName": null,
        "ClearAvatarFile": false,
        "Id": 303914611,
        "UpdatedOn": "2019-12-09T15:25:28Z",
        "CreatedOn": "2017-02-24T23:45:48Z",
        "UniqueId": "d3767b81-49c3-4167-bd0b-d185a079e9ff",
        "UpdatedBy": "demoaccount@nexudus.com",
        "IsNew": false,
        "SystemId": null,
        "ToStringText": "John Doe (Original) - demoaccount@nexudus.com",
        "LocalizationDetails": null
    },
    "OpenInDialog": false,
    "OpenInWindow": false,
    "RedirectURL": null,
    "JavaScript": null,
    "UpdatedOn": null,
    "UpdatedBy": null,
    "Errors": null,
    "WasSuccessful": true
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "Status": 500,
    "Message": "The email address or password you entered is not valid.",
    "Value": null,
    "OpenInDialog": false,
    "OpenInWindow": false,
    "RedirectURL": null,
    "JavaScript": null,
    "UpdatedOn": null,
    "UpdatedBy": null,
    "Errors": null,
    "WasSuccessful": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://spaces.nexudus.com" path="/api/sys/users/:userId/token/refresh" %}
{% api-method-summary %}
Refresh Access Token
{% endapi-method-summary %}

{% api-method-description %}
Generates a new access token for for a user. This endpoint requires a full unrestricted admin credential or a user that has the User-Edit role.  
  
**NOTE: This endpoint requires the user-edit role.  
NOTE: This endpoint uses the REST API domain \(spaces.nexudus.com\)**
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userId" type="string" required=true %}
The Id of the user to refresh the token for
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic ZGVtb2FjY291...5jb206RGVtbzEyMzQ=
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
    "Message": "OK",
    "Value": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJlbWFpbCI6ImRlbW9hY2NvdW50QG5leHVkdXMuY29tIiwiaXNzIjoic2VsZiIsImF1ZCI6Imh0dHBzOi8vc3BhY2VzLm5leHVkdXMuY29tIiwiZXhwIjoxNTc1OTA3MjY2LCJuYmYiOjE1NzU5MDU0NjZ9._qXna9_rtYd9xYnNz8JxTG_sLgmPVhAgWzXeWY43l1Q",
    "OpenInDialog": false,
    "OpenInWindow": false,
    "RedirectURL": null,
    "JavaScript": null,
    "UpdatedOn": null,
    "UpdatedBy": null,
    "Errors": null,
    "WasSuccessful": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> Requires user role `user-edit`

