# Reset Anonymous ID

 The `reset` method clears the SDK’s internal stores for the current user id. This is useful for apps where users can log in and out with different identities over time.

{% tabs %}
{% tab title="Swift" %}
```swift
ITAnalytic.resetAnonymousID()
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
[ITAnalytics resetAnonymousID];
```
{% endtab %}
{% endtabs %}

**Note**: Each time you call `reset`, a new AnonymousID is generated the next time the app is opened.  


