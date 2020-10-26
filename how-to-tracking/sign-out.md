# Sign Out

This event should be sent when a user sign out for your service.

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventSignOut](../tracking-event/log-event.md) |
| contextObject | [Context item]() |
| items | [List user item]() |

{% tabs %}
{% tab title="Swift" %}
```swift
let context = ITContextObj(screenName: "ProfileViewController")
let user = ITUserObj(userID: "62", username: "ants2020", firstName: "Nguyen", lastName: "An", 
address: "92 Nguyen Huu Canh", avatar: "https://www.dataimage.com/profile_image", birthday: "1992-12-12", 
email: "Annl@antsprogrammatic.com", gender: "Male", phone: "0382992070" customerID: "211")
ITAnalytic.logEvent(action: .ITActionEventSignOut, contextObject: context, items: [user])
```
{% endtab %}
{% endtabs %}

