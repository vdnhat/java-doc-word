# Make A Purchase

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventProductPurchase](../tracking-event/log-event.md) |
| contextObject | [Context item]() |
| extraObject | [Extra item]() |
| dimsObject | [Dimension item]() |
| items | [List product item]() |

{% tabs %}
{% tab title="Swift" %}
```swift
let context = ITContextObj(screenName: "OrderPlaceViewController")
var dims = [ITDimsObj]()
let dim = ITDimsObj(itemCategory: "payment", itemID: "CheckMo", itemName: "Check / Money ")
dims.append(dim)
let extra = ITExtraObj(orderID: "121",
           revenue: 320,
           discountAmount: 12,
           promotionCode: "ANTSSOMI",
           tax: 7,
           deliveryCost: 21)
ITAnalytic.logEvent(action: .ITActionEventProductPurchase, 
           contextObject: context, extraObject: extra, dimsObject: dims, 
           items: self.convertProductsToItemTracking(products:productList))
```
{% endtab %}
{% endtabs %}

