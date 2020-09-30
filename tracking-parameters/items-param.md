---
description: >-
  Items parameter is a list item object. It represent for two type data:
  ITUserObj or ITProductObj item. And this is an optional parameter.
---

# Items Param

#### Creating an ITProductObj object <a id="creating-an-itproductobj-object"></a>

{% tabs %}
{% tab title="Swift" %}
```swift
let product = ITProductObj(productID: <String>, productName: <String>, 
productDescription: <String>, SKU: <String>, price: <Int>, 
quantity: <Int>, brand: <String>, category: <String>, variant: <String>, 
imageURL: <String>, productURL: <String>, coupon: <String>, 
sellerID: <String>, options: <[ITOptionObj]>)
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
ITProductObj *product = [[ITProductObj alloc] 
initWithProductID:@"product id"
productName:@"product name"
productDescription:@"product description"
SKU:@"sku of the product"
price:price of product
quantity:quantity
brand:@"product brand"
category:@"product category"
variant:@"product variant"
imageURL:@"product image url"
productURL:@"product url"
coupon:@"coupon"
sellerID:@"seller id"
options:list option objects];
```
{% endtab %}
{% endtabs %}

In this case the item is a product item, if has information about color, size,..are available, you will create an ITOptionObj and fill out the option property:

{% tabs %}
{% tab title="Swift" %}
```swift
let option = ITOptionObj(optionName: "option name", 
optionValue: "option value")
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
ITOptionObj *option = [[ITOptionObj alloc] 
initWithOptionName:@"option name" optionValue:@"option value"];
```
{% endtab %}
{% endtabs %}

For example, we has color and size information so you will need create a list option bellow:

{% tabs %}
{% tab title="Swift" %}
```swift
var options = [ITOptionObj]()
let color = ITOptionObj(optionName: "color", optionValue: "blue")
options.append(color)
let size = ITOptionObj(optionName: "size", optionValue: "XS")
options.append(size)
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
NSMutableArray *options = [[NSMutableArray alloc] init];
ITOptionObj *color = [[ITOptionObj alloc] initWithOptionName:@"color" optionValue:@"blue"];
[options addObject:color];
ITOptionObj *size = [[ITOptionObj alloc] initWithOptionName:@"size" optionValue:@"XS"];
[options addObject:size];
```
{% endtab %}
{% endtabs %}

* **Product Property**

| **Name** |  **Type** |  **Description** |  **Default** |
| :--- | :--- | :--- | :--- |
| productID | String | Identify of the product | null |
| productName | String | Name of the product | 0.0 |
| productDescription | String | Description of the product | 0.0 |
| SKU | String | SKU of the product | null |
| price | Int | Price of the product | null |
| quantity | Int | Quantity of a product | 0.0 |
| brand | String | Brand associated with the product | null |
| category | String | Product categories supported to 3 level by '/' \(e.g product category level 1/ category level 2/ category level 3\) | null |
| variant | String | Variant of the product \(e.g Black\) |  |
| imageURL | String | Image url of the product |  |
| productURL | String | URL of the product page |  |
| coupon | String | Coupon code associated with a product |  |
| sellerID | String | ID of seller who offers the product |  |
| itemOption | \[ITOptionObj\] | List item of information about the device's screen, containing density, height and width |  |

#### Creating an ITUserObj object <a id="creating-an-ituserobj-object"></a>

{% tabs %}
{% tab title="Swift" %}
```swift
let user = ITUserObj(userID: <String>, username: <String>, 
firstName: <String>, lastName: <String>, address: <String>, 
avatar: <String>, birthday: <String>, email: <String>, gender: <String>,
phone: <String>, customerID: <String>)
```
{% endtab %}
{% endtabs %}

* **User Property**



| **Name** |  **Type** |  **Description** |  **Default** |
| :--- | :--- | :--- | :--- |
| userID | String | Unique ID in your database for a user such as: User Login ID, User Account | null |
| username | String | User's username. This should be unique to each user, like the username of FB, Google. | null |
| firstName | String | First name of a user | null |
| lastName | String | Last name of a user | null |
| address | String | Address of a user | null |
| avatar | String | URL string avatar image of the user | null |
| birthday | String | User's birthday, format: yyyy-MM-dd | null |
| email | String | Email address of a user | null |
| gender | String | Gender of a user. Ex: male, female | null |
| customerID | String | Unique ID your database for a customer | null |
| phone | String | Phone number of a user  | null |

