---
description: >-
  If your language of choice is C#, then the following SDK will run on any .NET
  or Mono platforms
---

# SDK

[Download SDK](http://help.spaces.nexudus.com/Content/files/Nexudus.Coworking.API.Connector.dll)   
[Download Support Libraries](http://help.spaces.nexudus.com/Content/files/nexudus-spaces-sdk-support-libraries.zip)

Here is a quick example of how to authenticate and request the list of bookings.

```csharp
var username = "youruser@example.com";
var password = "YourPassword1234";
if (Auth.IsValidAuth(username, password))
{
    var bookings = Bookings.List();
    var booking = Bookings.Get(bookings.Records[0].Id);

    Console.Write(booking.Resource.Name);
}
```

If you are running in the context of a Web Request, you can actually use the SDK to generate the authentication token for you. Here is an example:

```csharp
  //Try to validate the request
  var secret = "Your Application Key";
  
  //Validate the request and create the auth token
  var validRequest = Auth.Authenticate(secret);

  //If we could not validate the request, redirect to Nexudus spaces auth URL.
  if(!validRequest)
      return Redirect("Url To Login Page");

  var appKey = Auth.GetAppKey();
  var password = Auth.GetPassword();
  var username = string.Format("{0}:{1}", appKey, password);

  //Keep the auth token in the Forms Authentication Cookie for future requests
  FormsAuthentication.SetAuthCookie(username, false);

  return RedirectToAction("Url to your App Home Page");
```

