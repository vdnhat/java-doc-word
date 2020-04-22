---
description: User searched for products  (optional)
---

# Products Searched

Function 

```javascript
web_event.track("browsing", "product_search", {
    items: [{list products properties}], // option
    dims: {the relation items}, // option
    extra:  {the extra properties}
});
```

Sample data for event browsing products after user searched  by a keyword  

```javascript
web_event.track("browsing", "product_search", {
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
    extra: {
        "src_search_term":"tivi samsung" // search keyword
    } 
});
```

