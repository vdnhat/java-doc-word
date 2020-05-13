---
description: User viewed a product list or category (optional)
---

# Product List Viewed

Function 

```javascript
web_event.track("browsing", "product_list_view", {
    items: [{list products properties}], // option
    dims: {the relation items}, // option
    extra:  {the extra properties}
});
```

Sample data for event browsing products when user viewed a product list or category

```javascript
web_event.track("browsing", "product_list_view", {
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
    },
    {
        "type": "product",
        "id": "864116",
        "name": "Samsung Tivi 40 inch"
        "sku": "5261971730648",
        "brand": "Samsung",
        "main_category": "Điện tử - Điện Lạnh",
        "category_level_1": "Tivi",
        "category_level_2": "Tivi samsung",
        "price": 5099000,
        "quantity": 1,
        "image_url": "http://...",
        "page_url": "http://..."
    }
    ]
});
```

