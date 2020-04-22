---
description: This sample data structure for post Event data to API
---

# Event structure

Here’s an example of these common fields in raw JSON:

```text
{
  "uid": "97980cfea0067",
  "aid": "7A3CBEA0-BDF5-11E4-8DFC-AA07A5B093DB"",
  "sid": "123456789",
  "ec": "product",
  "ea": "purchase",
  "items":[{
    "type": "product",
	"id":"864115",
	"sku":"5261971730647",
	"quantity":1,
	"brand":"Samsung",
	"seller_id":"12345",
	"price":4500000,
	"category":"Điện tử-Điện lạnh/Tivi/Tivi 4K"
	}
 ],
 "dims": {"shop":{"id":"sh1","name":"Shop HCM"},"warehouse":{"id":"wh1","name":"Kho HCM"}},
 "extra":{
	"order_id":"977895452",
	"revenue":14500000,
	"num_item":4,
	"discount_amount":45000,
	"promotion_code":""
 },
  "context": {
    "app": {
      "name": "InitechGlobal",
      "version": "545",
      "build": "3.0.1.545"
    },
    "campaign": {
      "name": "Email Campaign Loyalty T12",
      "source": "Newsletter",
      "medium": "email",
      "term": "tps reports",
      "content": "image link"
    },
    "device": {
      "id": "B5372DB0-C21E-11E4-8DFC-AA07A5B093DB",
      "advertisingId": "7A3CBEA0-BDF5-11E4-8DFC-AA07A5B093DB",
      "adTrackingEnabled": true,
      "manufacturer": "Apple",
      "model": "iPhone7,2",
      "name": "sudoku's phone",
      "type": "ios" // android,...
    },
    "ip": "8.8.8.8",
    "library": {
      "name": "analytic sdk android",
      "version": "2.11.1"
    },
    "locale": "en-US",
    "geo": {
      "city": "Ho Chi Minh",
      "country": "Viet Nam",
      "latitude": 40.2964197,
      "longitude": -76.9411617
    },
    "network": {
      "bluetooth": false,
      "carrier": "Viettel",
      "cellular": true,
      "wifi": false
    },
    "os": {
      "name": "iPhone OS",
      "version": "8.1.3"
    },
    "page": {
      "path": "/academy/",
      "referrer": "",
      "search": "",
      "title": "Analytics Academy",
      "url": "https://demox.com/academy/"
    },
    "navigation": "thankyou",
    "referrer": {
      "id": "ABCD582CDEFFFF01919",
      "name": "facebook.com",
      "type": "social"
    },
    "screen": {
      "width": 320,
      "height": 568
    },
    "timezone": "Asia/Ho_Chi_Minh",
    "userAgent": "Mozilla/5.0 (iPhone; CPU iPhone OS 9_1 like Mac OS X) AppleWebKit/601.1.46 (KHTML, like Gecko) Version/9.0 Mobile/13B143 Safari/601.1"
  }
 
}
```



