---
description: Lets you work with files and media available to customers.
---

# Content

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/images/:name" %}
{% api-method-summary %}
Images
{% endapi-method-summary %}

{% api-method-description %}
Get an image file with specific dimensions.  
  
You can manage files in your account from https://platform.nexudus.com/templates   
- Images: https://platform.nexudus.com/templates/custom-files/image-files   
- Audio Files: https://platform.nexudus.com/templates/custom-files/audio-files   
- Image Gallery: https://platform.nexudus.com/templates/custom-files/image-gallery   
- Video Files: https://platform.nexudus.com/templates/custom-files/video-files   
- Other Files: https://platform.nexudus.com/templates/custom-files/other-files
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
the name of the image to return \(image-name.png, for example\)
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

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/audios/:name" %}
{% api-method-summary %}
Audios
{% endapi-method-summary %}

{% api-method-description %}
Get a audio file.  
  
You can manage files in your account from https://platform.nexudus.com/templates   
- Images: https://platform.nexudus.com/templates/custom-files/image-files   
- Audio Files: https://platform.nexudus.com/templates/custom-files/audio-files   
- Image Gallery: https://platform.nexudus.com/templates/custom-files/image-gallery   
- Video Files: https://platform.nexudus.com/templates/custom-files/video-files   
- Other Files: https://platform.nexudus.com/templates/custom-files/other-files
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
The name of the audio file to return.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/videos/:name" %}
{% api-method-summary %}
Videos
{% endapi-method-summary %}

{% api-method-description %}
Get a video file.  
  
You can manage files in your account from https://platform.nexudus.com/templates   
- Images: https://platform.nexudus.com/templates/custom-files/image-files   
- Audio Files: https://platform.nexudus.com/templates/custom-files/audio-files   
- Image Gallery: https://platform.nexudus.com/templates/custom-files/image-gallery   
- Video Files: https://platform.nexudus.com/templates/custom-files/video-files   
- Other Files: https://platform.nexudus.com/templates/custom-files/other-files
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
The name of the video file to return.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/files/:name" %}
{% api-method-summary %}
Files
{% endapi-method-summary %}

{% api-method-description %}
Gets a binary file.  
  
You can manage files in your account from https://platform.nexudus.com/templates   
- Images: https://platform.nexudus.com/templates/custom-files/image-files   
- Audio Files: https://platform.nexudus.com/templates/custom-files/audio-files   
- Image Gallery: https://platform.nexudus.com/templates/custom-files/image-gallery   
- Video Files: https://platform.nexudus.com/templates/custom-files/video-files   
- Other Files: https://platform.nexudus.com/templates/custom-files/other-files
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
The name of the audio file to return.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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



{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/ProposalFile/:guid" %}
{% api-method-summary %}
Proposal File
{% endapi-method-summary %}

{% api-method-description %}
Gets the binary file attached to a proposal.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="guid" type="string" required=true %}
The proposal UniqueId
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/CoworkerDataFile/:id" %}
{% api-method-summary %}
Data File
{% endapi-method-summary %}

{% api-method-description %}
Gets the binary file attached to a customer CRM module.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The proposal UniqueId
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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

🔓 This endpoint requires authentication. Make sure you submit authentication credentials valid for the customer the file to fetch is attached to.

{% api-method method="get" host="https://xyz.spaces.nexudus.com" path="/:language/:guid" %}
{% api-method-summary %}
Delivery Scan
{% endapi-method-summary %}

{% api-method-description %}
Gets the binary file attached to a delivery.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="guid" type="string" required=true %}
The delivery UniqueId
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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

