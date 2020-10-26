# Product list search

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventProductSearch](../tracking-event/log-event.md) |
| contextObject | [Context item]() |
| extraObject | [Extra item]() |
| items | [List product item which searched by keyword]() |

{% tabs %}
{% tab title="Swift" %}
```swift
let context = ITContextObj(screenName: "SearchDataViewController")
let extra = ITExtraObj(searchTerm: "watch")
ITAnalytic.logEvent(action: .ITActionEventProductSearch, contextObject: context, extraObject: extra, items: self.convertProductsToItemTracking(products: productList))

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
{% endtab %}
{% endtabs %}

