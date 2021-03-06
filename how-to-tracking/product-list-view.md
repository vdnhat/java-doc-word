# Product list view

| **Parameters** | **Context** |
| :--- | :--- |
| action | [ITActionEventProductListView](../tracking-event/log-event.md) |
| contextObject | [Context item](../tracking-parameters/context-param.md) |
| items | [List product item](../tracking-parameters/items-param.md#creating-an-itproductobj-object) |

{% tabs %}
{% tab title="Swift" %}
```swift
let context = ITContextObj(screenName: "CategoryProductsViewController")
ITAnalytic.logEvent(action: .ITActionEventProductListView, contextObject: context, items: self.convertProductsToItemTracking(products:productList))

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

Copy  


