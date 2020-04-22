---
description: User viewed a product detail (PDP)
---

# Product view

Function 

```javascript
web_event.track("product", "view", {
    items: [{list products properties}],
    dims: {the relation items} // option
});
```

Sample data for event product has viewed 

```javascript
web_event.track("product", "view", {
    items: [{
        "type": "product",
        "id": "864115",
        "sku": "5261971730647",
        "brand": "Samsung",
        "seller_id": "11315",
        "category": "Điện Tử - Điện Lạnh/Tivi/Tivi 4K",
        "price": 4999000,
        "quantity": 1
    }],
    dims: {shop:{"id":"sh1","name":"Shop HCM"},warehouse:{"id":"wh1","name":"Kho HCM"}},
});
```



