# Sign In

This event should be sent when a user sign in for your service.

| **Parameters** | **Content** |
| :--- | :--- |
| categoryName | String |
| actionName | String |
| extra | Dictionary |

**Example:**

{% tabs %}
{% tab title="Swift" %}
```swift
CDP365Analytic.logEvent(categoryName: "user", actionName: "sign_in", extra: [
  "phone": "09xx", //PHONE_NUMBER_VALUE
  "customer_id": "1234567890123456" // CARD_NUMBER_ID_VALUE
])
```
{% endtab %}

{% tab title="Objective C" %}
```
[CDP365Analytic logEventWithCategoryName: @ "user"
  actionName: @ "sign_in"
  items: nil
  extra: @ {
    @ "phone": @ "09xx", @ "customer_id": @ "1234567890123456"
  }
  dimension: nil
];
```
{% endtab %}
{% endtabs %}



