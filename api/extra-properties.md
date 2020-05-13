# Extra properties

Extra is a dictionary of extra information that provides useful such as e-com properties 

| **STT** | **Field**  | **Type** | **Description** | Sample |
| :--- | :--- | :--- | :--- | :--- |
| 1 | `order_id` | String | User's order ID |  |
| 2 | `revenue` | Number | Total gross merchandise value \(in VND, USD,...\) of the order.  | 1000000 |
| 3 | `discount_amount` | Number | Total discount value \(in VND, USD,..\) of the order | 10000 |
| 4 | `promotion_code` | String | The coupon code that is used in the order |  |
| 5 | `tax` | Number | Percent  of tax  \(%\) | 10 |
| 6 | `delivery_cost` | Number | Cost of delivery value \(in VND, USD,..\)  | 200000 |
| 7 | `src_search_term` | String | Search term that leads to this product view |  |
| 8 | `any_fields...` | Any | Any fields to add to extra |  |

#### Data structure sample

```javascript
extra: {
        "order_id": "977895452",
        "revenue": 4999000,
        "discount_amount": 0,
        "promotion_code": ""
    }
```

