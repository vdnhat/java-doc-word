---
description: >-
  Dims is an array ITDimsObj object of the relation items that provides . You
  should only use Dims types for their intended meaning. And this parameter is
  optional.
---

# Dimension Param

#### Creating an ITDimsObj object <a id="creating-an-itdimsobj-object"></a>

The relation item on events as shop, warehouse, payment method, delivery method,...in this case, you will need to create an Dims object and fill out the dims property:

{% tabs %}
{% tab title="Swift" %}
```swift
let dimsObject = ITDimsObj(itemCategory: <String>, 
itemID: <String>, itemName: <String>)
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
ITDimsObj *dims = [[ITDimsObj alloc] initWithItemCategory:@"category"
itemID:@"item id" itemName:@"item name"];
```
{% endtab %}
{% endtabs %}

#### Dims Properties <a id="dims-properties"></a>

| **Name** |  **Type** |  **Description** |  **Default** |
| :--- | :--- | :--- | :--- |
| itemCategory | String | Category of the item | null |
| itemID | String | Relation item id | null |
| itemName | String | Relation item name | null |

**Example**

For example, if you wanted to set a payment method and warehouse, you would do:Swift

{% tabs %}
{% tab title="Swift" %}
```swift
var dimsList = [ITDimsObj]()
let payment = ITDimsObj(itemCategory: "payment", itemID: "1", itemName: "Online payment")
dimsList.append(payment)
let warehouse = ITDimsObj(itemCategory: "warehouse", itemID: "UHW1", itemName: "HCM city")
dimsList.append(warehouse)

```
{% endtab %}
{% endtabs %}



