---
description: >-
  The Nexudus space PUBLIC API lets you implement applications that connect with
  the public and members areas of a Nexudus account.
---

# Public API

As opposed to the REST API, the PUBLIC API assumes you will be making non-authenticated requests or authenticated as the end user. I.e., you will be asking the end user for their username and password in your application and the API will return data in the context of that user

This works in the same exact way as the actual space website. Some pages in that website are publicly available whilst others are only available if there is a user logged in.

## How does it work?

The Nexudus Spaces PUBLIC API is implemented as JSON over HTTP/HTTPS using GET AND POST verbs. Unlike the REST API, no other verbs are allowed.

The API endpoints reflect the same exact URL as the space website. For example, if the home page of your Nexudus space website is xyz.spaces.nexudus.com, the API will have the same exact url. The way we decide whether to expect and return JSON instead of HTML is by using the Content-Type set to “application/json”

For example, you can get the JSON representation of the home page by making a request as follows:

```text
GET https://XYZ.spaces.nexudus.com/en
```

```javascript
Request Method: GET
Content-Type: application/json

Response Status Code: 200
Response Body:
{
  "HomePageMyAccount": true,
  "HomePageInvoices": true,
  "HomePageHelp": true,
  "HomePageBookings": true,
  "HomePageWall": true,
  "PublicDirectory": true,
  "HomePageNewsletterSignUp": false,
  "MembersSignUp": true,
  "ChepeastPlan": {
    "Name": "Early Bird",
    "GroupName": null,
    "Description": "<p>Getting started with coworking? This price plan lets you start to experience what coworking is about.</p>\r\n<div>Includes:<br />\r\n<div>\r\n<ul>\r\n<li>5 days of access to the space a month.</li>\r\n<li>60 minutes of meeting room use a month.</li>\r\n</ul>\r\n</div>\r\n</div>",
    "TermsAndConditions": "Legal Terms go here",
    "Price": "150.00",
    "PriceFormatted": "150.00€",
    "PriceDecimal": 150,
    "Currency": {},
    "InvoiceEvery": 36,
    "InvoiceEveryWeeks": 0,
    "TimePasses": [],
    "ExtraServices": [
      {}
    ],
    "BookingCredits": [],
    "InvoiceInMonths": true,
    "InvoicePeriod": 36,
    "Id": 450450,
    "IdString": "450450",
    "CreatedOn": "2012-02-25T09:13:38Z",
    "UniqueId": "8bc0276c-0400-4b9c-b2fa-8ce4157551f9",
    "IsNull": false
  },
  "PricePlans": [
    {
      "Name": "Early Bird",
      "GroupName": null,
      "Description": "<p>Getting started with coworking? This price plan lets you start to experience what coworking is about.</p>\r\n<div>Includes:<br />\r\n<div>\r\n<ul>\r\n<li>5 days of access to the space a month.</li>\r\n<li>60 minutes of meeting room use a month.</li>\r\n</ul>\r\n</div>\r\n</div>",
      "TermsAndConditions": "Legal Terms go here",
      "Price": "150.00",
      "PriceFormatted": "150.00€",
      "PriceDecimal": 150,
      "Currency": {},
      "InvoiceEvery": 36,
      "InvoiceEveryWeeks": 0,
      "TimePasses": [],
      "ExtraServices": [
        {}
      ],
      "BookingCredits": [],
      "InvoiceInMonths": true,
      "InvoicePeriod": 36,
      "Id": 450450,
      "IdString": "450450",
      "CreatedOn": "2012-02-25T09:13:38Z",
      "UniqueId": "8bc0276c-0400-4b9c-b2fa-8ce4157551f9",
      "IsNull": false
    }
  ],
  "Products": [
    {
      "Name": "10 day pass bundle",
      "Description": "10 day pass bundle http://nexudus.spaces.nexudus.com/en/page/custom-pages",
      "Tags": null,
      "Price": 300,
      "PriceFormatted": "$300.00",
      "HasTimePasses": true,
      "Currency": {},
      "Quantity": 0,
      "RegularCharge": false,
      "AlwaysRecurrent": false,
      "AlwaysOneOff": false,
      "Id": 17910893,
      "IdString": "17910893",
      "CreatedOn": "2014-07-22T19:41:03Z",
      "UniqueId": "6584f05c-5790-4ff8-9625-dfd3a93ace7a",
      "IsNull": false
    },
    {
      "Name": "Estacionamiento",
      "Description": "Estacionamiento",
      "Tags": "estacionamiento",
      "Price": 10,
      "PriceFormatted": "$10.00",
      "HasTimePasses": false,
      "Currency": {},
      "Quantity": 0,
      "RegularCharge": false,
      "AlwaysRecurrent": false,
      "AlwaysOneOff": false,
      "Id": 160102946,
      "IdString": "160102946",
      "CreatedOn": "2016-03-14T18:35:51Z",
      "UniqueId": "0a5471cc-321f-4af5-bd92-2ae0082ab6a3",
      "IsNull": false
    },
    {
      "Name": "1 day pass",
      "Description": "Access to the space for 1 day",
      "Tags": null,
      "Price": 15,
      "PriceFormatted": "$15.00",
      "HasTimePasses": true,
      "Currency": {},
      "Quantity": 0,
      "RegularCharge": false,
      "AlwaysRecurrent": false,
      "AlwaysOneOff": false,
      "Id": 14423409,
      "IdString": "14423409",
      "CreatedOn": "2014-04-13T22:40:46Z",
      "UniqueId": "8243019d-c43e-47a4-8bc6-32c3b77b0259",
      "IsNull": false
    },
    {
      "Name": "Private Parking Slot",
      "Description": "Reserve a space in the secure underground parking.",
      "Tags": null,
      "Price": 225,
      "PriceFormatted": "$225.00",
      "HasTimePasses": false,
      "Currency": {},
      "Quantity": 0,
      "RegularCharge": false,
      "AlwaysRecurrent": false,
      "AlwaysOneOff": false,
      "Id": 14050037,
      "IdString": "14050037",
      "CreatedOn": "2014-04-05T11:56:55Z",
      "UniqueId": "217c663c-419a-4573-b9b5-0b9d20627a70",
      "IsNull": false
    },
    {
      "Name": "Ten 1-day Passes",
      "Description": "Access the space 10 days",
      "Tags": null,
      "Price": 250,
      "PriceFormatted": "$250.00",
      "HasTimePasses": true,
      "Currency": {},
      "Quantity": 0,
      "RegularCharge": false,
      "AlwaysRecurrent": false,
      "AlwaysOneOff": false,
      "Id": 14050038,
      "IdString": "14050038",
      "CreatedOn": "2014-04-05T12:27:28Z",
      "UniqueId": "5a92723c-1220-45d5-ac75-f50a48dc148a",
      "IsNull": false
    }
  ],
  "ProductTags": [
    [
      {
        "Name": "Estacionamiento",
        "Description": "Estacionamiento",
        "Tags": "estacionamiento",
        "Price": 10,
        "PriceFormatted": "$10.00",
        "HasTimePasses": false,
        "Currency": {},
        "Quantity": 0,
        "RegularCharge": false,
        "AlwaysRecurrent": false,
        "AlwaysOneOff": false,
        "Id": 160102946,
        "IdString": "160102946",
        "CreatedOn": "2016-03-14T18:35:51Z",
        "UniqueId": "0a5471cc-321f-4af5-bd92-2ae0082ab6a3",
        "IsNull": false
      }
    ]
  ],
  "HomeBlogPosts": [],
  "BannerBlogPosts": [],
  "HomeEvents": [],
  "BannerEvents": []
}
```



## Structure

The API has a set of endpoints for each of the pages in the space website.

* Home Page: GET /en
* About Us: GET /en/about
* Help: GET /en/support
* Events: GET /en/events
* Bookings: GET /en/bookings
* Resources: GET /en/publicresources
* Directory: GET /en/directory
* Community Board: GET /en/community
* My Profile: GET /en/profile
* Payments: GET /en/invoices
* Price Plans: GET /en/profile/tariff
* Allowances: GET /en/allowances
* Store: GET /en/store/products



