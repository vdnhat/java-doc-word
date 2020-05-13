---
description: User clicked on a product
---

# Product click

Function 

```javascript
web_event.track("product", "click", {
    items: [{list products properties}],
    dims: {the relation items} // option
});
```

Sample data for event product click 

```javascript
web_event.track("product", "click", {
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
});
```



