# Screen view

Here you'll send a named screen view to Analytics whenever the user opens or changes screens on your app. Open a ViewController that you would like to track, your code should do the following:

|  **Parameters** |  **Content** |
| :--- | :--- |
| action |  [ITActionEventScreenView](../tracking-event/log-event.md) |
| contentObject | [ Context item](../tracking-parameters/context-param.md) |

 **Example:**

{% tabs %}
{% tab title="Swift" %}
```swift
let contextObject = ITContextObj(screenName: "<Screen Name>")
ITAnalytic.logEvent(action: .ITActionEventScreenView, contextObject: contextObject)
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
ITContextObj *context = [[ITContextObj alloc] initWithScreenName:@"HomeViewController"];
[ITAnalytics logEventWithAction:ITActionEventITActionEventScreenView
contextObject:context extraObject:nil dimsObject:nil itemsObject:nil];
```
{% endtab %}
{% endtabs %}

