---
description: >-
  There are pieces of information you know about a user that are included in an
  identify call.
---

# User Identify properties

| **Trait** | **Type** | **Description** |
| :--- | :--- | :--- |
| `address` | String | ddress of a user |
| `avatar` | String | URL to an avatar image for the user |
| `birthday` | String | User’s birthday. format : yyyy-MM-dd |
| `description` | String | Description of the user |
| `email` | String | Email address of a user |
| `first_name` | String | First name of a user |
| `gender` | String | Gender of a user. Sample: male, female |
| `id` | String | Unique ID in your database for a user such as: User Login ID, User Account  |
| `customer_id` | String | Unique ID in your database for a Customer |
| `last_ame` | String | Last name of a user |
| `name` | String | Full name of a user &lt;p&gt; If you only pass a first and last name we’ll automatically fill in the full name for you.&lt;/p&gt; |
| `phone` | String | Phone number of a user |
| `username` | String | User’s username &lt;p&gt; This should be unique to each user, like the usernames of Twitter or GitHub.&lt;/p&gt; |

Here’s an example of these common fields of user identify event in raw JSON:

```text
{ 
"uid":"97980cfea0067",
"aid":"7A3CBEA0-BDF5-11E4-8DFC-AA07A5B093DB",
"sid":"123456789",
"ec":"user",
"ea":"identify",
"items":[ 
{ 
"type":"lead",
"id":"864115",
"name":"Barack Obama",
"first_name":"Barack",
"last_name":"Obama",
"phone":"09123456789",
"gender":"male",
"birthday":"1960-12-01",
"email":"obama@agmail.com"
}
],
"context":{ 
"app":{ 
"name":"InitechGlobal",
"version":"545",
"build":"3.0.1.545"
},
"device":{ 
"id":"B5372DB0-C21E-11E4-8DFC-AA07A5B093DB",
"advertisingId":"7A3CBEA0-BDF5-11E4-8DFC-AA07A5B093DB",
"adTrackingEnabled":true,
"manufacturer":"Apple",
"model":"iPhone7,2",
"name":"sudoku's phone",
"type":"ios"
},
"ip":"8.8.8.8",
"library":{ 
"name":"analytic sdk android",
"version":"2.11.1"
},
"locale":"en-US",
"geo":{ 
"city":"Ho Chi Minh",
"country":"Viet Nam",
"latitude":40.2964197,
"longitude":-76.9411617
},
"network":{ 
"bluetooth":false,
"carrier":"Viettel",
"cellular":true,
"wifi":false
},
"os":{ 
"name":"iPhone OS",
"version":"8.1.3"
},
"page":{ 
"path":"/academy/",
"referrer":"",
"search":"",
"title":"Analytics Academy",
"url":"https://demox.com/academy/"
},
"navigation":"thankyou",
"referrer":{ 
"id":"ABCD582CDEFFFF01919",
"name":"facebook.com",
"type":"social"
},
"screen":{ 
"width":320,
"height":568
},
"timezone":"Asia/Ho_Chi_Minh",
"userAgent":"Mozilla/5.0 (iPhone; CPU iPhone OS 9_1 like Mac OS X) AppleWebKit/601.1.46 (KHTML, like Gecko) Version/9.0 Mobile/13B143 Safari/601.1"
},
"extra":{ 
"id":"864115",
"name":"Barack Obama",
"first_name":"Barack",
"last_name":"Obama",
"phone":"09123456789",
"gender":"male",
"birthday":"1960-12-01",
"email":"obama@agmail.com"
}
}
```



