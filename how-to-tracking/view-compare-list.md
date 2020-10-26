# View compare list

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventProductViewCompare](../tracking-event/log-event.md) |
| contextObject | [Context item]() |
| items | [List product item]() |

{% tabs %}
{% tab title="Swift" %}
```swift
let context = ITContextObj(screenName: "CategoryProductsViewController")
ITAnalytic.logEvent(action: .ITActionEventProductViewCompare, contextObject: context, items: self.convertProductsToItemTracking(products:productList))

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

