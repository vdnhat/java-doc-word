---
description: The reset method only clears the cookies and localStorage set by SDK
---

# Reset anonymous ID

Calling reset resets the user\_id \(uid\) when user sign out and sign in with an other account.

Function

```text
web_event.track("user", "reset_anonymous_id",{
    extra: {the detail info} // option
});
```

Sample 

```text
web_event.track("user", "reset_anonymous_id", {
   extra: { 
      "reset_uid":"864115",
      "generate_uid":"864115_1",
   }
});
```

[  
](https://developers.ants.vn/analytics-v2/user-identify)

