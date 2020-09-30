---
description: >-
  Extra is a object of extra information that provides useful such as e-com
  properties
---

# Extra Param

#### Creating an Extra object <a id="creating-an-extra-object"></a>

Each event has fields revenue, order\_id,..are available. You will need to create an Extra object and fill out the extra property:

{% tabs %}
{% tab title="Swift" %}
```swift
let extraObject = ITExtraObj(orderID: <String>, revenue: <Float>, 
discountAmount: <Float>, promotionCode: <String>, tax: <String>, 
deliveryCost: <Float>, searchTerm: <String>, pushNotificationID: <String>)
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
ITExtraObj *extra = [[ITExtraObj alloc] initWithOrderID: @"order id"
revenue:revenue value
discountAmount:discount amount value
promotionCode:@"promotion code"
tax:@"tax "
deliveryCost:delivery cost value
searchTerm:@"search term"
pushNotificationID:@"push notification service id"];
```
{% endtab %}
{% endtabs %}

#### Extra Properties <a id="extra-properties"></a>

| **Name** |  **Type** |  **Description** |  **Default** |
| :--- | :--- | :--- | :--- |
| orderID | String | User's order ID | null |
| revenue | Float | Total gross merchandise value of the order | 0.0 |
| discountAmount | Float | Total discount value of there order | 0.0 |
| promotionCode | String | The coupon code that is used in the order | null |
| tax | String | Percent of tax | null |
| deliveryCost | Float | Cost of delivery value | 0.0 |
| searchTerm | String | Search term that leads to this product view | null |
| pushNotificationID | String | Service push notification ID. Example: Onesignal ID,.. | null |

