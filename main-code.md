---
description: >-
  This is javascript (insight.js) which has included functions for event
  tracking.
---

# Main code

This is pixel code tag \(which is placed in all pages\) is used to track pageview \(\#1\) of all page and is a required component to track other events. Add it to Header for all of the pages of website similar to GA , Facebook pixel.

Default code load will automation track  page view event and context properties.  

```javascript
<!--  Web Insight V2 script -->
<script type = "text/javascript" >
   var _portalId = "PORTAL_ID"; // Your Portal ID 
   var _propId = "PROPERTY_ID"; // Your Website Property ID
(function() {
    var w = window;
    if (w.web_event) return;
    var a = window.web_event = function() {
        a.queue.push(arguments);
    }
    a.propId = _propId;
    a.track = a;
    a.queue = [];
    var e = document.createElement("script");
    e.type = "text/javascript", e.async = !0, e.src = "//st-domain.com/insight.js";
    var t = document.getElementsByTagName("script")[0];
    t.parentNode.insertBefore(e, t)
})(); </script>
<!-- End of Web Insight V2 script -->

```

