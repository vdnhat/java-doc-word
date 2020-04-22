---
description: User added payment information
---

# Payment Info Entered

Function 

```javascript
web_event.track("product", "payment", {
    items: [{list products properties}],
    dims: {the relation items} // option
});
```

Sample data for event after user has entered payment method  

```javascript
web_event.track("product", "payment", {
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
    dims: {
        payment: {
            "id": "1",
            "name": "Online payment"
        }
    },
});
```

