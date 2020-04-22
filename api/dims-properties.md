---
description: >-
  Dims is a dictionary of the relation items that provides . You should only use
  Dims types for their intended meaning.
---

# Dims properties

####  The  relation item types popularity

The relation items on events as shop, warehouse, payment method, delivery method...

| **Field** | Required | **Type** | **Description** |
| :--- | :--- | :--- | :--- |
| `id` | yes | String | Relation item id.  |
| `name` |  | String | Relation item name |

#### Data structure sample

```javascript
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

    }
```

