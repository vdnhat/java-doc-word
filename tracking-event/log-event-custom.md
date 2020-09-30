# Log Event Custom

Tracks an event custom. To track an event anywhere in the app, call:

{% tabs %}
{% tab title="Swift" %}
```swift
ITAnalytic.logEventCustom(actionName: <String>, category: <String>)
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
[ITAnalytics logEventCustomWithAction:@"action name"
 category:@"category name"];
```
{% endtab %}
{% endtabs %}

 **Parameters:**

| **Parameters** |  **Required?** |  **Description** |
| :--- | :--- | :--- |
| actionName | Yes | Free text. The name of the event you wish to track |
| category | No | Free text. The category name of the event you wish to track |

