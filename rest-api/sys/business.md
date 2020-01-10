# Business

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/businesses" %}
{% api-method-summary %}
Find
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of businesses based on one or more filter querystring parameters.
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
?Business\_SystemId=...
{% endapi-method-parameter %}

{% api-method-parameter name="Name" type="string" %}
?Business\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="DefaultLanguage" type="enum" %}
?Business\_DefaultLanguage=...
{% endapi-method-parameter %}

{% api-method-parameter name="SpaceWebsiteLanguage" type="Language" %}
?Business\_SpaceWebsiteLanguage=...
{% endapi-method-parameter %}

{% api-method-parameter name="RootLocation" type="Business" %}
?Business\_RootLocation=...
{% endapi-method-parameter %}

{% api-method-parameter name="WebAddress" type="string" %}
?Business\_WebAddress=...
{% endapi-method-parameter %}

{% api-method-parameter name="DefaultPaymentGateway" type="PaymentGateway" %}
?Business\_DefaultPaymentGateway=...
{% endapi-method-parameter %}

{% api-method-parameter name="NextInvoice" type="DateTime?" %}
?Business\_NextInvoice=...
{% endapi-method-parameter %}

{% api-method-parameter name="TermsAndConditions" type="string" %}
?Business\_TermsAndConditions=...
{% endapi-method-parameter %}

{% api-method-parameter name="ShortIntroduction" type="string" %}
?Business\_ShortIntroduction=...
{% endapi-method-parameter %}

{% api-method-parameter name="AboutUs" type="string" %}
?Business\_AboutUs=...
{% endapi-method-parameter %}

{% api-method-parameter name="Quote" type="string" %}
?Business\_Quote=...
{% endapi-method-parameter %}

{% api-method-parameter name="PrivacyPolicyUrl" type="string" %}
?Business\_PrivacyPolicyUrl=...
{% endapi-method-parameter %}

{% api-method-parameter name="CookiePolicyUrl" type="string" %}
?Business\_CookiePolicyUrl=...
{% endapi-method-parameter %}

{% api-method-parameter name="WebContact" type="string" %}
?Business\_WebContact=...
{% endapi-method-parameter %}

{% api-method-parameter name="Address" type="string" %}
?Business\_Address=...
{% endapi-method-parameter %}

{% api-method-parameter name="Phone" type="string" %}
?Business\_Phone=...
{% endapi-method-parameter %}

{% api-method-parameter name="Fax" type="string" %}
?Business\_Fax=...
{% endapi-method-parameter %}

{% api-method-parameter name="EmailContact" type="string" %}
?Business\_EmailContact=...
{% endapi-method-parameter %}

{% api-method-parameter name="Country" type="Country" %}
?Business\_Country=...
{% endapi-method-parameter %}

{% api-method-parameter name="Currency" type="Currency" %}
?Business\_Currency=...
{% endapi-method-parameter %}

{% api-method-parameter name="SimpleTimeZone" type="SimpleTimeZone" %}
?Business\_SimpleTimeZone=...
{% endapi-method-parameter %}

{% api-method-parameter name="Last4Digits" type="string" %}
?Business\_Last4Digits=...
{% endapi-method-parameter %}

{% api-method-parameter name="PreAuthLastError" type="string" %}
?Business\_PreAuthLastError=...
{% endapi-method-parameter %}

{% api-method-parameter name="PassportChannels" type="string" %}
?Business\_PassportChannels=...
{% endapi-method-parameter %}

{% api-method-parameter name="PassportPublished" type="bool" %}
?Business\_PassportPublished=...
{% endapi-method-parameter %}

{% api-method-parameter name="PassportSpaceName" type="string" %}
?Business\_PassportSpaceName=...
{% endapi-method-parameter %}

{% api-method-parameter name="PassportTagLine" type="string" %}
?Business\_PassportTagLine=...
{% endapi-method-parameter %}

{% api-method-parameter name="VenueType" type="enum" %}
?Business\_VenueType=...
{% endapi-method-parameter %}

{% api-method-parameter name="Tags" type="string" %}
?Business\_Tags=...
{% endapi-method-parameter %}

{% api-method-parameter name="NumberOfFloors" type="int?" %}
?Business\_NumberOfFloors=...
{% endapi-method-parameter %}

{% api-method-parameter name="FloorSpace" type="int?" %}
?Business\_FloorSpace=...
{% endapi-method-parameter %}

{% api-method-parameter name="FloorSpaceUnit" type="enum" %}
?Business\_FloorSpaceUnit=...
{% endapi-method-parameter %}

{% api-method-parameter name="Longitude" type="decimal?" %}
?Business\_Longitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="Latitude" type="decimal?" %}
?Business\_Latitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="PassportDescription" type="string" %}
?Business\_PassportDescription=...
{% endapi-method-parameter %}

{% api-method-parameter name="TownCity" type="string" %}
?Business\_TownCity=...
{% endapi-method-parameter %}

{% api-method-parameter name="PostalCode" type="string" %}
?Business\_PostalCode=...
{% endapi-method-parameter %}

{% api-method-parameter name="StreetName" type="string" %}
?Business\_StreetName=...
{% endapi-method-parameter %}

{% api-method-parameter name="StreetNumber" type="string" %}
?Business\_StreetNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="Neighborhood" type="string" %}
?Business\_Neighborhood=...
{% endapi-method-parameter %}

{% api-method-parameter name="ContactPhoneNumber" type="string" %}
?Business\_ContactPhoneNumber=...
{% endapi-method-parameter %}

{% api-method-parameter name="ContactEmail" type="string" %}
?Business\_ContactEmail=...
{% endapi-method-parameter %}

{% api-method-parameter name="PassportMembersAccess" type="enum" %}
?Business\_PassportMembersAccess=...
{% endapi-method-parameter %}

{% api-method-parameter name="PassportEventsAccess" type="enum" %}
?Business\_PassportEventsAccess=...
{% endapi-method-parameter %}

{% api-method-parameter name="PassportCommunityAccess" type="enum" %}
?Business\_PassportCommunityAccess=...
{% endapi-method-parameter %}

{% api-method-parameter name="PassportBlogPostsAccess" type="enum" %}
?Business\_PassportBlogPostsAccess=...
{% endapi-method-parameter %}

{% api-method-parameter name="MondayOpenTime" type="int?" %}
?Business\_MondayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="MondayCloseTime" type="int?" %}
?Business\_MondayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayOpenTime" type="int?" %}
?Business\_TuesdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayCloseTime" type="int?" %}
?Business\_TuesdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayOpenTime" type="int?" %}
?Business\_WednesdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayCloseTime" type="int?" %}
?Business\_WednesdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayOpenTime" type="int?" %}
?Business\_ThursdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayCloseTime" type="int?" %}
?Business\_ThursdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="FridayOpenTime" type="int?" %}
?Business\_FridayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="FridayCloseTime" type="int?" %}
?Business\_FridayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayOpenTime" type="int?" %}
?Business\_SaturdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayCloseTime" type="int?" %}
?Business\_SaturdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SundayOpenTime" type="int?" %}
?Business\_SundayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SundayCloseTime" type="int?" %}
?Business\_SundayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="MondayClosed" type="bool" %}
?Business\_MondayClosed=...
{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayClosed" type="bool" %}
?Business\_TuesdayClosed=...
{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayClosed" type="bool" %}
?Business\_WednesdayClosed=...
{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayClosed" type="bool" %}
?Business\_ThursdayClosed=...
{% endapi-method-parameter %}

{% api-method-parameter name="FridayClosed" type="bool" %}
?Business\_FridayClosed=...
{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayClosed" type="bool" %}
?Business\_SaturdayClosed=...
{% endapi-method-parameter %}

{% api-method-parameter name="SundayClosed" type="bool" %}
?Business\_SundayClosed=...
{% endapi-method-parameter %}

{% api-method-parameter name="SameOpeningTimes" type="bool" %}
?Business\_SameOpeningTimes=...
{% endapi-method-parameter %}

{% api-method-parameter name="Country\_Name" type="string" %}
?Business\_Country\_Name=...
{% endapi-method-parameter %}

{% api-method-parameter name="Currency\_Code" type="string" %}
?Business\_Currency\_Code=...
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
        "Name": "Joe",
        "DefaultLanguage": Nexudus.Coworking.Core.Enums.eLanguage.Spanish,
        "SpaceWebsiteLanguage": null,
        "RootLocation": null,
        "WebAddress": "url",
        "DefaultPaymentGateway": null,
        "NextInvoice": null,
        "TermsAndConditions": "TermsAndConditions",
        "ShortIntroduction": "",
        "AboutUs": "",
        "Quote": "Joe",
        "PrivacyPolicyUrl": "Joe",
        "CookiePolicyUrl": "Joe",
        "WebContact": "www.example.com",
        "Address": "Joe",
        "Phone": "0207768885828",
        "Fax": "0207768885828",
        "EmailContact": "me@example.com",
        "Country": null,
        "Currency": null,
        "SimpleTimeZone": null,
        "Last4Digits": "0",
        "PreAuthLastError": "0",
        "PassportChannels": "null",
        "PassportPublished": null,
        "PassportSpaceName": "null",
        "PassportTagLine": "null",
        "VenueType": Nexudus.Coworking.Core.Enums.eVenueType.CoworkingSpace,
        "Tags": "null",
        "NumberOfFloors": 1,
        "FloorSpace": 1,
        "FloorSpaceUnit": Nexudus.Coworking.Core.Enums.eFloorUnit.SqFt,
        "Longitude": 1,
        "Latitude": 1,
        "PassportDescription": "Joe",
        "TownCity": "",
        "PostalCode": "",
        "StreetName": "",
        "StreetNumber": "",
        "Neighborhood": "",
        "ContactPhoneNumber": "",
        "ContactEmail": "",
        "PassportMembersAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportEventsAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportCommunityAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportBlogPostsAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "MondayOpenTime": null,
        "MondayCloseTime": null,
        "TuesdayOpenTime": null,
        "TuesdayCloseTime": null,
        "WednesdayOpenTime": null,
        "WednesdayCloseTime": null,
        "ThursdayOpenTime": null,
        "ThursdayCloseTime": null,
        "FridayOpenTime": null,
        "FridayCloseTime": null,
        "SaturdayOpenTime": null,
        "SaturdayCloseTime": null,
        "SundayOpenTime": null,
        "SundayCloseTime": null,
        "MondayClosed": null,
        "TuesdayClosed": null,
        "WednesdayClosed": null,
        "ThursdayClosed": null,
        "FridayClosed": null,
        "SaturdayClosed": null,
        "SundayClosed": null,
        "SameOpeningTimes": null,
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

> 🔒 Requires user role `business-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/businesses" %}
{% api-method-summary %}
List
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to GET a list of businesses.
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
        "Name": "Joe",
        "DefaultLanguage": Nexudus.Coworking.Core.Enums.eLanguage.Spanish,
        "SpaceWebsiteLanguage": null,
        "RootLocation": null,
        "WebAddress": "url",
        "DefaultPaymentGateway": null,
        "NextInvoice": null,
        "TermsAndConditions": "TermsAndConditions",
        "ShortIntroduction": "",
        "AboutUs": "",
        "Quote": "Joe",
        "PrivacyPolicyUrl": "Joe",
        "CookiePolicyUrl": "Joe",
        "WebContact": "www.example.com",
        "Address": "Joe",
        "Phone": "0207768885828",
        "Fax": "0207768885828",
        "EmailContact": "me@example.com",
        "Country": null,
        "Currency": null,
        "SimpleTimeZone": null,
        "Last4Digits": "0",
        "PreAuthLastError": "0",
        "PassportChannels": "null",
        "PassportPublished": null,
        "PassportSpaceName": "null",
        "PassportTagLine": "null",
        "VenueType": Nexudus.Coworking.Core.Enums.eVenueType.CoworkingSpace,
        "Tags": "null",
        "NumberOfFloors": 1,
        "FloorSpace": 1,
        "FloorSpaceUnit": Nexudus.Coworking.Core.Enums.eFloorUnit.SqFt,
        "Longitude": 1,
        "Latitude": 1,
        "PassportDescription": "Joe",
        "TownCity": "",
        "PostalCode": "",
        "StreetName": "",
        "StreetNumber": "",
        "Neighborhood": "",
        "ContactPhoneNumber": "",
        "ContactEmail": "",
        "PassportMembersAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportEventsAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportCommunityAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportBlogPostsAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "MondayOpenTime": null,
        "MondayCloseTime": null,
        "TuesdayOpenTime": null,
        "TuesdayCloseTime": null,
        "WednesdayOpenTime": null,
        "WednesdayCloseTime": null,
        "ThursdayOpenTime": null,
        "ThursdayCloseTime": null,
        "FridayOpenTime": null,
        "FridayCloseTime": null,
        "SaturdayOpenTime": null,
        "SaturdayCloseTime": null,
        "SundayOpenTime": null,
        "SundayCloseTime": null,
        "MondayClosed": null,
        "TuesdayClosed": null,
        "WednesdayClosed": null,
        "ThursdayClosed": null,
        "FridayClosed": null,
        "SaturdayClosed": null,
        "SundayClosed": null,
        "SameOpeningTimes": null,
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

> 🔒 Requires user role `business-list`

{% hint style="info" %}
You can also get a list of records based when they were created or updated. This is useful if you want to get a list of records created after or before a particular point in time. You can also use range query parameters for all date, integer and decimal properties.
{% endhint %}

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/businesses" %}
{% api-method-summary %}
By date range
{% endapi-method-summary %}

{% api-method-description %}
Gets a list of businesses based on the date when they were created or updated.
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
?to\_Business\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="CreatedOn" type="object" required=false %}
?from\_Business\_CreatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?to\_Business\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="UpdatedOn" type="object" required=false %}
?from\_Business\_UpdatedOn=...
{% endapi-method-parameter %}

{% api-method-parameter name="NextInvoice" type="datetime" required=false %}
?from\_Business\_NextInvoice=...
{% endapi-method-parameter %}

{% api-method-parameter name="NextInvoice" type="datetime" required=false %}
?to\_Business\_NextInvoice=...
{% endapi-method-parameter %}

{% api-method-parameter name="NumberOfFloors" type="int" required=false %}
?from\_Business\_NumberOfFloors=...
{% endapi-method-parameter %}

{% api-method-parameter name="NumberOfFloors" type="int" required=false %}
?to\_Business\_NumberOfFloors=...
{% endapi-method-parameter %}

{% api-method-parameter name="FloorSpace" type="int" required=false %}
?from\_Business\_FloorSpace=...
{% endapi-method-parameter %}

{% api-method-parameter name="FloorSpace" type="int" required=false %}
?to\_Business\_FloorSpace=...
{% endapi-method-parameter %}

{% api-method-parameter name="Longitude" type="decimal" required=false %}
?from\_Business\_Longitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="Longitude" type="decimal" required=false %}
?to\_Business\_Longitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="Latitude" type="decimal" required=false %}
?from\_Business\_Latitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="Latitude" type="decimal" required=false %}
?to\_Business\_Latitude=...
{% endapi-method-parameter %}

{% api-method-parameter name="MondayOpenTime" type="int" required=false %}
?from\_Business\_MondayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="MondayOpenTime" type="int" required=false %}
?to\_Business\_MondayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="MondayCloseTime" type="int" required=false %}
?from\_Business\_MondayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="MondayCloseTime" type="int" required=false %}
?to\_Business\_MondayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayOpenTime" type="int" required=false %}
?from\_Business\_TuesdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayOpenTime" type="int" required=false %}
?to\_Business\_TuesdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayCloseTime" type="int" required=false %}
?from\_Business\_TuesdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayCloseTime" type="int" required=false %}
?to\_Business\_TuesdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayOpenTime" type="int" required=false %}
?from\_Business\_WednesdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayOpenTime" type="int" required=false %}
?to\_Business\_WednesdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayCloseTime" type="int" required=false %}
?from\_Business\_WednesdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayCloseTime" type="int" required=false %}
?to\_Business\_WednesdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayOpenTime" type="int" required=false %}
?from\_Business\_ThursdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayOpenTime" type="int" required=false %}
?to\_Business\_ThursdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayCloseTime" type="int" required=false %}
?from\_Business\_ThursdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayCloseTime" type="int" required=false %}
?to\_Business\_ThursdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="FridayOpenTime" type="int" required=false %}
?from\_Business\_FridayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="FridayOpenTime" type="int" required=false %}
?to\_Business\_FridayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="FridayCloseTime" type="int" required=false %}
?from\_Business\_FridayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="FridayCloseTime" type="int" required=false %}
?to\_Business\_FridayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayOpenTime" type="int" required=false %}
?from\_Business\_SaturdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayOpenTime" type="int" required=false %}
?to\_Business\_SaturdayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayCloseTime" type="int" required=false %}
?from\_Business\_SaturdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayCloseTime" type="int" required=false %}
?to\_Business\_SaturdayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SundayOpenTime" type="int" required=false %}
?from\_Business\_SundayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SundayOpenTime" type="int" required=false %}
?to\_Business\_SundayOpenTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SundayCloseTime" type="int" required=false %}
?from\_Business\_SundayCloseTime=...
{% endapi-method-parameter %}

{% api-method-parameter name="SundayCloseTime" type="int" required=false %}
?to\_Business\_SundayCloseTime=...
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
        "Name": "Joe",
        "DefaultLanguage": Nexudus.Coworking.Core.Enums.eLanguage.Spanish,
        "SpaceWebsiteLanguage": null,
        "RootLocation": null,
        "WebAddress": "url",
        "DefaultPaymentGateway": null,
        "NextInvoice": null,
        "TermsAndConditions": "TermsAndConditions",
        "ShortIntroduction": "",
        "AboutUs": "",
        "Quote": "Joe",
        "PrivacyPolicyUrl": "Joe",
        "CookiePolicyUrl": "Joe",
        "WebContact": "www.example.com",
        "Address": "Joe",
        "Phone": "0207768885828",
        "Fax": "0207768885828",
        "EmailContact": "me@example.com",
        "Country": null,
        "Currency": null,
        "SimpleTimeZone": null,
        "Last4Digits": "0",
        "PreAuthLastError": "0",
        "PassportChannels": "null",
        "PassportPublished": null,
        "PassportSpaceName": "null",
        "PassportTagLine": "null",
        "VenueType": Nexudus.Coworking.Core.Enums.eVenueType.CoworkingSpace,
        "Tags": "null",
        "NumberOfFloors": 1,
        "FloorSpace": 1,
        "FloorSpaceUnit": Nexudus.Coworking.Core.Enums.eFloorUnit.SqFt,
        "Longitude": 1,
        "Latitude": 1,
        "PassportDescription": "Joe",
        "TownCity": "",
        "PostalCode": "",
        "StreetName": "",
        "StreetNumber": "",
        "Neighborhood": "",
        "ContactPhoneNumber": "",
        "ContactEmail": "",
        "PassportMembersAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportEventsAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportCommunityAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportBlogPostsAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "MondayOpenTime": null,
        "MondayCloseTime": null,
        "TuesdayOpenTime": null,
        "TuesdayCloseTime": null,
        "WednesdayOpenTime": null,
        "WednesdayCloseTime": null,
        "ThursdayOpenTime": null,
        "ThursdayCloseTime": null,
        "FridayOpenTime": null,
        "FridayCloseTime": null,
        "SaturdayOpenTime": null,
        "SaturdayCloseTime": null,
        "SundayOpenTime": null,
        "SundayCloseTime": null,
        "MondayClosed": null,
        "TuesdayClosed": null,
        "WednesdayClosed": null,
        "ThursdayClosed": null,
        "FridayClosed": null,
        "SaturdayClosed": null,
        "SundayClosed": null,
        "SameOpeningTimes": null,
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

> 🔒 Requires user role `business-list`

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/businesses?Business\_Id=\[:id1,:id2,...\]" %}
{% api-method-summary %}
One by Id
{% endapi-method-summary %}

{% api-method-description %}
Gets one business record.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Comma-separated list of IDs of every business to fetch. I.e. \[123456,789102,...\]
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
        "Name": "Joe",
        "DefaultLanguage": Nexudus.Coworking.Core.Enums.eLanguage.Spanish,
        "SpaceWebsiteLanguage": null,
        "RootLocation": null,
        "WebAddress": "url",
        "DefaultPaymentGateway": null,
        "NextInvoice": null,
        "TermsAndConditions": "TermsAndConditions",
        "ShortIntroduction": "",
        "AboutUs": "",
        "Quote": "Joe",
        "PrivacyPolicyUrl": "Joe",
        "CookiePolicyUrl": "Joe",
        "WebContact": "www.example.com",
        "Address": "Joe",
        "Phone": "0207768885828",
        "Fax": "0207768885828",
        "EmailContact": "me@example.com",
        "Country": null,
        "Currency": null,
        "SimpleTimeZone": null,
        "Last4Digits": "0",
        "PreAuthLastError": "0",
        "PassportChannels": "null",
        "PassportPublished": null,
        "PassportSpaceName": "null",
        "PassportTagLine": "null",
        "VenueType": Nexudus.Coworking.Core.Enums.eVenueType.CoworkingSpace,
        "Tags": "null",
        "NumberOfFloors": 1,
        "FloorSpace": 1,
        "FloorSpaceUnit": Nexudus.Coworking.Core.Enums.eFloorUnit.SqFt,
        "Longitude": 1,
        "Latitude": 1,
        "PassportDescription": "Joe",
        "TownCity": "",
        "PostalCode": "",
        "StreetName": "",
        "StreetNumber": "",
        "Neighborhood": "",
        "ContactPhoneNumber": "",
        "ContactEmail": "",
        "PassportMembersAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportEventsAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportCommunityAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "PassportBlogPostsAccess": Nexudus.Coworking.Core.Enums.ePassportAccess.Everyone,
        "MondayOpenTime": null,
        "MondayCloseTime": null,
        "TuesdayOpenTime": null,
        "TuesdayCloseTime": null,
        "WednesdayOpenTime": null,
        "WednesdayCloseTime": null,
        "ThursdayOpenTime": null,
        "ThursdayCloseTime": null,
        "FridayOpenTime": null,
        "FridayCloseTime": null,
        "SaturdayOpenTime": null,
        "SaturdayCloseTime": null,
        "SundayOpenTime": null,
        "SundayCloseTime": null,
        "MondayClosed": null,
        "TuesdayClosed": null,
        "WednesdayClosed": null,
        "ThursdayClosed": null,
        "FridayClosed": null,
        "SaturdayClosed": null,
        "SundayClosed": null,
        "SameOpeningTimes": null,
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

> 🔒 Requires user role `business-read`

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/sys/businesses" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
Creates a new business.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The ID of the business to fetch.
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

{% api-method-parameter name="DefaultLanguage" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SpaceWebsiteLanguageId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="RootLocationId" type="int" required=false %}

```text
"Not found"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method-parameter name="WebAddress" type="string" required=true %}

{% api-method method="post" host="https://spaces.nexudus.com/api" path="/sys/businesses" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% endapi-method-parameter %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Basic Authentication token. Base64 encoding of 'username:password'.
{% endapi-method-parameter %}

{% api-method-parameter name="Content" type="string" required=true %}
application/json
{% endapi-method-parameter %}

{% api-method-body-parameters %}
{% api-method-parameter name="Name" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="DefaultLanguage" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SpaceWebsiteLanguageId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WebAddress" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="DefaultPaymentGatewayId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TermsAndConditions" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ShortIntroduction" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AboutUs" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Quote" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PrivacyPolicyUrl" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CookiePolicyUrl" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WebContact" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Address" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Phone" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Fax" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="EmailContact" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CountryId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CurrencyId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="SimpleTimeZoneId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Last4Digits" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PreAuthLastError" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportChannels" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportPublished" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportSpaceName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportTagLine" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="VenueType" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Tags" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NumberOfFloors" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FloorSpace" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FloorSpaceUnit" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Longitude" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Latitude" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportDescription" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TownCity" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PostalCode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="StreetName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="StreetNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Neighborhood" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ContactPhoneNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ContactEmail" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportMembersAccess" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportEventsAccess" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportCommunityAccess" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportBlogPostsAccess" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MondayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MondayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FridayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FridayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SundayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SundayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MondayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FridayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SundayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SameOpeningTimes" type="bool" required=false %}

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

> 🔒 Requires user role `business-create`

```javascript
{
    "Name": "Joe",
    "DefaultLanguage": 1 (check Enumerated values section below),
    "SpaceWebsiteLanguage": 12345678,
    "WebAddress": "url",
    "DefaultPaymentGateway": 12345678,
    "TermsAndConditions": "TermsAndConditions",
    "ShortIntroduction": "",
    "AboutUs": "",
    "Quote": "Joe",
    "PrivacyPolicyUrl": "Joe",
    "CookiePolicyUrl": "Joe",
    "WebContact": "www.example.com",
    "Address": "Joe",
    "Phone": "0207768885828",
    "Fax": "0207768885828",
    "EmailContact": "me@example.com",
    "Country": 12345678,
    "Currency": 12345678,
    "SimpleTimeZone": 12345678,
    "Last4Digits": "0",
    "PreAuthLastError": "0",
    "PassportChannels": "null",
    "PassportPublished": null,
    "PassportSpaceName": "null",
    "PassportTagLine": "null",
    "VenueType": 1 (check Enumerated values section below),
    "Tags": "null",
    "NumberOfFloors": 1,
    "FloorSpace": 1,
    "FloorSpaceUnit": 1 (check Enumerated values section below),
    "Longitude": 1,
    "Latitude": 1,
    "PassportDescription": "Joe",
    "TownCity": "",
    "PostalCode": "",
    "StreetName": "",
    "StreetNumber": "",
    "Neighborhood": "",
    "ContactPhoneNumber": "",
    "ContactEmail": "",
    "PassportMembersAccess": 1 (check Enumerated values section below),
    "PassportEventsAccess": 1 (check Enumerated values section below),
    "PassportCommunityAccess": 1 (check Enumerated values section below),
    "PassportBlogPostsAccess": 1 (check Enumerated values section below),
    "MondayOpenTime": null,
    "MondayCloseTime": null,
    "TuesdayOpenTime": null,
    "TuesdayCloseTime": null,
    "WednesdayOpenTime": null,
    "WednesdayCloseTime": null,
    "ThursdayOpenTime": null,
    "ThursdayCloseTime": null,
    "FridayOpenTime": null,
    "FridayCloseTime": null,
    "SaturdayOpenTime": null,
    "SaturdayCloseTime": null,
    "SundayOpenTime": null,
    "SundayCloseTime": null,
    "MondayClosed": null,
    "TuesdayClosed": null,
    "WednesdayClosed": null,
    "ThursdayClosed": null,
    "FridayClosed": null,
    "SaturdayClosed": null,
    "SundayClosed": null,
    "SameOpeningTimes": null,
}
```

{% api-method method="put" host="https://spaces.nexudus.com/api" path="/sys/businesses" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
Updates and existing business.Required User Role: `business-edit`
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
{% api-method-parameter name="Name" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="DefaultLanguage" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SpaceWebsiteLanguageId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WebAddress" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="DefaultPaymentGatewayId" type="int" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TermsAndConditions" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ShortIntroduction" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="AboutUs" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Quote" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PrivacyPolicyUrl" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CookiePolicyUrl" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WebContact" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Address" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Phone" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Fax" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="EmailContact" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="CountryId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="CurrencyId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="SimpleTimeZoneId" type="int" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Last4Digits" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PreAuthLastError" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportChannels" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportPublished" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportSpaceName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportTagLine" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="VenueType" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Tags" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="NumberOfFloors" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FloorSpace" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FloorSpaceUnit" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Longitude" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Latitude" type="decimal?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportDescription" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TownCity" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PostalCode" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="StreetName" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="StreetNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="Neighborhood" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ContactPhoneNumber" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ContactEmail" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportMembersAccess" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportEventsAccess" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportCommunityAccess" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="PassportBlogPostsAccess" type="enum" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MondayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MondayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FridayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FridayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SundayOpenTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SundayCloseTime" type="int?" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="MondayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="TuesdayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="WednesdayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="ThursdayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="FridayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SaturdayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SundayClosed" type="bool" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="SameOpeningTimes" type="bool" required=false %}

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

> 🔒 Requires user role `business-edit`

```javascript
{
    "Name": "Joe",
    "DefaultLanguage": 1 (check Enumerated values section below),
    "SpaceWebsiteLanguage": 12345678,
    "WebAddress": "url",
    "DefaultPaymentGateway": 12345678,
    "TermsAndConditions": "TermsAndConditions",
    "ShortIntroduction": "",
    "AboutUs": "",
    "Quote": "Joe",
    "PrivacyPolicyUrl": "Joe",
    "CookiePolicyUrl": "Joe",
    "WebContact": "www.example.com",
    "Address": "Joe",
    "Phone": "0207768885828",
    "Fax": "0207768885828",
    "EmailContact": "me@example.com",
    "Country": 12345678,
    "Currency": 12345678,
    "SimpleTimeZone": 12345678,
    "Last4Digits": "0",
    "PreAuthLastError": "0",
    "PassportChannels": "null",
    "PassportPublished": null,
    "PassportSpaceName": "null",
    "PassportTagLine": "null",
    "VenueType": 1 (check Enumerated values section below),
    "Tags": "null",
    "NumberOfFloors": 1,
    "FloorSpace": 1,
    "FloorSpaceUnit": 1 (check Enumerated values section below),
    "Longitude": 1,
    "Latitude": 1,
    "PassportDescription": "Joe",
    "TownCity": "",
    "PostalCode": "",
    "StreetName": "",
    "StreetNumber": "",
    "Neighborhood": "",
    "ContactPhoneNumber": "",
    "ContactEmail": "",
    "PassportMembersAccess": 1 (check Enumerated values section below),
    "PassportEventsAccess": 1 (check Enumerated values section below),
    "PassportCommunityAccess": 1 (check Enumerated values section below),
    "PassportBlogPostsAccess": 1 (check Enumerated values section below),
    "MondayOpenTime": null,
    "MondayCloseTime": null,
    "TuesdayOpenTime": null,
    "TuesdayCloseTime": null,
    "WednesdayOpenTime": null,
    "WednesdayCloseTime": null,
    "ThursdayOpenTime": null,
    "ThursdayCloseTime": null,
    "FridayOpenTime": null,
    "FridayCloseTime": null,
    "SaturdayOpenTime": null,
    "SaturdayCloseTime": null,
    "SundayOpenTime": null,
    "SundayCloseTime": null,
    "MondayClosed": null,
    "TuesdayClosed": null,
    "WednesdayClosed": null,
    "ThursdayClosed": null,
    "FridayClosed": null,
    "SaturdayClosed": null,
    "SundayClosed": null,
    "SameOpeningTimes": null,
}
```

## Commands

Commands allow to perform actions against one or more business records. Some commands accept only one record while others can run an action for a number of records at the same time. Each command has metadata with information about how it can be used and the amount of records, if any, it needs to run.

> ```javascript
> {
>     "AppliesOnlyToMultipleEntities": false|true,
>     "AppliesOnlyToOneEntity": false|true,
>     "AppliesOnlyToTwoEntities": false|true,
>     ...
> }
> ```

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/businesses/commands" %}
{% api-method-summary %}
Commands
{% endapi-method-summary %}

{% api-method-description %}
Get all commands available to run for business records.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/businesses/runcommand" %}
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

> 🔒 Requires user role `business-edit`

## Enumerated values

### VisitedHelpItems:

> GET /api/utils/enums?name=eHelpItemFlag

### DefaultLanguage:

> GET /api/utils/enums?name=eLanguage

### VenueType:

> GET /api/utils/enums?name=eVenueType

### FloorSpaceUnit:

> GET /api/utils/enums?name=eFloorUnit

### PassportMembersAccess:

> GET /api/utils/enums?name=ePassportAccess

### PassportEventsAccess:

> GET /api/utils/enums?name=ePassportAccess

### PassportCommunityAccess:

> GET /api/utils/enums?name=ePassportAccess

### PassportBlogPostsAccess:

> GET /api/utils/enums?name=ePassportAccess

## Binary files

The following endpoints return binary data. Check the `ContentType` header to understand the type of file being returned in the response stream.

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/businesses/getlogo/:id" %}
{% api-method-summary %}
Logo
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Business to get the logo for.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/businesses/getbannerimage/:id" %}
{% api-method-summary %}
BannerImage
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Business to get the bannerimage for.
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

{% api-method method="get" host="https://spaces.nexudus.com/api" path="/sys/businesses/getpassportbanner/:id" %}
{% api-method-summary %}
PassportBanner
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The id of the Business to get the passportbanner for.
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

* [Language](https://github.com/Nexudus/api-docs/tree/6c08c63d9c0c6779737ccfddc96f70c6623677d0/rest-api/sys/language.md)
* [Business](business.md)
* [PaymentGateway](https://github.com/Nexudus/api-docs/tree/6c08c63d9c0c6779737ccfddc96f70c6623677d0/rest-api/billing/paymentgateway.md)
* [Country](https://github.com/Nexudus/api-docs/tree/6c08c63d9c0c6779737ccfddc96f70c6623677d0/rest-api/sys/country.md)
* [Currency](currency.md)
* [SimpleTimeZone](simpletimezone.md)

