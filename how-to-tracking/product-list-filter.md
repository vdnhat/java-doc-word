# Product list filter



| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventProductListFilter](../tracking-event/log-event.md) |
| contextObject | [Context item]() |
| extraObject | [Extra item]() |
| items | [List product item which filtered by options]() |

```swift
let context = ITContextObj(screenName: "SearchDataViewController")
let extra = ITExtraObj(searchTerm: "analog")
ITAnalytic.logEvent(action: .ITActionEventProductListFilter, contextObject: context, extraObject: extra, items: self.convertProductsToItemTracking(products: productList))

func convertProductsToItemTracking(products: [ProductList]) -> [ITProductObj] {
    var itemsTracking = [ITProductObj]()
    if products.count > 0 {
            for prd in products {
                let productTracking = ITProductObj(productID: prd.productId,
                                                   productName: prd.name,
                                                   productDescription: prd.shortDescription,
                                                   SKU: prd.sku,
                                                   price: prd.finalPrice,
                                                   quantity: prd.quantity,
                                                   brand: prd.brand,
                                                   category: prd.category,
                                                   variant: prd.variant,
                                                   imageURL: prd.imageURL,
                                                   productURL: prd.productURL,
                                                   coupon: prd.coupon,
                                                   sellerID: "",
                                                   options: prd.options)

                itemsTracking.append(productTracking)

            }
   }

   return itemsTracking

}
```

