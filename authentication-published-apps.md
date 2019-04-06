---
description: >-
  The API for Nexudus Spaces uses a combination of a App Key and a App secret to
  authenticate your requests. All requests to the API must be authenticated.
---

# Authentication \(published apps\)

To make a request to the API you will need to issue a HTTP request using the appropiate VERB and always including a Basic Authentication header.

```text
Request Headers:
Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==
```

To calculate this token you need to use the application Id and application secret that you can find in each of the applications you have created in your account. Click [here](https://spaces.nexudus.com/Apps/applications) to see a list of the applications in your account or to create a new application.

[![](http://help.spaces.nexudus.com/content/images/captures/app-secret-en.png)](http://help.spaces.nexudus.com/content/images/captures/app-secret-en.png)

Each application running on Nexudus Spaces has a key and a secret. It is very important that you never share your application secret, doing so will mean that someone could access all the accounts which installed your application on your behalf.

Create a manage your applications click [here](https://spaces.nexudus.com/Apps/applications)

{% hint style="warning" %}
Never share your secret key!
{% endhint %}

## Creating the authentication token

To create the authentication token you will need to combine the information you know about your application, such as its key and secret, with a piece of information we provide to you when an user installs your application in their account.

When creating an application, we will ask you for an URL. This address is where we will send that piece of information, and usually, where your application will be hosted.

[![](http://help.spaces.nexudus.com/content/images/captures/install-url-en.png)](http://help.spaces.nexudus.com/content/images/captures/install-url-en.png)

In the example above, when users install your app, we will ask them if they are happy to install your app, and if so, we will redirect them to "http://myapp.com/Install" and provide you with the bit of data you need to create the authentication token.

[![](http://help.spaces.nexudus.com/content/images/captures/access-request-en.png)](http://help.spaces.nexudus.com/content/images/captures/access-request-en.png)  


If the user accepts to install your application, then we will make a request to the "Install Url" with the following parameters:

```text
http://myapp.com//Install?
  a=d420667525e0489d91068cbf732fe1dc&
  t=c90e30fca71a4c37810a292b99d4d4f2&
  d=634963729314011098&
  h=785a10afef749b1c26cc3c5eb3989082&
  b=subdomain&
  e=user_email@example.com
```

* a: is your application key.
* t: is a token you will need to generate the authentication token.
* d: a number representing the current time
* h: a MD5 hash of t\|a\|date in alphabetical + your secret.
* b: your Nexudus Spaces subdomain
* e: the email of the user installing your application

When receiving this request, your application should check that the request is legitimate. You do this by recalculating the hash yourself and then checking that it matches the h paremeter your received from our servers.

```csharp
//Calculate hash
var param = new[] {token, app, date};
param = param.OrderBy(x => x).ToArray();
var calculatedHash = (string.Join("|", param) + secret).MD5();

//Check if the request is valid
var valid = (calculatedHash == hash);
```

Once you know the request is coming from Nexudus Spaces, you can create the authentication token. This token will allow you to make requests to the API. To create the token concatenate the token your received \(t\) and the secret, then MD5 hash that string.

```csharp
var authToken = (token + secret).MD5();
```

Now that we have the authentication token we can make requests to the API. For each request, you will need to make sure that you add an authentication header.

```csharp
var uri = "https://spaces.nexudus.com/api/businesses"
var client = new HttpClient(uri);
client.DefaultHeaders.Authorization = Credential.CreateBasic(username, password);
```

If you need to manually create the value header, it's calculated by Base64 encoding the string username:password. The username is the application key \(not the secret!\) and the password is the token you created following the steps above.

