# Make A Purchase

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventProductPurchase](../tracking-event/log-event.md) |
| contextObject | [Context item](../tracking-parameters/context-param.md) |
| extraObject | [Extra item](../tracking-parameters/extra-param.md) |
| dimsObject | [Dimension item](../tracking-parameters/dimension-param.md) |
| items | [List product item](../tracking-parameters/items-param.md#creating-an-itproductobj-object) |

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

