---
description: Track event when user subscribed by email
---

# Email subscribe

Function 

![ Event trigger such as : click to button, submit a form,  ...](.gitbook/assets/1.png)

```javascript
web_event.track("email", "subscrible", {
    extra: {the detail info} // option
});
```

Sample data for event after user has .  

```javascript
web_event.track("email", "subscrible", {
    extra: { 
     "email":"obama@agmail.com"
}
});                                            
```

