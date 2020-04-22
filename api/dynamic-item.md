---
description: API to import a list items to CDP system
---

# API Import Item

{% hint style="info" %}
Noted: Access to CDP admin tool to defined item and item attributes before call this api. 
{% endhint %}

{% api-method method="post" host="https://api.cdp.asia" path="/be/item" %}
{% api-method-summary %}
Import dynamic Item 
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
item types has defined on cdp admin tool. such as: product, shop,...
{% endapi-method-parameter %}

{% api-method-parameter name="scope" type="string" required=true %}
**upsert** is ****using fixed value
{% endapi-method-parameter %}

{% api-method-parameter name="portal\_id" type="string" required=true %}
Portal  ID    
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="attribute\_5" type="object" required=false %}
 The attributes type object. 
{% endapi-method-parameter %}

{% api-method-parameter name="attribute\_4" type="array" required=false %}
 some attributes type array : array string, array number, array date-time 
{% endapi-method-parameter %}

{% api-method-parameter name="attribute\_3" type="boolean" required=false %}
 The attributes type boolean true or  
{% endapi-method-parameter %}

{% api-method-parameter name="attribute\_2" type="number" required=false %}
 The attributes type number 
{% endapi-method-parameter %}

{% api-method-parameter name="attribute\_1" type="string" required=false %}
 The attributes type string 
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
 item name 
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
 item id 
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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

### A - Attributes input parameters 

| name | data  |  |
| :--- | :--- | :--- |
| attribute 1     | string | "string value" |
| attribute 2 | number | 10000 or 10000.9 or 0.1 |
| attribute 3 | boolean | true or false |
| attribute 4 | datetime | "2020-03-27 05:58:10" . \(yyyy-MM-dd HH:mm:\) |
| attribute 5.1 | array\_string | \["Thor","Caption american", "Iron man"\] |
| attribute 5.2 | array\_number | \[1,2,3\] |
| attribute 5.3 | array\_ | \["2020-03-27 05:58:10","2020-03-27 05:58:11"\] |
| attribute 6 | object | { "key\_string":"xxxx", "key\_number":10000, "key\_datetime":"2020-03-17 00:00:00", "key\_boolean":true } |

### B - Sample import a dynamic item  type 

 **1. API request** 

```http
https://api.cdp.asia/be/item?scope=upsert&portal_id=PORTAL_ID&token=YOUR_&item_type=x
```

### 2. Data  

```bash
[
{
"id":"x1",
"name":"name of x1",
"type":"x",
"attr_number":10000,
"attr_boolean":true,
"attr_datetime":"2020-03-17 23:00:00",
"attr_string":"Description about item x",
"attr_bject":{
"key_string":"xxxx",
"key_number":10000,
"key_datetime":"2020-03-17 00:00:00",
"key_boolean":true
}
}
]
```

