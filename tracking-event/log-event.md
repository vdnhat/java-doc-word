# Log Event

Tracks an event. To track an event anywhere in the app, call:

{% tabs %}
{% tab title="Swift" %}
```swift
CDP365Analytic.logEvent(categoryName: <String>, 
                          actionName: <String>,
                               items: <[NSDictionary]>, 
                               extra: <NSDictionary>, 
                           dimension: <[NSDictionary]>)
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
[CDP365Analytic logEventWithCategory:@<String>
                          actionName:@<String>
                                item:@<[NSDictionary]>
                               extra:@<NSDictionary>
                           dimension:@<[NSDictionary]>];
```
{% endtab %}
{% endtabs %}

 **Parameters:**

|  **Parameters** |  **Required?** |  **Description** |
| :--- | :--- | :--- |
| categoryName | Yes | The category of the event you wish to tracking. |
| actionName | Yes | The action of the event you wish to track |
| items | No | Items is a list dictionary. Included infomation such as: User, Product, ... |
| extra | No | Extra is a dictionary  of extra information that provides useful such as e-com properties |
| dimension | No | Dims is a list dictionary  of the relation items that provides . |

