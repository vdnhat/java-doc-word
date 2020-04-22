---
description: Properties for item type product
---

# Product properties

| **Field** | Required | **Type** | **Description** |
| :--- | :--- | :--- | :--- |
| `id` |  yes | String | Product id |
| `type` | yes | String | product |
| `name` |  | String | Name of the product |
| `sku` |  | String | SKU of the product |
| `price` |  | Double | Price \(VND, USD,...\) of the product. |
| `curency` |  | String | VND, USD,... |
| `quantity` |  | Object | Quantity of a product. |
| `brand` |  | String | Brand associated with the product |
| `main_category` |  | String | Product main category |
| `category_level_1` |  | String | Category level 1 |
| `category_level_2` |  | String | Category level 2 |
| `variant` |  | String | Variant of the product \(e.g. Black\) |
| `image_url` |  | String | Image url of the product.  |
| `page_url` |  | String | URL of the product page. |
| `coupon` |  | String | Coupon code associated with a product \(e.g MAY\_DEALS\_3\) |
| `attribute_1` |  | type 1 | Other product attributes  |
| `attribute_n` |  | type  | Other product attributes  |

#### Data structure sample

```javascript
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
```

