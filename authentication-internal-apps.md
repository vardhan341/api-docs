---
description: >-
  If your application is not going to be published or used by other users than
  you or the people in your organisation then you can use a simpler way of
  authentication.
---

# Authentication \(internal apps\)

Instead of using the application key and the secret key, you can use your regular username and password. Any API calls using this authentication method will run in the context of the user making the call, and therefore inherit all the roles of that user.

{% hint style="warning" %}
Applications using this authentication method cannot be published in the App market as they would require your users to provide their username and password to the application developer.
{% endhint %}

In order to use the internal authentication your user must be granted API access. You can do this by accessing the user details from the [users list](https://spaces.nexudus.com/sys/users), clicking on the “Status” tab and enabling the option “API Access”

## Creating the authentication token

This authentication method doesn't need a calculated authentication token. Simply add a valid HTTP authentication header using your email and password

```csharp
var uri = "https://spaces.nexudus.com/api/business"
var client = new HttpClient(uri);
client.DefaultHeaders.Authorization = Credential.CreateBasic(email, password);
```

If you need to manually create the value header, it's calculated by Base64 encoding the string username:password. The username is the email of the user accessing your application \(parameter e\) and the password is the token you created following the steps above.

