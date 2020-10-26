# Sign Out

This event should be sent when a user sign out for your service.

| **Parameters** | **Content** |
| :--- | :--- |
| categoryName | String |
| actionName | String |
| extra | Dictionary |

**Example:**

{% tabs %}
{% tab title="Swift" %}
```swift
CDP365Analytic.logEvent(categoryName: "user", actionName: "sign_out", extra: [
  "customer_id": "1234567890123456" // CARD_NUMBER_ID_VALUE: 1234567890123456
])
```
{% endtab %}

{% tab title="Objective C" %}
```
[CDP365Analytic logEventWithCategoryName: @ "user"
  actionName: @ "sign_out"
  items: nil
  extra: @ {
    @ "customer_id": @ "1234567890123456" // CARD_NUMBER_ID_VALUE: 1234567890123456
  }
  dimension: nil
];
```
{% endtab %}
{% endtabs %}



