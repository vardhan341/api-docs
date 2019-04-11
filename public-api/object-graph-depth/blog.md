---
description: Returns the data available on the blog page.
---

# Blog

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/blog" %}
{% api-method-summary %}
Blog page
{% endapi-method-summary %}

{% api-method-description %}
Gets the data representing a list of blog posts.
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
{% api-method-parameter name="categoryId" type="integer" required=false %}
The id of the BlogPostCategory to show blog posts for.
{% endapi-method-parameter %}

{% api-method-parameter name="size" type="integer" required=false %}
the number of posts to return in every page. Defaults to 12. Same as 'top'
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=false %}
the page number. Defaults to 1.
{% endapi-method-parameter %}

{% api-method-parameter name="top" type="integer" required=false %}
the number of posts to return in every page. Defaults to 12. Same as 'size'
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "Top": 12,
  "Page": 1,
  "Size": 12,
  "BlogPosts": [
    {
      "Language": {},
      "PostedBy": {},
      "Title": "Test",
      "SummaryText": "Test",
      "FullText": "<p>Anoari as as</p>\r\n<p><strong><img style=\"border-width: 5px;\" src=\"http://nexudus.redirectme.net/images/adrianback.png\" alt=\"adrianback.png\" width=\"551\" height=\"369\" /></strong></p>\r\n<p><strong>asdasdas</strong></p>",
      "PublishDate": "2015-07-10T23:00:00",
      "AllowComments": true,
      "Comments": [
      ],
      "BlogCategories": [
      ],
      "HasImage": false,
      "HasLargeImage": false,
      "Id": 12581569,
      "IdString": "12581569",
      "UpdatedOn": "2016-08-14T23:24:03",
      "CreatedOn": "2015-07-12T18:14:58",
      "UniqueId": "95caba50-fdad-4d3c-be9d-bf3dda9a018e",
      "IsNull": false
    },
    {
      "Language": {},
      "PostedBy": {},
      "Title": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. The printing and typesetting industry.",
      "SummaryText": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. The printing and typesetting industry.",
      "FullText": "<p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. The printing and typesetting industry.</p>",
      "PublishDate": "2015-07-01T06:00:00",
      "AllowComments": true,
      "Comments": [],
      "BlogCategories": [],
      "HasImage": true,
      "HasLargeImage": false,
      "Id": 10954944,
      "IdString": "10954944",
      "UpdatedOn": "2016-07-02T11:39:34",
      "CreatedOn": "2015-03-29T23:12:48",
      "UniqueId": "ba506487-2fd4-4ac8-850b-61c8428228b6",
      "IsNull": false
    },
    {
      "Language": {},
      "PostedBy": {},
      "Title": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. The printing and typesetting industry.",
      "SummaryText": null,
      "FullText": "<p>Lorem Ipsum is simply dummy text of the printing and typesetting industry.</p>",
      "PublishDate": "2014-10-19T23:00:00",
      "AllowComments": true,
      "Comments": [
      ],
      "BlogCategories": [
      ],
      "HasImage": true,
      "HasLargeImage": true,
      "Id": 8459451,
      "IdString": "8459451",
      "UpdatedOn": "2016-08-14T20:18:08",
      "CreatedOn": "2014-10-26T16:20:32",
      "UniqueId": "6d866888-dc9d-47c9-afe5-0f761f6b2612",
      "IsNull": false
    }
  ],
  "CategoriesByPosts": [
    {
      "Language": {},
      "Title": "About us",
      "Id": 175175,
      "IdString": "175175",
      "UpdatedOn": "2013-07-31T21:33:21",
      "CreatedOn": "2012-09-21T22:19:06",
      "UniqueId": "73f65b03-eb6c-4f64-84f1-92e140255598",
      "IsNull": false
    },
    {
      "Language": {},
      "Title": "The space",
      "Id": 978978,
      "IdString": "978978",
      "UpdatedOn": "2014-01-18T19:26:08",
      "CreatedOn": "2013-07-31T21:36:31",
      "UniqueId": "f9b210eb-b106-4a55-9d1e-d4c5106ed704",
      "IsNull": false
    }
  ],
  "Categories": [
    {
      "Language": {},
      "Title": "About us",
      "Id": 175175,
      "IdString": "175175",
      "UpdatedOn": "2013-07-31T21:33:21",
      "CreatedOn": "2012-09-21T22:19:06",
      "UniqueId": "73f65b03-eb6c-4f64-84f1-92e140255598",
      "IsNull": false
    },
    {
      "Language": {},
      "Title": "The space",
      "Id": 978978,
      "IdString": "978978",
      "UpdatedOn": "2014-01-18T19:26:08",
      "CreatedOn": "2013-07-31T21:36:31",
      "UniqueId": "f9b210eb-b106-4a55-9d1e-d4c5106ed704",
      "IsNull": false
    }
  ],
  "Category": null
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/blog/:id/json" %}
{% api-method-summary %}
Blog post
{% endapi-method-summary %}

{% api-method-description %}
Gets the data representing a single blog post.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=false %}
the 'id' of the BlogPost to find.
{% endapi-method-parameter %}

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
{% api-method-parameter name="categoryId" type="integer" required=false %}
The id of the BlogPostCategory to show blog posts for.
{% endapi-method-parameter %}

{% api-method-parameter name="size" type="integer" required=false %}
the number of posts to return in every page. Defaults to 12. Same as 'top'
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=false %}
the page number. Defaults to 1.
{% endapi-method-parameter %}

{% api-method-parameter name="top" type="integer" required=false %}
the number of posts to return in every page. Defaults to 12. Same as 'size'
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "BlogPost": {
    "Language": {},
    "PostedBy": {},
    "Title": "Test",
    "SummaryText": "Test",
    "FullText": "<p>Anoari as as</p>\r\n<p><strong><img style=\"border-width: 5px;\" src=\"http://nexudus.redirectme.net/images/adrianback.png\" alt=\"adrianback.png\" width=\"551\" height=\"369\" /></strong></p>\r\n<p><strong>asdasdas</strong></p>",
    "PublishDate": "2015-07-10T23:00:00",
    "AllowComments": true,
    "Comments": [
      {},
      {}
    ],
    "BlogCategories": [
      {}
    ],
    "HasImage": false,
    "HasLargeImage": false,
    "Id": 12581569,
    "IdString": "12581569",
    "UpdatedOn": "2016-08-14T23:24:03",
    "CreatedOn": "2015-07-12T18:14:58",
    "UniqueId": "95caba50-fdad-4d3c-be9d-bf3dda9a018e",
    "IsNull": false
  },
  "Comments": [
    {
      "PostedBy": {},
      "Title": "asdasd asda",
      "Text": "asdasd asda",
      "Published": true,
      "Id": 15622607,
      "IdString": "15622607",
      "UpdatedOn": "2015-10-04T00:02:19",
      "CreatedOn": "2015-10-04T00:02:19",
      "UniqueId": "9ce320e6-eccd-47a8-9fb9-527659a718c3",
      "IsNull": false
    },
    {
      "PostedBy": {},
      "Title": "asdasd",
      "Text": "asdasd",
      "Published": true,
      "Id": 15622608,
      "IdString": "15622608",
      "UpdatedOn": "2015-10-04T00:02:23",
      "CreatedOn": "2015-10-04T00:02:23",
      "UniqueId": "17a5eda8-8b79-4a51-a0a2-a94c8f341d2d",
      "IsNull": false
    }
  ],
  "Comment": {
    "PostedBy": {},
    "Title": null,
    "Text": null,
    "Published": false,
    "Id": 0,
    "IdString": "0",
    "UpdatedOn": null,
    "CreatedOn": "2017-01-19T19:09:26",
    "UniqueId": "38de8cb1-c86d-48e0-afdd-ebce04b650c0",
    "IsNull": false
  },
  "RelatedPosts": [
    {
      "Language": {},
      "PostedBy": {},
      "Title": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. The printing and typesetting industry.",
      "SummaryText": null,
      "FullText": "<p>Lorem Ipsum is simply dummy text of the printing and typesetting industry.</p>",
      "PublishDate": "2014-10-19T23:00:00",
      "AllowComments": true,
      "Comments": [
        {},
        {},
        {},
        {}
      ],
      "BlogCategories": [
        {},
        {}
      ],
      "HasImage": true,
      "HasLargeImage": true,
      "Id": 8459451,
      "IdString": "8459451",
      "UpdatedOn": "2016-08-14T20:18:08",
      "CreatedOn": "2014-10-26T16:20:32",
      "UniqueId": "6d866888-dc9d-47c9-afe5-0f761f6b2612",
      "IsNull": false
    }
  ],
  "CategoriesByPosts": [
    {
      "Language": {},
      "Title": "About us",
      "Id": 175175,
      "IdString": "175175",
      "UpdatedOn": "2013-07-31T21:33:21",
      "CreatedOn": "2012-09-21T22:19:06",
      "UniqueId": "73f65b03-eb6c-4f64-84f1-92e140255598",
      "IsNull": false
    },
    {
      "Language": {},
      "Title": "The space",
      "Id": 978978,
      "IdString": "978978",
      "UpdatedOn": "2014-01-18T19:26:08",
      "CreatedOn": "2013-07-31T21:36:31",
      "UniqueId": "f9b210eb-b106-4a55-9d1e-d4c5106ed704",
      "IsNull": false
    }
  ],
  "Categories": [
    {
      "Language": {},
      "Title": "About us",
      "Id": 175175,
      "IdString": "175175",
      "UpdatedOn": "2013-07-31T21:33:21",
      "CreatedOn": "2012-09-21T22:19:06",
      "UniqueId": "73f65b03-eb6c-4f64-84f1-92e140255598",
      "IsNull": false
    },
    {
      "Language": {},
      "Title": "The space",
      "Id": 978978,
      "IdString": "978978",
      "UpdatedOn": "2014-01-18T19:26:08",
      "CreatedOn": "2013-07-31T21:36:31",
      "UniqueId": "f9b210eb-b106-4a55-9d1e-d4c5106ed704",
      "IsNull": false
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/blog/getImage/:id" %}
{% api-method-summary %}
Image
{% endapi-method-summary %}

{% api-method-description %}
Gets the small image of a blog post
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=false %}
the id of the BlogPost to return the image for.
{% endapi-method-parameter %}

{% api-method-parameter name="language" type="string" required=true %}
'en' or any other valid language in your account.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
binary. If no image is found a default image is returned. 
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



