---
description: This is the template API for event tracking.
---

# API Event Track

{% api-method method="post" host="http://DOMAIN\_X.com" path="?portal\_id=PORTAL\_ID&prop\_id=INSIGHT\_PROPERTY\_ID&resp\_type=RESPONSE\_TYPE" %}
{% api-method-summary %}
 API Track Event 
{% endapi-method-summary %}

{% api-method-description %}
In more detail these common params for each API call 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="redirect\_url" type="string" required=false %}
When param **resp\_type** is redirect nd event tracking is **click** then redirect\_url should be use.    
{% endapi-method-parameter %}

{% api-method-parameter name="resp\_type" type="string" required=false %}
Support that types: _javascript, json, redirect, pixel_. Default is javascript 
{% endapi-method-parameter %}

{% api-method-parameter name="portal\_id" type="integer" required=true %}
Your business  Account ID on the analytics system.
{% endapi-method-parameter %}

{% api-method-parameter name="prop\_id" type="integer" required=true %}
Your datasources ID on the analytics system such property as of Web , App Android, App IOS, POS,... 
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="context" type="object" required=false %}
Context properties data for events has describe detail bellowing. 
{% endapi-method-parameter %}

{% api-method-parameter name="extra" type="object" required=false %}
Extra properties data for event has described on bellowing  ****
{% endapi-method-parameter %}

{% api-method-parameter name="dims" type="object" required=false %}
The relation items on events as shop, warehouse, payment method, delivery method... 
{% endapi-method-parameter %}

{% api-method-parameter name="items" type="array" required=false %}
List items on events as: products
{% endapi-method-parameter %}

{% api-method-parameter name="ea" type="string" required=true %}
Event action
{% endapi-method-parameter %}

{% api-method-parameter name="ec" type="string" required=true %}
Event category 
{% endapi-method-parameter %}

{% api-method-parameter name="sid" type="integer" required=true %}
Hash any ID your users session on visiting your application and caching on SDK of device. **default expired after 30 minutes** over a session
{% endapi-method-parameter %}

{% api-method-parameter name="aid" type="string" required=true %}
The device advertising ID as: AAID, IDFA 
{% endapi-method-parameter %}

{% api-method-parameter name="uid" type="string" required=true %}
1. You can set to anonymous User ID  
2. On mobile can be able to use the device advertising id **similar** aid as AAID, IDFA . 
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
API successfully retrieved.
{% endapi-method-response-example-description %}

```
_event_callback_data({"dgs":"1576222588%3A3%3A0","au_gt":"1571290715","pv_id":"1576222602739-7","n_client_id":0,"session_id":"6320","n_user":0,"au_id":"7","type":"event","aid":"7","client_id":"7.1558521539","an_session":"zlzgzhzjzdzkzdzizmzkzlzhzhzhzmzrzrzdzgzdzizmzkzlzhzhzhzlzjzhzdzizmzkzlzhzhzhzlzjzhzdzhzdzhzqzdzizd2f27zdzjzdzlzmzlzkzjzd"});
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not found for matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "404 not found"}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

