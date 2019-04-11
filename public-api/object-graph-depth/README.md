# Object Graph Depth

The PUBLIC API always returns JSON formatted data. By default, we will return data for 2 levels of the object hierarchy. This should be enough for most applications but sometimes you may need additinal levels and a deeper object graph.

```text
{
 Level1: {
  Level2: {
    Level3: { }
  }
}
```

In these cases, you can use the \_depth parameter to request a specific number of levels.

{% hint style="warning" %}
Use this with caution as additional levels of data will require additional processing and more data, which will basically degrade performance and make your requests hit the rate limits quicker.
{% endhint %}

