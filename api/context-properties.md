---
description: >-
  Properties as device information , ip address, locate, geo, app
  information,...
---

# Context properties

Context is a dictionary of the core information that provides useful context about a datapoint, for example the user’s `ip` address or `locale` or device . Context is a complete and explicit specification, so properties outside the spec are ignored. You should **only use** Context fields for their intended meaning.

| **Field** | **Type** | **Description** |
| :--- | :--- | :--- |
| `app` | Object | Dictionary of information about the current application, containing `name`, `version` and `build`. This is collected automatically from our mobile libraries when possible. |
| `sdk` | Object | Dictionary of information about the current SDK or library containing `name`, `version` and `build`. This is collected automatically from our mobile libraries when possible. |
| `campaign` | Object | Dictionary of information about the campaign that resulted in the API call, containing `name`, `source`, `medium`, `term` and `content, source_prop_id`. This maps directly to the common UTM campaign parameters.`source_prop_id` is relation to the current Insight property.   |
| `device` | Object | Dictionary of information about the device, containing `id`, `manufacturer`, `model`, `name`, `type` and `version`. |
| `ip` | String | Current user’s IP address. |
| `library` | Object | Dictionary of information about the library making the requests to the API, containing `name` and `version`. |
| `locale` | String | Locale string for the current user, for example `en-US`. |
| `geo` | Object | Dictionary of information about the user’s current location, containing `city`, `country`, `latitude`, `longitude`, `region` and `speed`. |
| `network` | Object | Dictionary of information about the current network connection, containing `bluetooth`, `carrier`, `cellular` and `wifi` |
| `os` | Object | Dictionary of information about the operating system, containing `name` and `version` |
| `page` | Object | Dictionary of information about the current page in the browser, containing `hash`, `path`, `referrer`, `search`, `title` and `url`. This is automatically collected by SDK on  insight.js. |
| `navigation` | String | The current navigation path `home`, `categories`, `search`, `detail, thankyou, cart, account,...` |
| `referrer` | Object | Dictionary of information about the way the user was referred to the website or app, containing `type`, `name`, `url` and `link` |
| `screen` | Object | Dictionary of information about the device’s screen, containing `density`, `height` and `width` |
| `timezone` | String | Timezones are sent as tzdata strings to add user timezone information which might be stripped from the timestamp, for example`Asia/Ho_Chi_Minh, America/New_York` |
| `userAgent` | String | User agent of the device making the request |

#### Data structure sample

```text
"context": {
    "app": {
      "name": "InitechGlobal",
      "version": "545",
      "build": "3.0.1.545"
    },
    "sdk": {
      "name": "SDK Analytics V2 on iOS",
      "version": "v2",
      "build": "3.0.1.545"
    },
    "campaign": {
      "source_prop_id": "123456",
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
 
```

