# Register

Track this event when user create a new account success:

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventIdentify](../tracking-event/log-event.md) |
| contextObject | [Context item]() |
| items | [List user item]() |

{% tabs %}
{% tab title="Swift" %}
```swift
let context = ITContextObj(screenName: "CreateAnAccountViewController")
let user = ITUserObj(userID: "62", username: "ants2020", firstName: "Nguyen", lastName: "An",
 address: "92 Nguyen Huu Canh", avatar: "https://www.dataimage.com/profile_image",
 birthday: "1992-12-12", email: "Annl@antsprogrammatic.com", gender: "Male", 
 phone: "0382992070" customerID: "211")
ITAnalytic.logEvent(action: .ITActionEventIdentify, contextObject: context, items: [user])
```
{% endtab %}
{% endtabs %}

