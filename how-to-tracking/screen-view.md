# Screen view

Here you'll send a named screen view to Analytics whenever the user opens or changes screens on your app. Open a ViewController that you would like to track, your code should do the following:

|  **Parameters** |  **Content** |
| :--- | :--- |
| screenName |  String |

 **Example:**

{% tabs %}
{% tab title="Swift" %}
```swift
CDP365Analytic.logEvent(screenName: "HomeViewController")
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
[CDP365Analytic logEventWithScreenName:@"HomeViewController"];
```
{% endtab %}
{% endtabs %}

