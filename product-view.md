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
        "name": "Samsung Tivi 32 inch"
        "sku": "5261971730647",
        "brand": "Samsung",
        "main_category": "Điện tử - Điện Lạnh",
        "category_level_1": "Tivi",
        "category_level_2": "Tivi samsung",
        "price": 4999000,
        "quantity": 1,
        "image_url": "http://...",
        "page_url": "http://..."
    }]
    dims: {shop:{"id":"sh1","name":"Shop HCM"},warehouse:{"id":"wh1","name":"Kho HCM"}},
});
```



