---
description: User added a product to compare.
---

# Add compare

Function 

```javascript
web_event.track("product", "add_compare", {
    items: [{list products properties}]
});
```

Sample data for event product has added to cart 

```javascript
web_event.track("product", "add_compare", {
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

![](.gitbook/assets/3.png)

