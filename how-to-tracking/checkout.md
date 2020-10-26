# Checkout

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventProductCheckout](../tracking-event/log-event.md) |
| contextObject | [Context item]() |
| extraObject | [Extra item]() |
| items | [List product item]() |

```swift
let context = ITContextObj(screenName: "CheckoutDataViewController")
let extra = ITExtraObj(revenue: 320,
                discountAmount: 12,
                promotionCode: "ANTSSOMI",
                tax: 7,
                deliveryCost: 21)
ITAnalytic.logEvent(action: .ITActionEventProductCheckout, 
                contextObject: context, extraObject: extra, items: 
                self.convertProductsToItemTracking(products:productList))
```

