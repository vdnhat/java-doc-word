---
description: User viewed their shopping cart
---

# Cart view

Function 

```javascript
web_event.track("product", "view_cart", {
    items: [{list products properties}],
    dims: {the relation items} // option
});
```

Sample data for event cart has viewed  

```javascript
web_event.track("product", "view_cart", {
    items: [{
        "type": "product",
        "id": "864115",
        "sku": "5261971730647",
        "brand": "Samsung",
        "seller_id": "11315",
        "category": "Điện Tử - Điện Lạnh/Tivi/Tivi 4K",
        "price": 4999000,
        "quantity": 1
    }]
});
```

