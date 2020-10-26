# Allow push notification

When user allow the push notification service

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventAllowPushNotification](../tracking-event/log-event.md) |
| extraObject | [Extra item]() |

{% tabs %}
{% tab title="Swift" %}
```swift
let extra = ITExtraObj(pushNotificationID: "3c80bd93-ce53-4180-b423-8ae62b014f04")
ITAnalytic.logEvent(action: .ITActionEventAllowPushNotification, extraObject: extra)
```
{% endtab %}
{% endtabs %}

