---
description: API to import a list product feeds to CDP system
---

# API Product feeds

{% api-method method="post" host="https://api.cdp.asia" path="/be/item" %}
{% api-method-summary %}
Import product Item 
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="token" type="string" required=true %}
Private key API for each Portal / Client    
\(Request to help desk admin CDP to get token\)
{% endapi-method-parameter %}

{% api-method-parameter name="item\_type" type="string" required=true %}
  **product**
{% endapi-method-parameter %}

{% api-method-parameter name="scope" type="string" required=true %}
**upsert** is ****using fixed value
{% endapi-method-parameter %}

{% api-method-parameter name="portal\_id" type="string" required=true %}
Portal  ID   
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
List items successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "msg": "success. list size:1",
    "status": true,
    "data": {
        "lost_time": "48ms",
        "version": "20200227"
    },
    "code": 200
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Item type is not found.
{% endapi-method-response-example-description %}

```
{
    "msg": "itemType is not found. portal_id:561236459, item_type:nhatvd1",
    "status": false,
    "code": 0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> Using product properties to set for data post body request

{% page-ref page="product-properties.md" %}

###  Sample import list products 

 **1. API request** 

```http
https://api.cdp.asia/be/item?scope=upsert&portal_id=PORTAL_ID&token=YOUR_&item_type=product
```

### 2. Data  

```bash
[
{
"type":"product",
"id":"864115",
"name":"Samsung Tivi 32 inch",
"sku":"5261971730647",
"brand":"Samsung",
"main_category":"Điện Tử - Điện Lạnh",
"category_level_1":"Tivi",
"category_level_2":"Tivi samsung",
"price":4999000,
"currency":"vnd",
"image_url":"http://antsomi.com/img.png",
"page_url":"http://antsomi.com/product1",
"key1":"value1",
"keyn":"valuen"
},
{
"type":"product",
"id":"864116",
"name":"Samsung Tivi 40 inch",
"sku":"5261971730648",
"brand":"Samsung",
"category":"Điện Tử - Điện Lạnh/Tivi/Tivi samsung",
"price":5099000,
"currency":"vnd",
"image_url":"http://antsomi.com/img.png",
"page_url":"http://antsomi.com/product1",
"key1":"value1",
"keyn":"valuen"
}
]
```

