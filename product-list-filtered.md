---
description: User filtered a product list or category
---

# Product List Filtered

Function 

```javascript
web_event.track("browsing", "product_list_filter", {
    items: [{list products properties}], // option
    dims: {the relation items}, // option
    extra:  {the extra properties}
});
```

Sample data for event browsing products when user viewed a product list or category

```javascript
web_event.track("browsing", "product_list_filter", {
    items: [{
        "type": "product",
        "id": "864115",
        "name": "Samsung Tivi 32 inch"
        "sku": "5261971730647",
        "brand": "Samsung",
        "seller_id": "11315",
        "category": "Điện Tử - Điện Lạnh/Tivi/Tivi samsung",
        "price": 4999000,
        "quantity": 1
    },
    {
        "type": "product",
        "id": "864116",
        "name": "Samsung Tivi 40 inch"
        "sku": "5261971730648",
        "brand": "Samsung",
        "seller_id": "11315",
        "category": "Điện Tử - Điện Lạnh/Tivi/Tivi samsung",
        "price": 5099000,
        "quantity": 1
    }
    ],
    dims: {category:{"id":"cate_id1", "name":"Tivi"}}
});
```

