---
description: >-
  The API uses a dynamic throttle which ensures everyone can enjoy the service
  and no one takes over by making many requests which will slow down responses
  to other users.
---

# Request Limits

Best practices suggest that you should always throttle any requests to API services. There is a great how-to for you C\# devs here: [http://joelfillmore.com/throttling-web-api-calls/](http://joelfillmore.com/throttling-web-api-calls/). Other languages should use a similar approach.

When you request has been throttled you will receive a message like this:

```text
409: "You must wait before accessing this url again."
```

The HTTP status you will get back is 409 Conflict.

```text

HTTP/1.1 409 You must wait before accessing this url again.
Cache-Control: no-cache
Pragma: no-cache
Expires: -1
Retry-After: 1
Date: Wed, 21 May 2014 01:54:48 GMT
Content-Length: 0

```

Consider the following javascript code that takes advantage of the "Retry-After" response header to repeat an API request.

```javascript
function getContent(id) {
 $.ajax('api/content/article/' + id)
  .success(function(data) {
      handleContentData(data);
  })
  .error(function(xhr, textStatus, errorThrown) {
      if (xhr.status == 409) {
          var delay = request.getResponseHeader('Retry-After');
          if (delay) {
              //re-try again in "delay" seconds
              setTimeout('getContent("' + id + '");', delay * 1000);
          }
      } else {
          //handle other errors...
      }
  });
}
```

