---
description: >-
  When users install your application in their account, the level of access that
  you (as the application developer) have to their account is controlled by the
  roles you assign to it.
---

# Access Rights and Roles

{% hint style="info" %}
This only applies to published apps, not internal apps
{% endhint %}

Before users install your application they are presented with a screen showing these roles. If they agree to install your application then the API calls you can make will be restricted to those roles

If you change the roles of your application after users have installed it, they will be asked again to approve those roles the next time they access your application. Until then, you won't have access to their accounts, not even based on the old roles.

{% hint style="warning" %}
Some roles may require us to manually approve your application before it can be installed by any user.
{% endhint %}

