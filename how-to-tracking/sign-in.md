# Sign In

This event should be sent when a user sign in for your service.

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventIdentify](../tracking-event/log-event.md) |
| contextObject | [Context item](../tracking-parameters/context-param.md) |
| items | [List user item](../tracking-parameters/items-param.md#creating-an-ituserobj-object) |

{% tabs %}
{% tab title="Swift" %}
```swift
let context = ITContextObj(screenName: "SignInViewController")
let user = ITUserObj(username: "ants2020", email: "Annl@antsprogrammatic.com", customerID: "211")
ITAnalytic.logEvent(action: .ITActionEventIdentify, contextObject: context, items: [user])
```
{% endtab %}
{% endtabs %}



