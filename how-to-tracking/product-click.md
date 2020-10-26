# Product click

| **Parameters** | **Content** |
| :--- | :--- |
| categoryName | String |
| actionName | String |
| items | List dictionary |

**Example:**

{% tabs %}
{% tab title="Swift" %}
```swift
CDP365Analytic.logEvent(categoryName: "product", actionName: "click", items: [
  [
    "item_id": "12", // PRODUCT_ID: 12,123,124,.. etc
    "item_name": "Women discount 50%", // PRODUCT_NAME or TITLE
    "item_type": "product",
    "product_value": 20, // sample discount 20$
    "proudct_type": "clother" // types: free, discount, 50% off,...,etc
  ]
])
```
{% endtab %}

{% tab title="Objective C" %}
```
[CDP365Analytic logEventWithCategoryName: @ "product"
  actionName: @ "click"
  items: @[
    @ {
       @ "item_id": @ "12", // PRODUCT_ID: 12,123,124,.. etc
        @ "item_name": @ "Women discount 50%", // PRODUCT_NAME or TITLE
        @ "item_type": @ "product",
        @ "product_value": 20, // sample discount 20$
        @ "product_type": @ "clother" // types: free, discount, 50% off,...,etc
    }]
  extra: nil
  dimension: nil
];
```
{% endtab %}
{% endtabs %}



