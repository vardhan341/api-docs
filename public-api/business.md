# Business

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:langauge/business/getlogo" %}
{% api-method-summary %}
Logo
{% endapi-method-summary %}

{% api-method-description %}
Gets the current logo of the space. xyz represents you account subdomain as displayed in https://platform.nexudus.com/settings/website. You can upload the logo of a business from https://platform.nexudus.com/settings/general.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mode" type="string" required=false %}
The cropping mode to use when resizing the image. It can be one of:  
  
- None  
- Max  
- Pad  
- Crop \(default\)  
- Carve  
- Stretch
{% endapi-method-parameter %}

{% api-method-parameter name="h" type="number" required=false %}
The height of the image to return
{% endapi-method-parameter %}

{% api-method-parameter name="w" type="number" required=false %}
The width of the image to return
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Content-Type: image/png
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:langauge/business/getBanner" %}
{% api-method-summary %}
Banner
{% endapi-method-summary %}

{% api-method-description %}
Gets the current banner of the space. xyz represents you account subdomain as displayed in https://platform.nexudus.com/settings/website. You can update the logo of a business from https://platform.nexudus.com/settings/general.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mode" type="string" required=false %}
The cropping mode to use when resizing the image. It can be one of:  
  
- None  
- Max  
- Pad  
- Crop \(default\)  
- Carve  
- Stretch
{% endapi-method-parameter %}

{% api-method-parameter name="h" type="number" required=false %}
The height of the image to return
{% endapi-method-parameter %}

{% api-method-parameter name="w" type="number" required=false %}
The width of the image to return
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:langauge/business/getBanner/:id" %}
{% api-method-summary %}
Banner By Id
{% endapi-method-summary %}

{% api-method-description %}
Gets the banner of the space. xyz represents you account subdomain as displayed in https://platform.nexudus.com/settings/website. You can update the logo of a business from https://platform.nexudus.com/settings/general.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=false %}
The id of the location to get the banner for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="mode" type="string" required=false %}
The cropping mode to use when resizing the image. It can be one of:  
  
- None  
- Max  
- Pad  
- Crop \(default\)  
- Carve  
- Stretch
{% endapi-method-parameter %}

{% api-method-parameter name="h" type="number" required=false %}
The height of the image to return
{% endapi-method-parameter %}

{% api-method-parameter name="w" type="number" required=false %}
The width of the image to return
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:langauge/business/getLogo/:id" %}
{% api-method-summary %}
Logo By Id
{% endapi-method-summary %}

{% api-method-description %}
Gets the logo of the space. xyz represents you account subdomain as displayed in https://platform.nexudus.com/settings/website. You can update the logo of a business from https://platform.nexudus.com/settings/general.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=false %}
The id of the location to get the logo for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="mode" type="string" required=false %}
The cropping mode to use when resizing the image. It can be one of:  
  
- None  
- Max  
- Pad  
- Crop \(default\)  
- Carve  
- Stretch
{% endapi-method-parameter %}

{% api-method-parameter name="h" type="number" required=false %}
The height of the image to return
{% endapi-method-parameter %}

{% api-method-parameter name="w" type="number" required=false %}
The width of the image to return
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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

