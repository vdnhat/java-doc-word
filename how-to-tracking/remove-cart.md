# Remove cart

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventRemoveCart](../tracking-event/log-event.md) |
| contextObject | [Context item]() |
| items | [List product will remove from cart]() |

{% tabs %}
{% tab title="Swift" %}
```swift
let context = ITContextObj(screenName: "CartDataViewController")
ITAnalytic.logEvent(action: .ITActionEventRemoveCart, contextObject: context, items: self.convertCartProductToItemTracking(cartProducts: cartViewModal.cartModel.cartProducts))

func convertCartProductsToItemTracking(cartProducts: [ProductList]) -> [ITProductObj] {
    var itemsTracking = [ITProductObj]()
    if cartProducts.count > 0 {
            for prd in cartProducts {
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

