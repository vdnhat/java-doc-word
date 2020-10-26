# Register

Track this event when user create a new account success:

| **Parameters** | **Content** |
| :--- | :--- |
| categoryName | String |
| actionName | String |
| items | List dictionary |
| extra | Dictionary |

**Example:**

{% tabs %}
{% tab title="Swift" %}
```swift
CDP365Analytic.logEvent(
  categoryName: "user",
  actionName: "sign_up",
  items: [
    [
      "item_id": "1234567890123456", // CARD_NUMBER_ID_VALUE
      "item_name": "Barack obama" // CARD_NAME
    ]
  ],
  extra: [
    "sign_up_type": "link_card",
    "phone": "09xxx",
    "first_name": "Barack",
    "last_name": "Obama",
    "email": "obama@antsomi.com",
    "customer_id": "1234567890123456" // CARD_NUMBER_ID_VALUE
  ])

```
{% endtab %}

{% tab title="Objective C" %}
```
[CDP365Analytic logEventWithCategoryName: @ "user"
  actionName: @ "sign_up"
  items: @[
    @ {
      @ "item_id": @ "1234567890123456", // CARD_NUMBER_ID_VALUE
        @ "item_name": @ "Barack obama" // CARD_NAME
    }
  ]
  extra: @ {
    @ "sign_up_type": @ "link_card",
      @ "phone": @ "09xxx",
      @ "first_name": @ "Barack",
      @ "last_name": @ "Obama",
      @ "email": @ "obama@antsomi.com",
      // CARD_NUMBER_ID_VALUE: 1234567890123456
      @ "customer_id": @ "1234567890123456"
  }
  dimension: nil
];

```
{% endtab %}
{% endtabs %}

