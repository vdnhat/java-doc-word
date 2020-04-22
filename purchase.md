---
description: User purchased and completed the order
---

# Purchase

Function 

```javascript
web_event.track("product", "payment", {
    items: [{list products properties}],
    dims: {the relation items} // option
});
```

Sample data for event after user purchased and completed the order.  

```javascript
web_event.track("product", "purchase", {
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
        },
        delivery: {
            "id": "124",
            "name": "Giao tận nhà"
        },
        shop: {
            "id": "sh1",
            "name": "Shop HCM"
        },
        warehouse: {
            "id": "wh1",
            "name": "Kho HCM"
        }

    },
    extra: {
        "order_id": "977895452",
        "revenue": 4999000,
        "discount_amount": 0,
        "promotion_code": ""
    }
});
```

