---
description: A dictionary of properties for user lead
---

# User Identify

Trigger and called this function. 

* After a user registers
* After a user logs in
* When a user updates their info \(eg changes or adds a new address\)
* Upon loading any pages that are accessible by a logged in user \(optional\)

## Case 1: Track when page is ready state \(DOMContentLoaded\)

Function 

Using this function when the main script CDP script loaded . Event trigger such as : click to button, submit a form,  ...

```javascript
web_event.track("user", "identify", {
    items: [{user  properties}],
    extra: {the detail info} // option
});
```

Sample data for event after user has .  

```javascript
web_event.track("user", "identify", {
    items: [ 
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
    extra: { 
"id":"864115",
"name":"Barack Obama",
"first_name":"Barack",
"last_name":"Obama",
"phone":"09123456789",
"gender":"male",
"birthday":"1960-12-01",
"email":"obama@agmail.com"
}
});                                            
```



## Case 2: Track on load page .

Function 

Can be able to using this function when the page is on load such as the script has render by server side. 

```javascript
web_event('track', "user", "identify", {
    items: [{user  properties}],
    extra: {the detail info} // option
});
```

Sample data for event after user has .  

```javascript
web_event("track", "user", "identify", {
    items: [ 
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
    extra: { 
"id":"864115",
"name":"Barack Obama",
"first_name":"Barack",
"last_name":"Obama",
"phone":"09123456789",
"gender":"male",
"birthday":"1960-12-01",
"email":"obama@agmail.com"
}
});
```

