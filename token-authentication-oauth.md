---
description: >-
  Token authentication can be used to obtain a token that can be used in
  requests the Nexudus REST API without having to use admin credentials.
---

# Token Authentication \(oauth\)

The general process to use token authentication is as follows:

1. Get a short-lived authentication **access token** and a long-lived **refresh token**.
2. Refresh the access token as needed by using a refresh token.
3. Use the "Bearer" HTTP header to make requests to the [REST API](rest-api/).

Access tokens are generally short-lived and you should not assume they last for more than a few minutes or hours.

{% hint style="danger" %}
You should always keep your refresh tokens secure, treat them as passwords.
{% endhint %}

{% api-method method="post" host="https://spaces.nexudus.com" path="/api/token" %}
{% api-method-summary %}
Authentication and Refresh Token
{% endapi-method-summary %}

{% api-method-description %}
Gets a short-lived access token and a long-lived refresh token.`grant_ype=password&username=EMAIL_ADDRESS&    
password=Demo1234`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="client\_id" %}
A unique identifier for the client making these requests. A single refresh token will be created per client, existing tokens for a given client\_id are invalidated when a new token is requested for that client\_id. If no client\_id header is passed, the client id would be set to your email.
{% endapi-method-parameter %}

{% api-method-parameter name="Accept" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="grant\_type" required=true type="string" %}
password
{% endapi-method-parameter %}

{% api-method-parameter name="username" type="string" required=true %}
your email
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
your password
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "access_token": "v8hNJebN2....",
    "token_type": "bearer",
    "expires_in": 604799,
    "refresh_token": "2669808..."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
If you submit an invalid username and/or password
{% endapi-method-response-example-description %}

```javascript
{
    "error": "invalid_grant",
    "error_description": "The user name or password is incorrect."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://spaces.nexudus.com" path="/api/token" %}
{% api-method-summary %}
Refresh Access Token
{% endapi-method-summary %}

{% api-method-description %}
Gets a new short-lived access token based on a refresh token. Refreshing a token for a client ID will invalidate all previous refresh tokens for that client ID but not existing Access Tokens that may not have expired.Refresh Tokens are valid for 15 days. If your refresh token has expired, you will need to use a username and password to create a new access token.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Accept" required=true type="string" %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="client\_id" type="string" required=true %}
The client id to refresh the access token for. This must the same as the client id you passed in when creating the access token. If you did not pass a client\_id header to get the initial token, you must pass the email used to obtain the initial token as the client\_id header to refresh it.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="grant\_type" type="string" required=true %}
refresh\_token
{% endapi-method-parameter %}

{% api-method-parameter name="refresh\_token" type="string" required=true %}
2669808...
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "access_token": "5o8X7pSy....",
    "token_type": "bearer",
    "expires_in": 604799,
    "refresh_token": "c3c14715..."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "error": "invalid_grant"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://spaces.nexudus.com" path="/api/auth/me" %}
{% api-method-summary %}
Making a Request
{% endapi-method-summary %}

{% api-method-description %}
This is an example of passing a access token to any requests to the REST API.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Bearer" type="string" required=true %}
v8hNJebN2...
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "NewPasswordConfirm": null,
    "OldPassword": null,
    "DefaultBusinessId": 1234566,
    "DefaultBusinessName": "Demo Space",
    "DefaultCurrencyId": 3005,
    "DefaultCurrencyName": "UK Pound Sterling (GBP)",
    "DefaultCurrencyCode": "GBP",
    "DefaultCountryId": 1221,
    "DefaultCountryName": "United States",
    "DefaultSimpleTimeZoneId": 2023,
    "DefaultSimpleTimeZoneName": "GMT Standard Time",
    "DefaultSimpleTimeZoneNameIana": "Europe/London",
    "FullName": "John Doe",
    "Email": "demoaccount@nexudus.com",
    "AccessToken": "...",
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
    "LastAccess": "2019-05-13T23:30:00Z",
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
    "ReceiveEveryMessage": false,
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
    "UpdatedOn": "2019-05-14T08:22:25Z",
    "CreatedOn": "2017-02-24T23:45:48Z",
    "UniqueId": "d3767b81-49c3-4167-bd0b-d185a079e9ff",
    "UpdatedBy": "email@example.com",
    "IsNew": false,
    "SystemId": null,
    "ToStringText": "John Doe - email@example.com",
    "LocalizationDetails": null
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

