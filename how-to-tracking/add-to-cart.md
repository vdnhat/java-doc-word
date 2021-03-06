# Add to cart

| **Parameters** | **Content** |
| :--- | :--- |
| action | [ITActionEventAddToCart](../tracking-event/log-event.md) |
| contextObject | [Context item](../tracking-parameters/context-param.md) |
| items | [List product will add to cart](../tracking-parameters/items-param.md#creating-an-itproductobj-object) |

{% tabs %}
{% tab title="Swift" %}
```swift
let context = ITContextObj(screenName: "ProductPageDataViewController")
var options = [ITOptionObj]()
let size = ITOptionObj(optionName: "size", optionValue: "SS")
options.append(size)
let product = ITProductObj(productID: "21",
                   productName: "Luna Analog Watch",
                   productDescription: "Designed to stand up to your active lifestyle, this women's Luma Analog Watch features a tasteful brushed chrome finish and a stainless steel, water-resistant construction for lasting durability.",
                   SKU: "24-WG09",
                   price: 44,
                   quantity: 0,
                   brand: "Luna",
                   category: "Home/ListProduct/ProductDetail",
                   variant: "Gray",
                   imageURL: "https://magento.antsomi.com/media/catalog/product/cache/f0fbff4a5f7972cd5749243e72ffc851/w/g/wg09-gr-0.jpg",
                   productURL: "https://magento.antsomi.com/index.php/luma-analog-watch.html",
                   coupon: "ANTSSOMI",
                   sellerID: "",
                   options: options)
ITAnalytic.logEvent(action: .ITActionEventAddToCart, contextObject: context, items: [product])
```
{% endtab %}
{% endtabs %}

